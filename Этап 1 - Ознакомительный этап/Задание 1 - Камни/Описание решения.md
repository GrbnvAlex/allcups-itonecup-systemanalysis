# Описание решения

Составители задания сказали, что это задание нужно, только чтобы пользователи свыкнулись с платформой. Поэтому не стал тратить много времени на задание. Открытый список результатов других участников показал, что максимум - это 20 очков силы.

# `Попытка 1` - 18 баллов

Изучил данные о камнях и понял, что первый очевидный претендент на победу - это просто список всех камней без параметров (они не дают бонусов) и без благословений богов:

```json
{
	"gems" : [
		{"Pearl" : {"GodsBlessed" : ["Zeus"]}},
		{"Ruby" : {"GodsBlessed" : ["Zeus", "Gefest"]}},
		{"Berill" : {"GodsBlessed" : ["Aid", "Gefest"], "Necromancy" : true }}, 
		{"Emerald" : {"GodsBlessed" : ["Aid", "Zeus"], "Necromancy" : true }}, 
		{"Amethyst" : {"GodsBlessed" : ["Aid"]}}, 
		{"Sapphire" : {"GodsBlessed" : ["Gefest"]}},
		{"Amber" : {"GodsBlessed" : ["Zeus"]}},
		{"Diamond" : {"GodsBlessed" : ["Gefest"]}},
		{"Onyx" : {"GodsBlessed" : ["Zeus", "Aid", "Gefest"]}}
	]
}
```

Такой вариант дал мне почему-то 18 баллов, вместо 20

# `Попытка 2` - 13 баллов

Что-то не так - подумал я. Попробовал такой вариант (все параметры + без благословений):

```json
{
	"gems" : [
		{"Pearl" : {
			"STR" : 200,
			"GodsBlessed" : ["Zeus"],
			"Necromancy" : true,
			"Weapons" : ["Spear"],
			"Mana" : 10,
			"INT" : 50,
			"Skills" : ["Furious Strike", "Healing"]
		}},
		{"Ruby" : {
			"STR" : 350,
			"GodsBlessed" : ["Zeus", "Gefest"],
			"Necromancy" : true,
			"Weapons" : ["Hummer", "Spear"],
			"Mana" : 50,
			"INT" : 150,
			"Skills" : ["Night Whisper", "Healing"]
		}},
		{"Berill" : {
			"STR" : 250,
			"GodsBlessed" : ["Aid", "Gefest"], 
			"Necromancy" : true,
			"Weapons" : ["Hummer", "Axe"],
			"Mana" : 0,
			"INT" : 30,
			"Skills" : ["Furious Strike", "Night Whisper", "Healing"]
		}}, 
		{"Emerald" : {
			"STR" : 100,
			"GodsBlessed" : ["Aid", "Zeus"], 
			"Necromancy" : true,
			"Weapons" : [],
			"Mana" : 0,
			"INT" : 100,
			"Skills" : ["Furious Strike", "Healing"]
		}}, 
		{"Amethyst" : {
			"STR" : 250,
			"GodsBlessed" : ["Aid"],
			"Necromancy" : true,
			"Weapons" : ["Sword", "Hummer"],
			"Mana" : 0,
			"INT" : 0,
			"Skills" : ["Furious Strike"]
		}}, 
		{"Sapphire" : {
			"STR" : 100,
			"GodsBlessed" : ["Gefest"],
			"Necromancy" : false,
			"Weapons" : ["Hummer"],
			"Mana" : 100,
			"INT" : 50,
			"Skills" : ["Night Whisper"]
		}},
		{"Amber" : {
			"STR" : 50,
			"GodsBlessed" : ["Zeus"],
			"Necromancy" : false,
			"Weapons" : ["Spear"],
			"Mana" : 150,
			"INT" : 150,
			"Skills" : ["Night Whisper", "Healing"]
		}},
		{"Diamond" : {
			"STR" : 100,
			"GodsBlessed" : ["Gefest"],
			"Necromancy" : true,
			"Weapons" : ["Spear", "Axe"],
			"Mana" : 0,
			"INT" : 200,
			"Skills" : ["Furious Strike", "Healing"]
		}},
		{"Onyx" : {
			"STR" : 150,
			"GodsBlessed" : ["Zeus", "Aid", "Gefest"],
			"Necromancy" : true,
			"Weapons" : ["Hummer", "Axe"],
			"Mana" : 0,
			"INT" : 100,
			"Skills" : ["Furious Strike", "Night Whisper"]
		}}
	]
}
```

Этот вариант по какой-то причине дал мне 13 баллов вместо тех же 20

# Вывод

Похоже, система подсчёта баллов барахлит. Поэтому остановился на очевидном решении. Не хотел дальше решать эту задачу оптимизации: задача неинтересная и не имеет отношения к системному анализу

_P.S. кто-то смог набить 24 балла_

![image](https://user-images.githubusercontent.com/26649753/159273947-dc2a23a8-05f3-436a-bdb0-261c798c0eaf.png)

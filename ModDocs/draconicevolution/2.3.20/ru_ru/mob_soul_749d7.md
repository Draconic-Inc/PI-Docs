§align:center
##### §nДуши существ§n

§stack[draconicevolution:mob_soul,1,0,{EntityName:"[Random-Display]"}]{size:92} 

§rule{colour:0x606060,height:3,width:100%,top_pad:0}
Души можно выбить с существ, если убить их оружием с зачарованием "Жнец".

Шанс выпадения крайне низок.
Для враждебных существ шанс составляет 1 к 1000, а для нейтральных существ 1 к 800 (можно изменить в конфиге), но это только для оружия Виверны.
Шанс можно увеличить с помощью зачарования "Жнец".

DE tools essentially have a built-in reaper modifier equivalent to reaper lvl 1 for Wyvern, lvl 2 for Draconic and lvl 3 for the Staff of Power.
The calculation to figure out your drop chance is the base drop chance divided by the weapons built in reaper modifier plus the reaper enchant lvl.

So the calculation for say.. A Draconic sword with reaper 5 would be as follows,
built-in modifier = 2,
reaper lvl = 5,
drop chance = 1000 / (2 + 5)

Result: Drop chance is 1 in 142

If the reaper modifier is 0 (so a non-DE weapon without the reaper enchant) there is 0 chance of getting a soul.

Some mods may implement the reaper modifier on their weapons but as of the time of writing this, I do not know of any that do.


The main use for a mob soul is setting the spawn type for a Stabilized spawner but they can also be used to spawn their respective entity by shift right clicking on a block with a soul (Doing this consumes the soul)

§rule{colour:0x606060,height:3,width:100%,top_pad:0}
§recipe[draconicevolution:mob_soul]{spacing:2}
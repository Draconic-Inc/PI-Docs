§align:center
# __MC Markdown__
#### *Reference*
§rule[height:2,colour:#990000]
This document is meant to serve as a reference and a demonstration of the MC Markdown element's capabilities.

MC Markdown is a custom version of markdown designed specifically for minecraft. 
This markdown language works with the modular gui system n Brandon's Core and is the base data format used by Project Intelligence.

§align:left 
#### Basics ##################################################################################################################################################################
§rule[height:2,colour:#990000,top_padding:0]
Before we get started its worth noting that this system uses the select symbol "\§" to designate formatting and element flags. 
Normally when the parser finds this symbol it will consume it and attempt to read what comes after it as ether a formatting flag or an element tag.
To avoid this you can "escape" the sysbol by placing a backslash \ in front of it.

###### Formatting: ##############################
§rule[height:1,colour:#0,top_padding:0]
This system supports most of the usual markdown formatting flags.
Normal formatting codes using *, ~ and _ can also be escaped with \ but the \ is not hidden so ignore it in the bellow examples.

Minecraft formatting codes using \§ can also be used.
However it should be noted that unlike vanilla the font renderer used by this system toggles the formate state when ever it encounters a formatting code. 
This means you can §lactivate and deactivate§l a formatting flag without having to reset the the entire font renderer via the reset \§r flag.

\*Italic\* OR §oI
*Italic*

\*\*Bold\*\* OR §lB
**Bold**

\_\_Underline\_\_ OR \§n
__Underline__

\~\~Strikethrough\~\~ OR \§m
~~Strikethrough~~

\~\?\~Obfuscated\~\?\~ OR \§k
~?~Obfuscated~?~

###### Colour: ##############################
§rule[height:1,colour:#0,top_padding:0]
Colours can be applied via the vanilla formatting codes.
§0\§0 Black            §1\§1 Dark Blue         
§2\§2 Dark Green    §3\§3 Dark Aqua
§4\§4 Dark Red       §5\§5 Dark Purple
§6\§6 Gold             §7\§7 Gray
§8\§8 Dark Gray      §9\§9 Blue
§a\§a Green           §b\§b Aqua
§c\§c Red              §d\§d Light Purple
§e\§e Yellow           §f\§f White

You can also set the base colour for a paragraph using the \§colour[] tag.
For example.

\§colour[#FF0000]
§colour[#FF0000]
Will set the base colour of the following paragraph to red.
It should be noted that this only sets the colour of the next full line of markdown. The colour will reset on the next line.

The colour tag accepts ether a hex value that starts with ether # or 0x or comma separated red,green,blue values.

###### Headings: ##############################
§rule[height:1,colour:#0,top_padding:0]
Headings in this system are identical to regular markdown headings.

 # Heading 1              OR ====== (under heading text)
# Heading 1
 ## Heading 2             OR ------ (under heading text)
## Heading 2
 ### Heading 3
### Heading 3
 #### Heading4
#### Heading4
 ##### Heading 5
##### Heading 5
 ###### Heading 6
###### Heading 6

###### Alignment: ##############################
§rule[height:1,colour:#0,top_padding:0]
Page alignment can be set using the \§align flag.
Valid alignments are:
§3\§align:left
§align:center
§3\§align:center
§align:right
§3\§align:right
§align:left
The align tag will apply its alignment to all following content until the next align tag.

###### Rules: ##############################
§rule[height:1,colour:#0,top_padding:0]
Used to draw a horizontal line on the screen. Similar to normal markdown rules but a lot more flexible. 

Tag Format:
§3\§rule[parameter:value,parameter2:value,parameter3:value]
Parameters:
§3colour§3            
 - Sets the colour of the rule. Takes that same colour format as the colour tag.
§3align§3              
 - Overrides the alignment if the rule. 
§3width§3              
 - Sets the width of the rule. Takes ether an exact width in pixels with the px extension. Or a percentage value that is a percentage of the screen width. Default value: 100%
§3height§3             
 - sets the height of the rule. Default: 5
§3top_padding§3      
 - Adds padding to the top of the rule. Default: 5
§3bottom_padding§3  
 - Adds padding to the bottom of the rule. Default: 5

Rules can also be used as precise spacers by setting the height to 0 and using the padding value to adjust the height.

Some example rules
\§rule[]
§rule[]
\§rule[height:1,colour:#0,top_padding:0]
§rule[height:1,colour:#0,top_padding:0]
\§rule[height:10,colour:#FF0000,top_padding:0,width:100px]
§rule[height:10,colour:#FF0000,top_padding:0,width:100px]
\§rule[height:1,colour:#00FF00,top_padding:0,width:50%,align:center]
§rule[height:1,colour:#00FF00,top_padding:0,width:50%,align:center]

####   Advanced ##################################################################################################################################################################
§rule[height:2,colour:#990000,top_padding:0]
§entity[player:brandon3055]{size:1,scale:20,x_offset:6,y_offset:-8,track_mouse:true}§entity[player:covers1624]{size:1,scale:20,x_offset:120,y_offset:-8,track_mouse:true}
Now that all of the basic boring stuff is out of the way we can get to the fancy stuff!
The following tags allow you to add minecraft related content such as recipes, stacks and entity renderers.

###### Links: ##############################
§rule[height:1,colour:#0,top_padding:0]
The functionality of links will depend on the gui this markdown is being written for. 
For example in Project intelligence links can ether link to a web page or to another documentation page.
The link format is as follows.

§3\§link[target]
Or
§3\§link[target]{parameter:value,parameter2:value,parameter3:value}

There are 3 types of link. 
Basic Text link:
§3\§link[http://www.google.com]
§link[http://www.google.com]
§3\§link[http://www.google.com]{alt_text:"Link with alternate text and hover text",hover:"Some hover text"}
§link[http://www.google.com]{alt_text:"Link with alternate text and hover text",hover:"Some hover text"}

Button Link. This link renderes like a vanilla button.
§3\§link[http://www.google.com]{render:vanilla}
§link[http://www.google.com]{render:vanilla}

§3\§link[http://www.google.com]{render:vanilla,alt_text:"All sides padded",padding:5} 
§3\§link[http://www.google.com]{render:vanilla,alt_text:"Left Padding",left_pad:20} 
§3\§link[http://www.google.com]{render:vanilla,alt_text:"Right Padding",right_pad:20} 
§3\§link[http://www.google.com]{render:vanilla,alt_text:"Top Padding",top_pad:10} 
§3\§link[http://www.google.com]{render:vanilla,alt_text:"Bottom Padding",bottom_pad:10} 
§link[http://www.google.com]{render:vanilla,alt_text:"All sides padded",padding:5} §link[http://www.google.com]{render:vanilla,alt_text:"Left Padding",left_pad:20} §link[http://www.google.com]{render:vanilla,alt_text:"Right Padding",right_pad:20} §link[http://www.google.com]{render:vanilla,alt_text:"Top Padding",top_pad:10} §link[http://www.google.com]{render:vanilla,alt_text:"Bottom Padding",bottom_pad:10} 

Solid Button Link. This link renderes as a solid bordered rectangle.
Supports the same padding and alt text parameters as the vanilla button style link.
§3\§link[http://www.google.com]{render:solid,alt_text:"Solid Button",padding:5} 
§3\§link[http://www.google.com]{render:solid,alt_text:"Solid Button",padding:5,fill_colour:#FF0000,fill_colour_hover:#00FF00}  
§3\§link[http://www.google.com]{render:solid,alt_text:"Solid Button",padding:5,border_colour:#FF0000,b_colour_hover:#00FF00}
§link[http://www.google.com]{render:solid,alt_text:"Solid Button",padding:5} §link[http://www.google.com]{render:solid,alt_text:"Solid Button",padding:5,fill_colour:#FF0000,fill_colour_hover:#00FF00} §link[http://www.google.com]{render:solid,alt_text:"Solid Button",padding:5,border_colour:#FF0000,b_colour_hover:#00FF00}

###### Images: ##############################
§rule[height:1,colour:#0,top_padding:0]
Allowed you to render an image from the internet on the screen. Once downloaded for the first time the image will be cached locally.
Depending on the gui this markdown is written for the image may also act as a link/button.
The image format is as follows.

§3\§img[url]
or
§3\§img[url]{parameter:value,parameter2:value,parameter3:value}

You can apply padding to the image using the padding parameters:
padding, left_pad, right_pad, top_pad, bottom_pad
You can then colour the padded area using 
border_colour and border_colour_hover

You can also adjust the width and/or the height. If you only adjust one the other will be adjusted to maintain the same aspect ratio.
Width and height allow exact sizes in the following format 512px or a size relative to the window size e.g. 50%

Examples:
§3\§img[http://ss.brandon3055.com/htpbbti.png]{width:128px} 
§3\§img[http://ss.brandon3055.com/htpbbti.png]{width:128px,padding:5,border_colour:#000000,border_colour_hover:#00FF00}
§img[http://ss.brandon3055.com/htpbbti.png]{width:128px} §img[http://ss.brandon3055.com/htpbbti.png]{width:128px,padding:5,border_colour:#000000,border_colour_hover:#00FF00}

###### Stacks: ##############################
§rule[height:1,colour:#0,top_padding:0]
The \§stack tag allows you to render an item stack on the page. The format is as follows.
§3\§stack[stackString]
Or
§3\§stack[stackString]{parameter:value,parameter2:value,parameter3:value}

Parameters:
§3size§3            
 - Sets size of the stack.
§3draw_slot§3              
 - If set to true there will be an inventory slot rendered behind the stack.
§3draw_hover§3              
 - Can be used to disable the stack hover text (tool tip)
§3alt_hover§3             
 - Can be used to set alternate hover text for the stack.

Stack string format is as follows:
§3minecraft:stone         §3Or
§3minecraft:stone,64      §3Or
§3minecraft:stone,64,3    §3Or
§3minecraft:stone,64,3,{NBT} 
The first number is the stack size and the second is the damage value.

Examples:
\§stack[minecraft:stone] 
\§stack[minecraft:gold_block]{draw_slot:true} 
\§stack[minecraft:gold_block]{draw_slot:true,size:32} 
\§stack[minecraft:diamond_sword,1,0,{ench:[0:{lvl:1s,id:18s}]}]{draw_slot:true,size:32}
§stack[minecraft:stone] §stack[minecraft:gold_block]{draw_slot:true} §stack[minecraft:gold_block]{draw_slot:true,size:32} §stack[minecraft:diamond_sword,1,0,{ench:[0:{lvl:1s,id:18s}]}]{draw_slot:true,size:32}

###### Recipes: ##############################
§rule[height:1,colour:#0,top_padding:0]
The recipe tag allows you to render all of the crafting recipe's for an item on the page. 
Recipe's are similar to images in that they allow you to add a border around them but you can not adjust their size.
The format for the border/padding and colour is identical to images.

The recipe format is as follows.
§3\§recipe[stackString]
Or
§3\recipe[stackString]{parameter:value,parameter2:value,parameter3:value}

Examples:
§3\§recipe[minecraft:iron_ingot]{padding:10,border_colour:0xc6c6c6}
§recipe[minecraft:iron_ingot]{padding:10,border_colour:0xc6c6c6}

§3\§recipe[minecraft:lingering_potion,1,0,{Potion:"minecraft:long_slowness"}]{padding:10,border_colour:0xc6c6c6}
§recipe[minecraft:lingering_potion,1,0,{Potion:"minecraft:long_slowness"}]{padding:10,border_colour:0xc6c6c6}

###### Entities: ##############################
§rule[height:1,colour:#0,top_padding:0]
The entity tag allows you to render entities on the page.
This tag allows you to render almost any entity including players on the page.

The entity format is as follows.
§3\§entity[entityString]
Or
§3\§entity[entityString]{parameter:value,parameter2:value,parameter3:value}

Parameters:
§3size§3            
 - Sets size of the entity renderer.
§3scale§3              
 - Sets the scale of the entity relative to the size of the renderer. Default: 1
§3x_offset,y_offset§3              
 - Allows you to adjust the position of the entity.
§3hover§3             
 - Can be used to set hover text for the entity.
§3track_mouse§3            
 - When true the entity will track the cursor on the screen.
§3draw_name§3             
 - Only applicable to players. Renders the players username.
§3main_hand,off_hand,head,chest,legs,boots§3             
 - Allows you to set the entities equipment.
§3rotate_speed§3             
 - Entity rotation speed. Default 1. Can be negative to reverse rotation.
§3rotation§3
 - The entities rotation if rotate_speed is set to 0.             

§3\§entity[player:brandon3055] 
§3\§entity[player:covers1624]{track_mouse:true} 
§3\§entity[minecraft:pig]{rotate_speed:0}
§entity[player:brandon3055] §entity[player:covers1624]{track_mouse:true} §entity[minecraft:pig]{rotate_speed:0}

§3\§entity[player:brandon3055]{size:128,track_mouse:true,hover:"This is the creator of this mod!",main_hand:"minecraft:diamond_sword,1,0,{ench:[0:{lvl:1s,id:18s}]}",off_hand:"minecraft:shield,1,0,{ench:[0:{lvl:1s,id:70s}]}",chest:"minecraft:diamond_chestplate,1,0,{ench:[0:{lvl:1s,id:3s}]}"}


§entity[player:brandon3055]{draw_name:true,size:128,track_mouse:true,hover:"This is the creator of this mod!",main_hand:"minecraft:diamond_sword,1,0,{ench:[0:{lvl:1s,id:18s}]}",off_hand:"minecraft:shield,1,0,{ench:[0:{lvl:1s,id:70s}]}",chest:"minecraft:diamond_chestplate,1,0,{ench:[0:{lvl:1s,id:3s}]}"}

§link[URL]{alt_text:Reload}

###### Tables: ##############################
§rule[height:1,colour:#0,top_padding:0]
\§table[parameter:value,parameter2:value,parameter3:value]
<Heading row> (optional)
<Delimiter>
<Content row>
<Content row>
<Content row>

Parameters:
§3width§3            
 - Sets the total width of the table. Default is 100% but also accepts an exact Npx value
§3align§3              
 - Sets horizontal alignment of cells in the table. Accepts left, center or right Default: left
§3vertical_align§3              
 - Sets vertical alignment of cells in the table. Accepts top, middle or bottom Default: top
§3cell_colour§3              
 - Sets the colour of the table cell's Accepts hex value starting with # or 0x, Or seperate r,g,b values. 
§3heading_colour§3              
 - Sets the background colour of the table's heading cell's Accepts hex value starting with # or 0x, Or seperate r,g,b values. 
§3render§3              
 - Allows the cell boxes to be disabled so the table can be used to simply align elements.
 
Delimiter:
The delimiter is what defines the number of columns, the width and alignment of each column.

Example delimiter:
| :-- | :---: | -----: |

First lets take a look a the dashes - these specify the width of each column.
You can use any number of dashes in each column and the width of each column is determined but comparing its number against the total.
In the example i use a total of 10 dashes which makes it very simple to figure out the width of each column. They are just 20%, 30% and 50% of the total width of the table.

The colon's set the column alignment. A single colon on the left is left align, no colon or colon on both left and right is center align and a single colon on the right is right align. 

You can also specify an exact fixed width for the columns like so. 
| :n64 | :---: | -----: |

Adding a content line above the delimiter as in the following example makes that line a heading line.

§table[heading_colour:0x8200ff,aligh:right]
| §bHeading 1 | §bHeading 2 | §bHeading 3 |
| :- | :--: | ---: |
| §img[http://ss.brandon3055.com/r892cfh.png]{width:100%} | Content 2 | Content 3 |
| Content 4 | Content 5 | Content 6 |
| Content 7 | Content 8 This is a long table item that will make the table wrap to multiple lines | Content 9 |
| Content 10 | Content 11 | Content 12 §link[http://www.google.com.au] |

§table[width:80%,align:center,cell_colour:0xFF0000,vertical_align:middle]
| :n83 | :--: | ---: |
| §img[http://ss.brandon3055.com/r892cfh.png]{width:80px} | Content 2 | Content 3 |

§table[]
| :n64 | :n128: | n128 |  
| §img[http://ss.brandon3055.com/r892cfh.png]{width:64px} | Content 2 | Content 3 |

Table Demonstration
§table[vertical_align:middle]
| User | Description |
| :n50: | :- |
| §entity[player:brandon3055]{size:50,scale:0.9,track_mouse:true} | The creator of Draconic Evolution. |
| §entity[player:covers1624]{size:50,scale:0.9,track_mouse:true} | The maintainer of ALL THE MODS! No literally all of them! |
| §entity[player:TheRealp455w0rd]{size:50,scale:0.9,track_mouse:true} | Never tell anyone your password! |

Table Used to align items Demonstration
§table[render:false,vertical_align:middle]
| :n50: | :- |
| §entity[player:brandon3055]{size:50,scale:0.9,track_mouse:true} | The creator of Draconic Evolution. |
| §entity[player:covers1624]{size:50,scale:0.9,track_mouse:true} | The maintainer of ALL THE MODS! No literally all of them! |
| §entity[player:TheRealp455w0rd]{size:50,scale:0.9,track_mouse:true} | Never tell anyone your password! |





§entity[player:covers1624]{size:300,scale:0.9,track_mouse:false,rotate_speed:0}
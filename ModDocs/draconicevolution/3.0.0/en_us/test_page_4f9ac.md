§align:center
§stack[draconicevolution:overworld_draconium_ore]{size:32,draw_slot:true,tooltip:"test\nTool\nTip"} §stack[draconicevolution:draconium_dust]{size:32,draw_slot:true} §stack[draconicevolution:draconium_ingot]{size:32,draw_slot:true} §stack[draconicevolution:draconium_block]{size:32,draw_slot:true}
 

§entity[player:covers1624]{size:64,track_mouse:false} §entity[player:covers1624]{size:64,track_mouse:true}
§entity[player:covers1624]{size:64,tooltip:"This is covers!",track_mouse:true,draw_name:true,main_hand:"draconicevolution:chaotic_staff,1,0,{}"} §entity[player:covers1624]{size:64,rotate_speed:0.0,rotation:45} §entity[player:covers1624]{size:64,draw_name:true,rotate_speed:1.0,chest:"draconicevolution:chaotic_chestpiece,1,0,{Damage:0}"} 

§entity[minecraft:pig]{size:18} 






A Test String This Is A Test String This Is A Test String This Is A Test String This Is A Test String This Is A Test String This Is A Test String This Is A Test String This Is A Test String This Is A Test String This Is A Test String This Is A Test String This Is A Test String

TODO Texty Scale

§rule{colour:0xFF0000,border_colour:0x00FFFF,height:5,padding:2,width:100%}



§align:center

#### Basic Markdown Table
§table{width:100%,colour:0x0,border_colour:0xffffff,heading_colour:0xff0000,vert_align:middle,padding:2,render_cells:true}
| No.	| ###### Description 	| ###### Tag 																						|
| :n25: 	| :-------------------- 		| :n80: 																								|
| 1		| Stone Block 			| §stack[minecraft:stone]{size:18} 																	|
| 2		| A Pig 					| §entity[minecraft:pig]{size:18,rotate_speed:1}  														|
| 3		| An Image 				| §img[http://ss.brandon3055.com/045f1]{border_colour:0x0,border_colour_hover:0x0,width:100%}	|
| 4		| A link 					| §link[www.googe.com]{colour:0xE0E0E0,colour_hover:0xFFFFA0,padding:3,link_style:vanilla}		|

#### Similar table using xml format
This allows per row or per cell colour and alignment customization... Oh yea. and Tables in Tables! in Tables! in Tables! in Tables! in .....

§table{width:100%,colour:0x0,border_colour:0xffffff,heading_colour:0xff0000,render_cells:true} 
<table column_layout="25,1*,80">
<tr padding="3,0,0,0" align="middle center" colour="0xFF00FF">
	<td>No.</td>   
	<td>###### Description </td> 
	<td>###### Tag</td>
</tr>
<tr padding="2" align="middle">
	<td align="center">1</td>
	<td>Stone Block</td>
	<td align="center">§stack[minecraft:stone]{size:18} </td>
</tr>
<tr padding="2" align="middle">
	<td align="center">2</td>
	<td>A Pig</td> 
	<td align="center" padding="2">§entity[minecraft:pig]{size:18,rotate_speed:1}</td> 
</tr>
<tr padding="2" align="middle">
	<td align="center">3</td>
	<td colour="0xFF9040">An Image</td> 
	<td align="center" padding="2">§img[http://ss.brandon3055.com/045f1]{border_colour:0x0,border_colour_hover:0x0,width:100%}</td>
</tr>
<tr padding="2" align="middle">	
	<td align="center" colour="0xFFFF00">4</td>
	<td>A Link! (Finally!)</td>
	<td align="center" padding="2">§link[www.googe.com]{colour:0xE0E0E0,colour_hover:0xFFFFA0,padding:3,link_style:vanilla}</td>
</tr>
</table> 

§table{width:100%,colour:0x0,border_colour:0xffffff,heading_colour:0xff0000,render_cells:true} 
<table column_layout="25,1*,80">
<tr padding="3,0,0,0" align="middle center" colour="0xFF0000">
	<td>No.</td>   
	<td>###### Description </td> 
	<td>###### Tag</td>
</tr>
<tr padding="2" align="middle">
	<td align="center">1</td>
	<td>Stone Block</td>
	<td align="center">§stack[minecraft:stone]{size:18} </td>
</tr>
<tr padding="2" align="middle">
	<td align="center">2</td>
	<td>A Pig</td> 
	<td align="center" padding="2">§entity[minecraft:pig]{size:18,rotate_speed:1}</td> 
</tr>
<tr padding="2" align="middle">
	<td align="center">3</td>
	<td>An Image</td> 
	<td align="center" padding="2">§img[http://ss.brandon3055.com/045f1]{border_colour:0x0,border_colour_hover:0x0,width:100%}</td>
</tr>
<tr padding="2" align="middle">
	<td align="center" colour="0xFF0000">4</td>
	<td>
		So...... Yea.... This is a thing now....
		§table{width:100%,colour:0x0,border_colour:0xffffff,heading_colour:0x00FF00,render_cells:true} 
		<table column_layout="25,1*,80">
		<tr padding="3,0,0,0" align="middle center" colour="0x00FF00">
			<td>No.</td>   
			<td>###### Description </td> 
			<td>###### Tag</td>
		</tr>
		<tr padding="2" align="middle">
			<td align="center">1</td>
			<td colour="0x505050">Stone Block</td>
			<td align="center">§stack[minecraft:stone]{size:18} </td>
		</tr>
		<tr padding="2" align="middle">
			<td align="center">2</td>
			<td>A Pig</td> 
			<td align="center" padding="2">§entity[minecraft:pig]{size:18,rotate_speed:1}</td> 
		</tr>
		<tr padding="2" align="middle">
			<td align="center">3</td>
			<td>An Image</td> 
			<td align="center" padding="2">§img[http://ss.brandon3055.com/045f1]{border_colour:0x0,border_colour_hover:0x0,width:100%}</td>
		</tr>
		<tr padding="2" align="middle">
			<td align="center" colour="0x00FF00">4</td>
			<td>
				So...... Yea.... This is a thing now....
				§table{width:100%,colour:0x0,border_colour:0xffffff,heading_colour:0xff0000,render_cells:true} 
				<table column_layout="25,1*,80">
				<tr padding="3,0,0,0" align="middle center" colour="0x0000FF">
					<td>No.</td>   
					<td colour="0x00FFFF">###### Description </td> 
					<td>###### Tag</td>
				</tr>
				<tr padding="2" align="middle">
					<td align="center">1</td>
					<td>Stone Block</td>
					<td align="center">§stack[minecraft:stone]{size:18} </td>
				</tr>
				<tr padding="2" align="middle">
					<td align="center">2</td>
					<td>A Pig</td> 
					<td align="center" padding="2">§entity[minecraft:pig]{size:18,rotate_speed:1}</td> 
				</tr>
				<tr padding="2" align="middle">
					<td align="center">3</td>
					<td colour="0x4090FF">An Image</td> 
					<td align="center" padding="2">§img[http://ss.brandon3055.com/045f1]{border_colour:0x0,border_colour_hover:0x0,width:100%}</td>
				</tr>
				<tr padding="2" align="middle">
					<td align="center" colour="0x0000FF">4</td>
					<td>
						So...... Yea.... This is a thing now....
						§table{width:100%,colour:0x0,border_colour:0xffffff,heading_colour:0xff0000,render_cells:true} 
						<table column_layout="25,1*,80">
						<tr padding="3,0,0,0" align="middle center" colour="0xFF00FF">
							<td>No.</td>   
							<td>###### Description </td> 
							<td>###### Tag</td>
						</tr>
						<tr padding="2" align="middle">
							<td align="center">1</td>
							<td>Stone Block</td>
							<td align="center">§stack[minecraft:stone]{size:18} </td>
						</tr>
						<tr padding="2" align="middle">
							<td align="center">2</td>
							<td>A Pig</td> 
							<td align="center" padding="2">§entity[minecraft:pig]{size:18,rotate_speed:1}</td> 
						</tr>
						<tr padding="2" align="middle">
							<td align="center">3</td>
							<td colour="0xFF9040">An Image</td> 
							<td align="center" padding="2">§img[http://ss.brandon3055.com/045f1]{border_colour:0x0,border_colour_hover:0x0,width:100%}</td>
						</tr>
						<tr padding="2" align="middle">
							<td align="center" colour="0xFFFF00">4</td>
							<td>A Link! (Finally!)</td>
							<td align="center" padding="2">§link[www.googe.com]{colour:0xE0E0E0,colour_hover:0xFFFFA0,padding:3,link_style:vanilla}</td>
						</tr>
						</table> 
					</td>
					<td align="center" padding="2">§link[www.googe.com]{colour:0xE0E0E0,colour_hover:0xFFFFA0,padding:3,link_style:vanilla}</td>
				</tr>
				</table>
			</td> 
			<td align="center" padding="2">§link[www.googe.com]{colour:0xE0E0E0,colour_hover:0xFFFFA0,padding:3,link_style:vanilla}</td>
		</tr>
		</table>
	</td>
	<td align="center" padding="2">§link[www.googe.com]{colour:0xE0E0E0,colour_hover:0xFFFFA0,padding:3,link_style:vanilla}</td>
</tr>
</table>


§entity[draconicevolution:chaosguardian]{tooltip:"This is Brandon",y_offset:80,track_mouse:false,scale:64,draw_name:true,rotate_speed:1,size:1,main_hand:"draconicevolution:draconic_staff_of_power,1,0,{Energy:47940608,ToolProfile:1b,Profile_0:{showDigAOE:0b,digDepth:0,digSpeed:100,aoeSafeMode:0b,digAOE:2,attackAOE:2.0d,junkNbtSens:1b,enableJunkFilter:1b},Profile_1:{showDigAOE:0b,digDepth:0,digSpeed:100,aoeSafeMode:0b,digAOE:0,attackAOE:2.0d,junkNbtSens:1b,enableJunkFilter:1b}}",off_hand:minecraft:shield} 

§img[http://ss.brandon3055.com/c9982]{width:40%,tooltip:"Its A Kitty!!!!!",link_to:"www.google.com"}

§rule{colour:0xFF0000,border_colour:0x00FFFF,height:5,padding:2,width:100%}

This is an §link[amod:some_page]{tooltip:"A Tool Tip!",colour:0x4444FF,colour_hover:0xFF69B4,alt_text:In Line} link!

§link[www.google.com]{tooltip:"A Tool Tip!",colour:0x4444FF,colour_hover:0xFF69B4,alt_text:This is a very long link that should wrap to the next line} 

§link[www.test.com]{colour:0xE0E0E0,colour_hover:0xFFFFA0,link_style:vanilla,padding:4,alt_text:This is a very long link that should wrap to the next line}

§colour[0xffffcc] 
§link[http://test.com]{colour:0x303030,colour_hover:0x303030,border_colour:0xFFFFFF,border_colour_hover:0x00FF00,padding:5,link_style:solid,alt_text:This is a very long link that should wrap to the next line}

§recipe[draconicevolution:crafting_injector,1,3]{spacing:4}
§recipe[minecraft:lingering_potion,1,0,{Potion:"minecraft:harming"}]{spacing:4}
§recipe[computercraft:disk_expanded,1,0,{color:1118481}]{spacing:4}

# §nHeading 1ds
Some Randome Text sd sdsd sd  sd

Heading 1


Heading 2

## Heading 2

### Heading 3

#### Heading 4

##### Heading 5

###### Heading 6

#### §nStyle Colour Test§n

§0BLACK§0
§1DARK_BLUE§1
§2DARK_GREEN§2
§3DARK_AQUA§3
§4DARK_RED§4
§5DARK_PURPLE§5
§6GOLD§6
§7GRAY§7
§8DARK_GRAY§8
§9BLUE§9
§aGREEN§a
§bAQUA§b
§cRED§c
§dLIGHT_PURPLE§d
§eYELLOW§e
§fWHITE§f
§kOBFUSCATED§k
§lBOLD§l
§mSTRIKETHROUGH§m
§nUNDERLINE§n
§oITALIC§o



Testing 123 §0BLACK§0 Testing 456
Testing 123 §1DARK_BLUE§1 Testing 456
Testing 123 §2DARK_GREEN§2 Testing 456
Testing 123 §3DARK_AQUA§3 Testing 456
Testing 123 §4§nDARK_RED§4§n Testing 456
Testing 123 §5§lDARK_PURPLE§l§5 Testing 456
Testing 123 §6GOLD§6 Testing 456
§colour[0xff6600]
Testing 123 §7GRAY§7 Testing 456
Testing 123 §8DARK_GRAY§8 Testing 456
Testing 123 §9BLUE§9 Testing 456
Testing 123 §aGREEN§a Testing 456
Testing 123 §bAQUA§b Testing 456
Testing 123 §cRED§c Testing 456
Testing 123 §dLIGHT_PURPLE§d Testing 456
Testing 123 §eYELLOW§e Testing 456
Testing 123 §fWHITE§f Testing 456
Testing 123 §kOBFUSCATED§k Testing 456
Testing 123 §lBOLD§l Testing 456
Testing 123 §mSTRIKETHROUGH§m Testing 456
Testing 123 §nUNDERLINE§n Testing 456
Testing 123 §oITALIC§o Testing 456


Lorem ipsum dolor sit amet, §lconsectetur adipiscing elit. In a porta eros, §n§4vitae aliquam§4§n elit§l. Vivamus sapien §nnisi, convallis vitae varius sit amet, suscipit vitae neque. Curabitur§n ut enim volutpat ante §oconsectetur lacinia quis non elit. Nam volutpat, diam in porta ullamcorper, arcu§o tortor mattis nunc, non tempor sapien orci.

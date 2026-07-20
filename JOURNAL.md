# July 4: Basic concept understanding, and working on the cad.
I have seen several other implementations of Stewart's platforms, however, all of them seemed to not nesecarily be super robust or able to take any decent payload. I want to make something that is able to have a generic payload adapter (similar to my previous gimbal project). I will look at another design for a base and try to work out how I can best increase the robustness and usability.

<img width="294" height="227" alt="{7708621C-4849-4F1F-8B9E-15CF98B89B5D}" src="https://github.com/user-attachments/assets/581963b7-62c6-4814-a5ff-5bd724736706" />

Above is the image that I am taking inspiration from. The design that they implemented is very simple, but you are able to see how everything works so I am going to use it as a base for my project.

I also had the recommendation from a friend to use mg996r servos for anything where any amount of load is being moved. I also concidered other servos, but looking around, the price to performance of the servos that he recommended are just best. They are also semi-frequently sold in packs of 6

Servo sourcing plan (cheap, good reviews, and 6 pack)

https://www.amazon.com/KEAcvise-Packs-mg996r-servo-Motor/dp/B0FGP9ZPJN

I am now going to figure out how closely I can logically package the servos into the base. The goal is a more compact base for easy adaptation in the future.

<img width="687" height="453" alt="{B584B507-7369-4E37-B5E9-1328EBD415F6}" src="https://github.com/user-attachments/assets/50c2aded-6e9b-47e8-8f5e-815fc70063ed" />

Above is what I came up with. It should be noted that the servos are sticking out, this is worst case clearance here to ensure they will fit well. There is also a plan to later integrate a 9 dof imu into the top of the case for later control improvements. (space is being left in the container so they will fit internally, to make later modification easier)

<img width="398" height="340" alt="{6741CD3E-74F1-46A1-B29D-13A477A4EEA9}" src="https://github.com/user-attachments/assets/d15fe689-a5e9-4a8c-9a68-d7575e41608d" />

This is what it looks like stood up. I notice that the 3 little walls (which will be bearing a decent amount of load) are really thin, and it is making me nervous, so I will ensure there are more layers for that to be a little more rigid in the future.

<img width="420" height="289" alt="{BA7941BE-7033-4282-A654-466BBA05E55F}" src="https://github.com/user-attachments/assets/975c78fa-ab65-47f5-a97a-21547d6edaf8" />

I added the bottom screw holes (above). They look a bit weird, but I believe that this will be sufficient. If not, I have a rediculous amount of petg and can just reprint the part until its good enough. The plan will be to have the second (top) screw couples on the top element/top case. This is mainly to be easier to print without fail. I need to first make a way for the top of this to attach however.

<img width="435" height="325" alt="{ADCCC9FD-2649-416B-894D-74BAC281DD39}" src="https://github.com/user-attachments/assets/dc94013b-801f-4e09-8d82-f52c004a736d" />

I added mounting holes for the top onto the walls that have less load on them to ballance it out. I also added a passthrough with some slight printing optimizations to the side to allow the power and possibly a control cable to be run through the side of the model.

<img width="432" height="309" alt="{3E43B1B1-DBBC-4251-BCD3-43D21B207348}" src="https://github.com/user-attachments/assets/35935e05-1092-4614-a15e-a1f83c508707" />

Like I said, I was nervous about the thickness of these little walls so I have added these wedge things in order to improve the rigidity. I will have to account for them in the design of the top of this, as they are going right up to the edge of the wall. Anyway, I will now put everything together in the main assembly how it is to see how the packaging is looking.

<img width="515" height="388" alt="{264E91C8-03C2-4743-A8B0-B292043C7E27}" src="https://github.com/user-attachments/assets/b1c7c0a7-a0ae-4e83-b52e-91ec7fa54901" />

I think it looks decent, I will continue with designing the top. I also see that with how I want to mount the servos, that they are going to require free space at the top of the model for their cables, this is unfortunate. I should also note that I am planning to use the left over m3 screws that I have from the Potatomatic project to assemble this in order to save costs.

<img width="444" height="341" alt="{C7A08C58-994B-41CB-BDE0-317925B3F584}" src="https://github.com/user-attachments/assets/e3dd7e4e-7a9c-4aaf-9def-b3f7cfcf922e" />

Here is a rough concept of the top plate.

<img width="475" height="351" alt="{55CF6593-B2A6-4264-8C56-0BE5EBFA97F7}" src="https://github.com/user-attachments/assets/633300ee-3d50-47ea-87fb-2e8d05fe062d" />

And here it is in the main assembly.

<img width="391" height="194" alt="{2EB23810-CFFF-498B-9FF3-BDC86DFFC4B5}" src="https://github.com/user-attachments/assets/593d9bbe-952f-4d4e-b914-a445e6705a84" />

Looking at where the servo attaches, it seems it will be nessecary for me to drop down the plate a little more for it to be thick enough on the bottom. I will also need to raise it roughly a millimeter on the top for more material there as well. It sucks that there is no way to print this that makes it so that the screw isnt going to be splitting the layers apart.

<img width="384" height="264" alt="{193AC73F-C306-4EBB-A3E5-E983F9CDB948}" src="https://github.com/user-attachments/assets/83e2f307-0682-451f-8221-bd57ab24e726" />

I have now polished the part.

<img width="337" height="254" alt="{ACE63CB6-6EF3-4794-8CF9-CCE3B20B8174}" src="https://github.com/user-attachments/assets/83910207-7a7e-4f1d-bc42-ac6367813595" />

The screw holes for the servos are now properly in place and have sufficient thickness in the places where it's needed.

<img width="478" height="376" alt="{DC22E7E0-B3A2-44E5-8347-32755850A53D}" src="https://github.com/user-attachments/assets/957169c0-e7cb-46af-842b-eec306910307" />

This is the overall look now. I will next move onto the part of designing the control arms, but I first want to do a little bit of research to figure out how the length/other factors changes the behaviour.

https://raw.org/research/inverse-kinematics-of-a-stewart-platform/

I found this awesome website, with a super awesome article detailing the inverse kinematics, not only this, it allowed me to easily tweak the settings of the control arms and driving rod lengths. This gave valuable insight, as I now understand how the length effects it. I spent about 10 minutes looking a little bit into their code (which I understood none of :sob:) as well as playing with the length of the control arms.  From looking at it. the only effect that they really have is the range of motion that your platform has. For example, short control arms means you are only able to move your platform a little bit, but the lack of precision of the servos is accounted for a little bit better, and with longer ones, any error of the servos is amplified but you get decently larger range of motion. I also noticed if they are too long, they are able to collide with eachother. So next, I am going to find step files for the servo horns, and model a control arm that maximizes the achievable positions of the system.

<img width="310" height="286" alt="{CC1C07BD-DBCB-4EA6-AB8A-6E77BAE61B1C}" src="https://github.com/user-attachments/assets/5f791651-739b-435b-8018-1eb668a55832" />

Hmmmmm... those are going to collide at this size....
Luckily I made everything intent driven, so it will simply be changing a few numbers to change everything. Still sucks though.

<img width="560" height="424" alt="{1E59FDD9-F150-4E86-BC50-04DC1E2669FB}" src="https://github.com/user-attachments/assets/e1cd78e4-a989-48ac-8ffd-a86c432f2a17" />

Fusion is testing my pacience. It broke the entire model for the base, I spent a bit fixing that. Some of the geometry sketches for the mounting holes were constrained wrongly when they were copied between the sketches, and a lot of them just decided they want to fail to compute. Then, after fixing all of the base, I tried updating the model just to see the damage, and was greeted with this wonderful piece of modern artwork (slop) that I will now have to spend my time fixing. Delightful!

<img width="428" height="322" alt="{CC3863F8-A4AC-4C55-9D65-8D3235942493}" src="https://github.com/user-attachments/assets/7e1db747-0ee0-4526-bcc3-a7a32252f542" />

I will first fix this top plate, then reconstrain everything again. For me this feels less overwhelming then fixing a ton of small errors.

<img width="580" height="361" alt="{464E0E61-C5F8-4216-B478-98CCD330A679}" src="https://github.com/user-attachments/assets/c5b0fe2a-edce-4309-8c18-dfbe59b7e422" />

Intent driven for the win :100: I love intent driven :heart:

The top was much easier to fix since I did everything properly. It was changing about 4 numbers between 2 sketches and everything was all good. I will now re insert and joint all of the servos together.

I also verified that the servos have the required range of motion, they seem to be 360 which is not standard for these servos to my understanding.

<img width="312" height="254" alt="{35CF77CF-9B23-4C36-8AD6-604776D82AB0}" src="https://github.com/user-attachments/assets/68f3fc06-49b9-4c58-b9fb-240b28755bd3" />

I now have all of the things put on there.

<img width="448" height="325" alt="{0F38C60F-6E5E-4631-A7CB-6289051E86CA}" src="https://github.com/user-attachments/assets/9913210d-3c53-4550-915a-9404a5165fb9" />

Here is the hole that the servo horn is going to get put on.

<img width="372" height="292" alt="{7766989E-C96C-4622-A41C-EEDB0266B852}" src="https://github.com/user-attachments/assets/8cc73bae-bf56-4184-b5a8-8673476b8f0a" />

I realized I forgot the way to screw it in, this is what I came up with. The m3 screw that is included will be too short, so I am going to replace it with one of my own, longer ones. I may also improve this geometry, but my printer is probably too crap for it to matter anyway.

<img width="489" height="112" alt="{7359E234-FEF2-4035-8B6E-4F17F7F43342}" src="https://github.com/user-attachments/assets/9f63026c-ede0-4373-8aa7-83e1d008d1d2" />

I made the arm a little thinner, it was really thick, and it will be in petg so I know the strength is not going to be an issue.

<img width="419" height="231" alt="{42FDEA49-88B1-4488-A795-8FD30214A6F2}" src="https://github.com/user-attachments/assets/cdaac48a-ed82-4e23-a56d-8a9b3b2235a4" />

I have continued to optimize this for the control rod attachment, I made sure that the fixtures will attach as best as possible. I am still a little unsure of how it will all end up factoring together, so I will try and make the push rods next just to see what they are going to look like roughly.

<img width="432" height="390" alt="{0284CCE8-381B-44F2-9D7C-2662C3E2D7CF}" src="https://github.com/user-attachments/assets/68293eee-038b-458a-bf43-25bdb2c31e8f" />

Man...... these pushrods are really thin aren't they.....
Im sure it wont be a problem

https://www.amazon.com/HobbyPark-Adjustable-Connector-Pushrods-Replacement/dp/B08CBSWMR5/141-2591928-2634929?psc=1

Above are the pushrods that I am intending to get btw. I also had to learn how to use the sweep tool to make them in fusion :sob:

<img width="396" height="317" alt="{E34BBB38-DA87-4670-9158-C333024C7C63}" src="https://github.com/user-attachments/assets/4a601bb5-5c5f-46b4-8cea-2587b3f65aeb" />

I may end up shortening the control rods in real life if they aren't rigid enough. They look like they will fail fast honestly. I also worry that once they are bent, that they aren't going to be easy to unbend and get working again.

Sorry for big dev log today. It is currently the next day actually, so this is technically multiple days of work.

I also made a bom, this was a few days ago when I was still planning the rough idea of the project out, but it is still unlogged work.

https://docs.google.com/document/d/1bmJ8n-eDoXSdFWSxfQN4pvn6DaG_fgnzeeZT4vmXuGE/edit?usp=sharing

** Total time spent: 5.9 hours **

# July 5: Working on the top payload, and kinematics/code
I speant the first 40 minutes today working on the top platform that the plate will be attached to. I still dont know for sure what I am going to do for the plate, it will have to be something transparent to make use cases like bouncing a ping pong ball easier.

<img width="577" height="586" alt="{D2C29C5F-D418-43F5-B01C-BD269D2E2E26}" src="https://github.com/user-attachments/assets/4f85f356-755c-4a4d-8f5d-00aecca3bc61" />

Above is the image of what that looks like in the overall design. I cant decide if I am going to bend the push rods like shown, or if I am going to take advantage of the link things that come in the kit of them. The kit isnt super clear about their size so I dont know how to cad for them without having that. I have a place to either bend the wire or put a bolt, depending on what I end up doing.

Youtube of cad, stopped trying lapse because it NEVER works. Sorry for 1x speed, and weird aspect ratio (peak framework).
https://www.youtube.com/watch?v=UD7uxmYwpVk

I will now look into how I can implement the kinematics engine into python.

For working on the kinematics, I need to first get some of the main parameters for the control, those are: horn length, rod length, base radius and base raduis outer, platform radius, platform radius outer, shaft distance, anchor distance. (disclosure: I am getting help from Gemini to understand the kinematics, as well as refferencing the stewart.js from the web demo I talked about yesterday. I don't understand a majority of the math so I am seeking LLM assistance, everything else I will be writing myself.)

Here are the values I have measured from my model (note: all in mm)

```python
horn_length = 82.50
rod_length = 169.00
base_radius = 97.342
base_radius_outer = 90.00
platform_radius = 81.293
platform_radius_outer = 123.198
shaft_distance = 30.00
anchor_distance = 112.50
```

Horn length: 

<img width="584" height="404" alt="{3A344BA8-43A7-4DE4-A1C0-9EBD12153CDD}" src="https://github.com/user-attachments/assets/d5237ab2-3c31-46b6-9f30-276773e2750d" />

Rod length:

<img width="413" height="391" alt="{7ADF7757-6D76-44C3-9E2A-94BBC2EA63F2}" src="https://github.com/user-attachments/assets/a8f5d37a-6e18-4fe2-bda5-3daf377c146c" />

Base Radius:

<img width="367" height="220" alt="{16644CE8-8193-4C16-9567-7A8AE65D8448}" src="https://github.com/user-attachments/assets/dea46089-aadb-47bf-9c0c-01bafdfa5c0b" />

<img width="409" height="242" alt="{168CA614-B971-422A-B4B4-20F02DB826A6}" src="https://github.com/user-attachments/assets/2e9855af-7d12-488c-ae78-6cb3885957d7" />

Base Radius (outer):

<img width="307" height="308" alt="{52B913E2-7397-4D8C-B3CC-4CA2CCBF47E9}" src="https://github.com/user-attachments/assets/d7ce6dd8-8cc1-487c-b0a1-a53fa2ae6f38" />

Platform Radius:

<img width="601" height="321" alt="{A6326FF2-A38A-445D-87B1-B7B76F02757F}" src="https://github.com/user-attachments/assets/19b48dd3-7902-4bc5-a66a-8a226e381cdb" />

Platform Radius (outer):

<img width="630" height="391" alt="{00A32B14-F5F0-42A4-81A5-427C9D99E484}" src="https://github.com/user-attachments/assets/b0406d7a-98f8-4cf0-9c7d-853a7651199d" />

Shaft Distance:

<img width="614" height="340" alt="{BF8E1D49-5830-47E3-A02E-939B34D53DE6}" src="https://github.com/user-attachments/assets/9cb5975e-de63-4540-9b6f-4003e0dacc36" />


Anchor Distance:

<img width="661" height="396" alt="{696FCF2E-CB64-4703-B590-D0A17781D279}" src="https://github.com/user-attachments/assets/51bfdd78-3381-48c8-a979-d103f40d6099" />

Now that I have these measurements, I am going to boot back into Linux where my development environment is, and work on the rest of the programming. I want to make a TKinter control GUI, and basic easy to control kinematics. I plan to also look into how difficult a 3d preview of the movements would be. I also need to write the firmware for the esp32 that it will be controlling. The idea is to have the code run mainly on the laptop, and use the lan to connect to the esp32 and issue the servo angles. All kinematics will be done in the desktop companion app for simplicity.

I spent about 2 more hours working on the code for the project, this simple tkinter gui was super obnoxious to make. I just need to add jump to position, position validity verification, connection logic and piping the position to the kinematics so the commands can be sent and this project will largely be completed. Overall, I think that this is not the most complicated part of the gui and that a lot more time is going to need to be spent in order to complete this. Namely, the connection is something that is going to take a while. I most likely will want to do something websocket based running on the esp32, and some of light feedback in it for better control. I am not sure yet. I also want to add a 3d visualizer to the gui, similar to the one website that I found the stewart.js library from. Overall, with what was done today I know that there is still a lot more to come. In the end, this is a code heavy project rather than hardware heavy (hence me doing t3).

<img width="1920" height="1080" alt="2026-07-06_03-51" src="https://github.com/user-attachments/assets/f1ca95d7-6b03-4a4d-8bb1-097fbc2b9ea1" />

Note: yes, it's open in antigravity, but thats bc its the only ide I have configured with everything on this machine (other than FRC VSCode which is missing hackatime). The hackatime project is stewartcontroller, I tried to share it, but it says "anyone with the link can view it" but I litteraly cant find a public link anywhere. The only link I see has /my/ which I know won't work on another machine, if it did, so many duplicates would have to exist. I will assume it being public is enough for whoever is reviewing the project. Lmk if there is anything else that I need to do. I did also get some help with small syntax errors from ChatGPT and other missuses of tkinter, bc honestly this is my first time in a while not just fully vibe coding the interface, I have forgotten most of even the basic stuff unfortunately. I used to be good at this :sob:

** Total Time Spent: 3.5 hours **

# July 19: Finishing code, finalizing for ship
After finishing getting distracted by the FTC premier event and working on a new drivebase for next year, I finally have gone back to this project to get it finished and out of the way. I also need the 12v supply this project will fund over other things, so I am trying to get this shipped asap. I know Forge is against AI firmware, but I dont really know cpp so I had to get some help from gemini. I used it to assist with basic usage of the apis I needed to host a wireless network and parse json in order to control this project effectively.

I ended up finishing it up, and it looks something like this:

<img width="910" height="318" alt="2026-07-19_20-15" src="https://github.com/user-attachments/assets/a2dedd41-e7a8-4378-bf11-031b556905c8" />

Litteraly just accepting a json object of the positions and sending the pwm signal to each of the servos in order to set their position.

I also had some assistance from gemini in order to create a visualization of the platform:

<img width="1446" height="1274" alt="2026-07-19_20-19" src="https://github.com/user-attachments/assets/27fbdd24-c77a-4db8-9fc2-adbb0edfcb34" />

I have kept it so that the code is less than 30% written by ai, though of the 70% of my code about 50% of it was written with assistance (asking how to use apis in context, but implemnting myself) (all of this is just as a disclosure)

I will now boot back into windows and begin work on assembly, wiring, and other finalization to meet the requirements. I will also copy the code from the other repository that I made accidentally to here.

<img width="927" height="158" alt="{FB7F5493-3F80-4C67-B9E0-88EF0DA67D7C}" src="https://github.com/user-attachments/assets/61f05b40-1754-431d-b7f8-36a9cf7a3eb9" />

I have made the bom.csv (above). it should be noted that the 12v and buck are nessecary rather than just a 5v, as the power supply is needed to save another Forge project I can't complete since the power supply unfortunately was fried. (This is to fix Potatomatic)

I have also exported all of the cad in the requested format as well as stl for easier printing of the project. Its all in the `cad/` folder of the repo. I will next complete the assembly guides and wiring diagrams.

Here is the finished assmebly guide and wiring diagram combo:

https://docs.google.com/presentation/d/1fX6R6pKFSlhVpZevY7VcBayyEp1o772PA0JAKRDqIYo/edit?usp=sharing

Finally, I made an image in sketchpad for the repo banner and forge banner.

<img width="2880" height="1754" alt="{38EFED0E-58FD-4C1D-82DD-88AE67AA784D}" src="https://github.com/user-attachments/assets/6bb6452a-1c89-4a95-89e6-df86fca28339" />

I then put together the readme file, finalized everything to meet the forge shipping requirements, all of this took a little over 30 minutes however I was waiting for a render for part of that time that I will not count. I ended up scrapping that render and using the one from the assembly guide anyway.

<img width="504" height="189" alt="{5F63E4D0-7F8A-474A-ABB6-F0F511B82756}" src="https://github.com/user-attachments/assets/6c8645bf-8227-4db0-9cb7-f7f7680885d3" />

I will now update this journal one final time and submit the project for review!

Hackatime: 
<img width="140" height="78" alt="2026-07-19_20-33" src="https://github.com/user-attachments/assets/d168e142-2e99-43d6-8902-5cea8a0115b2" />

** Total time spent: 2.6 hours **

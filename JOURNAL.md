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

** Total time spent: 4.9 hours **

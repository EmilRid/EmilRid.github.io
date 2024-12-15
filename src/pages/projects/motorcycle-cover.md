---
layout: "../../layouts/BlogLayout.astro"

date: "2024-12-15"
title: "Motorcycle Cover"
---

## Motorcycle Cover
In the summer of 2022, [my brother](https://nicolo.se)'s friend had asked him if I per chance could 3d print something for him. It was a motorcycle cover because the one on the left side of their motorcycle was absent. As it was a identical to the one of the left, he thought that maybe it was possible to recreate it and only have to flip it make it fit on the right side. I felt confident that this would be possible, therefore I set out to do it.
![Left side of motorcycle](/motorcycle-cover/1.jpg)

My first idea was to recreate it in CAD (Computer Aided Design) in Fusion 360. I started by creating an object that you could mould into different shapes. Slowly though, I noticed that the motorcycle cover had many different angled and slopes that I, with only experience in modeling conventionally, would not be able to recreate.

I had to find another solution. I came up with the idea that I could scan the part with my phone, process the images and then have the 3D files to 3D print and paint. But my first scan did not go very well. As you could see, there were many imperfections. I spent a while trying to use [Blender](https://www.blender.org) in order to smooth out these imperfections with different tools and also reduce the vertice count. In the end I realized that I had to scan it again.
![First scan](/motorcycle-cover/2.mov)

The second scan I tried to take better pictures with better lighting. After the images had finished processing into a 3D model I dragged them into blender. Then again the quality was still not good, the edges were uneven and the surfaces weren't smooth like the one in real life.

I started searching for solutions online and what I found out was that when 3D scanning you want a lot of edges and shapes for the 3D scanning to register and be able to track. Then you also want a surface that reflects as little light as possible so therefore I applied this new knowledge to my third attempt.
![Taped motorcycle cover](/motorcycle-cover/3.jpg)

This scan went way better. As my "client" only needed the outer surface of the cover to match the real one, I didn't need to make the inside perfect or accurate. Therefore I smoothed out the inside so that it then would be easier to manufacture later.
![Third scan](/motorcycle-cover/4.mov)

Although this was much better, I didn't trust that the shape of the cover was accurate enough compared to the real one. I felt that I needed a small prototype to see if it was any good. Using [Slic3r](https://slic3r.org) I resized it down to a minimally viable size to be able to compare the shape and then I also mirrored it because I'm making the left side, not the right. Later when making the real size it would be too big and also too difficult to print in one go on my [Creality Ender 3](https://www.creality.com/products/ender-3-3d-printer), therefore splitting it into multiple pieces would be the only solution. To practice this I did the same with the prototype. After I was done splitting the model into pieces, I put each one in a slicer called [Ultimaker Cura](https://ultimaker.com/software/ultimaker-cura/) that would convert the .stl files into .gcode files that contain instructions for how my 3D printed needs to move and place plastic.
![Printing piece of prototype](/motorcycle-cover/5.jpg)
![Lower piece of prototype cover](/motorcycle-cover/6.jpg)

After a some more printing I had this. Although tiny it was very significant as it gave me an idea for how the finished motorcycle cover would turn out. Now it was time to do it for real.
![Complete prototype cover](/motorcycle-cover/7.jpg)

I started by splitting the motorcycle cover into even more pieces because now the model was bigger and real size. I made each piece easy to print with the cut edge on the build plate so that it made adequate contact with my surface. Then in put them in the slicer and generated the instructions and paths for my 3D printer. Then it was off to the printer to make the parts.
![A couple of pieces and support](/motorcycle-cover/8.jpg)
![Taped pieces of cover](/motorcycle-cover/9.jpg)
![Bow of the cover printed](/motorcycle-cover/10.jpg)

As you could see in the previous pictures, the pieces were way bigger. Even a single piece was bigger than the first prototype and each one took many hours to print, the biggest of which taking almost 10 hours 😴. Then It came to gluing the pieces together and that was actually more difficult than I expected. First I needed the correct glue which wasn't very difficult to find. Then I needed to secure the pieces into place and put pressure to adjacent pieces which was difficult when the motorcycle cover wasn't an ordinary shape. I glued one piece at a time and strangely enough the pieces didn't line up properly but with a clamp I could line up the edges to give a "smooth" alignment. Although as you can see, after all of the gluing, the pieces had very visible edges. This was caused by an artifact in 3D printing called [Elephant's foot](https://runebrush.pa-sy.com/wp-content/uploads/2023/09/elephants-foot-example.png) where the base of the print is seemingly squashed outwards and therefore the base becomes wider than the rest of the part. Another issue I had was that my 3D printed randomly had [line shifting](https://us2.dh-cdn.net/uploads/db5587/original/3X/7/3/73dbe780dc8c474494a63b905279ac8eed50b45c.jpeg) happen in the middle of the print which made me have to stop it, remove and sand the shifted edge and continue the rest of the piece in another try. That's why there are some big pieces (correct size) and smaller pieces (incorrect size). This was the end result of all the gluing.
![Glued cover](/motorcycle-cover/11.jpg)

After a lot and I mean a lot of sanding and reapplying glue to the bonds, the cover looked way better. It didn't look as if it was 3D printed. I later sanded away the glue so that the bonds wouldn't be too apparent.
![Glued and sanded cover](/motorcycle-cover/12.jpg)

And this was the result! 🥳
After a couple of layers of black paint, it looked new. I was happy with this result and my "client" was happy with the result. The bonds weren't too obvious and it still looked better than the original piece. It was difficult to get the paint surface good enough because it's easy to accidentally get drops or orange peel looking surface but with a bit of sanding and reapplying paint it mostly fixed these issues. 
![Both covers](/motorcycle-cover/13.jpg)
![Both covers with hand for scale](/motorcycle-cover/14.jpg)

Here are both covers on the motorcycle, the left being the old one and the right being the new one.
![left side of motorcycle](/motorcycle-cover/15.jpg)
![right side of motorcycle](/motorcycle-cover/16.jpg)

I felt happy with these results but as any other engineer, there are always things to improve. One thing being the bonds are still visible although I did a lot of sanding. Maybe this will always be an issue when putting together many pieces into a single part. I could otherwise have put a paste over the whole cover and then sanded, hiding the bonds and creating a smoother surface. 

Another thing is that I feel like the part is slightly smaller than the original piece from some angles. What I should have done was take a few thin slices in both x and y and print them. Then I would be able to compare the measurement to the original and rescale my model to the correct size.

Lastly, I feel like the use of PLA as filament material was incorrect, I should have used something else such as ABS instead. This is because PLA has a glass transition temperature of around 60 degrees celscius which means that it will start becoming pliable at that temperature. It isn't until around 180 degrees celscius that the PLA actually starts melting. The reason why I think this could become an issue is because the cover is fully black, close to hot parts on the motorcycle and usually in direct sunlight. It was when I was outside spraypainting the cover when checking if the paint had dried that when in the sun the cover got pretty warm. ABS has a higher galss transition temperature of around 105 degrees celsius which is why a lot of car parts are made in ABS. The issue here instead is that it shrinks a procent or two when printing which makes it more difficult to use as uneven heating could cause it to warp. With a housing around the printer this defect could be circumvented but that is a whole other process to make. 

Thank you for reading to the end. 😊

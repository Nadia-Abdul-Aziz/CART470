# Weekly Project Reflection

## Exploring Second Life

The majority of this week consisted of laying the groundwork for the project prior to its official start.

The first thing we did as a group was visit the Second Life gallery together. We understand that Second Life is an integral part of Skawennati’s work, although she has directly expressed her desire for the AbTeC Gallery to exist as a standalone entity. As we explored the platform, we identified several shortcomings, some of which may be intentional, and took notes on our observations as we went.

## Discussing Our Roles

We also had an open discussion as a group about our individual skills and what each of us would be willing to contribute to the project. Despite having worked together in the past, this gave us an opportunity to better understand one another’s strengths and interests in the context of this project.

Personally, I noted that I would be willing to contribute to anything related to 3D integration, as well as potentially MetaSounds of Fmod integration alongside Jeremy if opportunities for sound work arise.

## Cultural Considerations

I have worked with Skawennati’s work in the past, as I played a role in integrating her Tree of Life into ELEKTRA’s EVM gallery. However, some of my teammates had never encountered her work before or had limited experience with Indigenous artwork.

As a group, we acknowledged the importance of approaching the project carefully and remaining attentive to cultural considerations, particularly by following Skawennati’s guidance throughout the process.

## Establishing Communication with AbTeC

Alex and I visited Skawennati spontaneously at the AbTeC offices on the 11th floor on Wednesday afternoon. We spoke with her and Arijit about setting up a meeting and establishing the necessary communication pipelines with the AbTeC team.

I sent the initial email to Arijit, with all team members CC’d, to confirm our meeting for the morning of the 23rd. This process also contributes to the team developing professional communication practices, such as using “Reply All” appropriately and remaining attentive to response times.

## Researching Similar Projects

Additionally, we explored projects with similar goals to those outlined in the brief, namely games like Big Walk that we would like to consult for accesibility features, and other VR games. We concluded that ELEKTRA’s EVM shares several similarities with what we are being asked to develop.

Through my personal contacts, I reached out to EVM’s developer, and we will be setting up a meeting shortly. This should provide valuable insight into the technical and design considerations involved in building a prototype similar to the one described in the brief.

## Weekly Reflection

Overall, this week was heavily focused on reflection, research, and preparation. As a group, we spent considerable time discussing the intentions and possibilities of the project while establishing the groundwork necessary to move forward.

However, many of our assumptions and potential directions remain preliminary until we are able to speak directly with the AbTeC team and better understand their needs and expectations.

# September 29th Project Reflection

## The Meeting

During class, we had a meeting with Nancy and Arijit only as Skawenatti could not make it. The meeting lasted around an hour as we explored Second Life once again as Nancy went over her primary concerns. I have detailed the majority of these concerns in the living learning contract under the "knowledge scope" tag. They have a rather broad view of the project and are not dead set on any elements, all they know is Second Life has too many limitations and is dated. They are not married to any particular aesthetic or building either, so we have a great degree of creative freedom not only in visuals but also in mechanics to address issues like text readability. The final goal is not necessarily to have a publishable gallery, but to have a usable prototype the staff can build upon. Non-negotiables are a viable blender-engine pipeline, a robust sound solution, and clean modular capabilities to move artworks around. Accessibility is of utmost concern, notably in UI/UX, VR availability, and distribution.  

## Work

The consensus that we came to is to firstly decide the engine, they would like a prototype in all engines, and we will be splitting the load based on our skillset as such:

Jeremy & Bea: Godot

Alex & Ryan: Unity

Nadia: Unreal

Nancy's requirements were pretty low; simply have a navigable environment with the gallery building and Skawenatti's Tree of Life. It did not need to have any interactivity at all, but we proposed to have the text interactivity done and potentially some other interactions of our choosing. 

We will be making web builds and Windows builds where possible, and despite disagreeing with the notion of creating a less accessible platform, we will make a VR build. Whoever has time for it, will get to it. 

This engine exploration is to be able to speak on the speed and ease of use of these platforms, we have all agreed Unreal will look good and realistic the fastest, Godot is suitable for custom toolsets and is open source, and Unity is a good all-rounder. 

## 3D files & Privacy Concerns
The 3D models we recieved are intellectual property of AbTeC and proposed some privacy concerns. We recieved the models from Arijit via email to all team members.
We expressed following the meeting that we had a public repository for this class, and needed to clarify if this was a concern. Nancy stated that ideally, as we are dealing with copyrighted assets and files, they would be more comfortable if the files were not easily accessible through the Github pages. We have set up a private repository in lieu of public, and as such, while Sabine will be a co-owner of the repo, it will not be accessible to anyone else.

## Work done

I think we are all procrastinating a tiny bit, and while I can't speak for the others, I believe little progress has been made on the Unity and Godot side as well. I have...created the project...okay no a little more than that. I have compiled a list of tutorials to follow in the next few days to slowly but surely build this prototype for the meeting, and I currently have a landscape with a first person cntroller with some vegetation. There really isn't much to show for yet, but the development has begun. I ran some tests with text popups for interactivity as well. 

## LLC

The Living Learning Contract was written majoritarily by myself and Jeremy, with the rest of the team filling in their respective sections. The contract first describes all the information we gathered from the meeting as factual information we must all abide by, to ensure we are all on the same page. While the project is broad and we cannot outline week-to-week responsibilities, we did outline what we need to do for the meeting on the 8th, all subsequent task management will be done via the Kanban Fizzy page. See Below:

https://github.com/Nadia-Abdul-Aziz/CART470/blob/main/LivingLearningContract_ABTEC.pdf

We all ensured to remain humble about our starting knowledge and skills as well as being flexible on the roles we may end up taking on. We designated a section where all members can directly state this information, along with their hopes for the project.

We all looked over the document together via our group chat before submitting.

## Weekly Reflection

Overall, this week marked the start of the work to be done, with absolute clarity on the project, our tasks, access to all the necessary materials, and impending expectations from the AbTeC team. 
# Weekly Reflection - Oct 7

This would have been the heaviest week of the month as we believed our meeting with Skawenatti would have been on Thursday, but due to its postponement, a large chunk of the work was done, but a lot was still left to do. 

## Blender

I opened the Blender file simply out of curiosity, as multiple members of the team mentioned missing meshes, overlapping faces and general malaise when importing assets. I was not expecting to rebuild the structure, I was expecting to need to remedy some quick fixes to optimize the models for game engines. What I discovered, was topology that was not game-ready and non-modular. The blend file received from Nancy and Arijit, presented the following:

- Triangulated faces that cut into each other
- Layered vertices (Faces were duplicated upon themselves)
- Unnecessary and unorganized subdivisions
- Flipped normals
- Meshes with no thickness (planes instead of geometry)
- no discernable UVs 

The team claimed that the files we were being sent were modularized and in progress of being modernized. That said, despite that not holding true, we understand that Second Life does not give headaches about 3D models, and pretty much anything goes, so their perspective on the files was rather shallow, but that is what we are here for. 

Thus, I worked on creating a fully modular building kit. 

Each floor was rebuilt with proper quad topology and laid out at the Blender origin for easy manipulation. Each floor had two versions, one plain and one with raised sides for aesthetics. Some pieces were also given holes to accommodate for the tree or other artworks. 

The spheres were rebuilt with the proper solidification and normals.

Instead of recreating the walls, I opted for a tileset system.

That said, the user can create a curve as they desire and array the tiles along that curve, this allows for endless possibilities and design without needing to manually extrude the wall. The design flow of the kit consists of the builder choosing their floor arrangements, laying them as they wish at origin, choose their desired wall design, and creating the walls along their structure, or anywhere they please. 

This is a huge improvement as it is a robust solution to their modularity concerns that allows them to experiment with design, space and aesthetics, and generates game-ready assets with clean UVs for texturing and automatic in-engine optimization

I spent a few hours recreating the second life buildings using the kit, and the team response was very positive when used in engine. I also experimented with alternative designs using the flexible wall making capabilities, such as an installation arrangement I could present to show the possibilities of the kit.

## UE5

Due to my time spent on the Blender file, my UE by this point was crude. I opened up the first person template, and deleted everything I did not need, so I possessed the following:

- Walking, sprinting, jumping
  
- Hand animations
  
- Sky sphere
  
- Landscape/floor

That said, all the basic navigation was essentially in-built for me and I did not need to do any work past get rid of extras and modify these existing parameters.

For the class check-in, I prepared a basic audio controller, it is nothing special but it shows how easy it is to implement audio in a robust fashion to sync with an animation. Walking sounds were triggered through a metasounds blueprint with exposure to all other project blueprints. In the animation sequencer, I was able to insert audio tags to trigger the randomized (for realism) walking sounds.

I also began preparing a proposed solution for text viewing, as bio readability was a huge issue in Second Life. I proposed a podium with a proximity sensor that would pop up an interact widget upon approaching it. The interact prompt would then be used by pressing "I" to trigger the full bio text widget while blurring the background behind the text.

The last thing I had comp;leted by this point was the UE5 foliage scatter system. I placed various types of foliage on the terrain for several reasons

1. To emulate the natural outdoor environment of Second Life
   
3. To have a hardware stressor for the demo to monitor FPS and tech accessibility of the platform

The foliage models I selected all had in-built material modifiers that caused them to move in the wind automatically, which is an extra computation task for UE5 to render, thus becoming a valuable test.

The UE5 needed to be finished by the time we met with AbTeC and this was nowhere near finished, thus, lots of work still needed to be done.

## Unity Troubles

I am not officially on the Unity project, but I am familiar with the platform and available as an extra hand as needed. When Alex attempted to pull the file sent over from Ryan, he was met with a multiutude of compiler errors, causing the project to refuse to open with the exception of in safe mode. Everything was fine on Ryan's end when the file was sent, so there was a lot of confusion and frustration. 

I was tasked with figuring out the solution after Alex managed to pull from github itself (which presented its own issues). The cause of the issue remains undefined, but the errors originated from poorly compiled packages upon import. That said, the fix was to delete the compile data and cache from the C files, forcing unity to reinstall and compile all packages to run the program. In doing so, the file exploded in size and I could no longer upload anything, even with a gitignore. I fought with the terminal for a long time to set up github lfs.

While I ended up being able to upload the repaired file, it was unpullable, causing even more frustration. Ryan narrowed the cause down to something to do with the HD rendering pipeline not being properly supported by the gitignore. A new file was created, and the Unity team dealt with it from there. 

## What is left + expectations for next week

Most other builds were nearing completion, with the Godot team being the most advanced. Hopes were high and we were confident in the work we had done thus far. I was behind on the UE, but I was clonfident I would be able to catch up adequately to have a build for the meeting with Skawenatti and AbTeC

# Weekly Reflection - Oct 21

This week marks the completion of the Unreal Engine prototype as we presented it to the AbTeC team, in addition to the finalization of what we are required to complete. 

## Unreal Engine

The Unreal prototype was completed the day of the presentation, horrible decision. The list of features completed are as follows:

- Tree of Life with glowing flowers (As per the work's guidelines)
- Podium and backdrop for the tree
- Unreal native glossy material and Unreal native glass 
- 

## Presentation

We presented to the AbTeC team on the Thursday of reading week. We began by walking them through the modular blender kit, as I did a live demo of its capabilities. They were open to hearing our concerns about the original blender file, and said they would talk to their 3D modelers to see what they think. Skawenatti had a bit of trouble understanding the purpose since it looked exactly the same as the original of it at first, then I explained that it functioned much better in-engine, could be texture painted or have PBRs applied to it, did not present any geometry issues, and gave way to a lot of freedom as I demonstrated by creating an abstract structure on the fly in demonstration. 

The Unreal engine did not build in time, the build itself failed, but it was not a big deal as I could ultimately run it in the editor. Nancy was online this week recovering from an injury, so we had some issues starting up the zoom for them to view the gallery. While they were relatively neutral on the build itself, they did praise the platform for its quick graphics, and how it can become realistic quickly, as I mentioned I built the prototype in only a few hours. I walked them through the issues UE presented, like the mesh slicing, large file sizes, etc, and they commented very little. 

From this meeting, I learned that artists can be very stone faced when evaluating proposals, with very little body language and comments. It is so difficult to know if they are happy or unhappy, so I can only assume, I now understand this is common in professional environments, so confidence and humility is key. 

## Godot + UE5

The final consensuses on builds became Godot + UE5, they explained wanting two things:

2. General accessibility with a windows & mac web option
   
4. A high end gallery they can show to special audiences in VR

The Godot build was chosen due to its flexibility in toolmaking and how lightweight it can be for the web option. Unity was immediately disqualified due to its technical issues for both builds. The VR build remains heavily inspired by Elektra and they aim for hyperrealism and high definition visuals, thus Unreal Engine was chosen. 

The assignments were therefore reshuffled to the following:

Godot - Jeremy, Bea, Ryan

Unreal - Me, Alex

## Going Forward

I will not be present for the meeting as I am feeling quite terrible from crunching for exhibitions this week, so I will not be at the meeting to bear witness to Sabine's opinion on our findings and work. I am happy with what I presented to the AbTeC team and felt I gave them enough information to make an informed choice. Although, I am concerned about the Unreal build on my end, as I was worried about how I would manage a clean build using only Blueprints that will be deprecated in the following UE6 launch in 2027. If their goal was to future proof the project, I felt using Unreal when such a big change is coming up would undermine their goals but ultimately, they were informed and made their choice, I suppose they would leave the gallery as is and have a staff convert all blueprints into C++ when the time comes. 

On my end, I was tasked with cleaning up the build, creating UI, making robust mechanics, and overall building everything a gallery requires to operate, essentially a EVM clone in VR. I have a lot of work to do. The difference between EVM and this is really the absence of the multiplayer aspect, so this will be a fully sandboxed experience they can run in their blackbox.

I spoke to the EVM dev again, and he was worried it might be too similar so I need to inform Ida and Alain that this is happening. I have not emailed them yet, and was waiting for confirmation from the overall team, and perhaps for all our other work to calm down. 

# Weekly Reflection - Oct 28

I have no idea what to write because...we did a whole lot of nothing this week.

I am meeting with Bea at 11 today to film some unreal and Blender documentation, so if this journal magically updates past the deadline...yup. I wasn't there for the discussions about this, but I do agree that files are worth nearly nothing if no documentation is provided.

I am not sure what to reflect on either, we were relatively thorough last week when Alex and I were filled in by the team, I am not sure how I feel regarding the lack of a midterm, because we are all slacking off but oh well. 

Some weeks are slower, and that's okay, I think after the first milestone, some breathing room is needed to then come back to the project strong, so yeah, I think we're taking a pause. 

# Weekly Reflection - Nov 11

Welp...it's been A GOOD TWO WEEKS, HELLO!!

I was in the hospital the week before so hehe...I did not do anything (Much) because looking at a screen hurt, so safe to say when I was cleared I got to business.

## The Original Revamp

The original UE file was...inexplicably lost (I cleaned out my drive and it went bye bye) but it's okay because it needed to be scrapped in any case as it was a very crude 1st person prototype, very much not in the right vein. That said, Alex and I came up with a plan on how to move forward as working on Unreal posed one major issue: FILE SHARING. Unreal was never meant to go on github, sure we can use LFS, but it's definitely a hassle. Instead of exploring and trying other options right away, Alex has remote access to my PC for other purposes, so this was the best solution, for him to simply access the file on my local computer as he needs to work on it. 

I was still locked up in the dungeon by this point, but I began the new file, I opened it with the default UE5 VR template, but on a blank scene so I could strip all the stuff I didn't need. I started working on a procedural terrain and landscape using PCG so they have a flexible base to modify and create elements for scenography as time goes on. I also made some sexy water, very sexy (Posting it on the group chat...had reactions).

The VR controller was working very well on my meta quest, so I was confident the template was working alright, even with the stripping, but the file began having rendering issues, where the map kept corrupting. The map would crash, then simply would not open, unless I went back into the autosaves and loaded up an old version. I could not figure out the source, I believed it was a nanite issue as shaders kept crashing, but in the end it may have had more to do with how the VR template compiled shaders. Alex was working on a menu, and got pretty far in the work, but it crashed for I believe the 4th or 5th time, and we got fed up, so we decided to start anew, completely fresh to get rid of all potential issues we may have inherited along the way.

## The Blank File

So, I scrapped it, much to Alex's dismay, and started over. A completely BLANK file, no controller, no nothing, BLANK. Here's what we got done before Wednesday:

- Importing the buildings
- Materials
- Tree of life import and rendering
- Water
- Basic scenography, grass and island look
- 1st person controller
- I for information text popup interactivity (!!)

We have not tested it in VR or attempted anything, Alex is working on UI atm, and my task is to figure out the controller until next week.

# Weekly Reflection - Nov 18

The blank file is no longer blank, we have done a lot. All the goals were achieved before the meeting with Sabine, resulting in an environment that looks different from the initial prototype, but arguably better.

Scenography & Models:

I made a SMALL landscape, tiny, I do not want to make it too big and increase lag, then raised all the sides to cover up the fact that there is nothing behind it, it works, and looks good. I placed a ground texture on it, and scattered some Quixel Megascan rocks to look like beachy mountains. The textures needed to be slightly adjusted, and the rocks were placed strategically to not remove from the gallery experience. I started placing some foliage, several types of grass, but I did not pay much mind to the cleanliness or polycount of it all, it is most definitely excessive, and is causing lag in the headset. We do not have any guidelines on what AbTeC's vision of the experience is like, so this environment is a placeholder, and from here on in, I will be optimizing it then working solely on systems, I do not want to beautify something that may be fundamentally changed. 

I imported the gallery building using the kit, placing it in front of a mountanous region to obscure the back. I fixed the collisions again so the user could navigate properly, and slapped on the same plastic and glass texture I made many many weeks ago. Triangulation issues still present. I imported Skawenatti's Tree of Life, and once again slapped on the textures I previously made. Given the lack of vision, I took liberties, and I placed the tree on a long platform emerging from the gallery suspended in a bed of water. 

Headset:

I took out the Samsung Odyssey headset from the Clab from Elio (Thank you, we love you), and started testing. It works currently through SteamVR and OpenXR on Windows 10. Once I got through putting in all the functionality, it ran with nearly no issues, I did not have any crashes (Yet...) so we hope it stays that way. Looking around is very smooth, the point and click functionality that comes with the headset to move work ever since I actually mapped it (I didn't at first and was banging my head against the wall because it wouldn't work), but it has a significant offset I will need to fix, I may switch it to a more universal joystick solution. The lag is terrible...not unplayable...but disgusting. Optimization is a task for next week. There is also this...black square that frames the player when they turn around??? 

Interactivity:

I placed an I to interact plaque in front of the tree, I made the widget + blueprint, and it worked for a bit, but because the center of the object coming out of Blender was messed up, when the user approaches the plaque, the "interact" text appears away from the object. I disconnected all the blueprints, and am in the process of debugging, might go into Blender and fix it though. 

No other interactivity in place at the moment, the to-do list includes:

- Sound (I have the old blueprints and foley to just smack it in) and expand it into a robust system
- Intro/Tutorial
- VR walking issue fix
- Shooting the Indian act

On another note, THE VR VERSION HAS HANDS!!! HUMAN HANDS!!!

# Weekly Reflection - Nov 25

See Weekly Reflection above this one (Nov 18, unsubmitted to Moodle in time but is here) to see details on what was achieved in the previous week.

Despite the deadline approaching, I did not do a whole lot this week to prioritize my electroacoustics work and get it out of the way so I can focus on this once we have guidelines from AbTeC. 
My goals for today, as we don't have much to tell Sabine on the Godot end either I believe, are to optimize the environment for VR and create a landing page. Then, once home and I have access to the headset today or tomorrow, before we meet or get answers from AbTeC, I can work on the controller, and integrate Alex's new widgets.  

Optimization:

- Enable Nanite
- Single Layer Water
- Geometry and Collisions
- Aspect Ratio?

The first thing I will be doing is replacing the foliage with Nanite compatible low-poly foliage to reduce the polycount and make it easily chunk renderable to the engine on startup, reducing the amount to render per tick. This is a whole thing because I am fairly certain this is what was causing our earlier corruptions, so probably gna be figured out tonight with a red bull at TAG. The water has been lagging on headset, so it really isn't worth keeping as the UE5 default water (Multi-layer, interactable), I will simply replace it with a plane with the Single Layer Water plugin enabled to have a texture and some ripples, call it a day. The geometry was really badly reconstructed, and I am not entirely sure why, we knew from the beginning that Unreal was triangulating meshes on import, and brought the issue up to AbTeC, they wanted to proceed anyway. That said, I need to find a solution, because it is impacting the frame rate on the headset because the renderer is not able to group them into bins properly. I showed the rest of my team what I talked about in the Sabine meeting, the whole lag when turning so you just see a black square around you. They also said it is probably an aspect ratio issue and I can overcompensate to go slightly bigger than the field of view to compensate for the square while I still have lag, red bull here I come tonight. 

Landing page & Onboarding:

- Welcome
- Controls

I want to make a loading screen, which includes the AbTeC logo and a welcome message, tbd. We have access to their logo files. When they spawn in the world, I want them to be in somewhat of a "tutorial" room. I want to have an overlay with diagrams that explain the controls of the experience, and how to use "I" for information to open the artist statements. 

Controller:

There is still no joystick movement, so I need to do that, still deciding between the default point and click that is built into the Samsung headset as opposed to using the universal joystick. 

Widgets: 

Alex created the artist overlay widget, so I will be adding that in to be functional. 

For everything else, I am waiting for AbTeC, because we need to consolidate what they want. 





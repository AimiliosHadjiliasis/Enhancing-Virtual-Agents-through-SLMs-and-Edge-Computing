<hr>

<h1 align="center">
  Enhancing Virtual Agents through SLMs and Edge Computing:<br>
  An Exploratory Evaluation of Think and Memory Processes
</h1>

<p align="center">
  <strong><a href="https://www.uclancyprus.ac.cy/academic/dr-aimilios-hadjiliasi/">Aimilios Hadjiliasi</a></strong><sup>*</sup>
  &emsp;&emsp;&emsp;&emsp;&emsp;
  <strong><a href="https://www.uclancyprus.ac.cy/academic/dr-louis-nisiotis/K">Louis Nisiotis</a></strong><sup>*</sup>
  <br>
  <a href="mailto:ahadjiliasi@uclan.ac.uk">ahadjiliasi@uclan.ac.uk</a>
  &emsp;&emsp;&emsp;&emsp;
  <a href="mailto:lnisiotis@uclan.ac.uk">lnisiotis@uclan.ac.uk</a>
</p>

<p align="center">
  <sup>*</sup><b>Department of Computing, Engineering and Mathematics<br>
    University of Central Lancashire, Cyprus</b>
</p>

<p align="center">
  IEEE International Symposium on Mixed and Augmented Reality (ISMAR) <br>
  XRAG'26 - Agentic AI for Extented Reality
  (<a href="">XRAG'26</a>),
  <br>
</p>

<p align="center">
  <img
    src="./ceaaAndPipeline.png"
    alt="System architecture"
    width="850"
  >
</p>

<h2 align="center"> Abstract </h2>
<p align="center">
  Embodied intelligent virtual agents are expected to operate as persistent, adaptive, and context-aware entities within complex virtual Metaverse worlds. 
However, implementing cognitively capable agents in such environments is conceptually and technologically challenging. 
Among a range of blueprints and development approaches, the Cognitive Embodied Agent Architecture (CEAA) is an implementation-oriented framework for architecting components of perception, memory, reasoning, planning, and embodied action. Considering the recent advances in edge computing and generative AI language models, this paper explore the use of Small Language Models (SLMs) to support edge-based operation of selected CEAA components, focusing on <b>Think</b> and <b>Memory</b> as processes central to cognitive orchestration and persistence of virtual agents in interactive virtual worlds. 
An edge-based virtual agent gateway system was developed and evaluated on an NVIDIA Jetson Orin NX using Qwen2.5 models of different sizes, exploring the systems capability to process service requests and handle memory driven conversations. <b>Thinking</b> was examined through service routing, where the agent classifies user requests and selects the appropriate processing route, and <b>Memory</b> was examined through structured write--read interactions for storing, retrieving, and updating contextual information. A series of simulation experiments evaluated routing accuracy, memory-read performance, and latency demonstrating an SLM driven prototype agent system that partially operationalise selected CEAA processes, to support the development of embodied agents whose cognitive “brain” can operate efficiently and contextually for interactive experiences in immersive virtual worlds.
</p>

<hr>
<p>
  <b>The below tables present the prompts used for testing the memory and the correct mapping of routing evaluation </b>
</p>

## Evaluation Prompt Dataset

The dataset contains **500 prompts**: **250 memory prompts** and **250 routing prompts**.

| No. | Phase | Prompt |
|---:|:---:|---|
| 1 | Memory | For this session, keep the prototype codename as Ember Ward. |
| 2 | Memory | What is the prototype codename for this session? |
| 3 | Memory | The current build target is standalone VR with a desktop debug simulator. |
| 4 | Memory | What is the current build target? |
| 5 | Memory | The opening scene starts in a flooded hospital corridor. |
| 6 | Memory | Where does the opening scene start? |
| 7 | Memory | The intended player feeling is calm under pressure rather than panic. |
| 8 | Memory | What player feeling are we targeting? |
| 9 | Memory | The main risk for the demo is hand-tracking latency during object grabbing. |
| 10 | Memory | What is the main risk for the demo? |
| 11 | Memory | The accessibility rule is that every colour warning also needs a shape cue. |
| 12 | Memory | What accessibility rule did we store? |
| 13 | Memory | The vertical slice must demonstrate cooperation without using voice chat. |
| 14 | Memory | What must the vertical slice demonstrate? |
| 15 | Memory | The prototype visual benchmark is stylised realism with low saturation. |
| 16 | Memory | What visual benchmark are we using? |
| 17 | Memory | The first playtest audience is first-year game-development students. |
| 18 | Memory | Who is the first playtest audience? |
| 19 | Memory | The baseline input method is gaze selection with a confirm button. |
| 20 | Memory | What is the baseline input method? |
| 21 | Memory | The sprint goal is interaction polish, not adding new levels. |
| 22 | Memory | What is the current sprint goal? |
| 23 | Memory | The build should favour seated VR interaction over room-scale movement. |
| 24 | Memory | What movement constraint did we agree on? |
| 25 | Memory | The tutorial should fail gracefully if the player drops the first tool. |
| 26 | Memory | What did we say about the grab tutorial? |
| 27 | Memory | The safe-zone outline shader is only for accessibility mode. |
| 28 | Memory | What did we say about the safe-zone outline shader? |
| 29 | Memory | The fail-safe rule is that puzzle-critical valves cannot spawn behind locked doors. |
| 30 | Memory | What is the fail-safe rule about puzzle-critical valves? |
| 31 | Memory | At stand-up, Rhea took ownership of lighting readability. |
| 32 | Memory | Who took ownership of lighting readability? |
| 33 | Memory | Rhea is interested in volumetric fog that keeps navigation markers visible. |
| 34 | Memory | What is Rhea interested in? |
| 35 | Memory | Update Rhea's task from lighting readability to safe-zone colour contrast. |
| 36 | Memory | What is Rhea responsible for now? |
| 37 | Memory | At stand-up, Nikos took ownership of backend telemetry. |
| 38 | Memory | Who took ownership of backend telemetry? |
| 39 | Memory | Nikos is interested in FastAPI health checks for generation backends. |
| 40 | Memory | What is Nikos interested in? |
| 41 | Memory | Update Nikos's task from backend telemetry to service-call logging dashboard. |
| 42 | Memory | What is Nikos responsible for now? |
| 43 | Memory | At stand-up, Mira took ownership of diegetic UI. |
| 44 | Memory | Who took ownership of diegetic UI? |
| 45 | Memory | Mira is interested in interface layouts for seated VR. |
| 46 | Memory | What is Mira interested in? |
| 47 | Memory | Update Mira's task from diegetic UI to wrist map readability. |
| 48 | Memory | What is Mira responsible for now? |
| 49 | Memory | At stand-up, Theo took ownership of physics props. |
| 50 | Memory | Who took ownership of physics props? |
| 51 | Memory | Theo is interested in weighted crate behaviour. |
| 52 | Memory | What is Theo interested in? |
| 53 | Memory | Update Theo's task from physics props to stable grab constraints. |
| 54 | Memory | What is Theo responsible for now? |
| 55 | Memory | At stand-up, Amina took ownership of comfort options. |
| 56 | Memory | Who took ownership of comfort options? |
| 57 | Memory | Amina is interested in reduced-motion mode. |
| 58 | Memory | What is Amina interested in? |
| 59 | Memory | Update Amina's task from comfort options to snap-turn tuning. |
| 60 | Memory | What is Amina responsible for now? |
| 61 | Memory | At stand-up, Jonas took ownership of soundscape layers. |
| 62 | Memory | Who took ownership of soundscape layers? |
| 63 | Memory | Jonas is interested in adaptive ambience. |
| 64 | Memory | What is Jonas interested in? |
| 65 | Memory | Update Jonas's task from soundscape layers to danger stingers. |
| 66 | Memory | What is Jonas responsible for now? |
| 67 | Memory | At stand-up, Petra took ownership of narrative structure. |
| 68 | Memory | Who took ownership of narrative structure? |
| 69 | Memory | Petra is interested in environmental storytelling. |
| 70 | Memory | What is Petra interested in? |
| 71 | Memory | Update Petra's task from narrative structure to mission scripting. |
| 72 | Memory | What is Petra responsible for now? |
| 73 | Memory | At stand-up, Oren took ownership of enemy readability. |
| 74 | Memory | Who took ownership of enemy readability? |
| 75 | Memory | Oren is interested in clear anticipation cues. |
| 76 | Memory | What is Oren interested in? |
| 77 | Memory | Update Oren's task from enemy readability to silhouette testing. |
| 78 | Memory | What is Oren responsible for now? |
| 79 | Memory | At stand-up, Selene took ownership of material references. |
| 80 | Memory | Who took ownership of material references? |
| 81 | Memory | Selene is interested in wet metal material studies. |
| 82 | Memory | What is Selene interested in? |
| 83 | Memory | Update Selene's task from material references to burned concrete surfaces. |
| 84 | Memory | What is Selene responsible for now? |
| 85 | Memory | At stand-up, Ilias took ownership of network synchronisation. |
| 86 | Memory | Who took ownership of network synchronisation? |
| 87 | Memory | Ilias is interested in latency testing for co-op objects. |
| 88 | Memory | What is Ilias interested in? |
| 89 | Memory | Update Ilias's task from network synchronisation to shared lever replication. |
| 90 | Memory | What is Ilias responsible for now? |
| 91 | Memory | At stand-up, Dana took ownership of tutorial pacing. |
| 92 | Memory | Who took ownership of tutorial pacing? |
| 93 | Memory | Dana is interested in first-time user guidance. |
| 94 | Memory | What is Dana interested in? |
| 95 | Memory | Update Dana's task from tutorial pacing to hint timing. |
| 96 | Memory | What is Dana responsible for now? |
| 97 | Memory | At stand-up, Kora took ownership of accessibility validation. |
| 98 | Memory | Who took ownership of accessibility validation? |
| 99 | Memory | Kora is interested in shape cues for warnings. |
| 100 | Memory | What is Kora interested in? |
| 101 | Memory | Update Kora's task from accessibility validation to subtitles while crouching. |
| 102 | Memory | What is Kora responsible for now? |
| 103 | Memory | At stand-up, Basil took ownership of asset integration. |
| 104 | Memory | Who took ownership of asset integration? |
| 105 | Memory | Basil is interested in runtime asset loading. |
| 106 | Memory | What is Basil interested in? |
| 107 | Memory | Update Basil's task from asset integration to GLB import checks. |
| 108 | Memory | What is Basil responsible for now? |
| 109 | Memory | At stand-up, Nora took ownership of level greyboxing. |
| 110 | Memory | Who took ownership of level greyboxing? |
| 111 | Memory | Nora is interested in corridor landmark placement. |
| 112 | Memory | What is Nora interested in? |
| 113 | Memory | Update Nora's task from level greyboxing to safe-route visibility. |
| 114 | Memory | What is Nora responsible for now? |
| 115 | Memory | At stand-up, Yannis took ownership of QA logging. |
| 116 | Memory | Who took ownership of QA logging? |
| 117 | Memory | Yannis is interested in comfort issue triage. |
| 118 | Memory | What is Yannis interested in? |
| 119 | Memory | Update Yannis's task from QA logging to dizziness reports. |
| 120 | Memory | What is Yannis responsible for now? |
| 121 | Memory | Character note: Milo Finch is the radio companion. |
| 122 | Memory | Who is the radio companion? |
| 123 | Memory | Behaviour note for Milo Finch: gives short radio hints when the player stands still too long. |
| 124 | Memory | What does Milo Finch do? |
| 125 | Memory | When we discuss companion hint timing, link it back to Milo Finch. |
| 126 | Memory | What do you remember about companion hint timing? |
| 127 | Memory | Character note: Glass Warden is the slow enemy. |
| 128 | Memory | Who is the slow enemy? |
| 129 | Memory | Behaviour note for Glass Warden: reacts to flashlight beams rather than footsteps. |
| 130 | Memory | What does Glass Warden do? |
| 131 | Memory | When we discuss light-reactive enemy behaviour, link it back to Glass Warden. |
| 132 | Memory | What do you remember about light-reactive enemy behaviour? |
| 133 | Memory | Character note: Nurse Vale is the mission guide. |
| 134 | Memory | Who is the mission guide? |
| 135 | Memory | Behaviour note for Nurse Vale: gives objective hints after each checkpoint. |
| 136 | Memory | What does Nurse Vale do? |
| 137 | Memory | When we discuss mission guide dialogue, link it back to Nurse Vale. |
| 138 | Memory | What do you remember about mission guide dialogue? |
| 139 | Memory | Character note: Ash Drone is the flying hazard detector. |
| 140 | Memory | Who is the flying hazard detector? |
| 141 | Memory | Behaviour note for Ash Drone: scans closed rooms for heat signatures. |
| 142 | Memory | What does Ash Drone do? |
| 143 | Memory | When we discuss hazard scanning behaviour, link it back to Ash Drone. |
| 144 | Memory | What do you remember about hazard scanning behaviour? |
| 145 | Memory | Character note: Sable Clerk is the merchant automaton. |
| 146 | Memory | Who is the merchant automaton? |
| 147 | Memory | Behaviour note for Sable Clerk: trades salvage for temporary traversal tools. |
| 148 | Memory | What does Sable Clerk do? |
| 149 | Memory | When we discuss economy NPC logic, link it back to Sable Clerk. |
| 150 | Memory | What do you remember about economy NPC logic? |
| 151 | Memory | Character note: Jun Reed is the maintenance engineer. |
| 152 | Memory | Who is the maintenance engineer? |
| 153 | Memory | Behaviour note for Jun Reed: unlocks pump controls after the repair puzzle. |
| 154 | Memory | What does Jun Reed do? |
| 155 | Memory | When we discuss repair-gate NPC, link it back to Jun Reed. |
| 156 | Memory | What do you remember about repair-gate NPC? |
| 157 | Memory | Character note: Aster Lane is the child survivor. |
| 158 | Memory | Who is the child survivor? |
| 159 | Memory | Behaviour note for Aster Lane: hides whenever emergency lights switch off. |
| 160 | Memory | What does Aster Lane do? |
| 161 | Memory | When we discuss fear-state behaviour, link it back to Aster Lane. |
| 162 | Memory | What do you remember about fear-state behaviour? |
| 163 | Memory | Character note: The Glass Choir is the environmental threat. |
| 164 | Memory | Who is the environmental threat? |
| 165 | Memory | Behaviour note for The Glass Choir: sings before pressure windows fracture. |
| 166 | Memory | What does The Glass Choir do? |
| 167 | Memory | When we discuss warning-state hazard, link it back to The Glass Choir. |
| 168 | Memory | What do you remember about warning-state hazard? |
| 169 | Memory | Character note: Vera Pike is the rival rescuer. |
| 170 | Memory | Who is the rival rescuer? |
| 171 | Memory | Behaviour note for Vera Pike: blocks shortcuts if optional rescues are ignored. |
| 172 | Memory | What does Vera Pike do? |
| 173 | Memory | When we discuss reactive rival logic, link it back to Vera Pike. |
| 174 | Memory | What do you remember about reactive rival logic? |
| 175 | Memory | Character note: Mina Rowe is the lost intern. |
| 176 | Memory | Who is the lost intern? |
| 177 | Memory | Behaviour note for Mina Rowe: waits in the smoke corridor until the player activates the beacon. |
| 178 | Memory | What does Mina Rowe do? |
| 179 | Memory | When we discuss rescue-state NPC, link it back to Mina Rowe. |
| 180 | Memory | What do you remember about rescue-state NPC? |
| 181 | Memory | For the equipment spec, the pressure compass is used to point players toward unstable bulkheads. |
| 182 | Memory | What is the pressure compass used for? |
| 183 | Memory | System behaviour: the pressure compass needle shakes when a flood event is nearby. |
| 184 | Memory | What happens to the pressure compass? |
| 185 | Memory | For the equipment spec, the thermal flare is used to mark safe exits for the second player. |
| 186 | Memory | What is the thermal flare used for? |
| 187 | Memory | System behaviour: the thermal flare smoke bends toward safe exits when the alarm level is high. |
| 188 | Memory | What happens to the thermal flare? |
| 189 | Memory | For the equipment spec, the cracked oxygen meter is used to warn players before oxygen drops below twenty percent. |
| 190 | Memory | What is the cracked oxygen meter used for? |
| 191 | Memory | System behaviour: the cracked oxygen meter screen flickers when the generator is unstable. |
| 192 | Memory | What happens to the cracked oxygen meter? |
| 193 | Memory | For the equipment spec, the evacuation map is used to show route changes after each checkpoint. |
| 194 | Memory | What is the evacuation map used for? |
| 195 | Memory | System behaviour: the evacuation map display becomes wrist-mounted after the correction. |
| 196 | Memory | What happens to the evacuation map? |
| 197 | Memory | For the equipment spec, the repair foam is used to seal small leaks temporarily. |
| 198 | Memory | What is the repair foam used for? |
| 199 | Memory | System behaviour: the repair foam hardens faster near heat sources. |
| 200 | Memory | What happens to the repair foam? |
| 201 | Memory | For the equipment spec, the tether reel is used to pull a partner across broken platforms. |
| 202 | Memory | What is the tether reel used for? |
| 203 | Memory | System behaviour: the tether reel cable slack increases if both players sprint. |
| 204 | Memory | What happens to the tether reel? |
| 205 | Memory | For the equipment spec, the signal beacon is used to show the partner's last confirmed position. |
| 206 | Memory | What is the signal beacon used for? |
| 207 | Memory | System behaviour: the signal beacon range drops in flooded rooms. |
| 208 | Memory | What happens to the signal beacon? |
| 209 | Memory | For the equipment spec, the airlock crank is used to restore pressure manually during outages. |
| 210 | Memory | What is the airlock crank used for? |
| 211 | Memory | System behaviour: the airlock crank handle locks when alarms are active. |
| 212 | Memory | What happens to the airlock crank? |
| 213 | Memory | For the equipment spec, the map slate is used to store scanned room annotations. |
| 214 | Memory | What is the map slate used for? |
| 215 | Memory | System behaviour: the map slate screen flickers after water damage. |
| 216 | Memory | What happens to the map slate? |
| 217 | Memory | For the equipment spec, the echo probe is used to detect hidden chambers through walls. |
| 218 | Memory | What is the echo probe used for? |
| 219 | Memory | System behaviour: the echo probe pulse gets noisy around machinery. |
| 220 | Memory | What happens to the echo probe? |
| 221 | Memory | For the equipment spec, the oxygen refill station is used to restore limited oxygen charges. |
| 222 | Memory | What is the oxygen refill station used for? |
| 223 | Memory | System behaviour: the oxygen refill station status changes after the third rescue. |
| 224 | Memory | What happens to the oxygen refill station? |
| 225 | Memory | For the equipment spec, the checkpoint board is used to show active rescue objectives. |
| 226 | Memory | What is the checkpoint board used for? |
| 227 | Memory | System behaviour: the checkpoint board status changes when the player reaches a checkpoint. |
| 228 | Memory | What happens to the checkpoint board? |
| 229 | Memory | For the equipment spec, the sprinkler panel is used to open the fire-suppression puzzle route. |
| 230 | Memory | What is the sprinkler panel used for? |
| 231 | Memory | System behaviour: the sprinkler panel lights turn amber when pressure is unstable. |
| 232 | Memory | What happens to the sprinkler panel? |
| 233 | Memory | For the equipment spec, the radio beacon is used to guide civilians toward the nearest safe room. |
| 234 | Memory | What is the radio beacon used for? |
| 235 | Memory | System behaviour: the radio beacon signal distorts near the Glass Warden. |
| 236 | Memory | What happens to the radio beacon? |
| 237 | Memory | For the equipment spec, the equipment locker is used to store unlocked firefighter tools. |
| 238 | Memory | What is the equipment locker used for? |
| 239 | Memory | System behaviour: the equipment locker door jams after the alarm level reaches three. |
| 240 | Memory | What happens to the equipment locker? |
| 241 | Memory | Correction for evacuation map: earlier it was wall display; update it to wrist-mounted map. |
| 242 | Memory | What do you remember about evacuation map after the correction? |
| 243 | Memory | Correction for pressure compass: earlier it was main navigation item; update it to secondary guidance item after the map slate. |
| 244 | Memory | What do you remember about pressure compass after the correction? |
| 245 | Memory | Correction for Glass Warden: earlier it was first enemy; update it to mid-game pursuer introduced after the flooded corridor. |
| 246 | Memory | What do you remember about Glass Warden after the correction? |
| 247 | Memory | Correction for thermal flare: earlier it was unlimited navigation tool; update it to limited emergency marker with three charges. |
| 248 | Memory | What do you remember about thermal flare after the correction? |
| 249 | Memory | Correction for Milo Finch: earlier it was mandatory tutorial narrator; update it to optional companion voice. |
| 250 | Memory | What do you remember about Milo Finch after the correction? |
| 251 | Routing | Generate a 3D model of a rusted hospital cross mounted on a wall. |
| 252 | Routing | Create a GLB asset of a cracked oxygen cylinder for a VR horror game. |
| 253 | Routing | Make a 3D model of a portable evacuation radio with a broken antenna. |
| 254 | Routing | Generate a low-poly 3D fire extinguisher prop with worn labels. |
| 255 | Routing | Create a 3D model of a flooded corridor warning sign. |
| 256 | Routing | Generate a 3D mesh of a medical supply crate with metal hinges. |
| 257 | Routing | Make a game-ready 3D model of a damaged flashlight. |
| 258 | Routing | Generate a 3D model of a sacred wooden cross with worn edges. |
| 259 | Routing | Create a 3D mesh of a wrist-mounted evacuation map. |
| 260 | Routing | Make a 3D model of a thermal flare launcher. |
| 261 | Routing | Generate a 3D model of a cracked hospital bed. |
| 262 | Routing | Create a GLB model of a rescue drone with small propellers. |
| 263 | Routing | Make a 3D prop of a checkpoint board with glowing objective slots. |
| 264 | Routing | Generate a 3D mesh of a corroded airlock crank. |
| 265 | Routing | Create a game-ready 3D pressure valve with red handles. |
| 266 | Routing | Generate a 3D model of an old chapel candle stand. |
| 267 | Routing | Make a 3D prop of a broken generator panel. |
| 268 | Routing | Create a GLB asset of a wall-mounted fire alarm. |
| 269 | Routing | Generate a 3D model of a wet floor caution sign. |
| 270 | Routing | Make a 3D object of a folded emergency stretcher. |
| 271 | Routing | Create a 3D mesh of a radio beacon with blinking antenna. |
| 272 | Routing | Generate a 3D model of a rusted metal locker. |
| 273 | Routing | Make a 3D prop of a sealed medical door. |
| 274 | Routing | Create a game-ready 3D oxygen refill station. |
| 275 | Routing | Generate a 3D model of a cracked ceramic statue. |
| 276 | Routing | Make a GLB asset of a rescue tool crate. |
| 277 | Routing | Create a 3D model of a ceiling sprinkler panel. |
| 278 | Routing | Generate a 3D model of a burned wooden cross. |
| 279 | Routing | Use this uploaded image to create a GLB model of a rescue helmet. |
| 280 | Routing | Convert this reference photo into a 3D model of a wall-mounted alarm. |
| 281 | Routing | Use the sketch I uploaded to generate a 3D mesh of a pressure valve. |
| 282 | Routing | Create a GLB asset from this concept image of a rescue drone. |
| 283 | Routing | Turn this screenshot into a 3D prop for a hospital checkpoint board. |
| 284 | Routing | Use this picture as reference to generate a 3D oxygen mask. |
| 285 | Routing | Convert the uploaded concept art into a 3D model of a chapel door. |
| 286 | Routing | Use this photo to make a 3D model of a medical trolley. |
| 287 | Routing | Generate a GLB from the uploaded sketch of a thermal flare. |
| 288 | Routing | Make a 3D asset from this screenshot of a rescue sign. |
| 289 | Routing | Use the reference image to create a 3D model of a damaged flashlight. |
| 290 | Routing | Convert this uploaded picture into a mesh of an evacuation map. |
| 291 | Routing | Use this concept image to generate a 3D hospital bed prop. |
| 292 | Routing | Create a 3D model from this photo of a fire extinguisher. |
| 293 | Routing | Turn this uploaded sketch into a 3D radio beacon. |
| 294 | Routing | Use this visual reference to create a GLB asset of a safe-room marker. |
| 295 | Routing | Convert this image into a 3D model of a generator switch. |
| 296 | Routing | Use the uploaded screenshot to create a 3D wall panel. |
| 297 | Routing | Generate a mesh from this reference image of an equipment locker. |
| 298 | Routing | Create a 3D prop from this photo of a wet corridor sign. |
| 299 | Routing | Use this image to make a GLB model of a cracked statue. |
| 300 | Routing | Convert this concept art into a 3D pressure gauge. |
| 301 | Routing | Use the uploaded picture to create a 3D chapel candle stand. |
| 302 | Routing | Generate a 3D model from this sketch of a rescue crate. |
| 303 | Routing | Turn this reference photo into a 3D airlock crank. |
| 304 | Routing | Generate a PBR texture for burned concrete with soot marks. |
| 305 | Routing | Create a seamless rusty metal material for an old hospital door. |
| 306 | Routing | Make a normal map for cracked ceramic floor tiles. |
| 307 | Routing | Generate a wet plastic texture for emergency tarps. |
| 308 | Routing | Create a glowing red warning decal material for a checkpoint panel. |
| 309 | Routing | Make a PBR marble material for a chapel floor. |
| 310 | Routing | Generate an albedo and roughness texture for damp concrete walls. |
| 311 | Routing | Create a seamless material for corroded brass handles. |
| 312 | Routing | Make a cracked white paint texture for hospital corridors. |
| 313 | Routing | Generate a dark rubber material for oxygen mask straps. |
| 314 | Routing | Create a stained glass texture with subtle damage. |
| 315 | Routing | Make a wet metal surface material for a flooded airlock. |
| 316 | Routing | Generate a dirty plastic texture for old medical equipment. |
| 317 | Routing | Create a PBR material for burned wood with ash edges. |
| 318 | Routing | Make a seamless tile texture for emergency room flooring. |
| 319 | Routing | Generate a flickering emissive warning sign texture. |
| 320 | Routing | Create a scratched steel material for rescue tools. |
| 321 | Routing | Make a mossy concrete texture for basement walls. |
| 322 | Routing | Generate a translucent plastic material for oxygen tubes. |
| 323 | Routing | Create a decal texture for evacuation arrows. |
| 324 | Routing | Make a PBR texture for scorched chapel stone. |
| 325 | Routing | Generate a peeling paint material for a safe-room door. |
| 326 | Routing | Create a wet paper label texture for medical crates. |
| 327 | Routing | Make a grungy rubber floor material. |
| 328 | Routing | Generate a seamless cracked plaster texture. |
| 329 | Routing | Create a metallic warning panel material with scratches. |
| 330 | Routing | Make a normal map for dented metal lockers. |
| 331 | Routing | Generate a non-verbal warning siren with no spoken words. |
| 332 | Routing | Create an ambience loop for a flooded underground hospital corridor. |
| 333 | Routing | Make a short metallic impact sound for a dropped oxygen tank. |
| 334 | Routing | Generate creature breathing audio without speech. |
| 335 | Routing | Create a looping electrical hum for a failing generator. |
| 336 | Routing | Make footsteps splashing through shallow water. |
| 337 | Routing | Generate a distant alarm bell sound effect. |
| 338 | Routing | Create a low rumble for unstable pressure pipes. |
| 339 | Routing | Make a glass cracking sound for pressure windows. |
| 340 | Routing | Generate a soft radio static loop. |
| 341 | Routing | Create a door hinge creak for an old hospital ward. |
| 342 | Routing | Make a heavy valve turning Foley sound. |
| 343 | Routing | Generate a short UI beep for oxygen warnings. |
| 344 | Routing | Create a muffled explosion sound for a blocked corridor. |
| 345 | Routing | Make a quiet chapel ambience with distant water drops. |
| 346 | Routing | Generate an enemy proximity audio cue with no speech. |
| 347 | Routing | Create a rising tension sound for alarm escalation. |
| 348 | Routing | Make a metal locker slam sound effect. |
| 349 | Routing | Generate a wet tarp rustling Foley sound. |
| 350 | Routing | Create a failing fluorescent light buzz. |
| 351 | Routing | Make a short success chime for completing a rescue. |
| 352 | Routing | Generate an underwater corridor ambience loop. |
| 353 | Routing | Create a heavy breathing non-verbal player warning. |
| 354 | Routing | Make a pressure leak hissing sound effect. |
| 355 | Routing | Generate a distant siren tail for level transitions. |
| 356 | Routing | Create a low-frequency drone for the Glass Warden. |
| 357 | Routing | Make a small button click sound for UI selection. |
| 358 | Routing | Create spoken tutorial audio saying check your oxygen level. |
| 359 | Routing | Make an NPC voice line saying stay close to the green markers. |
| 360 | Routing | Generate narration that says the evacuation route has changed. |
| 361 | Routing | Create a mission announcement saying return to the safe room. |
| 362 | Routing | Make a text-to-speech voice line for Milo Finch saying hold your breath. |
| 363 | Routing | Generate an NPC line saying the generator is unstable. |
| 364 | Routing | Create tutorial speech that says press the confirm button to scan. |
| 365 | Routing | Make a calm voice line saying follow the wrist map. |
| 366 | Routing | Generate a radio message saying corridor B is flooded. |
| 367 | Routing | Create a spoken warning saying oxygen below twenty percent. |
| 368 | Routing | Make a companion voice line saying I found a safer route. |
| 369 | Routing | Generate narration saying the pressure valve is locked. |
| 370 | Routing | Create a survivor voice line saying I am trapped behind the door. |
| 371 | Routing | Make a text-to-speech line saying wait for the alarm to stop. |
| 372 | Routing | Generate a mission voice saying rescue complete. |
| 373 | Routing | Create an announcement saying return to checkpoint board. |
| 374 | Routing | Make an NPC line saying do not use the flashlight now. |
| 375 | Routing | Generate tutorial audio saying open the equipment locker. |
| 376 | Routing | Create spoken dialogue saying the Glass Warden is nearby. |
| 377 | Routing | Make a radio line saying signal lost in the flooded room. |
| 378 | Routing | Generate a calm narrator saying breathe slowly. |
| 379 | Routing | Create a voice prompt saying scan the room for heat signatures. |
| 380 | Routing | Make a mission update saying safe zone unlocked. |
| 381 | Routing | Generate spoken instructions for using the thermal flare. |
| 382 | Routing | Create an NPC dialogue line saying I can hear the pipes cracking. |
| 383 | Routing | Generate motion data for a firefighter crouch walk. |
| 384 | Routing | Create an idle animation for a frightened civilian NPC. |
| 385 | Routing | Make a dodge animation for a player avoiding falling debris. |
| 386 | Routing | Generate a slow patrol walk cycle for the Glass Warden enemy. |
| 387 | Routing | Create a waving gesture animation for a rescued survivor. |
| 388 | Routing | Make a crawling animation for a player moving under smoke. |
| 389 | Routing | Generate a limping walk cycle for an injured NPC. |
| 390 | Routing | Create a two-handed valve turning animation. |
| 391 | Routing | Make a character animation for lifting an oxygen tank. |
| 392 | Routing | Generate a short stumble animation for wet floor slipping. |
| 393 | Routing | Create an animation clip for pointing toward a safe exit. |
| 394 | Routing | Make an enemy attack wind-up animation. |
| 395 | Routing | Generate a motion clip for opening a heavy airlock door. |
| 396 | Routing | Create a breathing idle animation for a scared survivor. |
| 397 | Routing | Make a kneeling rescue animation. |
| 398 | Routing | Generate a hand gesture for scanning with the wrist map. |
| 399 | Routing | Create a sprint-to-stop locomotion animation. |
| 400 | Routing | Make a slow turn animation for a flashlight search. |
| 401 | Routing | Generate a crouched idle pose for stealth gameplay. |
| 402 | Routing | Create a recoil animation for pushing a stuck valve. |
| 403 | Routing | Make a wave-over-here gesture for a companion NPC. |
| 404 | Routing | Generate a collapse animation for a smoke-exposed civilian. |
| 405 | Routing | Create a gesture animation for covering the mouth from smoke. |
| 406 | Routing | Make a climbing-over-debris animation. |
| 407 | Routing | Generate a motion clip for dragging a rescue crate. |
| 408 | Routing | Write a Unity C# script for an oxygen gauge UI. |
| 409 | Routing | Fix a NullReferenceException in a Unity interaction script. |
| 410 | Routing | Create a FastAPI endpoint that forwards prompts to the 3D backend. |
| 411 | Routing | Write a C# component that rotates an objective marker toward the player. |
| 412 | Routing | Debug this JSON parsing issue in my Unity gateway client. |
| 413 | Routing | Implement a Unity script that highlights usable valves. |
| 414 | Routing | Write Python code that checks whether backend services are online. |
| 415 | Routing | Create a C# coroutine that sends chat messages to the gateway. |
| 416 | Routing | Fix a compile error in a Unity script that references TextMeshPro. |
| 417 | Routing | Write a Unity component for oxygen depletion over time. |
| 418 | Routing | Create a C# trigger that updates the checkpoint board. |
| 419 | Routing | Debug a FastAPI timeout when the generation backend is offline. |
| 420 | Routing | Write code to parse asset_url from the gateway response. |
| 421 | Routing | Implement a Unity script for toggling accessibility outlines. |
| 422 | Routing | Create a C# script that plays a siren when oxygen is low. |
| 423 | Routing | Fix a coroutine that never receives the HTTP response. |
| 424 | Routing | Write Python code for logging gateway latency into a CSV file. |
| 425 | Routing | Create a Unity script for grabbing and releasing the pressure valve. |
| 426 | Routing | Debug a JSON serialization error in AgentRequest. |
| 427 | Routing | Write a C# class for storing service response metadata. |
| 428 | Routing | Implement retry logic for failed HTTP service calls. |
| 429 | Routing | Create a FastAPI health route for the sound backend. |
| 430 | Routing | Write a Unity script that displays generated texture URLs. |
| 431 | Routing | Fix an issue where session_id changes every message. |
| 432 | Routing | Create a C# script that sends player position in world_context. |
| 433 | Routing | Debug a route-only endpoint returning router_orchestrator. |
| 434 | Routing | Write Python code to summarise memory test results. |
| 435 | Routing | Implement a Unity UI panel for showing gateway status. |
| 436 | Routing | Design a progression system for unlocking firefighter tools. |
| 437 | Routing | Create rules for a risk-reward loop between fast evacuation and safe evacuation. |
| 438 | Routing | Design a scoring system for rescuing civilians without wasting oxygen. |
| 439 | Routing | Define a cooldown mechanic for using the thermal flare. |
| 440 | Routing | Design a puzzle where two players must stabilise the pressure valve. |
| 441 | Routing | Create a resource economy around oxygen charges and flare uses. |
| 442 | Routing | Design a checkpoint reward system for rescuing optional civilians. |
| 443 | Routing | Define the gameplay loop for scanning rooms and marking exits. |
| 444 | Routing | Create balance rules for flashlight battery drain. |
| 445 | Routing | Design a stealth mechanic around avoiding the Glass Warden. |
| 446 | Routing | Define fail-state rules for running out of oxygen. |
| 447 | Routing | Create a cooperative puzzle using the tether reel and airlock crank. |
| 448 | Routing | Design objective rules for the evacuation map. |
| 449 | Routing | Create a progression system for unlocking safe-zone shortcuts. |
| 450 | Routing | Define player-facing rules for using repair foam. |
| 451 | Routing | Design a risk system where alarms increase enemy aggression. |
| 452 | Routing | Create a reward loop for exploring optional hospital rooms. |
| 453 | Routing | Define how thermal flare charges should be earned. |
| 454 | Routing | Design a mechanic for sharing oxygen between two players. |
| 455 | Routing | Create scoring rules for completing rescues quietly. |
| 456 | Routing | Define a puzzle sequence for restoring generator power. |
| 457 | Routing | Design rules for safe-room discovery. |
| 458 | Routing | Create a balance model for enemy detection and player hiding. |
| 459 | Routing | Define player objectives for the first five minutes of gameplay. |
| 460 | Routing | Design a mechanic where water level changes navigation options. |
| 461 | Routing | Create rules for checkpoint board updates. |
| 462 | Routing | Define a progression loop for learning tools gradually. |
| 463 | Routing | Design patrol behaviour for the Glass Warden enemy. |
| 464 | Routing | Create an AI state machine for a civilian NPC that hides during alarms. |
| 465 | Routing | Define perception rules for an enemy that reacts to flashlight beams. |
| 466 | Routing | Design companion behaviour for Milo Finch during player inactivity. |
| 467 | Routing | Create chase logic for an enemy that slows down near safe zones. |
| 468 | Routing | Define behaviour tree nodes for an evacuation NPC. |
| 469 | Routing | Design an AI decision loop for a survivor choosing safe exits. |
| 470 | Routing | Create investigation behaviour for a guard hearing metal impacts. |
| 471 | Routing | Define enemy state transitions from idle to search to chase. |
| 472 | Routing | Design companion follow-distance behaviour in narrow corridors. |
| 473 | Routing | Create NPC panic behaviour when emergency lights switch off. |
| 474 | Routing | Define AI perception using sound level and flashlight exposure. |
| 475 | Routing | Design a rescue drone behaviour for scanning closed rooms. |
| 476 | Routing | Create enemy attack decision rules for the Glass Warden. |
| 477 | Routing | Define civilian regrouping behaviour after the alarm stops. |
| 478 | Routing | Design patrol route adaptation when the corridor floods. |
| 479 | Routing | Create behaviour rules for a merchant automaton NPC. |
| 480 | Routing | Define a companion hint system based on player hesitation. |
| 481 | Routing | Design enemy retreat behaviour near chapel safe zones. |
| 482 | Routing | Create AI logic for NPCs avoiding smoke-filled rooms. |
| 483 | Routing | Define a behaviour tree for checking doors and calling for help. |
| 484 | Routing | Design perception logic for enemies losing sight of the player. |
| 485 | Routing | Create state transitions for a drone moving from scan to alert. |
| 486 | Routing | Define AI behaviour for a survivor following green markers. |
| 487 | Routing | Design a guard NPC that blocks shortcuts when optional rescues are ignored. |
| 488 | Routing | Generate a 3D model of a cracked rescue chapel altar. |
| 489 | Routing | Create a GLB asset of a portable defibrillator with worn buttons. |
| 490 | Routing | Use this uploaded reference image to create a 3D model of a hospital corridor sign. |
| 491 | Routing | Generate a PBR texture for wet cracked asphalt outside the hospital. |
| 492 | Routing | Create a non-verbal alarm escalation sound effect. |
| 493 | Routing | Make a spoken NPC line saying the north stairwell is blocked. |
| 494 | Routing | Generate motion data for a survivor crawling under smoke. |
| 495 | Routing | Write a Unity C# script that updates the wrist map objective text. |
| 496 | Routing | Design a gameplay rule for sharing rescue tools between two players. |
| 497 | Routing | Create AI behaviour for a drone that marks rooms with heat signatures. |
| 498 | Routing | Generate a 3D model of a broken wall-mounted oxygen gauge. |
| 499 | Routing | Create a seamless stained concrete texture with water damage. |
| 500 | Routing | Design enemy search behaviour after the player turns off the flashlight. |


## Router Evaluation Dataset

The dataset contains **1,000 evaluation prompts** covering **10 expected routing categories**.

| No. | User Message | Expected Route |
|---:|---|:---:|
| 1 | Hello, can you explain your role in this workspace? | `router_orchestrator` |
| 2 | What can this assistant help me with during a game-development session? | `router_orchestrator` |
| 3 | Can you give me a short overview of your available capabilities? | `router_orchestrator` |
| 4 | Before I start, can you explain how I should interact with this agent? | `router_orchestrator` |
| 5 | I am new to this workspace; what should I ask you first? | `router_orchestrator` |
| 6 | Can you help me understand what kind of support is available here? | `router_orchestrator` |
| 7 | What kinds of tasks can this virtual assistant coordinate? | `router_orchestrator` |
| 8 | Can you explain the difference between general guidance and specialised support? | `router_orchestrator` |
| 9 | How should I decide what kind of help to request? | `router_orchestrator` |
| 10 | Can you summarise how this game-development assistant works? | `router_orchestrator` |
| 11 | What is your purpose in this collaborative workspace? | `router_orchestrator` |
| 12 | Can you explain how this assistant supports a development team? | `router_orchestrator` |
| 13 | What can I ask you about while working on this project? | `router_orchestrator` |
| 14 | Can you give me a quick orientation to this workspace? | `router_orchestrator` |
| 15 | I need a general overview before starting the task. | `router_orchestrator` |
| 16 | Can you explain how to use this assistant effectively? | `router_orchestrator` |
| 17 | What are the main categories of help available here? | `router_orchestrator` |
| 18 | Can you describe the support options without starting a task yet? | `router_orchestrator` |
| 19 | I want to understand the workspace capabilities first. | `router_orchestrator` |
| 20 | Can you help me decide how to phrase my next request? | `router_orchestrator` |
| 21 | What should I do if I am unsure what kind of help I need? | `router_orchestrator` |
| 22 | Can you explain how task selection works in this agent? | `router_orchestrator` |
| 23 | How does this assistant decide whether to answer directly or use a specialist? | `router_orchestrator` |
| 24 | Can you describe the workflow from a user message to a response? | `router_orchestrator` |
| 25 | Can you explain the available help categories at a high level? | `router_orchestrator` |
| 26 | I am just exploring the system; what can you do? | `router_orchestrator` |
| 27 | Can you give me a non-technical overview of the workspace assistant? | `router_orchestrator` |
| 28 | What is the best way to ask for help here? | `router_orchestrator` |
| 29 | Can you explain how this assistant supports project planning? | `router_orchestrator` |
| 30 | Can you help me understand the available options before I choose one? | `router_orchestrator` |
| 31 | What are you designed to do in this virtual environment? | `router_orchestrator` |
| 32 | Can you explain your capabilities in simple terms? | `router_orchestrator` |
| 33 | Can you guide me through what this agent can and cannot do? | `router_orchestrator` |
| 34 | I want to know how to use the assistant before making a specific request. | `router_orchestrator` |
| 35 | Can you describe the role of the assistant in the game-development hub? | `router_orchestrator` |
| 36 | How should a developer interact with this assistant? | `router_orchestrator` |
| 37 | Can you explain how requests are interpreted in this workspace? | `router_orchestrator` |
| 38 | What should I ask if I need general guidance? | `router_orchestrator` |
| 39 | Can you provide an overview of the interaction process? | `router_orchestrator` |
| 40 | I am not asking for an output yet; can you explain the system? | `router_orchestrator` |
| 41 | Can you describe the help available to a designer in this workspace? | `router_orchestrator` |
| 42 | Can you describe the help available to a developer in this workspace? | `router_orchestrator` |
| 43 | Can you describe the help available to an artist in this workspace? | `router_orchestrator` |
| 44 | Can you describe the help available to a student using this workspace? | `router_orchestrator` |
| 45 | Can you give me a general introduction to this agent? | `router_orchestrator` |
| 46 | What can this agent do for a team project? | `router_orchestrator` |
| 47 | How do I know which kind of request to make? | `router_orchestrator` |
| 48 | Can you explain the agent's decision process at a high level? | `router_orchestrator` |
| 49 | Can you tell me what kind of assistant you are? | `router_orchestrator` |
| 50 | Can you orient me before I start using the system? | `router_orchestrator` |
| 51 | What is the general purpose of this agent? | `router_orchestrator` |
| 52 | Can you explain how the workspace is organised? | `router_orchestrator` |
| 53 | Can you help me understand the available support without selecting a specialist? | `router_orchestrator` |
| 54 | I need a general explanation of the assistant's capabilities. | `router_orchestrator` |
| 55 | Can you explain how this system helps with game-development collaboration? | `router_orchestrator` |
| 56 | What should I know before using this assistant? | `router_orchestrator` |
| 57 | Can you describe the interaction model for this workspace? | `router_orchestrator` |
| 58 | Can you give me a short help message for new users? | `router_orchestrator` |
| 59 | How should I use this assistant during a design session? | `router_orchestrator` |
| 60 | How should I use this assistant during a development session? | `router_orchestrator` |
| 61 | Can you explain the difference between asking for guidance and asking for output? | `router_orchestrator` |
| 62 | What happens after I send a message to the gateway? | `router_orchestrator` |
| 63 | Can you describe how the gateway chooses the next step? | `router_orchestrator` |
| 64 | Can you explain the role of the local orchestrator? | `router_orchestrator` |
| 65 | Can you explain what the gateway does before answering? | `router_orchestrator` |
| 66 | What are the general types of support in this system? | `router_orchestrator` |
| 67 | Can you help me plan what kind of question to ask next? | `router_orchestrator` |
| 68 | I am unsure what the assistant can do; can you clarify? | `router_orchestrator` |
| 69 | Can you explain this workspace to a first-time user? | `router_orchestrator` |
| 70 | Can you describe the agent workflow in one paragraph? | `router_orchestrator` |
| 71 | Can you tell me how to start a session with this assistant? | `router_orchestrator` |
| 72 | What does this assistant need from me to help properly? | `router_orchestrator` |
| 73 | Can you explain how to make requests clearer? | `router_orchestrator` |
| 74 | Can you give me general usage guidance for the assistant? | `router_orchestrator` |
| 75 | Can you explain what happens if my request is unclear? | `router_orchestrator` |
| 76 | Can you explain when the assistant answers directly? | `router_orchestrator` |
| 77 | Can you explain when the assistant uses another component? | `router_orchestrator` |
| 78 | Can you describe the available support without performing a task? | `router_orchestrator` |
| 79 | I need help understanding the system, not creating anything yet. | `router_orchestrator` |
| 80 | Can you explain how this assistant fits into the Unity workflow? | `router_orchestrator` |
| 81 | Can you describe how Unity messages are handled by the gateway? | `router_orchestrator` |
| 82 | Can you explain the difference between local answers and delegated tasks? | `router_orchestrator` |
| 83 | Can you explain how the system avoids calling the wrong component? | `router_orchestrator` |
| 84 | What is the role of the gateway in this project? | `router_orchestrator` |
| 85 | Can you give me a short orientation for the agent interface? | `router_orchestrator` |
| 86 | Can you explain how users should interact with the virtual assistant? | `router_orchestrator` |
| 87 | Can you describe what support is available before I give a specific task? | `router_orchestrator` |
| 88 | What are the main things this assistant can help coordinate? | `router_orchestrator` |
| 89 | Can you explain the assistant's capabilities for a project meeting? | `router_orchestrator` |
| 90 | Can you help me understand how the system handles user intent? | `router_orchestrator` |
| 91 | Can you describe the agent's general responsibilities? | `router_orchestrator` |
| 92 | Can you provide general help for using this workspace? | `router_orchestrator` |
| 93 | How should I begin if I have multiple possible tasks? | `router_orchestrator` |
| 94 | Can you explain how to choose the next step in the workspace? | `router_orchestrator` |
| 95 | Can you describe the assistant's role without launching any tool? | `router_orchestrator` |
| 96 | Can you explain how the agent supports collaborative work? | `router_orchestrator` |
| 97 | What should a new user know about this assistant? | `router_orchestrator` |
| 98 | Can you summarise the workspace assistant in practical terms? | `router_orchestrator` |
| 99 | Can you explain how this assistant helps organise requests? | `router_orchestrator` |
| 100 | I only need orientation; what can this agent help with? | `router_orchestrator` |
| 101 | Write a Unity C# inventory script. | `coding_support` |
| 102 | Debug this issue in my Python client for the route endpoint. | `coding_support` |
| 103 | Create code for a debug NullReferenceException. | `coding_support` |
| 104 | Explain how to implement a networked lobby manager. | `coding_support` |
| 105 | Fix a bug in my Unreal Blueprint door trigger. | `coding_support` |
| 106 | Refactor my C# component to apply a material for cleaner structure. | `coding_support` |
| 107 | Generate a Unity C# script for shader code for dissolve effect. | `coding_support` |
| 108 | Help me call the backend API from FastAPI endpoint for texture generation. | `coding_support` |
| 109 | Diagnose why my Unity script to play a WAV file is failing. | `coding_support` |
| 110 | Show me an implementation plan for refactor an animation controller script. | `coding_support` |
| 111 | Write a FastAPI endpoint for texture generation. | `coding_support` |
| 112 | Debug this issue in my Unity script to play a WAV file. | `coding_support` |
| 113 | Create code for a refactor an animation controller script. | `coding_support` |
| 114 | Explain how to implement a Unity C# inventory script. | `coding_support` |
| 115 | Fix a bug in my Python client for the route endpoint. | `coding_support` |
| 116 | Refactor my debug NullReferenceException for cleaner structure. | `coding_support` |
| 117 | Generate a Unity C# script for networked lobby manager. | `coding_support` |
| 118 | Help me call the backend API from Unreal Blueprint door trigger. | `coding_support` |
| 119 | Diagnose why my C# component to apply a material is failing. | `coding_support` |
| 120 | Show me an implementation plan for shader code for dissolve effect. | `coding_support` |
| 121 | Write a Unreal Blueprint door trigger. | `coding_support` |
| 122 | Debug this issue in my C# component to apply a material. | `coding_support` |
| 123 | Create code for a shader code for dissolve effect. | `coding_support` |
| 124 | Explain how to implement a FastAPI endpoint for texture generation. | `coding_support` |
| 125 | Fix a bug in my Unity script to play a WAV file. | `coding_support` |
| 126 | Refactor my refactor an animation controller script for cleaner structure. | `coding_support` |
| 127 | Generate a Unity C# script for Unity C# inventory script. | `coding_support` |
| 128 | Help me call the backend API from Python client for the route endpoint. | `coding_support` |
| 129 | Diagnose why my debug NullReferenceException is failing. | `coding_support` |
| 130 | Show me an implementation plan for networked lobby manager. | `coding_support` |
| 131 | Write a Python client for the route endpoint. | `coding_support` |
| 132 | Debug this issue in my debug NullReferenceException. | `coding_support` |
| 133 | Create code for a networked lobby manager. | `coding_support` |
| 134 | Explain how to implement a Unreal Blueprint door trigger. | `coding_support` |
| 135 | Fix a bug in my C# component to apply a material. | `coding_support` |
| 136 | Refactor my shader code for dissolve effect for cleaner structure. | `coding_support` |
| 137 | Generate a Unity C# script for FastAPI endpoint for texture generation. | `coding_support` |
| 138 | Help me call the backend API from Unity script to play a WAV file. | `coding_support` |
| 139 | Diagnose why my refactor an animation controller script is failing. | `coding_support` |
| 140 | Show me an implementation plan for Unity C# inventory script. | `coding_support` |
| 141 | Write a Unity script to play a WAV file. | `coding_support` |
| 142 | Debug this issue in my refactor an animation controller script. | `coding_support` |
| 143 | Create code for a Unity C# inventory script. | `coding_support` |
| 144 | Explain how to implement a Python client for the route endpoint. | `coding_support` |
| 145 | Fix a bug in my debug NullReferenceException. | `coding_support` |
| 146 | Refactor my networked lobby manager for cleaner structure. | `coding_support` |
| 147 | Generate a Unity C# script for Unreal Blueprint door trigger. | `coding_support` |
| 148 | Help me call the backend API from C# component to apply a material. | `coding_support` |
| 149 | Diagnose why my shader code for dissolve effect is failing. | `coding_support` |
| 150 | Show me an implementation plan for FastAPI endpoint for texture generation. | `coding_support` |
| 151 | Write a C# component to apply a material. | `coding_support` |
| 152 | Debug this issue in my shader code for dissolve effect. | `coding_support` |
| 153 | Create code for a FastAPI endpoint for texture generation. | `coding_support` |
| 154 | Explain how to implement a Unity script to play a WAV file. | `coding_support` |
| 155 | Fix a bug in my refactor an animation controller script. | `coding_support` |
| 156 | Refactor my Unity C# inventory script for cleaner structure. | `coding_support` |
| 157 | Generate a Unity C# script for Python client for the route endpoint. | `coding_support` |
| 158 | Help me call the backend API from debug NullReferenceException. | `coding_support` |
| 159 | Diagnose why my networked lobby manager is failing. | `coding_support` |
| 160 | Show me an implementation plan for Unreal Blueprint door trigger. | `coding_support` |
| 161 | Write a debug NullReferenceException. | `coding_support` |
| 162 | Debug this issue in my networked lobby manager. | `coding_support` |
| 163 | Create code for a Unreal Blueprint door trigger. | `coding_support` |
| 164 | Explain how to implement a C# component to apply a material. | `coding_support` |
| 165 | Fix a bug in my shader code for dissolve effect. | `coding_support` |
| 166 | Refactor my FastAPI endpoint for texture generation for cleaner structure. | `coding_support` |
| 167 | Generate a Unity C# script for Unity script to play a WAV file. | `coding_support` |
| 168 | Help me call the backend API from refactor an animation controller script. | `coding_support` |
| 169 | Diagnose why my Unity C# inventory script is failing. | `coding_support` |
| 170 | Show me an implementation plan for Python client for the route endpoint. | `coding_support` |
| 171 | Write a refactor an animation controller script. | `coding_support` |
| 172 | Debug this issue in my Unity C# inventory script. | `coding_support` |
| 173 | Create code for a Python client for the route endpoint. | `coding_support` |
| 174 | Explain how to implement a debug NullReferenceException. | `coding_support` |
| 175 | Fix a bug in my networked lobby manager. | `coding_support` |
| 176 | Refactor my Unreal Blueprint door trigger for cleaner structure. | `coding_support` |
| 177 | Generate a Unity C# script for C# component to apply a material. | `coding_support` |
| 178 | Help me call the backend API from shader code for dissolve effect. | `coding_support` |
| 179 | Diagnose why my FastAPI endpoint for texture generation is failing. | `coding_support` |
| 180 | Show me an implementation plan for Unity script to play a WAV file. | `coding_support` |
| 181 | Write a shader code for dissolve effect. | `coding_support` |
| 182 | Debug this issue in my FastAPI endpoint for texture generation. | `coding_support` |
| 183 | Create code for a Unity script to play a WAV file. | `coding_support` |
| 184 | Explain how to implement a refactor an animation controller script. | `coding_support` |
| 185 | Fix a bug in my Unity C# inventory script. | `coding_support` |
| 186 | Refactor my Python client for the route endpoint for cleaner structure. | `coding_support` |
| 187 | Generate a Unity C# script for debug NullReferenceException. | `coding_support` |
| 188 | Help me call the backend API from networked lobby manager. | `coding_support` |
| 189 | Diagnose why my Unreal Blueprint door trigger is failing. | `coding_support` |
| 190 | Show me an implementation plan for C# component to apply a material. | `coding_support` |
| 191 | Write a networked lobby manager. | `coding_support` |
| 192 | Debug this issue in my Unreal Blueprint door trigger. | `coding_support` |
| 193 | Create code for a C# component to apply a material. | `coding_support` |
| 194 | Explain how to implement a shader code for dissolve effect. | `coding_support` |
| 195 | Fix a bug in my FastAPI endpoint for texture generation. | `coding_support` |
| 196 | Refactor my Unity script to play a WAV file for cleaner structure. | `coding_support` |
| 197 | Generate a Unity C# script for refactor an animation controller script. | `coding_support` |
| 198 | Help me call the backend API from Unity C# inventory script. | `coding_support` |
| 199 | Diagnose why my Python client for the route endpoint is failing. | `coding_support` |
| 200 | Show me an implementation plan for debug NullReferenceException. | `coding_support` |
| 201 | Design a zone control objective. | `gameplay_mechanics` |
| 202 | How can I balance a turn-based tank balance? | `gameplay_mechanics` |
| 203 | Suggest mechanics for a capture-and-defend win condition. | `gameplay_mechanics` |
| 204 | Improve the player feedback loop for a combat stamina mechanic. | `gameplay_mechanics` |
| 205 | Create non-code design rules for a cooperative puzzle mechanic. | `gameplay_mechanics` |
| 206 | Evaluate whether this difficulty curve for boss fights will be fun. | `gameplay_mechanics` |
| 207 | Tune the difficulty of a platformer progression. | `gameplay_mechanics` |
| 208 | What rewards should support a stealth horror loop? | `gameplay_mechanics` |
| 209 | Help structure progression for a reward system for exploration. | `gameplay_mechanics` |
| 210 | Design the core gameplay loop around a resource economy. | `gameplay_mechanics` |
| 211 | Design a stealth horror loop. | `gameplay_mechanics` |
| 212 | How can I balance a reward system for exploration? | `gameplay_mechanics` |
| 213 | Suggest mechanics for a resource economy. | `gameplay_mechanics` |
| 214 | Improve the player feedback loop for a zone control objective. | `gameplay_mechanics` |
| 215 | Create non-code design rules for a turn-based tank balance. | `gameplay_mechanics` |
| 216 | Evaluate whether this capture-and-defend win condition will be fun. | `gameplay_mechanics` |
| 217 | Tune the difficulty of a combat stamina mechanic. | `gameplay_mechanics` |
| 218 | What rewards should support a cooperative puzzle mechanic? | `gameplay_mechanics` |
| 219 | Help structure progression for a difficulty curve for boss fights. | `gameplay_mechanics` |
| 220 | Design the core gameplay loop around a platformer progression. | `gameplay_mechanics` |
| 221 | Design a cooperative puzzle mechanic. | `gameplay_mechanics` |
| 222 | How can I balance a difficulty curve for boss fights? | `gameplay_mechanics` |
| 223 | Suggest mechanics for a platformer progression. | `gameplay_mechanics` |
| 224 | Improve the player feedback loop for a stealth horror loop. | `gameplay_mechanics` |
| 225 | Create non-code design rules for a reward system for exploration. | `gameplay_mechanics` |
| 226 | Evaluate whether this resource economy will be fun. | `gameplay_mechanics` |
| 227 | Tune the difficulty of a zone control objective. | `gameplay_mechanics` |
| 228 | What rewards should support a turn-based tank balance? | `gameplay_mechanics` |
| 229 | Help structure progression for a capture-and-defend win condition. | `gameplay_mechanics` |
| 230 | Design the core gameplay loop around a combat stamina mechanic. | `gameplay_mechanics` |
| 231 | Design a turn-based tank balance. | `gameplay_mechanics` |
| 232 | How can I balance a capture-and-defend win condition? | `gameplay_mechanics` |
| 233 | Suggest mechanics for a combat stamina mechanic. | `gameplay_mechanics` |
| 234 | Improve the player feedback loop for a cooperative puzzle mechanic. | `gameplay_mechanics` |
| 235 | Create non-code design rules for a difficulty curve for boss fights. | `gameplay_mechanics` |
| 236 | Evaluate whether this platformer progression will be fun. | `gameplay_mechanics` |
| 237 | Tune the difficulty of a stealth horror loop. | `gameplay_mechanics` |
| 238 | What rewards should support a reward system for exploration? | `gameplay_mechanics` |
| 239 | Help structure progression for a resource economy. | `gameplay_mechanics` |
| 240 | Design the core gameplay loop around a zone control objective. | `gameplay_mechanics` |
| 241 | Design a reward system for exploration. | `gameplay_mechanics` |
| 242 | How can I balance a resource economy? | `gameplay_mechanics` |
| 243 | Suggest mechanics for a zone control objective. | `gameplay_mechanics` |
| 244 | Improve the player feedback loop for a turn-based tank balance. | `gameplay_mechanics` |
| 245 | Create non-code design rules for a capture-and-defend win condition. | `gameplay_mechanics` |
| 246 | Evaluate whether this combat stamina mechanic will be fun. | `gameplay_mechanics` |
| 247 | Tune the difficulty of a cooperative puzzle mechanic. | `gameplay_mechanics` |
| 248 | What rewards should support a difficulty curve for boss fights? | `gameplay_mechanics` |
| 249 | Help structure progression for a platformer progression. | `gameplay_mechanics` |
| 250 | Design the core gameplay loop around a stealth horror loop. | `gameplay_mechanics` |
| 251 | Design a difficulty curve for boss fights. | `gameplay_mechanics` |
| 252 | How can I balance a platformer progression? | `gameplay_mechanics` |
| 253 | Suggest mechanics for a stealth horror loop. | `gameplay_mechanics` |
| 254 | Improve the player feedback loop for a reward system for exploration. | `gameplay_mechanics` |
| 255 | Create non-code design rules for a resource economy. | `gameplay_mechanics` |
| 256 | Evaluate whether this zone control objective will be fun. | `gameplay_mechanics` |
| 257 | Tune the difficulty of a turn-based tank balance. | `gameplay_mechanics` |
| 258 | What rewards should support a capture-and-defend win condition? | `gameplay_mechanics` |
| 259 | Help structure progression for a combat stamina mechanic. | `gameplay_mechanics` |
| 260 | Design the core gameplay loop around a cooperative puzzle mechanic. | `gameplay_mechanics` |
| 261 | Design a capture-and-defend win condition. | `gameplay_mechanics` |
| 262 | How can I balance a combat stamina mechanic? | `gameplay_mechanics` |
| 263 | Suggest mechanics for a cooperative puzzle mechanic. | `gameplay_mechanics` |
| 264 | Improve the player feedback loop for a difficulty curve for boss fights. | `gameplay_mechanics` |
| 265 | Create non-code design rules for a platformer progression. | `gameplay_mechanics` |
| 266 | Evaluate whether this stealth horror loop will be fun. | `gameplay_mechanics` |
| 267 | Tune the difficulty of a reward system for exploration. | `gameplay_mechanics` |
| 268 | What rewards should support a resource economy? | `gameplay_mechanics` |
| 269 | Help structure progression for a zone control objective. | `gameplay_mechanics` |
| 270 | Design the core gameplay loop around a turn-based tank balance. | `gameplay_mechanics` |
| 271 | Design a resource economy. | `gameplay_mechanics` |
| 272 | How can I balance a zone control objective? | `gameplay_mechanics` |
| 273 | Suggest mechanics for a turn-based tank balance. | `gameplay_mechanics` |
| 274 | Improve the player feedback loop for a capture-and-defend win condition. | `gameplay_mechanics` |
| 275 | Create non-code design rules for a combat stamina mechanic. | `gameplay_mechanics` |
| 276 | Evaluate whether this cooperative puzzle mechanic will be fun. | `gameplay_mechanics` |
| 277 | Tune the difficulty of a difficulty curve for boss fights. | `gameplay_mechanics` |
| 278 | What rewards should support a platformer progression? | `gameplay_mechanics` |
| 279 | Help structure progression for a stealth horror loop. | `gameplay_mechanics` |
| 280 | Design the core gameplay loop around a reward system for exploration. | `gameplay_mechanics` |
| 281 | Design a platformer progression. | `gameplay_mechanics` |
| 282 | How can I balance a stealth horror loop? | `gameplay_mechanics` |
| 283 | Suggest mechanics for a reward system for exploration. | `gameplay_mechanics` |
| 284 | Improve the player feedback loop for a resource economy. | `gameplay_mechanics` |
| 285 | Create non-code design rules for a zone control objective. | `gameplay_mechanics` |
| 286 | Evaluate whether this turn-based tank balance will be fun. | `gameplay_mechanics` |
| 287 | Tune the difficulty of a capture-and-defend win condition. | `gameplay_mechanics` |
| 288 | What rewards should support a combat stamina mechanic? | `gameplay_mechanics` |
| 289 | Help structure progression for a cooperative puzzle mechanic. | `gameplay_mechanics` |
| 290 | Design the core gameplay loop around a difficulty curve for boss fights. | `gameplay_mechanics` |
| 291 | Design a combat stamina mechanic. | `gameplay_mechanics` |
| 292 | How can I balance a cooperative puzzle mechanic? | `gameplay_mechanics` |
| 293 | Suggest mechanics for a difficulty curve for boss fights. | `gameplay_mechanics` |
| 294 | Improve the player feedback loop for a platformer progression. | `gameplay_mechanics` |
| 295 | Create non-code design rules for a stealth horror loop. | `gameplay_mechanics` |
| 296 | Evaluate whether this reward system for exploration will be fun. | `gameplay_mechanics` |
| 297 | Tune the difficulty of a resource economy. | `gameplay_mechanics` |
| 298 | What rewards should support a zone control objective? | `gameplay_mechanics` |
| 299 | Help structure progression for a turn-based tank balance. | `gameplay_mechanics` |
| 300 | Design the core gameplay loop around a capture-and-defend win condition. | `gameplay_mechanics` |
| 301 | Design non-code AI logic for guard patrol behaviour. | `game_ai_guidance` |
| 302 | How should I structure a FSM for a flying drone? | `game_ai_guidance` |
| 303 | Should I use a behaviour tree or FSM for NPC perception system? | `game_ai_guidance` |
| 304 | Explain the AI design for AI debugging for stuck enemies. | `game_ai_guidance` |
| 305 | Suggest NPC decision-making for behaviour tree for a boss. | `game_ai_guidance` |
| 306 | Improve the perception model for GOAP planning for enemies. | `game_ai_guidance` |
| 307 | Help design pathfinding behaviour for pathfinding around obstacles. | `game_ai_guidance` |
| 308 | Create a tactical AI plan for enemy chase and search logic. | `game_ai_guidance` |
| 309 | Evaluate the enemy behaviour for utility AI for villagers. | `game_ai_guidance` |
| 310 | Design game AI guidance for squad tactics. | `game_ai_guidance` |
| 311 | Design non-code AI logic for enemy chase and search logic. | `game_ai_guidance` |
| 312 | How should I structure a utility AI for villagers? | `game_ai_guidance` |
| 313 | Should I use a behaviour tree or FSM for squad tactics? | `game_ai_guidance` |
| 314 | Explain the AI design for guard patrol behaviour. | `game_ai_guidance` |
| 315 | Suggest NPC decision-making for FSM for a flying drone. | `game_ai_guidance` |
| 316 | Improve the perception model for NPC perception system. | `game_ai_guidance` |
| 317 | Help design pathfinding behaviour for AI debugging for stuck enemies. | `game_ai_guidance` |
| 318 | Create a tactical AI plan for behaviour tree for a boss. | `game_ai_guidance` |
| 319 | Evaluate the enemy behaviour for GOAP planning for enemies. | `game_ai_guidance` |
| 320 | Design game AI guidance for pathfinding around obstacles. | `game_ai_guidance` |
| 321 | Design non-code AI logic for behaviour tree for a boss. | `game_ai_guidance` |
| 322 | How should I structure a GOAP planning for enemies? | `game_ai_guidance` |
| 323 | Should I use a behaviour tree or FSM for pathfinding around obstacles? | `game_ai_guidance` |
| 324 | Explain the AI design for enemy chase and search logic. | `game_ai_guidance` |
| 325 | Suggest NPC decision-making for utility AI for villagers. | `game_ai_guidance` |
| 326 | Improve the perception model for squad tactics. | `game_ai_guidance` |
| 327 | Help design pathfinding behaviour for guard patrol behaviour. | `game_ai_guidance` |
| 328 | Create a tactical AI plan for FSM for a flying drone. | `game_ai_guidance` |
| 329 | Evaluate the enemy behaviour for NPC perception system. | `game_ai_guidance` |
| 330 | Design game AI guidance for AI debugging for stuck enemies. | `game_ai_guidance` |
| 331 | Design non-code AI logic for FSM for a flying drone. | `game_ai_guidance` |
| 332 | How should I structure a NPC perception system? | `game_ai_guidance` |
| 333 | Should I use a behaviour tree or FSM for AI debugging for stuck enemies? | `game_ai_guidance` |
| 334 | Explain the AI design for behaviour tree for a boss. | `game_ai_guidance` |
| 335 | Suggest NPC decision-making for GOAP planning for enemies. | `game_ai_guidance` |
| 336 | Improve the perception model for pathfinding around obstacles. | `game_ai_guidance` |
| 337 | Help design pathfinding behaviour for enemy chase and search logic. | `game_ai_guidance` |
| 338 | Create a tactical AI plan for utility AI for villagers. | `game_ai_guidance` |
| 339 | Evaluate the enemy behaviour for squad tactics. | `game_ai_guidance` |
| 340 | Design game AI guidance for guard patrol behaviour. | `game_ai_guidance` |
| 341 | Design non-code AI logic for utility AI for villagers. | `game_ai_guidance` |
| 342 | How should I structure a squad tactics? | `game_ai_guidance` |
| 343 | Should I use a behaviour tree or FSM for guard patrol behaviour? | `game_ai_guidance` |
| 344 | Explain the AI design for FSM for a flying drone. | `game_ai_guidance` |
| 345 | Suggest NPC decision-making for NPC perception system. | `game_ai_guidance` |
| 346 | Improve the perception model for AI debugging for stuck enemies. | `game_ai_guidance` |
| 347 | Help design pathfinding behaviour for behaviour tree for a boss. | `game_ai_guidance` |
| 348 | Create a tactical AI plan for GOAP planning for enemies. | `game_ai_guidance` |
| 349 | Evaluate the enemy behaviour for pathfinding around obstacles. | `game_ai_guidance` |
| 350 | Design game AI guidance for enemy chase and search logic. | `game_ai_guidance` |
| 351 | Design non-code AI logic for GOAP planning for enemies. | `game_ai_guidance` |
| 352 | How should I structure a pathfinding around obstacles? | `game_ai_guidance` |
| 353 | Should I use a behaviour tree or FSM for enemy chase and search logic? | `game_ai_guidance` |
| 354 | Explain the AI design for utility AI for villagers. | `game_ai_guidance` |
| 355 | Suggest NPC decision-making for squad tactics. | `game_ai_guidance` |
| 356 | Improve the perception model for guard patrol behaviour. | `game_ai_guidance` |
| 357 | Help design pathfinding behaviour for FSM for a flying drone. | `game_ai_guidance` |
| 358 | Create a tactical AI plan for NPC perception system. | `game_ai_guidance` |
| 359 | Evaluate the enemy behaviour for AI debugging for stuck enemies. | `game_ai_guidance` |
| 360 | Design game AI guidance for behaviour tree for a boss. | `game_ai_guidance` |
| 361 | Design non-code AI logic for NPC perception system. | `game_ai_guidance` |
| 362 | How should I structure a AI debugging for stuck enemies? | `game_ai_guidance` |
| 363 | Should I use a behaviour tree or FSM for behaviour tree for a boss? | `game_ai_guidance` |
| 364 | Explain the AI design for GOAP planning for enemies. | `game_ai_guidance` |
| 365 | Suggest NPC decision-making for pathfinding around obstacles. | `game_ai_guidance` |
| 366 | Improve the perception model for enemy chase and search logic. | `game_ai_guidance` |
| 367 | Help design pathfinding behaviour for utility AI for villagers. | `game_ai_guidance` |
| 368 | Create a tactical AI plan for squad tactics. | `game_ai_guidance` |
| 369 | Evaluate the enemy behaviour for guard patrol behaviour. | `game_ai_guidance` |
| 370 | Design game AI guidance for FSM for a flying drone. | `game_ai_guidance` |
| 371 | Design non-code AI logic for squad tactics. | `game_ai_guidance` |
| 372 | How should I structure a guard patrol behaviour? | `game_ai_guidance` |
| 373 | Should I use a behaviour tree or FSM for FSM for a flying drone? | `game_ai_guidance` |
| 374 | Explain the AI design for NPC perception system. | `game_ai_guidance` |
| 375 | Suggest NPC decision-making for AI debugging for stuck enemies. | `game_ai_guidance` |
| 376 | Improve the perception model for behaviour tree for a boss. | `game_ai_guidance` |
| 377 | Help design pathfinding behaviour for GOAP planning for enemies. | `game_ai_guidance` |
| 378 | Create a tactical AI plan for pathfinding around obstacles. | `game_ai_guidance` |
| 379 | Evaluate the enemy behaviour for enemy chase and search logic. | `game_ai_guidance` |
| 380 | Design game AI guidance for utility AI for villagers. | `game_ai_guidance` |
| 381 | Design non-code AI logic for pathfinding around obstacles. | `game_ai_guidance` |
| 382 | How should I structure a enemy chase and search logic? | `game_ai_guidance` |
| 383 | Should I use a behaviour tree or FSM for utility AI for villagers? | `game_ai_guidance` |
| 384 | Explain the AI design for squad tactics. | `game_ai_guidance` |
| 385 | Suggest NPC decision-making for guard patrol behaviour. | `game_ai_guidance` |
| 386 | Improve the perception model for FSM for a flying drone. | `game_ai_guidance` |
| 387 | Help design pathfinding behaviour for NPC perception system. | `game_ai_guidance` |
| 388 | Create a tactical AI plan for AI debugging for stuck enemies. | `game_ai_guidance` |
| 389 | Evaluate the enemy behaviour for behaviour tree for a boss. | `game_ai_guidance` |
| 390 | Design game AI guidance for GOAP planning for enemies. | `game_ai_guidance` |
| 391 | Design non-code AI logic for AI debugging for stuck enemies. | `game_ai_guidance` |
| 392 | How should I structure a behaviour tree for a boss? | `game_ai_guidance` |
| 393 | Should I use a behaviour tree or FSM for GOAP planning for enemies? | `game_ai_guidance` |
| 394 | Explain the AI design for pathfinding around obstacles. | `game_ai_guidance` |
| 395 | Suggest NPC decision-making for enemy chase and search logic. | `game_ai_guidance` |
| 396 | Improve the perception model for utility AI for villagers. | `game_ai_guidance` |
| 397 | Help design pathfinding behaviour for squad tactics. | `game_ai_guidance` |
| 398 | Create a tactical AI plan for guard patrol behaviour. | `game_ai_guidance` |
| 399 | Evaluate the enemy behaviour for FSM for a flying drone. | `game_ai_guidance` |
| 400 | Design game AI guidance for NPC perception system. | `game_ai_guidance` |
| 401 | Generate a complete 3D model of a medieval sword. | `generation_3d` |
| 402 | Create a GLB asset of a dungeon door. | `generation_3d` |
| 403 | Make a game-ready mesh for a fantasy shield. | `generation_3d` |
| 404 | Produce a full 3D prop: low-poly tree stump. | `generation_3d` |
| 405 | Generate a low-poly 3D object of a wooden barrel. | `generation_3d` |
| 406 | Create a complete scene object model: robot drone. | `generation_3d` |
| 407 | Make a textured 3D asset of a space console. | `generation_3d` |
| 408 | Generate a 3D mesh suitable for Unity: sci-fi crate. | `generation_3d` |
| 409 | Create a full object model for a market stall. | `generation_3d` |
| 410 | Produce a complete 3D asset, not just a surface, of a stone arch. | `generation_3d` |
| 411 | Generate a complete 3D model of a sci-fi crate. | `generation_3d` |
| 412 | Create a GLB asset of a market stall. | `generation_3d` |
| 413 | Make a game-ready mesh for a stone arch. | `generation_3d` |
| 414 | Produce a full 3D prop: medieval sword. | `generation_3d` |
| 415 | Generate a low-poly 3D object of a dungeon door. | `generation_3d` |
| 416 | Create a complete scene object model: fantasy shield. | `generation_3d` |
| 417 | Make a textured 3D asset of a low-poly tree stump. | `generation_3d` |
| 418 | Generate a 3D mesh suitable for Unity: wooden barrel. | `generation_3d` |
| 419 | Create a full object model for a robot drone. | `generation_3d` |
| 420 | Produce a complete 3D asset, not just a surface, of a space console. | `generation_3d` |
| 421 | Generate a complete 3D model of a wooden barrel. | `generation_3d` |
| 422 | Create a GLB asset of a robot drone. | `generation_3d` |
| 423 | Make a game-ready mesh for a space console. | `generation_3d` |
| 424 | Produce a full 3D prop: sci-fi crate. | `generation_3d` |
| 425 | Generate a low-poly 3D object of a market stall. | `generation_3d` |
| 426 | Create a complete scene object model: stone arch. | `generation_3d` |
| 427 | Make a textured 3D asset of a medieval sword. | `generation_3d` |
| 428 | Generate a 3D mesh suitable for Unity: dungeon door. | `generation_3d` |
| 429 | Create a full object model for a fantasy shield. | `generation_3d` |
| 430 | Produce a complete 3D asset, not just a surface, of a low-poly tree stump. | `generation_3d` |
| 431 | Generate a complete 3D model of a dungeon door. | `generation_3d` |
| 432 | Create a GLB asset of a fantasy shield. | `generation_3d` |
| 433 | Make a game-ready mesh for a low-poly tree stump. | `generation_3d` |
| 434 | Produce a full 3D prop: wooden barrel. | `generation_3d` |
| 435 | Generate a low-poly 3D object of a robot drone. | `generation_3d` |
| 436 | Create a complete scene object model: space console. | `generation_3d` |
| 437 | Make a textured 3D asset of a sci-fi crate. | `generation_3d` |
| 438 | Generate a 3D mesh suitable for Unity: market stall. | `generation_3d` |
| 439 | Create a full object model for a stone arch. | `generation_3d` |
| 440 | Produce a complete 3D asset, not just a surface, of a medieval sword. | `generation_3d` |
| 441 | Generate a complete 3D model of a market stall. | `generation_3d` |
| 442 | Create a GLB asset of a stone arch. | `generation_3d` |
| 443 | Make a game-ready mesh for a medieval sword. | `generation_3d` |
| 444 | Produce a full 3D prop: dungeon door. | `generation_3d` |
| 445 | Generate a low-poly 3D object of a fantasy shield. | `generation_3d` |
| 446 | Create a complete scene object model: low-poly tree stump. | `generation_3d` |
| 447 | Make a textured 3D asset of a wooden barrel. | `generation_3d` |
| 448 | Generate a 3D mesh suitable for Unity: robot drone. | `generation_3d` |
| 449 | Create a full object model for a space console. | `generation_3d` |
| 450 | Produce a complete 3D asset, not just a surface, of a sci-fi crate. | `generation_3d` |
| 451 | Generate a complete 3D model of a robot drone. | `generation_3d` |
| 452 | Create a GLB asset of a space console. | `generation_3d` |
| 453 | Make a game-ready mesh for a sci-fi crate. | `generation_3d` |
| 454 | Produce a full 3D prop: market stall. | `generation_3d` |
| 455 | Generate a low-poly 3D object of a stone arch. | `generation_3d` |
| 456 | Create a complete scene object model: medieval sword. | `generation_3d` |
| 457 | Make a textured 3D asset of a dungeon door. | `generation_3d` |
| 458 | Generate a 3D mesh suitable for Unity: fantasy shield. | `generation_3d` |
| 459 | Create a full object model for a low-poly tree stump. | `generation_3d` |
| 460 | Produce a complete 3D asset, not just a surface, of a wooden barrel. | `generation_3d` |
| 461 | Generate a complete 3D model of a fantasy shield. | `generation_3d` |
| 462 | Create a GLB asset of a low-poly tree stump. | `generation_3d` |
| 463 | Make a game-ready mesh for a wooden barrel. | `generation_3d` |
| 464 | Produce a full 3D prop: robot drone. | `generation_3d` |
| 465 | Generate a low-poly 3D object of a space console. | `generation_3d` |
| 466 | Create a complete scene object model: sci-fi crate. | `generation_3d` |
| 467 | Make a textured 3D asset of a market stall. | `generation_3d` |
| 468 | Generate a 3D mesh suitable for Unity: stone arch. | `generation_3d` |
| 469 | Create a full object model for a medieval sword. | `generation_3d` |
| 470 | Produce a complete 3D asset, not just a surface, of a dungeon door. | `generation_3d` |
| 471 | Generate a complete 3D model of a stone arch. | `generation_3d` |
| 472 | Create a GLB asset of a medieval sword. | `generation_3d` |
| 473 | Make a game-ready mesh for a dungeon door. | `generation_3d` |
| 474 | Produce a full 3D prop: fantasy shield. | `generation_3d` |
| 475 | Generate a low-poly 3D object of a low-poly tree stump. | `generation_3d` |
| 476 | Create a complete scene object model: wooden barrel. | `generation_3d` |
| 477 | Make a textured 3D asset of a robot drone. | `generation_3d` |
| 478 | Generate a 3D mesh suitable for Unity: space console. | `generation_3d` |
| 479 | Create a full object model for a sci-fi crate. | `generation_3d` |
| 480 | Produce a complete 3D asset, not just a surface, of a market stall. | `generation_3d` |
| 481 | Generate a complete 3D model of a space console. | `generation_3d` |
| 482 | Create a GLB asset of a sci-fi crate. | `generation_3d` |
| 483 | Make a game-ready mesh for a market stall. | `generation_3d` |
| 484 | Produce a full 3D prop: stone arch. | `generation_3d` |
| 485 | Generate a low-poly 3D object of a medieval sword. | `generation_3d` |
| 486 | Create a complete scene object model: dungeon door. | `generation_3d` |
| 487 | Make a textured 3D asset of a fantasy shield. | `generation_3d` |
| 488 | Generate a 3D mesh suitable for Unity: low-poly tree stump. | `generation_3d` |
| 489 | Create a full object model for a wooden barrel. | `generation_3d` |
| 490 | Produce a complete 3D asset, not just a surface, of a robot drone. | `generation_3d` |
| 491 | Generate a complete 3D model of a low-poly tree stump. | `generation_3d` |
| 492 | Create a GLB asset of a wooden barrel. | `generation_3d` |
| 493 | Make a game-ready mesh for a robot drone. | `generation_3d` |
| 494 | Produce a full 3D prop: space console. | `generation_3d` |
| 495 | Generate a low-poly 3D object of a sci-fi crate. | `generation_3d` |
| 496 | Create a complete scene object model: market stall. | `generation_3d` |
| 497 | Make a textured 3D asset of a stone arch. | `generation_3d` |
| 498 | Generate a 3D mesh suitable for Unity: medieval sword. | `generation_3d` |
| 499 | Create a full object model for a dungeon door. | `generation_3d` |
| 500 | Produce a complete 3D asset, not just a surface, of a fantasy shield. | `generation_3d` |
| 501 | Generate a rainy forest ambience. | `sound_generation` |
| 502 | Create a game-ready audio clip for magic spell impact sound. | `sound_generation` |
| 503 | Produce a non-speech sound asset: monster roar. | `sound_generation` |
| 504 | Make an ambience loop of explosion impact sound. | `sound_generation` |
| 505 | Design an SFX cue for heavy robot footsteps on metal. | `sound_generation` |
| 506 | Create Foley audio for wooden door creak. | `sound_generation` |
| 507 | Generate a short sound effect: cave dripping loop. | `sound_generation` |
| 508 | Make an environmental audio loop for laser weapon sound effect. | `sound_generation` |
| 509 | Produce an audio cue for UI confirmation beep. | `sound_generation` |
| 510 | Create a sound effect, not spoken dialogue, for coin pickup audio cue. | `sound_generation` |
| 511 | Generate a laser weapon sound effect. | `sound_generation` |
| 512 | Create a game-ready audio clip for UI confirmation beep. | `sound_generation` |
| 513 | Produce a non-speech sound asset: coin pickup audio cue. | `sound_generation` |
| 514 | Make an ambience loop of rainy forest ambience. | `sound_generation` |
| 515 | Design an SFX cue for magic spell impact sound. | `sound_generation` |
| 516 | Create Foley audio for monster roar. | `sound_generation` |
| 517 | Generate a short sound effect: explosion impact sound. | `sound_generation` |
| 518 | Make an environmental audio loop for heavy robot footsteps on metal. | `sound_generation` |
| 519 | Produce an audio cue for wooden door creak. | `sound_generation` |
| 520 | Create a sound effect, not spoken dialogue, for cave dripping loop. | `sound_generation` |
| 521 | Generate a heavy robot footsteps on metal. | `sound_generation` |
| 522 | Create a game-ready audio clip for wooden door creak. | `sound_generation` |
| 523 | Produce a non-speech sound asset: cave dripping loop. | `sound_generation` |
| 524 | Make an ambience loop of laser weapon sound effect. | `sound_generation` |
| 525 | Design an SFX cue for UI confirmation beep. | `sound_generation` |
| 526 | Create Foley audio for coin pickup audio cue. | `sound_generation` |
| 527 | Generate a short sound effect: rainy forest ambience. | `sound_generation` |
| 528 | Make an environmental audio loop for magic spell impact sound. | `sound_generation` |
| 529 | Produce an audio cue for monster roar. | `sound_generation` |
| 530 | Create a sound effect, not spoken dialogue, for explosion impact sound. | `sound_generation` |
| 531 | Generate a magic spell impact sound. | `sound_generation` |
| 532 | Create a game-ready audio clip for monster roar. | `sound_generation` |
| 533 | Produce a non-speech sound asset: explosion impact sound. | `sound_generation` |
| 534 | Make an ambience loop of heavy robot footsteps on metal. | `sound_generation` |
| 535 | Design an SFX cue for wooden door creak. | `sound_generation` |
| 536 | Create Foley audio for cave dripping loop. | `sound_generation` |
| 537 | Generate a short sound effect: laser weapon sound effect. | `sound_generation` |
| 538 | Make an environmental audio loop for UI confirmation beep. | `sound_generation` |
| 539 | Produce an audio cue for coin pickup audio cue. | `sound_generation` |
| 540 | Create a sound effect, not spoken dialogue, for rainy forest ambience. | `sound_generation` |
| 541 | Generate a UI confirmation beep. | `sound_generation` |
| 542 | Create a game-ready audio clip for coin pickup audio cue. | `sound_generation` |
| 543 | Produce a non-speech sound asset: rainy forest ambience. | `sound_generation` |
| 544 | Make an ambience loop of magic spell impact sound. | `sound_generation` |
| 545 | Design an SFX cue for monster roar. | `sound_generation` |
| 546 | Create Foley audio for explosion impact sound. | `sound_generation` |
| 547 | Generate a short sound effect: heavy robot footsteps on metal. | `sound_generation` |
| 548 | Make an environmental audio loop for wooden door creak. | `sound_generation` |
| 549 | Produce an audio cue for cave dripping loop. | `sound_generation` |
| 550 | Create a sound effect, not spoken dialogue, for laser weapon sound effect. | `sound_generation` |
| 551 | Generate a wooden door creak. | `sound_generation` |
| 552 | Create a game-ready audio clip for cave dripping loop. | `sound_generation` |
| 553 | Produce a non-speech sound asset: laser weapon sound effect. | `sound_generation` |
| 554 | Make an ambience loop of UI confirmation beep. | `sound_generation` |
| 555 | Design an SFX cue for coin pickup audio cue. | `sound_generation` |
| 556 | Create Foley audio for rainy forest ambience. | `sound_generation` |
| 557 | Generate a short sound effect: magic spell impact sound. | `sound_generation` |
| 558 | Make an environmental audio loop for monster roar. | `sound_generation` |
| 559 | Produce an audio cue for explosion impact sound. | `sound_generation` |
| 560 | Create a sound effect, not spoken dialogue, for heavy robot footsteps on metal. | `sound_generation` |
| 561 | Generate a monster roar. | `sound_generation` |
| 562 | Create a game-ready audio clip for explosion impact sound. | `sound_generation` |
| 563 | Produce a non-speech sound asset: heavy robot footsteps on metal. | `sound_generation` |
| 564 | Make an ambience loop of wooden door creak. | `sound_generation` |
| 565 | Design an SFX cue for cave dripping loop. | `sound_generation` |
| 566 | Create Foley audio for laser weapon sound effect. | `sound_generation` |
| 567 | Generate a short sound effect: UI confirmation beep. | `sound_generation` |
| 568 | Make an environmental audio loop for coin pickup audio cue. | `sound_generation` |
| 569 | Produce an audio cue for rainy forest ambience. | `sound_generation` |
| 570 | Create a sound effect, not spoken dialogue, for magic spell impact sound. | `sound_generation` |
| 571 | Generate a coin pickup audio cue. | `sound_generation` |
| 572 | Create a game-ready audio clip for rainy forest ambience. | `sound_generation` |
| 573 | Produce a non-speech sound asset: magic spell impact sound. | `sound_generation` |
| 574 | Make an ambience loop of monster roar. | `sound_generation` |
| 575 | Design an SFX cue for explosion impact sound. | `sound_generation` |
| 576 | Create Foley audio for heavy robot footsteps on metal. | `sound_generation` |
| 577 | Generate a short sound effect: wooden door creak. | `sound_generation` |
| 578 | Make an environmental audio loop for cave dripping loop. | `sound_generation` |
| 579 | Produce an audio cue for laser weapon sound effect. | `sound_generation` |
| 580 | Create a sound effect, not spoken dialogue, for UI confirmation beep. | `sound_generation` |
| 581 | Generate a cave dripping loop. | `sound_generation` |
| 582 | Create a game-ready audio clip for laser weapon sound effect. | `sound_generation` |
| 583 | Produce a non-speech sound asset: UI confirmation beep. | `sound_generation` |
| 584 | Make an ambience loop of coin pickup audio cue. | `sound_generation` |
| 585 | Design an SFX cue for rainy forest ambience. | `sound_generation` |
| 586 | Create Foley audio for magic spell impact sound. | `sound_generation` |
| 587 | Generate a short sound effect: monster roar. | `sound_generation` |
| 588 | Make an environmental audio loop for explosion impact sound. | `sound_generation` |
| 589 | Produce an audio cue for heavy robot footsteps on metal. | `sound_generation` |
| 590 | Create a sound effect, not spoken dialogue, for wooden door creak. | `sound_generation` |
| 591 | Generate a explosion impact sound. | `sound_generation` |
| 592 | Create a game-ready audio clip for heavy robot footsteps on metal. | `sound_generation` |
| 593 | Produce a non-speech sound asset: wooden door creak. | `sound_generation` |
| 594 | Make an ambience loop of cave dripping loop. | `sound_generation` |
| 595 | Design an SFX cue for laser weapon sound effect. | `sound_generation` |
| 596 | Create Foley audio for UI confirmation beep. | `sound_generation` |
| 597 | Generate a short sound effect: coin pickup audio cue. | `sound_generation` |
| 598 | Make an environmental audio loop for rainy forest ambience. | `sound_generation` |
| 599 | Produce an audio cue for magic spell impact sound. | `sound_generation` |
| 600 | Create a sound effect, not spoken dialogue, for monster roar. | `sound_generation` |
| 601 | Generate a rusty metal material. | `texture_generation` |
| 602 | Create a surface texture for cracked concrete normal map. | `texture_generation` |
| 603 | Make a PBR material: muddy terrain texture. | `texture_generation` |
| 604 | Produce a tileable texture of painted metal roughness map. | `texture_generation` |
| 605 | Generate a material-only asset for old wooden floor material. | `texture_generation` |
| 606 | Create a texture map set for sci-fi panel decal. | `texture_generation` |
| 607 | Make a seamless material for icy cave wall texture. | `texture_generation` |
| 608 | Generate surface appearance only: seamless stone wall texture. | `texture_generation` |
| 609 | Create a decal or material map for mossy brick PBR material. | `texture_generation` |
| 610 | Produce a texture, not a 3D mesh, for worn leather material. | `texture_generation` |
| 611 | Generate a seamless stone wall texture. | `texture_generation` |
| 612 | Create a surface texture for mossy brick PBR material. | `texture_generation` |
| 613 | Make a PBR material: worn leather material. | `texture_generation` |
| 614 | Produce a tileable texture of rusty metal material. | `texture_generation` |
| 615 | Generate a material-only asset for cracked concrete normal map. | `texture_generation` |
| 616 | Create a texture map set for muddy terrain texture. | `texture_generation` |
| 617 | Make a seamless material for painted metal roughness map. | `texture_generation` |
| 618 | Generate surface appearance only: old wooden floor material. | `texture_generation` |
| 619 | Create a decal or material map for sci-fi panel decal. | `texture_generation` |
| 620 | Produce a texture, not a 3D mesh, for icy cave wall texture. | `texture_generation` |
| 621 | Generate a old wooden floor material. | `texture_generation` |
| 622 | Create a surface texture for sci-fi panel decal. | `texture_generation` |
| 623 | Make a PBR material: icy cave wall texture. | `texture_generation` |
| 624 | Produce a tileable texture of seamless stone wall texture. | `texture_generation` |
| 625 | Generate a material-only asset for mossy brick PBR material. | `texture_generation` |
| 626 | Create a texture map set for worn leather material. | `texture_generation` |
| 627 | Make a seamless material for rusty metal material. | `texture_generation` |
| 628 | Generate surface appearance only: cracked concrete normal map. | `texture_generation` |
| 629 | Create a decal or material map for muddy terrain texture. | `texture_generation` |
| 630 | Produce a texture, not a 3D mesh, for painted metal roughness map. | `texture_generation` |
| 631 | Generate a cracked concrete normal map. | `texture_generation` |
| 632 | Create a surface texture for muddy terrain texture. | `texture_generation` |
| 633 | Make a PBR material: painted metal roughness map. | `texture_generation` |
| 634 | Produce a tileable texture of old wooden floor material. | `texture_generation` |
| 635 | Generate a material-only asset for sci-fi panel decal. | `texture_generation` |
| 636 | Create a texture map set for icy cave wall texture. | `texture_generation` |
| 637 | Make a seamless material for seamless stone wall texture. | `texture_generation` |
| 638 | Generate surface appearance only: mossy brick PBR material. | `texture_generation` |
| 639 | Create a decal or material map for worn leather material. | `texture_generation` |
| 640 | Produce a texture, not a 3D mesh, for rusty metal material. | `texture_generation` |
| 641 | Generate a mossy brick PBR material. | `texture_generation` |
| 642 | Create a surface texture for worn leather material. | `texture_generation` |
| 643 | Make a PBR material: rusty metal material. | `texture_generation` |
| 644 | Produce a tileable texture of cracked concrete normal map. | `texture_generation` |
| 645 | Generate a material-only asset for muddy terrain texture. | `texture_generation` |
| 646 | Create a texture map set for painted metal roughness map. | `texture_generation` |
| 647 | Make a seamless material for old wooden floor material. | `texture_generation` |
| 648 | Generate surface appearance only: sci-fi panel decal. | `texture_generation` |
| 649 | Create a decal or material map for icy cave wall texture. | `texture_generation` |
| 650 | Produce a texture, not a 3D mesh, for seamless stone wall texture. | `texture_generation` |
| 651 | Generate a sci-fi panel decal. | `texture_generation` |
| 652 | Create a surface texture for icy cave wall texture. | `texture_generation` |
| 653 | Make a PBR material: seamless stone wall texture. | `texture_generation` |
| 654 | Produce a tileable texture of mossy brick PBR material. | `texture_generation` |
| 655 | Generate a material-only asset for worn leather material. | `texture_generation` |
| 656 | Create a texture map set for rusty metal material. | `texture_generation` |
| 657 | Make a seamless material for cracked concrete normal map. | `texture_generation` |
| 658 | Generate surface appearance only: muddy terrain texture. | `texture_generation` |
| 659 | Create a decal or material map for painted metal roughness map. | `texture_generation` |
| 660 | Produce a texture, not a 3D mesh, for old wooden floor material. | `texture_generation` |
| 661 | Generate a muddy terrain texture. | `texture_generation` |
| 662 | Create a surface texture for painted metal roughness map. | `texture_generation` |
| 663 | Make a PBR material: old wooden floor material. | `texture_generation` |
| 664 | Produce a tileable texture of sci-fi panel decal. | `texture_generation` |
| 665 | Generate a material-only asset for icy cave wall texture. | `texture_generation` |
| 666 | Create a texture map set for seamless stone wall texture. | `texture_generation` |
| 667 | Make a seamless material for mossy brick PBR material. | `texture_generation` |
| 668 | Generate surface appearance only: worn leather material. | `texture_generation` |
| 669 | Create a decal or material map for rusty metal material. | `texture_generation` |
| 670 | Produce a texture, not a 3D mesh, for cracked concrete normal map. | `texture_generation` |
| 671 | Generate a worn leather material. | `texture_generation` |
| 672 | Create a surface texture for rusty metal material. | `texture_generation` |
| 673 | Make a PBR material: cracked concrete normal map. | `texture_generation` |
| 674 | Produce a tileable texture of muddy terrain texture. | `texture_generation` |
| 675 | Generate a material-only asset for painted metal roughness map. | `texture_generation` |
| 676 | Create a texture map set for old wooden floor material. | `texture_generation` |
| 677 | Make a seamless material for sci-fi panel decal. | `texture_generation` |
| 678 | Generate surface appearance only: icy cave wall texture. | `texture_generation` |
| 679 | Create a decal or material map for seamless stone wall texture. | `texture_generation` |
| 680 | Produce a texture, not a 3D mesh, for mossy brick PBR material. | `texture_generation` |
| 681 | Generate a icy cave wall texture. | `texture_generation` |
| 682 | Create a surface texture for seamless stone wall texture. | `texture_generation` |
| 683 | Make a PBR material: mossy brick PBR material. | `texture_generation` |
| 684 | Produce a tileable texture of worn leather material. | `texture_generation` |
| 685 | Generate a material-only asset for rusty metal material. | `texture_generation` |
| 686 | Create a texture map set for cracked concrete normal map. | `texture_generation` |
| 687 | Make a seamless material for muddy terrain texture. | `texture_generation` |
| 688 | Generate surface appearance only: painted metal roughness map. | `texture_generation` |
| 689 | Create a decal or material map for old wooden floor material. | `texture_generation` |
| 690 | Produce a texture, not a 3D mesh, for sci-fi panel decal. | `texture_generation` |
| 691 | Generate a painted metal roughness map. | `texture_generation` |
| 692 | Create a surface texture for old wooden floor material. | `texture_generation` |
| 693 | Make a PBR material: sci-fi panel decal. | `texture_generation` |
| 694 | Produce a tileable texture of icy cave wall texture. | `texture_generation` |
| 695 | Generate a material-only asset for seamless stone wall texture. | `texture_generation` |
| 696 | Create a texture map set for mossy brick PBR material. | `texture_generation` |
| 697 | Make a seamless material for worn leather material. | `texture_generation` |
| 698 | Generate surface appearance only: rusty metal material. | `texture_generation` |
| 699 | Create a decal or material map for cracked concrete normal map. | `texture_generation` |
| 700 | Produce a texture, not a 3D mesh, for muddy terrain texture. | `texture_generation` |
| 701 | Convert this uploaded image into a 3D model. | `image_to_3d_generation` |
| 702 | Turn the uploaded concept art into a GLB asset. | `image_to_3d_generation` |
| 703 | Create a 3D mesh from this picture. | `image_to_3d_generation` |
| 704 | Generate a 3D model using the provided drawing. | `image_to_3d_generation` |
| 705 | Reconstruct a game-ready asset from this sketch. | `image_to_3d_generation` |
| 706 | Make a textured 3D object from the line drawing. | `image_to_3d_generation` |
| 707 | Use this visual reference as input for image-to-3D generation. | `image_to_3d_generation` |
| 708 | Build a full 3D model from the reference photo. | `image_to_3d_generation` |
| 709 | Transform this screenshot into a game-ready 3D asset. | `image_to_3d_generation` |
| 710 | Generate geometry from the provided reference image. | `image_to_3d_generation` |
| 711 | Convert this reference photo into a 3D model. | `image_to_3d_generation` |
| 712 | Turn the uploaded screenshot into a GLB asset. | `image_to_3d_generation` |
| 713 | Create a 3D mesh from this reference image. | `image_to_3d_generation` |
| 714 | Generate a 3D model using the provided uploaded image. | `image_to_3d_generation` |
| 715 | Reconstruct a game-ready asset from this concept art. | `image_to_3d_generation` |
| 716 | Make a textured 3D object from the picture. | `image_to_3d_generation` |
| 717 | Use this drawing as input for image-to-3D generation. | `image_to_3d_generation` |
| 718 | Build a full 3D model from the sketch. | `image_to_3d_generation` |
| 719 | Transform this line drawing into a game-ready 3D asset. | `image_to_3d_generation` |
| 720 | Generate geometry from the provided visual reference. | `image_to_3d_generation` |
| 721 | Convert this sketch into a 3D model. | `image_to_3d_generation` |
| 722 | Turn the uploaded line drawing into a GLB asset. | `image_to_3d_generation` |
| 723 | Create a 3D mesh from this visual reference. | `image_to_3d_generation` |
| 724 | Generate a 3D model using the provided reference photo. | `image_to_3d_generation` |
| 725 | Reconstruct a game-ready asset from this screenshot. | `image_to_3d_generation` |
| 726 | Make a textured 3D object from the reference image. | `image_to_3d_generation` |
| 727 | Use this uploaded image as input for image-to-3D generation. | `image_to_3d_generation` |
| 728 | Build a full 3D model from the concept art. | `image_to_3d_generation` |
| 729 | Transform this picture into a game-ready 3D asset. | `image_to_3d_generation` |
| 730 | Generate geometry from the provided drawing. | `image_to_3d_generation` |
| 731 | Convert this concept art into a 3D model. | `image_to_3d_generation` |
| 732 | Turn the uploaded picture into a GLB asset. | `image_to_3d_generation` |
| 733 | Create a 3D mesh from this drawing. | `image_to_3d_generation` |
| 734 | Generate a 3D model using the provided sketch. | `image_to_3d_generation` |
| 735 | Reconstruct a game-ready asset from this line drawing. | `image_to_3d_generation` |
| 736 | Make a textured 3D object from the visual reference. | `image_to_3d_generation` |
| 737 | Use this reference photo as input for image-to-3D generation. | `image_to_3d_generation` |
| 738 | Build a full 3D model from the screenshot. | `image_to_3d_generation` |
| 739 | Transform this reference image into a game-ready 3D asset. | `image_to_3d_generation` |
| 740 | Generate geometry from the provided uploaded image. | `image_to_3d_generation` |
| 741 | Convert this screenshot into a 3D model. | `image_to_3d_generation` |
| 742 | Turn the uploaded reference image into a GLB asset. | `image_to_3d_generation` |
| 743 | Create a 3D mesh from this uploaded image. | `image_to_3d_generation` |
| 744 | Generate a 3D model using the provided concept art. | `image_to_3d_generation` |
| 745 | Reconstruct a game-ready asset from this picture. | `image_to_3d_generation` |
| 746 | Make a textured 3D object from the drawing. | `image_to_3d_generation` |
| 747 | Use this sketch as input for image-to-3D generation. | `image_to_3d_generation` |
| 748 | Build a full 3D model from the line drawing. | `image_to_3d_generation` |
| 749 | Transform this visual reference into a game-ready 3D asset. | `image_to_3d_generation` |
| 750 | Generate geometry from the provided reference photo. | `image_to_3d_generation` |
| 751 | Convert this line drawing into a 3D model. | `image_to_3d_generation` |
| 752 | Turn the uploaded visual reference into a GLB asset. | `image_to_3d_generation` |
| 753 | Create a 3D mesh from this reference photo. | `image_to_3d_generation` |
| 754 | Generate a 3D model using the provided screenshot. | `image_to_3d_generation` |
| 755 | Reconstruct a game-ready asset from this reference image. | `image_to_3d_generation` |
| 756 | Make a textured 3D object from the uploaded image. | `image_to_3d_generation` |
| 757 | Use this concept art as input for image-to-3D generation. | `image_to_3d_generation` |
| 758 | Build a full 3D model from the picture. | `image_to_3d_generation` |
| 759 | Transform this drawing into a game-ready 3D asset. | `image_to_3d_generation` |
| 760 | Generate geometry from the provided sketch. | `image_to_3d_generation` |
| 761 | Convert this picture into a 3D model. | `image_to_3d_generation` |
| 762 | Turn the uploaded drawing into a GLB asset. | `image_to_3d_generation` |
| 763 | Create a 3D mesh from this sketch. | `image_to_3d_generation` |
| 764 | Generate a 3D model using the provided line drawing. | `image_to_3d_generation` |
| 765 | Reconstruct a game-ready asset from this visual reference. | `image_to_3d_generation` |
| 766 | Make a textured 3D object from the reference photo. | `image_to_3d_generation` |
| 767 | Use this screenshot as input for image-to-3D generation. | `image_to_3d_generation` |
| 768 | Build a full 3D model from the reference image. | `image_to_3d_generation` |
| 769 | Transform this uploaded image into a game-ready 3D asset. | `image_to_3d_generation` |
| 770 | Generate geometry from the provided concept art. | `image_to_3d_generation` |
| 771 | Convert this reference image into a 3D model. | `image_to_3d_generation` |
| 772 | Turn the uploaded uploaded image into a GLB asset. | `image_to_3d_generation` |
| 773 | Create a 3D mesh from this concept art. | `image_to_3d_generation` |
| 774 | Generate a 3D model using the provided picture. | `image_to_3d_generation` |
| 775 | Reconstruct a game-ready asset from this drawing. | `image_to_3d_generation` |
| 776 | Make a textured 3D object from the sketch. | `image_to_3d_generation` |
| 777 | Use this line drawing as input for image-to-3D generation. | `image_to_3d_generation` |
| 778 | Build a full 3D model from the visual reference. | `image_to_3d_generation` |
| 779 | Transform this reference photo into a game-ready 3D asset. | `image_to_3d_generation` |
| 780 | Generate geometry from the provided screenshot. | `image_to_3d_generation` |
| 781 | Convert this visual reference into a 3D model. | `image_to_3d_generation` |
| 782 | Turn the uploaded reference photo into a GLB asset. | `image_to_3d_generation` |
| 783 | Create a 3D mesh from this screenshot. | `image_to_3d_generation` |
| 784 | Generate a 3D model using the provided reference image. | `image_to_3d_generation` |
| 785 | Reconstruct a game-ready asset from this uploaded image. | `image_to_3d_generation` |
| 786 | Make a textured 3D object from the concept art. | `image_to_3d_generation` |
| 787 | Use this picture as input for image-to-3D generation. | `image_to_3d_generation` |
| 788 | Build a full 3D model from the drawing. | `image_to_3d_generation` |
| 789 | Transform this sketch into a game-ready 3D asset. | `image_to_3d_generation` |
| 790 | Generate geometry from the provided line drawing. | `image_to_3d_generation` |
| 791 | Convert this drawing into a 3D model. | `image_to_3d_generation` |
| 792 | Turn the uploaded sketch into a GLB asset. | `image_to_3d_generation` |
| 793 | Create a 3D mesh from this line drawing. | `image_to_3d_generation` |
| 794 | Generate a 3D model using the provided visual reference. | `image_to_3d_generation` |
| 795 | Reconstruct a game-ready asset from this reference photo. | `image_to_3d_generation` |
| 796 | Make a textured 3D object from the screenshot. | `image_to_3d_generation` |
| 797 | Use this reference image as input for image-to-3D generation. | `image_to_3d_generation` |
| 798 | Build a full 3D model from the uploaded image. | `image_to_3d_generation` |
| 799 | Transform this concept art into a game-ready 3D asset. | `image_to_3d_generation` |
| 800 | Generate geometry from the provided picture. | `image_to_3d_generation` |
| 801 | Generate a walking animation for a guard. | `motion_generation` |
| 802 | Create an animation clip for sword attack animation. | `motion_generation` |
| 803 | Make skeletal motion for dodge roll animation. | `motion_generation` |
| 804 | Produce a character motion clip: door-opening interaction animation. | `motion_generation` |
| 805 | Generate a locomotion cycle: idle breathing animation for a shopkeeper. | `motion_generation` |
| 806 | Create a rigged animation for jump landing motion clip. | `motion_generation` |
| 807 | Make a game-ready motion asset for dance emote. | `motion_generation` |
| 808 | Generate keyframe animation for run cycle for a robot. | `motion_generation` |
| 809 | Create character movement for VR avatar wave gesture. | `motion_generation` |
| 810 | Produce an animation, not a 3D model, for spell-casting hand motion. | `motion_generation` |
| 811 | Generate a run cycle for a robot. | `motion_generation` |
| 812 | Create an animation clip for VR avatar wave gesture. | `motion_generation` |
| 813 | Make skeletal motion for spell-casting hand motion. | `motion_generation` |
| 814 | Produce a character motion clip: walking animation for a guard. | `motion_generation` |
| 815 | Generate a locomotion cycle: sword attack animation. | `motion_generation` |
| 816 | Create a rigged animation for dodge roll animation. | `motion_generation` |
| 817 | Make a game-ready motion asset for door-opening interaction animation. | `motion_generation` |
| 818 | Generate keyframe animation for idle breathing animation for a shopkeeper. | `motion_generation` |
| 819 | Create character movement for jump landing motion clip. | `motion_generation` |
| 820 | Produce an animation, not a 3D model, for dance emote. | `motion_generation` |
| 821 | Generate a idle breathing animation for a shopkeeper. | `motion_generation` |
| 822 | Create an animation clip for jump landing motion clip. | `motion_generation` |
| 823 | Make skeletal motion for dance emote. | `motion_generation` |
| 824 | Produce a character motion clip: run cycle for a robot. | `motion_generation` |
| 825 | Generate a locomotion cycle: VR avatar wave gesture. | `motion_generation` |
| 826 | Create a rigged animation for spell-casting hand motion. | `motion_generation` |
| 827 | Make a game-ready motion asset for walking animation for a guard. | `motion_generation` |
| 828 | Generate keyframe animation for sword attack animation. | `motion_generation` |
| 829 | Create character movement for dodge roll animation. | `motion_generation` |
| 830 | Produce an animation, not a 3D model, for door-opening interaction animation. | `motion_generation` |
| 831 | Generate a sword attack animation. | `motion_generation` |
| 832 | Create an animation clip for dodge roll animation. | `motion_generation` |
| 833 | Make skeletal motion for door-opening interaction animation. | `motion_generation` |
| 834 | Produce a character motion clip: idle breathing animation for a shopkeeper. | `motion_generation` |
| 835 | Generate a locomotion cycle: jump landing motion clip. | `motion_generation` |
| 836 | Create a rigged animation for dance emote. | `motion_generation` |
| 837 | Make a game-ready motion asset for run cycle for a robot. | `motion_generation` |
| 838 | Generate keyframe animation for VR avatar wave gesture. | `motion_generation` |
| 839 | Create character movement for spell-casting hand motion. | `motion_generation` |
| 840 | Produce an animation, not a 3D model, for walking animation for a guard. | `motion_generation` |
| 841 | Generate a VR avatar wave gesture. | `motion_generation` |
| 842 | Create an animation clip for spell-casting hand motion. | `motion_generation` |
| 843 | Make skeletal motion for walking animation for a guard. | `motion_generation` |
| 844 | Produce a character motion clip: sword attack animation. | `motion_generation` |
| 845 | Generate a locomotion cycle: dodge roll animation. | `motion_generation` |
| 846 | Create a rigged animation for door-opening interaction animation. | `motion_generation` |
| 847 | Make a game-ready motion asset for idle breathing animation for a shopkeeper. | `motion_generation` |
| 848 | Generate keyframe animation for jump landing motion clip. | `motion_generation` |
| 849 | Create character movement for dance emote. | `motion_generation` |
| 850 | Produce an animation, not a 3D model, for run cycle for a robot. | `motion_generation` |
| 851 | Generate a jump landing motion clip. | `motion_generation` |
| 852 | Create an animation clip for dance emote. | `motion_generation` |
| 853 | Make skeletal motion for run cycle for a robot. | `motion_generation` |
| 854 | Produce a character motion clip: VR avatar wave gesture. | `motion_generation` |
| 855 | Generate a locomotion cycle: spell-casting hand motion. | `motion_generation` |
| 856 | Create a rigged animation for walking animation for a guard. | `motion_generation` |
| 857 | Make a game-ready motion asset for sword attack animation. | `motion_generation` |
| 858 | Generate keyframe animation for dodge roll animation. | `motion_generation` |
| 859 | Create character movement for door-opening interaction animation. | `motion_generation` |
| 860 | Produce an animation, not a 3D model, for idle breathing animation for a shopkeeper. | `motion_generation` |
| 861 | Generate a dodge roll animation. | `motion_generation` |
| 862 | Create an animation clip for door-opening interaction animation. | `motion_generation` |
| 863 | Make skeletal motion for idle breathing animation for a shopkeeper. | `motion_generation` |
| 864 | Produce a character motion clip: jump landing motion clip. | `motion_generation` |
| 865 | Generate a locomotion cycle: dance emote. | `motion_generation` |
| 866 | Create a rigged animation for run cycle for a robot. | `motion_generation` |
| 867 | Make a game-ready motion asset for VR avatar wave gesture. | `motion_generation` |
| 868 | Generate keyframe animation for spell-casting hand motion. | `motion_generation` |
| 869 | Create character movement for walking animation for a guard. | `motion_generation` |
| 870 | Produce an animation, not a 3D model, for sword attack animation. | `motion_generation` |
| 871 | Generate a spell-casting hand motion. | `motion_generation` |
| 872 | Create an animation clip for walking animation for a guard. | `motion_generation` |
| 873 | Make skeletal motion for sword attack animation. | `motion_generation` |
| 874 | Produce a character motion clip: dodge roll animation. | `motion_generation` |
| 875 | Generate a locomotion cycle: door-opening interaction animation. | `motion_generation` |
| 876 | Create a rigged animation for idle breathing animation for a shopkeeper. | `motion_generation` |
| 877 | Make a game-ready motion asset for jump landing motion clip. | `motion_generation` |
| 878 | Generate keyframe animation for dance emote. | `motion_generation` |
| 879 | Create character movement for run cycle for a robot. | `motion_generation` |
| 880 | Produce an animation, not a 3D model, for VR avatar wave gesture. | `motion_generation` |
| 881 | Generate a dance emote. | `motion_generation` |
| 882 | Create an animation clip for run cycle for a robot. | `motion_generation` |
| 883 | Make skeletal motion for VR avatar wave gesture. | `motion_generation` |
| 884 | Produce a character motion clip: spell-casting hand motion. | `motion_generation` |
| 885 | Generate a locomotion cycle: walking animation for a guard. | `motion_generation` |
| 886 | Create a rigged animation for sword attack animation. | `motion_generation` |
| 887 | Make a game-ready motion asset for dodge roll animation. | `motion_generation` |
| 888 | Generate keyframe animation for door-opening interaction animation. | `motion_generation` |
| 889 | Create character movement for idle breathing animation for a shopkeeper. | `motion_generation` |
| 890 | Produce an animation, not a 3D model, for jump landing motion clip. | `motion_generation` |
| 891 | Generate a door-opening interaction animation. | `motion_generation` |
| 892 | Create an animation clip for idle breathing animation for a shopkeeper. | `motion_generation` |
| 893 | Make skeletal motion for jump landing motion clip. | `motion_generation` |
| 894 | Produce a character motion clip: dance emote. | `motion_generation` |
| 895 | Generate a locomotion cycle: run cycle for a robot. | `motion_generation` |
| 896 | Create a rigged animation for VR avatar wave gesture. | `motion_generation` |
| 897 | Make a game-ready motion asset for spell-casting hand motion. | `motion_generation` |
| 898 | Generate keyframe animation for walking animation for a guard. | `motion_generation` |
| 899 | Create character movement for sword attack animation. | `motion_generation` |
| 900 | Produce an animation, not a 3D model, for dodge roll animation. | `motion_generation` |
| 901 | Generate spoken audio saying: Welcome to the village. | `text_to_speech` |
| 902 | Create a text-to-speech voice line: Warning, oxygen levels are low. | `text_to_speech` |
| 903 | Synthesize speech for the line: Quest complete. | `text_to_speech` |
| 904 | Produce a narrator voice saying: Training sequence started. | `text_to_speech` |
| 905 | Create NPC dialogue audio: Fresh supplies just arrived. | `text_to_speech` |
| 906 | Generate a voiceover clip that says: Follow the path to the old tower. | `text_to_speech` |
| 907 | Make spoken dialogue for this sentence: The bridge ahead is unstable. | `text_to_speech` |
| 908 | Create speech audio, not ambience, for: The gate is locked. | `text_to_speech` |
| 909 | Synthesize a character voice line: You have discovered an ancient relic. | `text_to_speech` |
| 910 | Generate TTS audio for: I need your help, traveler. | `text_to_speech` |
| 911 | Generate spoken audio saying: The gate is locked. | `text_to_speech` |
| 912 | Create a text-to-speech voice line: You have discovered an ancient relic. | `text_to_speech` |
| 913 | Synthesize speech for the line: I need your help, traveler. | `text_to_speech` |
| 914 | Produce a narrator voice saying: Welcome to the village. | `text_to_speech` |
| 915 | Create NPC dialogue audio: Warning, oxygen levels are low. | `text_to_speech` |
| 916 | Generate a voiceover clip that says: Quest complete. | `text_to_speech` |
| 917 | Make spoken dialogue for this sentence: Training sequence started. | `text_to_speech` |
| 918 | Create speech audio, not ambience, for: Fresh supplies just arrived. | `text_to_speech` |
| 919 | Synthesize a character voice line: Follow the path to the old tower. | `text_to_speech` |
| 920 | Generate TTS audio for: The bridge ahead is unstable. | `text_to_speech` |
| 921 | Generate spoken audio saying: Fresh supplies just arrived. | `text_to_speech` |
| 922 | Create a text-to-speech voice line: Follow the path to the old tower. | `text_to_speech` |
| 923 | Synthesize speech for the line: The bridge ahead is unstable. | `text_to_speech` |
| 924 | Produce a narrator voice saying: The gate is locked. | `text_to_speech` |
| 925 | Create NPC dialogue audio: You have discovered an ancient relic. | `text_to_speech` |
| 926 | Generate a voiceover clip that says: I need your help, traveler. | `text_to_speech` |
| 927 | Make spoken dialogue for this sentence: Welcome to the village. | `text_to_speech` |
| 928 | Create speech audio, not ambience, for: Warning, oxygen levels are low. | `text_to_speech` |
| 929 | Synthesize a character voice line: Quest complete. | `text_to_speech` |
| 930 | Generate TTS audio for: Training sequence started. | `text_to_speech` |
| 931 | Generate spoken audio saying: Warning, oxygen levels are low. | `text_to_speech` |
| 932 | Create a text-to-speech voice line: Quest complete. | `text_to_speech` |
| 933 | Synthesize speech for the line: Training sequence started. | `text_to_speech` |
| 934 | Produce a narrator voice saying: Fresh supplies just arrived. | `text_to_speech` |
| 935 | Create NPC dialogue audio: Follow the path to the old tower. | `text_to_speech` |
| 936 | Generate a voiceover clip that says: The bridge ahead is unstable. | `text_to_speech` |
| 937 | Make spoken dialogue for this sentence: The gate is locked. | `text_to_speech` |
| 938 | Create speech audio, not ambience, for: You have discovered an ancient relic. | `text_to_speech` |
| 939 | Synthesize a character voice line: I need your help, traveler. | `text_to_speech` |
| 940 | Generate TTS audio for: Welcome to the village. | `text_to_speech` |
| 941 | Generate spoken audio saying: You have discovered an ancient relic. | `text_to_speech` |
| 942 | Create a text-to-speech voice line: I need your help, traveler. | `text_to_speech` |
| 943 | Synthesize speech for the line: Welcome to the village. | `text_to_speech` |
| 944 | Produce a narrator voice saying: Warning, oxygen levels are low. | `text_to_speech` |
| 945 | Create NPC dialogue audio: Quest complete. | `text_to_speech` |
| 946 | Generate a voiceover clip that says: Training sequence started. | `text_to_speech` |
| 947 | Make spoken dialogue for this sentence: Fresh supplies just arrived. | `text_to_speech` |
| 948 | Create speech audio, not ambience, for: Follow the path to the old tower. | `text_to_speech` |
| 949 | Synthesize a character voice line: The bridge ahead is unstable. | `text_to_speech` |
| 950 | Generate TTS audio for: The gate is locked. | `text_to_speech` |
| 951 | Generate spoken audio saying: Follow the path to the old tower. | `text_to_speech` |
| 952 | Create a text-to-speech voice line: The bridge ahead is unstable. | `text_to_speech` |
| 953 | Synthesize speech for the line: The gate is locked. | `text_to_speech` |
| 954 | Produce a narrator voice saying: You have discovered an ancient relic. | `text_to_speech` |
| 955 | Create NPC dialogue audio: I need your help, traveler. | `text_to_speech` |
| 956 | Generate a voiceover clip that says: Welcome to the village. | `text_to_speech` |
| 957 | Make spoken dialogue for this sentence: Warning, oxygen levels are low. | `text_to_speech` |
| 958 | Create speech audio, not ambience, for: Quest complete. | `text_to_speech` |
| 959 | Synthesize a character voice line: Training sequence started. | `text_to_speech` |
| 960 | Generate TTS audio for: Fresh supplies just arrived. | `text_to_speech` |
| 961 | Generate spoken audio saying: Quest complete. | `text_to_speech` |
| 962 | Create a text-to-speech voice line: Training sequence started. | `text_to_speech` |
| 963 | Synthesize speech for the line: Fresh supplies just arrived. | `text_to_speech` |
| 964 | Produce a narrator voice saying: Follow the path to the old tower. | `text_to_speech` |
| 965 | Create NPC dialogue audio: The bridge ahead is unstable. | `text_to_speech` |
| 966 | Generate a voiceover clip that says: The gate is locked. | `text_to_speech` |
| 967 | Make spoken dialogue for this sentence: You have discovered an ancient relic. | `text_to_speech` |
| 968 | Create speech audio, not ambience, for: I need your help, traveler. | `text_to_speech` |
| 969 | Synthesize a character voice line: Welcome to the village. | `text_to_speech` |
| 970 | Generate TTS audio for: Warning, oxygen levels are low. | `text_to_speech` |
| 971 | Generate spoken audio saying: I need your help, traveler. | `text_to_speech` |
| 972 | Create a text-to-speech voice line: Welcome to the village. | `text_to_speech` |
| 973 | Synthesize speech for the line: Warning, oxygen levels are low. | `text_to_speech` |
| 974 | Produce a narrator voice saying: Quest complete. | `text_to_speech` |
| 975 | Create NPC dialogue audio: Training sequence started. | `text_to_speech` |
| 976 | Generate a voiceover clip that says: Fresh supplies just arrived. | `text_to_speech` |
| 977 | Make spoken dialogue for this sentence: Follow the path to the old tower. | `text_to_speech` |
| 978 | Create speech audio, not ambience, for: The bridge ahead is unstable. | `text_to_speech` |
| 979 | Synthesize a character voice line: The gate is locked. | `text_to_speech` |
| 980 | Generate TTS audio for: You have discovered an ancient relic. | `text_to_speech` |
| 981 | Generate spoken audio saying: The bridge ahead is unstable. | `text_to_speech` |
| 982 | Create a text-to-speech voice line: The gate is locked. | `text_to_speech` |
| 983 | Synthesize speech for the line: You have discovered an ancient relic. | `text_to_speech` |
| 984 | Produce a narrator voice saying: I need your help, traveler. | `text_to_speech` |
| 985 | Create NPC dialogue audio: Welcome to the village. | `text_to_speech` |
| 986 | Generate a voiceover clip that says: Warning, oxygen levels are low. | `text_to_speech` |
| 987 | Make spoken dialogue for this sentence: Quest complete. | `text_to_speech` |
| 988 | Create speech audio, not ambience, for: Training sequence started. | `text_to_speech` |
| 989 | Synthesize a character voice line: Fresh supplies just arrived. | `text_to_speech` |
| 990 | Generate TTS audio for: Follow the path to the old tower. | `text_to_speech` |
| 991 | Generate spoken audio saying: Training sequence started. | `text_to_speech` |
| 992 | Create a text-to-speech voice line: Fresh supplies just arrived. | `text_to_speech` |
| 993 | Synthesize speech for the line: Follow the path to the old tower. | `text_to_speech` |
| 994 | Produce a narrator voice saying: The bridge ahead is unstable. | `text_to_speech` |
| 995 | Create NPC dialogue audio: The gate is locked. | `text_to_speech` |
| 996 | Generate a voiceover clip that says: You have discovered an ancient relic. | `text_to_speech` |
| 997 | Make spoken dialogue for this sentence: I need your help, traveler. | `text_to_speech` |
| 998 | Create speech audio, not ambience, for: Welcome to the village. | `text_to_speech` |
| 999 | Synthesize a character voice line: Warning, oxygen levels are low. | `text_to_speech` |
| 1000 | Generate TTS audio for: Quest complete. | `text_to_speech` |


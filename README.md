Game name: AVOID AND RUN
Unreal Engine version: 5.7
Controls:
Movement is AWSD; Shift = sprint; Space = Jump; Ctrl = Dash; Max walk speed 800(speed of the character); Breaking deceleration walking 5000(regulates how fast the character will stop); Jump Z velocity 500(Velocity when jumping)
For launching game download an archive containing game build and run an AvoidANDRun.exe 
Blueprints and their purpose:
BP_MainChar; Purpose: regulation of events + movement + collision
BP_Enemy; Purpose:self-explanatory(enemy with sphere collision, which ends game if overlap with player); speed 1200(exposed variable)
BP_GMBase - game mode; Purpose: calculate current score, calculate and save best score
BPI_GameMode - Blueprint interface which helps BP_GMBase
PC_MainChar - Player Controller; Purpose: work with HUD and Graphic settings
BP_SaveGame - save game object; Purpose: save best score
BP_Coin; Purpose: collectible item with an overlap logic, we're using cast to BP_MainChar because it's only works if MainChar picks up a coin
AI_Controller + BT_Enemy + BB_Enemy + BTT_get patrol Location + EQS_Coin; Purpose: controlling AI behaviour(sight radius 1500, lose radius 2000; sight con fig in AI perception), chase, patrol + choosing coin locations
WBP_Death + WBP_Settings + WBP_MainMenu + WBP_PauseMenu + WBP_Score + WBP_Victory; Purpose: Widgets for victory, death, pause, changing graphics/audio, show current/best score; We're using event updates architecture instead of per frame binding, because it's much cheaper for optimization;

Optimization: 60 fps at any graphics; illumination takes the most resources;
Stat UNIT: 59.73 FPS, 16.74 ms, Frame: 16.67 ms, Game: 10.65 ms, Draw: 6.13 ms, RHIT: 3.17 ms, GPU Time: 16.71 ms, Input: 16.80 ms, Mem: 1.32 GB, RenderRes: 91.2% (1300x737, Draws: 356, Prims: 24.7K;
CPU: WaitForTasks: 42, 27.6 ms, 27.6 ms; FEngineLoop::Tick: 1, 16.8 ms, 0; Frame: 1, 16.8 ms, 50.6 µs; Frame: 57, 9.6 ms, 386.7 µs; FEngineLoop_UpdateTimeAndHandleMaxTickRate: 1, 9.2 ms, 9.2 ms; Slate::Tick (Time and Widgets): 1, 4.2 ms, 297.8 µs; SceneRender: 34, 4.2 ms, 274.8 µs; Slate::DrawWindows: 1, 3.9 ms, 33 µs; Scene: 21, 2.5 ms, 228.2 µs; Tick_Engine: 1, 2.4 ms, 285.6 µs; TaskWorkerIsLookingForWork: 113, 2.4 ms, 2.4 ms; RenderGraphExecute: 44, 2.4 ms, 158.8 µs; Slate::DrawWindow: 1, 1.9 ms, 11.8 µs; Slate_PaintSlowPath: 1, 1.9 ms, 1.4 ms; ExecuteForegroundTask: 121, 1.9 ms, 646.8 µs; Slate::Prepass: 1, 1.8 ms, 1.8 ms; RHI_Translate: 54, 1.6 ms, 46.5 µs; FDeferredShadingSceneRenderer_Render: 1, 1.5 ms, 700 ns; WorldTick: 15, 1.3 ms, 98.4 µs; UWorld_Tick: 5, 1.2 ms, 244.8 µs
The biggest number is Waiting for tasks, which means that processor has no tasks to do, which is normal
GPU: Nothing problematic and interesting, which means that GPU executes all tasks very well

Errors while packaging: None
Used assets and licences(rechecked):

Scheming Weasel (faster version, looped) — Kevin MacLeod
https://incompetech.com/music/royalty-free/index.html?isrc=USUAN1100085
https://creativecommons.org/licenses/by/4.0/

Short alarm — yd
https://opengameart.org/content/short-alarm
https://creativecommons.org/publicdomain/zero/1.0/

Chase — lifeasaghost(looped) 
https://opengameart.org/content/chase-0
https://creativecommons.org/licenses/by/4.0/

Plingy Coin — Fupi
https://opengameart.org/content/plingy-coin
https://creativecommons.org/publicdomain/zero/1.0/

St2 - Footstep sfx — Yarzur_ofc
https://pixabay.com/sound-effects/film-special-effects-st2-footstep-sfx-323055/
https://pixabay.com/service/terms/

Niagara Examples Pack - Epic Games
https://www.fab.com/listings/0e188eca-4e54-4fb2-a9ed-d8b8a565e600
https://www.unrealengine.com/eula/content

Known bugs: None

Learned: Global illumination on cinematic setting has a terrible optimization
What was the hardest: to implement savegame mechanic 

https://drive.google.com/drive/folders/1CltaRfyJVGBVpWbAaX_oX4N9JJ2sTJ5B?usp=sharing


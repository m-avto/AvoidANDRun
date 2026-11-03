<!-- Game name: AVOID AND RUN --> -->
<!-- Unreal Engine version: 5.7 -->
<!-- Controls:
Movement is AWSD; Shift = sprint; Space = Jump; Ctrl = Dash; -->
<!-- For launching game download an archive containing game build and run an AvoidANDRun.exe -->
<!-- Blueprints and their purpose:
BP_MainChar; Purpose: regulation of events + self-explanatory
BP_Enemy; Purpose:self-explanatory, just a model wiwh collision
BP_GMBase - game mode; Purpose: calculate current score, calculate and save best score
BPI_GameMode - Blueprint interface which helps BP_GMBase
PC_MainChar - Player Controller; Purpose: work with HUD and Graphic settings
BP_SaveGame - save game object; Purpose: save best score
BP_Coin; Purpose: collectible item with an overlap logic
AI_Controller + BT_Enemy + BB_Enemy + BTT_get patrol Location + EQS_Coin; Purpose: controlling AI behaviour, chase, patrol + choosing coin locations
WBP_Death + WBP_Settings + WBP_MainMenu + WBP_PauseMenu + WBP_Score + WBP_Victory; Purpose: Self-explanatory
Optimization: 60 fps at any graphics; illumination takes the most resources
Errors while packaging: None
Used assets and licences:

Scheming Weasel (faster version, looped) — Kevin MacLeod
https://incompetech.com/music/royalty-free/index.html?isrc=USUAN1100085&utm_source=chatgpt.com 
https://creativecommons.org/licenses/by/4.0/?utm_source=chatgpt.com

Short alarm — yd
https://opengameart.org/content/short-alarm?utm_source=chatgpt.com
https://creativecommons.org/publicdomain/zero/1.0/?utm_source=chatgpt.com

Chase — lifeasaghost(looped) 
https://opengameart.org/content/chase-0?utm_source=chatgpt.com
https://creativecommons.org/licenses/by/4.0/?utm_source=chatgpt.com

Plingy Coin — Fupi
https://opengameart.org/content/plingy-coin?utm_source=chatgpt.com
https://creativecommons.org/publicdomain/zero/1.0/?utm_source=chatgpt.com

St2 - Footstep sfx — Yarzur_ofc
https://pixabay.com/sound-effects/film-special-effects-st2-footstep-sfx-323055/?utm_source=chatgpt.com
https://pixabay.com/service/terms/

Niagara Examples Pack - Epic Games
https://www.fab.com/listings/0e188eca-4e54-4fb2-a9ed-d8b8a565e600?utm_source=chatgpt.com
https://www.unrealengine.com/eula/content

Known bugs:
Alarm sound of chase start repeats during the chase, I decided not to fix it, because it's only making sound better
What I learned and what was hard
Learned: Global illumination on cinematic setting has a terrible optimization
What was hard: nothing-->
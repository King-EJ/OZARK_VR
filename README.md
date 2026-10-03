# OZARK_VR
VR Mod for OZARK

OZARK VR  -  VR mod for OZARK (Unity 2021.3, IL2CPP) "WIP"
=====================================================

Version 0.1.24 (test build on Quest 3).

NEW IN 0.1.26
* Grenades: hold the throw buttons (right grip + left trigger) longer to throw further. The target
  marker moves out from you while you hold - about 1.5 s to the furthest throw - in the direction you
  aim the gun (first person) or face (third person). Let go to throw. Config [Grenades] ChargeThrow,
  ChargeTime (1.5 s), MaxThrow (1 = the game's longest stick throw, ~10 m; 2 = twice that). Hold time
  and furthest throw are also in the settings menu.

NEW IN 0.1.25
* Enemies now SHOOT from far away. The game only lets an enemy open fire once it is on its own flat
  side-view screen - in VR that is a small area around you, so far enemies turned to you but held fire.
  Now an enemy in your VR view and within its sight distance (Enemies / SightMultiplier) can shoot too
  (line of sight still needed). Config [Enemies] FireWhenInVRView (on) and FireViewAngle (70 degrees
  from where you look; 180 = even behind you). Also "Enemies shoot when in VR view" in the settings menu.

NEW IN 0.1.24
* Enemy sight distance FIXED: a timing bug kept the mod from ever looking for the enemies during play.

NEW IN 0.1.23
* More enemy diagnostics in the log (every 30 s while playing: enemies, spawners, active enemy zones).

NEW IN 0.1.22
* Third person: both sticks are plain gamepad sticks now (left stick right = walk right on the game's
  screen, no head-direction turning).
* Enemy sight: the log now says how many enemies / spawners the mod finds ("Enemy sight: N enemies in
  the level ...") - please send it.

NEW IN 0.1.21
* Enemy sight distance now really applies: it changes each enemy's own vision settings (0.1.19/0.1.20
  only changed the shared templates, which the enemies had already copied). The log shows
  "Enemy sight x... (N enemy vision settings, e.g. 15 m -> 150 m)".

NEW IN 0.1.20
* Interaction prompts (the circle that fills while you hold Y): drawn bright and on top - no longer
  darkened by the game's effects or hidden behind things - and the Xbox button picture shows inside
  again (the game showed none because no real gamepad is plugged in). [UI] BrightPrompts, XboxButtonIcons.

NEW IN 0.1.19
* Enemy sight distance: settings menu -> Aiming -> "Enemy sight distance (x game)" (live), or
  [Enemies] SightMultiplier in the config. 1 = the game's own, 2 = enemies see you twice as far, 0.5 = half.

NEW IN 0.1.18
* Objective on the left hand: written out by the mod in plain text (yellow title, white tasks, blue pick-up
  messages) - the game's objective font came out as yellow blocks in VR. Size: [UI] HandHudObjectiveScale.

NEW IN 0.1.17
* Y is now held for as long as you hold it - the game's hold-Y interactions work (before, the mod only
  sent a short Y tap).
* Hand HUD: the objective text is drawn bigger and smoothly scaled down, so it reads as words instead
  of yellow blocks. [UI] HandHudObjectiveScale (objective size), HandHudSize (whole hand HUD).

NEW IN 0.1.16
* GRENADES: in OZARK the grenade is the game's RB button (hold = get ready, let go = throw), LT aims and
  R3 kicks. Now: hold the right grip (aim) + hold the left trigger, LET GO of the left trigger to throw.
  A quick pull of the left trigger alone still kicks.
* The left grip (LB) opens the inventory in this game, so no combos use it any more - the right grip is
  the modifier now: right grip + right stick left = Back, + right stick up = d-pad up, + right stick right
  = d-pad right (third person). Flashlight = left trigger + left stick click only.
* LASER SETUP is now HOLD B for 2 s (Y is the game's interact button). In setup: short B = reset,
  A = save, hold B 2 s again = cancel.

NEW IN 0.1.15
* Yellow icons: the game's waypoint / objective markers now float in the world at what they mark, facing
  you, always readable (seen through walls, like in the flat game). The game's in-world icons / prompts
  (UI layer) are drawn in the headset too. [UI] WorldIcons, WorldIconSize, WorldIconHeight.

NEW IN 0.1.14
* Left trigger (quick pull) = R3 = KICK.
* Hold the right grip + pull the left trigger = LT = grenade (release the trigger to throw).
* Melee (RB) = hold the left grip + pull the left trigger.
* Holding the left trigger (for RB + Y d-pad down, RB + L3 flashlight) does not kick.

NEW IN 0.1.13
* Right grip = R3 = KICK.
* Hold the left trigger (RB) + press the right grip = LT = grenade (throw).
* (RB + X no longer kicks - X is just X again.) The laser still shows while the right grip is held.

NEW IN 0.1.12
* Hold the left trigger (RB) + X = KICK - the mod now does the kick itself (works while aiming too).
* Normal (third person) view: the right controller is a normal gamepad right stick - the stick aims, no
  hand aiming, no VR laser, shots go where the game aims. In this view: left grip + right stick up = d-pad up,
  left grip + right stick right = d-pad right, left grip + right stick left = Back (inventory).
* First person: the view no longer shakes while aiming / shooting - the eye height follows the character's
  head smoothly. [View] EyeHeightSmoothing (lower = steadier, 0 = off).

NEW IN 0.1.11
* Hold the left trigger (RB) + click the left stick (L3) = flashlight on / off (straight away, no crouch, no melee).
  (The game itself needs d-pad down HELD for the flashlight - a quick d-pad down is the helmet sight.)

NEW IN 0.1.10
* The game's own laser sight (red line / dot from the gun) is hidden - only the VR laser shows.
  [Aiming] HideGameLaser = false brings it back.

NEW IN 0.1.9
* D-pad down = hold the left trigger (RB) + click the left stick (L3) (RB + Y did not work).

NEW IN 0.1.8 - buttons
* Right stick down = d-pad right.        * Hold X = d-pad left.
* (0.1.9: d-pad down is now RB + left stick click.)   * Hold the left trigger (RB) + X = R3 (kick).
* RB (melee) is now a QUICK pull of the left trigger, so holding it for the combos doesn't swing.
* Back (inventory) moved to left grip + right stick left. Hold Y no longer sends R3 (only laser setup).

NEW IN 0.1.7
* Hand HUD: the health / status bars and, above them, the objective (and pick-up messages) float over
  your LEFT hand, facing you; the ammo (and grenades) float to the right of your gun. In menus /
  inventory the HUD goes back to the VR screen. [UI] HandHud (on/off), HandHudSize, HandHudLeftOffset,
  HandHudGunOffset.
* Shots: your bullets now start at the laser start and fly along the laser (the game's auto-aim no
  longer pulls them off), reach 300 m instead of the game's short side-view range, and fly through the
  side view's invisible walls. [Aiming] ShotsAlongLaser, BulletRange, BulletIgnoreLayers.

NEW IN 0.1.6
* Game hands: put on the controllers right before the eyes draw again (as in 0.1.3, which worked), and the
  stretched skin from the hands down to the body is gone (the arm now ends cleanly at the elbow).
* LASER SETUP (like RetroSpace VR) - hold Y for 1.2 s with a weapon in hand:
    left grip (hold) ... grab the yellow start point and put it on the barrel tip
    right stick ........ steer the laser end (left/right, up/down)
    right grip (hold) .. the laser keeps pointing where it points while you turn the gun
    B = reset, A = save for this weapon, hold Y again = cancel
  Saved per weapon in [Weapon - <name>] LaserStart / LaserRotation. The game aims along the laser.
  [Aiming] LaserAdjustHold = how long to hold Y (0 = off).

NEW IN 0.1.5
* Right eye too bright: FIXED. The eye test found it - the camera that draws the VR screen (menus / HUD)
  for the left eye ran between the two eyes and left the renderer in a state that made the right eye
  several times brighter. Both of those screen cameras now draw after both eyes. ("Same picture in both
  eyes" should no longer be needed - switch it off if you turned it on.)
* Game hands: new default "Forearms" - the character's hands AND forearms are on your controllers, so
  there is no open, hollow-looking wrist any more (the arm ends at the elbow, out of view).
  Settings menu -> Hands -> "Game hands": Forearms / HandsOnly / Arms.

NEW IN 0.1.4
* Body / silhouette in first person: the game's see-through outline of the player is switched off, and
  the body is now hidden at the right moment (it was done too late before, after the game had already
  shaped the body mesh). Your character's hands now really follow the controllers.
* Eye brightness: the log showed the right eye 7-20x brighter than the left, even with post-processing
  off. About 12 s after you start playing, the mod runs a 30 s automatic test (the picture may flicker
  briefly): it changes one thing at a time and logs which one makes the eyes match. If one fixes it, it is
  kept. Please send the log after that.
* Settings menu -> "Same picture in both eyes": both eyes get the left eye's picture (no 3D depth, but
  they always match). Use it until the real fix is in.

NEW IN 0.1.3
* Walking fixed: the game read a plugged-in gamepad directly and ignored the VR stick and the keyboard.
  Push the left stick where you want to go (relative to where you look) - the mod turns that into the
  game's side-scroller movement.
* The character's own hands are now your VR hands (first person): settings menu -> Hands ->
  "Hand model" = Game (default), "Game hands" = HandsOnly (just the hands) or Arms (hands + arms).
  Fine-tune them live in the same menu (back / forward, up / down, tilt, roll). Hand model = Hand gives the
  mod's hands back.
* One eye brighter / darker: the log now measures both eyes ("Eye brightness" lines). If it still
  happens, switch "Post processing" off in the settings menu once to see if it goes away, and send the log.

WHAT IT DOES
------------
* Stereo VR through OpenXR (SteamVR, Meta/Oculus, Virtual Desktop, WMR...).
* Two views - the right stick click switches between them:
    FIRST PERSON  you are the character: the view sits at its head, the left stick walks where you look,
                  the character's hands are on your controllers,
                  the right stick turns, your right hand aims.
    NORMAL        you stand where the game's own camera is, like the flat game.
* The VR controllers act as an Xbox gamepad for all of the game's controls and menus: every game action
  gets the gamepad button the game itself uses for it.
* Menus / HUD are on a screen floating in front of you.

INSTALL
-------
1. Copy extracted file from zip into the game folder (merge / overwrite).
2. Start SteamVR (or your OpenXR runtime), then start the game.

CONTROLS (as an Xbox gamepad)
-----------------------------
Left stick ......... left stick (walk)        Right stick ............. turn (first person) / aim

Right trigger ...... RT (fire)                Right grip .............. LT (aim) + red laser while held

Left trigger (quick pull) .. KICK (R3)    Left grip ............... LB (inventory)

A / B .............. A / B                    X (tap) / hold X ........ X / d-pad left

Y ................... Y (interact)             Hold B 2 s .............. laser setup

X + Y together ..... Start (pause)            Left stick click ........ L3

Right stick up ..... d-pad up                 Right stick down ........ d-pad right

Hold left trigger (RB) + left stick click .. FLASHLIGHT on / off    Hold right grip + hold left trigger, let go of the trigger .. grenade throw (RB)

Hold left trigger (RB) + Y .. d-pad down (helmet sight)

Right grip + right stick left .. Back

Right stick click .. switch first person / normal view

Hold left trigger + left stick click .. flashlight on / off

Both stick clicks .. re-centre

While aiming (right grip or trigger held) the character aims where your right hand points.

WEAPON POSITION / ROTATION (each weapon its own, saved live)
-------------------------------------------------------------
In-game settings menu (hold Y + left stick click 1.7 s) -> "Weapon in hand":
  move left/right, down/up, back/forward (cm) and tilt / turn / roll (degrees) with right stick left/right,
  "Reset this weapon", or "Grab it with the left hand".
Grab mode (also: hold B + right stick click 1.5 s): hold the LEFT GRIP to grab the weapon, move / turn it,
let go. B = undo, A = save. Saved in BepInEx\config\ozark.vr.cfg as [Weapon - <name>].

RENDER EFFECTS
--------------
Depth of field, motion blur and ambient occlusion are OFF by default (blur / one eye darker in a headset) - switch them on
in the settings menu if you want them.
Settings menu -> "Render effects": switch any of the game's post-processing effects (Bloom, Vignette,
Depth of field, Motion blur, Chromatic aberration, Grain...) and the fog off / on for VR.
Saved in [Camera] DisabledRenderFeatures.

ALSO IN THE SETTINGS MENU: view, zoom of the normal view, snap / smooth turn, unlimited ammo, unlimited HP,
screen distance / size, hand models.  HAND ADJUST: hold Y + right stick click for 1.5 s.

If a game action is on the wrong button: [Input] ActionOverrides in the config, e.g. Melee=RB;Jump=A
(the log lists every action and the button it got).

Uses Astien's OpenXR bridge (see BepInEx\plugins\OZVR\LICENSES). Free, non-commercial.

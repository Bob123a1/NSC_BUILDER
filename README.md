# Nintendo Switch Cleaner and Builder (NSC_Builder)

**NOTE: For my hacbuild's fix go to** https://github.com/julesontheroad/hacbuild 

## 1. Description

NSC_Builder is based in the awesome function "REMOVE_TITLE_RIGHTS" from nut by blawar
this function let's you erase the titlerights encryption from nsp files.
Tinfoil and SX installer will install the ticket either way so for it to not stay in 
your system you need to erase the ticket and cert from the nsp, this batch will take
care of that.

Current version of the program allow you to make multi-content xci or nsp files.

The batch has 2 modes:

- auto mode: you drag nsp files individually or folders with several files over the batch to enter in auto mode.
- manual mode: you double click the batch and you can build a list of files to process.

The behavior of these modes can be controlled by editing ztools\NSCB_options.cmd

## 2. Important

The program incorporates a custom build of nut.py and hacbuild with several added 
functions. You won't be able to use it if you replace these files for the official
builds.

## 3. Requirements

- A computer with a Window's OS is needed
- You'll need to have Python 3 installed for the program to work correctly
- You'll need to install these libraries: "urllib3 unidecode tqdm bs4 tqdm requests image"
  to assist you in this you can run "install_dependencies.bat" file.
- You need to fill the keys_template.txt file inside the ztools folder and rename to keys.txt
- You'll need to have at least .net frameworks 4.5.2 installed so hacbuild can work correctly.

## 4. Option description

#### OPTION 1: Work and Output folders setup
#### OPTION 2: Route to needed programs
#### OPTION 3: Nut options
  - pycommand -> your command to invoke python 3 (by deffault py -3)
  - buffer -> buffer in number of bytes for the copy functions
####  OPTION 4: Route to game_info.ini and keys.txt
#### OPTION 5: REPACK OPTIONS. Controls repack in auto mode.
##### Repack option for auto-mode
  - xci -> repack as xci
  - nsp -> repacck as nsp
  - both -> repacck as both
##### Type of repack for folders
  - indiv -> repack content individually as multiple xci/nsp
  - multi -> repack content as single multicontent xci/nsp
#### OPTION 6: MANUAL MODE INTRO. 
  - indiv-> Enter in individual packing mode directly
  - multi-> Enter in multi-pack mode directly
  - choose-> Prompt to choose the mode in which you want to enter
#### OPTION 7: ZIP FILES 
Select if you want to zip things that will allow to restore nsp files to original state.

## 5. Limitations 
- You can't make multi-content xci files with more than 8 games. It'll give error when loading
in horizon. I suspect it may be a qlauncher limitation so it could work with theme mods but INTRO
didn't test it.
- If you pack an update that requires a superior firmware that you're in you won't be able to skip
the update prompt.

## 6. Planned features 
- List manager.
- Batch tools to put in application some of my changes to nut libraries.
- Support for meta patching and control nca building for custom logos.
- Skips for individual mode.
- Content splitter.
- Titlerights restoration mode.

## 7. Thanks and credits to 

NSC_Builder is based on

a.) Nut: Without the work of "blawar" one of the most talented Switch sceners nothing of this would
be possible at this point.
https://github.com/blawar/nut

a.) Hacbuild: The xci repacking functions are based in hacbuild made by LucaFraga

- Original hacbuild: https://github.com/LucaFraga/hacbuild) by LucaFraga

- Revised hacbuild by me: https://github.com/julesontheroad/hacbuild

c.) hactool: Program which function is give information, decrypt and extract a lot of different kind of files us by the NX System. Hactool was made by SciresM

https://github.com/SciresM/hactool

d.) 7zip: Program meant to compress and extract files in several formats. 7zip was made by Igor Pavlov
https://www.7-zip.org/

Thx to MadScript77 his great suggestions,specially the idea of profiles for the batch.
Thx to Liam from old SH discord for always being helpfull.
Thx to XCI-Explorer's creator StudentBlake since his program made easier for me to came up with the fix for hacbuild.

Also thanks to all members from gbatemp, elotrolado.net and my friends at discord ;)

# cg9_counter
Counter-engineering some stuff

This is the instructions to build a script in Python that will make possible to take full advantage of MH characters.

1- PRE-NODES SETUP:
1.1- Select all the "file" nodes with name starting with "maskFile_head" and set the following:

   1.1.1- in the "File Attributes" tab:
   	- Ignore Color Space File Rules: On
   	- Color Space: Raw

   1.1.2- in the "Color Balance" tab:
   	- Alpha is Luminance: On
   
1.2- Select all the "file" nodes with name containing "mapFile_*normal" and set the following:
  1.2.1- in the "File Attributes" tab:
   	- Ignore Color Space File Rules: On
   	- Color Space: Raw



2- NODES CREATION – HEAD NORMAL MAP MASKS

2.1- Create a VRayLayeredTex called VRL_WM1_MASKS

2.1.1- Configure the base layer ("Layers[0]") as follows:
 Name: BASE
 Enabled: On
 Tex: full black color
 Mask: full white color
 Blend Mode: Normal
 Opacity: 1
 
2.1.2- Create 19 new layers in the VRL_WM1_MASKS texture. They will be set as follows:
 Layers[1]
 Name: WM13_Lips_DL
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm13_lips_DL" node
 Blend Mode: Add
 Opacity: connect here the "head_wm1_normal_head_wm13_lips_DL" output connection from "FRM_WMmultipliers" node
 
 Layers[2]
 Name: WM13_Lips_DR
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm13_lips_DR" node
 Blend Mode: Add
 Opacity: connect here the "head_wm1_normal_head_wm13_lips_DR" output connection from "FRM_WMmultipliers" node
 
 Layers[3]
 Name: WM13_Lips_UL
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm13_lips_UL" node
 Blend Mode: Add
 Opacity: connect here the "head_wm1_normal_head_wm13_lips_UL" output connection from "FRM_WMmultipliers" node
 
 Layers[4]
 Name: WM13_Lips_UR
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm13_lips_UR" node
 Blend Mode: Add
 Opacity: connect here the "head_wm1_normal_head_wm13_lips_UR" output connection from "FRM_WMmultipliers" node
 
 Layers[5]
 Name: WM1_Blink_L
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm1_blink_L" node
 Blend Mode: Add
 Opacity: connect here the "head_wm1_normal_head_wm1_blink_L" output connection from "FRM_WMmultipliers" node
 
 Layers[6]
 Name: WM1_Blink_R
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm1_blink_R" node
 Blend Mode: Add
 Opacity: connect here the "head_wm1_normal_head_wm1_blink_R" output connection from "FRM_WMmultipliers" node
 
 Layers[7]
 Name: WM1_Brows_Raise_Inner_L
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm1_browsRaiseInner_L" node
 Blend Mode: Add
 Opacity: connect here the "head_wm1_normal_head_wm1_browsRaiseInner_L" output connection from "FRM_WMmultipliers" node
 
 Layers[8]
 Name: WM1_Brows_Raise_Inner_R
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm1_browsRaiseInner_R" node
 Blend Mode: Add
 Opacity: connect here the "head_wm1_normal_head_wm1_browsRaiseInner_R" output connection from "FRM_WMmultipliers" node
 
 Layers[9]
 Name: WM1_Brows_Raise_Outer_L
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm1_browsRaiseOuter_L" node
 Blend Mode: Add
 Opacity: connect here the "head_wm1_normal_head_wm1_browsRaiseOuter_L" output connection from "FRM_WMmultipliers" node
 
 Layers[10]
 Name: WM1_Brows_Raise_Outer_R
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm1_browsRaiseOuter_R" node
 Blend Mode: Add
 Opacity: connect here the "head_wm1_normal_head_wm1_browsRaiseOuter_R" output connection from "FRM_WMmultipliers" node
 
 Layers[11]
 Name: WM1_Chin_Raise_L
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm1_chinRaise_L" node
 Blend Mode: Add
 Opacity: connect here the "head_wm1_normal_head_wm1_chinRaise_L" output connection from "FRM_WMmultipliers" node
 
 Layers[12]
 Name: WM1_Chin_Raise_R
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm1_chinRaise_R" node
 Blend Mode: Add
 Opacity: connect here the "head_wm1_normal_head_wm1_chinRaise_R" output connection from "FRM_WMmultipliers" node
 
 Layers[13]
 Name: WM1_Jaw_Open
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm1_jawOpen" node
 Blend Mode: Add
 Opacity: connect here the "head_wm1_normal_head_wm1_jawOpen" output connection from "FRM_WMmultipliers" node
 
 Layers[14]
 Name: WM1_Purse_DL
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm1_purse_DL" node
 Blend Mode: Add
 Opacity: connect here the "head_wm1_normal_head_wm1_purse_DL" output connection from "FRM_WMmultipliers" node
 
 Layers[15]
 Name: WM1_Purse_DR
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm1_purse_DR" node
 Blend Mode: Add
 Opacity: connect here the "head_wm1_normal_head_wm1_purse_DR" output connection from "FRM_WMmultipliers" node
 
 Layers[16]
 Name: WM1_Purse_UL
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm1_purse_UL" node
 Blend Mode: Add
 Opacity: connect here the "head_wm1_normal_head_wm1_purse_UL" output connection from "FRM_WMmultipliers" node
 
 Layers[17]
 Name: WM1_Purse_UR
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm1_purse_UR" node
 Blend Mode: Add
 Opacity: connect here the "head_wm1_normal_head_wm1_purse_UR" output connection from "FRM_WMmultipliers" node
 
 Layers[18]
 Name: WM1_Squint_Inner_L
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm1_squintInner_L" node
 Blend Mode: Add
 Opacity: connect here the "head_wm1_normal_head_wm1_squintInner_L" output connection from "FRM_WMmultipliers" node
 
 Layers[19]
 Name: WM1_Squint_Inner_R
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm1_squintInner_R" node
 Blend Mode: Add
 Opacity: connect here the "head_wm1_normal_head_wm1_squintInner_R" output connection from "FRM_WMmultipliers" node
 
2.2- Create a VRayLayeredTex called VRL_WM2_MASKS

2.2.1- Configure the base layer ("Layers[0]") as follows:
 Name: BASE
 Enabled: On
 Tex: full black color
 Mask: full white color
 Blend Mode: Normal
 Opacity: 1
 
2.2.2- Create 10 new layers in the VRL_WM2_MASKS texture. They will be set as follows:

 Layers[1]
 Name: WM2_Brows_Down_L
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm2_browsDown_L" node
 Blend Mode: Add
 Opacity: connect here the "head_wm2_normal_head_wm2_browsDown_L" output connection from "FRM_WMmultipliers" node
 
 Layers[2]
 Name: WM2_Brows_Down_R
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm2_browsDown_R" node
 Blend Mode: Add
 Opacity: connect here the "head_wm2_normal_head_wm2_browsDown_R" output connection from "FRM_WMmultipliers" node
 
 Layers[3]
 Name: WM2_Brows_Lateral_L
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm2_browsLateral_L" node
 Blend Mode: Add
 Opacity: connect here the "head_wm2_normal_head_wm2_browsLateral_L" output connection from "FRM_WMmultipliers" node
 
 Layers[4]
 Name: WM2_Brows_Lateral_R
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm2_browsLateral_R" node
 Blend Mode: Add
 Opacity: connect here the "head_wm2_normal_head_wm2_browsLateral_R" output connection from "FRM_WMmultipliers" node
 
 Layers[5]
 Name: WM2_Mouth_Stretch_L
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm2_mouthStretch_L" node
 Blend Mode: Add
 Opacity: connect here the "head_wm2_normal_head_wm2_mouthStretch_L" output connection from "FRM_WMmultipliers" node
 
 Layers[6]
 Name: WM2_Mouth_Stretch_R
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm2_mouthStretch_R" node
 Blend Mode: Add
 Opacity: connect here the "head_wm2_normal_head_wm2_mouthStretch_R" output connection from "FRM_WMmultipliers" node
 
 Layers[7]
 Name: WM2_Neck_Stretch_L
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm2_neckStretch_L" node
 Blend Mode: Add
 Opacity: connect here the "head_wm2_normal_head_wm2_neckStretch_L" output connection from "FRM_WMmultipliers" node
 
 Layers[8]
 Name: WM2_Neck_Stretch_R
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm2_neckStretch_R" node
 Blend Mode: Add
 Opacity: connect here the "head_wm2_normal_head_wm2_neckStretch_R" output connection from "FRM_WMmultipliers" node
 
 Layers[9]
 Name: WM2_Nose_Wrinkler_L
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm2_noseWrinkler_L" node
 Blend Mode: Add
 Opacity: connect here the "head_wm2_normal_head_wm2_noseWrinkler_L" output connection from "FRM_WMmultipliers" node
 
 Layers[10]
 Name: WM2_Nose_Wrinkler_R
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm2_noseWrinkler_R" node
 Blend Mode: Add
 Opacity: connect here the "head_wm2_normal_head_wm2_noseWrinkler_R" output connection from "FRM_WMmultipliers" node
 
 
2.3- Create a VRayLayeredTex called VRL_WM3_MASKS

2.3.1- Configure the base layer ("Layers[0]") as follows:
 Name: BASE
 Enabled: On
 Tex: full black color
 Mask: full white color
 Blend Mode: Normal
 Opacity: 1
 
2.3.2- Create 12 new layers in the VRL_WM3_MASKS texture. They will be set as follows:
 Layers[1]
 Name: WM13_Lips_DL
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm13_lips_DL" node
 Blend Mode: Add
 Opacity: connect here the "head_wm3_normal_head_wm13_lips_DL" output connection from "FRM_WMmultipliers" node
 
 Layers[2]
 Name: WM13_Lips_DR
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm13_lips_DR" node
 Blend Mode: Add
 Opacity: connect here the "head_wm3_normal_head_wm13_lips_DR" output connection from "FRM_WMmultipliers" node
 
 Layers[3]
 Name: WM13_Lips_UL
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm13_lips_UL" node
 Blend Mode: Add
 Opacity: connect here the "head_wm3_normal_head_wm13_lips_UL" output connection from "FRM_WMmultipliers" node
 
 Layers[4]
 Name: WM13_Lips_UR
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm13_lips_UR" node
 Blend Mode: Add
 Opacity: connect here the "head_wm3_normal_head_wm13_lips_UR" output connection from "FRM_WMmultipliers" node
 
 Layers[5]
 Name: WM3_CHEEK_RAISE_INNER_L
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm3_cheekRaiseInner_L" node
 Blend Mode: Add
 Opacity: connect here the "head_wm3_normal_head_wm3_cheekRaiseInner_L" output connection from "FRM_WMmultipliers" node
 
 Layers[6]
 Name: WM3_CHEEK_RAISE_INNER_R
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm3_cheekRaiseInner_R" node
 Blend Mode: Add
 Opacity: connect here the "head_wm3_normal_head_wm3_cheekRaiseInner_R" output connection from "FRM_WMmultipliers" node
 
 Layers[7]
 Name: WM3_CHEEK_RAISE_OUTER_L
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm3_cheekRaiseOuter_L" node
 Blend Mode: Add
 Opacity: connect here the "head_wm3_normal_head_wm3_cheekRaiseOuter_L" output connection from "FRM_WMmultipliers" node
 
 Layers[8]
 Name: WM3_CHEEK_RAISE_OUTER_R
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm3_cheekRaiseOuter_R" node
 Blend Mode: Add
 Opacity: connect here the "head_wm3_normal_head_wm3_cheekRaiseOuter_R" output connection from "FRM_WMmultipliers" node
 
 Layers[9]
 Name: WM3_CHEEK_RAISE_UPPER_L
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm3_cheekRaiseUpper_L" node
 Blend Mode: Add
 Opacity: connect here the "head_wm3_normal_head_wm3_cheekRaiseUpper_L" output connection from "FRM_WMmultipliers" node
 
 Layers[10]
 Name: WM3_CHEEK_RAISE_UPPER_R
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm3_cheekRaiseUpper_R" node
 Blend Mode: Add
 Opacity: connect here the "head_wm3_normal_head_wm3_cheekRaiseUpper_R" output connection from "FRM_WMmultipliers" node
 
 Layers[11]
 Name: WM3_SMILE_L
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm3_smile_L" node
 Blend Mode: Add
 Opacity: connect here the "head_wm3_normal_head_wm3_smile_L" output connection from "FRM_WMmultipliers" node
 
 Layers[12]
 Name: WM3_SMILE_L
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm3_smile_L" node
 Blend Mode: Add
 Opacity: connect here the "head_wm3_normal_head_wm3_smile_L" output connection from "FRM_WMmultipliers" node
 
 
3- NODES CREATION – DIFFUSE MAP MASKS

3.1- Create a VRayLayeredTex called VRL_CM1_MASKS

3.1.1- Configure the base layer ("Layers[0]") as follows:
 Name: BASE
 Enabled: On
 Tex: full black color
 Mask: full white color
 Blend Mode: Normal
 Opacity: 1
 
3.1.2- Create 19 new layers in the VRL_CM1_MASKS texture. They will be set as follows:
 Layers[1]
 Name: CM13_Lips_DL
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm13_lips_DL" node
 Blend Mode: Add
 Opacity: connect here the "head_cm1_normal_head_wm13_lips_DL" output connection from "FRM_WMmultipliers" node
 
 Layers[2]
 Name: CM13_Lips_DR
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm13_lips_DR" node
 Blend Mode: Add
 Opacity: connect here the "head_cm1_normal_head_wm13_lips_DR" output connection from "FRM_WMmultipliers" node
 
 Layers[3]
 Name: CM13_Lips_UL
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm13_lips_UL" node
 Blend Mode: Add
 Opacity: connect here the "head_cm1_normal_head_wm13_lips_UL" output connection from "FRM_WMmultipliers" node
 
 Layers[4]
 Name: CM13_Lips_UR
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm13_lips_UR" node
 Blend Mode: Add
 Opacity: connect here the "head_cm1_normal_head_wm13_lips_UR" output connection from "FRM_WMmultipliers" node
 
Layers[5]
 Name: CM1_Blink_L
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm1_blink_L" node
 Blend Mode: Add
 Opacity: connect here the "head_cm1_normal_head_wm1_blink_L" output connection from "FRM_WMmultipliers" node
 
 Layers[6]
 Name: CM1_Blink_R
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm1_blink_R" node
 Blend Mode: Add
 Opacity: connect here the "head_cm1_normal_head_wm1_blink_R" output connection from "FRM_WMmultipliers" node
 
 Layers[7]
 Name: CM1_Brows_Raise_Inner_L
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm1_browsRaiseInner_L" node
 Blend Mode: Add
 Opacity: connect here the "head_cm1_normal_head_wm1_browsRaiseInner_L" output connection from "FRM_WMmultipliers" node
 
 Layers[8]
 Name: CM1_Brows_Raise_Inner_R
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm1_browsRaiseInner_R" node
 Blend Mode: Add
 Opacity: connect here the "head_cm1_normal_head_wm1_browsRaiseInner_R" output connection from "FRM_WMmultipliers" node
 
 Layers[9]
 Name: CM1_Brows_Raise_Outer_L
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm1_browsRaiseOuter_L" node
 Blend Mode: Add
 Opacity: connect here the "head_cm1_normal_head_wm1_browsRaiseOuter_L" output connection from "FRM_WMmultipliers" node
 
 Layers[10]
 Name: CM1_Brows_Raise_Outer_R
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm1_browsRaiseOuter_R" node
 Blend Mode: Add
 Opacity: connect here the "head_cm1_normal_head_wm1_browsRaiseOuter_R" output connection from "FRM_WMmultipliers" node
 
 Layers[11]
 Name: CM1_Chin_Raise_L
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm1_chinRaise_L" node
 Blend Mode: Add
 Opacity: connect here the "head_cm1_normal_head_wm1_chinRaise_L" output connection from "FRM_WMmultipliers" node
 
 Layers[12]
 Name: CM1_Chin_Raise_R
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm1_chinRaise_R" node
 Blend Mode: Add
 Opacity: connect here the "head_cm1_normal_head_wm1_chinRaise_R" output connection from "FRM_WMmultipliers" node
 
 Layers[13]
 Name: CM1_Jaw_Open
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm1_jawOpen" node
 Blend Mode: Add
 Opacity: connect here the "head_cm1_normal_head_wm1_jawOpen" output connection from "FRM_WMmultipliers" node
 
 Layers[14]
 Name: CM1_Purse_DL
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm1_purse_DL" node
 Blend Mode: Add
 Opacity: connect here the "head_cm1_normal_head_wm1_purse_DL" output connection from "FRM_WMmultipliers" node
 
 Layers[15]
 Name: CM1_Purse_DR
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm1_purse_DR" node
 Blend Mode: Add
 Opacity: connect here the "head_cm1_normal_head_wm1_purse_DR" output connection from "FRM_WMmultipliers" node
 
 Layers[16]
 Name: CM1_Purse_UL
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm1_purse_UL" node
 Blend Mode: Add
 Opacity: connect here the "head_cm1_normal_head_wm1_purse_UL" output connection from "FRM_WMmultipliers" node
 
 Layers[17]
 Name: CM1_Purse_UR
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm1_purse_UR" node
 Blend Mode: Add
 Opacity: connect here the "head_cm1_normal_head_wm1_purse_UR" output connection from "FRM_WMmultipliers" node
 
 Layers[18]
 Name: CM1_Squint_Inner_L
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm1_squintInner_L" node
 Blend Mode: Add
 Opacity: connect here the "head_cm1_normal_head_wm1_squintInner_L" output connection from "FRM_WMmultipliers" node
 
 Layers[19]
 Name: CM1_Squint_Inner_R
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm1_squintInner_R" node
 Blend Mode: Add
 Opacity: connect here the "head_cm1_normal_head_wm1_squintInner_R" output connection from "FRM_WMmultipliers" node
 
3.2- Create a VRayLayeredTex called VRL_CM2_MASKS

3.2.1- Configure the base layer ("Layers[0]") as follows:
 Name: BASE
 Enabled: On
 Tex: full black color
 Mask: full white color
 Blend Mode: Normal
 Opacity: 1
 
3.2.2- Create 10 new layers in the VRL_WM2_MASKS texture. They will be set as follows:

 Layers[1]
 Name: CM2_Brows_Down_L
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm2_browsDown_L" node
 Blend Mode: Add
 Opacity: connect here the "head_cm2_normal_head_wm2_browsDown_L" output connection from "FRM_WMmultipliers" node
 
 Layers[2]
 Name: CM2_Brows_Down_R
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm2_browsDown_R" node
 Blend Mode: Add
 Opacity: connect here the "head_cm2_normal_head_wm2_browsDown_R" output connection from "FRM_WMmultipliers" node
 
 Layers[3]
 Name: CM2_Brows_Lateral_L
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm2_browsLateral_L" node
 Blend Mode: Add
 Opacity: connect here the "head_cm2_normal_head_wm2_browsLateral_L" output connection from "FRM_WMmultipliers" node
 
 Layers[4]
 Name: CM2_Brows_Lateral_R
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm2_browsLateral_R" node
 Blend Mode: Add
 Opacity: connect here the "head_cm2_normal_head_wm2_browsLateral_R" output connection from "FRM_WMmultipliers" node
 
 Layers[5]
 Name: CM2_Mouth_Stretch_L
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm2_mouthStretch_L" node
 Blend Mode: Add
 Opacity: connect here the "head_cm2_normal_head_wm2_mouthStretch_L" output connection from "FRM_WMmultipliers" node
 
 Layers[6]
 Name: CM2_Mouth_Stretch_R
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm2_mouthStretch_R" node
 Blend Mode: Add
 Opacity: connect here the "head_cm2_normal_head_wm2_mouthStretch_R" output connection from "FRM_WMmultipliers" node
 
 Layers[7]
 Name: CM2_Neck_Stretch_L
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm2_neckStretch_L" node
 Blend Mode: Add
 Opacity: connect here the "head_cm2_normal_head_wm2_neckStretch_L" output connection from "FRM_WMmultipliers" node
 
 Layers[8]
 Name: CM2_Neck_Stretch_R
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm2_neckStretch_R" node
 Blend Mode: Add
 Opacity: connect here the "head_cm2_normal_head_wm2_neckStretch_R" output connection from "FRM_WMmultipliers" node
 
 Layers[9]
 Name: CM2_Nose_Wrinkler_L
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm2_noseWrinkler_L" node
 Blend Mode: Add
 Opacity: connect here the "head_cm2_normal_head_wm2_noseWrinkler_L" output connection from "FRM_WMmultipliers" node
 
 Layers[10]
 Name: CM2_Nose_Wrinkler_R
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm2_noseWrinkler_R" node
 Blend Mode: Add
 Opacity: connect here the "head_cm2_normal_head_wm2_noseWrinkler_R" output connection from "FRM_WMmultipliers" node
 
 
3.3- Create a VRayLayeredTex called VRL_CM3_MASKS

3.3.1- Configure the base layer ("Layers[0]") as follows:
 Name: BASE
 Enabled: On
 Tex: full black color
 Mask: full white color
 Blend Mode: Normal
 Opacity: 1
 
3.3.2- Create 12 new layers in the VRL_CM3_MASKS texture. They will be set as follows:
 Layers[1]
 Name: CM13_Lips_DL
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm13_lips_DL" node
 Blend Mode: Add
 Opacity: connect here the "head_cm3_normal_head_wm13_lips_DL" output connection from "FRM_WMmultipliers" node
 
 Layers[2]
 Name: CM13_Lips_DR
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm13_lips_DR" node
 Blend Mode: Add
 Opacity: connect here the "head_cm3_normal_head_wm13_lips_DR" output connection from "FRM_WMmultipliers" node
 
 Layers[3]
 Name: CM13_Lips_UL
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm13_lips_UL" node
 Blend Mode: Add
 Opacity: connect here the "head_cm3_normal_head_wm13_lips_UL" output connection from "FRM_WMmultipliers" node
 
 Layers[4]
 Name: CM13_Lips_UR
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm13_lips_UR" node
 Blend Mode: Add
 Opacity: connect here the "head_cm3_normal_head_wm13_lips_UR" output connection from "FRM_WMmultipliers" node
 
 Layers[5]
 Name: CM3_CHEEK_RAISE_INNER_L
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm3_cheekRaiseInner_L" node
 Blend Mode: Add
 Opacity: connect here the "head_cm3_normal_head_wm3_cheekRaiseInner_L" output connection from "FRM_WMmultipliers" node
 
 Layers[6]
 Name: CM3_CHEEK_RAISE_INNER_R
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm3_cheekRaiseInner_R" node
 Blend Mode: Add
 Opacity: connect here the "head_cm3_normal_head_wm3_cheekRaiseInner_R" output connection from "FRM_WMmultipliers" node
 
 Layers[7]
 Name: CM3_CHEEK_RAISE_OUTER_L
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm3_cheekRaiseOuter_L" node
 Blend Mode: Add
 Opacity: connect here the "head_cm3_normal_head_wm3_cheekRaiseOuter_L" output connection from "FRM_WMmultipliers" node
 
 Layers[8]
 Name: CM3_CHEEK_RAISE_OUTER_R
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm3_cheekRaiseOuter_R" node
 Blend Mode: Add
 Opacity: connect here the "head_cm3_normal_head_wm3_cheekRaiseOuter_R" output connection from "FRM_WMmultipliers" node
 
 Layers[9]
 Name: CM3_CHEEK_RAISE_UPPER_L
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm3_cheekRaiseUpper_L" node
 Blend Mode: Add
 Opacity: connect here the "head_cm3_normal_head_wm3_cheekRaiseUpper_L" output connection from "FRM_WMmultipliers" node
 
 Layers[10]
 Name: CM3_CHEEK_RAISE_UPPER_R
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm3_cheekRaiseUpper_R" node
 Blend Mode: Add
 Opacity: connect here the "head_cm3_normal_head_wm3_cheekRaiseUpper_R" output connection from "FRM_WMmultipliers" node
 
 Layers[11]
 Name: CM3_SMILE_L
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm3_smile_L" node
 Blend Mode: Add
 Opacity: connect here the "head_cm3_normal_head_wm3_smile_L" output connection from "FRM_WMmultipliers" node
 
 Layers[12]
 Name: CM3_SMILE_L
 Tex: full white color
 Mask: connect here the "Out Color" connection from "maskFile_head_wm3_smile_L" node
 Blend Mode: Add
 Opacity: connect here the "head_cm3_normal_head_wm3_smile_L" output connection from "FRM_WMmultipliers" node
 

 
4- NODES CREATION – HEAD NORMAL MAP LAYERS SETUP

4.1- Create a VRayLayeredTex called VRL_HEAD_NORMAL

4.1.1- Configure the base layer ("Layers[0]") as follows:
 Name: normal_Base
 Enabled: On
 Tex: Connect here the "baseMapFile_head_normal" file node
 Mask: full white color
 Blend Mode: Normal
 Opacity: 1
 
4.1.2- Create 3 new layers in the VRL_HEAD_NORMAL texture. They will be set as follows:
 Layers[1]
 Name: WM1_MASKS
 Tex: Connect here the "mapFile_head_wm1_normal" file node
 Mask: connect here the "Out Color" connection from "VRL_WM1_MASKS" node
 Blend Mode: Lighten
 Opacity: 1
 
 Layers[2]
 Name: WM2_MASKS
 Tex: Connect here the "mapFile_head_wm2_normal" file node
 Mask: connect here the "Out Color" connection from "VRL_WM2_MASKS" node
 Blend Mode: Lighten
 Opacity: 1
 
 Layers[3]
 Name: WM3_MASKS
 Tex: Connect here the "mapFile_head_wm3_normal" file node
 Mask: connect here the "Out Color" connection from "VRL_WM3_MASKS" node
 Blend Mode: Lighten
 Opacity: 1
 

 
5- NODES CREATION – HEAD DIFFUSE MAP LAYERS SETUP
  
5.1- Create a VRayLayeredTex called VRL_HEAD_DIFFUSE

5.1.1- Configure the base layer ("Layers[0]") as follows:
 Name: diffuse_Base
 Enabled: On
 Tex: Connect here the "baseMapFile_head_color" file node
 Mask: full white color
 Blend Mode: Normal
 Opacity: 1
 
5.1.2- Create 3 new layers in the VRL_HEAD_DIFFUSE texture. They will be set as follows:
 Layers[1]
 Name: CM1_MASKS
 Tex: Connect here the "mapFile_head_cm1_color" file node
 Mask: connect here the "Out Color" connection from "VRL_CM1_MASKS" node
 Blend Mode: Lighten
 Opacity: 1
 
 Layers[2]
 Name: CM2_MASKS
 Tex: Connect here the "mapFile_head_cm2_color" file node
 Mask: connect here the "Out Color" connection from "VRL_CM2_MASKS" node
 Blend Mode: Normal
 Opacity: 1
 
 Layers[3]
 Name: CM3_MASKS
 Tex: Connect here the "mapFile_head_cm3_color" file node
 Mask: connect here the "Out Color" connection from "VRL_CM3_MASKS" node
 Blend Mode: Normal
 Opacity: 1
 

6- NODES CREATION – HEAD SKIN SHADER
  
6.1- Create a new VRayAlSurface shader. Name it "SHD_HEAD_INT_MAT" and set as follows:

   6.1.1- In "General parameters" tab, connect the out color from VRL_HEAD_NORMAL node into "Bump Map" slot.
   6.1.2- Set "Bump Type" as "Normal map in tangent space".
   
   6.1.3- In the "Diffuse" tab, connect the out color from VRL_HEAD_DIFFUSE node into "Diffuse" slot
   6.1.4 - Set "Sss Mix" to 1
   
6.2- Create a new VRayBumpMtl shader. Name it "SHD_HEAD_BMP_MAT" and set as follows:

   6.2.1- In "Base parameters" tab, connect the "SHD_HEAD_INT_MAT" shader into "Base Material" slot.
   6.2.2- In "Bump and Normal mapping" tab, connect the "baseMapFile_head_cavity" node into "Map" slot.
   6.2.3- Set "Bump Mult" to 0.1.
   
6.3- Apply the "SHD_HEAD_BMP_MAT" to "head_lod*_mesh".



7- NODES CREATION – BODY SKIN SHADER

7.1- Create a new VRayAlSurface shader. Name it "SHD_BODY_INT_MAT" and set as follows:

   7.1.1- In "General parameters" tab, connect the out color from "baseMapFile_body_normal" node into "Bump Map" slot.
   7.1.2- Set "Bump Type" as "Normal map in tangent space".
   
   7.1.3- In the "Diffuse" tab, connect the out color from "baseMapFile_body_color" node into "Diffuse" slot
   7.1.4 - Set "Sss Mix" to 1

7.2- Create a new VRayBumpMtl shader. Name it "SHD_BODY_BMP_MAT" and set as follows:

   7.2.1- In "Base parameters" tab, connect the "SHD_BODY_INT_MAT" shader into "Base Material" slot.
   7.2.2- In "Bump and Normal mapping" tab, connect the "baseMapFile_body_cavity" node into "Map" slot.
   7.2.3- Set "Bump Mult" to 0.1.
   
7.3- Apply the "SHD_BODY_INT_MAT" to "*_body_lod*_mesh".


8- NODES CREATION - MOUTH SHADER

8.1- Create a new VRayAlSurface shader. Name it "SHD_MOUTH_MAT" and set as follows:

   8.1.1- In "General parameters" tab, connect the out color from "baseMapFile_teeth_normal" node into "Bump Map" slot.
   8.1.2- Set "Bump Type" as "Normal map in tangent space".
   
   8.1.3- In the "Diffuse" tab, connect the out color from "baseMapFile_teeth_color" node into "Diffuse" slot
   8.1.4 - Set "Sss Mix" to 1

   8.1.5- In the "Reflection 1" tab, set “Reflection 1 Roughness” to 0.03

   8.1.6- Apply the "SHD_MOUTH_MAT" to " teeth_lod*_mesh".


8- NODES CREATION – INNER EYE SHADER

8.1- Create a new VRayAlSurface shader. Name it "SHD_EYE_IN_MAT" and set as follows:

   8.1.1- In "General parameters" tab, connect the out color from "baseMapFile_eyes_normal" node into "Bump Map" slot.
   8.1.2- Set "Bump Type" as "Normal map in tangent space".
   
   8.1.3- In the "Diffuse" tab, connect the out color from "baseMapFile_eyes_color" node into "Diffuse" slot
   8.1.4 - Set "Sss Mix" to 1

   8.1.5- In the "Reflection 1" tab, set “Reflection 1 Roughness” to 0.03

   8.1.6- Apply the "SHD_EYE_IN_MAT" to " eyeRight_lod*_mesh" and “eyeLeft_lod*_mesh”.

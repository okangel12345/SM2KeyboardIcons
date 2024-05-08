# Customs Textures Guide
**This guide is gonna be divided in two parts:**
1. Convert .texture to .dds
2. Convert .dds to .texture
## Prerequisites:
1. HxD editor
2. A .dds editing software
3. Modding Tool
4. Overstrike

## You need to rename .texture to .dds and then .dds to .texture after you've done the hex editing.
## 1. Convert .texture to .dds
Every single .texture file is a .dds that can be converted with the use of HxD. The game uses multiple formats, most of which are BC1_sRGB (for 48 kb color textures) and BC7_sRGB for (96 kb color textures). Color textures are the ones that end in "_c.texture". To convert them to .dds you need to do the following:
1. Extract the original 48 kb or 96 kb texture with the modding tool and **make a copy of it**.
2. Open it in HxD editor and select the first characters all the way to 0x73 (check Reference 1)
3. Paste one of the following:

**If 0x6E is equal to 48 = H**

```44 44 53 20 7C 00 00 00 07 10 0A 00 00 01 00 00 00 01 00 00 00 80 00 00 01 00 00 00 09 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 20 00 00 00 04 00 00 00 44 58 31 30 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 08 10 40 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 48 00 00 00 03 00 00 00 00 00 00 00 01 00 00 00 00 00 00 00```

**If 0x6E is equal to 63 = C**

```44 44 53 20 7C 00 00 00 07 10 0A 00 01 08 00 00 01 08 00 00 00 53 07 00 01 00 00 00 0A 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 20 00 00 00 04 00 00 00 44 58 31 30 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 08 10 40 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 63 00 00 00 03 00 00 00 00 00 00 00 01 00 00 00 00 00 00 00```

**For color HD textures use one of the following:**

```44 44 53 20 7C 00 00 00 07 10 0A 00 00 08 00 00 00 08 00 00 00 00 20 00 01 00 00 00 01 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 20 00 00 00 04 00 00 00 44 58 31 30 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 10 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 48 00 00 00 03 00 00 00 00 00 00 00 01 00 00 00 00 00 00 00```
### or
```44 44 53 20 7C 00 00 00 07 10 0A 00 00 08 00 00 00 08 00 00 00 00 20 00 01 00 00 00 01 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 20 00 00 00 04 00 00 00 44 58 31 30 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 10 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 63 00 00 00 03 00 00 00 00 00 00 00 01 00 00 00 00 00 00 00```

4. These headers will convert the .texture to .dds. However you may wanna experiment with the width and height values if you're gonna do anything that doesn't use a square aspect ratio. Same thing for format (which is usually decoded as H, C, or G)

## Reference 1
![Reference 1](https://cdn.discordapp.com/attachments/1237598576381661215/1237599366810697738/image.png?ex=663c3bba&is=663aea3a&hm=6b5a54ad5e13dcd03aebd04991eb6f6e0fc4804f90f70108e2ee3504410e7148&)

## 2. Convert .dds to .texture
1. Edit the .dds however you want and save following these parameters (check Reference 2)
2. Open it in HxD editor and select the first characters all the way to 0x93 (check Reference 3)
3. Paste the original texture ID you got rid of in the beginning (You can refer back to Reference 1 to see what I'm talking about)
4. Save the file and use it to replace both the low quality and hd versions of the texture in modding tool.

For HD textures just delete the DDS header.

## Reference 2
![image](https://github.com/okangel12345/SM2KeyboardIcons/assets/111395240/1e0100b9-981c-450b-9355-f38f483c5056)
## Reference 3
![Reference3](https://cdn.discordapp.com/attachments/1237598576381661215/1237599418853756978/7497786e-ff2a-47da-8d73-a2dec7a51152.png?ex=663c3bc6&is=663aea46&hm=e9df5ebb8e209e7e4cade2e1ed41adcdb8cab8a37646f97760ec748294968bd6&)

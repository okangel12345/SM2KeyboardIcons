# Customs Textures Guide
**This guide is gonna be divided in two parts:**
1. Convert .texture to .dds
2. Convert .dds to .texture
## Prerequisites:
1. HxD editor
2. A .dds editing software
3. Modding Tool
4. Overstrike

Convert .dds to .texture
1. Edit the .dds however you want and save following these parameters for low quality textures (check Reference 2)
2. Open it in HxD editor and select the first characters all the way to 0x93 (check Reference 3)
3. Paste the original texture ID you got rid of in the beginning (You can refer back to Reference 1 to see what I'm talking about)
4. Save the file and use it to replace both the low quality and hd versions of the texture in modding tool.

For HD textures just save as BC7_sRGB with no mip maps and delete the DDS header.

## Reference 2
![image](https://github.com/okangel12345/SM2KeyboardIcons/assets/111395240/1e0100b9-981c-450b-9355-f38f483c5056)
## Reference 3
![Reference3](https://cdn.discordapp.com/attachments/1237598576381661215/1237599418853756978/7497786e-ff2a-47da-8d73-a2dec7a51152.png?ex=663c3bc6&is=663aea46&hm=e9df5ebb8e209e7e4cade2e1ed41adcdb8cab8a37646f97760ec748294968bd6&)

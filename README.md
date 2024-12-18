# KTX2Loader_Gdevelop
Gdevelop extension to use ThreeJS KTX2Loader

HOW TO USE KTX2Loader:

1. Install the extension.
2. Use ktx2Loader action.
3. Write ktx2 file name. A path of the file doesnt matter. For example if the file path is "/assets/image.ktx2" you must write just "image.ktx2".
4. Create any custom name for the loaded texture map.
5. The loaded map is stored at scene.userData.textures[mapName]. You can use any other extension to add this texture map to desired material.


HOW TO CREATE KTX2 TEXTURE:

1. Download ktx-software from: https://github.com/KhronosGroup/KTX-Software/releases (or any other source).
2. Put desired jpg/png/any_other image in any folder.
3. Open console in this folder.
4. Use the next command: ktx create --format R8G8B8A8_UNORM --encode basis-lz --clevel 1 --qlevel 120 --assign-oetf srgb --assign-primaries srgb --convert-oetf srgb --convert-primaries srgb original_image_name.jpg desired_name_for_newImage.ktx2
5. --clevel can have values 1-5.
6. --qlevel can have values 1-255.
7. Mipmaps generation is available. Add --generate-mipmap --mipmap-filter box to the command above to generate mipmaps.

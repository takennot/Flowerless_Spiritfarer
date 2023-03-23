# Flowerless Spiritfarer
A patched Spiritfarer .dll file that removes spirit flowers requirements from recipes.

# Install
**_Don't forget to backup the original file before replacing!_**

* Download to `Spiritfarer\Spiritfarer_Data\Managed` folder. Agree to replace.

# Uninstall
Place the orignal .dll file (**_You did create a backup, right?_**) to `Spiritfarer\Spiritfarer_Data\Managed` and agree to replace.

If you do not have a backup, then download original dll file from [here](https://github.com/takennot/Flowerless_Spiritfarer/raw/main/Assembly-CSharp_clean.dll).
Don't forget to rename it to `Assembly-CSharp.dll`!

If the method above did not work for whatever reason - go to steam library, right click on the game, properties --> local files --> Verify integrity

# How
Just changed `false` to `true` in the `MeetInventoryRequirement` method (`Assembly_CSharp.dll --> MainInventory --> MeetInventoryRequirement`).

From:
`if (base.CountItemOfType(GameUtil.MainInventory._spiritFlowerProperty) < itemStack.Quantity)
			{
				return false;
			}`

To:
`if (base.CountItemOfType(GameUtil.MainInventory._spiritFlowerProperty) < itemStack.Quantity)
			{
				return true;
			}`

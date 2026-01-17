# Concept Board Creator ![Concept Board Creator Icon](Resources/ConceptBoardCreator_icon32.png)

**Concept Board Creator** is a powerful Unreal Engine Editor Utility Widget designed to instantly turn reference images into organized, 3D concept boards within your level. Whether you are building a mood board for a virtual production shoot or a reference wall for environment art, this tool automates the tedious process of material creation and aspect-ratio scaling.

![Concept Board Creator UI](Resources/ConceptBoard_UI.png) 
*Load your textures, set your grid, and generate organized reference boards in seconds.*

---

## 🚀 The Concept
Creating reference boards in 3D space usually involves manually creating planes, making material instances, and painstakingly lining them up. **Concept Board Creator** handles the heavy lifting by:

1. **Automating Materials:** It checks if a texture already has a dedicated material instance. If not, it generates one from a high-quality unlit master material (with exposed desaturation and emissive parameters) and saves it alongside your texture.
2. **Smart Layouts:** It calculates the correct aspect ratio for every image and organizes them into a clean grid based on your "Max Images Per Row" settings.
3. **Flexible Spawning:** You can spawn boards directly in front of your current viewport camera or at a specific world location, all parented to a single actor for easy movement and rotation.

---

## ✨ Key Features

* **One-Click Material Generation:** Automatically creates and assigns Material Instances with unlit, desaturatable, and emissive properties.
* **Aspect Ratio Awareness:** Planes are automatically scaled to match the dimensions of the source texture, preventing any image stretching.
* **Integrated Backing:** Generates a transparent grey backing panel (with its own customizable master material) that can be sized to fit your custom layout.
* **Customizable Spacing:** Fine-tune the X and Z padding between images directly from the UI.
* **World/Camera Alignment:** Toggle between spawning the board at the world origin or snapping it to your current perspective.

---

## 📖 Quick Start Guide

1. **Launch the Tool:** Right-click `EUW_ConceptBoardCreator` and select **Run Editor Utility Widget**.
2. **Load Textures:** Add your reference images to the **Textures** array in the UI.
3. **Configure Layout:**
    * Set your **Image Scale** and **Max Images Per Row**.
    * Adjust **XSpacing** and **ZSpacing** to define the gaps between frames.
    * Set the **Backing Border** size to adjust the frame of your board.
4. **Choose Location:** Check **Spawn Infront Camera** if you want the board to appear where you are currently looking.
5. **Generate:** Click **Create Board**. The tool will generate the parent actor, the planes, the materials, and the backing.
    * *Note: To update a board, simply delete the generated actor and click "Create Board" again. Previously created material instances will be reused automatically.*

---

## 🛠 UI Overview

| Feature | Function |
| :--- | :--- |
| **Textures Array** | List of all textures to be included on the board. |
| **Image Scale** | Master multiplier for the size of all image planes. |
| **Max Images Per Row** | Defines when the grid logic should start a new horizontal line. |
| **X/Z Spacing** | Controls the horizontal and vertical gaps between image planes. |
| **Backing Border** | Allows the user to size and adjust the border of the transparent background panel. |
| **Spawn Infront Camera** | Snaps the board's spawn location to your current viewport perspective. |

---

## 📦 Installation & Prerequisites

### Prerequisites
To use this tool, the following built-in Unreal Engine plugins must be enabled:
* **Virtual Production Utilities**
* **Blueprint Material and Texture Nodes**

### Installation
1. Download the repository and extract the files.
2. Copy the `ConceptBoardCreator` folder into your project's `Plugins` directory.
3. Restart Unreal Engine.
4. Ensure **Show Plugin Content** is enabled in your Content Browser settings to locate the widget.
5. Developed and tested for **Unreal Engine 5.7**.

---

## 🤝 Contributing
Concept Board Creator was built to streamline the art direction workflow. If you have ideas for improvements, new features, or find a bug, please open an issue or submit a pull request!

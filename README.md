# CIDOO QK61 V2 Custom VIA Layout

A repository dedicated to archiving the official layout definitions and my personal custom keymap configuration for the **CIDOO QK61 V2** 60% mechanical keyboard using the VIA web configurator.

Since the CIDOO QK61 V2 is not natively detected by VIA out of the box, this repository ensures you always have the necessary canvas/definition files and backup configurations ready.

## 📁 Repository Files

*   **`CIDOO QK61 V2.JSON`**: The official keyboard definition file downloaded from CIDOO's website. It acts as the bridge for VIA to physically recognize the keyboard layout.
*   **`cidoo_qk61_v2.layout.json`**: My custom 4-layer layout export. It maps out dual operating system layers and specialized macro/navigation sub-layers.


## 🎹 Custom Layout Architecture

My layout splits the keyboard into 4 specific layers (`0` through `3`) to maximize the utility of the 60% physical footprint:

### Layer 0: Default Windows Profile
*   **Grave Escape**: The escape key uses `KC_GESC`. It triggers standard Escape when tapped alone, but outputs modifiers like Til (`~`) or Crase (`` ` ``) when used with Shift or GUI.
*   **Standard Modifiers**: Retains classic physical Left Ctrl, Left GUI, and Left Alt execution for native Windows workflows.

### Layer 1: Dedicated macOS Profile
*   **Caps Lock Layer Tap**: Programmed as `MT(MOD_LCTL, KC_ESC)`. Tapping the physical Caps Lock key sends a clean `Escape` command, while holding it acts as a true `Left Control`.
*   **Pure Hyper Key**: Placed precisely on the bottom-left corner modifier. It leverages custom quantum mapping (`MEH(KC_LGUI)`) to fire **Ctrl + Shift + Alt + Win/Cmd** instantly as a pure shortcut activator.
*   **Mac Navigation Mapping**: Flips physical space layouts to mimic a native Apple MacBook platform layout (`Opt` $\rightarrow$ `Cmd` sequence).

### Layer 2: Media, Navigation & RGB Extensions
*   **Arrow Cluster**: Accessible via layer modifiers, shifting `W, A, S, D` or standard alphanumeric locations into dedicated `Up, Left, Down, Right` arrows.
*   **System Controls**: Integrates hardware volume keys (`MUTE`, `VOLD`, `VOLU`), screen brightness controls (`BRID`, `BRIU`), and default media tracking switches.
*   **RGB Management**: Maps lighting configuration variables directly onto the layout matrix (`RGB_VAD`, `RGB_VAI`).

### Layer 3: Function Keys & Integrated Numpad
*   **F-Row Execution**: Transforms the numeric row (`1` through `=`) into true functional operations (`F1` through `F12`).
*   **Hidden Numpad Cluster**: Maps an entire 10-key numpad matrix straight over the alpha cluster (`P1` through `P9` and `P0`) for fast data entry.
*   **Profile Toggles**: Houses profile toggles (`TG(0)` and `TG(1)`) to transition the primary layout state safely.

## 🚀 Setup & Configuration Guide

Follow these steps exactly to get the keyboard running with VIA and import the custom configuration.

### 1. Prerequisites & Connection
1. Flip the physical toggle switch on the back of the keyboard to **Wired mode** (middle position).
2. Connect the keyboard to your computer via a **USB-C cable** (VIA requires a wired connection to map keys).
3. Open a compatible WebUSB browser (strictly **Google Chrome** is recommended, as privacy browsers like Brave may block layout file downloads).
4. Navigate to the web app: [usevia.app](https://usevia.app).

### 2. Loading the JSON Keyboard Definition (Crucial Step)
Because the keyboard requires external definitions to be recognized, you must load this first:
1. Inside VIA, click on the **Settings** tab (the gear icon ⚙️) in the top-left area.
2. Toggle on the switch labeled **"Show Design tab"**.
3. A new **Design** tab (represented by a paintbrush icon 🖌️) will unlock in the top navigation bar. Click it.
4. Drag and drop the **`CIDOO QK61 V2.JSON`** file from this repository into the upload box.
5. **⚠️ CRUCIAL STEP:** Once the JSON is uploaded, **refresh the web page (`F5` or `Ctrl + R`)**. VIA requires a quick reload after injecting unsubmitted definitions to correctly pair and match the hardware signature.
6. Head back to the main **Configure** tab, click **Authorize device**, select your keyboard from the prompt, and hit connect.

### 3. Importing My Custom Layout Configuration
Once VIA successfully renders the 60% visual keymap, you can apply my personal setup:
1. Click on the **Save + Load** tab (represented by an icon with a sheet of paper and arrows) in the top menu.
2. Under the **Load Saved Layout** section, click the **Load** button.
3. Select the **`cidoo_qk61_v2.layout.json`** file from this repository.
4. The keymap will flash instantaneously and save into the keyboard's onboard memory.

## 📜 License

This project is licensed under the terms of the **MIT License**. For full details, please refer to the dedicated [LICENSE](LICENSE) file included in this repository.

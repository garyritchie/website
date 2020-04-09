---
title: "1.4 Release Notes"
linkTitle: "1.4 Release Notes"
weight: 1
description: >
  Release notes for Regolith 1.4.
---

Regolith R1.4 is a major feature release which includes several big changes.  The ISO-based installer is now based from the Xubuntu image, and moves from the gdm3 display manager to LightDM.  This means less resource consumption and dramatically smaller download size.  This does **not** mean that Regolith uses XFCE4 or any other aspect of Xubuntu other than the install image.  A new look, `ayu-mirage-regolith` and file search dialog round out the major new features.  Read below for more details.

{{% pageinfo %}}
If you maintain your own i3 config file, note that the copy shipped in Regolith 1.4 has changed in that it reads more configuration from Xresources.  The intention of this change is to require a full copy of the i3 config file <b>less often</b>, by allowing users to customize the system via Xresource overrides instead of copy/edit of the i3 config file.  Merging changes from version to version can be error-prone and confusing for some users.
{{% /pageinfo %}}

Gratitude goes out to Regolith contributors and users @cheginit, @nalderto, @baldrailers, @ivomarino, @Josh-Letts, @LawZava, @SkyyySi, @tomster, @gdeflaux, @appelgriebsch, and @MrKovar for their time and attention.  Also thanks to all that helped to test and filed issues for bugs and feature requests!

## Features

<table class="table">
    <tbody>
        <tr>
            <td>Remontoire 1.3.1</td>
            <td><a href="../regolith-remontoire-screenshot-131.png"><img class="shadow" src="../regolith-remontoire-screenshot-131.png"/></a></td>
            <td>
            <ul>
            <li>Can render keybindings from i3 over socket or from any file.</li>
            <li>Can be configured to display on any screen edge.</li>
            <li>Visual updates and bug fixes.</li>
            </ul>
            </td>
        </tr>
        <tr>
            <td>New default look: TBD</td>
            <td>TBD</td>
            <td>A new look with a bolder typeface (JetBrains Mono) and a darker, higher constrast color theme (Ayu Mirage) complement Regolith's default look in 1.4.  Cahuella, and other looks are still available.</td>
        </tr>
        <tr>
            <td>New File Search Dialog</td>
            <td>TBD</td>
            <td>Based on Rofi and mlocate, users can now quickly find files and launch their default editors from a global dialog.</td>
        </tr>
        <tr>
            <td>Easier Customization</td>
            <td></td>
            <td>Virtually everything exportable from the i3 config can now be overridden directly with Xresources declarations, from changing the meta key to specifying the command that launches the app search dialog.  Additionally, up to 3 user configured programs can be set to be loaded upon start.  All of this is possible without creating a user copy of the i3 config file.</td>
        </tr>
        <tr>
            <td>i3xrocks supports conf.d style configuration</td>
            <td></td>
            <td>The status indicators in the bar can now be installed and configured independently.  This allows for a cleaner dependency model and more efficient runtime characteristics. It also provides future flexibility for user contributed modules and status indicators.  Plus, users can provide their own block descriptors in the user directory to easily override the defaults without having to change the i3 config file.</td>
        </tr>
        <tr>
            <td>New architecture support: <code>arm64</code></td>
            <td></td>
            <td>With testing done on a Raspberry Pi 4, Regolith now is installable via PPA when using Ubuntu on arm64 devices with the necessary hardware support.</td>
        </tr>
        <tr>
            <td>New Ubuntu release support: Focal Fossa</td>
            <td>TBD</td>
            <td>Regolith runs as a desktop environment in Canonical's latest release of Ubuntu: 20.04.</td>
        </tr>
        <tr>
            <td>Time and Space Optimizations in ISO release</td>
            <td>TBD</td>
            <td>By switching from gdm3 to LightDM, Regolith avoids loading some unnecessary desktop components into RAM, resulting in between 200MB to 300MB savings on cold start.  Additionally, the LiveCD installer is now based on the Xubuntu LiveCD which dramatically lowers the size of the installer and install image of the system.  The trade-off is that users need to install more of the software they require after installation.</td>
        </tr>
        <tr>
            <td>Pluggable Desktop Notification Components</td>
            <td>TBD</td>
            <td>Users can now cleanly switch between desktop notification implementations such as dunst and notify-osd, in addition to Rofication without resorting to hacks.</td>
        </tr>        
        <tr>
            <td>Picom (Compton) config can be overriden by user</td>
            <td></td>
            <td>Users can provide their own Picom compositor config in their user directory.</td>
        </tr>
        <tr>
            <td>i3 reload becomes Regolith reload</td>
            <td></td>
            <td>Refreshing the UI (look, colors, fonts, etc.) after making changes is now as easy as <span class="text-nowrap"><span class="badge badge-warning">super</span> <span class="badge badge-warning">shift</span> <span class="badge badge-warning">r</span></span>.</td>
        </tr>   
    </tbody>
</table>

## Fixes

Have a look at the R1.4 project page for a [list of bug fixes](https://github.com/orgs/regolith-linux/projects/11).
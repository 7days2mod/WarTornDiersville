# WarTornDiersville

Prefabs by GuppyCur and Lazman

![Wartorn1](https://raw.githubusercontent.com/7days2mod/WarTornDiersville/master/Wartorn1.jpg)
![Wartorn2](https://raw.githubusercontent.com/7days2mod/WarTornDiersville/master/Wartorn2.jpg)

Copy the prefabs .tts and .xml into the /Data/Prefabs folder (or extract the zip in the game folder for 7 days to die)

In rwgmixer.xml:

Add to the `ruleset` section:

```
      <cell_rule name="WartornDiers" position="0,0" prob="0"/>
```

change the position to the hub where you want it to spawn, or remove the position attribute and increase the prob to a value above 0 (0.05 would work) to allow it to spawn randomly.

Add to the `cell_rules` section:

```
    <cell_rule name="WartornDiers">
      <cave_count value="1,3"/>
      <path_material value="asphalt" />
      <path_radius value="7" />
      <hub_rule name="WartornDiers"/>
      <wilderness_rule name="wildernessDefault"/>
    </cell_rule>
```

Add to the `hub_rules` section:

```
    <hub_rule name="WartornDiers">
      <hub_type value="town"/>
      <width value="299,299" />
      <height value="312,312" />
      <hub_layout name="WartornDiersLayout"/>
      <prefab_rule name="townBuildings"/>
    </hub_rule>
```

Add to the `hub_layouts` section:

```
    <hub_layout name="WartornDiersLayout">
      <township_type value="town"/>
      <street start_point="0,0" end_point="299,0" path_material="asphalt" path_radius="7"/>
      <street start_point="299,0" end_point="299,258" path_material="asphalt" path_radius="7"/>
      <street start_point="299,258" end_point="0,258" path_material="asphalt" path_radius="7"/>
      <street start_point="0,258" end_point="0,0" path_material="asphalt" path_radius="7"/>
      <street start_point="0,129" end_point="299,129" path_material="asphalt" path_radius="7"/>
      <street start_point="150,0" end_point="150,312" path_material="asphalt" path_radius="7"/>
      <lot min_x_y="157,123" prefab="_WartornDiers04" rotation_to_road="0"/><!-- 135x115 -->
      <lot min_x_y="157,252" prefab="_WartornDiers02" rotation_to_road="0"/><!-- 135x115 -->
      <lot min_x_y="8,123" prefab="_WartornDiers03" rotation_to_road="0"/><!-- 135x115 -->
      <lot min_x_y="8,252" prefab="_WartornDiers01" rotation_to_road="0"/><!-- 135x115 -->
      <lot min_x_y="60,300" prefab="_WartornSchool(LazMan)" rotation_to_road="0"/><!-- 36x34 -->
      <lot min_x_y="100,309" prefab="_WartornAutomotive(Laz_Man)" rotation_to_road="0"/><!-- 44x43 -->
      <lot min_x_y="158,311" prefab="_WartornStripmall(Guppycur)" rotation_to_road="0"/><!-- 45x45 -->
      <lot min_x_y="207,287" prefab="_WartornWooden_Store(Guppycur)" rotation_to_road="0"/><!-- 26x21 -->
    </hub_layout>
```

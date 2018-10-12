# Contributing

General details of how to work on BattleScribe data files can be found on the [BSData Catalogue Development Wiki][].

In addition to our [Code of Conduct][] please remember these guidelines:

- Be polite. Everyone here gets no money for this work. It's open-source community.
- Don't complain, but instead try to fix it. Or at least open an issue. Someone probably will fix it.
- Spend only spare time here. You won't get money for this.
- Try to fix current issues first.

Please try to keep the following recommendations in mind when working on Middle-earth&trade;:

## Prefer Shared Entries over Repetition

It's better to write something once, and use it many places than to have copies of it in many different places - if an issue is found with the selection, fixing it in one place should resolve the issue everywhere.

You'll find that we have Shared Selection Entries in the main GST for:

- Common wargear, including armour, weapons and other equipment.
- Hero wargear that is used by multiple versions of a model, for example _Andrúil, the Flame of the West_ is used by both ___Aragorn - Strider___ and ___Aragorn, King Elessar___.
- Models that appear in more than one Army List, including both heroes and warriors.

We also have Shared Rules and Shared Profiles for the rules and underlying upgrades that the Entries use, these can also be used on any custom entries you need in your list - for example _Narsil_ is specific to the ___Heroes of Númenor___ list, but it uses the shared rules  _Master-forged Weapon_, _Hand-and-a-half Weapon_ as well as it's own Rule and Profile.

## Modifiers are your friends

The vast majority of the shared wargear is configured with a Max In Parent constraint of 1, and a Hero Point cost. When including these as standard wargear, add the Entry Link, and then add a modifier to set the Point cost to 0 and a constraint for Min in Parent to 1 to have the item automatically selected. Similarly if adding the entry as an optional purchase on a warrior, add a modifier to correct the Point cost.

## Armour, Shields and `(Included)` Entries

Armour and Shields both give a benefit to the model's Defence, and to reflect this on the roster these Entries have been configured with Profiles that include the defence bonus text. In keeping with other systems, we also adjust the stat-line on the model's profile when the user selects the option. However in the case of standard wargear, this bonus is already inlcuded in the model's stat-line, so in these cases we use the `ArmourType (Included)` shared entry - this has the point cost set to 0, as well as a Min in Parent constraint to add it to the unit, and doesn't display the bonus rule to avoid confusion. 

## Don't forget The Leader

All heroes above __Minor Hero__ could be chosen as the Armies Leader, so please add that Entry Link to each hero so that the user can select the appropriate leader. Once added to all heroes the option should automatically hide itself in the Roster Editor if there's a higher tier hero in the roster.

[BSData Catalogue Development Wiki]: https://github.com/BSData/catalogue-development/wiki
[Code of Conduct]: /BSData/middle-earth/blob/master/CODE_OF_CONDUCT.md

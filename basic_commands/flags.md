## Flags

Flags are similar to bookmarks. They represent a certain offset in the file. Flags can be grouped in 'flag spaces'. A flag space is something like a namespace for flags. They are used to group flags of similar characteristic or type. Some example of flagspaces could be sections, registers, symbols.

To create a flag just type:

     [0x4A13B8C0]> f flag_name @ offset
    
You can remove a flag by prefixing its name with `-`. Most commands accept `-` as argument-prefix as a way to delete items.

     [0x4A13B8C0]> f -flag_name 

To switch between or create new flagspaces use the `fs` command:

     [0x4A13B8C0]> fs   ; list flag spaces

     00   symbols
     01   imports
     02   sections
     03   strings
     04   regs
     05   maps
     
     [0x4A13B8C0]> fs symbols ; select only flags in symbols flagspace
     [0x4A13B8C0]> f          ; list only flags in symbols flagspace

     [0x4A13B8C0]> fs *      ; select all flagspaces
     
You can rename flags with `fr`.

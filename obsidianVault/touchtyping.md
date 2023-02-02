default  partial alphanumeric_keys

xkb_symbols "basic" {

  

include "latin"

  

name[Group1]="French";

  

key <AE01>    { [ ampersand,      1,  onesuperior,   exclamdown ]    };

key <AE02>    { [ eacute,      2,   asciitilde, oneeighth ]    };

key <AE03>    { [  quotedbl,      3,   numbersign, sterling ]    };

key <AE04>    { [apostrophe,      4, dead_circumflex,   dollar ]    };

key <AE05>    { [ parenleft,      5,  ugrave, threeeighths ]    };

key <AE06>    { [ minus,      6,      bar,  fiveeighths ]    };

key <AE07>    { [ egrave,      7,    grave, seveneighths ]    };

key <AE08>    { [underscore,      8, backslash, trademark ]    };

key <AE09>    { [  period,      9,  asciicircum, plusminus ]    };

key <AE10>    { [ 0,      agrave,       at,   degree ]    };

key <AE11>    { [parenright, degree, exclam, questiondown ]    };

key <AE12>    { [ equal,   plus,   dollar,  dead_ogonek ]    };

  

key <AD01>    { [     a,      A,       ae,       AE ]    };

key <AD02>    { [     z,      Z, guillemotleft,    less ]    };

key <AD03>    { [     e,      E, EuroSign,     cent ]    };

key <AD11>    { [braceleft, dead_diaeresis, dead_diaeresis, dead_abovering ] };

key <AD12>    { [ braceright,   sterling, currency,  dead_macron ]    };

  

key <AC01>    { [     q,      Q,       at,  Greek_OMEGA ]    };

key <AC10>    { [     m,      M,       mu, masculine ]    };

key <AC11>    { [ bracketleft, percent, dead_circumflex, dead_caron]    };

key <TLDE>    { [twosuperior, asciitilde, notsign,  notsign ]    };

  

key <BKSL>    { [  asterisk,     mu,   dead_grave,   dead_breve ]    };

key <AB01>    { [     w,      W,  lstroke,  Lstroke ]    };

key <AB07>    { [ comma,   question,   dead_acute, dead_doubleacute ] };

key <AB08>    { [ semicolon, ccedilla, horizconnector,   multiply ]    };

key <AB09>    { [ colon,  slash, periodcentered,   division ]    };

key <AB10>    { [ bracketright, section, dead_belowdot, dead_abovedot ] };

  

include "level3(ralt_switch)"

};

  

partial alphanumeric_keys

xkb_symbols "olpc" {

// Contact: Sayamindu Dasgupta <sayamindu@laptop.org>

include "fr(basic)"

  

name[Group1]="French";

  

key <I219>    { [ less, greater ]    };

key <AD11>    { [ dead_circumflex, dead_diaeresis, notsign, dead_abovering ]    };

key <AB08>    { [ semicolon, period, underscore, multiply ]    };

key <TLDE>    { [ twosuperior, asciitilde, VoidSymbol, VoidSymbol ]    };

  

// Some keys only have the Shift+AltGr character printed on them (alongside

// the unmodified one). Make such keys shift-invariant so that the printed

// value is achieved by pressing AltGr or Shift+AltGr.

key <AB02>    { [ x,  X,  guillemotright, guillemotright ]    };

key <AC02>    { [ s,  S,  ssharp, U1E9E ]    };

key <AD02>    { [ z,  Z,  guillemotleft, guillemotleft ]    };

};

  

partial alphanumeric_keys

xkb_symbols "Sundeadkeys" {

  

// Modifies the basic French layout to use the Sun dead keys

  

include "fr(basic)"

  

key <AD11>    { [dead_circumflex, dead_diaeresis ]    };

key <AB07>    { [comma,   question,  dead_acute, dead_doubleacute ]    };

};

  

partial alphanumeric_keys

xkb_symbols "sundeadkeys" {

include "fr(Sundeadkeys)"

  

name[Group1]="French (with Sun dead keys)";

};

  

partial alphanumeric_keys

xkb_symbols "nodeadkeys" {

  

// Modifies the basic French layout to eliminate all dead keys

  

include "fr(basic)"

  

name[Group1]="French (no dead keys)";

  

key <AE12>    { [ equal,   plus,   braceright,   ogonek ]    };

key <AD11>    { [asciicircum,  diaeresis ]    };

key <AD12>    { [ dollar,   sterling, currency,   macron ]    };

key <AC11>    { [ ugrave, percent,  asciicircum,    caron ]    };

key <BKSL>    { [  asterisk,     mu,    grave,    breve ]    };

key <AB07>    { [ comma,   question,    acute,  doubleacute ]    };

key <AB10>    { [ exclam, section, dead_belowdot, abovedot ]    };

};

  
  

// Unicode French derivative

// Loose refactoring of the historic Linux French keyboard layout

//

// Copyright © 2006-2008 Nicolas Mailhot <nicolas.mailhot @ laposte.net>

//

// Credits (fr-latin1, fr-latin0, fr-latin9)

//   © 199x-1996 René Cougnenc ✝

//   © 1997-2002 Guylhem Aznar <clavier @ externe.net>

//   © 2003-2006 Nicolas Mailhot <nicolas.mailhot @ laposte.net>

//

// ┌─────┬─────┬─────┬─────┬─────┬─────┬─────┬─────┬─────┬─────┬─────┬─────┬─────┲━━━━━━━━━┓

// │ ³ ¸ │ 1 ̨  │ 2 É │ 3 ˘ │ 4 — │ 5 – │ 6 ‑ │ 7 È │ 8 ™ │ 9 Ç │ 0 À │ ° ≠ │ + ± ┃ ⌫ Retour┃

// │ ² ¹ │ & ˇ │ é ~ │ " # │ ' { │ ( [ │ - | │ è ` │ _ \ │ ç ^ │ à @ │ ) ] │ = } ┃  arrière┃

// ┢━━━━━┷━┱───┴─┬───┴─┬───┴─┬───┴─┬───┴─┬───┴─┬───┴─┬───┴─┬───┴─┬───┴─┬───┴─┬───┺━┳━━━━━━━┫

// ┃   ┃ A Æ │ Z Â │ E ¢ │ R Ê │ T Þ │ Y Ÿ │ U Û │ I Î │ O Œ │ P Ô │ ¨ ˚ │ £ Ø ┃Entrée ┃

// ┃Tab ↹  ┃ a æ │ z â │ e € │ r ê │ t þ │ y ÿ │ u û │ i î │ o œ │ p ô │ ^ ~ │ $ ø ┃   ⏎   ┃

// ┣━━━━━━━┻┱────┴┬────┴┬────┴┬────┴┬────┴┬────┴┬────┴┬────┴┬────┴┬────┴┬────┴┬────┺┓  ┃

// ┃    ┃ Q Ä │ S „ │ D Ë │ F ‚ │ G ¥ │ H Ð │ J Ü │ K Ï │ L Ŀ │ M Ö │ % Ù │ µ ̄  ┃  ┃

// ┃Maj ⇬   ┃ q ä │ s ß │ d ë │ f ‘ │ g ’ │ h ð │ j ü │ k ï │ l ŀ │ m ö │ ù ' │ * ` ┃  ┃

// ┣━━━━━━━┳┹────┬┴────┬┴────┬┴────┬┴────┬┴────┬┴────┬┴────┬┴────┬┴────┬┴────┲┷━━━━━┻━━━━━━┫

// ┃   ┃ > ≥ │ W “ │ X ” │ C ® │ V ← │ B ↑ │ N → │ ? … │ . . │ / ∕ │ § − ┃         ┃

// ┃Shift ⇧┃ < ≤ │ w « │ x » │ c © │ v ⍽ │ b ↓ │ n ¬ │ , ¿ │ ; × │ : ÷ │ ! ¡ ┃Shift ⇧  ┃

// ┣━━━━━━━╋━━━━━┷━┳━━━┷━━━┱─┴─────┴─────┴─────┴─────┴─────┴───┲━┷━━━━━╈━━━━━┻━┳━━━━━━━┳━━━┛

// ┃   ┃   ┃   ┃ ␣     Espace fine insécable ⍽ ┃   ┃   ┃   ┃

// ┃Ctrl   ┃Meta   ┃Alt ┃ ␣ Espace   Espace insécable ⍽ ┃AltGr ⇮┃Menu   ┃Ctrl   ┃

// ┗━━━━━━━┻━━━━━━━┻━━━━━━━┹───────────────────────────────────┺━━━━━━━┻━━━━━━━┻━━━━━━━┛

partial alphanumeric_keys

xkb_symbols "oss" {

  

include "latin"

include "level3(ralt_switch)"

include "nbsp(level4n)"

include "keypad(oss)"

  

name[Group1]="French (alt.)";

  

// First row

key <TLDE>    { [  twosuperior, threesuperior,      onesuperior,      dead_cedilla ] }; // ² ³ ¹ ¸

key <AE01>    { [    ampersand,            1,       dead_caron,       dead_ogonek ] }; // & 1 ˇ ̨

key <AE02>    { [       eacute,            2,       asciitilde,            Eacute ] }; // é 2 ~ É

key <AE03>    { [     quotedbl,            3,       numbersign,        dead_breve ] }; // " 3 # ˘

key <AE04>    { [   apostrophe,            4,        braceleft,         0x1002014 ] }; // ' 4 { — (tiret cadratin)

key <AE05>    { [    parenleft,            5,      bracketleft,         0x1002013 ] }; // ( 5 [ – (tiret demi-cadratin)

key <AE06>    { [        minus,            6,              bar,         0x1002011 ] }; // - 6 | ‑ (tiret insécable)

key <AE07>    { [       egrave,            7,            grave,            Egrave ] }; // è 7 ` È

key <AE08>    { [   underscore,            8,        backslash,         trademark ] }; // _ 8 \ ™

key <AE09>    { [     ccedilla,            9,      asciicircum,          Ccedilla ] }; // ç 9 ^ Ç

key <AE10>    { [       agrave,            0,               at,            Agrave ] }; // à 0 @ À

key <AE11>    { [   parenright,       degree,     bracketright,          notequal ] }; // ) ° ] ≠

key <AE12>    { [        equal,         plus,       braceright,         plusminus ] }; // = + } ±

  

// Second row

key <AD01>    { [            a,            A,               ae,                AE ] }; // a A æ Æ

key <AD02>    { [            z,            Z,      acircumflex,       Acircumflex ] }; // z Z â Â

key <AD03>    { [            e,            E,         EuroSign,              cent ] }; // e E € ¢

key <AD04>    { [            r,            R,      ecircumflex,       Ecircumflex ] }; // r R ê Ê

key <AD05>    { [            t,            T,            thorn,             THORN ] }; // t T þ Þ

key <AD06>    { [            y,            Y,       ydiaeresis,        Ydiaeresis ] }; // y Y ÿ Ÿ

key <AD07>    { [            u,            U,      ucircumflex,       Ucircumflex ] }; // u U û Û

key <AD08>    { [            i,            I,      icircumflex,       Icircumflex ] }; // i I î Î

key <AD09>    { [            o,            O,               oe,                OE ] }; // o O œ Œ

key <AD10>    { [            p,            P,      ocircumflex,       Ocircumflex ] }; // p P ô Ô

key <AD11>    { [  dead_circumflex,   dead_diaeresis,       dead_tilde,    dead_abovering ] }; // ^ ̈ ̃ ˚

key <AD12>    { [       dollar,     sterling,           oslash,          Ooblique ] }; // $ £ ø Ø

  

// Third row

key <AC01>    { [            q,            Q,       adiaeresis,        Adiaeresis ] }; // q Q ä Ä

key <AC02>    { [            s,            S,           ssharp, doublelowquotemark ] }; // s S ß „

key <AC03>    { [            d,            D,       ediaeresis,        Ediaeresis ] }; // d D ë Ë

key <AC04>    { [            f,            F,  leftsinglequotemark, singlelowquotemark ] }; // f F ‘ ‚

key <AC05>    { [            g,            G, rightsinglequotemark,               yen ] }; // g G ’ ¥

key <AC06>    { [            h,            H,              eth,               ETH ] }; // h H ð Ð

key <AC07>    { [            j,            J,       udiaeresis,        Udiaeresis ] }; // j J ü Ü

key <AC08>    { [            k,            K,       idiaeresis,        Idiaeresis ] }; // k K ï Ï

key <AC09>    { [            l,            L,        0x1000140,         0x100013F ] }; // l L ŀ Ŀ

key <AC10>    { [            m,            M,       odiaeresis,        Odiaeresis ] }; // m M ö Ö

key <AC11>    { [       ugrave,      percent,       dead_acute,            Ugrave ] }; // ù % ' Ù

key <BKSL>    { [     asterisk,           mu,       dead_grave,       dead_macron ] }; // * µ ` ̄

  

// Fourth row

key <LSGT>  { [         less,      greater,    lessthanequal,  greaterthanequal ] }; // < > ≤ ≥

key <AB01>  { [            w,            W,    guillemotleft,   leftdoublequotemark ] }; // w W « “

key <AB02>  { [            x,            X,   guillemotright,  rightdoublequotemark ] }; // x X » ”

key <AB03>  { [            c,            C,        copyright,        registered ] }; // c C © ®

key <AB04>  { [            v,            V,        0x100202F,         leftarrow ] }; // v V ⍽ ← (espace fine insécable)

key <AB05>  { [            b,            B,        downarrow,           uparrow ] }; // b B ↓ ↑

key <AB06>  { [            n,            N,          notsign,        rightarrow ] }; // n N ¬ →

key <AB07>  { [        comma,     question,     questiondown,         0x1002026 ] }; // , ? ¿ …

key <AB08>  { [    semicolon,       period,         multiply,         0x10022C5 ] }; // ; . × ⋅

key <AB09>  { [        colon,        slash,         division,         0x1002215 ] }; // : / ÷ ∕

key <AB10>  { [       exclam,      section,       exclamdown,         0x1002212 ] }; // ! § ¡ −

};

  

partial alphanumeric_keys

xkb_symbols "oss_latin9" {

  

// Restricts the fr(oss) layout to latin9 symbols

  

include "fr(oss)"

include "keypad(oss_latin9)"

  

name[Group1]="French (alt., Latin-9 only)";

  

// First row

key <AE01>    { [    ampersand,            1,       dead_caron,      dead_cedilla ] }; // & 1 ˇ ¸

key <AE03>    { [     quotedbl,            3,       numbersign,        dead_tilde ] }; // " 3 # ~

key <AE04>    { [   apostrophe,            4,        braceleft,        underscore ] }; // ' 4 { _

key <AE05>    { [    parenleft,            5,      bracketleft,             minus ] }; // ( 5 [ -

key <AE06>    { [        minus,            6,              bar,             minus ] }; // - 6 | -

key <AE08>    { [   underscore,            8,        backslash,         backslash ] }; // _ 8 \ \

key <AE11>    { [   parenright,       degree,     bracketright,             equal ] }; // ) ° ] =

  

// Third row

key <AC02>    { [            s,            S,           ssharp,     guillemotleft ] }; // s S ß «

key <AC04>    { [            f,            F,       apostrophe,        apostrophe ] }; // f F ' '

key <AC05>    { [            g,            G,       apostrophe,               yen ] }; // g G ' ¥

key <AC09>    { [            l,            L,   periodcentered,    periodcentered ] }; // l L · ·

key <BKSL>    { [     asterisk,           mu,       dead_grave,   dead_circumflex ] }; // * µ ` ^

  

// Fourth row

key <LSGT>  { [         less,      greater,             less,           greater ] }; // < > < >

key <AB01>  { [            w,            W,    guillemotleft,     guillemotleft ] }; // w W « «

key <AB02>  { [            x,            X,   guillemotright,    guillemotright ] }; // x X » »

key <AB04>  { [            v,            V,     nobreakspace,              less ] }; // v V ⍽ < (espace insécable)

key <AB05>  { [            b,            B,            minus,       asciicircum ] }; // b B - ^

key <AB06>  { [            n,            N,          notsign,           greater ] }; // n N ¬ >

key <AB07>  { [        comma,     question,     questiondown,            period ] }; // , ? ¿ .

key <AB08>  { [    semicolon,       period,         multiply,    periodcentered ] }; // ; . × ·

key <AB09>  { [        colon,        slash,         division,             slash ] }; // : / ÷ /

key <AB10>  { [       exclam,      section,       exclamdown,             minus ] }; // ! § ¡ -

};

  

partial alphanumeric_keys

xkb_symbols "oss_Sundeadkeys" {

  

// Modifies the basic fr(oss) layout to use the Sun dead keys

  

include "fr(oss)"

  

key <TLDE>    { [  twosuperior, threesuperior,      onesuperior,      dead_cedilla ] }; // ¹ ² ³ ¸

  

key <AD11>    { [  dead_circumflex,   dead_diaeresis,       dead_tilde,    dead_abovering ] }; // ^ ̈ ̃ ˚

  

key <AC11>    { [       ugrave,      percent,       dead_acute,            Ugrave ] }; // ù % ' Ù

key <BKSL>    { [     asterisk,           mu,       dead_grave,       dead_macron ] }; // * µ ` ̄

};

  

partial alphanumeric_keys

xkb_symbols "oss_sundeadkeys" {

  

include "fr(oss_Sundeadkeys)"

  

name[Group1]="French (alt., with Sun dead keys)";

};

  

partial alphanumeric_keys

xkb_symbols "oss_nodeadkeys" {

  

// Modifies the basic fr(oss) layout to eliminate all dead keys

  

include "fr(oss)"

  

name[Group1]="French (alt., no dead keys)";

  

key <TLDE>    { [  twosuperior, threesuperior,      onesuperior,           cedilla ] }; // ² ³ ¹ ¸

key <AE01>    { [    ampersand,            1,            caron,            ogonek ] }; // & 1 ˇ ̨

key <AE03>    { [     quotedbl,            3,       numbersign,             breve ] }; // " 3 # ˘

  

key <AD11>    { [  asciicircum,    diaeresis,       asciitilde,             Aring ] }; // ^ ̈ ̃ Å

key <AC11>    { [       ugrave,      percent,            acute,            Ugrave ] }; // ù % ' Ù

key <BKSL>    { [     asterisk,           mu,            grave,            macron ] }; // * µ ` ̄

};

  
  

// Historic Linux French keyboard layout (fr-latin9)

// Copyright (c) 199x, 2002 Rene Cougnenc (original work)

//                      Guylhem Aznar <clavier @ externe.net> (maintainer)

//                      Nicolas Mailhot <Nicolas.Mailhot @ laposte.net>

//                          (XFree86 submission)

//

// This layout has long been distributed and refined outside official channels.

// To this day it remains more feature-rich and popular than the 'fr' layout.

//

// This layout is derived from an original version by Guylhem Aznar.

// The original version is always available from:

// http://en.tldp.org/HOWTO/Francophones-HOWTO.html

// and is distributed under a GPL license.

//

// The author has given permission for this derived version to be distributed

// under the standard XFree86 license. He would like all changes to this

// version to be sent to him at <clavier @ externe.net>, so he can sync

// the identically named linux console map (kbd, linux-console) and his

// out-of-tree GPL version.

//

// Now follows the keyboard design description in French.

// (If you can't read it you probably have no business changing this file anyway:)

//

// Les accents circonflexes des principales voyelles sont obtenus avec

// la touche Alt_Gr, les trémas sont obtenus par Alt_Gr + Shift.

//

//  ____                                 _________ _____________ _______

// | S A| S = Shift,  A = AltGr + Shift | Imprime | Arrêt défil | Pause |

// | s a| s = normal, a = AltGr         |  Exec   |         | Halte |

//  ¯¯¯¯                                 ¯¯¯¯¯¯¯¯¯ ¯¯¯¯¯¯¯¯¯¯¯¯¯ ¯¯¯¯¯¯¯

//  ____ ____ ____ ____ ____ ____ ____ ____ ____ ____ ____ ____ ____ _______

// | œ "| 1 ·| 2 É| 3 ,| 4 '| 5 "| 6 || 7 È| 8 ¯| 9 Ç| 0 À| ° ÿ| + °| <--   |

// | Œ "| & '| é ~| " #| ' {| ( [| - || è `| _ \| ç ^| à @| ) ]| = }|   |

//  ========================================================================

// | |<-  | A ä| Z Å| E ¢| R Ç| T Þ| Y Ý| U ü| I ï| O ö| P '| " `| $ ë|   , |

// |  ->| | a â| z å| e €| r ç| t þ| y ý| u û| i î| o ô| p ¶| ^ ~| £ ê| <-' |

//  ===================================================================¬ |

// |   | Q Ä| S Ø| D Ë| F ª| G Æ| H Ð| J Ü| K Ï| L Ö| M º| % Ù| µ ¥| |

// | MAJ   | q Â| s ø| d Ê| f ±| g æ| h ð| j Û| k Î| l Ô| m ¹| ù ²| * ³| |

//  ========================================================================

// | ^   | >  | W  | X  | C  | V  | B  | N  | ?  | .  | /  | §  | ^ |

// | |   | < || w «| x »| c ©| v ®| b ß| n ¬| , ¿| ; ×| : ÷| ! ¡| | |

//  ========================================================================

// |  |  |  |                   |   |  | |  |

// | Ctrl | Super| Alt  | Space Nobreakspace | AltGr | Super|Menu | Ctrl |

//  ¯¯¯¯¯¯ ¯¯¯¯¯¯ ¯¯¯¯¯¯ ¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯ ¯¯¯¯¯¯¯ ¯¯¯¯¯¯ ¯¯¯¯¯ ¯¯¯¯¯¯

//

//

//   Si les touches mortes fonctionnent, utiliser les accents dits

//   « morts », i.e. fonctionnant comme l'accent circonflexe & le

//   tréma des machines à écrire ; sont disponibles :

//

// (^) : accent circonflexe,

// Shift+(^) : tréma,

// Shift+AltGr+(^) : tilde,

// AltGr+(1) : accent aigu,

// AltGr+(7) : accent grave

//

// Pour s'en servir, procéder comme avec l'accent circonflexe & le tréma

// sur les vielles machines à écrire :

//

// AltGr+(1) puis e : é

// AltGr+(1) puis E : É

//

partial alphanumeric_keys

  

xkb_symbols "latin9" {

  

include "latin"

include "nbsp(level3)"

  

name[Group1]="French (legacy, alt.)";

  

key <TLDE>    { [          oe,          OE, leftdoublequotemark, rightdoublequotemark ] };

key <AE01>    { [   ampersand,           1,      dead_acute,   periodcentered ] };

key <AE02>    { [      eacute,           2,      asciitilde,           Eacute ] };

key <AE03>    { [    quotedbl,           3,      numbersign,          cedilla ] };

key <AE04>    { [  apostrophe,           4,       braceleft,            acute ] };

key <AE05>    { [   parenleft,           5,     bracketleft,        diaeresis ] };

key <AE06>    { [       minus,           6,             bar,        brokenbar ] };

key <AE07>    { [      egrave,           7,      dead_grave,           Egrave ] };

key <AE08>    { [  underscore,           8,       backslash,           macron ] };

key <AE09>    { [    ccedilla,           9,     asciicircum,         Ccedilla ] };

key <AE10>    { [      agrave,           0,              at,           Agrave ] };

key <AE11>    { [  parenright,      degree,    bracketright,       ydiaeresis ] };

key <AE12>    { [       equal,        plus,      braceright,   dead_abovering ] };

  

key <AD01>    { [           a,           A,     acircumflex,       adiaeresis ] };

key <AD02>    { [           z,           Z,           aring,            Aring ] };

key <AD03>    { [           e,           E,        EuroSign,             cent ] };

key <AD04>    { [           r,           R,        ccedilla,         Ccedilla ] };

key <AD05>    { [           t,           T,           thorn,            THORN ] };

key <AD06>    { [           y,           Y,          yacute,           Yacute ] };

key <AD07>    { [           u,           U,     ucircumflex,       udiaeresis ] };

key <AD08>    { [           i,           I,     icircumflex,       idiaeresis ] };

key <AD09>    { [           o,           O,     ocircumflex,       odiaeresis ] };

key <AD10>    { [           p,           P,       paragraph,            grave ] };

key <AD11>    { [ dead_circumflex,  dead_diaeresis,      dead_tilde,       apostrophe ] };

key <AD12>    { [      dollar,    sterling,     ecircumflex,       ediaeresis ] };

  

key <AC01>    { [           q,           Q,     Acircumflex,       Adiaeresis ] };

key <AC02>    { [           s,           S,          oslash,         Ooblique ] };

key <AC03>    { [           d,           D,     Ecircumflex,       Ediaeresis ] };

key <AC04>    { [           f,           F,       plusminus,      ordfeminine ] };

key <AC05>    { [           g,           G,              ae,               AE ] };

key <AC06>    { [           h,           H,             eth,              ETH ] };

key <AC07>    { [           j,           J,     Ucircumflex,       Udiaeresis ] };

key <AC08>    { [           k,           K,     Icircumflex,       Idiaeresis ] };

key <AC09>    { [           l,           L,     Ocircumflex,       Odiaeresis ] };

key <AC10>    { [           m,           M,     onesuperior,        masculine ] };

key <AC11>    { [      ugrave,     percent,     twosuperior,           Ugrave ] };

key <BKSL>  { [    asterisk,          mu,   threesuperior,              yen ] };

  

key <LSGT>    { [        less,     greater,             bar                   ] };

key <AB01>    { [           w,           W,   guillemotleft       ] };

key <AB02>    { [           x,           X,  guillemotright                   ] };

key <AB03>    { [           c,           C,       copyright                   ] };

key <AB04>    { [           v,           V,      registered       ] };

key <AB05>    { [           b,           B,          ssharp,            U1E9E ] };

key <AB06>    { [           n,           N,         notsign                   ] };

key <AB07>    { [       comma,    question,    questiondown                   ] };

key <AB08>    { [   semicolon,      period,        multiply       ] };

key <AB09>    { [       colon,       slash,        division                   ] };

key <AB10>    { [      exclam,     section,      exclamdown                   ] };

  

// French uses a comma as decimal separator, but keyboards are labeled with a period

// Will take effect when KP_Decimal is mapped to the locale decimal separator

key <KPDL>  { [   KP_Delete,  KP_Decimal,       KP_Delete,       KP_Decimal ] };

  

include "level3(ralt_switch)"

};

  

partial alphanumeric_keys

xkb_symbols "latin9_Sundeadkeys" {

  

// Modifies the basic fr-latin9 layout to use the Sun dead keys

  

include "fr(latin9)"

  

key <AE01>    { [   ampersand,           1,     dead_acute,   periodcentered ] };

key <AE07>    { [      egrave,           7,     dead_grave,           Egrave ] };

key <AD11>    { [ dead_circumflex,  dead_diaeresis,     dead_tilde,       apostrophe ] };

};

  

partial alphanumeric_keys

xkb_symbols "latin9_sundeadkeys" {

  

include "fr(latin9_Sundeadkeys)"

  

name[Group1]="French (legacy, alt., with Sun dead keys)";

};

  

partial alphanumeric_keys

xkb_symbols "latin9_nodeadkeys" {

  

// Modifies the basic fr-latin9 layout to eliminate all dead keys

  

include "fr(latin9)"

  

name[Group1]="French (legacy, alt., no dead keys)";

  

key <AE01>    { [   ampersand,           1,      apostrophe,   periodcentered ] };

key <AE07>    { [      egrave,           7,           grave,           Egrave ] };

key <AE12>    { [       equal,        plus,      braceright        ] };

key <AD11>    { [    asciicircum, diaeresis,      asciitilde,       apostrophe ] };

};

  

// Bépo : Improved ergonomic french keymap using Dvorak method.

// Built by community on 'Dvorak Fr / Bépo' :

// see http://www.clavier-dvorak.org/wiki/ to join and help.

// XOrg integration (1.0rc2 version) in 2008

// by Frédéric Boiteux <fboiteux at free dot fr>

//

// Bépo layout (1.0rc2 version) for a pc105 keyboard (french) :

// ┌─────┐

// │ S A │   S = Shift,  A = AltGr + Shift

// │ s a │   s = normal, a = AltGr

// └─────┘

//

// ┌─────┬─────┬─────┬─────┬─────┬─────┬─────┬─────┬─────┬─────┬─────┬─────┬─────┲━━━━━━━━━┓

// │ # ¶ │ 1 „ │ 2 “ │ 3 ” │ 4 ≤ │ 5 ≥ │ 6   │ 7 ¬ │ 8 ¼ │ 9 ½ │ 0 ¾ │ ° ′ │ ` ″ ┃ ⌫ Retour┃

// │ $ – │ " — │ « < │ » > │ ( [ │ ) ] │ @ ^ │ + ± │ - − │ / ÷ │ * × │ = ≠ │ % ‰ ┃  arrière┃

// ┢━━━━━┷━┱───┴─┬───┴─┬───┴─┬───┴─┬───┴─┬───┴─┬───┴─┬───┴─┬───┴─┬───┴─┬───┴─┬───┺━┳━━━━━━━┫

// ┃   ┃ B ¦ │ É ˝ │ P § │ O Œ │ È ` │ !   │ V   │ D Ð │ L   │ J Ĳ │ Z Ə │ W   ┃Entrée ┃

// ┃Tab ↹  ┃ b | │ é ˊ │ p & │ o œ │ è ` │ ˆ ¡ │ v ˇ │ d ð │ l / │ j ĳ │ z ə │ w ̆  ┃   ⏎   ┃

// ┣━━━━━━━┻┱────┴┬────┴┬────┴┬────┴┬────┴┬────┴┬────┴┬────┴┬────┴┬────┴┬────┴┬────┺┓  ┃

// ┃    ┃ A Æ │ U Ù │ I ˙ │ E ¤ │ ; ̛  │ C ſ │ T Þ │ S ẞ │ R ™ │ N   │ M º │ Ç , ┃  ┃

// ┃Maj ⇬   ┃ a æ │ u ù │ i ̈  │ e € │ , ’ │ c © │ t þ │ s ß │ r ® │ n ˜ │ m ¯ │ ç ¸ ┃  ┃

// ┣━━━━━━━┳┹────┬┴────┬┴────┬┴────┬┴────┬┴────┬┴────┬┴────┬┴────┬┴────┬┴────┲┷━━━━━┻━━━━━━┫

// ┃   ┃ Ê   │ À   │ Y ‘ │ X ’ │ : · │ K   │ ? ̉  │ Q ̣  │ G   │ H ‡ │ F ª ┃         ┃

// ┃Shift ⇧┃ ê / │ à \ │ y { │ x } │ . … │ k ~ │ ' ¿ │ q ˚ │ g µ │ h † │ f ˛ ┃Shift ⇧  ┃

// ┣━━━━━━━╋━━━━━┷━┳━━━┷━━━┱─┴─────┴─────┴─────┴─────┴─────┴───┲━┷━━━━━╈━━━━━┻━┳━━━━━━━┳━━━┛

// ┃   ┃   ┃   ┃ Espace inséc.   Espace inséc. fin ┃   ┃   ┃   ┃

// ┃Ctrl   ┃Meta   ┃Alt ┃ ␣ (Espace)  _           ␣ ┃AltGr ⇮┃Menu   ┃Ctrl   ┃

// ┗━━━━━━━┻━━━━━━━┻━━━━━━━┹───────────────────────────────────┺━━━━━━━┻━━━━━━━┻━━━━━━━┛

partial alphanumeric_keys

xkb_symbols "bepo" {

  

include "level3(ralt_switch)"

include "keypad(oss)"

  

name[Group1]= "French (Bepo, ergonomic, Dvorak way)";

  

// First row

key <TLDE> { [      dollar,   numbersign,    endash,   paragraph ] }; // $ # – ¶

key <AE01> { type[group1] = "FOUR_LEVEL_SEMIALPHABETIC", [    quotedbl,        1,     emdash, doublelowquotemark ] }; // " 1 — „

key <AE02> { type[group1] = "FOUR_LEVEL_SEMIALPHABETIC", [   guillemotleft,        2,       less,  leftdoublequotemark ] }; // « 2 < “

key <AE03> { type[group1] = "FOUR_LEVEL_SEMIALPHABETIC", [  guillemotright,        3,    greater, rightdoublequotemark ] }; // » 3 > ”

key <AE04> { type[group1] = "FOUR_LEVEL_SEMIALPHABETIC", [   parenleft,        4, bracketleft,  lessthanequal ] }; // ( 4 [ ≤

key <AE05> { type[group1] = "FOUR_LEVEL_SEMIALPHABETIC", [  parenright,        5,   bracketright,   greaterthanequal ] }; // ) 5 ] ≥

key <AE06> { type[group1] = "FOUR_LEVEL_SEMIALPHABETIC", [          at,        6, asciicircum             ] }; // @ 6 ^

key <AE07> { type[group1] = "FOUR_LEVEL_SEMIALPHABETIC", [        plus,        7,  plusminus,    notsign ] }; // + 7 ± ¬

key <AE08> { type[group1] = "FOUR_LEVEL_SEMIALPHABETIC", [       minus,        8,      U2212, onequarter ] }; // - 8 − ¼

key <AE09> { type[group1] = "FOUR_LEVEL_SEMIALPHABETIC", [       slash,        9,   division,    onehalf ] }; // / 9 ÷ ½

key <AE10> { type[group1] = "FOUR_LEVEL_SEMIALPHABETIC", [    asterisk,        0,   multiply,  threequarters ] }; // * 0 × ¾

key <AE11> { [       equal,   degree,   notequal,    minutes ] }; // = ° ≠ ′

key <AE12> { [     percent,    grave,   permille,    seconds ] }; // % ` ‰ ″

  

// Second row

key <AD01> { [           b,        B,        bar,  brokenbar ] }; // b B | ¦

key <AD02> { [      eacute,   Eacute, dead_acute, dead_doubleacute ] }; // é É ˊ ˝

key <AD03> { [           p,        P,  ampersand,    section ] }; // p P & §

key <AD04> { [           o,        O,         oe,         OE ] }; // o O œ Œ

key <AD05> { [      egrave,   Egrave, dead_grave,      grave ] }; // è È ` `

key <AD06> { [ dead_circumflex,   exclam, exclamdown             ] }; // ^ ! ¡

key <AD07> { [           v,        V, dead_caron             ] }; // v V ˇ

key <AD08> { [           d,        D,        eth,        ETH ] }; // d D ð Ð

key <AD09> { [           l,        L, dead_stroke             ] }; // l L /

key <AD10> { [           j,        J,      U0133,      U0132 ] }; // j J ĳ Ĳ

key <AD11> { [           z,        Z,      schwa,      SCHWA ] }; // z Z ə Ə

key <AD12> { [           w,        W, dead_breve             ] }; // w W ̆

  

// Third row

key <AC01> { [           a,        A,         ae,         AE ] }; // a A æ Æ

key <AC02> { [           u,        U,     ugrave,     Ugrave ] }; // u U ù Ù

key <AC03> { [           i,        I, dead_diaeresis,  dead_abovedot ] }; // i I ̈ ˙

key <AC04> { [           e,        E,   EuroSign,  dead_currency ] }; // e E € ¤

key <AC05> { [       comma, semicolon, rightsinglequotemark, dead_horn ] }; // , ; ’ ̛

key <AC06> { [           c,        C,  copyright,      U017F ] }; // c C © ſ

key <AC07> { [           t,        T,      thorn,      THORN ] }; // t T þ Þ

key <AC08> { [           s,        S,     ssharp,      U1E9E ] }; // s S ß ẞ

key <AC09> { [           r,        R, registered,  trademark ] }; // r R ® ™

key <AC10> { [           n,        N, dead_tilde             ] }; // n N ~

key <AC11> { [           m,        M, dead_macron,  masculine ] }; // m M ̄ º

key <BKSL> { [    ccedilla, Ccedilla,   dead_cedilla, dead_belowcomma ] }; // ç Ç ¸ ,

  

// Fourth row

key <LSGT> { [ ecircumflex,  Ecircumflex,      slash             ] }; // ê Ê /

key <AB01> { [      agrave,   Agrave,  backslash             ] }; // à À \

key <AB02> { [           y,        Y,  braceleft, leftsinglequotemark  ] }; // y Y { ‘

key <AB03> { [           x,        X, braceright, rightsinglequotemark ] }; // x X } ’

key <AB04> { [      period,    colon,   ellipsis, periodcentered ] }; // . : … ·

key <AB05> { [           k,        K, asciitilde             ] }; // k K ~

key <AB06> { [  apostrophe, question,   questiondown,  dead_hook ] }; // ' ? ¿ ̉

key <AB07> { [           q,        Q, dead_abovering,  dead_belowdot ] }; // q Q ˚ ̣

key <AB08> { [           g,        G, dead_greek             ] }; // g G µ

key <AB09> { [           h,        H,     dagger,   doubledagger ] }; // h H † ‡

key <AB10> { [           f,        F, dead_ogonek, ordfeminine ] }; // f F ̨ ª

  

key <SPCE> { [       space, nobreakspace, underscore,      U202F ] }; // ␣ (espace insécable) _ (espace insécable fin)

};

  

partial alphanumeric_keys

xkb_symbols "bepo_latin9" {

  

// Restricts the fr(bepo) layout to latin9 symbols

  

include "fr(bepo)"

include "keypad(oss_latin9)"

  

name[Group1]="French (Bepo, ergonomic, Dvorak way, Latin-9 only)";

  

key <TLDE> { [      dollar,   numbersign,    dollar,   paragraph ] }; // $ # $ ¶

  

key <AE01> { type[group1] = "FOUR_LEVEL_SEMIALPHABETIC", [    quotedbl,        1                             ] }; // " 1

key <AE02> { type[group1] = "FOUR_LEVEL_SEMIALPHABETIC", [   guillemotleft,        2,       less             ] }; // « 2 <

key <AE03> { type[group1] = "FOUR_LEVEL_SEMIALPHABETIC", [  guillemotright,        3,    greater             ] }; // » 3 >

key <AE04> { type[group1] = "FOUR_LEVEL_SEMIALPHABETIC", [   parenleft,        4, bracketleft             ] }; // ( 4 [

key <AE05> { type[group1] = "FOUR_LEVEL_SEMIALPHABETIC", [  parenright,        5,   bracketright             ] }; // ) 5 ]

key <AE08> { type[group1] = "FOUR_LEVEL_SEMIALPHABETIC", [       minus,        8,      minus, onequarter ] }; // - 8 - ¼

key <AE11> { [       equal,   degree                             ] }; // = °

key <AE12> { [     percent,    grave                             ] }; // % `

  

key <AD01> { [           b,        B,        bar             ] }; // b B |

key <AD02> { [      eacute,   Eacute, dead_acute             ] }; // é É ˊ

key <AD10> { [           j,        J                             ] }; // j J

key <AD11> { [           z,        Z                             ] }; // z Z

key <AD12> { [           w,        W                             ] }; // w W

  

key <AC03> { [           i,        I, dead_diaeresis             ] }; // i I ̈

key <AC05> { [       comma, semicolon,      comma,  dead_horn ] }; // , ; , ̛

key <AC06> { [           c,        C,  copyright             ] }; // c C ©

key <AC08> { [           s,        S,     ssharp,      U1E9E ] }; // s S ß ẞ

key <AC09> { [           r,        R, registered             ] }; // r R ®

key <AC11> { [           m,        M,     macron,  masculine ] }; // m M ̄ º

  

key <AB02> { [           y,        Y,  braceleft             ] }; // y Y {

key <AB03> { [           x,        X, braceright             ] }; // x X }

key <AB04> { [      period,    colon                             ] }; // . :

key <AB09> { [           h,        H                             ] }; // h H

key <AB10> { [           f,        F,          f, ordfeminine ] }; // f F   ª

  

// Note : on a besoin de redéfinir les niveaux 3 et 4,

// donc nbsp(level2) ne suffit pas !

key <SPCE> { [       space,  nobreakspace, underscore,   nobreakspace ] }; // ␣ (espace insécable) _ (espace insécable)

};

  

// Version 1.1rc2 of the Bépo keyboard layout,

// normalized by the AFNOR NF Z71‐300 norm.

//

// Layout: https://bepo.fr/wiki/Version_1.1rc2

// Normalization: https://normalisation.afnor.org/actualites/faq-clavier-francais/

//

// ┌────┬────┬────┬────┬────┬────┬────┬────┬────┬────┬────┬────┬────╔═════════╗

// │ # ¶│ 1 „│ 2 “│ 3 ”│ 4 ⩽│ 5 ⩾║ 6  │ 7 ¬│ 8 ¼│ 9 ½│ 0 ¾│ ° ′│ ` ″║     ║

// │ $ –│ " —│ « <│ » >│ ( [│ ) ]║ @ ^│ + ±│ - −│ / ÷│ * ×│ = ≠│ % ‰║ <-- ║

// ╔════╧══╗─┴──┬─┴──┬─┴──┬─┴──┬─┴──┬─┴──┬─┴──┬─┴──┬─┴──┬─┴──┬─┴──┬─╚══╦══════╣

// ║  |<-  ║ B _│ É  │ P §│ O Œ│ È `║ !  │ V  │ D  │ L £│ J  │ Z  │ W  ║   |  ║

// ║  ->|  ║ b |│ é ´│ p &│ o œ│ è `║ ˆ ¡│ v ˇ│ d ∞│ l /│ j  │ z ―│ w  ║ <-'  ║

// ╠═══════╩╗───┴┬───┴┬───┴┬───┴┬───┴┬───┴┬───┴┬───┴┬───┴┬───┴┬───┴┬───╚╗ ║

// ║    ║ A Æ│ U Ù│ I ˙│ E ¤│ ; ,║ C ©│ T ™│ S ſ│ R ®│ N  │ M  │ Ç ©║ ║

// ║  CAPS  ║ a æ│ u ù│ i ¨│ e €│ , '║ c ¸│ t ᵉ│ s ß│ r ˘│ n ~│ m ¯│ ç  ║ ║

// ╠══════╦═╝──┬─┴──┬─┴──┬─┴─══─┴──┬─┴──┬─┴─══─┴──┬─┴──┬─┴──┬─┴──╔═╧════╩═════╣

// ║   ^  ║ Ê ^│ À ‚│ Y ‘│ X ’│ : ·│ K ‑║ ? ̉ │ Q ̛│ G †│ H ‡│ F  ║ ^  ║

// ║   |  ║ ê /│ à \│ y {│ x }│ . …│ k ~║ ’ ¿│ q °│ g µ│ h ̣ │ f ˛║ |  ║

// ╠══════╩╦═══╧══╦═╧═══╦╧════╧════╧════╧════╧════╧═╦══╧══╦═╧════╬═════╦══════╣

// ║   ║  ║ ║ Fine insécable  Insécable ║ ║  ║ ║  ║

// ║ Ctrl  ║ WinG ║ Alt ║ Espace              _ ║AltGr║ WinD ║WinM ║ Ctrl ║

// ╚═══════╩══════╩═════╩═══════════════════════════╩═════╩══════╩═════╩══════╝

partial alphanumeric_keys

xkb_symbols "bepo_afnor" {

  

    name[Group1]= "French (Bepo, ergonomic, Dvorak way, AFNOR)";

  

    include "pc(pc105)"

  

    key <TLDE> { type[group1] = "FOUR_LEVEL", [ dollar, numbersign, endash, paragraph ] }; // $ # – ¶

    key <AE01> { type[group1] = "FOUR_LEVEL_SEMIALPHABETIC", [ quotedbl, 1, emdash, doublelowquotemark ] }; // " 1 — „

    key <AE02> { type[group1] = "FOUR_LEVEL_SEMIALPHABETIC", [ guillemotleft, 2, less, leftdoublequotemark ] }; // « 2 < “

    key <AE03> { type[group1] = "FOUR_LEVEL_SEMIALPHABETIC", [ guillemotright, 3, greater, rightdoublequotemark ] }; // » 3 > ”

    key <AE04> { type[group1] = "FOUR_LEVEL_SEMIALPHABETIC", [ parenleft, 4, bracketleft, U2A7D ] }; // ( 4 [ ⩽

    key <AE05> { type[group1] = "FOUR_LEVEL_SEMIALPHABETIC", [ parenright, 5, bracketright, U2A7E ] }; // ) 5 ] ⩾

    key <AE06> { type[group1] = "FOUR_LEVEL_SEMIALPHABETIC", [ at, 6, asciicircum, U262D ] }; // @ 6 ^ ☭

    key <AE07> { type[group1] = "FOUR_LEVEL_SEMIALPHABETIC", [ plus, 7, plusminus, notsign ] }; // + 7 ± ¬

    key <AE08> { type[group1] = "FOUR_LEVEL_SEMIALPHABETIC", [ minus, 8, U2212, onequarter ] }; // - 8 − ¼

    key <AE09> { type[group1] = "FOUR_LEVEL_SEMIALPHABETIC", [ slash, 9, division, onehalf ] }; // / 9 ÷ ½

    key <AE10> { type[group1] = "FOUR_LEVEL_SEMIALPHABETIC", [ asterisk, 0, multiply, threequarters ] }; // * 0 × ¾

    key <AE11> { type[group1] = "FOUR_LEVEL", [ equal, degree, notequal, minutes ] }; // = ° ≠ ′

    key <AE12> { type[group1] = "FOUR_LEVEL", [ percent, grave, U2030, seconds ] }; // % ` ‰ ″

  

    key <AD01> { type[group1] = "FOUR_LEVEL_SEMIALPHABETIC", [ b, B, bar, underscore ] }; // b B | _

    key <AD02> { type[group1] = "FOUR_LEVEL_SEMIALPHABETIC", [ eacute, Eacute, dead_acute, heart ] }; // é É ´ ♥

    key <AD03> { type[group1] = "FOUR_LEVEL_SEMIALPHABETIC", [ p, P, ampersand, section ] }; // p P & §

    key <AD04> { type[group1] = "FOUR_LEVEL_ALPHABETIC", [ o, O, oe, OE ] }; // o O œ Œ

    key <AD05> { type[group1] = "FOUR_LEVEL_SEMIALPHABETIC", [ egrave, Egrave, dead_grave, grave ] }; // è È ` `

    key <AD06> { type[group1] = "FOUR_LEVEL", [ dead_circumflex, exclam, exclamdown, U2620 ] }; // ^ ! ¡ ☠

    key <AD07> { type[group1] = "FOUR_LEVEL_SEMIALPHABETIC", [ v, V, dead_caron, U2622 ] }; // v V ˇ ☢

    key <AD08> { type[group1] = "FOUR_LEVEL_SEMIALPHABETIC", [ d, D, UFDD7, U2623 ] }; // d D ∞ ☣

    key <AD09> { type[group1] = "FOUR_LEVEL_SEMIALPHABETIC", [ l, L, dead_stroke, sterling ] }; // l L / £

    key <AD10> { type[group1] = "FOUR_LEVEL_SEMIALPHABETIC", [ j, J, U262E, U262F ] }; // j J ☮ ☯

    key <AD11> { type[group1] = "FOUR_LEVEL_SEMIALPHABETIC", [ z, Z, UFDD8, U2619 ] }; // z Z ― ☙

    key <AD12> { type[group1] = "FOUR_LEVEL_SEMIALPHABETIC", [ w, W, U269C, U267F ] }; // w W ⚜ ♿

  

    key <AC01> { type[group1] = "FOUR_LEVEL_ALPHABETIC", [ a, A, ae, AE ] }; // a A æ Æ

    key <AC02> { type[group1] = "FOUR_LEVEL_ALPHABETIC", [ u, U, ugrave, Ugrave ] }; // u U ù Ù

    key <AC03> { type[group1] = "FOUR_LEVEL_SEMIALPHABETIC", [ i, I, dead_diaeresis, dead_abovedot ] }; // i I ¨ ˙

    key <AC04> { type[group1] = "FOUR_LEVEL_SEMIALPHABETIC", [ e, E, EuroSign, dead_currency ] }; // e E € ¤

    key <AC05> { type[group1] = "FOUR_LEVEL", [ comma, semicolon, apostrophe, dead_belowcomma ] }; // , ; ' ,

    key <AC06> { type[group1] = "FOUR_LEVEL_SEMIALPHABETIC", [ c, C, dead_cedilla, copyright ] }; // c C ¸ ©

    key <AC07> { type[group1] = "FOUR_LEVEL_SEMIALPHABETIC", [ t, T, UFDD5, trademark ] }; // t T ᵉ ™

    key <AC08> { type[group1] = "FOUR_LEVEL_SEMIALPHABETIC", [ s, S, UFDD4, U017F ] }; // s S ß ſ

    key <AC09> { type[group1] = "FOUR_LEVEL_SEMIALPHABETIC", [ r, R, dead_breve, registered ] }; // r R ˘ ®

    key <AC10> { type[group1] = "FOUR_LEVEL_SEMIALPHABETIC", [ n, N, dead_tilde, U2693 ] }; // n N ~ ⚓

    key <AC11> { type[group1] = "FOUR_LEVEL_SEMIALPHABETIC", [ m, M, dead_macron, U26FD ] }; // m M ¯ ⛽

    key <BKSL> { type[group1] = "FOUR_LEVEL_SEMIALPHABETIC", [ ccedilla, Ccedilla, U2708, U1F12F ] }; // ç Ç ✈ 🄯

  

    key <LSGT> { type[group1] = "FOUR_LEVEL_SEMIALPHABETIC", [ ecircumflex, Ecircumflex, slash, asciicircum ] }; // ê Ê / ^

    key <AB01> { type[group1] = "FOUR_LEVEL_SEMIALPHABETIC", [ agrave, Agrave, backslash, singlelowquotemark ] }; // à À \ ‚

    key <AB02> { type[group1] = "FOUR_LEVEL_SEMIALPHABETIC", [ y, Y, braceleft, leftsinglequotemark ] }; // y Y { ‘

    key <AB03> { type[group1] = "FOUR_LEVEL_SEMIALPHABETIC", [ x, X, braceright, rightsinglequotemark ] }; // x X } ’

    key <AB04> { type[group1] = "FOUR_LEVEL", [ period, colon, ellipsis, periodcentered ] }; // . : … ·

    key <AB05> { type[group1] = "FOUR_LEVEL_SEMIALPHABETIC", [ k, K, asciitilde, U2011 ] }; // k K ~ ‑

    key <AB06> { type[group1] = "FOUR_LEVEL", [ rightsinglequotemark, question, questiondown, dead_hook ] }; // ’ ? ¿ ̉

    key <AB07> { type[group1] = "FOUR_LEVEL_SEMIALPHABETIC", [ q, Q, dead_abovering, dead_horn ] }; // q Q ˚ ̛

    key <AB08> { type[group1] = "FOUR_LEVEL_SEMIALPHABETIC", [ g, G, dead_greek, dagger ] }; // g G µ †

    key <AB09> { type[group1] = "FOUR_LEVEL_SEMIALPHABETIC", [ h, H, dead_belowdot, doubledagger ] }; // h H ̣ ‡

    key <AB10> { type[group1] = "FOUR_LEVEL_SEMIALPHABETIC", [ f, F, dead_ogonek, U26C4 ] }; // f F ˛ ⛄

    key <SPCE> { type[group1] = "FOUR_LEVEL", [ space, U202F, underscore, nobreakspace ] }; //     _  

  
  

    include "level3(ralt_switch)"

};

  

// Author   : Francis Leboutte, http://www.algo.be/ergo/dvorak-fr.html

//        thanks to Fabien Cazenave for his help

// Licence  : X11

// Version  : 0.3

  

// Base layer + dead AltGr key (`):

// ┌─────┬─────┬─────┬─────┬─────┬─────┬─────┬─────┬─────┬─────┬─────┬─────┬─────┲━━━━━━━━━━┓

// │ *   │ 1   │ 2   │ 3   │ 4   │ 5   │ 6   │ 7   │ 8   │ 9   │ 0   │ +   │ %   ┃      ┃

// │ _   │ =   │ / ± │ - ¼ │ è ½ │ \ ¾ │ ^   │ (   │ ` ` │ )   │ "   │ [   │ ]   ┃ ⌫    ┃

// ┢━━━━━┷━━┱──┴──┬──┴──┬──┴──┬──┴──┬──┴──┬──┴──┬──┴──┬──┴──┬──┴──┬──┴──┬──┴──┬──┺━━┳━━━━━━━┫

// ┃    ┃ ? Æ │ <   │ >   │ G   │ !   │ H   │ V   │ C Ç │ M   │ K   │ Z   │ &   ┃   ┃

// ┃ ↹  ┃ : æ │ ' $ │ é É │ g € │ . ° │ h   │ v   │ c ç │ m µ │ k   │ z   │ ¨   ┃   ┃

// ┣━━━━━━━━┻┱────┴┬────┴┬────┴┬────┴┬────┴┬────┴┬────┴┬────┴┬────┴┬────┴┬────┴┬────┺┓  ⏎   ┃

// ┃     ┃ O Ò │ A À │ U Ù │ E È │ B   │ F   │ S   │ T   │ N   │ D   │ W   │ #   ┃  ┃

// ┃ ⇬   ┃ o ò │ a à │ u ù │ e è │ b   │ f   │ s « │ t   │ n » │ d   │ w   │ ~   ┃  ┃

// ┣━━━━━━┳━━┹──┬──┴──┬──┴──┬──┴──┬──┴──┬──┴──┬──┴──┬──┴──┬──┴──┬──┴──┬──┴──┲━━┷━━━━━┻━━━━━━┫

// ┃  ┃ ç Ç │ | Œ │ Q   │ @   │ I Ì │ Y   │ X   │ R   │ L   │ P   │ J   ┃           ┃

// ┃ ⇧ ┃ à À │ ; œ │ q { │ , } │ i ì │ y £ │ x   │ r º │ l   │ p § │ j   ┃ ⇧         ┃

// ┣━━━━━━┻┳━━━━┷━━┳━━┷━━━━┱┴─────┴─────┴─────┴─────┴─────┴─┲━━━┷━━━┳━┷━━━━━╋━━━━━━━┳━━━━━━━┫

// ┃   ┃   ┃   ┃ ␣                        ⍽ ┃   ┃   ┃   ┃   ┃

// ┃ ctrl  ┃ super ┃ alt   ┃ ␣ Espace Espace insécable ⍽ ┃ alt   ┃ super ┃ menu  ┃ ctrl  ┃

// ┗━━━━━━━┻━━━━━━━┻━━━━━━━┹────────────────────────────────┺━━━━━━━┻━━━━━━━┻━━━━━━━┻━━━━━━━┛

  

// Notice the specific Caps_Lock layer:

// ┌─────┬─────┬─────┬─────┬─────┬─────┬─────┬─────┬─────┬─────┬─────┬─────┬─────┲━━━━━━━━━━┓

// │ *   │ 1   │ 2   │ 3   │ 4   │ 5   │ 6   │ 7   │ 8   │ 9   │ 0   │ +   │ %   ┃      ┃

// │ │ │ │ │ │ │ │ │ │ │ │ │ ┃ ⌫    ┃

// ┢━━━━━┷━━┱──┴──┬──┴──┬──┴──┬──┴──┬──┴──┬──┴──┬──┴──┬──┴──┬──┴──┬──┴──┬──┴──┬──┺━━┳━━━━━━━┫

// ┃    ┃ │ <   │ >   │ │ │ │ │ │ │ │ │ ┃   ┃

// ┃ ↹  ┃ │ │ │ │ │ │ │ │ │ │ │ ┃   ┃

// ┣━━━━━━━━┻┱────┴┬────┴┬────┴┬────┴┬────┴┬────┴┬────┴┬────┴┬────┴┬────┴┬────┴┬────┺┓  ⏎   ┃

// ┃     ┃ │ │ │ │ │ │ │ │ │ │ │ ┃  ┃

// ┃ ⇬   ┃ │ │ │ │ │ │ │ │ │ │ │ ┃  ┃

// ┣━━━━━━┳━━┹──┬──┴──┬──┴──┬──┴──┬──┴──┬──┴──┬──┴──┬──┴──┬──┴──┬──┴──┬──┴──┲━━┷━━━━━┻━━━━━━┫

// ┃  ┃ /   │ -   │ │ │ │ │ │ │ │ │ ┃           ┃

// ┃ ⇧ ┃ │ │ │ │ │ │ │ │ │ │ ┃ ⇧         ┃

// ┣━━━━━━┻┳━━━━┷━━┳━━┷━━━━┱┴─────┴─────┴─────┴─────┴─────┴─┲━━━┷━━━┳━┷━━━━━╋━━━━━━━┳━━━━━━━┫

// ┃   ┃   ┃   ┃ ␣                        ⍽ ┃   ┃   ┃   ┃   ┃

// ┃ ctrl  ┃ super ┃ alt   ┃ ␣ Espace Espace insécable ⍽ ┃ alt   ┃ super ┃ menu  ┃ ctrl  ┃

// ┗━━━━━━━┻━━━━━━━┻━━━━━━━┹────────────────────────────────┺━━━━━━━┻━━━━━━━┻━━━━━━━┻━━━━━━━┛

  

partial alphanumeric_keys modifier_keys

xkb_symbols "dvorak" {

  name[Group1]="French (Dvorak)";

  

  // First row

  key <TLDE> { type[group1] = "FOUR_LEVEL_SEMIALPHABETIC", [   underscore,   asterisk              ] };

  key <AE01> { type[group1] = "FOUR_LEVEL_SEMIALPHABETIC", [        equal,      1              ] };

  key <AE02> { type[group1] = "FOUR_LEVEL_SEMIALPHABETIC", [        slash,      2,   plusminus ] };

  key <AE03> { type[group1] = "FOUR_LEVEL_SEMIALPHABETIC", [        minus,      3,  onequarter ] };

  key <AE04> { type[group1] = "FOUR_LEVEL_SEMIALPHABETIC", [       egrave,      4,     onehalf ] };

  key <AE05> { type[group1] = "FOUR_LEVEL_SEMIALPHABETIC", [    backslash,      5,   threequarters ] };

  key <AE06> { type[group1] = "FOUR_LEVEL_SEMIALPHABETIC", [  dead_circumflex,      6              ] };

  key <AE07> { type[group1] = "FOUR_LEVEL_SEMIALPHABETIC", [    parenleft,      7              ] };

  key <AE08> { type[group1] = "FOUR_LEVEL_SEMIALPHABETIC", [ ISO_Level3_Latch,      8,       grave ] };

  key <AE09> { type[group1] = "FOUR_LEVEL_SEMIALPHABETIC", [   parenright,      9              ] };

  key <AE10> { type[group1] = "FOUR_LEVEL_SEMIALPHABETIC", [     quotedbl,      0              ] };

  key <AE11> { type[group1] = "FOUR_LEVEL_SEMIALPHABETIC", [  bracketleft,   plus              ] };

  key <AE12> { type[group1] = "FOUR_LEVEL_SEMIALPHABETIC", [ bracketright, percent              ] };

  

  // Second row

  key <AD01> { [        colon,     question,          ae,           AE ] };

  key <AD02> { type[group1] = "FOUR_LEVEL_SEMIALPHABETIC", [   apostrophe,   less,      dollar ] };

  key <AD03> { type[group1] = "FOUR_LEVEL_SEMIALPHABETIC", [       eacute, greater,      Eacute ] };

  key <AD04> { [            g,            G,    EuroSign               ] };

  key <AD05> { [       period,       exclam,      degree               ] };

  key <AD06> { [            h,            H                                ] };

  key <AD07> { [            v,            V                                ] };

  key <AD08> { [            c,            C,    ccedilla,     Ccedilla ] };

  key <AD09> { [            m,            M,          mu               ] };

  key <AD10> { [            k,            K                                ] };

  key <AD11> { [            z,            Z                                ] };

  key <AD12> { [   dead_diaeresis,    ampersand                                ] };

  

  // Third row

  key <AC01> { [            o,            O,      ograve,       Ograve ] };

  key <AC02> { [            a,            A,      agrave,       Agrave ] };

  key <AC03> { [            u,            U,      ugrave,       Ugrave ] };

  key <AC04> { [            e,            E,      egrave,       Egrave ] };

  key <AC05> { [            b,            B                                ] };

  key <AC06> { [            f,            F                                ] };

  key <AC07> { [            s,            S,   guillemotleft               ] };

  key <AC08> { [            t,            T                                ] };

  key <AC09> { [            n,            N,  guillemotright               ] };

  key <AC10> { [            d,            D                                ] };

  key <AC11> { [            w,            W                                ] };

  key <BKSL> { [   asciitilde,   numbersign                                ] };

  

  // Fourth row

  key <LSGT> { type[group1] = "FOUR_LEVEL_PLUS_LOCK", [   agrave, ccedilla,  Agrave, Ccedilla,   slash ] };

  key <AB01> { type[group1] = "FOUR_LEVEL_PLUS_LOCK", [ semicolon,  bar,  oe,   OE,   minus ] };

  key <AB02> { [            q,            Q,   braceleft               ] };

  key <AB03> { [        comma,           at,  braceright               ] };

  key <AB04> { [            i,            I,      igrave,       Igrave ] };

  key <AB05> { [            y,            Y,    sterling               ] };

  key <AB06> { [            x,            X                                ] };

  key <AB07> { [            r,            R,   masculine               ] };

  key <AB08> { [            l,            L                                ] };

  key <AB09> { [            p,            P,     section               ] };

  key <AB10> { [            j,            J                                ] };

  

  key <SPCE> { [        space,        space, nobreakspace, nobreakspace ] };

};

  

// C'WHERTY: Breton keyboard. Ar c'hlavier brezhoneg.

// Copyright © 2009 Dominique Pellé <dominique.pelle@gmail.com>

// Version: 0.1

//

// ┌─────┐

// │ S A │   S = Reol = Shift,  A = ArErl + Pennlizherenn = AltGr + Shift

// │ s a │   s = normal,    a = ArErl = AltGr

// └─────┘

//

// ┌─────┬─────┬─────┬─────┬─────┬─────┬─────┬─────┬─────┬─────┬─────┬─────┬─────┲━━━━━━━━━┓

// │ $ Γ │ 1 Δ │ 2 Θ │ 3 Λ │ 4 Ξ │ 5 Π │ 6 Σ │ 7 Φ │ 8 Ψ │ 9 Ç │ 0 Ω │ ° ß │ + ¬ ┃ ⌫ Souzañ┃

// │ ² ˙ │ & ¯ │ é ´ │ " # │ ' { │ ( [ │ - | │ è ` │ - \ │ ç ± │ à @ │ ) ] │ = } ┃     ┃

// ┢━━━━━┷━┱───┴─┬───┴─┬───┴─┬───┴─┬───┴─┬───┴─┬───┴─┬───┴─┬───┴─┬───┴─┬───┴─┬───┺━┳━━━━━━━┫

// ┃Toalenn┃ C'h │ W ω │ E ε │ R ρ │ T τ │ Y ψ │ U υ │ I ι │ O OE│ P π │ ¨ ¥ │ * £ ┃Enankañ┃

// ┃ ↹ ┃ c'h │ w   │ e € │ r   │ t   │ y   │ u   │ i ı │ o oe│ p   │ ^ « │ / » ┃   ⏎   ┃

// ┣━━━━━━━┻┱────┴┬────┴┬────┴┬────┴┬────┴┬────┴┬────┴┬────┴┬────┴┬────┴┬────┴┬────┺┓  ┃

// ┃Prenn   ┃ A Æ │ S σ │ D δ │ F φ │ G γ │ H η │ J ς │ K κ │ L λ │ M μ │ Ù ® │ ! ¡ ┃  ┃

// ┃Pennli ⇬┃ a æ │ s   │ d $ │ f   │ g   │ h   │ j   │ k   │ l   │ m   │ ù ŭ │ ? ¿ ┃  ┃

// ┣━━━━━━━┳┹────┬┴────┬┴────┬┴────┬┴────┬┴────┬┴────┬┴────┬┴────┬┴────┬┴────┲┷━━━━━┻━━━━━━┫

// ┃   ┃ Q θ │ Z ζ │ X ξ │ C χ │ V   │ B β │ N ν │ CH  │ Ñ   │ : © │ ;   ┃         ┃

// ┃Shift ⇧┃ q < │ z > │ x   │ c ¢ │ v   │ b   │ n   │ ch  │ ñ   │ .   │ ,   ┃Shift ⇧  ┃

// ┣━━━━━━━╋━━━━━┷━┳━━━┷━━━┱─┴─────┴─────┴─────┴─────┴─────┴───┲━┷━━━━━╈━━━━━┻━┳━━━━━━━┳━━━┛

// ┃   ┃   ┃   ┃ ⍽ Espace insécable          ␣ ┃   ┃   ┃   ┃

// ┃Reol   ┃Meta   ┃Erl ┃ ␣ Espace                    ␣ ┃ArErl ⇮┃Menu   ┃Reol   ┃

// ┗━━━━━━━┻━━━━━━━┻━━━━━━━┹───────────────────────────────────┺━━━━━━━┻━━━━━━━┻━━━━━━━┛

partial alphanumeric_keys

xkb_symbols "bre" {

  

include "keypad(oss)"

  

name[Group1]= "French (Breton)";

  

// First row

key <TLDE> { [ twosuperior, dead_tilde,   dead_abovedot, Greek_GAMMA ] };

key <AE01> { [   ampersand,          1, dead_macron, Greek_DELTA ] };

key <AE02> { [      eacute,          2,  dead_acute, Greek_THETA ] };

key <AE03> { [    quotedbl,          3,  numbersign, Greek_LAMDA ] };

key <AE04> { [  apostrophe,          4,   braceleft,   Greek_XI ] };

key <AE05> { [   parenleft,          5, bracketleft,   Greek_PI ] };

key <AE06> { [       minus,          6,         bar, Greek_SIGMA ] };

key <AE07> { [      egrave,          7,  dead_grave,  Greek_PHI ] };

key <AE08> { [  underscore,          8,   backslash,  Greek_PSI ] };

key <AE09> { [    ccedilla,          9,   plusminus,   Ccedilla ] };

key <AE10> { [      agrave,          0,          at, Greek_OMEGA ] };

key <AE11> { [  parenright, dead_abovering, bracketright,     ssharp ] };

key <AE12> { [       equal,       plus,  braceright,    notsign ] };

  

// Second row

// Handling the C'H key correctly requires an inputmethod (XIM)

// See https://bugs.freedesktop.org/show_bug.cgi?id=19506

 // key <AD01> { [ trigraph_c_h,   trigraph_C_h, trigraph_C_H, Greek_alpha ] };

key <AD01> { [       UF8FD,      UF8FE,       UF8FF, Greek_alpha ] };

key <AD02> { [           w,          W, Greek_omega, Greek_omega ] };

key <AD03> { [           e,          E,    EuroSign,  Greek_epsilon ] };

key <AD04> { [           r,          R,   Greek_rho,  Greek_rho ] };

key <AD05> { [           t,          T,   Greek_tau,  Greek_tau ] };

key <AD06> { [           y,          Y,   Greek_psi,  Greek_psi ] };

key <AD07> { [           u,          U,   Greek_upsilon,  Greek_upsilon ] };

key <AD08> { [           i,          I,    idotless, Greek_iota ] };

key <AD09> { [           o,          O,          oe,         OE ] };

key <AD10> { [           p,          P,    Greek_pi,   Greek_pi ] };

key <AD11> { [ dead_circumflex, dead_diaeresis,   guillemotleft,        yen ] };

key <AD12> { [       slash,   asterisk,  guillemotright,   sterling ] };

  

// Third row

key <AC01> { [           a,          A,          ae,         AE ] };

key <AC02> { [           s,          S, Greek_sigma, Greek_sigma ] };

key <AC03> { [           d,          D,      dollar, Greek_delta ] };

key <AC04> { [           f,          F,   Greek_phi,  Greek_phi ] };

key <AC05> { [           g,          G, Greek_gamma, Greek_gamma ] };

key <AC06> { [           h,          H,   Greek_eta,  Greek_eta ] };

key <AC07> { [           j,          J, Greek_finalsmallsigma, Greek_finalsmallsigma ] };

key <AC08> { [           k,          K,   Greek_kappa,  Greek_kappa ] };

key <AC09> { [           l,          L,   Greek_lamda, Greek_lambda ] };

key <AC10> { [           m,          M,      Greek_mu, Greek_mu ] };

key <AC11> { [      ugrave,     Ugrave,        ubreve,   registered ] };

key <BKSL> { [    question,     exclam,  questiondown,   exclamdown ] };

  

// Fourth row

key <LSGT> { [           q,          Q,        less, Greek_theta ] };

key <AB01> { [           z,          Z,     greater, Greek_zeta ] };

key <AB02> { [           x,          X,    Greek_xi,   Greek_xi ] };

key <AB03> { [           c,          C,        cent,  Greek_chi ] };

key <AB04> { [           v,          V                              ] };

key <AB05> { [           b,          B,  Greek_beta, Greek_beta ] };

key <AB06> { [           n,          N,    Greek_nu,   Greek_nu ] };

// Handling the CH key correctly requires an inputmethod (XIM)

// See https://bugs.freedesktop.org/show_bug.cgi?id=19506

 // key <AB07> { [  digraph_ch, digraph_Ch,  digraph_CH,  Greek_omicron ] };

key <AB07> { [       UF8FA,      UF8FB,       UF8FC,  Greek_omicron ] };

key <AB08> { [      ntilde,     Ntilde                              ] };

key <AB09> { [      period,      colon,     section,  copyright ] };

key <AB10> { [       comma,  semicolon,     percent             ] };

  

key <SPCE> { [       space,   nobreakspace,       space,   nobreakspace ] };

  

include "level3(ralt_switch)"

};

  

// Occitan layout

// Author : 2009 Thomas Metz <tmetz @ free.fr>

// Derived from the layout defined at http://www.panoccitan.org

// Version: 0.1

// Differences from OSS French keyboard :

// - add á, í, ò, ó et ú, Á, Í, Ò, Ó, Ú, ñ, Ñ

// - change position of æ, ü, î, û, œ, ô, ö, ï, â, ë

//

// ┌─────┬─────┬─────┬─────┬─────┬─────┬─────┬─────┬─────┬─────┬─────┬─────┬─────┲━━━━━━━━━┓

// │ ³ ¸ │ 1 ̨  │ 2 É │ 3 ˘ │ 4 — │ 5 – │ 6 ‑ │ 7 È │ 8 ™ │ 9 Ç │ 0 À │ ° ≠ │ + ± ┃ ⌫ Retour┃

// │ ² ¹ │ & ˇ │ é ~ │ " # │ ' { │ ( [ │ - | │ è ` │ _ \ │ ç ^ │ à @ │ ) ] │ = } ┃  arrière┃

// ┢━━━━━┷━┱───┴─┬───┴─┬───┴─┬───┴─┬───┴─┬───┴─┬───┴─┬───┴─┬───┴─┬───┴─┬───┴─┬───┺━┳━━━━━━━┫

// ┃   ┃ A Á │ Z Æ │ E ¢ │ R Ê │ T Ë │ Y Û │ U Ú │ I Í │ O Ó │ P Ò │ ¨ Œ │ £ Ø ┃Entrée ┃

// ┃Tab ↹  ┃ a á │ z æ │ e € │ r ê │ t ë │ y û │ u ú │ i í │ o ó │ p ò │ ^ œ │ $ ø ┃   ⏎   ┃

// ┣━━━━━━━┻┱────┴┬────┴┬────┴┬────┴┬────┴┬────┴┬────┴┬────┴┬────┴┬────┴┬────┴┬────┺┓  ┃

// ┃    ┃ Q Ä │ S „ │ D Â │ F ‚ │ G ¥ │ H Ü │ J Î │ K Ï │ L Ô │ M Ö │ % Ù │ µ ̄  ┃  ┃

// ┃Maj ⇬   ┃ q ä │ s ß │ d â │ f ‘ │ g ’ │ h ü │ j î │ k ï │ l ô │ m ö │ ù ' │ * ` ┃  ┃

// ┣━━━━━━━┳┹────┬┴────┬┴────┬┴────┬┴────┬┴────┬┴────┬┴────┬┴────┬┴────┬┴────┲┷━━━━━┻━━━━━━┫

// ┃   ┃ > ≥ │ W “ │ X ” │ C ® │ V ← │ B ↑ │ N Ñ │ ? … │ . . │ / ∕ │ § − ┃         ┃

// ┃Shift ⇧┃ < ≤ │ w « │ x » │ c © │ v → │ b ↓ │ n ñ │ , ¿ │ ; × │ : ÷ │ ! ¡ ┃Shift ⇧  ┃

// ┣━━━━━━━╋━━━━━┷━┳━━━┷━━━┱─┴─────┴─────┴─────┴─────┴─────┴───┲━┷━━━━━╈━━━━━┻━┳━━━━━━━┳━━━┛

// ┃   ┃   ┃   ┃ ␣     Espace fine insécable ⍽ ┃   ┃   ┃   ┃

// ┃Ctrl   ┃Meta   ┃Alt ┃ ␣ Espace   Espace insécable ⍽ ┃AltGr ⇮┃Menu   ┃Ctrl   ┃

// ┗━━━━━━━┻━━━━━━━┻━━━━━━━┹───────────────────────────────────┺━━━━━━━┻━━━━━━━┻━━━━━━━┛

partial alphanumeric_keys

xkb_symbols "oci" {

  

include "fr(oss)"

  

name[Group1]= "Occitan";

  

key <AD01>    { [            a,            A,           aacute,            Aacute ] }; // a A á Á

key <AD02>    { [            z,            Z,               ae,                AE ] }; // z Z æ Æ

key <AD05>    { [            t,            T,       ediaeresis,        Ediaeresis ] }; // t T ë Ë

key <AD06>    { [            y,            Y,      ucircumflex,       Ucircumflex ] }; // y Y û Û

key <AD07>    { [            u,            U,           uacute,            Uacute ] }; // u U ú Ú

key <AD08>    { [            i,            I,           iacute,            Iacute ] }; // i I í Í

key <AD09>    { [            o,            O,           oacute,            Oacute ] }; // o O ó Ó

key <AD10>    { [            p,            P,           ograve,            Ograve ] }; // p P ò Ò

key <AD11>    { [  dead_circumflex,   dead_diaeresis,               oe,                OE ] }; // ^ ̈ ̃ œ Œ

  

key <AC03>    { [            d,            D,      acircumflex,       Acircumflex ] }; // d D â Â

key <AC06>    { [            h,            H,       udiaeresis,        Udiaeresis ] }; // h H ü Ü

key <AC07>    { [            j,            J,      icircumflex,       Icircumflex ] }; // j J î Î

key <AC08>    { [            k,            K,       idiaeresis,        Idiaeresis ] }; // k K ï Ï

key <AC09>    { [            l,            L,      ocircumflex,       Ocircumflex ] }; // l L ô Ô

  

key <AB04>  { [            v,            V,       rightarrow,         leftarrow ] }; // v V → ←

key <AB06>  { [            n,            N,           ntilde,            Ntilde ] }; // n N ñ Ñ

};

  

// Marc.Shapiro@inria.fr 19-sep-1998

// modifications : Etienne Herlent <eherlent@linux-france.org> june 2000

// adapted to the new input layer :

//    Martin Costabel <costabel@wanadoo.fr> 3-jan-2001

// adapted for Latin9 alphabet (ISO-8859-15):

//    Etienne Herlent <eherlent@linux-france.org> march 2005

  

// This map is an almost-complete mapping of the standard French

// MacIntosh keyboard under Xwindows.  I tried to remain as faithful

// as possible to the Mac meaning of each key.    I did this entirely by

// hand and by intuition, relying on the Clavier (Keyboard?) Desktop

// Accessory for the Mac meaning of keys, and on reading keysymdef.h

// to intuit the corresponding X names.     Lacking proper documentation,

// I may have made some mistakes.

  

// Entries marked CHECK are particularly uncertain

  

// Entries marked MISSING mark Mac characters for which I was unable

// to find a corresponding keysym.  (Some for sure don't: e.g. the

// Apple mark and the oe/OE character; others I may have simply not

// found.)

  

// Copied from macintosh_vndr/fr

partial alphanumeric_keys

xkb_symbols "mac" {

  

name[Group1]= "French (Macintosh)";

  

key <TLDE> {    [      at, numbersign, periodcentered,  Ydiaeresis    ]    }; // MISSING: Ydiaeresis; eherlent : ok in Latin9

key <AE01> {    [   ampersand, 1,   VoidSymbol, dead_acute    ]    }; // MISSING: Apple

key <AE02> {    [  eacute, 2,   ediaeresis,    Eacute    ]    };

key <AE03> {    [ quotedbl, 3,   VoidSymbol, VoidSymbol    ]     }; // CHECK all quotemarks

key <AE04> {    [  apostrophe, 4,   VoidSymbol, VoidSymbol    ]     };

key <AE05> {    [   parenleft, 5, braceleft,   bracketleft    ]    };

 // CHECK section

key <AE06> {    [ section, 6, paragraph,     aring    ]    };

key <AE07> {    [  egrave, 7, guillemotleft, guillemotright    ]    };

key <AE08> {    [  exclam, 8,   exclamdown,   Ucircumflex    ]    };

key <AE09> {    [ ccedilla, 9, Ccedilla,    Aacute    ]    };

key <AE10> {    [  agrave, 0,   oslash, VoidSymbol    ]    }; // MISSING: Oslash

key <AE11> {    [  parenright, degree, braceright,  bracketright    ]    };

key <AE12> {    [   minus, underscore, emdash,    endash    ]    }; // CHECK dashes

  

key <AD01> {    [       a,  A,       ae,      AE    ]    };

key <AD02> {    [       z,  Z,  Acircumflex,   Aring    ]    };

key <AD03> {    [       e,  E,  ecircumflex, Ecircumflex    ]    };

key <AD04> {    [       r,  R,   registered, currency    ]    };

key <AD05> {    [       t,  T,   VoidSymbol,  VoidSymbol    ]    };

key <AD06> {    [       y,  Y,   Uacute,  Ydiaeresis    ]    }; // MISSING: Ydiaeresis; eherlent : ok in Latin9

key <AD07> {    [       u,  U,   VoidSymbol, ordfeminine    ]    }; // MISSING: ordmasculine?

key <AD08> {    [       i,  I,  icircumflex,  idiaeresis    ]    };

key <AD09> {    [       o,  O,       oe,      OE    ]    }; // MISSING: oe, OE lacking in Latin1; eherlent ok in Latin9

key <AD10> {    [       p,  P,   VoidSymbol,  VoidSymbol    ]    };

key <AD11> {    [dead_circumflex,dead_diaeresis, ocircumflex, Ocircumflex    ]    };

key <AD12> {    [  dollar, asterisk,   EuroSign, yen    ]    }; // eherlent : EuroSign in Latin9

  

key <AC01> {    [     q, Q, acircumflex,     Agrave    ]    };

key <AC02> {    [     s, S,  Ograve, VoidSymbol    ]    };

key <AC03> {    [     d, D,  VoidSymbol, VoidSymbol    ]    };

key <AC04> {    [     f, F,  VoidSymbol, periodcentered    ]    }; // MISSING: oblong script f??

key <AC05> {    [     g, G,  VoidSymbol, VoidSymbol    ]    }; // MISSING: kerned fi, fl

key <AC06> {    [     h, H,  Igrave, Icircumflex    ]    };

key <AC07> {    [     j, J,  Idiaeresis,     Iacute    ]    };

key <AC08> {    [     k, K,  Egrave, Ediaeresis    ]    };

key <AC09> {    [     l, L, notsign,        bar    ]    };

key <AC10> {    [     m, M,      mu,     Oacute    ]    };

key <AC11> {    [ ugrave,percent, Ugrave, ucircumflex    ]    }; // MISSING: per-mille

key <BKSL> {    [ dead_grave, sterling,  at, numbersign    ]    };

  

key <LSGT> {    [  less, greater, VoidSymbol, VoidSymbol    ]    };

key <AB01> {    [     w, W, VoidSymbol,   VoidSymbol    ]    }; // MISSING: half-guillemot (single angle bracket)

key <AB02> {    [     x, X, VoidSymbol,   VoidSymbol    ]    }; // CHECK similarequal; MISSING: extra-slanted slash

key <AB03> {    [     c, C,  copyright,     cent    ]    };

key <AB04> {    [     v, V, diamond,  leftradical    ]    }; // CHECK diamond, leftradical

key <AB05> {    [     b, B, ssharp,    U1E9E    ]    }; // CHECK: Greek_beta or ssharp?; MISSING: oblong script s

key <AB06> {    [     n, N,  dead_tilde,  asciitilde    ]    };

key <AB07> {    [ comma,  question, VoidSymbol,  questiondown    ]    };

key <AB08> {    [ semicolon,  period, VoidSymbol,  periodcentered    ]    };

key <AB09> {    [ colon,  slash,   division,    backslash    ]    };

key <AB10> {    [ equal,   plus, VoidSymbol,    plusminus    ]    };

  

key <SPCE> {    [ space,  space, nobreakspace,   nobreakspace    ]    };

  

key <KPDL> {    [  comma,KP_Decimal    ]    };

  

include "level3(ralt_switch)"

};

  

partial alphanumeric_keys

xkb_symbols "geo" {

include "ge(basic)"

  

name[Group1]= "Georgian (France, AZERTY Tskapo)";

  

key <TLDE> { [ exclam, noSymbol ] };

key <AE01> { [ 0x0100201e, 1 ] };

key <AE02> { [ 0x01002116, 2 ] };

key <AE03> { [ percent, 3 ] };

key <AE04> { [ parenleft, 4  ] };

key <AE05> { [ colon, 5  ] };

key <AE06> { [ semicolon, 6  ] };

key <AE07> { [ question, 7   ] };

key <AE08> { [ 0x01002116, 8 ] };

key <AE09> { [ degree, 9 ] };

key <AE10> { [ parenright, 0 ] };

key <AE11> { [ minus, underscore, 0x01002014 ] };

key <AE12> { [ less, greater ] };

  

key <AD01> { [ Georgian_an, 0x010010fa ] };

key <AD02> { [ Georgian_zen,   Z          ] };

key <AD03> { [ Georgian_en, E, Georgian_he ] };

key <AD04> { [ Georgian_rae,   0x010000ae ] };

key <AD05> { [ Georgian_tar,   T          ] };

key <AD06> { [ Georgian_qar,   0x010010f8 ] };

key <AD07> { [ Georgian_un, U          ] };

key <AD08> { [ Georgian_in, Georgian_hie   ] };

key <AD09> { [ Georgian_on, O          ] };

key <AD10> { [ Georgian_par,   P          ] };

key <AD11> { [ Georgian_tan,   T          ] };

key <AD12> { [ Georgian_jil,   Z          ] };

  

key <AC01> { [ Georgian_khar,  Q          ] };

key <AC02> { [ Georgian_san,   S          ] };

key <AC03> { [ Georgian_don,   D          ] };

key <AC04> { [ Georgian_phar,  Georgian_fi ] };

key <AC05> { [ Georgian_gan,   0x010010f9 ] };

key <AC06> { [ Georgian_hae,   Georgian_hoe   ] };

key <AC07> { [ Georgian_jhan,  0x010010f7 ] };

key <AC08> { [ Georgian_kan,   K          ] };

key <AC09> { [ Georgian_las,   L          ] };

key <AC10> { [ Georgian_man,   M          ] };

key <AC11> { [ Georgian_zhar,  J          ] };

key <BKSL> { [ Georgian_chin,  0x010000a9 ] };

  

key <LSGT> { [ guillemotleft,  guillemotright ] };

key <AB01> { [ Georgian_cil,   W          ] };

key <AB02> { [ Georgian_xan,   Georgian_har   ] };

key <AB03> { [ Georgian_can,   0x010000a9 ] };

key <AB04> { [ Georgian_vin,   Georgian_we ] };

key <AB05> { [ Georgian_ban,   B          ] };

key <AB06> { [ Georgian_nar,   0x010010fc ] };

key <AB07> { [ comma,      0x01002014 ] };

key <AB08> { [ Georgian_shin,  S          ] };

key <AB09> { [ Georgian_ghan,  noSymbol   ] };

key <AB10> { [ Georgian_char,  noSymbol   ] };

  

};

  

// US keyboard made French

//

// Copyright (C) 2018, Florent Gallaire <f@gallai.re>

partial alphanumeric_keys

xkb_symbols "us" {

  

include "us(euro)"

name[Group1]= "French (US, with French letters)";

  
  

key <TLDE> { [ grave, asciitilde, dead_grave               ] };

key <AE06> { [     6,asciicircum,dead_circumflex              ] };

  

key <AB01> { [   z,      Z,   acircumflex,  Acircumflex ] }; // â Â

key <AB03> { [   c,      C,  ccedilla,     Ccedilla ] }; // ç Ç

  

key <AC01> { [   a,      A,    agrave,       Agrave ] }; // à À

key <AC02> { [   s,      S,        ae,           AE ] }; // æ Æ

key <AC03> { [   d,      D,   ecircumflex,  Ecircumflex ] }; // ê Ê

key <AC04> { [   f,      F, ediaeresis,   Ediaeresis ] }; // ë Ë

key <AC06> { [   h,      H, udiaeresis,   Udiaeresis ] }; // ü Ü

key <AC07> { [   j,      J,   ucircumflex,  Ucircumflex ] }; // û Û

key <AC08> { [   k,      K,   icircumflex,  Icircumflex ] }; // î Î

key <AC11> { [apostrophe,   quotedbl,dead_diaeresis               ] };

  

key <AD03> { [   e,      E,    eacute,       Eacute ] }; // é É

key <AD04> { [   r,      R,    egrave,       Egrave ] }; // è È

key <AD06> { [   y,      Y, ydiaeresis,   Ydiaeresis ] }; // ÿ Ÿ

key <AD07> { [   u,      U,    ugrave,       Ugrave ] }; // ù Ù

key <AD08> { [   i,      I, idiaeresis,   Idiaeresis ] }; // ï Ï

key <AD09> { [   o,      O,   ocircumflex,  Ocircumflex ] }; // ô Ô

key <AD10> { [   p,      P,        oe,           OE ] }; // œ Œ

key <AD11> { [ bracketleft,  braceleft,  guillemotleft,  leftdoublequotemark ] }; // « “

key <AD12> { [bracketright, braceright, guillemotright, rightdoublequotemark ] }; // » ”

  

key <AE04> { [    4, dollar,  EuroSign,     currency ] }; // € ¤

};

  

// EXTRAS:

  

partial alphanumeric_keys

    xkb_symbols "sun_type6" {

    include "sun_vndr/fr(sun_type6)"

};

  
  

partial alphanumeric_keys

xkb_symbols "azerty" {

name[Group1]="French (AZERTY)";

  

include "level3(ralt_switch)"

  

// French AZERTY-Keyboard layout

// Author : 2015, Mats Blakstad <mats @ globalbility.org>

// Based on the layout at https://en.wikipedia.org/wiki/File:KB_France.svg

  

// LAYOUT OVERVIEW                          

//  ____ ____ ____ ____ ____ ____ ____ ____ ____ ____ ____ ____ ____ _______

// | | 1  | 2  | 3  | 4  | 5  | 6  | 7  | 8  | 9  | 0  | °  | +  | <--   |

// | ²  | &  | é ~| " #| ' {| ( [| - || è `| _ \| ç ^| à @| ) ]| = }|   |

//  ========================================================================

// | |<-  | A  | Z  | E  | R  | T  | Y  | U  | I  | O  | P  | ¨  | $  |   , |

// |  ->| | a  | z  | e €| r  | t  | y  | u  | i  | o  | p  | ^  | £ ¤| <-' |

//  ===================================================================¬ |

// |   | Q  | S  | D  | F  | G  | H  | J  | K  | L  | M  | %  | µ  | |

// | MAJ   | q  | s  | d  | f  | g  | h  | j  | k  | l  | m  | ù  | *  | |

//  ========================================================================

// | ^   | >  | W  | X  | C  | V  | B  | N  | ?  | .  | /  | §  | ^ |

// | |   | <  | w  | x  | c  | v  | b  | n  | ,  | ;  | :  | !  | | |

//  ========================================================================

// |  |  |  |                   |   |  | |  |

// | Ctrl | Super| Alt  | Space Nobreakspace | AltGr | Super|Menu | Ctrl |

//  ¯¯¯¯¯¯ ¯¯¯¯¯¯ ¯¯¯¯¯¯ ¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯ ¯¯¯¯¯¯¯ ¯¯¯¯¯¯ ¯¯¯¯¯ ¯¯¯¯¯¯

  

// First row

key <TLDE>    { [    twosuperior    ] };

key <AE01>    { [    ampersand,    1    ] };

key <AE02> { [    eacute,   2,   asciitilde         ] };

key <AE03>    { [    quotedbl,    3,   numbersign   ] };

key <AE04>    { [    apostrophe,    4,   braceleft   ] };

key <AE05>    { [    parenleft,    5,   bracketleft   ] };

key <AE06>    { [    minus,   6,   bar   ] };

key <AE07>    { [    egrave,   7,   grave   ] };

key <AE08>    { [    underscore,     8,   backslash   ] };

key <AE09>    { [    ccedilla,     9,   asciicircum   ] };

key <AE10>    { [    agrave,   0,   at   ] };

key <AE11>    { [    parenright,    degree,   bracketright   ] };

key <AE12>    { [    equal,   plus,   braceright   ] };

  

// Second row

key <AD01>    { [    a,   A   ] };

key <AD02>    { [    z,   Z         ] };

key <AD03>    { [    e,   E,   EuroSign   ] };    

key <AD04>    { [    r,   R         ] };

key <AD05>    { [    t,   T   ] };

key <AD06>    { [    y,   Y   ] };    

key <AD07>    { [    u,   U   ] };    

key <AD08>    { [    i,   I   ] };    

key <AD09>    { [    o,   O   ] };    

key <AD10>    { [    p,   P   ] };

key <AD11>    { [    dead_circumflex,dead_diaeresis   ] };

key <AD12>    { [    dollar,   sterling,    currency   ] };    

  

// Third row

key <AC01>    { [    q,   Q   ] };

key <AC02>    { [    s,   S         ] };

key <AC03>    { [    d,   D   ] };    

key <AC04>    { [    f,   F   ] };

key <AC05>    { [    g,   G   ] };    

key <AC06>    { [    h,   H         ] };

key <AC07>    { [    j,   J   ] };

key <AC08>    { [    k,   K   ] };

key <AC09>    { [    l,   L   ] };

key <AC10>    { [    m,   M   ] };    

key <AC11>    { [    ugrave,   percent   ] };

key <BKSL>  { [    asterisk,    mu   ] };

  

// Fourth row

key <LSGT>    { [    less,   greater   ] };

key <AB01>    { [    w,   W   ] };

key <AB02>    { [    x,   X   ] };

key <AB03>    { [    c,   C   ] };

key <AB04>    { [    v,   V   ] };    

key <AB05>  { [    b,   B         ] };

key <AB06>    { [    n,   N         ] };

key <AB07>    { [    comma,   question   ] };

key <AB08>    { [     semicolon,    period   ] };

key <AB09>    { [     colon,   slash   ] };

key <AB10>    { [    exclam,   section   ] };

};

  

// US keyboard made French (with dead keys, alternative)

//

// Copyright (C) 2018, Florent Gallaire <f@gallai.re>

  

partial alphanumeric_keys

xkb_symbols "us-alt" {

  

include "us(euro)"

name[Group1]= "French (US, with French letters, with dead keys, alternative)";

  

key <AB03> { [     c,      C,  ccedilla,     Ccedilla ] }; // ç Ç

  

key <AC01> { [     a,      A,        ae,           AE ] }; // æ Æ

key <AC11> { [dead_diaeresis, quotedbl,  apostrophe ] };

  

key <AD03> { [     e,      E,    eacute,       Eacute ] }; // é É

key <AD09> { [     o,      O,        oe,           OE ] }; // œ Œ

key <AD11> { [ bracketleft,  braceleft,  guillemotleft,  leftdoublequotemark ] }; // « “

key <AD12> { [bracketright, braceright, guillemotright, rightdoublequotemark ] }; // » ”

  

key <TLDE> { [dead_grave, asciitilde,     grave ] };

key <AE06> { [dead_circumflex, asciicircum,   6 ] };

key <AE04> { [     4, dollar,  EuroSign,     currency ] }; // € ¤

  

};

  

// For physically modified US keyboard (Q <-> A, W <-> Z and ; <-> M)

//

// Copyright (C) 2018, Florent Gallaire <f@gallai.re>

  

partial alphanumeric_keys

xkb_symbols "us-azerty" {

  

include "us"

name[Group1]= "French (US, AZERTY)";

  

key <AB01> { [     w,      W, guillemotleft, leftdoublequotemark ] }; // « “

key <AB02> { [     x,      X,guillemotright,rightdoublequotemark ] }; // » ”

key <AB07> { [ semicolon,  colon                              ] };

  

key <AC01> { [     q,      Q                              ] };

key <AC10> { [     m,      M                              ] };

key <AC11> { [apostrophe,   quotedbl,    ugrave,       Ugrave ] }; // ù Ù

  

key <AD01> { [     a,      A,        ae,           AE ] }; // æ Æ

key <AD02> { [     z,      Z                              ] };

key <AD09> { [     o,      O,        oe,           OE ] }; // œ Œ

key <AD11> { [bracketleft, braceleft,dead_circumflex,  dead_diaeresis ] };

  

key <TLDE> { [ grave, asciitilde, dead_grave               ] };

key <AE02> { [     2,     at,    eacute,       Eacute ] }; // é É

key <AE04> { [     4, dollar,  currency               ] }; // ¤

key <AE06> { [     6,asciicircum,dead_circumflex              ] };

key <AE07> { [     7,  ampersand,    egrave,       Egrave ] }; // è È

key <AE09> { [     9,  parenleft,  ccedilla,     Ccedilla ] }; // ç Ç

key <AE10> { [     0, parenright,    agrave,       Agrave ] }; // à À

  

include "eurosign(e)"

include "level3(ralt_switch)"

};

  

// Unicode French standardized new azerty

// Defined by the French national organization for standardization (AFNOR) in norm NF Z71-300 (http://norme-azerty.fr/)

//

// Credits

//   © 2019 Cimbali <me @ cimba.li>

//

// ┌─────┬─────┬─────┬─────┬─────┬─────┬─────┬─────┬─────┬─────┬─────┬─────┬─────┲━━━━━━━━━┓

// │ # ̑  │ 1 À │ 2 É │ 3 È │ 4 Ê │ 5 ̋  │ 6 ̏  │ 7   │ 8 — │ 9 ‹ │ 0 › │ "   │ ¨   ┃ ⌫ Retour┃

// │ @ ̆̆̆  ̆│ à § │ é  ́ │ è  ̀ │ ê & │ ( [ │ ) ] │ ‘ ̄̄  │ ’ _ │ « “ │ » ” │ ' ° │ ̂  ̌̌̌  ┃  arrière┃

// ┢━━━━━┷━┱───┴─┬───┴─┬───┴─┬───┴─┬───┴─┬───┴─┬───┴─┬───┴─┬───┴─┬───┴─┬───┴─┬───┺━┳━━━━━━━┫

// ┃   ┃ A Æ │ Z   │ E   │ R   │ T ™ │ Y   │ U Ù │ I  ̣ │ O Œ │ P ‰ │ – ‑ │ ± ‡ ┃Entrée ┃

// ┃Tab ↹  ┃ a æ │ z £ │ e € │ r ® │ t { │ y } │ u ù │ i ̇  │ o œ │ p % │ - − │ + † ┃   ⏎   ┃

// ┣━━━━━━━┻┱────┴┬────┴┬────┴┬────┴┬────┴┬────┴┬────┴┬────┴┬────┴┬────┴┬────┴┬────┺┓  ┃

// ┃    ┃ Q   │ S ẞ │ D   │ F   │ G   │ H ̱  │ J", │ K   │ L   │ M   │ \ √ │ ½ ¼ ┃  ┃

// ┃Maj ⇬   ┃ q θ │ s ß │ d $ │ f ¤ │ g µ │ h   │ j   │ k ̷  │ l | │ m ∞ │ / ÷ │ * × ┃  ┃

// ┣━━━━━━━┳┹────┬┴────┬┴────┬┴────┬┴────┬┴────┬┴────┬┴────┬┴────┬┴────┬┴────┲┷━━━━━┻━━━━━━┫

// ┃   ┃ > ≥ │ W “ │ X ” │ C ® │ V ← │ B ↑ │ N → │ ? … │ . . │ / ∕ │ § − ┃         ┃

// ┃Shift ⇧┃ < ≤ │ w « │ x » │ c © │ v ⍽ │ b ↓ │ n ¬ │ , ¿ │ ; × │ : ÷ │ ! ¡ ┃Shift ⇧  ┃

// ┣━━━━━━━╋━━━━━┷━┳━━━┷━━━┱─┴─────┴─────┴─────┴─────┴─────┴───┲━┷━━━━━╈━━━━━┻━┳━━━━━━━┳━━━┛

// ┃   ┃   ┃   ┃ ␣     Espace fine insécable ⍽ ┃   ┃   ┃   ┃

// ┃Ctrl   ┃Meta   ┃Alt ┃ ␣ Espace   Espace insécable ⍽ ┃AltGr ⇮┃Menu   ┃Ctrl   ┃

// ┗━━━━━━━┻━━━━━━━┻━━━━━━━┹───────────────────────────────────┺━━━━━━━┻━━━━━━━┻━━━━━━━┛

partial alphanumeric_keys

xkb_symbols "afnor" {

  

include "latin"

include "level3(ralt_switch)"

include "nbsp(level3n)"

include "keypad(oss)"

  

name[Group1]="French (AFNOR standardized AZERTY)";

  

  // First row

  key <TLDE> { [              at,  numbersign,           dead_breve,   dead_invertedbreve ] }; // @ # ̑  ̆̆̆  //

  key <AE01> { [          agrave,           1,              section,           Agrave ] }; // à 1 § À

  key <AE02> { [          eacute,           2,           dead_acute,           Eacute ] }; // é 2  ́ É

  key <AE03> { [          egrave,           3,           dead_grave,           Egrave ] }; // è 3  ̀ È

  key <AE04> { [     ecircumflex,           4,            ampersand,      Ecircumflex ] }; // ê 4 & Ê

  key <AE05> { [       parenleft,           5,          bracketleft, dead_doubleacute ] }; // ( 5 [

  key <AE06> { [      parenright,           6,         bracketright, dead_doublegrave ] }; // ) 6 ]

  key <AE07> { [ leftsinglequotemark,           7,          dead_macron,       VoidSymbol ] }; // ‘ 7

  key <AE08> { [rightsinglequotemark,           8,           underscore,           emdash ] }; // ’ 8 _ —

  key <AE09> { [   guillemotleft,           9,  leftdoublequotemark,       VoidSymbol ] }; // « 9 “ ‹

  key <AE10> { [  guillemotright,           0, rightdoublequotemark,       VoidSymbol ] }; // » 0 ” ›

  key <AE11> { [      apostrophe,    quotedbl,               degree,   dead_abovering ] }; // ' " °

  key <AE12> { [ dead_circumflex,  dead_diaeresis,           dead_caron,       VoidSymbol ] }; // ̂  ¨ ̌̌̌ //

  

  // Second  ow

  key <AD01> { [               a,           A,                   ae,               AE ] }; // a A æ Æ

  key <AD02> { [               z,           Z,             sterling,       VoidSymbol ] }; // z Z £

  key <AD03> { [               e,           E,             EuroSign,       VoidSymbol ] }; // e E €

  key <AD04> { [               r,           R,           registered,       VoidSymbol ] }; // r R ®

  key <AD05> { [               t,           T,            braceleft,        trademark ] }; // t T { ™

  key <AD06> { [               y,           Y,           braceright,       VoidSymbol ] }; // y Y }

  key <AD07> { [               u,           U,               ugrave,           Ugrave ] }; // u U ù Ù

  key <AD08> { [               i,           I,        dead_abovedot,    dead_belowdot ] }; // i I ̇   ̣ //

  key <AD09> { [               o,           O,                   oe,               OE ] }; // o O œ Œ

  key <AD10> { [               p,           P,              percent,         permille ] }; // p P % ‰

  key <AD11> { [           minus,      endash,            0x1002212,        0x1002011 ] }; // - – − ‑ // signe moins (minus sign), trait d'union insécable (non-breaking hyphen)

  key <AD12> { [            plus,   plusminus,               dagger,     doubledagger ] }; // + ± † ‡

  

  // Third r w

  key <AC01> { [               q,           Q,          Greek_theta,       VoidSymbol ] }; // q Q θ

  key <AC02> { [               s,           S,               ssharp,        0x1001E9E ] }; // s S ß ẞ // lettre majuscule latine S dur (latin capital letter sharp s)

  key <AC03> { [               d,           D,               dollar,       VoidSymbol ] }; // d D $

  key <AC04> { [               f,           F,        dead_currency,       VoidSymbol ] }; // f F ¤

  key <AC05> { [               g,           G,           dead_greek,       VoidSymbol ] }; // g G µ

  key <AC06> { [               h,           H,           VoidSymbol, dead_belowmacron ] }; // h H   ̱  // Missing dead key for other european keys (ªəƏþÞıİºſðÐƞȠĳĲ)

  key <AC07> { [               j,           J,           VoidSymbol,       VoidSymbol ] }; // j J

  key <AC08> { [               k,           K,  dead_longsolidusoverlay,       VoidSymbol ] }; // k K ̷ //

  key <AC09> { [               l,           L,                  bar,       VoidSymbol ] }; // l L |

  key <AC10> { [               m,           M,             infinity,       VoidSymbol ] }; // m M ∞

  key <AC11> { [           slash,   backslash,             division,          radical ] }; // / \ ÷ √

  key <BKSL> { [        asterisk,     onehalf,             multiply,       onequarter ] }; // * ½ × ¼

  

  // Fourth row

  key <LSGT> { [            less,     greater,        lessthanequal, greaterthanequal ] }; // < > ≤ ≥

  key <AB01> { [               w,           W,                  ezh,             EZH ] }; // w W ʒ Ʒ

  key <AB02> { [               x,           X,            copyright,      VoidSymbol ] }; // x X ©

  key <AB03> { [               c,           C,             ccedilla,        Ccedilla ] }; // c C ç Ç

  key <AB04> { [               v,           V,         dead_cedilla,     dead_ogonek ] }; // v V ̧  ̨  //

  key <AB05> { [               b,           B,          dead_stroke,      VoidSymbol ] }; // b B ̵ //

  key <AB06> { [               n,           N,           dead_tilde,      VoidSymbol ] }; // n N ~

  key <AB07> { [          period,    question,         questiondown,      VoidSymbol ] }; // . ? ¿

  key <AB08> { [           comma,      exclam,           exclamdown, dead_belowcomma ] }; // , ! ¡ ̦  //

  key <AB09> { [           colon,    ellipsis,       periodcentered,      VoidSymbol ] }; // : … ·

  key <AB10> { [       semicolon,       equal,         similarequal,        notequal ] }; // ; = ≃ ≠

};
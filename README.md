SubGHz_Phy/Target/radio_board_if.hの66行目
```C
#define RBI_CONF_RFO RBI_CONF_RFO_HP
```
これがCubeMXでコード生成をかけた後
```C
#define RBI_CONF_RFO RBI_CONF_RFO_LP_HP
```
となる．この状態だと無線通信の強度が弱くなり，通信できなくなる．  
なので，手動で`#define RBI_CONF_RFO RBI_CONF_RFO_HP`に戻してやる必要がある．

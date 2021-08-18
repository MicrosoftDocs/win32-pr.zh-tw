---
description: 在 MOF 中，數位是描述數值的數位。 MOF 提供各種可轉譯成自動化的資料類型，也可讓這些數位採用不同的格式。 下表列出 MOF 所支援的數位值。
ms.assetid: 7a18ed36-9c12-42be-a4ee-0f6c0097b130
ms.tgt_platform: multiple
title: " (WMI) 的數位"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f3441988bb91d4bb2f3742016f01cb69996e3dcb55081a6723d851ed74cc1cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118555132"
---
# <a name="numbers-wmi"></a> (WMI) 的數位

在 MOF 中，數位是描述數值的數位。 MOF 提供各種可轉譯成自動化的資料類型，也可讓這些數位採用不同的格式。 下表列出 MOF 所支援的數位值。



| 資料類型  | Automation 類型 | 描述                                                                                                                                                             |
|------------|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **sint8**  | **VT \_ I2**      | 帶正負號的8位整數。<br/>                                                                                                                                        |
| **sint16** | **VT \_ I2**      | 帶正負號的16位整數。<br/>                                                                                                                                       |
| **sint32** | VT \_ I4          | 帶正負號的32位整數。<br/>                                                                                                                                       |
| **sint64** | **VT \_ BSTR**    | 字串格式的帶正負號64位整數。 根據美國國家標準局 (ANSI) C 規則，此類型遵循十六進位或十進位格式。<br/> |
| **real32** | **VT \_ R4**      | 四位元組浮點數，依照電氣和電子工程師協會，Inc. (IEEE) 標準。<br/>                                        |
| **real64** | **VT \_ R8**      | 遵循 IEEE 標準的8位元組浮點值。<br/>                                                                                                  |
| **uint8**  | **VT \_ UI1**     | 不帶正負號的8位整數。<br/>                                                                                                                                      |
| **uint16** | **VT \_ I4**      | 不帶正負號的16位整數。<br/>                                                                                                                                     |
| **uint32** | **VT \_ I4**      | 不帶正負號的32位整數。<br/>                                                                                                                                     |
| **uint64** | **VT \_ BSTR**    | 字串格式的不帶正負號64位整數。 此類型遵循的是十六進位或十進位格式（根據 ANSI C 規則）。<br/>                                           |



 

雖然有彈性，但 MOF 程式碼會在處理自動化時遇到一些變更：

-   您必須將64位整數編碼為字串。

    Automation 不支援64位整數類型。

-   Automation 型別不一定會對應到 MOF 資料類型的位大小。

    例如，Automation 使用 VT \_ I4 傳回不帶正負號的16位值。 因為有正負號延伸的問題，所以這項差異存在。 如果自動化使用 VT （ \_ 而非 vt \_ I4），65536會顯示為值1，導致類型和範圍問題。 同樣地，Automation 將 **uint32** 類型表示為 VT \_ I4，因為沒有較大的整數類型可包含 **uint32**。

-   您不需要變更8位數位類型的任何標記法。

    Automation 支援 VT \_ UI1，這是一個不帶正負號的8位類型。

MOF 支援長常數。 您可以使用具有選擇性負號的簡單數位系列來宣告長常數。 長常數不能超過宣告用來保存它之變數的大小。 長常數的一些範例是1000和12310。

MOF 也支援替代的數位格式。 下表列出您必須用來描述十六進位、二進位和八進位常數的特殊字元。



| 常數               | 特殊字元     | 範例                   |
|------------------------|-----------------------|---------------------------|
| Decimal<br/>     | 無<br/>       | val = 65<br/>       |
| 十六進位<br/> | 0x 前置詞<br/>  | val = 0x41 向<br/>     |
| 八進位<br/>       | 前置0<br/>  | val = 0101<br/>     |
| Binary<br/>      | 尾端 B<br/> | val = 1000001B<br/> |



 

您可以使用浮點常數來表示科學記號和分數，如下所示：

``` syntax
3.14
-3.14
-1.2778E+02
```

WMI 會將浮點常數視為自動化的 **VT \_ R8** 類型。

下列範例描述的類別和實例宣告，說明如何使用每個數值資料類型來設定屬性：

``` syntax
Class NumericDataClass
 {
   [key] uint8 Duint8;
   SInt8       Dchar;
   UInt16      Dtword;
   Sint16      Dinst16;
   UInt32      Ddword;
   Sint32      Dinst1;
   Sint32      Dinst2;
   Sint32      Dinst3;
   Sint32      Dinst4;
   Sint32      Dinst5;
   Real32      Dfloat;
   Real64      Ddouble1;
   Real64      Ddouble2;
 };

instance of NumericDataClass
 {
   Duint8   =  122;
   Dchar    = -128;
   Dtword   =  30;
   Dinst16  = -1445;
   Ddword   =  6987777;
   Dinst1   = -455589;
   Dinst2   =  23;
   Dinst3   =  03;         // Base 8
   Dinst4   =  0xFe;       // Base 16
   Dinst5   =  11b;        // Base 2
   Dfloat   =  3.1478;
   Ddouble1 =  99987.3654;
   Ddouble2 =  2.3e-2;
 };
```

 

 





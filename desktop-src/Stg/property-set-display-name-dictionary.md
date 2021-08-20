---
title: 屬性集顯示名稱字典
description: 屬性顯示名稱的字典可讓屬性（property）使用者將意義附加至屬性，而不是由類型指標所提供的屬性。
ms.assetid: b6813a86-39d3-4754-86e4-51035a7c91d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90e416b41844348b80ce6db561a5c63a7717b1e6a98da1f6edead0d48f66e780
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117960737"
---
# <a name="property-set-display-name-dictionary"></a>屬性集顯示名稱字典

屬性顯示名稱的字典可讓屬性（property）使用者將意義附加至屬性，而不是由類型指標所提供的屬性。

## <a name="dictionary-structure"></a>字典結構

字典包含清單中的專案計數，後面接著字典專案的清單。

``` syntax
typedef struct tagDICTIONARY 
{ 
    DWORD  cEntries ;               // Count of entries in the list 
    ENTRY  rgEntry[ cEntries ] ;    // Property ID/String pair 
} DICTIONARY ;
```

## <a name="dictionary-entry-structure"></a>字典輸入結構

清單中的每個字典專案都是屬性識別碼/字串配對。 以下是字典專案的虛擬結構定義。 它是虛擬結構，因為 sz 成員的 \[ \] 大小是可變的。

``` syntax
typedef struct tagENTRY 
{ 
    DWORD  propid ;    // Property ID 
    DWORD  cch ;       // Count of characters in the string 
    char  sz[cch];     // Zero-terminated string 
} ENTRY ;
```

## <a name="sample-dictionary"></a>範例字典

下列股票市場資料傳輸範例可能會在整個集合中包含可顯示的名稱「股票報價」，以及 PID 符號的「代號符號」 \_ 。 如果屬性集只包含符號和字典，屬性集區段會有如下所示的位元組資料流程。

``` syntax
Offset     Bytes 
; Start of section 
0000    5C 01 00 00    ; DWORD size of section 
0004    04 00 00 00    ; DWORD number of properties in section 
 
; Start of PropID/Offset pairs 
0008    01 00 00 00    ; DWORD Property ID (1 == code page) 
000C    28 00 00 00    ; DWORD offset to property ID 
0010    00 00 00 80    ; DWORD Property ID (0x80000000 == locale
                                                 ID) 
0014    30 00 00 00    ; DWORD offset to property ID 
0018    00 00 00 00    ; DWORD Property ID (0 == dictionary) 
001C    38 00 00 00    ; DWORD offset to property ID 
0020    07 00 00 00    ; DWORD Property ID (7 == PID_SYMBOL)
0024    5C 01 00 00    ; DWORD offset to property ID
 
; Start of Property 1 (code page)
0028    01 00 00 00    ; DWORD type indicator (VT_12)
002C    B0 04          ; USHORT codepage (0x04b0 == 1200 ==
                                                 unicode)
002E    00 00          ; Pad to 32-bit boundary
 
; Start of Property 0x80000000 (Local ID)
0030    13 00 00 00    ; DWORD type indicator (VT_U14)
0034    09 04 00 00    ; ULONG locale ID (0x0409 == American 
                                                 English)
 
; Start of Property 0 (the dictionary)
0038    08 00 00 00    ; DWORD number of entries in dictionary
                             (Note:  No type indicator)
003C    00 00 00 00    ; DWORD propid == 0 (the dictionary)
0040    0C 00 00 00    ; DWORD cch == wcslen(L"Stock Quote") +
                                                 sizeof(L'\0') == 12
0044    L"Stock Quote" ; wchar_t wsz(12)
005C    05 00 00 00    ; DWORD propid == 5 (PID_HIGH)
0060    0B 00 00 00    ; DWORD cch == wcslen(L"High Price") + 
                                                 sizeof(L'\0') == 11
0064    L"High Price\0"; wchar_t wsz(11)
007A    00 00          ; padding for 32-bit alignment (necessary
                             because the codepage is unicode)
007C    07 00 00 00    ; DWORD propid == 7 (PID_SYMBOL)
0080    0E 00 00 00    ; DWORD cch - wcslen(L"Ticker Symbol\0") 
                             == 14
0084    L"Ticker Symbol\0" ; wchar_t wsz(14)
 
    // The dictionary would continue, but may not contain entries 
    // for every possible property, and may contain entries for 
    // properties that are not present. Entries are not required  
    // to be in order.
```

請注意下列有關屬性集字典的問題：

-   屬性識別碼0沒有類型指標。 **DWORD** 資料類型，指出位於類型指標位置的專案計數。
-   *Cch* 字串中的字元計數包含終止字串的零個字元。 當屬性集的字碼頁不是 Unicode 時，此欄位實際上是 **位元組** 計數。 若是格式為0的屬性集，這個計數可能不會超過256。 針對格式為1的屬性集，這個計數可能會和 total property set 大小所允許的大小一樣大。
-   字典是選擇性的。 並非集合中的所有屬性名稱都必須出現在字典中。 相反地，並非字典中的所有名稱都需要對應至集合中的屬性。 字典應該略過屬性的專案，而這些屬性是由操作屬性集的應用程式所被視為普遍辨識的。 一般而言，會省略廣泛接受標準的基底屬性集名稱，但特殊用途的屬性集可能包含瀏覽器所使用的字典。
-   字典中的屬性名稱會儲存在由 [屬性識別碼 1](/windows/desktop/Stg/reserved-property-identifiers)指出的字碼頁中。 針對 ANSI 字碼頁，每個字典專案都是以位元組對齊。 因此，屬性識別碼為0的屬性名稱之間沒有間距。 這是在32位界限上，不需要對齊 **DWORD** 資料類型 (屬性識別碼和屬性名稱長度 **DWORD** s) 值的唯一情況。 若為 Unicode 頁面，每個字典專案都會對齊32位。
-   以二進位 Unicode 字元（以0x0001 到0x001F）開頭的屬性名稱會保留供日後使用。
-   與屬性識別碼0相關聯的屬性名稱代表整個屬性集的名稱。

 

 
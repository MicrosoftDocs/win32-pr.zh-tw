---
description: 下列 (Guid) 的全域唯一識別碼，Windows 筆記本用來識別筆劃或繪圖屬性上的自訂屬性。
ms.assetid: a7488c26-b61f-47d8-a19b-d630a8c00875
title: 自訂屬性 Guid
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eb1d9069f2c655f658752a6ae3891910ff68103
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987331"
---
# <a name="custom-property-guids"></a>自訂屬性 Guid

下列 (Guid) 的全域唯一識別碼，Windows 筆記本用來識別筆劃或繪圖屬性上的自訂屬性。

## <a name="guid_stroke_timestamp"></a>GUID \_ 筆劃 \_ 時間戳記


```C++
GUID_STROKE_TIMESTAMP = {4EA66C4-F33A-461B-B8FE-68070D9C7575}
```



這是一個 [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) 結構，表示筆劃的建立時間或新增至檔的時間。


```C++
typedef struct _FILETIME {
    DWORD dwLowDateTime;
    DWORD dwHighDateTime;
} FILETIME, *PFILETIME;
```



## <a name="guid_stroke_timeid"></a>GUID \_ 筆劃 \_ TIMEID


```C++
GUID_STROKE_TIMEID = {50B6BC8-3B7D-4816-8C61-BC7E905B2132}
```



這是 **TIMEID** 結構。 它可讓您在貼上和卸載作業期間維持筆劃順序。 如果沒有 **TIMEID** 結構，在 [InkStrokes 集合](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))中剪下和貼上的所有 [**IInkStrokeDisp 介面**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)物件的時間戳記都會相同。


```C++
typedef struct tagTIMEID {
    FILETIME  tmFiletime;
    ULONG     uiOrder;
} TIMEID;
```



## <a name="guid_highlighter"></a>GUID \_ 螢光筆

這是 **布林** 值，其中 **TRUE**= 螢光筆筆墨， **FALSE**= 一般筆跡。 這會套用至繪圖屬性。


```C++
GUID_HIGHLIGHTER = {9B6267B8-3968-4048-AB74-F490406A2DFA}
```



## <a name="guid_ink_style_bold"></a>GUID \_ 筆墨 \_ 樣式 \_ 粗體

這是 **布林** 值，其中 **TRUE**= bold 筆墨， **FALSE**= normal。 這會套用至繪圖屬性。


```C++
GUID_INK_STYLE_BOLD = {E02FB5C1-9693-4312-A434-00DE7F3AD493}
```



## <a name="guid_ink_style_italics"></a>GUID \_ 筆墨 \_ 樣式 \_ 斜體

這是 **布林** 值，其中 **TRUE**= 斜體筆墨， **FALSE**= normal。 這會套用至繪圖屬性。


```C++
GUID_INK_STYLE_ITALICS = {05253B51-49C6-4A04-8993-64DD9ABD842A}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IJournalReader 介面**](ijournalreader.md)
</dt> </dl>

 

 

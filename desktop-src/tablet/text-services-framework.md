---
description: Tablet PC 的文字服務架構總覽。
ms.assetid: f77fe77a-8625-47c5-bfc7-b473c8e8a8c6
title: '文字服務架構 (Tablet PC) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c25eb3e635ae7394502ed203cb9ea31e115dc09e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981676"
---
# <a name="text-services-framework-tablet-pc"></a>文字服務架構 (Tablet PC) 

當已附加[PenInputPanel](/previous-versions/aa514041(v=msdn.10))物件的控制項上啟用[文字服務架構 (TSF) ](../tsf/text-services-framework.md)時，PenInputPanel 物件可以直接插入文字。 如果控制項不支援文字服務架構 (TSF) ，則 PenInputPanel 物件必須使用 [SendInput 函數](/windows/win32/api/winuser/nf-winuser-sendinput) 來插入文字。

直接插入文字的功能對於輸入東亞字元而言非常重要，因為使用 [SendInput](/windows/win32/api/winuser/nf-winuser-sendinput) 函式可能會產生不正確的字元。

TSF 提供可更正辨識錯誤的介面，讓使用者能夠更正、重寫或甚至聽寫適當的文字。

藉由呼叫 [EnableTsf](/previous-versions/ms569656(v=vs.100)) 方法，並將 *enable* 參數設定為 **TRUE**，即可啟用 TSF。

\[C\#\]


```C++
PenInputPanel thePenInputPanel = new PenInputPanel(theControl);
//...
thePenInputPanel.EnableTsf(true);
```



附加至[InkEdit](/previous-versions/ms552265(v=vs.100))控制項的[PenInputPanel](/previous-versions/aa514041(v=msdn.10))物件可提供健全的使用者經驗，因為 InkEdit 支援 TSF。 不過，請務必將 InkEdit 控制項上的 [InkMode](/previous-versions/ms835850(v=msdn.10)) 屬性設定為 [InkMode](/previous-versions/ms827399(v=msdn.10)) ，如 [最佳作法](best-practices.md) 主題所述。

[PenInputPanel 範例](peninputpanel-sample.md)提供啟用 TSF 的範例。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Text Services Framework (TSF)](../tsf/text-services-framework.md)
</dt> </dl>

 

 

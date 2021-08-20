---
title: 如何處理 DTN_WMKEYDOWN 通知
description: 本主題將示範如何處理 DTN \_ WMKEYDOWN 通知。 處理此通知程式碼可讓控制項的擁有者在控制項的回呼欄位內提供對按鍵的特定回應。
ms.assetid: CD521C62-CF52-4FFF-A598-E5EBA34471FB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbef0804afb388f9cadad60b04bf93ce4730ef255476f0c7f216edfd24846a19
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540348"
---
# <a name="how-to-process-the-dtn_wmkeydown-notification"></a>如何處理 DTN \_ WMKEYDOWN 通知

本主題將示範如何處理 [DTN \_ WMKEYDOWN](dtn-wmkeydown.md) 通知。 處理此通知程式碼可讓控制項的擁有者在控制項的回呼欄位內提供對按鍵的特定回應。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [Windows控制](window-controls.md)

### <a name="prerequisites"></a>必要條件

-   C/C++
-   Windows消費者介面程式設計

## <a name="instructions"></a>指示


日期和時間選擇器 (DTP) 控制項傳送 [DTN \_ WMKEYDOWN](dtn-wmkeydown.md) 訊息，以報告使用者已在回呼欄位中輸入輸入。 如果您想要模擬標準 DTP 欄位所支援的相同鍵盤回應，或提供自訂回應，您的應用程式必須包含程式碼來處理此通知。

下列 c + + 程式碼範例是應用程式定義的函數，可處理 [DTN \_ WMKEYDOWN](dtn-wmkeydown.md) 通知。

**安全性警告：** 不當使用 **lstrcmp** 可能會危及應用程式的安全性。 例如，在下列程式碼範例中呼叫 **lstrcmp** 之前，您應該確定兩個字串是以 null 結束。 您應複習[安全性考慮： Microsoft Windows 控制項](sec-comctls.md)，再繼續進行。



```C++
//  DoWMKeydown increments or decrements the day of month according 
//  to user keyboard input.

void WINAPI DoWMKeydown(
 HWND hwndDP,
 LPNMDATETIMEWMKEYDOWN lpDTKeystroke)
{
    int delta =1;
    if(!lstrcmp(lpDTKeystroke->pszFormat,L"XX")){
        switch(lpDTKeystroke->nVirtKey){
            case VK_DOWN:
            case VK_SUBTRACT:
                delta = -1;  // fall through

            case VK_UP:
            case VK_ADD:
                lpDTKeystroke->st.wDay += (WORD) delta;
                break;
        }
    }
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用日期時間選擇器控制項](using-date-and-time-picker.md)
</dt> <dt>

[日期和時間選擇器控制項參考](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[日期和時間選擇器](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 





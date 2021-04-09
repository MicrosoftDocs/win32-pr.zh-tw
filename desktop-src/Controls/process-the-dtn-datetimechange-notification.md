---
title: 如何處理 DTN_DATETIMECHANGE 通知
description: 本主題示範如何將使用者所做的變更通知， (DTP) 控制項的日期和時間選擇器處理。
ms.assetid: AE029962-E9D3-47BC-A24F-312B54137F18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5434c7ebbda673f76a757375e9a3d23504483d42
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "103933759"
---
# <a name="how-to-process-the-dtn_datetimechange-notification"></a>如何處理 DTN \_ DATETIMECHANGE 通知

本主題示範如何將使用者所做的變更通知， (DTP) 控制項的日期和時間選擇器處理。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [Windows 控制項](window-controls.md)

### <a name="prerequisites"></a>必要條件

-   C/C++
-   Windows 消費者介面程式設計

## <a name="instructions"></a>指示


每當發生變更時，DTP 控制項會傳送 [DTN \_ DATETIMECHANGE](dtn-datetimechange.md) 通知程式碼。 例如，當使用者變更控制項中的其中一個欄位，或在控制項設定為 [**DTS \_ SHOWNONE**](date-and-time-picker-control-styles.md) 樣式的情況下，當使用者變更控制項核取方塊的狀態時，就會產生這項通知。

您的應用程式必須包含程式碼，以處理 \_ 由 DTP 控制項所傳送的 DTN DATETIMECHANGE 訊息。

下列 c + + 程式碼範例是應用程式定義的函式，設計來指出設定為 **DTS \_ SHOWNONE** 樣式之 DTP 控制項的狀態。



```C++
void WINAPI DoDateTimeChange(LPNMDATETIMECHANGE lpChange)
{
    // If the user has unchecked the DTP's check box, change the
    // text in a static control to show the appropriate message.
    //
    // g_hwndDlg - a program-global address of a dialog box.

    if(lpChange->dwFlags == GDT_NONE)
        SetDlgItemText(g_hwndDlg, IDC_STATUS, L"Disabled");
    else
        SetDlgItemText(g_hwndDlg, IDC_STATUS, L"Active");
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

 

 





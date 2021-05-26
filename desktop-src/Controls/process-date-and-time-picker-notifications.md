---
title: 如何處理日期和時間選擇器通知
description: 本節示範如何處理日期和時間選擇器的通知。
ms.assetid: DBF624F0-89E0-435B-BE96-60B7A4CEDA61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffa1214ebd671b4ae222990bde4b44586e6d7b11
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424178"
---
# <a name="how-to-process-date-and-time-picker-notifications"></a>如何處理日期和時間選擇器通知

本節示範如何處理日期和時間選擇器的通知。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [Windows 控制項](window-controls.md)

### <a name="prerequisites"></a>必要條件

-   C/C++
-   Windows 消費者介面程式設計

## <a name="instructions"></a>指示


日期和時間選擇器 () 控制項會在控制項中發生事件（通常是由使用者輸入觸發）時，將通知訊息傳送至父視窗。 您的應用程式必須包含程式碼，以判斷通知訊息的類型並適當地回應。

如果您打算在應用程式中搭配使用回呼欄位與 DTP 控制項，您必須準備好處理 [DTN \_ FORMATQUERY](dtn-formatquery.md)、 [DTN \_ 格式](dtn-format.md)和 [DTN \_ WMKEYDOWN](dtn-wmkeydown.md) 通知碼。 如需回呼欄位的詳細資訊，請參閱 [回呼欄位](date-and-time-picker-controls.md)。

下列 c + + 程式碼範例會識別由 DTP 控制項所傳送的通知訊息，並呼叫適當的應用程式定義函數。 請參閱下列主題中的程式碼範例，以瞭解如何處理此範例中所顯示的通知。

|   主題                                                                                                     |
|--------------------------------------------------------------------------------------------------------|
| [如何處理 DTN \_ DATETIMECHANGE 通知](process-the-dtn-datetimechange-notification.md) |
| [如何處理 DTN \_ FORMATQUERY 通知](process-the-dtn-formatquery-notification.md)       |
| [如何處理 DTN \_ 格式通知](process-the-dtn-format-notfication.md)                  |
| [如何處理 DTN \_ WMKEYDOWN 通知](process-the-dtn-wmkeydown-notification.md)           |



 



```C++
BOOL WINAPI DoNotify(HWND hwnd, WPARAM wParam, LPARAM lParam)
{
    LPNMHDR hdr = (LPNMHDR)lParam;

    switch(hdr->code){

        case DTN_DATETIMECHANGE:{
            LPNMDATETIMECHANGE lpChange = (LPNMDATETIMECHANGE)lParam;
            DoDateTimeChange(lpChange);
        }
        break;

        case DTN_FORMATQUERY:{
            LPNMDATETIMEFORMATQUERY lpDTFQuery = (LPNMDATETIMEFORMATQUERY)lParam;

            // Process DTN_FORMATQUERY to ensure that the control
            // displays callback information properly.
            DoFormatQuery(hdr->hwndFrom, lpDTFQuery);
        }
        break;

        case DTN_FORMAT:{
            LPNMDATETIMEFORMAT lpNMFormat = (LPNMDATETIMEFORMAT) lParam;

            // Process DTN_FORMAT to supply information about callback
            // fields (fields) in the DTP control.
            DoFormat(hdr->hwndFrom, lpNMFormat);
        }
        break;

        case DTN_WMKEYDOWN:{
            LPNMDATETIMEWMKEYDOWN lpDTKeystroke = 
                            (LPNMDATETIMEWMKEYDOWN)lParam;

            // Process DTN_WMKEYDOWN to respond to a user's keystroke in
            // a callback field.
            DoWMKeydown(hdr->hwndFrom, lpDTKeystroke);
        }
        break;
    }

    // All of the above notifications require the owner to return zero.
    return FALSE;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[日期和時間選擇器通知](bumper-date-and-time-picker-control-reference-notifications.md)
</dt> <dt>

[日期和時間選擇器控制項參考](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[使用日期時間選擇器控制項](using-date-and-time-picker.md)
</dt> <dt>

[日期和時間選擇器](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 





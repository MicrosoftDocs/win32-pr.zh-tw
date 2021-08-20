---
title: 如何設定日期狀態
description: 本主題將示範如何設定日狀態資訊。 月曆控制項會使用日期狀態資訊來決定它在控制項內的特定天數。
ms.assetid: EA92D858-BC80-4D08-9768-29A2BBDF900C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e3ed2c99e6faf18f0e1d06ec06eaaf9a0d573faebe6f3697e43562603447571
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078472"
---
# <a name="how-to-set-day-states"></a>如何設定日期狀態

本主題將示範如何設定日狀態資訊。 月曆控制項會使用日期狀態資訊來決定它在控制項內的特定天數。

使用 [**MCS \_ DAYSTATE**](month-calendar-control-styles.md) 樣式支援日狀態的月曆控制項。 日期狀態資訊會以32位資料類型 [**MONTHDAYSTATE**](monthdaystate.md)表示。 **MONTHDAYSTATE** 等位中的每個位 (0 到 30) 指定一個月中某一天的狀態。 如果位為開啟，對應的日期會以粗體顯示。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [Windows控制](window-controls.md)

### <a name="prerequisites"></a>必要條件

-   C/C++
-   Windows消費者介面程式設計

## <a name="instructions"></a>指示


應用程式可以藉由傳送 [**MCM \_ SETDAYSTATE**](mcm-setdaystate.md) 訊息或使用對應的宏 [**MonthCal \_ SETDAYSTATE**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setdaystate)來明確設定日狀態資訊。 但是，日期狀態資訊通常是為了回應 [MCN \_ GETDAYSTATE](mcn-getdaystate.md) 通知碼而設定的，這會在每次控制項需要重新整理時傳送，例如，每個月都已滾動查看。

下列範例程式碼示範如何在 [**WM \_ 通知**](wm-notify.md)訊息處理常式中處理 [MCN \_ GETDAYSTATE](mcn-getdaystate.md)通知程式碼。 它會 \_ 指定每個可見月份的第一天和第十五天應該反白顯示，以處理 MCN GETDAYSTATE。 [**NMDAYSTATE**](/windows/win32/api/commctrl/ns-commctrl-nmdaystate)結構的 **cDayState** 成員會指定陣列中所需的 [**MONTHDAYSTATE**](monthdaystate.md)值數目，其具有任意大小的上限。 然後，程式碼會使用應用程式定義的 **BOLDDAY** 宏，迴圈在陣列的每個有效元素中設定適當的位。



```C++
    #define BOLDDAY(ds, iDay)  \
        if (iDay > 0 && iDay < 32)(ds) |= (0x00000001 << (iDay - 1))

    case WM_NOTIFY:
            if (((LPNMHDR)lParam)->code == MCN_GETDAYSTATE)
            {
                MONTHDAYSTATE rgMonths[12] = { 0 };
                int cMonths = ((NMDAYSTATE*)lParam)->cDayState;
                for (int i = 0; i < cMonths; i++)
                {
                    BOLDDAY(rgMonths[i], 1);
                    BOLDDAY(rgMonths[i], 15);
                }
                ((NMDAYSTATE*)lParam)->prgDayState = rgMonths;
                return TRUE;
            }
            break;
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[月曆控制項參考](bumper-month-calendar-month-calendar-control-reference.md)
</dt> <dt>

[關於 Month Calendar 控制項](month-calendar-controls.md)
</dt> <dt>

[使用月曆控制項](using-month-calendar-controls.md)
</dt> </dl>

 

 





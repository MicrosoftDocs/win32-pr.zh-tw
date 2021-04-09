---
title: 如何設定日期狀態
description: 本主題將示範如何設定日狀態資訊。 月曆控制項會使用日期狀態資訊來決定它在控制項內的特定天數。
ms.assetid: EA92D858-BC80-4D08-9768-29A2BBDF900C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa1fc105c94a15e1a658218013dca00129c883c2
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "103933755"
---
# <a name="how-to-set-day-states"></a><span data-ttu-id="157a1-104">如何設定日期狀態</span><span class="sxs-lookup"><span data-stu-id="157a1-104">How to Set Day States</span></span>

<span data-ttu-id="157a1-105">本主題將示範如何設定日狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="157a1-105">This topic demonstrates how to set day state information.</span></span> <span data-ttu-id="157a1-106">月曆控制項會使用日期狀態資訊來決定它在控制項內的特定天數。</span><span class="sxs-lookup"><span data-stu-id="157a1-106">The month calendar control uses day state information to determine how it draws specific days within the control.</span></span>

<span data-ttu-id="157a1-107">使用 [**MCS \_ DAYSTATE**](month-calendar-control-styles.md) 樣式支援日狀態的月曆控制項。</span><span class="sxs-lookup"><span data-stu-id="157a1-107">Month calendar controls that use the [**MCS\_DAYSTATE**](month-calendar-control-styles.md) style support day states.</span></span> <span data-ttu-id="157a1-108">日期狀態資訊會以32位資料類型 [**MONTHDAYSTATE**](monthdaystate.md)表示。</span><span class="sxs-lookup"><span data-stu-id="157a1-108">Day state information is expressed as a 32-bit data type, [**MONTHDAYSTATE**](monthdaystate.md).</span></span> <span data-ttu-id="157a1-109">**MONTHDAYSTATE** 等位中的每個位 (0 到 30) 指定一個月中某一天的狀態。</span><span class="sxs-lookup"><span data-stu-id="157a1-109">Each bit in a **MONTHDAYSTATE** bitfield (0 through 30) specifies the state of a day in a month.</span></span> <span data-ttu-id="157a1-110">如果位為開啟，對應的日期會以粗體顯示。</span><span class="sxs-lookup"><span data-stu-id="157a1-110">If a bit is on, the corresponding day is displayed in bold.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="157a1-111">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="157a1-111">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="157a1-112">技術</span><span class="sxs-lookup"><span data-stu-id="157a1-112">Technologies</span></span>

-   [<span data-ttu-id="157a1-113">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="157a1-113">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="157a1-114">必要條件</span><span class="sxs-lookup"><span data-stu-id="157a1-114">Prerequisites</span></span>

-   <span data-ttu-id="157a1-115">C/C++</span><span class="sxs-lookup"><span data-stu-id="157a1-115">C/C++</span></span>
-   <span data-ttu-id="157a1-116">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="157a1-116">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="157a1-117">指示</span><span class="sxs-lookup"><span data-stu-id="157a1-117">Instructions</span></span>


<span data-ttu-id="157a1-118">應用程式可以藉由傳送 [**MCM \_ SETDAYSTATE**](mcm-setdaystate.md) 訊息或使用對應的宏 [**MonthCal \_ SETDAYSTATE**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setdaystate)來明確設定日狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="157a1-118">An application can explicitly set day state information by sending the [**MCM\_SETDAYSTATE**](mcm-setdaystate.md) message or by using the corresponding macro, [**MonthCal\_SetDayState**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setdaystate).</span></span> <span data-ttu-id="157a1-119">但是，日期狀態資訊通常是為了回應 [MCN \_ GETDAYSTATE](mcn-getdaystate.md) 通知碼而設定的，這會在每次控制項需要重新整理時傳送，例如，每個月都已滾動查看。</span><span class="sxs-lookup"><span data-stu-id="157a1-119">However, day state information is usually set in response to the [MCN\_GETDAYSTATE](mcn-getdaystate.md) notification code, which is sent whenever the control needs to be refreshed because, for example, a different month has scrolled into view.</span></span>

<span data-ttu-id="157a1-120">下列範例程式碼示範如何在 [**WM \_ 通知**](wm-notify.md)訊息處理常式中處理 [MCN \_ GETDAYSTATE](mcn-getdaystate.md)通知程式碼。</span><span class="sxs-lookup"><span data-stu-id="157a1-120">The following example code shows how to process the [MCN\_GETDAYSTATE](mcn-getdaystate.md) notification code in a [**WM\_NOTIFY**](wm-notify.md) message handler.</span></span> <span data-ttu-id="157a1-121">它會 \_ 指定每個可見月份的第一天和第十五天應該反白顯示，以處理 MCN GETDAYSTATE。</span><span class="sxs-lookup"><span data-stu-id="157a1-121">It processes MCN\_GETDAYSTATE by specifying that the first and fifteenth day of each visible month should be highlighted.</span></span> <span data-ttu-id="157a1-122">[**NMDAYSTATE**](/windows/win32/api/commctrl/ns-commctrl-nmdaystate)結構的 **cDayState** 成員會指定陣列中所需的 [**MONTHDAYSTATE**](monthdaystate.md)值數目，其具有任意大小的上限。</span><span class="sxs-lookup"><span data-stu-id="157a1-122">The **cDayState** member of the [**NMDAYSTATE**](/windows/win32/api/commctrl/ns-commctrl-nmdaystate) structure specifies the number of [**MONTHDAYSTATE**](monthdaystate.md) values that are needed in the array, which is given an arbitrary maximum size.</span></span> <span data-ttu-id="157a1-123">然後，程式碼會使用應用程式定義的 **BOLDDAY** 宏，迴圈在陣列的每個有效元素中設定適當的位。</span><span class="sxs-lookup"><span data-stu-id="157a1-123">The code then loops to set the appropriate bits in each valid element of the array, using the application-defined **BOLDDAY** macro.</span></span>



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



## <a name="related-topics"></a><span data-ttu-id="157a1-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="157a1-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="157a1-125">月曆控制項參考</span><span class="sxs-lookup"><span data-stu-id="157a1-125">Month Calendar Control Reference</span></span>](bumper-month-calendar-month-calendar-control-reference.md)
</dt> <dt>

[<span data-ttu-id="157a1-126">關於 Month Calendar 控制項</span><span class="sxs-lookup"><span data-stu-id="157a1-126">About Month Calendar Controls</span></span>](month-calendar-controls.md)
</dt> <dt>

[<span data-ttu-id="157a1-127">使用月曆控制項</span><span class="sxs-lookup"><span data-stu-id="157a1-127">Using Month Calendar Controls</span></span>](using-month-calendar-controls.md)
</dt> </dl>

 

 





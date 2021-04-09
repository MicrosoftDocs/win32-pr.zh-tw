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
# <a name="how-to-process-the-dtn_datetimechange-notification"></a><span data-ttu-id="8def1-103">如何處理 DTN \_ DATETIMECHANGE 通知</span><span class="sxs-lookup"><span data-stu-id="8def1-103">How to Process the DTN\_DATETIMECHANGE Notification</span></span>

<span data-ttu-id="8def1-104">本主題示範如何將使用者所做的變更通知， (DTP) 控制項的日期和時間選擇器處理。</span><span class="sxs-lookup"><span data-stu-id="8def1-104">This topic demonstrates how to process notification of changes, made by the user, to the date and time picker (DTP) control.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="8def1-105">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="8def1-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="8def1-106">技術</span><span class="sxs-lookup"><span data-stu-id="8def1-106">Technologies</span></span>

-   [<span data-ttu-id="8def1-107">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="8def1-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="8def1-108">必要條件</span><span class="sxs-lookup"><span data-stu-id="8def1-108">Prerequisites</span></span>

-   <span data-ttu-id="8def1-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="8def1-109">C/C++</span></span>
-   <span data-ttu-id="8def1-110">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="8def1-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="8def1-111">指示</span><span class="sxs-lookup"><span data-stu-id="8def1-111">Instructions</span></span>


<span data-ttu-id="8def1-112">每當發生變更時，DTP 控制項會傳送 [DTN \_ DATETIMECHANGE](dtn-datetimechange.md) 通知程式碼。</span><span class="sxs-lookup"><span data-stu-id="8def1-112">A DTP control sends the [DTN\_DATETIMECHANGE](dtn-datetimechange.md) notification code whenever a change occurs.</span></span> <span data-ttu-id="8def1-113">例如，當使用者變更控制項中的其中一個欄位，或在控制項設定為 [**DTS \_ SHOWNONE**](date-and-time-picker-control-styles.md) 樣式的情況下，當使用者變更控制項核取方塊的狀態時，就會產生這項通知。</span><span class="sxs-lookup"><span data-stu-id="8def1-113">For example, this notification will be generated when the user changes one of the fields in the control or, in the case where the control is set to the [**DTS\_SHOWNONE**](date-and-time-picker-control-styles.md) style, when the user changes the state of the control's check box.</span></span>

<span data-ttu-id="8def1-114">您的應用程式必須包含程式碼，以處理 \_ 由 DTP 控制項所傳送的 DTN DATETIMECHANGE 訊息。</span><span class="sxs-lookup"><span data-stu-id="8def1-114">Your application must include code to process DTN\_DATETIMECHANGE messages that are sent by the DTP control.</span></span>

<span data-ttu-id="8def1-115">下列 c + + 程式碼範例是應用程式定義的函式，設計來指出設定為 **DTS \_ SHOWNONE** 樣式之 DTP 控制項的狀態。</span><span class="sxs-lookup"><span data-stu-id="8def1-115">The following C++ code example is an application-defined function designed to indicate the state of a DTP control that is set to the **DTS\_SHOWNONE** style.</span></span>



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



## <a name="related-topics"></a><span data-ttu-id="8def1-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="8def1-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8def1-117">使用日期時間選擇器控制項</span><span class="sxs-lookup"><span data-stu-id="8def1-117">Using Date and Time Picker Controls</span></span>](using-date-and-time-picker.md)
</dt> <dt>

[<span data-ttu-id="8def1-118">日期和時間選擇器控制項參考</span><span class="sxs-lookup"><span data-stu-id="8def1-118">Date and Time Picker Control Reference</span></span>](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[<span data-ttu-id="8def1-119">日期和時間選擇器</span><span class="sxs-lookup"><span data-stu-id="8def1-119">Date and Time Picker</span></span>](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 





---
description: 錯誤對話方塊是顯示錯誤訊息的強制回應對話方塊。 每個安裝中都可以存在一個以上的錯誤對話方塊。
ms.assetid: 11d4fe8b-ec5f-4576-95e5-c86344f0195c
title: 錯誤對話方塊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a153f5e6ee38235f830937d794a9ca9b81314583
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512161"
---
# <a name="error-dialog"></a><span data-ttu-id="6728b-104">錯誤對話方塊</span><span class="sxs-lookup"><span data-stu-id="6728b-104">Error Dialog</span></span>

<span data-ttu-id="6728b-105">錯誤對話方塊是顯示錯誤訊息的強制回應對話方塊。</span><span class="sxs-lookup"><span data-stu-id="6728b-105">An Error dialog box is a modal dialog box box that displays an error message.</span></span> <span data-ttu-id="6728b-106">每個安裝中都可以存在一個以上的錯誤對話方塊。</span><span class="sxs-lookup"><span data-stu-id="6728b-106">More than one Error dialog box can exist in each installation.</span></span>

<span data-ttu-id="6728b-107">必須設定 ErrorDialog 屬性，以指定要使用哪一個對話方塊。</span><span class="sxs-lookup"><span data-stu-id="6728b-107">An ErrorDialog property needs to be set that specifies which dialog box is to be used.</span></span> <span data-ttu-id="6728b-108">如果未設定此屬性，或未指向有效的錯誤對話方塊，則不會顯示錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="6728b-108">If this property is not set or does not point to a valid Error dialog box, then the error messages will not be displayed.</span></span> <span data-ttu-id="6728b-109">在此情況下，只會記錄錯誤，並出現關於遺漏對話方塊的警告。</span><span class="sxs-lookup"><span data-stu-id="6728b-109">In this case, the error is only logged with a warning about the missing dialog box.</span></span>

<span data-ttu-id="6728b-110">錯誤對話方塊必須設定 [錯誤對話方塊樣式位](error-dialog-style-bit.md) 。</span><span class="sxs-lookup"><span data-stu-id="6728b-110">An Error dialog box must have the [Error Dialog style bit](error-dialog-style-bit.md) set.</span></span> <span data-ttu-id="6728b-111">對話方塊必須有一個名為 ErrorText 的 [文字控制項](text-control.md) 。</span><span class="sxs-lookup"><span data-stu-id="6728b-111">The dialog box must have a [Text control](text-control.md) named ErrorText.</span></span> <span data-ttu-id="6728b-112">[對話方塊資料表](dialog-table.md)中錯誤對話方塊的記錄必須在控制項的第一個欄位中輸入 ErrorText 控制項 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6728b-112">The record for the Error dialog box in the [Dialog table](dialog-table.md) must have the ErrorText control entered into the Control\_First field.</span></span>

<span data-ttu-id="6728b-113">對話方塊必須包含七個 [按鈕](pushbutton-control.md)。</span><span class="sxs-lookup"><span data-stu-id="6728b-113">The dialog box must contain seven [PushButtons](pushbutton-control.md).</span></span> <span data-ttu-id="6728b-114">所有這些按鈕會在[ControlEvent 資料表](controlevent-table.md)中指定[EndDialog](enddialog-controlevent.md) ControlEvent。</span><span class="sxs-lookup"><span data-stu-id="6728b-114">All of these buttons specify the [EndDialog](enddialog-controlevent.md) ControlEvent in the [ControlEvent table](controlevent-table.md).</span></span> <span data-ttu-id="6728b-115">每個按鈕都會指定下列其中一個屬性： **ErrorAbort**、 **ErrorCancel**、 **ErrorIgnore**、 **ErrorNo**、 **ErrorOk**、 **ErrorRetry**、 **ErrorYes**。</span><span class="sxs-lookup"><span data-stu-id="6728b-115">Each button specifies one of the following attributes: **ErrorAbort**, **ErrorCancel**, **ErrorIgnore**, **ErrorNo**, **ErrorOk**, **ErrorRetry**, **ErrorYes**.</span></span>

> [!Note]  
> <span data-ttu-id="6728b-116">這些控制項的焦點不應透過使用 \_ [控制資料表](control-table.md)中的 [下一步] 資料行來連結。</span><span class="sxs-lookup"><span data-stu-id="6728b-116">The focus of these controls should not be linked through the use of the Control\_Next column in the [Control table](control-table.md).</span></span>

 

<span data-ttu-id="6728b-117">這些按鈕的位置應該與對話方塊中的位置大致相同，因為當建立時，根據訊息而定，只會建立這七個按鈕的子集。</span><span class="sxs-lookup"><span data-stu-id="6728b-117">These buttons should be placed in approximately the same position in the dialog box because when it is created, only a subset of these seven buttons is created, depending on the message.</span></span> <span data-ttu-id="6728b-118">按鈕的 X 座標會進行修改，因此顯示的按鈕會平均間距。</span><span class="sxs-lookup"><span data-stu-id="6728b-118">The X coordinate of the buttons is modified so the buttons that are displayed are evenly spaced.</span></span> <span data-ttu-id="6728b-119">按鈕的 Y 座標、高度和寬度都不會變更。</span><span class="sxs-lookup"><span data-stu-id="6728b-119">The Y coordinate, height, and width of the buttons are unchanged.</span></span> <span data-ttu-id="6728b-120">因為按鈕會水準排列，所以不能將其他控制項放在對話方塊的相同水準區域中。</span><span class="sxs-lookup"><span data-stu-id="6728b-120">Because the buttons are arranged horizontally, no other control can be placed in the same horizontal region of the dialog box.</span></span>

<span data-ttu-id="6728b-121">針對錯誤對話方塊， \_ 會忽略對話方塊資料表中的 [控制項預設值] 和 [控制項 \_ 取消 []](dialog-table.md) 欄位。</span><span class="sxs-lookup"><span data-stu-id="6728b-121">For an Error dialog box, the Control\_Default and Control\_Cancel fields in the [Dialog table](dialog-table.md) are ignored.</span></span> <span data-ttu-id="6728b-122">\_錯誤對話方塊的控制項第一個欄位必須指定 ErrorText 控制項。</span><span class="sxs-lookup"><span data-stu-id="6728b-122">The Control\_First field for an Error dialog box must specify the ErrorText control.</span></span>

<span data-ttu-id="6728b-123">如果此對話方塊中包含名為 ErrorIcon 的 [圖示控制項](icon-control.md) ，則會顯示下列標準 Windows 圖示：</span><span class="sxs-lookup"><span data-stu-id="6728b-123">If an [Icon control](icon-control.md) named ErrorIcon is included on this dialog, the following standard Windows icons are displayed:</span></span>

-   <span data-ttu-id="6728b-124">IDI \_ 錯誤，以回應 imtFatalExit 訊息。</span><span class="sxs-lookup"><span data-stu-id="6728b-124">IDI\_ERROR in response to imtFatalExit messages.</span></span>
-   <span data-ttu-id="6728b-125">IDI \_ 警告以回應 imtError 和 imtWarning 訊息。</span><span class="sxs-lookup"><span data-stu-id="6728b-125">IDI\_WARNING in response to imtError and imtWarning messages.</span></span>
-   <span data-ttu-id="6728b-126">IDI \_ 資訊以回應 imtOutOfDiskSpace 訊息。</span><span class="sxs-lookup"><span data-stu-id="6728b-126">IDI\_INFORMATION in response to imtOutOfDiskSpace messages.</span></span>

<span data-ttu-id="6728b-127">應建立 ErrorIcon 控制項，並設定 [FixedSize control 屬性](fixedsize-control-attribute.md) ，以避免標準 Windows 圖示的大小不適當。</span><span class="sxs-lookup"><span data-stu-id="6728b-127">The ErrorIcon control should be created with the [FixedSize control attribute](fixedsize-control-attribute.md) set to avoid improper sizing of the standard Windows icons.</span></span>

 

 




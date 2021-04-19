---
description: 如果設定此位，對話方塊會是錯誤對話方塊。
ms.assetid: a8a95f6a-6465-433b-98a4-95281cddedd3
title: 錯誤對話方塊樣式位
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0ff3e4868cf1941f80be4f7b2d70068ec949a4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974323"
---
# <a name="error-dialog-style-bit"></a><span data-ttu-id="da8e6-103">錯誤對話方塊樣式位</span><span class="sxs-lookup"><span data-stu-id="da8e6-103">Error Dialog Style Bit</span></span>

<span data-ttu-id="da8e6-104">如果設定此位，對話方塊會是錯誤對話方塊。</span><span class="sxs-lookup"><span data-stu-id="da8e6-104">If this bit is set, the dialog box is an error dialog.</span></span>

<span data-ttu-id="da8e6-105">可以有一個以上的對話方塊具有這個樣式。</span><span class="sxs-lookup"><span data-stu-id="da8e6-105">There can be more than one dialog with this style.</span></span> <span data-ttu-id="da8e6-106">**ErrorDialog** 屬性會決定要使用哪一個對話方塊做為錯誤對話方塊。</span><span class="sxs-lookup"><span data-stu-id="da8e6-106">The **ErrorDialog** property determines which dialog is used as an error dialog.</span></span> <span data-ttu-id="da8e6-107">選取的對話只能是已設定此樣式位的對話方塊之一。</span><span class="sxs-lookup"><span data-stu-id="da8e6-107">The selected dialog can be only one of those that have this style bit set.</span></span> <span data-ttu-id="da8e6-108">錯誤對話方塊必須有一個名為 ErrorText 的靜態文字控制項。</span><span class="sxs-lookup"><span data-stu-id="da8e6-108">The error dialog must have a static text control named ErrorText.</span></span> <span data-ttu-id="da8e6-109">此控制項會接收錯誤訊息的文字。</span><span class="sxs-lookup"><span data-stu-id="da8e6-109">This control receives the text of the error message.</span></span> <span data-ttu-id="da8e6-110">對話方塊也應該具有對應至可能傳回值的七個推播按鈕。</span><span class="sxs-lookup"><span data-stu-id="da8e6-110">The dialog should also have the seven push buttons corresponding to the possible return values.</span></span> <span data-ttu-id="da8e6-111">錯誤訊息會決定實際顯示的按鈕。</span><span class="sxs-lookup"><span data-stu-id="da8e6-111">The error message determines which of these buttons are actually displayed.</span></span> <span data-ttu-id="da8e6-112">顯示的按鈕會重新排列，因此會平均地分散在對話方塊上。</span><span class="sxs-lookup"><span data-stu-id="da8e6-112">The displayed buttons are rearranged so they are evenly distributed on the dialog.</span></span> <span data-ttu-id="da8e6-113">此重新排列會變更按鈕的 X 座標，但不會變更其他三個座標。</span><span class="sxs-lookup"><span data-stu-id="da8e6-113">This rearrangement changes the X coordinate of the buttons, but not the other three coordinates.</span></span> <span data-ttu-id="da8e6-114">因此，建議您不要在對話方塊的相同水準區域中撰寫其他控制項做為按鈕。</span><span class="sxs-lookup"><span data-stu-id="da8e6-114">Therefore it is advisable that no other control should be authored in the same horizontal region of the dialog as the buttons.</span></span> <span data-ttu-id="da8e6-115">如果錯誤訊息未指定按鈕，則會顯示 [ **確定]** 按鈕。</span><span class="sxs-lookup"><span data-stu-id="da8e6-115">If the error message specifies no button, the **OK** button is displayed.</span></span> <span data-ttu-id="da8e6-116">[錯誤] 對話方塊會忽略 [ **預設** ] 按鈕、[第一個使用中控制項] 和 [ **取消** ] 按鈕的值。</span><span class="sxs-lookup"><span data-stu-id="da8e6-116">The **Default** button, First active control and **Cancel** button values are ignored for an error dialog.</span></span> <span data-ttu-id="da8e6-117">錯誤訊息中定義的 **預設** 按鈕將會指派給這三個值。</span><span class="sxs-lookup"><span data-stu-id="da8e6-117">The **Default** button defined in the error message will be assigned to all three values.</span></span> <span data-ttu-id="da8e6-118">推送這些按鈕的效果必須在 [ControlEvent 資料表](controlevent-table.md) 中定義，就像所有其他按鈕一樣。</span><span class="sxs-lookup"><span data-stu-id="da8e6-118">The effect of pushing these buttons have to be defined in the [ControlEvent table](controlevent-table.md) just like for all other buttons.</span></span> <span data-ttu-id="da8e6-119">對話方塊的標題會以類似于其他對話的方式來撰寫。</span><span class="sxs-lookup"><span data-stu-id="da8e6-119">The title of the dialog is authored in a way similar to other dialogs.</span></span> <span data-ttu-id="da8e6-120">如果錯誤訊息指定了按鈕清單之後的標頭文字，就會覆寫它。</span><span class="sxs-lookup"><span data-stu-id="da8e6-120">It can get overwritten by the error message if it specifies a header text after the button list.</span></span>

## <a name="value"></a><span data-ttu-id="da8e6-121">值</span><span class="sxs-lookup"><span data-stu-id="da8e6-121">Value</span></span>



| <span data-ttu-id="da8e6-122">Decimal</span><span class="sxs-lookup"><span data-stu-id="da8e6-122">Decimal</span></span> | <span data-ttu-id="da8e6-123">十六進位</span><span class="sxs-lookup"><span data-stu-id="da8e6-123">Hexadecimal</span></span> | <span data-ttu-id="da8e6-124">常數</span><span class="sxs-lookup"><span data-stu-id="da8e6-124">Constant</span></span>                       |
|---------|-------------|--------------------------------|
| <span data-ttu-id="da8e6-125">65536</span><span class="sxs-lookup"><span data-stu-id="da8e6-125">65536</span></span>   | <span data-ttu-id="da8e6-126">0x00010000</span><span class="sxs-lookup"><span data-stu-id="da8e6-126">0x00010000</span></span>  | <span data-ttu-id="da8e6-127">**msidbDialogAttributesError**</span><span class="sxs-lookup"><span data-stu-id="da8e6-127">**msidbDialogAttributesError**</span></span> |



 

 

 




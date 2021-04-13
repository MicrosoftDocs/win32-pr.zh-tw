---
title: 'DL_DRAGGING (Commctrl 的通知碼) '
description: 指出使用者在拖曳專案時移動滑鼠的信號。
ms.assetid: 87fc4c24-8e88-4e3c-8f54-ecc7f80de5d7
keywords:
- DL_DRAGGING 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- DL_DRAGGING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f5c9f3f6cec3ef95745eed88ec0208dff581ada
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509496"
---
# <a name="dl_dragging-notification-code"></a><span data-ttu-id="f10bd-104">DL \_ 拖曳通知碼</span><span class="sxs-lookup"><span data-stu-id="f10bd-104">DL\_DRAGGING notification code</span></span>

<span data-ttu-id="f10bd-105">指出使用者在拖曳專案時移動滑鼠的信號。</span><span class="sxs-lookup"><span data-stu-id="f10bd-105">Signals that the user has moved the mouse while dragging an item.</span></span> <span data-ttu-id="f10bd-106">\_即使滑鼠未移動，也會在拖曳期間定期傳送 DL 拖曳。</span><span class="sxs-lookup"><span data-stu-id="f10bd-106">DL\_DRAGGING is also sent periodically during dragging even if the mouse is not moved.</span></span> <span data-ttu-id="f10bd-107">拖曳清單方塊會將此通知碼以拖曳清單訊息的形式傳送至其父視窗。</span><span class="sxs-lookup"><span data-stu-id="f10bd-107">A drag list box sends this notification code to its parent window in the form of a drag list message.</span></span> <span data-ttu-id="f10bd-108">如需詳細資訊，請參閱 [拖曳清單方塊訊息](about-list-boxes.md)。</span><span class="sxs-lookup"><span data-stu-id="f10bd-108">For more information, see [Drag List Box Messages](about-list-boxes.md).</span></span>


```C++
DL_DRAGGING

    pDragInfo = (LPARAM)(LPDRAGLISTINFO) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="f10bd-109">參數</span><span class="sxs-lookup"><span data-stu-id="f10bd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f10bd-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f10bd-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f10bd-111">拖曳清單方塊的控制項識別碼。</span><span class="sxs-lookup"><span data-stu-id="f10bd-111">The control identifier of the drag list box.</span></span>

</dd> <dt>

<span data-ttu-id="f10bd-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f10bd-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f10bd-113">[**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo)結構的指標，其中包含 DL \_ 拖曳通知碼、拖曳清單方塊的控制碼，以及游標位置。</span><span class="sxs-lookup"><span data-stu-id="f10bd-113">A pointer to a [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) structure that contains the DL\_DRAGGING notification code, the handle to the drag list box, and the cursor position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f10bd-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="f10bd-114">Return value</span></span>

<span data-ttu-id="f10bd-115">傳回值決定拖曳清單應設定的滑鼠游標類型;它可以是 DL \_ STOPCURSOR、dl \_ COPYCURSOR 或 dl \_ MOVECURSOR 值。</span><span class="sxs-lookup"><span data-stu-id="f10bd-115">The return value determines the type of mouse cursor that the drag list should set; it can be the DL\_STOPCURSOR, DL\_COPYCURSOR, or DL\_MOVECURSOR value.</span></span> <span data-ttu-id="f10bd-116">如果傳回任何其他值，則不會變更資料指標。</span><span class="sxs-lookup"><span data-stu-id="f10bd-116">If any other value is returned, the cursor does not change.</span></span>

## <a name="remarks"></a><span data-ttu-id="f10bd-117">備註</span><span class="sxs-lookup"><span data-stu-id="f10bd-117">Remarks</span></span>

<span data-ttu-id="f10bd-118">視窗程式通常會藉 \_ 由判斷游標下的專案，然後繪製插入圖示，來處理 DL 拖曳通知程式碼。</span><span class="sxs-lookup"><span data-stu-id="f10bd-118">A window procedure typically processes the DL\_DRAGGING notification code by determining the item under the cursor and then drawing an insert icon.</span></span> <span data-ttu-id="f10bd-119">若要取得資料指標下的專案，請使用 [**LBItemFromPt**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt)函式，針對 *BAutoScroll* 參數指定 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="f10bd-119">To retrieve the item under the cursor, use the [**LBItemFromPt**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) function, specifying **TRUE** for the *bAutoScroll* parameter.</span></span> <span data-ttu-id="f10bd-120">如果游標位於其工作區的上方或下方，此選項會讓拖曳清單方塊定期滾動。</span><span class="sxs-lookup"><span data-stu-id="f10bd-120">This option causes the drag list box to scroll periodically if the cursor is above or below its client area.</span></span> <span data-ttu-id="f10bd-121">若要繪製插入圖示，請使用 [**DrawInsert**](/windows/desktop/api/Commctrl/nf-commctrl-drawinsert) 函數。</span><span class="sxs-lookup"><span data-stu-id="f10bd-121">To draw the insert icon, use the [**DrawInsert**](/windows/desktop/api/Commctrl/nf-commctrl-drawinsert) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="f10bd-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="f10bd-122">Requirements</span></span>



| <span data-ttu-id="f10bd-123">需求</span><span class="sxs-lookup"><span data-stu-id="f10bd-123">Requirement</span></span> | <span data-ttu-id="f10bd-124">值</span><span class="sxs-lookup"><span data-stu-id="f10bd-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f10bd-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f10bd-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f10bd-126">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f10bd-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f10bd-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f10bd-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f10bd-128">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f10bd-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f10bd-129">標頭</span><span class="sxs-lookup"><span data-stu-id="f10bd-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="f10bd-130"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="f10bd-130"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






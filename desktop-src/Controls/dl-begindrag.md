---
title: 'DL_BEGINDRAG (Commctrl 的通知碼) '
description: 通知拖曳清單方塊的父視窗，指出使用者已按下某個專案的滑鼠左鍵。 拖曳清單方塊會以拖曳清單訊息的形式傳送此通知碼。 如需詳細資訊，請參閱拖曳清單方塊訊息。
ms.assetid: ccf66818-e5f7-4165-8d0d-4d279944f70e
keywords:
- DL_BEGINDRAG 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- DL_BEGINDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f2d3ee211641c5b5e02482f914145fdf2e119f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844495"
---
# <a name="dl_begindrag-notification-code"></a><span data-ttu-id="95b56-106">DL \_ BEGINDRAG 通知碼</span><span class="sxs-lookup"><span data-stu-id="95b56-106">DL\_BEGINDRAG notification code</span></span>

<span data-ttu-id="95b56-107">通知拖曳清單方塊的父視窗，指出使用者已按下某個專案的滑鼠左鍵。</span><span class="sxs-lookup"><span data-stu-id="95b56-107">Notifies the drag list box's parent window that the user has clicked the left mouse button on an item.</span></span> <span data-ttu-id="95b56-108">拖曳清單方塊會以拖曳清單訊息的形式傳送此通知碼。</span><span class="sxs-lookup"><span data-stu-id="95b56-108">A drag list box sends this notification code in the form of a drag list message.</span></span> <span data-ttu-id="95b56-109">如需詳細資訊，請參閱 [拖曳清單方塊訊息](about-list-boxes.md)。</span><span class="sxs-lookup"><span data-stu-id="95b56-109">For more information, see [Drag List Box Messages](about-list-boxes.md).</span></span>


```C++
DL_BEGINDRAG

    pDragInfo = (LPARAM)(LPDRAGLISTINFO) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="95b56-110">參數</span><span class="sxs-lookup"><span data-stu-id="95b56-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95b56-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="95b56-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="95b56-112">[**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo)結構的指標，其中包含 DL \_ BEGINDRAG 通知碼、拖曳清單方塊的控制碼，以及游標位置。</span><span class="sxs-lookup"><span data-stu-id="95b56-112">A pointer to a [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) structure that contains the DL\_BEGINDRAG notification code, the handle to the drag list box, and the cursor position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95b56-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="95b56-113">Return value</span></span>

<span data-ttu-id="95b56-114">傳回 **TRUE** 以開始拖曳作業，或傳回 **FALSE** 以防止拖曳作業。</span><span class="sxs-lookup"><span data-stu-id="95b56-114">Return **TRUE** to begin the drag operation, or **FALSE** to prevent the drag operation.</span></span>

## <a name="remarks"></a><span data-ttu-id="95b56-115">備註</span><span class="sxs-lookup"><span data-stu-id="95b56-115">Remarks</span></span>

<span data-ttu-id="95b56-116">處理此通知程式碼時，視窗程式通常會使用 [**LBItemFromPt**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) 函數來判斷指定之資料指標位置的清單專案。</span><span class="sxs-lookup"><span data-stu-id="95b56-116">When processing this notification code, a window procedure typically determines the list item at the specified cursor position by using the [**LBItemFromPt**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) function.</span></span> <span data-ttu-id="95b56-117">然後，它會傳回 **TRUE** 或 **FALSE**，取決於是否應該拖曳專案。</span><span class="sxs-lookup"><span data-stu-id="95b56-117">It then returns **TRUE** or **FALSE**, depending on whether the item should be dragged.</span></span> <span data-ttu-id="95b56-118">在傳回 **TRUE** 之前，視窗程式應儲存清單專案的索引，讓應用程式知道拖曳作業完成時要移動或複製的專案。</span><span class="sxs-lookup"><span data-stu-id="95b56-118">Before returning **TRUE**, the window procedure should save the index of the list item so the application knows which item to move or copy when the drag operation is completed.</span></span>

## <a name="requirements"></a><span data-ttu-id="95b56-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="95b56-119">Requirements</span></span>



| <span data-ttu-id="95b56-120">需求</span><span class="sxs-lookup"><span data-stu-id="95b56-120">Requirement</span></span> | <span data-ttu-id="95b56-121">值</span><span class="sxs-lookup"><span data-stu-id="95b56-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="95b56-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="95b56-122">Minimum supported client</span></span><br/> | <span data-ttu-id="95b56-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="95b56-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="95b56-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="95b56-124">Minimum supported server</span></span><br/> | <span data-ttu-id="95b56-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="95b56-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="95b56-126">標頭</span><span class="sxs-lookup"><span data-stu-id="95b56-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="95b56-127"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="95b56-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






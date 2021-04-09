---
title: 'DL_DROPPED (Commctrl 的通知碼) '
description: 透過放開滑鼠左鍵，表示使用者已完成拖曳操作。 拖曳清單方塊會將此通知碼以拖曳清單訊息的形式傳送至其父視窗。 如需詳細資訊，請參閱拖曳清單方塊訊息。
ms.assetid: 81b9b424-2735-407d-bac9-f03ea2f48b4e
keywords:
- DL_DROPPED 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- DL_DROPPED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1b2480360ea38a00c4dd8efe6eb84eed8999890
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844496"
---
# <a name="dl_dropped-notification-code"></a><span data-ttu-id="5f8d7-106">DL 已卸載 \_ 通知碼</span><span class="sxs-lookup"><span data-stu-id="5f8d7-106">DL\_DROPPED notification code</span></span>

<span data-ttu-id="5f8d7-107">透過放開滑鼠左鍵，表示使用者已完成拖曳操作。</span><span class="sxs-lookup"><span data-stu-id="5f8d7-107">Signals that the user has completed a drag operation by releasing the left mouse button.</span></span> <span data-ttu-id="5f8d7-108">拖曳清單方塊會將此通知碼以拖曳清單訊息的形式傳送至其父視窗。</span><span class="sxs-lookup"><span data-stu-id="5f8d7-108">A drag list box sends this notification code to its parent window in the form of a drag list message.</span></span> <span data-ttu-id="5f8d7-109">如需詳細資訊，請參閱 [拖曳清單方塊訊息](about-list-boxes.md)。</span><span class="sxs-lookup"><span data-stu-id="5f8d7-109">For more information, see [Drag List Box Messages](about-list-boxes.md).</span></span>


```C++
DL_DROPPED

    pDragInfo = (LPARAM)(LPDRAGLISTINFO) lParam;
```



## <a name="parameters"></a><span data-ttu-id="5f8d7-110">參數</span><span class="sxs-lookup"><span data-stu-id="5f8d7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f8d7-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5f8d7-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5f8d7-112">[**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo)結構的指標，其中包含 DL 卸載的 \_ 通知碼、拖曳清單方塊的控制碼，以及游標位置。</span><span class="sxs-lookup"><span data-stu-id="5f8d7-112">A pointer to a [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) structure that contains the DL\_DROPPED notification code, the handle to the drag list box, and the cursor position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f8d7-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="5f8d7-113">Return value</span></span>

<span data-ttu-id="5f8d7-114">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="5f8d7-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f8d7-115">備註</span><span class="sxs-lookup"><span data-stu-id="5f8d7-115">Remarks</span></span>

<span data-ttu-id="5f8d7-116">通常會藉由將拖曳的專案插入至游標下專案前面的清單來處理此通知碼。</span><span class="sxs-lookup"><span data-stu-id="5f8d7-116">This notification code is normally processed by inserting the item being dragged into the list in front of the item under the cursor.</span></span> <span data-ttu-id="5f8d7-117">若要在游標位置取出專案的索引，請使用 [**LBItemFromPt**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) 函數。</span><span class="sxs-lookup"><span data-stu-id="5f8d7-117">To retrieve the index of the item at the cursor position, use the [**LBItemFromPt**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) function.</span></span> <span data-ttu-id="5f8d7-118">請注意， \_ 即使資料指標不在清單專案上，仍會傳送 DL 捨棄的通知碼。</span><span class="sxs-lookup"><span data-stu-id="5f8d7-118">Note that the DL\_DROPPED notification code is sent even if the cursor is not on a list item.</span></span> <span data-ttu-id="5f8d7-119">在此情況下， **LBItemFromPt** 會傳回-1。</span><span class="sxs-lookup"><span data-stu-id="5f8d7-119">In that case, **LBItemFromPt** returns -1.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f8d7-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="5f8d7-120">Requirements</span></span>



| <span data-ttu-id="5f8d7-121">需求</span><span class="sxs-lookup"><span data-stu-id="5f8d7-121">Requirement</span></span> | <span data-ttu-id="5f8d7-122">值</span><span class="sxs-lookup"><span data-stu-id="5f8d7-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5f8d7-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5f8d7-123">Minimum supported client</span></span><br/> | <span data-ttu-id="5f8d7-124">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5f8d7-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5f8d7-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5f8d7-125">Minimum supported server</span></span><br/> | <span data-ttu-id="5f8d7-126">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5f8d7-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5f8d7-127">標頭</span><span class="sxs-lookup"><span data-stu-id="5f8d7-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f8d7-128"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="5f8d7-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






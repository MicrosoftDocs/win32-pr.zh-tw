---
title: 'LVM_GETITEMSTATE 訊息 (Commctrl .h) '
description: 抓取清單視圖專案的狀態。 您可以明確地傳送此訊息，或使用 ListView \_ GetItemState 宏來傳送。
ms.assetid: 862960ed-a64a-4d66-b384-9228932eae6f
keywords:
- LVM_GETITEMSTATE message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETITEMSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 817b355e78f22c01c289f681d256ee6b4d0aa882
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466509"
---
# <a name="lvm_getitemstate-message"></a><span data-ttu-id="bb0ab-105">LVM \_ GETITEMSTATE 訊息</span><span class="sxs-lookup"><span data-stu-id="bb0ab-105">LVM\_GETITEMSTATE message</span></span>

<span data-ttu-id="bb0ab-106">抓取清單視圖專案的狀態。</span><span class="sxs-lookup"><span data-stu-id="bb0ab-106">Retrieves the state of a list-view item.</span></span> <span data-ttu-id="bb0ab-107">您可以明確地傳送此訊息，或使用 [**ListView \_ GetItemState**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemstate) 宏來傳送。</span><span class="sxs-lookup"><span data-stu-id="bb0ab-107">You can send this message explicitly or by using the [**ListView\_GetItemState**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemstate) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="bb0ab-108">參數</span><span class="sxs-lookup"><span data-stu-id="bb0ab-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb0ab-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bb0ab-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bb0ab-110">清單視圖專案的索引。</span><span class="sxs-lookup"><span data-stu-id="bb0ab-110">Index of the list-view item.</span></span>

</dd> <dt>

<span data-ttu-id="bb0ab-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bb0ab-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bb0ab-112">要取出的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="bb0ab-112">State information to retrieve.</span></span> <span data-ttu-id="bb0ab-113">這個參數可以是下列值的組合：</span><span class="sxs-lookup"><span data-stu-id="bb0ab-113">This parameter can be a combination of the following values:</span></span>



| <span data-ttu-id="bb0ab-114">值</span><span class="sxs-lookup"><span data-stu-id="bb0ab-114">Value</span></span>                                                                                                                                                                           | <span data-ttu-id="bb0ab-115">意義</span><span class="sxs-lookup"><span data-stu-id="bb0ab-115">Meaning</span></span>                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LVIS_CUT"></span><span id="lvis_cut"></span><dl> <span data-ttu-id="bb0ab-116"><dt>**LVIS \_ 剪下**</dt></span><span class="sxs-lookup"><span data-stu-id="bb0ab-116"><dt>**LVIS\_CUT**</dt></span></span> </dl>                                  | <span data-ttu-id="bb0ab-117">：項目已標記為進行剪貼作業。</span><span class="sxs-lookup"><span data-stu-id="bb0ab-117">The item is marked for a cut-and-paste operation.</span></span><br/>                                                                                                         |
| <span id="LVIS_DROPHILITED"></span><span id="lvis_drophilited"></span><dl> <span data-ttu-id="bb0ab-118"><dt>**LVIS \_ DROPHILITED**</dt></span><span class="sxs-lookup"><span data-stu-id="bb0ab-118"><dt>**LVIS\_DROPHILITED**</dt></span></span> </dl>          | <span data-ttu-id="bb0ab-119">：項目會隨著拖放目標而反白顯示。</span><span class="sxs-lookup"><span data-stu-id="bb0ab-119">The item is highlighted as a drag-and-drop target.</span></span><br/>                                                                                                        |
| <span id="LVIS_FOCUSED"></span><span id="lvis_focused"></span><dl> <span data-ttu-id="bb0ab-120"><dt>**LVIS \_ 焦點**</dt></span><span class="sxs-lookup"><span data-stu-id="bb0ab-120"><dt>**LVIS\_FOCUSED**</dt></span></span> </dl>                      | <span data-ttu-id="bb0ab-121">專案具有焦點，因此會以標準焦點矩形括住。</span><span class="sxs-lookup"><span data-stu-id="bb0ab-121">The item has the focus, so it is surrounded by a standard focus rectangle.</span></span> <span data-ttu-id="bb0ab-122">雖然可以選取一個以上的專案，但只有一個專案可以有焦點。</span><span class="sxs-lookup"><span data-stu-id="bb0ab-122">Although more than one item may be selected, only one item can have the focus.</span></span><br/> |
| <span id="LVIS_SELECTED"></span><span id="lvis_selected"></span><dl> <span data-ttu-id="bb0ab-123"><dt>**LVIS 已 \_ 選取**</dt></span><span class="sxs-lookup"><span data-stu-id="bb0ab-123"><dt>**LVIS\_SELECTED**</dt></span></span> </dl>                   | <span data-ttu-id="bb0ab-124">這個項目已選取。</span><span class="sxs-lookup"><span data-stu-id="bb0ab-124">The item is selected.</span></span> <span data-ttu-id="bb0ab-125">選取專案的外觀取決於它是否具有焦點，也會顯示用於選取的系統色彩。</span><span class="sxs-lookup"><span data-stu-id="bb0ab-125">The appearance of a selected item depends on whether it has the focus and also on the system colors used for selection.</span></span><br/>             |
| <span id="LVIS_OVERLAYMASK"></span><span id="lvis_overlaymask"></span><dl> <span data-ttu-id="bb0ab-126"><dt>**LVIS \_ OVERLAYMASK**</dt></span><span class="sxs-lookup"><span data-stu-id="bb0ab-126"><dt>**LVIS\_OVERLAYMASK**</dt></span></span> </dl>          | <span data-ttu-id="bb0ab-127">使用此遮罩來抓取專案的重迭影像索引。</span><span class="sxs-lookup"><span data-stu-id="bb0ab-127">Use this mask to retrieve the item's overlay image index.</span></span><br/>                                                                                                 |
| <span id="LVIS_STATEIMAGEMASK"></span><span id="lvis_stateimagemask"></span><dl> <span data-ttu-id="bb0ab-128"><dt>**LVIS \_ STATEIMAGEMASK**</dt></span><span class="sxs-lookup"><span data-stu-id="bb0ab-128"><dt>**LVIS\_STATEIMAGEMASK**</dt></span></span> </dl> | <span data-ttu-id="bb0ab-129">使用此遮罩來取得專案的狀態影像索引。</span><span class="sxs-lookup"><span data-stu-id="bb0ab-129">Use this mask to retrieve the item's state image index.</span></span><br/>                                                                                                   |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb0ab-130">傳回值</span><span class="sxs-lookup"><span data-stu-id="bb0ab-130">Return value</span></span>

<span data-ttu-id="bb0ab-131">傳回指定之專案的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="bb0ab-131">Returns the current state for the specified item.</span></span> <span data-ttu-id="bb0ab-132">傳回值中唯一有效的位是對應至 *lParam* 參數中所設定之位的有效位。</span><span class="sxs-lookup"><span data-stu-id="bb0ab-132">The only valid bits in the return value are those that correspond to the bits set in the *lParam* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb0ab-133">備註</span><span class="sxs-lookup"><span data-stu-id="bb0ab-133">Remarks</span></span>

<span data-ttu-id="bb0ab-134">專案的狀態資訊包含一組位旗標，以及表示專案狀態影像和重迭影像的影像清單索引。</span><span class="sxs-lookup"><span data-stu-id="bb0ab-134">An item's state information includes a set of bit flags as well as image list indexes that indicate the item's state image and overlay image.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb0ab-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="bb0ab-135">Requirements</span></span>



| <span data-ttu-id="bb0ab-136">需求</span><span class="sxs-lookup"><span data-stu-id="bb0ab-136">Requirement</span></span> | <span data-ttu-id="bb0ab-137">值</span><span class="sxs-lookup"><span data-stu-id="bb0ab-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bb0ab-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bb0ab-138">Minimum supported client</span></span><br/> | <span data-ttu-id="bb0ab-139">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bb0ab-139">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bb0ab-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bb0ab-140">Minimum supported server</span></span><br/> | <span data-ttu-id="bb0ab-141">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bb0ab-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bb0ab-142">標頭</span><span class="sxs-lookup"><span data-stu-id="bb0ab-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb0ab-143"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="bb0ab-143"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb0ab-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bb0ab-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb0ab-145">**LVM \_ SETITEMSTATE**</span><span class="sxs-lookup"><span data-stu-id="bb0ab-145">**LVM\_SETITEMSTATE**</span></span>](lvm-setitemstate.md)
</dt> </dl>

 

 






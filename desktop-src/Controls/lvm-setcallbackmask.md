---
title: 'LVM_SETCALLBACKMASK 訊息 (Commctrl .h) '
description: 變更清單視圖控制項的回呼遮罩。 您可以明確地傳送此訊息，或使用 ListView \_ SetCallbackMask 宏來傳送。
ms.assetid: d7828bab-9897-408c-99ca-fad42b431be8
keywords:
- LVM_SETCALLBACKMASK message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_SETCALLBACKMASK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef6dd46228c4e4aeada30f469a77f9e67aff3a37
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094312"
---
# <a name="lvm_setcallbackmask-message"></a><span data-ttu-id="150d2-105">LVM \_ SETCALLBACKMASK 訊息</span><span class="sxs-lookup"><span data-stu-id="150d2-105">LVM\_SETCALLBACKMASK message</span></span>

<span data-ttu-id="150d2-106">變更清單視圖控制項的回呼遮罩。</span><span class="sxs-lookup"><span data-stu-id="150d2-106">Changes the callback mask for a list-view control.</span></span> <span data-ttu-id="150d2-107">您可以明確地傳送此訊息，或使用 [**ListView \_ SetCallbackMask**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcallbackmask) 宏來傳送。</span><span class="sxs-lookup"><span data-stu-id="150d2-107">You can send this message explicitly or by using the [**ListView\_SetCallbackMask**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcallbackmask) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="150d2-108">參數</span><span class="sxs-lookup"><span data-stu-id="150d2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="150d2-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="150d2-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="150d2-110">回呼遮罩的值。</span><span class="sxs-lookup"><span data-stu-id="150d2-110">Value of the callback mask.</span></span> <span data-ttu-id="150d2-111">遮罩的位表示應用程式儲存目前狀態資料的專案狀態或影像。</span><span class="sxs-lookup"><span data-stu-id="150d2-111">The bits of the mask indicate the item states or images for which the application stores the current state data.</span></span> <span data-ttu-id="150d2-112">這個值可以是下列常數的任意組合：</span><span class="sxs-lookup"><span data-stu-id="150d2-112">This value can be any combination of the following constants:</span></span>



| <span data-ttu-id="150d2-113">值</span><span class="sxs-lookup"><span data-stu-id="150d2-113">Value</span></span>                                                                                                                                                                           | <span data-ttu-id="150d2-114">意義</span><span class="sxs-lookup"><span data-stu-id="150d2-114">Meaning</span></span>                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span id="LVIS_CUT"></span><span id="lvis_cut"></span><dl> <span data-ttu-id="150d2-115"><dt>**LVIS \_ 剪下**</dt></span><span class="sxs-lookup"><span data-stu-id="150d2-115"><dt>**LVIS\_CUT**</dt></span></span> </dl>                                  | <span data-ttu-id="150d2-116">：項目已標記為進行剪貼作業。</span><span class="sxs-lookup"><span data-stu-id="150d2-116">The item is marked for a cut-and-paste operation.</span></span><br/>                                       |
| <span id="LVIS_DROPHILITED"></span><span id="lvis_drophilited"></span><dl> <span data-ttu-id="150d2-117"><dt>**LVIS \_ DROPHILITED**</dt></span><span class="sxs-lookup"><span data-stu-id="150d2-117"><dt>**LVIS\_DROPHILITED**</dt></span></span> </dl>          | <span data-ttu-id="150d2-118">：項目會隨著拖放目標而反白顯示。</span><span class="sxs-lookup"><span data-stu-id="150d2-118">The item is highlighted as a drag-and-drop target.</span></span><br/>                                      |
| <span id="LVIS_FOCUSED"></span><span id="lvis_focused"></span><dl> <span data-ttu-id="150d2-119"><dt>**LVIS \_ 焦點**</dt></span><span class="sxs-lookup"><span data-stu-id="150d2-119"><dt>**LVIS\_FOCUSED**</dt></span></span> </dl>                      | <span data-ttu-id="150d2-120">：項目具有焦點。</span><span class="sxs-lookup"><span data-stu-id="150d2-120">The item has the focus.</span></span><br/>                                                                 |
| <span id="LVIS_SELECTED"></span><span id="lvis_selected"></span><dl> <span data-ttu-id="150d2-121"><dt>**LVIS 已 \_ 選取**</dt></span><span class="sxs-lookup"><span data-stu-id="150d2-121"><dt>**LVIS\_SELECTED**</dt></span></span> </dl>                   | <span data-ttu-id="150d2-122">這個項目已選取。</span><span class="sxs-lookup"><span data-stu-id="150d2-122">The item is selected.</span></span> <br/>                                                                  |
| <span id="LVIS_OVERLAYMASK"></span><span id="lvis_overlaymask"></span><dl> <span data-ttu-id="150d2-123"><dt>**LVIS \_ OVERLAYMASK**</dt></span><span class="sxs-lookup"><span data-stu-id="150d2-123"><dt>**LVIS\_OVERLAYMASK**</dt></span></span> </dl>          | <span data-ttu-id="150d2-124">應用程式會儲存每個專案之目前覆迭影像的影像清單索引。</span><span class="sxs-lookup"><span data-stu-id="150d2-124">The application stores the image list index of the current overlay image for each item.</span></span><br/> |
| <span id="LVIS_STATEIMAGEMASK"></span><span id="lvis_stateimagemask"></span><dl> <span data-ttu-id="150d2-125"><dt>**LVIS \_ STATEIMAGEMASK**</dt></span><span class="sxs-lookup"><span data-stu-id="150d2-125"><dt>**LVIS\_STATEIMAGEMASK**</dt></span></span> </dl> | <span data-ttu-id="150d2-126">應用程式會儲存每個專案之目前狀態影像的影像清單索引。</span><span class="sxs-lookup"><span data-stu-id="150d2-126">The application stores the image list index of the current state image for each item.</span></span> <br/>  |



 

</dd> <dt>

<span data-ttu-id="150d2-127">*lParam*</span><span class="sxs-lookup"><span data-stu-id="150d2-127">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="150d2-128">必須為零。</span><span class="sxs-lookup"><span data-stu-id="150d2-128">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="150d2-129">傳回值</span><span class="sxs-lookup"><span data-stu-id="150d2-129">Return value</span></span>

<span data-ttu-id="150d2-130">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="150d2-130">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="150d2-131">備註</span><span class="sxs-lookup"><span data-stu-id="150d2-131">Remarks</span></span>

<span data-ttu-id="150d2-132">清單視圖控制項的 *回呼遮罩* 是一組位旗標，用來指定應用程式（而非控制項）儲存目前資料的專案狀態。</span><span class="sxs-lookup"><span data-stu-id="150d2-132">The *callback mask* of a list-view control is a set of bit flags that specify the item states for which the application, rather than the control, stores the current data.</span></span> <span data-ttu-id="150d2-133">回呼遮罩適用於所有控制項的項目，與套用至特定項目的回呼項目指定不同。</span><span class="sxs-lookup"><span data-stu-id="150d2-133">The callback mask applies to all of the control's items, unlike the callback item designation, which applies to a specific item.</span></span> <span data-ttu-id="150d2-134">回呼遮罩預設為零，表示清單視圖控制項會儲存所有專案狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="150d2-134">The callback mask is zero by default, meaning that the list-view control stores all item state information.</span></span> <span data-ttu-id="150d2-135">建立清單視圖控制項並初始化其專案之後，您可以傳送 **LVM \_ SETCALLBACKMASK** 訊息來變更回呼遮罩。</span><span class="sxs-lookup"><span data-stu-id="150d2-135">After creating a list-view control and initializing its items, you can send the **LVM\_SETCALLBACKMASK** message to change the callback mask.</span></span> <span data-ttu-id="150d2-136">若要取得目前的回呼遮罩，請傳送 [**LVM \_ GETCALLBACKMASK**](lvm-getcallbackmask.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="150d2-136">To retrieve the current callback mask, send the [**LVM\_GETCALLBACKMASK**](lvm-getcallbackmask.md) message.</span></span>

<span data-ttu-id="150d2-137">如需覆迭影像和狀態影像的詳細資訊，請參閱 [新增 List-View 的影像清單](using-list-view-controls.md)。</span><span class="sxs-lookup"><span data-stu-id="150d2-137">For more information about overlay images and state images, see [Adding List-View Image Lists](using-list-view-controls.md).</span></span>

<span data-ttu-id="150d2-138">如需清單視圖回呼的詳細資訊，請參閱 [回呼專案和回呼遮罩](list-view-controls-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="150d2-138">For more information on list-view callbacks, see [Callback Items and the Callback Mask](list-view-controls-overview.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="150d2-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="150d2-139">Requirements</span></span>



| <span data-ttu-id="150d2-140">需求</span><span class="sxs-lookup"><span data-stu-id="150d2-140">Requirement</span></span> | <span data-ttu-id="150d2-141">值</span><span class="sxs-lookup"><span data-stu-id="150d2-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="150d2-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="150d2-142">Minimum supported client</span></span><br/> | <span data-ttu-id="150d2-143">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="150d2-143">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="150d2-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="150d2-144">Minimum supported server</span></span><br/> | <span data-ttu-id="150d2-145">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="150d2-145">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="150d2-146">標頭</span><span class="sxs-lookup"><span data-stu-id="150d2-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="150d2-147"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="150d2-147"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="150d2-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="150d2-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="150d2-149">**LVN \_ GETDISPINFO**</span><span class="sxs-lookup"><span data-stu-id="150d2-149">**LVN\_GETDISPINFO**</span></span>](lvn-getdispinfo.md)
</dt> </dl>

 

 






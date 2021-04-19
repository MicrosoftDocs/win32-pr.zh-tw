---
title: 'Tree-View 控制項專案狀態 (CommCtrl .h) '
description: 此區段會列出用來指出樹狀檢視控制項中專案狀態的專案狀態旗標。
ms.assetid: 5b11d575-6dfd-47a8-b959-b19aaeeca70e
topic_type:
- apiref
api_name:
- TVIS_BOLD
- TVIS_CUT
- TVIS_DROPHILITED
- TVIS_EXPANDED
- TVIS_EXPANDEDONCE
- TVIS_EXPANDPARTIAL
- TVIS_SELECTED
- TVIS_OVERLAYMASK
- TVIS_STATEIMAGEMASK
- TVIS_USERMASK
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef4a19306855b7f38d03aa00323b26407f108bfe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978665"
---
# <a name="tree-view-control-item-states"></a><span data-ttu-id="a9e31-103">Tree-View 控制項專案狀態</span><span class="sxs-lookup"><span data-stu-id="a9e31-103">Tree-View Control Item States</span></span>

<span data-ttu-id="a9e31-104">此區段會列出用來指出樹狀檢視控制項中專案狀態的專案狀態旗標。</span><span class="sxs-lookup"><span data-stu-id="a9e31-104">This section lists the item state flags used to indicate the state of an item in a tree-view control.</span></span>



| <span data-ttu-id="a9e31-105">常數</span><span class="sxs-lookup"><span data-stu-id="a9e31-105">Constant</span></span>                                                                                                                                                                        | <span data-ttu-id="a9e31-106">描述</span><span class="sxs-lookup"><span data-stu-id="a9e31-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TVIS_BOLD"></span><span id="tvis_bold"></span><dl> <span data-ttu-id="a9e31-107"><dt>**TVIS \_ 粗體**</dt></span><span class="sxs-lookup"><span data-stu-id="a9e31-107"><dt>**TVIS\_BOLD**</dt></span></span> </dl>                               | <span data-ttu-id="a9e31-108">專案為粗體。</span><span class="sxs-lookup"><span data-stu-id="a9e31-108">The item is bold.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="TVIS_CUT"></span><span id="tvis_cut"></span><dl> <span data-ttu-id="a9e31-109"><dt>**TVIS \_ 剪下**</dt></span><span class="sxs-lookup"><span data-stu-id="a9e31-109"><dt>**TVIS\_CUT**</dt></span></span> </dl>                                  | <span data-ttu-id="a9e31-110">選取專案做為剪下和貼上作業的一部分。</span><span class="sxs-lookup"><span data-stu-id="a9e31-110">The item is selected as part of a cut-and-paste operation.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="TVIS_DROPHILITED"></span><span id="tvis_drophilited"></span><dl> <span data-ttu-id="a9e31-111"><dt>**TVIS \_ DROPHILITED**</dt></span><span class="sxs-lookup"><span data-stu-id="a9e31-111"><dt>**TVIS\_DROPHILITED**</dt></span></span> </dl>          | <span data-ttu-id="a9e31-112">專案會選取為拖放目標。</span><span class="sxs-lookup"><span data-stu-id="a9e31-112">The item is selected as a drag-and-drop target.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="TVIS_EXPANDED"></span><span id="tvis_expanded"></span><dl> <span data-ttu-id="a9e31-113"><dt>**展開的 TVIS \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a9e31-113"><dt>**TVIS\_EXPANDED**</dt></span></span> </dl>                   | <span data-ttu-id="a9e31-114">專案的子專案清單目前已展開;也就是說，可以看到子專案。</span><span class="sxs-lookup"><span data-stu-id="a9e31-114">The item's list of child items is currently expanded; that is, the child items are visible.</span></span> <span data-ttu-id="a9e31-115">這個值只適用于父代專案。</span><span class="sxs-lookup"><span data-stu-id="a9e31-115">This value applies only to parent items.</span></span><br/>                                                                                                                                                                                                                                                                                                                  |
| <span id="TVIS_EXPANDEDONCE"></span><span id="tvis_expandedonce"></span><dl> <span data-ttu-id="a9e31-116"><dt>**TVIS \_ EXPANDEDONCE**</dt></span><span class="sxs-lookup"><span data-stu-id="a9e31-116"><dt>**TVIS\_EXPANDEDONCE**</dt></span></span> </dl>       | <span data-ttu-id="a9e31-117">專案的子專案清單至少已展開一次。</span><span class="sxs-lookup"><span data-stu-id="a9e31-117">The item's list of child items has been expanded at least once.</span></span> <span data-ttu-id="a9e31-118">[Izdebski \_ ITEMEXPANDING](tvn-itemexpanding.md)和 [izdebski \_ ITEMEXPANDED](tvn-itemexpanded.md)通知碼不會針對已設定此狀態以回應 [**TVM \_ 展開**](tvm-expand.md)訊息的父專案產生。</span><span class="sxs-lookup"><span data-stu-id="a9e31-118">The [TVN\_ITEMEXPANDING](tvn-itemexpanding.md) and [TVN\_ITEMEXPANDED](tvn-itemexpanded.md) notification codes are not generated for parent items that have this state set in response to a [**TVM\_EXPAND**](tvm-expand.md) message.</span></span> <span data-ttu-id="a9e31-119">使用 \_ \_ 具有 **TVM \_ EXPAND** 的 TVE 折迭和 TVE COLLAPSERESET 將會重設此狀態。</span><span class="sxs-lookup"><span data-stu-id="a9e31-119">Using TVE\_COLLAPSE and TVE\_COLLAPSERESET with **TVM\_EXPAND** will cause this state to be reset.</span></span> <span data-ttu-id="a9e31-120">這個值只適用于父代專案。</span><span class="sxs-lookup"><span data-stu-id="a9e31-120">This value applies only to parent items.</span></span> <br/> |
| <span id="TVIS_EXPANDPARTIAL"></span><span id="tvis_expandpartial"></span><dl> <span data-ttu-id="a9e31-121"><dt>**TVIS \_ EXPANDPARTIAL**</dt></span><span class="sxs-lookup"><span data-stu-id="a9e31-121"><dt>**TVIS\_EXPANDPARTIAL**</dt></span></span> </dl>    | <span data-ttu-id="a9e31-122">**版本 4.70**。</span><span class="sxs-lookup"><span data-stu-id="a9e31-122">**Version 4.70**.</span></span> <span data-ttu-id="a9e31-123">部分擴充的樹狀檢視專案。</span><span class="sxs-lookup"><span data-stu-id="a9e31-123">A partially expanded tree-view item.</span></span> <span data-ttu-id="a9e31-124">在此狀態下，部分（但不是全部）的子專案會顯示出來，而且會顯示父專案的加號。</span><span class="sxs-lookup"><span data-stu-id="a9e31-124">In this state, some, but not all, of the child items are visible and the parent item's plus symbol is displayed.</span></span> <br/>                                                                                                                                                                                                                                                                              |
| <span id="TVIS_SELECTED"></span><span id="tvis_selected"></span><dl> <span data-ttu-id="a9e31-125"><dt>**TVIS 已 \_ 選取**</dt></span><span class="sxs-lookup"><span data-stu-id="a9e31-125"><dt>**TVIS\_SELECTED**</dt></span></span> </dl>                   | <span data-ttu-id="a9e31-126">這個項目已選取。</span><span class="sxs-lookup"><span data-stu-id="a9e31-126">The item is selected.</span></span> <span data-ttu-id="a9e31-127">其外觀取決於它是否具有焦點。</span><span class="sxs-lookup"><span data-stu-id="a9e31-127">Its appearance depends on whether it has the focus.</span></span> <span data-ttu-id="a9e31-128">將會使用系統色彩來繪製專案以供選取。</span><span class="sxs-lookup"><span data-stu-id="a9e31-128">The item will be drawn using the system colors for selection.</span></span> <br/>                                                                                                                                                                                                                                                                                                              |
| <span id="TVIS_OVERLAYMASK"></span><span id="tvis_overlaymask"></span><dl> <span data-ttu-id="a9e31-129"><dt>**TVIS \_ OVERLAYMASK**</dt></span><span class="sxs-lookup"><span data-stu-id="a9e31-129"><dt>**TVIS\_OVERLAYMASK**</dt></span></span> </dl>          | <span data-ttu-id="a9e31-130">用來指定專案之重迭影像索引之位的遮罩。</span><span class="sxs-lookup"><span data-stu-id="a9e31-130">Mask for the bits used to specify the item's overlay image index.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="TVIS_STATEIMAGEMASK"></span><span id="tvis_stateimagemask"></span><dl> <span data-ttu-id="a9e31-131"><dt>**TVIS \_ STATEIMAGEMASK**</dt></span><span class="sxs-lookup"><span data-stu-id="a9e31-131"><dt>**TVIS\_STATEIMAGEMASK**</dt></span></span> </dl> | <span data-ttu-id="a9e31-132">用來指定專案的狀態影像索引之位的遮罩。</span><span class="sxs-lookup"><span data-stu-id="a9e31-132">Mask for the bits used to specify the item's state image index.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="TVIS_USERMASK"></span><span id="tvis_usermask"></span><dl> <span data-ttu-id="a9e31-133"><dt>**TVIS \_ USERMASK**</dt></span><span class="sxs-lookup"><span data-stu-id="a9e31-133"><dt>**TVIS\_USERMASK**</dt></span></span> </dl>                   | <span data-ttu-id="a9e31-134">與 **TVIS \_ STATEIMAGEMASK** 相同。</span><span class="sxs-lookup"><span data-stu-id="a9e31-134">Same as **TVIS\_STATEIMAGEMASK**.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                     |



## <a name="remarks"></a><span data-ttu-id="a9e31-135">備註</span><span class="sxs-lookup"><span data-stu-id="a9e31-135">Remarks</span></span>

<span data-ttu-id="a9e31-136">當您設定或抓取專案的重迭影像索引或狀態影像索引時，您必須在 [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema)結構的 **stateMask** 成員中指定下列遮罩：</span><span class="sxs-lookup"><span data-stu-id="a9e31-136">When you set or retrieve an item's overlay image index or state image index, you must specify the following masks in the **stateMask** member of the [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure:</span></span>

-   <span data-ttu-id="a9e31-137">**TVIS \_ OVERLAYMASK**</span><span class="sxs-lookup"><span data-stu-id="a9e31-137">**TVIS\_OVERLAYMASK**</span></span>
-   <span data-ttu-id="a9e31-138">**TVIS \_ STATEIMAGEMASK**</span><span class="sxs-lookup"><span data-stu-id="a9e31-138">**TVIS\_STATEIMAGEMASK**</span></span>
-   <span data-ttu-id="a9e31-139">**TVIS \_ USERMASK**</span><span class="sxs-lookup"><span data-stu-id="a9e31-139">**TVIS\_USERMASK**</span></span>

<span data-ttu-id="a9e31-140">這些值也可以用來遮罩不感興趣的狀態位。</span><span class="sxs-lookup"><span data-stu-id="a9e31-140">These values can also be used to mask off the state bits that are not of interest.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9e31-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="a9e31-141">Requirements</span></span>



| <span data-ttu-id="a9e31-142">需求</span><span class="sxs-lookup"><span data-stu-id="a9e31-142">Requirement</span></span> | <span data-ttu-id="a9e31-143">值</span><span class="sxs-lookup"><span data-stu-id="a9e31-143">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a9e31-144">標頭</span><span class="sxs-lookup"><span data-stu-id="a9e31-144">Header</span></span><br/> | <dl> <span data-ttu-id="a9e31-145"><dt>CommCtrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="a9e31-145"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 






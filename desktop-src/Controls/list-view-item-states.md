---
title: 'List-View 專案狀態 (CommCtrl) '
description: 專案的狀態值包含專案的狀態、選擇性的覆迭遮罩索引，以及選擇性的狀態影像遮罩索引。
ms.assetid: 21827f4a-f133-489b-bbd2-6979d1928b40
topic_type:
- apiref
api_name:
- LVIS_ACTIVATING
- LVIS_CUT
- LVIS_DROPHILITED
- LVIS_FOCUSED
- LVIS_OVERLAYMASK
- LVIS_SELECTED
- LVIS_STATEIMAGEMASK
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8432760dd4cc7efde30700f837864ddcf04aac31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998612"
---
# <a name="list-view-item-states"></a><span data-ttu-id="1f132-103">List-View 專案狀態</span><span class="sxs-lookup"><span data-stu-id="1f132-103">List-View Item States</span></span>

<span data-ttu-id="1f132-104">專案的狀態值包含專案的狀態、選擇性的覆迭遮罩索引，以及選擇性的狀態影像遮罩索引。</span><span class="sxs-lookup"><span data-stu-id="1f132-104">An item's state value consists of the item's state, an optional overlay mask index, and an optional state image mask index.</span></span>

<span data-ttu-id="1f132-105">專案的狀態決定了其外觀和功能。</span><span class="sxs-lookup"><span data-stu-id="1f132-105">An item's state determines its appearance and functionality.</span></span> <span data-ttu-id="1f132-106">狀態可以是零或一或多個下列值：</span><span class="sxs-lookup"><span data-stu-id="1f132-106">The state can be zero or one or more of the following values:</span></span>



| <span data-ttu-id="1f132-107">常數</span><span class="sxs-lookup"><span data-stu-id="1f132-107">Constant</span></span>                                                                                                                                                                        | <span data-ttu-id="1f132-108">描述</span><span class="sxs-lookup"><span data-stu-id="1f132-108">Description</span></span>                                                                                                                                                          |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LVIS_ACTIVATING"></span><span id="lvis_activating"></span><dl> <span data-ttu-id="1f132-109"><dt>**LVIS \_ 啟用**</dt></span><span class="sxs-lookup"><span data-stu-id="1f132-109"><dt>**LVIS\_ACTIVATING**</dt></span></span> </dl>             | <span data-ttu-id="1f132-110">目前不支援。</span><span class="sxs-lookup"><span data-stu-id="1f132-110">Not currently supported.</span></span><br/>                                                                                                                                  |
| <span id="LVIS_CUT"></span><span id="lvis_cut"></span><dl> <span data-ttu-id="1f132-111"><dt>**LVIS \_ 剪下**</dt></span><span class="sxs-lookup"><span data-stu-id="1f132-111"><dt>**LVIS\_CUT**</dt></span></span> </dl>                                  | <span data-ttu-id="1f132-112">：項目已標記為進行剪貼作業。</span><span class="sxs-lookup"><span data-stu-id="1f132-112">The item is marked for a cut-and-paste operation.</span></span><br/>                                                                                                         |
| <span id="LVIS_DROPHILITED"></span><span id="lvis_drophilited"></span><dl> <span data-ttu-id="1f132-113"><dt>**LVIS \_ DROPHILITED**</dt></span><span class="sxs-lookup"><span data-stu-id="1f132-113"><dt>**LVIS\_DROPHILITED**</dt></span></span> </dl>          | <span data-ttu-id="1f132-114">：項目會隨著拖放目標而反白顯示。</span><span class="sxs-lookup"><span data-stu-id="1f132-114">The item is highlighted as a drag-and-drop target.</span></span><br/>                                                                                                        |
| <span id="LVIS_FOCUSED"></span><span id="lvis_focused"></span><dl> <span data-ttu-id="1f132-115"><dt>**LVIS \_ 焦點**</dt></span><span class="sxs-lookup"><span data-stu-id="1f132-115"><dt>**LVIS\_FOCUSED**</dt></span></span> </dl>                      | <span data-ttu-id="1f132-116">專案具有焦點，因此會以標準焦點矩形括住。</span><span class="sxs-lookup"><span data-stu-id="1f132-116">The item has the focus, so it is surrounded by a standard focus rectangle.</span></span> <span data-ttu-id="1f132-117">雖然可以選取一個以上的專案，但只有一個專案可以有焦點。</span><span class="sxs-lookup"><span data-stu-id="1f132-117">Although more than one item may be selected, only one item can have the focus.</span></span><br/> |
| <span id="LVIS_OVERLAYMASK"></span><span id="lvis_overlaymask"></span><dl> <span data-ttu-id="1f132-118"><dt>**LVIS \_ OVERLAYMASK**</dt></span><span class="sxs-lookup"><span data-stu-id="1f132-118"><dt>**LVIS\_OVERLAYMASK**</dt></span></span> </dl>          | <span data-ttu-id="1f132-119">遮罩會取出專案的重迭影像索引。</span><span class="sxs-lookup"><span data-stu-id="1f132-119">The item's overlay image index is retrieved by a mask.</span></span><br/>                                                                                                    |
| <span id="LVIS_SELECTED"></span><span id="lvis_selected"></span><dl> <span data-ttu-id="1f132-120"><dt>**LVIS 已 \_ 選取**</dt></span><span class="sxs-lookup"><span data-stu-id="1f132-120"><dt>**LVIS\_SELECTED**</dt></span></span> </dl>                   | <span data-ttu-id="1f132-121">這個項目已選取。</span><span class="sxs-lookup"><span data-stu-id="1f132-121">The item is selected.</span></span> <span data-ttu-id="1f132-122">選取專案的外觀取決於它是否具有焦點，也會顯示用於選取的系統色彩。</span><span class="sxs-lookup"><span data-stu-id="1f132-122">The appearance of a selected item depends on whether it has the focus and also on the system colors used for selection.</span></span><br/>             |
| <span id="LVIS_STATEIMAGEMASK"></span><span id="lvis_stateimagemask"></span><dl> <span data-ttu-id="1f132-123"><dt>**LVIS \_ STATEIMAGEMASK**</dt></span><span class="sxs-lookup"><span data-stu-id="1f132-123"><dt>**LVIS\_STATEIMAGEMASK**</dt></span></span> </dl> | <span data-ttu-id="1f132-124">遮罩會取出專案的狀態影像索引。</span><span class="sxs-lookup"><span data-stu-id="1f132-124">The item's state image index is retrieved by a mask.</span></span><br/>                                                                                                      |



## <a name="remarks"></a><span data-ttu-id="1f132-125">備註</span><span class="sxs-lookup"><span data-stu-id="1f132-125">Remarks</span></span>

<span data-ttu-id="1f132-126">您可以使用 **LVIS \_ OVERLAYMASK** mask 來隔離重迭影像的以一為基礎的索引。</span><span class="sxs-lookup"><span data-stu-id="1f132-126">You can use the **LVIS\_OVERLAYMASK** mask to isolate the one-based index of the overlay image.</span></span> <span data-ttu-id="1f132-127">您可以使用 **LVIS \_ STATEIMAGEMASK** mask 來隔離狀態影像的以一為基礎的索引。</span><span class="sxs-lookup"><span data-stu-id="1f132-127">You can use the **LVIS\_STATEIMAGEMASK** mask to isolate the one-based index of the state image.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f132-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="1f132-128">Requirements</span></span>



| <span data-ttu-id="1f132-129">需求</span><span class="sxs-lookup"><span data-stu-id="1f132-129">Requirement</span></span> | <span data-ttu-id="1f132-130">值</span><span class="sxs-lookup"><span data-stu-id="1f132-130">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1f132-131">標頭</span><span class="sxs-lookup"><span data-stu-id="1f132-131">Header</span></span><br/> | <dl> <span data-ttu-id="1f132-132"><dt>CommCtrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="1f132-132"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 






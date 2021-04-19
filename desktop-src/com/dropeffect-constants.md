---
title: 'DROPEFFECT 常數 (Oleidl.idl) '
description: 表示拖放作業之效果的相關資訊。
ms.assetid: d8e46899-3fbf-4012-8dd3-67fa627526d5
topic_type:
- apiref
api_name:
- DROPEFFECT_NONE
- DROPEFFECT_COPY
- DROPEFFECT_MOVE
- DROPEFFECT_LINK
- DROPEFFECT_SCROLL
api_location:
- OleIdl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2b1888aa028d4e047a9a8ec1f54e2497fa28ce4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969626"
---
# <a name="dropeffect-constants"></a><span data-ttu-id="b57d8-103">DROPEFFECT 常數</span><span class="sxs-lookup"><span data-stu-id="b57d8-103">DROPEFFECT Constants</span></span>

<span data-ttu-id="b57d8-104">表示拖放作業之效果的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b57d8-104">Represents information about the effects of a drag-and-drop operation.</span></span> <span data-ttu-id="b57d8-105">[**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop)函式和 [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource)和 [**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget)中的許多方法都會使用此列舉的值。</span><span class="sxs-lookup"><span data-stu-id="b57d8-105">The [**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop) function and many of the methods in the [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) and [**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget) use the values of this enumeration.</span></span>



| <span data-ttu-id="b57d8-106">常數/值</span><span class="sxs-lookup"><span data-stu-id="b57d8-106">Constant/value</span></span>                                                                                                                                                                                                                            | <span data-ttu-id="b57d8-107">Description</span><span class="sxs-lookup"><span data-stu-id="b57d8-107">Description</span></span>                                                                                                                         |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DROPEFFECT_NONE"></span><span id="dropeffect_none"></span><dl> <span data-ttu-id="b57d8-108"><dt>**DROPEFFECT \_無**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b57d8-108"><dt>**DROPEFFECT\_NONE**</dt> <dt>0</dt></span></span> </dl>                | <span data-ttu-id="b57d8-109">捨棄目標無法接受資料。</span><span class="sxs-lookup"><span data-stu-id="b57d8-109">Drop target cannot accept the data.</span></span><br/>                                                                                      |
| <span id="DROPEFFECT_COPY"></span><span id="dropeffect_copy"></span><dl> <span data-ttu-id="b57d8-110"><dt>**DROPEFFECT \_複製**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="b57d8-110"><dt>**DROPEFFECT\_COPY**</dt> <dt>1</dt></span></span> </dl>                | <span data-ttu-id="b57d8-111">將結果放置在複本中。</span><span class="sxs-lookup"><span data-stu-id="b57d8-111">Drop results in a copy.</span></span> <span data-ttu-id="b57d8-112">拖曳來源不會改變原始資料。</span><span class="sxs-lookup"><span data-stu-id="b57d8-112">The original data is untouched by the drag source.</span></span><br/>                                               |
| <span id="DROPEFFECT_MOVE"></span><span id="dropeffect_move"></span><dl> <span data-ttu-id="b57d8-113"><dt>**DROPEFFECT \_移動**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="b57d8-113"><dt>**DROPEFFECT\_MOVE**</dt> <dt>2</dt></span></span> </dl>                | <span data-ttu-id="b57d8-114">拖曳來源應該移除資料。</span><span class="sxs-lookup"><span data-stu-id="b57d8-114">Drag source should remove the data.</span></span> <br/>                                                                                     |
| <span id="DROPEFFECT_LINK"></span><span id="dropeffect_link"></span><dl> <span data-ttu-id="b57d8-115"><dt>**DROPEFFECT \_連結**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="b57d8-115"><dt>**DROPEFFECT\_LINK**</dt> <dt>4</dt></span></span> </dl>                | <span data-ttu-id="b57d8-116">拖曳來源應建立原始資料的連結。</span><span class="sxs-lookup"><span data-stu-id="b57d8-116">Drag source should create a link to the original data.</span></span><br/>                                                                   |
| <span id="DROPEFFECT_SCROLL"></span><span id="dropeffect_scroll"></span><dl> <span data-ttu-id="b57d8-117"><dt>**DROPEFFECT \_滾動**</dt>的 <dt>0x80000000</dt></span><span class="sxs-lookup"><span data-stu-id="b57d8-117"><dt>**DROPEFFECT\_SCROLL**</dt> <dt>0x80000000</dt></span></span> </dl> | <span data-ttu-id="b57d8-118">滾動即將開始，或目前在目標中發生。</span><span class="sxs-lookup"><span data-stu-id="b57d8-118">Scrolling is about to start or is currently occurring in the target.</span></span> <span data-ttu-id="b57d8-119">除了其他值之外，還會使用這個值。</span><span class="sxs-lookup"><span data-stu-id="b57d8-119">This value is used in addition to the other values.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="b57d8-120">備註</span><span class="sxs-lookup"><span data-stu-id="b57d8-120">Remarks</span></span>

<span data-ttu-id="b57d8-121">您的應用程式應該一律遮罩 **DROPEFFECT** 列舉中的值，以確保與未來的實施相容。</span><span class="sxs-lookup"><span data-stu-id="b57d8-121">Your application should always mask values from the **DROPEFFECT** enumeration to ensure compatibility with future implementations.</span></span> <span data-ttu-id="b57d8-122">目前，只有 **DROPEFFECT** 值中的某些位置具有意義。</span><span class="sxs-lookup"><span data-stu-id="b57d8-122">Presently, only some of the positions in a **DROPEFFECT** value have meaning.</span></span> <span data-ttu-id="b57d8-123">未來將會新增更多的位解釋。</span><span class="sxs-lookup"><span data-stu-id="b57d8-123">In the future, more interpretations for the bits will be added.</span></span> <span data-ttu-id="b57d8-124">拖曳來源和卸載目標應該在比較之前仔細地適當地遮罩這些值。</span><span class="sxs-lookup"><span data-stu-id="b57d8-124">Drag sources and drop targets should carefully mask these values appropriately before comparing.</span></span> <span data-ttu-id="b57d8-125">它們絕對不應該藉 \_ 由執行下列動作來比較 DROPEFFECT，例如 DROPEFFECT COPY：</span><span class="sxs-lookup"><span data-stu-id="b57d8-125">They should never compare a **DROPEFFECT** against, say, DROPEFFECT\_COPY by doing the following:</span></span>

``` syntax
if (dwDropEffect == DROPEFFECT_COPY)... 
```

<span data-ttu-id="b57d8-126">相反地，應用程式應該一律遮罩值，或使用下列其中一種技術來搜尋值：</span><span class="sxs-lookup"><span data-stu-id="b57d8-126">Instead, the application should always mask for the value or values being sought as using one of the following techniques:</span></span>

``` syntax
if (dwDropEffect & DROPEFFECT_COPY) == DROPEFFECT_COPY)...

if (dwDropEffect & DROPEFFECT_COPY)... 
```

<span data-ttu-id="b57d8-127">這可讓您定義新的捨棄效果，同時保留與現有程式碼的回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="b57d8-127">This allows for the definition of new drop effects, while preserving backward compatibility with existing code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b57d8-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="b57d8-128">Requirements</span></span>



| <span data-ttu-id="b57d8-129">需求</span><span class="sxs-lookup"><span data-stu-id="b57d8-129">Requirement</span></span> | <span data-ttu-id="b57d8-130">值</span><span class="sxs-lookup"><span data-stu-id="b57d8-130">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b57d8-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b57d8-131">Minimum supported client</span></span><br/> | <span data-ttu-id="b57d8-132">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b57d8-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="b57d8-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b57d8-133">Minimum supported server</span></span><br/> | <span data-ttu-id="b57d8-134">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b57d8-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b57d8-135">標頭</span><span class="sxs-lookup"><span data-stu-id="b57d8-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="b57d8-136"><dt>Oleidl.idl。h</dt></span><span class="sxs-lookup"><span data-stu-id="b57d8-136"><dt>OleIdl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b57d8-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b57d8-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b57d8-138">**DoDragDrop**</span><span class="sxs-lookup"><span data-stu-id="b57d8-138">**DoDragDrop**</span></span>](/windows/desktop/api/Ole2/nf-ole2-dodragdrop)
</dt> <dt>

[<span data-ttu-id="b57d8-139">**IDropSource**</span><span class="sxs-lookup"><span data-stu-id="b57d8-139">**IDropSource**</span></span>](/windows/desktop/api/OleIdl/nn-oleidl-idropsource)
</dt> <dt>

[<span data-ttu-id="b57d8-140">**IDropTarget**</span><span class="sxs-lookup"><span data-stu-id="b57d8-140">**IDropTarget**</span></span>](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget)
</dt> </dl>

 

 






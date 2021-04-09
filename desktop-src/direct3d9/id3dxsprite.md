---
description: ID3DXSprite 介面提供一組方法，可使用 Microsoft Direct3D 簡化繪製 sprite 的程式。
ms.assetid: ccf34fac-91a7-4734-bc62-aedaf4d66522
title: 'ID3DXSprite 介面 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3703132cd8a0f7744119d9b8cb5d9d48f260094c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103854019"
---
# <a name="id3dxsprite-interface"></a><span data-ttu-id="69d36-103">ID3DXSprite 介面</span><span class="sxs-lookup"><span data-stu-id="69d36-103">ID3DXSprite interface</span></span>

<span data-ttu-id="69d36-104">ID3DXSprite 介面提供一組方法，可使用 Microsoft Direct3D 簡化繪製 sprite 的程式。</span><span class="sxs-lookup"><span data-stu-id="69d36-104">The ID3DXSprite interface provides a set of methods that simplify the process of drawing sprites using Microsoft Direct3D.</span></span>

## <a name="members"></a><span data-ttu-id="69d36-105">成員</span><span class="sxs-lookup"><span data-stu-id="69d36-105">Members</span></span>

<span data-ttu-id="69d36-106">**ID3DXSprite** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="69d36-106">The **ID3DXSprite** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="69d36-107">**ID3DXSprite** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="69d36-107">**ID3DXSprite** also has these types of members:</span></span>

-   [<span data-ttu-id="69d36-108">方法</span><span class="sxs-lookup"><span data-stu-id="69d36-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="69d36-109">方法</span><span class="sxs-lookup"><span data-stu-id="69d36-109">Methods</span></span>

<span data-ttu-id="69d36-110">**ID3DXSprite** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="69d36-110">The **ID3DXSprite** interface has these methods.</span></span>



| <span data-ttu-id="69d36-111">方法</span><span class="sxs-lookup"><span data-stu-id="69d36-111">Method</span></span>                                                | <span data-ttu-id="69d36-112">描述</span><span class="sxs-lookup"><span data-stu-id="69d36-112">Description</span></span>                                                                                                                                                                                                                  |
|:------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="69d36-113">**開始**</span><span class="sxs-lookup"><span data-stu-id="69d36-113">**Begin**</span></span>](id3dxsprite--begin.md)                   | <span data-ttu-id="69d36-114">準備裝置以繪製 sprite。</span><span class="sxs-lookup"><span data-stu-id="69d36-114">Prepares a device for drawing sprites.</span></span><br/>                                                                                                                                                                            |
| [<span data-ttu-id="69d36-115">**Draw**</span><span class="sxs-lookup"><span data-stu-id="69d36-115">**Draw**</span></span>](id3dxsprite--draw.md)                     | <span data-ttu-id="69d36-116">將 sprite 新增至批次 sprite 的清單。</span><span class="sxs-lookup"><span data-stu-id="69d36-116">Adds a sprite to the list of batched sprites.</span></span><br/>                                                                                                                                                                     |
| [<span data-ttu-id="69d36-117">**結束**</span><span class="sxs-lookup"><span data-stu-id="69d36-117">**End**</span></span>](id3dxsprite--end.md)                       | <span data-ttu-id="69d36-118">呼叫 [**ID3DXSprite：： Flush**](id3dxsprite--flush.md) ，然後將裝置狀態還原為 [**ID3DXSprite：： Begin**](id3dxsprite--begin.md) 之前的狀態。</span><span class="sxs-lookup"><span data-stu-id="69d36-118">Calls [**ID3DXSprite::Flush**](id3dxsprite--flush.md) and restores the device state to how it was before [**ID3DXSprite::Begin**](id3dxsprite--begin.md) was called.</span></span><br/>                                            |
| [<span data-ttu-id="69d36-119">**清除**</span><span class="sxs-lookup"><span data-stu-id="69d36-119">**Flush**</span></span>](id3dxsprite--flush.md)                   | <span data-ttu-id="69d36-120">強制將所有批次中的 sprite 提交至裝置。</span><span class="sxs-lookup"><span data-stu-id="69d36-120">Forces all batched sprites to be submitted to the device.</span></span> <span data-ttu-id="69d36-121">裝置狀態會維持在最後一次呼叫 [**ID3DXSprite：： Begin**](id3dxsprite--begin.md)之後。</span><span class="sxs-lookup"><span data-stu-id="69d36-121">Device states remain as they were after the last call to [**ID3DXSprite::Begin**](id3dxsprite--begin.md).</span></span> <span data-ttu-id="69d36-122">然後會清除批次中的子後 sprite 清單。</span><span class="sxs-lookup"><span data-stu-id="69d36-122">The list of batched sprites is then cleared.</span></span><br/> |
| [<span data-ttu-id="69d36-123">**GetDevice**</span><span class="sxs-lookup"><span data-stu-id="69d36-123">**GetDevice**</span></span>](id3dxsprite--getdevice.md)           | <span data-ttu-id="69d36-124">捕獲與 sprite 物件相關聯的裝置。</span><span class="sxs-lookup"><span data-stu-id="69d36-124">Retrieves the device associated with the sprite object.</span></span><br/>                                                                                                                                                           |
| [<span data-ttu-id="69d36-125">**GetTransform**</span><span class="sxs-lookup"><span data-stu-id="69d36-125">**GetTransform**</span></span>](id3dxsprite--gettransform.md)     | <span data-ttu-id="69d36-126">取得 sprite 轉換。</span><span class="sxs-lookup"><span data-stu-id="69d36-126">Gets the sprite transform.</span></span><br/>                                                                                                                                                                                        |
| [<span data-ttu-id="69d36-127">**OnLostDevice**</span><span class="sxs-lookup"><span data-stu-id="69d36-127">**OnLostDevice**</span></span>](id3dxsprite--onlostdevice.md)     | <span data-ttu-id="69d36-128">您可以使用此方法來釋放視訊記憶體資源的所有參考，並刪除所有 stateblocks。</span><span class="sxs-lookup"><span data-stu-id="69d36-128">Use this method to release all references to video memory resources and delete all stateblocks.</span></span> <span data-ttu-id="69d36-129">只要裝置遺失或在重設裝置之前，都應該呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="69d36-129">This method should be called whenever a device is lost or before resetting a device.</span></span><br/>                              |
| [<span data-ttu-id="69d36-130">**OnResetDevice**</span><span class="sxs-lookup"><span data-stu-id="69d36-130">**OnResetDevice**</span></span>](id3dxsprite--onresetdevice.md)   | <span data-ttu-id="69d36-131">您可以使用這個方法來重新取得資源，並儲存初始狀態。</span><span class="sxs-lookup"><span data-stu-id="69d36-131">Use this method to re-acquire resources and save initial state.</span></span><br/>                                                                                                                                                   |
| [<span data-ttu-id="69d36-132">**SetTransform**</span><span class="sxs-lookup"><span data-stu-id="69d36-132">**SetTransform**</span></span>](id3dxsprite--settransform.md)     | <span data-ttu-id="69d36-133">設定 sprite 轉換。</span><span class="sxs-lookup"><span data-stu-id="69d36-133">Sets the sprite transform.</span></span><br/>                                                                                                                                                                                        |
| [<span data-ttu-id="69d36-134">**SetWorldViewLH**</span><span class="sxs-lookup"><span data-stu-id="69d36-134">**SetWorldViewLH**</span></span>](id3dxsprite--setworldviewlh.md) | <span data-ttu-id="69d36-135">為 sprite 設定左手的世界視圖轉換。</span><span class="sxs-lookup"><span data-stu-id="69d36-135">Sets the left-handed world-view transform for a sprite.</span></span> <span data-ttu-id="69d36-136">在 billboarding 或排序 sprite 之前，需要呼叫此方法。</span><span class="sxs-lookup"><span data-stu-id="69d36-136">A call to this method is required before billboarding or sorting sprites.</span></span><br/>                                                                                 |
| [<span data-ttu-id="69d36-137">**SetWorldViewRH**</span><span class="sxs-lookup"><span data-stu-id="69d36-137">**SetWorldViewRH**</span></span>](id3dxsprite--setworldviewrh.md) | <span data-ttu-id="69d36-138">為 sprite 設定右手的世界視圖轉換。</span><span class="sxs-lookup"><span data-stu-id="69d36-138">Sets the right-handed world-view transform for a sprite.</span></span> <span data-ttu-id="69d36-139">在 billboarding 或排序 sprite 之前，需要呼叫此方法。</span><span class="sxs-lookup"><span data-stu-id="69d36-139">A call to this method is required before billboarding or sorting sprites.</span></span><br/>                                                                                |



 

## <a name="remarks"></a><span data-ttu-id="69d36-140">備註</span><span class="sxs-lookup"><span data-stu-id="69d36-140">Remarks</span></span>

<span data-ttu-id="69d36-141">**ID3DXSprite** 介面是藉由呼叫 [**D3DXCreateSprite**](d3dxcreatesprite.md)函數來取得。</span><span class="sxs-lookup"><span data-stu-id="69d36-141">The **ID3DXSprite** interface is obtained by calling the [**D3DXCreateSprite**](d3dxcreatesprite.md) function.</span></span>

<span data-ttu-id="69d36-142">應用程式通常會先呼叫 [**ID3DXSprite：： Begin**](id3dxsprite--begin.md)，以便控制裝置轉譯狀態、Alpha 混色和 sprite 轉換和排序。</span><span class="sxs-lookup"><span data-stu-id="69d36-142">The application typically first calls [**ID3DXSprite::Begin**](id3dxsprite--begin.md), which allows control over the device render state, alpha blending, and sprite transformation and sorting.</span></span> <span data-ttu-id="69d36-143">然後，針對每個要顯示的 sprite，呼叫 [**ID3DXSprite：:D raw**](id3dxsprite--draw.md)。</span><span class="sxs-lookup"><span data-stu-id="69d36-143">Then for each sprite to be displayed, call [**ID3DXSprite::Draw**](id3dxsprite--draw.md).</span></span> <span data-ttu-id="69d36-144">**ID3DXSprite：:D raw** 可以重複呼叫，以儲存任何數目的 sprite。</span><span class="sxs-lookup"><span data-stu-id="69d36-144">**ID3DXSprite::Draw** can be called repeatedly to store any number of sprites.</span></span> <span data-ttu-id="69d36-145">若要對裝置顯示批次的分次，請呼叫 [**ID3DXSprite：： End**](id3dxsprite--end.md) 或 [**ID3DXSprite：： Flush**](id3dxsprite--flush.md)。</span><span class="sxs-lookup"><span data-stu-id="69d36-145">To display the batched sprites to the device, call [**ID3DXSprite::End**](id3dxsprite--end.md) or [**ID3DXSprite::Flush**](id3dxsprite--flush.md).</span></span>

<span data-ttu-id="69d36-146">LPD3DXSPRITE 型別定義為 **ID3DXSprite** 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="69d36-146">The LPD3DXSPRITE type is defined as a pointer to the **ID3DXSprite** interface.</span></span>


```
typedef interface ID3DXSprite ID3DXSprite;
typedef interface ID3DXSprite *LPD3DXSPRITE;
```



## <a name="requirements"></a><span data-ttu-id="69d36-147">規格需求</span><span class="sxs-lookup"><span data-stu-id="69d36-147">Requirements</span></span>



| <span data-ttu-id="69d36-148">需求</span><span class="sxs-lookup"><span data-stu-id="69d36-148">Requirement</span></span> | <span data-ttu-id="69d36-149">值</span><span class="sxs-lookup"><span data-stu-id="69d36-149">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="69d36-150">標頭</span><span class="sxs-lookup"><span data-stu-id="69d36-150">Header</span></span><br/>  | <dl> <span data-ttu-id="69d36-151"><dt>D3dx9core。h</dt></span><span class="sxs-lookup"><span data-stu-id="69d36-151"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="69d36-152">程式庫</span><span class="sxs-lookup"><span data-stu-id="69d36-152">Library</span></span><br/> | <dl> <span data-ttu-id="69d36-153"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="69d36-153"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="69d36-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="69d36-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69d36-155">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="69d36-155">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 

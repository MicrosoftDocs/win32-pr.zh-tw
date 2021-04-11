---
description: ID3DXLine 介面會使用紋理三角形來實行繪圖。
ms.assetid: 87472618-d3e4-4008-9009-ae17fc7b696d
title: 'ID3DXLine 介面 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1c535ff736e9a26e8316e4715f4be4022a6417df
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104035442"
---
# <a name="id3dxline-interface"></a><span data-ttu-id="64ade-103">ID3DXLine 介面</span><span class="sxs-lookup"><span data-stu-id="64ade-103">ID3DXLine interface</span></span>

<span data-ttu-id="64ade-104">ID3DXLine 介面會使用紋理三角形來實行繪圖。</span><span class="sxs-lookup"><span data-stu-id="64ade-104">The ID3DXLine interface implements line drawing using textured triangles.</span></span>

## <a name="members"></a><span data-ttu-id="64ade-105">成員</span><span class="sxs-lookup"><span data-stu-id="64ade-105">Members</span></span>

<span data-ttu-id="64ade-106">**ID3DXLine** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="64ade-106">The **ID3DXLine** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="64ade-107">**ID3DXLine** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="64ade-107">**ID3DXLine** also has these types of members:</span></span>

-   [<span data-ttu-id="64ade-108">方法</span><span class="sxs-lookup"><span data-stu-id="64ade-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="64ade-109">方法</span><span class="sxs-lookup"><span data-stu-id="64ade-109">Methods</span></span>

<span data-ttu-id="64ade-110">**ID3DXLine** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="64ade-110">The **ID3DXLine** interface has these methods.</span></span>



| <span data-ttu-id="64ade-111">方法</span><span class="sxs-lookup"><span data-stu-id="64ade-111">Method</span></span>                                                | <span data-ttu-id="64ade-112">描述</span><span class="sxs-lookup"><span data-stu-id="64ade-112">Description</span></span>                                                                                                                                                                                      |
|:------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="64ade-113">**開始**</span><span class="sxs-lookup"><span data-stu-id="64ade-113">**Begin**</span></span>](id3dxline--begin.md)                     | <span data-ttu-id="64ade-114">準備裝置來繪製線條。</span><span class="sxs-lookup"><span data-stu-id="64ade-114">Prepares a device for drawing lines.</span></span><br/>                                                                                                                                                  |
| [<span data-ttu-id="64ade-115">**Draw**</span><span class="sxs-lookup"><span data-stu-id="64ade-115">**Draw**</span></span>](id3dxline--draw.md)                       | <span data-ttu-id="64ade-116">在螢幕空間中繪製帶狀線。</span><span class="sxs-lookup"><span data-stu-id="64ade-116">Draws a line strip in screen space.</span></span> <span data-ttu-id="64ade-117">輸入的格式為數組，可定義 [**D3DXVECTOR2**](d3dxvector2.md)) 在行條紋 (的點。</span><span class="sxs-lookup"><span data-stu-id="64ade-117">Input is in the form of an array that defines points (of [**D3DXVECTOR2**](d3dxvector2.md)) on the line strip.</span></span><br/>                                   |
| [<span data-ttu-id="64ade-118">**DrawTransform**</span><span class="sxs-lookup"><span data-stu-id="64ade-118">**DrawTransform**</span></span>](id3dxline--drawtransform.md)     | <span data-ttu-id="64ade-119">使用指定的輸入轉換矩陣，在螢幕空間中繪製行帶狀。</span><span class="sxs-lookup"><span data-stu-id="64ade-119">Draws a line strip in screen space with a specified input transformation matrix.</span></span><br/>                                                                                                      |
| [<span data-ttu-id="64ade-120">**結束**</span><span class="sxs-lookup"><span data-stu-id="64ade-120">**End**</span></span>](id3dxline--end.md)                         | <span data-ttu-id="64ade-121">將裝置狀態還原為呼叫 [**ID3DXLine：： Begin**](id3dxline--begin.md) 時的狀態。</span><span class="sxs-lookup"><span data-stu-id="64ade-121">Restores the device state to how it was when [**ID3DXLine::Begin**](id3dxline--begin.md) was called.</span></span><br/>                                                                                 |
| [<span data-ttu-id="64ade-122">**GetAntialias**</span><span class="sxs-lookup"><span data-stu-id="64ade-122">**GetAntialias**</span></span>](id3dxline--getantialias.md)       | <span data-ttu-id="64ade-123">取得線條消除鋸齒狀態。</span><span class="sxs-lookup"><span data-stu-id="64ade-123">Gets the line antialiasing state.</span></span><br/>                                                                                                                                                     |
| [<span data-ttu-id="64ade-124">**GetDevice**</span><span class="sxs-lookup"><span data-stu-id="64ade-124">**GetDevice**</span></span>](id3dxline--getdevice.md)             | <span data-ttu-id="64ade-125">抓取與 line 物件相關聯的 Direct3D 裝置。</span><span class="sxs-lookup"><span data-stu-id="64ade-125">Retrieves the Direct3D device associated with the line object.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="64ade-126">**GetGLLines**</span><span class="sxs-lookup"><span data-stu-id="64ade-126">**GetGLLines**</span></span>](id3dxline--getgllines.md)           | <span data-ttu-id="64ade-127">取得 OpenGL 樣式的線條繪圖模式。</span><span class="sxs-lookup"><span data-stu-id="64ade-127">Gets the OpenGL-style line-drawing mode.</span></span><br/>                                                                                                                                              |
| [<span data-ttu-id="64ade-128">**System.windows.automation.peers.uielementautomationpeer.getpattern**</span><span class="sxs-lookup"><span data-stu-id="64ade-128">**GetPattern**</span></span>](id3dxline--getpattern.md)           | <span data-ttu-id="64ade-129">取得行 stipple 模式。</span><span class="sxs-lookup"><span data-stu-id="64ade-129">Gets the line stipple pattern.</span></span><br/>                                                                                                                                                        |
| [<span data-ttu-id="64ade-130">**GetPatternScale**</span><span class="sxs-lookup"><span data-stu-id="64ade-130">**GetPatternScale**</span></span>](id3dxline--getpatternscale.md) | <span data-ttu-id="64ade-131">取得 stipple 模式比例值。</span><span class="sxs-lookup"><span data-stu-id="64ade-131">Gets the stipple-pattern scale value.</span></span><br/>                                                                                                                                                 |
| [<span data-ttu-id="64ade-132">**GetWidth**</span><span class="sxs-lookup"><span data-stu-id="64ade-132">**GetWidth**</span></span>](id3dxline--getwidth.md)               | <span data-ttu-id="64ade-133">取得線條的粗細。</span><span class="sxs-lookup"><span data-stu-id="64ade-133">Gets the thickness of the line.</span></span><br/>                                                                                                                                                       |
| [<span data-ttu-id="64ade-134">**OnLostDevice**</span><span class="sxs-lookup"><span data-stu-id="64ade-134">**OnLostDevice**</span></span>](id3dxline--onlostdevice.md)       | <span data-ttu-id="64ade-135">您可以使用此方法來釋放視訊記憶體資源的所有參考，並刪除所有 stateblocks。</span><span class="sxs-lookup"><span data-stu-id="64ade-135">Use this method to release all references to video memory resources and delete all stateblocks.</span></span> <span data-ttu-id="64ade-136">只要裝置遺失或在重設裝置之前，都應該呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="64ade-136">This method should be called whenever a device is lost, or before resetting a device.</span></span><br/> |
| [<span data-ttu-id="64ade-137">**OnResetDevice**</span><span class="sxs-lookup"><span data-stu-id="64ade-137">**OnResetDevice**</span></span>](id3dxline--onresetdevice.md)     | <span data-ttu-id="64ade-138">您可以使用這個方法來重新取得資源，並儲存初始狀態。</span><span class="sxs-lookup"><span data-stu-id="64ade-138">Use this method to re-acquire resources and save initial state.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="64ade-139">**SetAntialias**</span><span class="sxs-lookup"><span data-stu-id="64ade-139">**SetAntialias**</span></span>](id3dxline--setantialias.md)       | <span data-ttu-id="64ade-140">切換線條消除鋸齒。</span><span class="sxs-lookup"><span data-stu-id="64ade-140">Toggles line antialiasing.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="64ade-141">**SetGLLines**</span><span class="sxs-lookup"><span data-stu-id="64ade-141">**SetGLLines**</span></span>](id3dxline--setgllines.md)           | <span data-ttu-id="64ade-142">切換模式以繪製 OpenGL 樣式的線條。</span><span class="sxs-lookup"><span data-stu-id="64ade-142">Toggles the mode to draw OpenGL-style lines.</span></span><br/>                                                                                                                                          |
| [<span data-ttu-id="64ade-143">**SetPattern**</span><span class="sxs-lookup"><span data-stu-id="64ade-143">**SetPattern**</span></span>](id3dxline--setpattern.md)           | <span data-ttu-id="64ade-144">將 stipple 模式套用至線條。</span><span class="sxs-lookup"><span data-stu-id="64ade-144">Applies a stipple pattern to the line.</span></span><br/>                                                                                                                                                |
| [<span data-ttu-id="64ade-145">**SetPatternScale**</span><span class="sxs-lookup"><span data-stu-id="64ade-145">**SetPatternScale**</span></span>](id3dxline--setpatternscale.md) | <span data-ttu-id="64ade-146">沿著線條方向伸展 stipple 模式。</span><span class="sxs-lookup"><span data-stu-id="64ade-146">Stretches the stipple pattern along the line direction.</span></span><br/>                                                                                                                               |
| [<span data-ttu-id="64ade-147">**SetWidth**</span><span class="sxs-lookup"><span data-stu-id="64ade-147">**SetWidth**</span></span>](id3dxline--setwidth.md)               | <span data-ttu-id="64ade-148">指定線條的粗細。</span><span class="sxs-lookup"><span data-stu-id="64ade-148">Specifies the thickness of the line.</span></span><br/>                                                                                                                                                  |



 

## <a name="remarks"></a><span data-ttu-id="64ade-149">備註</span><span class="sxs-lookup"><span data-stu-id="64ade-149">Remarks</span></span>

<span data-ttu-id="64ade-150">使用 [**D3DXCreateLine**](d3dxcreateline.md)建立線條繪圖物件。</span><span class="sxs-lookup"><span data-stu-id="64ade-150">Create a line drawing object with [**D3DXCreateLine**](d3dxcreateline.md).</span></span>

<span data-ttu-id="64ade-151">LPD3DXLINE 型別定義為 **ID3DXLine** 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="64ade-151">The LPD3DXLINE type is defined as a pointer to the **ID3DXLine** interface.</span></span>


```
typedef interface ID3DXLine ID3DXLine;
typedef interface ID3DXLine *LPD3DXLINE;
```



## <a name="requirements"></a><span data-ttu-id="64ade-152">規格需求</span><span class="sxs-lookup"><span data-stu-id="64ade-152">Requirements</span></span>



| <span data-ttu-id="64ade-153">需求</span><span class="sxs-lookup"><span data-stu-id="64ade-153">Requirement</span></span> | <span data-ttu-id="64ade-154">值</span><span class="sxs-lookup"><span data-stu-id="64ade-154">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="64ade-155">標頭</span><span class="sxs-lookup"><span data-stu-id="64ade-155">Header</span></span><br/>  | <dl> <span data-ttu-id="64ade-156"><dt>D3dx9core。h</dt></span><span class="sxs-lookup"><span data-stu-id="64ade-156"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="64ade-157">程式庫</span><span class="sxs-lookup"><span data-stu-id="64ade-157">Library</span></span><br/> | <dl> <span data-ttu-id="64ade-158"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="64ade-158"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="64ade-159">另請參閱</span><span class="sxs-lookup"><span data-stu-id="64ade-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64ade-160">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="64ade-160">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 

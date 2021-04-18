---
description: 應用程式會使用 ID3DXMATRIXStack 介面的方法來操作矩陣堆疊。
ms.assetid: 6c76f9e0-5f59-4cf3-b34a-2475536af6c7
title: 'ID3DXMatrixStack 介面 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMatrixStack
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 3d6956a6764683378c732c4ed859bfa13e537422
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323232"
---
# <a name="id3dxmatrixstack-interface"></a><span data-ttu-id="56121-103">ID3DXMatrixStack 介面</span><span class="sxs-lookup"><span data-stu-id="56121-103">ID3DXMatrixStack interface</span></span>

<span data-ttu-id="56121-104">應用程式會使用 ID3DXMATRIXStack 介面的方法來操作矩陣堆疊。</span><span class="sxs-lookup"><span data-stu-id="56121-104">Applications use the methods of the ID3DXMATRIXStack interface to manipulate a matrix stack.</span></span>

## <a name="members"></a><span data-ttu-id="56121-105">成員</span><span class="sxs-lookup"><span data-stu-id="56121-105">Members</span></span>

<span data-ttu-id="56121-106">**ID3DXMatrixStack** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="56121-106">The **ID3DXMatrixStack** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="56121-107">**ID3DXMatrixStack** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="56121-107">**ID3DXMatrixStack** also has these types of members:</span></span>

-   [<span data-ttu-id="56121-108">方法</span><span class="sxs-lookup"><span data-stu-id="56121-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="56121-109">方法</span><span class="sxs-lookup"><span data-stu-id="56121-109">Methods</span></span>

<span data-ttu-id="56121-110">**ID3DXMatrixStack** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="56121-110">The **ID3DXMatrixStack** interface has these methods.</span></span>



| <span data-ttu-id="56121-111">方法</span><span class="sxs-lookup"><span data-stu-id="56121-111">Method</span></span>                                                                      | <span data-ttu-id="56121-112">描述</span><span class="sxs-lookup"><span data-stu-id="56121-112">Description</span></span>                                                                                                                                |
|:----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="56121-113">**Vemap.gettop**</span><span class="sxs-lookup"><span data-stu-id="56121-113">**GetTop**</span></span>](id3dxmatrixstack-gettop.md)                                   | <span data-ttu-id="56121-114">抓取堆疊頂端的目前矩陣。</span><span class="sxs-lookup"><span data-stu-id="56121-114">Retrieves the current matrix at the top of the stack.</span></span><br/>                                                                           |
| [<span data-ttu-id="56121-115">**LoadIdentity**</span><span class="sxs-lookup"><span data-stu-id="56121-115">**LoadIdentity**</span></span>](id3dxmatrixstack-loadidentity.md)                       | <span data-ttu-id="56121-116">在目前的矩陣中載入識別。</span><span class="sxs-lookup"><span data-stu-id="56121-116">Loads identity in the current matrix.</span></span><br/>                                                                                           |
| [<span data-ttu-id="56121-117">**LoadMatrix**</span><span class="sxs-lookup"><span data-stu-id="56121-117">**LoadMatrix**</span></span>](id3dxmatrixstack-loadmatrix.md)                           | <span data-ttu-id="56121-118">將指定的矩陣載入至目前的矩陣。</span><span class="sxs-lookup"><span data-stu-id="56121-118">Loads the given matrix into the current matrix.</span></span><br/>                                                                                 |
| [<span data-ttu-id="56121-119">**MultMatrix**</span><span class="sxs-lookup"><span data-stu-id="56121-119">**MultMatrix**</span></span>](id3dxmatrixstack-multmatrix.md)                           | <span data-ttu-id="56121-120">決定目前矩陣和指定矩陣的乘積。</span><span class="sxs-lookup"><span data-stu-id="56121-120">Determines the product of the current matrix and the given matrix.</span></span><br/>                                                              |
| [<span data-ttu-id="56121-121">**MultMatrixLocal**</span><span class="sxs-lookup"><span data-stu-id="56121-121">**MultMatrixLocal**</span></span>](id3dxmatrixstack-multmatrixlocal.md)                 | <span data-ttu-id="56121-122">決定給定矩陣和目前矩陣的乘積。</span><span class="sxs-lookup"><span data-stu-id="56121-122">Determines the product of the given matrix and the current matrix.</span></span><br/>                                                              |
| [<span data-ttu-id="56121-123">**流行**</span><span class="sxs-lookup"><span data-stu-id="56121-123">**Pop**</span></span>](id3dxmatrixstack-pop.md)                                         | <span data-ttu-id="56121-124">從堆疊頂端移除目前的矩陣。</span><span class="sxs-lookup"><span data-stu-id="56121-124">Removes the current matrix from the top of the stack.</span></span><br/>                                                                           |
| [<span data-ttu-id="56121-125">**推**</span><span class="sxs-lookup"><span data-stu-id="56121-125">**Push**</span></span>](id3dxmatrixstack-push.md)                                       | <span data-ttu-id="56121-126">將矩陣加入至堆疊。</span><span class="sxs-lookup"><span data-stu-id="56121-126">Adds a matrix to the stack.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="56121-127">**RotateAxis**</span><span class="sxs-lookup"><span data-stu-id="56121-127">**RotateAxis**</span></span>](id3dxmatrixstack-rotateaxis.md)                           | <span data-ttu-id="56121-128">繞著任意軸的 (相對於全局座標空間) 旋轉。</span><span class="sxs-lookup"><span data-stu-id="56121-128">Rotates (relative to world coordinate space) around an arbitrary axis.</span></span><br/>                                                          |
| [<span data-ttu-id="56121-129">**RotateAxisLocal**</span><span class="sxs-lookup"><span data-stu-id="56121-129">**RotateAxisLocal**</span></span>](id3dxmatrixstack-rotateaxislocal.md)                 | <span data-ttu-id="56121-130">在任意軸周圍) 旋轉 (相對於物件的區域座標空間。</span><span class="sxs-lookup"><span data-stu-id="56121-130">Rotates (relative to the object's local coordinate space) around an arbitrary axis.</span></span><br/>                                             |
| [<span data-ttu-id="56121-131">**RotateYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="56121-131">**RotateYawPitchRoll**</span></span>](id3dxmatrixstack-rotateyawpitchroll.md)           | <span data-ttu-id="56121-132">繞著任意軸的 (相對於全局座標空間) 旋轉。</span><span class="sxs-lookup"><span data-stu-id="56121-132">Rotates (relative to world coordinate space) around an arbitrary axis.</span></span><br/>                                                          |
| [<span data-ttu-id="56121-133">**RotateYawPitchRollLocal**</span><span class="sxs-lookup"><span data-stu-id="56121-133">**RotateYawPitchRollLocal**</span></span>](id3dxmatrixstack-rotateyawpitchrolllocal.md) | <span data-ttu-id="56121-134">在任意軸周圍) 旋轉 (相對於物件的區域座標空間。</span><span class="sxs-lookup"><span data-stu-id="56121-134">Rotates (relative to the object's local coordinate space) around an arbitrary axis.</span></span><br/>                                             |
| [<span data-ttu-id="56121-135">**調整**</span><span class="sxs-lookup"><span data-stu-id="56121-135">**Scale**</span></span>](id3dxmatrixstack-scale.md)                                     | <span data-ttu-id="56121-136">調整目前的矩陣與全球座標原點的大小。</span><span class="sxs-lookup"><span data-stu-id="56121-136">Scale the current matrix about the world coordinate origin.</span></span><br/>                                                                     |
| [<span data-ttu-id="56121-137">**ScaleLocal**</span><span class="sxs-lookup"><span data-stu-id="56121-137">**ScaleLocal**</span></span>](id3dxmatrixstack-scalelocal.md)                           | <span data-ttu-id="56121-138">調整目前有關物件原點的矩陣。</span><span class="sxs-lookup"><span data-stu-id="56121-138">Scale the current matrix about the object origin.</span></span><br/>                                                                               |
| [<span data-ttu-id="56121-139">**翻譯**</span><span class="sxs-lookup"><span data-stu-id="56121-139">**Translate**</span></span>](id3dxmatrixstack-translate.md)                             | <span data-ttu-id="56121-140">決定目前矩陣的乘積，以及由給定因素 (x、y 和 z) 所決定的計算轉譯矩陣。</span><span class="sxs-lookup"><span data-stu-id="56121-140">Determines the product of the current matrix and the computed translation matrix determined by the given factors (x, y, and z).</span></span><br/> |
| [<span data-ttu-id="56121-141">**TranslateLocal**</span><span class="sxs-lookup"><span data-stu-id="56121-141">**TranslateLocal**</span></span>](id3dxmatrixstack-translatelocal.md)                   | <span data-ttu-id="56121-142">決定由給定因數決定的計算轉譯矩陣的乘積 (x、y 和 z) 和目前的矩陣。</span><span class="sxs-lookup"><span data-stu-id="56121-142">Determines the product of the computed translation matrix determined by the given factors (x, y, and z) and the current matrix.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="56121-143">備註</span><span class="sxs-lookup"><span data-stu-id="56121-143">Remarks</span></span>

<span data-ttu-id="56121-144">ID3DX10MATRIXStack 介面是藉由呼叫 [**D3DXCreateMatrixStack**](d3d10-d3dxcreatematrixstack.md) 函數來取得。</span><span class="sxs-lookup"><span data-stu-id="56121-144">The ID3DX10MATRIXStack interface is obtained by calling the [**D3DXCreateMatrixStack**](d3d10-d3dxcreatematrixstack.md) function.</span></span>

<span data-ttu-id="56121-145">LPD3DX10MATRIXSTACK 型別定義為 **ID3DXMatrixStack** 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="56121-145">The LPD3DX10MATRIXSTACK type is defined as a pointer to the **ID3DXMatrixStack** interface.</span></span>


```
typedef interface ID3DXMatrixStack ID3DXMatrixStack;
typedef interface ID3DXMatrixStack *LPD3DXMATRIXSTACK;
```



## <a name="requirements"></a><span data-ttu-id="56121-146">規格需求</span><span class="sxs-lookup"><span data-stu-id="56121-146">Requirements</span></span>



| <span data-ttu-id="56121-147">需求</span><span class="sxs-lookup"><span data-stu-id="56121-147">Requirement</span></span> | <span data-ttu-id="56121-148">值</span><span class="sxs-lookup"><span data-stu-id="56121-148">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="56121-149">標頭</span><span class="sxs-lookup"><span data-stu-id="56121-149">Header</span></span><br/>  | <dl> <span data-ttu-id="56121-150"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="56121-150"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="56121-151">程式庫</span><span class="sxs-lookup"><span data-stu-id="56121-151">Library</span></span><br/> | <dl> <span data-ttu-id="56121-152"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="56121-152"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56121-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="56121-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56121-154">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="56121-154">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 

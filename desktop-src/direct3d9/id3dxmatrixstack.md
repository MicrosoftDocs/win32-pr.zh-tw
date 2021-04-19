---
description: 應用程式會使用 ID3DXMATRIXStack 介面的方法來操作矩陣堆疊。
ms.assetid: 4d382d39-a9da-4a3b-b7b6-d6890357d467
title: 'ID3DXMATRIXStack 介面 (D3dx9math .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9446301ce057e788b4039f8ea3a144fb1fa19024
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106976519"
---
# <a name="id3dxmatrixstack-interface"></a><span data-ttu-id="203d7-103">ID3DXMATRIXStack 介面</span><span class="sxs-lookup"><span data-stu-id="203d7-103">ID3DXMATRIXStack interface</span></span>

<span data-ttu-id="203d7-104">應用程式會使用 ID3DXMATRIXStack 介面的方法來操作矩陣堆疊。</span><span class="sxs-lookup"><span data-stu-id="203d7-104">Applications use the methods of the ID3DXMATRIXStack interface to manipulate a matrix stack.</span></span>

## <a name="members"></a><span data-ttu-id="203d7-105">成員</span><span class="sxs-lookup"><span data-stu-id="203d7-105">Members</span></span>

<span data-ttu-id="203d7-106">**ID3DXMATRIXStack** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="203d7-106">The **ID3DXMATRIXStack** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="203d7-107">**ID3DXMATRIXStack** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="203d7-107">**ID3DXMATRIXStack** also has these types of members:</span></span>

-   [<span data-ttu-id="203d7-108">方法</span><span class="sxs-lookup"><span data-stu-id="203d7-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="203d7-109">方法</span><span class="sxs-lookup"><span data-stu-id="203d7-109">Methods</span></span>

<span data-ttu-id="203d7-110">**ID3DXMATRIXStack** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="203d7-110">The **ID3DXMATRIXStack** interface has these methods.</span></span>



| <span data-ttu-id="203d7-111">方法</span><span class="sxs-lookup"><span data-stu-id="203d7-111">Method</span></span>                                                                       | <span data-ttu-id="203d7-112">描述</span><span class="sxs-lookup"><span data-stu-id="203d7-112">Description</span></span>                                                                                                                                |
|:-----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="203d7-113">**Vemap.gettop**</span><span class="sxs-lookup"><span data-stu-id="203d7-113">**GetTop**</span></span>](id3dxmatrixstack--gettop.md)                                   | <span data-ttu-id="203d7-114">抓取堆疊頂端的目前矩陣。</span><span class="sxs-lookup"><span data-stu-id="203d7-114">Retrieves the current matrix at the top of the stack.</span></span><br/>                                                                           |
| [<span data-ttu-id="203d7-115">**LoadIdentity**</span><span class="sxs-lookup"><span data-stu-id="203d7-115">**LoadIdentity**</span></span>](id3dxmatrixstack--loadidentity.md)                       | <span data-ttu-id="203d7-116">在目前的矩陣中載入識別。</span><span class="sxs-lookup"><span data-stu-id="203d7-116">Loads identity in the current matrix.</span></span><br/>                                                                                           |
| [<span data-ttu-id="203d7-117">**LoadMatrix**</span><span class="sxs-lookup"><span data-stu-id="203d7-117">**LoadMatrix**</span></span>](id3dxmatrixstack--loadmatrix.md)                           | <span data-ttu-id="203d7-118">將指定的矩陣載入至目前的矩陣。</span><span class="sxs-lookup"><span data-stu-id="203d7-118">Loads the given matrix into the current matrix.</span></span><br/>                                                                                 |
| [<span data-ttu-id="203d7-119">**MultMatrix**</span><span class="sxs-lookup"><span data-stu-id="203d7-119">**MultMatrix**</span></span>](id3dxmatrixstack--multmatrix.md)                           | <span data-ttu-id="203d7-120">決定目前矩陣和指定矩陣的乘積。</span><span class="sxs-lookup"><span data-stu-id="203d7-120">Determines the product of the current matrix and the given matrix.</span></span><br/>                                                              |
| [<span data-ttu-id="203d7-121">**MultMatrixLocal**</span><span class="sxs-lookup"><span data-stu-id="203d7-121">**MultMatrixLocal**</span></span>](id3dxmatrixstack--multmatrixlocal.md)                 | <span data-ttu-id="203d7-122">決定給定矩陣和目前矩陣的乘積。</span><span class="sxs-lookup"><span data-stu-id="203d7-122">Determines the product of the given matrix and the current matrix.</span></span><br/>                                                              |
| [<span data-ttu-id="203d7-123">**流行**</span><span class="sxs-lookup"><span data-stu-id="203d7-123">**Pop**</span></span>](id3dxmatrixstack--pop.md)                                         | <span data-ttu-id="203d7-124">從堆疊頂端移除目前的矩陣。</span><span class="sxs-lookup"><span data-stu-id="203d7-124">Removes the current matrix from the top of the stack.</span></span><br/>                                                                           |
| [<span data-ttu-id="203d7-125">**推**</span><span class="sxs-lookup"><span data-stu-id="203d7-125">**Push**</span></span>](id3dxmatrixstack--push.md)                                       | <span data-ttu-id="203d7-126">將矩陣加入至堆疊。</span><span class="sxs-lookup"><span data-stu-id="203d7-126">Adds a matrix to the stack.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="203d7-127">**RotateAxis**</span><span class="sxs-lookup"><span data-stu-id="203d7-127">**RotateAxis**</span></span>](id3dxmatrixstack--rotateaxis.md)                           | <span data-ttu-id="203d7-128">繞著任意軸的 (相對於全局座標空間) 旋轉。</span><span class="sxs-lookup"><span data-stu-id="203d7-128">Rotates (relative to world coordinate space) around an arbitrary axis.</span></span><br/>                                                          |
| [<span data-ttu-id="203d7-129">**RotateAxisLocal**</span><span class="sxs-lookup"><span data-stu-id="203d7-129">**RotateAxisLocal**</span></span>](id3dxmatrixstack--rotateaxislocal.md)                 | <span data-ttu-id="203d7-130">在任意軸周圍) 旋轉 (相對於物件的區域座標空間。</span><span class="sxs-lookup"><span data-stu-id="203d7-130">Rotates (relative to the object's local coordinate space) around an arbitrary axis.</span></span><br/>                                             |
| [<span data-ttu-id="203d7-131">**RotateYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="203d7-131">**RotateYawPitchRoll**</span></span>](id3dxmatrixstack--rotateyawpitchroll.md)           | <span data-ttu-id="203d7-132">繞著任意軸的 (相對於全局座標空間) 旋轉。</span><span class="sxs-lookup"><span data-stu-id="203d7-132">Rotates (relative to world coordinate space) around an arbitrary axis.</span></span><br/>                                                          |
| [<span data-ttu-id="203d7-133">**RotateYawPitchRollLocal**</span><span class="sxs-lookup"><span data-stu-id="203d7-133">**RotateYawPitchRollLocal**</span></span>](id3dxmatrixstack--rotateyawpitchrolllocal.md) | <span data-ttu-id="203d7-134">在任意軸周圍) 旋轉 (相對於物件的區域座標空間。</span><span class="sxs-lookup"><span data-stu-id="203d7-134">Rotates (relative to the object's local coordinate space) around an arbitrary axis.</span></span><br/>                                             |
| [<span data-ttu-id="203d7-135">**調整**</span><span class="sxs-lookup"><span data-stu-id="203d7-135">**Scale**</span></span>](id3dxmatrixstack--scale.md)                                     | <span data-ttu-id="203d7-136">調整目前的矩陣與全球座標原點的大小。</span><span class="sxs-lookup"><span data-stu-id="203d7-136">Scale the current matrix about the world coordinate origin.</span></span><br/>                                                                     |
| [<span data-ttu-id="203d7-137">**ScaleLocal**</span><span class="sxs-lookup"><span data-stu-id="203d7-137">**ScaleLocal**</span></span>](id3dxmatrixstack--scalelocal.md)                           | <span data-ttu-id="203d7-138">調整目前有關物件原點的矩陣。</span><span class="sxs-lookup"><span data-stu-id="203d7-138">Scale the current matrix about the object origin.</span></span><br/>                                                                               |
| [<span data-ttu-id="203d7-139">**翻譯**</span><span class="sxs-lookup"><span data-stu-id="203d7-139">**Translate**</span></span>](id3dxmatrixstack--translate.md)                             | <span data-ttu-id="203d7-140">決定目前矩陣的乘積，以及由給定因素 (x、y 和 z) 所決定的計算轉譯矩陣。</span><span class="sxs-lookup"><span data-stu-id="203d7-140">Determines the product of the current matrix and the computed translation matrix determined by the given factors (x, y, and z).</span></span><br/> |
| [<span data-ttu-id="203d7-141">**TranslateLocal**</span><span class="sxs-lookup"><span data-stu-id="203d7-141">**TranslateLocal**</span></span>](id3dxmatrixstack--translatelocal.md)                   | <span data-ttu-id="203d7-142">決定由給定因數決定的計算轉譯矩陣的乘積 (x、y 和 z) 和目前的矩陣。</span><span class="sxs-lookup"><span data-stu-id="203d7-142">Determines the product of the computed translation matrix determined by the given factors (x, y, and z) and the current matrix.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="203d7-143">備註</span><span class="sxs-lookup"><span data-stu-id="203d7-143">Remarks</span></span>

<span data-ttu-id="203d7-144">**ID3DXMATRIXStack** 介面是藉由呼叫 [**D3DXCreateMatrixStack**](d3dxcreatematrixstack.md)函數來取得。</span><span class="sxs-lookup"><span data-stu-id="203d7-144">The **ID3DXMATRIXStack** interface is obtained by calling the [**D3DXCreateMatrixStack**](d3dxcreatematrixstack.md) function.</span></span>

<span data-ttu-id="203d7-145">LPD3DXMATRIXSTACK 型別定義為 **ID3DXMATRIXStack** 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="203d7-145">The LPD3DXMATRIXSTACK type is defined as a pointer to the **ID3DXMATRIXStack** interface.</span></span>


```
typedef interface ID3DXMATRIXStack ID3DXMATRIXStack;
typedef interface ID3DXMATRIXStack *LPD3DXMATRIXSTACK;
```



## <a name="requirements"></a><span data-ttu-id="203d7-146">規格需求</span><span class="sxs-lookup"><span data-stu-id="203d7-146">Requirements</span></span>



| <span data-ttu-id="203d7-147">需求</span><span class="sxs-lookup"><span data-stu-id="203d7-147">Requirement</span></span> | <span data-ttu-id="203d7-148">值</span><span class="sxs-lookup"><span data-stu-id="203d7-148">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="203d7-149">標頭</span><span class="sxs-lookup"><span data-stu-id="203d7-149">Header</span></span><br/>  | <dl> <span data-ttu-id="203d7-150"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="203d7-150"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="203d7-151">程式庫</span><span class="sxs-lookup"><span data-stu-id="203d7-151">Library</span></span><br/> | <dl> <span data-ttu-id="203d7-152"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="203d7-152"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="203d7-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="203d7-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="203d7-154">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="203d7-154">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 

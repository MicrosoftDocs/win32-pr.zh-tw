---
description: ID3DXTextureShader 介面。
ms.assetid: 48ea307d-857f-4b73-9e13-de391fbce07b
title: 'ID3DXTextureShader 介面 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c1b9581bced9d501800a8a8f3cb5d31a563ac261
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106974852"
---
# <a name="id3dxtextureshader-interface"></a><span data-ttu-id="9abef-103">ID3DXTextureShader 介面</span><span class="sxs-lookup"><span data-stu-id="9abef-103">ID3DXTextureShader interface</span></span>

<span data-ttu-id="9abef-104">ID3DXTextureShader 介面。</span><span class="sxs-lookup"><span data-stu-id="9abef-104">The ID3DXTextureShader interface.</span></span>

## <a name="members"></a><span data-ttu-id="9abef-105">成員</span><span class="sxs-lookup"><span data-stu-id="9abef-105">Members</span></span>

<span data-ttu-id="9abef-106">**ID3DXTextureShader** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="9abef-106">The **ID3DXTextureShader** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="9abef-107">**ID3DXTextureShader** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="9abef-107">**ID3DXTextureShader** also has these types of members:</span></span>

-   [<span data-ttu-id="9abef-108">方法</span><span class="sxs-lookup"><span data-stu-id="9abef-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="9abef-109">方法</span><span class="sxs-lookup"><span data-stu-id="9abef-109">Methods</span></span>

<span data-ttu-id="9abef-110">**ID3DXTextureShader** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="9abef-110">The **ID3DXTextureShader** interface has these methods.</span></span>



| <span data-ttu-id="9abef-111">方法</span><span class="sxs-lookup"><span data-stu-id="9abef-111">Method</span></span>                                                                                       | <span data-ttu-id="9abef-112">描述</span><span class="sxs-lookup"><span data-stu-id="9abef-112">Description</span></span>                                                                 |
|:---------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------|
| [<span data-ttu-id="9abef-113">**GetConstant**</span><span class="sxs-lookup"><span data-stu-id="9abef-113">**GetConstant**</span></span>](id3dxtextureshader--getconstant.md)                                       | <span data-ttu-id="9abef-114">藉由查閱索引來取得常數。</span><span class="sxs-lookup"><span data-stu-id="9abef-114">Gets a constant by looking up its index.</span></span><br/>                         |
| [<span data-ttu-id="9abef-115">**GetConstantBuffer**</span><span class="sxs-lookup"><span data-stu-id="9abef-115">**GetConstantBuffer**</span></span>](id3dxtextureshader--getconstantbuffer.md)                           | <span data-ttu-id="9abef-116">取得常數資料表的指標。</span><span class="sxs-lookup"><span data-stu-id="9abef-116">Get a pointer to the constant table.</span></span><br/>                             |
| [<span data-ttu-id="9abef-117">**GetConstantByName**</span><span class="sxs-lookup"><span data-stu-id="9abef-117">**GetConstantByName**</span></span>](id3dxtextureshader--getconstantbyname.md)                           | <span data-ttu-id="9abef-118">藉由查詢名稱來取得常數。</span><span class="sxs-lookup"><span data-stu-id="9abef-118">Gets a constant by looking up its name.</span></span><br/>                          |
| [<span data-ttu-id="9abef-119">**GetConstantDesc**</span><span class="sxs-lookup"><span data-stu-id="9abef-119">**GetConstantDesc**</span></span>](id3dxtextureshader--getconstantdesc.md)                               | <span data-ttu-id="9abef-120">取得常數資料表中常數陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="9abef-120">Gets a pointer to the array of constants in the constant table.</span></span><br/>  |
| [<span data-ttu-id="9abef-121">**GetConstantElement**</span><span class="sxs-lookup"><span data-stu-id="9abef-121">**GetConstantElement**</span></span>](id3dxtextureshader--getconstantelement.md)                         | <span data-ttu-id="9abef-122">從常數資料表取得常數。</span><span class="sxs-lookup"><span data-stu-id="9abef-122">Get a constant from the constant table.</span></span><br/>                          |
| [<span data-ttu-id="9abef-123">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="9abef-123">**GetDesc**</span></span>](id3dxtextureshader--getdesc.md)                                               | <span data-ttu-id="9abef-124">取得常數資料表的描述。</span><span class="sxs-lookup"><span data-stu-id="9abef-124">Gets a description of the constant table.</span></span><br/>                        |
| [<span data-ttu-id="9abef-125">**GetFunction**</span><span class="sxs-lookup"><span data-stu-id="9abef-125">**GetFunction**</span></span>](id3dxtextureshader--getfunction.md)                                       | <span data-ttu-id="9abef-126">取得函數 DWORD 資料流程的指標。</span><span class="sxs-lookup"><span data-stu-id="9abef-126">Gets a pointer to the function DWORD stream.</span></span><br/>                     |
| [<span data-ttu-id="9abef-127">**SetBool**</span><span class="sxs-lookup"><span data-stu-id="9abef-127">**SetBool**</span></span>](id3dxtextureshader--setbool.md)                                               | <span data-ttu-id="9abef-128">設定布林值。</span><span class="sxs-lookup"><span data-stu-id="9abef-128">Sets a BOOL value.</span></span><br/>                                               |
| [<span data-ttu-id="9abef-129">**SetBoolArray**</span><span class="sxs-lookup"><span data-stu-id="9abef-129">**SetBoolArray**</span></span>](id3dxtextureshader--setboolarray.md)                                     | <span data-ttu-id="9abef-130">設定 BOOL 值的陣列。</span><span class="sxs-lookup"><span data-stu-id="9abef-130">Sets an array of BOOL values.</span></span><br/>                                    |
| [<span data-ttu-id="9abef-131">**SetDefaults**</span><span class="sxs-lookup"><span data-stu-id="9abef-131">**SetDefaults**</span></span>](id3dxtextureshader--setdefaults.md)                                       | <span data-ttu-id="9abef-132">將常數設定為著色器中宣告的預設值。</span><span class="sxs-lookup"><span data-stu-id="9abef-132">Sets the constants to the default values declared in the shader.</span></span><br/> |
| [<span data-ttu-id="9abef-133">**SetFloat**</span><span class="sxs-lookup"><span data-stu-id="9abef-133">**SetFloat**</span></span>](id3dxtextureshader--setfloat.md)                                             | <span data-ttu-id="9abef-134">設定浮點數。</span><span class="sxs-lookup"><span data-stu-id="9abef-134">Sets a floating-point number.</span></span><br/>                                    |
| [<span data-ttu-id="9abef-135">**SetFloatArray**</span><span class="sxs-lookup"><span data-stu-id="9abef-135">**SetFloatArray**</span></span>](id3dxtextureshader--setfloatarray.md)                                   | <span data-ttu-id="9abef-136">設定浮點數字的陣列。</span><span class="sxs-lookup"><span data-stu-id="9abef-136">Sets an array of floating-point numbers.</span></span><br/>                         |
| [<span data-ttu-id="9abef-137">**SetInt**</span><span class="sxs-lookup"><span data-stu-id="9abef-137">**SetInt**</span></span>](id3dxtextureshader--setint.md)                                                 | <span data-ttu-id="9abef-138">設定整數值。</span><span class="sxs-lookup"><span data-stu-id="9abef-138">Sets an integer value.</span></span><br/>                                           |
| [<span data-ttu-id="9abef-139">**SetIntArray**</span><span class="sxs-lookup"><span data-stu-id="9abef-139">**SetIntArray**</span></span>](id3dxtextureshader--setintarray.md)                                       | <span data-ttu-id="9abef-140">設定整數的陣列。</span><span class="sxs-lookup"><span data-stu-id="9abef-140">Sets an array of integers.</span></span><br/>                                       |
| [<span data-ttu-id="9abef-141">**SetMatrix**</span><span class="sxs-lookup"><span data-stu-id="9abef-141">**SetMatrix**</span></span>](id3dxtextureshader--setmatrix.md)                                           | <span data-ttu-id="9abef-142">設定非轉換的矩陣。</span><span class="sxs-lookup"><span data-stu-id="9abef-142">Sets a non-transposed matrix.</span></span><br/>                                    |
| [<span data-ttu-id="9abef-143">**SetMatrixArray**</span><span class="sxs-lookup"><span data-stu-id="9abef-143">**SetMatrixArray**</span></span>](id3dxtextureshader--setmatrixarray.md)                                 | <span data-ttu-id="9abef-144">設定非轉換矩陣的陣列。</span><span class="sxs-lookup"><span data-stu-id="9abef-144">Sets an array of non-transposed matrices.</span></span><br/>                        |
| [<span data-ttu-id="9abef-145">**SetMatrixPointerArray**</span><span class="sxs-lookup"><span data-stu-id="9abef-145">**SetMatrixPointerArray**</span></span>](id3dxtextureshader--setmatrixpointerarray.md)                   | <span data-ttu-id="9abef-146">將指標的陣列設定為非轉換的矩陣。</span><span class="sxs-lookup"><span data-stu-id="9abef-146">Sets an array of pointers to non-transposed matrices.</span></span><br/>            |
| [<span data-ttu-id="9abef-147">**SetMatrixTranspose**</span><span class="sxs-lookup"><span data-stu-id="9abef-147">**SetMatrixTranspose**</span></span>](id3dxtextureshader--setmatrixtranspose.md)                         | <span data-ttu-id="9abef-148">設定已轉置的矩陣。</span><span class="sxs-lookup"><span data-stu-id="9abef-148">Sets a transposed matrix.</span></span><br/>                                        |
| [<span data-ttu-id="9abef-149">**SetMatrixTransposeArray**</span><span class="sxs-lookup"><span data-stu-id="9abef-149">**SetMatrixTransposeArray**</span></span>](id3dxtextureshader--setmatrixtransposearray.md)               | <span data-ttu-id="9abef-150">設定已轉置矩陣的陣列。</span><span class="sxs-lookup"><span data-stu-id="9abef-150">Sets an array of transposed matrices.</span></span><br/>                            |
| [<span data-ttu-id="9abef-151">**SetMatrixTransposePointerArray**</span><span class="sxs-lookup"><span data-stu-id="9abef-151">**SetMatrixTransposePointerArray**</span></span>](id3dxtextureshader--setmatrixtransposepointerarray.md) | <span data-ttu-id="9abef-152">將指標的陣列設定為已轉置的矩陣。</span><span class="sxs-lookup"><span data-stu-id="9abef-152">Sets an array of pointers to transposed matrices.</span></span><br/>                |
| [<span data-ttu-id="9abef-153">**SetValue**</span><span class="sxs-lookup"><span data-stu-id="9abef-153">**SetValue**</span></span>](id3dxtextureshader--setvalue.md)                                             | <span data-ttu-id="9abef-154">使用緩衝區中的資料來設定常數資料表。</span><span class="sxs-lookup"><span data-stu-id="9abef-154">Sets the constant table with the data in the buffer.</span></span><br/>             |
| [<span data-ttu-id="9abef-155">**SetVector**</span><span class="sxs-lookup"><span data-stu-id="9abef-155">**SetVector**</span></span>](id3dxtextureshader--setvector.md)                                           | <span data-ttu-id="9abef-156">設定4D 向量。</span><span class="sxs-lookup"><span data-stu-id="9abef-156">Sets a 4D vector.</span></span><br/>                                                |
| [<span data-ttu-id="9abef-157">**SetVectorArray**</span><span class="sxs-lookup"><span data-stu-id="9abef-157">**SetVectorArray**</span></span>](id3dxtextureshader--setvectorarray.md)                                 | <span data-ttu-id="9abef-158">設定4D 向量的陣列。</span><span class="sxs-lookup"><span data-stu-id="9abef-158">Sets an array of 4D vectors.</span></span><br/>                                     |



 

## <a name="remarks"></a><span data-ttu-id="9abef-159">備註</span><span class="sxs-lookup"><span data-stu-id="9abef-159">Remarks</span></span>

<span data-ttu-id="9abef-160">**ID3DXTextureShader** 介面是藉由呼叫 [**D3DXCreateTextureShader**](d3dxcreatetextureshader.md)函數來取得。</span><span class="sxs-lookup"><span data-stu-id="9abef-160">The **ID3DXTextureShader** interface is obtained by calling the [**D3DXCreateTextureShader**](d3dxcreatetextureshader.md) function.</span></span>

<span data-ttu-id="9abef-161">**ID3DXTextureShader** 介面就像所有的 COM 介面，會繼承 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="9abef-161">The **ID3DXTextureShader** interface, like all COM interfaces, inherits the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span>

<span data-ttu-id="9abef-162">LPD3DXTEXTURESHADER 型別定義為 **ID3DXTextureShader** 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="9abef-162">The LPD3DXTEXTURESHADER type is defined as a pointer to the **ID3DXTextureShader** interface.</span></span>


```
typedef interface ID3DXTextureShader *LPD3DXTEXTURESHADER;
```



## <a name="requirements"></a><span data-ttu-id="9abef-163">規格需求</span><span class="sxs-lookup"><span data-stu-id="9abef-163">Requirements</span></span>



| <span data-ttu-id="9abef-164">需求</span><span class="sxs-lookup"><span data-stu-id="9abef-164">Requirement</span></span> | <span data-ttu-id="9abef-165">值</span><span class="sxs-lookup"><span data-stu-id="9abef-165">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9abef-166">標頭</span><span class="sxs-lookup"><span data-stu-id="9abef-166">Header</span></span><br/>  | <dl> <span data-ttu-id="9abef-167"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="9abef-167"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="9abef-168">程式庫</span><span class="sxs-lookup"><span data-stu-id="9abef-168">Library</span></span><br/> | <dl> <span data-ttu-id="9abef-169"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="9abef-169"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="9abef-170">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9abef-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9abef-171">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="9abef-171">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 

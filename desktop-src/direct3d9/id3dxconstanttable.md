---
description: ID3DXConstantTable 介面是用來存取常數資料表。 此資料表包含高階語言著色器和效果所使用的變數。
ms.assetid: 5d412c77-3d35-4913-86e5-8efa0549a2bb
title: 'ID3DXConstantTable 介面 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bb2b7614c4d6a0e677f71e66ab94abdb89deb973
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982210"
---
# <a name="id3dxconstanttable-interface"></a><span data-ttu-id="46715-104">ID3DXConstantTable 介面</span><span class="sxs-lookup"><span data-stu-id="46715-104">ID3DXConstantTable interface</span></span>

<span data-ttu-id="46715-105">ID3DXConstantTable 介面是用來存取常數資料表。</span><span class="sxs-lookup"><span data-stu-id="46715-105">The ID3DXConstantTable interface is used to access the constant table.</span></span> <span data-ttu-id="46715-106">此資料表包含高階語言著色器和效果所使用的變數。</span><span class="sxs-lookup"><span data-stu-id="46715-106">This table contains the variables that are used by high-level language shaders and effects.</span></span>

## <a name="members"></a><span data-ttu-id="46715-107">成員</span><span class="sxs-lookup"><span data-stu-id="46715-107">Members</span></span>

<span data-ttu-id="46715-108">**ID3DXConstantTable** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="46715-108">The **ID3DXConstantTable** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="46715-109">**ID3DXConstantTable** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="46715-109">**ID3DXConstantTable** also has these types of members:</span></span>

-   [<span data-ttu-id="46715-110">方法</span><span class="sxs-lookup"><span data-stu-id="46715-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="46715-111">方法</span><span class="sxs-lookup"><span data-stu-id="46715-111">Methods</span></span>

<span data-ttu-id="46715-112">**ID3DXConstantTable** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="46715-112">The **ID3DXConstantTable** interface has these methods.</span></span>



| <span data-ttu-id="46715-113">方法</span><span class="sxs-lookup"><span data-stu-id="46715-113">Method</span></span>                                                                                       | <span data-ttu-id="46715-114">描述</span><span class="sxs-lookup"><span data-stu-id="46715-114">Description</span></span>                                                                                                                        |
|:---------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="46715-115">**GetBufferPointer**</span><span class="sxs-lookup"><span data-stu-id="46715-115">**GetBufferPointer**</span></span>](id3dxconstanttable--getbufferpointer.md)                             | <span data-ttu-id="46715-116">取得包含常數資料表之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="46715-116">Gets a pointer to the buffer that contains the constant table.</span></span><br/>                                                          |
| [<span data-ttu-id="46715-117">**GetBufferSize**</span><span class="sxs-lookup"><span data-stu-id="46715-117">**GetBufferSize**</span></span>](id3dxconstanttable--getbuffersize.md)                                   | <span data-ttu-id="46715-118">取得常數資料表的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="46715-118">Gets the buffer size of the constant table.</span></span><br/>                                                                             |
| [<span data-ttu-id="46715-119">**GetConstant**</span><span class="sxs-lookup"><span data-stu-id="46715-119">**GetConstant**</span></span>](id3dxconstanttable--getconstant.md)                                       | <span data-ttu-id="46715-120">藉由查閱索引來取得常數。</span><span class="sxs-lookup"><span data-stu-id="46715-120">Gets a constant by looking up its index.</span></span><br/>                                                                                |
| [<span data-ttu-id="46715-121">**GetConstantByName**</span><span class="sxs-lookup"><span data-stu-id="46715-121">**GetConstantByName**</span></span>](id3dxconstanttable--getconstantbyname.md)                           | <span data-ttu-id="46715-122">藉由查詢名稱來取得常數。</span><span class="sxs-lookup"><span data-stu-id="46715-122">Gets a constant by looking up its name.</span></span><br/>                                                                                 |
| [<span data-ttu-id="46715-123">**GetConstantDesc**</span><span class="sxs-lookup"><span data-stu-id="46715-123">**GetConstantDesc**</span></span>](id3dxconstanttable--getconstantdesc.md)                               | <span data-ttu-id="46715-124">取得常數資料表中常數描述陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="46715-124">Gets a pointer to an array of constant descriptions in the constant table.</span></span><br/>                                              |
| [<span data-ttu-id="46715-125">**GetConstantElement**</span><span class="sxs-lookup"><span data-stu-id="46715-125">**GetConstantElement**</span></span>](id3dxconstanttable--getconstantelement.md)                         | <span data-ttu-id="46715-126">從常數的陣列取得常數。</span><span class="sxs-lookup"><span data-stu-id="46715-126">Gets a constant from an array of constants.</span></span> <span data-ttu-id="46715-127">陣列是由元素所組成。</span><span class="sxs-lookup"><span data-stu-id="46715-127">An array is made up of elements.</span></span><br/>                                            |
| [<span data-ttu-id="46715-128">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="46715-128">**GetDesc**</span></span>](id3dxconstanttable--getdesc.md)                                               | <span data-ttu-id="46715-129">取得常數資料表的描述。</span><span class="sxs-lookup"><span data-stu-id="46715-129">Gets a description of the constant table.</span></span><br/>                                                                               |
| [<span data-ttu-id="46715-130">**GetSamplerIndex**</span><span class="sxs-lookup"><span data-stu-id="46715-130">**GetSamplerIndex**</span></span>](id3dxconstanttable--getsamplerindex.md)                               | <span data-ttu-id="46715-131">傳回取樣器索引。</span><span class="sxs-lookup"><span data-stu-id="46715-131">Returns the sampler index.</span></span><br/>                                                                                              |
| [<span data-ttu-id="46715-132">**SetBool**</span><span class="sxs-lookup"><span data-stu-id="46715-132">**SetBool**</span></span>](id3dxconstanttable--setbool.md)                                               | <span data-ttu-id="46715-133">設定布林值。</span><span class="sxs-lookup"><span data-stu-id="46715-133">Sets a Boolean value.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="46715-134">**SetBoolArray**</span><span class="sxs-lookup"><span data-stu-id="46715-134">**SetBoolArray**</span></span>](id3dxconstanttable--setboolarray.md)                                     | <span data-ttu-id="46715-135">設定布林值的陣列。</span><span class="sxs-lookup"><span data-stu-id="46715-135">Sets an array of Boolean values.</span></span><br/>                                                                                        |
| [<span data-ttu-id="46715-136">**SetDefaults**</span><span class="sxs-lookup"><span data-stu-id="46715-136">**SetDefaults**</span></span>](id3dxconstanttable--setdefaults.md)                                       | <span data-ttu-id="46715-137">將常數設定為其預設值。</span><span class="sxs-lookup"><span data-stu-id="46715-137">Sets the constants to their default values.</span></span> <span data-ttu-id="46715-138">預設值會在著色器的變數宣告中宣告。</span><span class="sxs-lookup"><span data-stu-id="46715-138">The default values are declared in the variable declarations in the shader.</span></span><br/> |
| [<span data-ttu-id="46715-139">**SetFloat**</span><span class="sxs-lookup"><span data-stu-id="46715-139">**SetFloat**</span></span>](id3dxconstanttable--setfloat.md)                                             | <span data-ttu-id="46715-140">設定浮點數。</span><span class="sxs-lookup"><span data-stu-id="46715-140">Sets a floating-point number.</span></span><br/>                                                                                           |
| [<span data-ttu-id="46715-141">**SetFloatArray**</span><span class="sxs-lookup"><span data-stu-id="46715-141">**SetFloatArray**</span></span>](id3dxconstanttable--setfloatarray.md)                                   | <span data-ttu-id="46715-142">設定浮點數字的陣列。</span><span class="sxs-lookup"><span data-stu-id="46715-142">Sets an array of floating-point numbers.</span></span><br/>                                                                                |
| [<span data-ttu-id="46715-143">**SetInt**</span><span class="sxs-lookup"><span data-stu-id="46715-143">**SetInt**</span></span>](id3dxconstanttable--setint.md)                                                 | <span data-ttu-id="46715-144">設定整數值。</span><span class="sxs-lookup"><span data-stu-id="46715-144">Sets an integer value.</span></span><br/>                                                                                                  |
| [<span data-ttu-id="46715-145">**SetIntArray**</span><span class="sxs-lookup"><span data-stu-id="46715-145">**SetIntArray**</span></span>](id3dxconstanttable--setintarray.md)                                       | <span data-ttu-id="46715-146">設定整數的陣列。</span><span class="sxs-lookup"><span data-stu-id="46715-146">Sets an array of integers.</span></span><br/>                                                                                              |
| [<span data-ttu-id="46715-147">**SetMatrix**</span><span class="sxs-lookup"><span data-stu-id="46715-147">**SetMatrix**</span></span>](id3dxconstanttable--setmatrix.md)                                           | <span data-ttu-id="46715-148">設定 nontransposed 矩陣。</span><span class="sxs-lookup"><span data-stu-id="46715-148">Sets a nontransposed matrix.</span></span><br/>                                                                                            |
| [<span data-ttu-id="46715-149">**SetMatrixArray**</span><span class="sxs-lookup"><span data-stu-id="46715-149">**SetMatrixArray**</span></span>](id3dxconstanttable--setmatrixarray.md)                                 | <span data-ttu-id="46715-150">設定 nontransposed 矩陣的陣列。</span><span class="sxs-lookup"><span data-stu-id="46715-150">Sets an array of nontransposed matrices.</span></span><br/>                                                                                |
| [<span data-ttu-id="46715-151">**SetMatrixPointerArray**</span><span class="sxs-lookup"><span data-stu-id="46715-151">**SetMatrixPointerArray**</span></span>](id3dxconstanttable--setmatrixpointerarray.md)                   | <span data-ttu-id="46715-152">設定 nontransposed 矩陣的指標陣列。</span><span class="sxs-lookup"><span data-stu-id="46715-152">Sets an array of pointers to nontransposed matrices.</span></span><br/>                                                                    |
| [<span data-ttu-id="46715-153">**SetMatrixTranspose**</span><span class="sxs-lookup"><span data-stu-id="46715-153">**SetMatrixTranspose**</span></span>](id3dxconstanttable--setmatrixtranspose.md)                         | <span data-ttu-id="46715-154">設定已轉置的矩陣。</span><span class="sxs-lookup"><span data-stu-id="46715-154">Sets a transposed matrix.</span></span><br/>                                                                                               |
| [<span data-ttu-id="46715-155">**SetMatrixTransposeArray**</span><span class="sxs-lookup"><span data-stu-id="46715-155">**SetMatrixTransposeArray**</span></span>](id3dxconstanttable--setmatrixtransposearray.md)               | <span data-ttu-id="46715-156">設定已轉置矩陣的陣列。</span><span class="sxs-lookup"><span data-stu-id="46715-156">Sets an array of transposed matrices.</span></span><br/>                                                                                   |
| [<span data-ttu-id="46715-157">**SetMatrixTransposePointerArray**</span><span class="sxs-lookup"><span data-stu-id="46715-157">**SetMatrixTransposePointerArray**</span></span>](id3dxconstanttable--setmatrixtransposepointerarray.md) | <span data-ttu-id="46715-158">將指標的陣列設定為已轉置的矩陣。</span><span class="sxs-lookup"><span data-stu-id="46715-158">Sets an array of pointers to transposed matrices.</span></span><br/>                                                                       |
| [<span data-ttu-id="46715-159">**SetValue**</span><span class="sxs-lookup"><span data-stu-id="46715-159">**SetValue**</span></span>](id3dxconstanttable--setvalue.md)                                             | <span data-ttu-id="46715-160">將緩衝區的內容設定為常數資料表。</span><span class="sxs-lookup"><span data-stu-id="46715-160">Sets the contents of the buffer to the constant table.</span></span><br/>                                                                  |
| [<span data-ttu-id="46715-161">**SetVector**</span><span class="sxs-lookup"><span data-stu-id="46715-161">**SetVector**</span></span>](id3dxconstanttable--setvector.md)                                           | <span data-ttu-id="46715-162">設定4D 向量。</span><span class="sxs-lookup"><span data-stu-id="46715-162">Sets a 4D vector.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="46715-163">**SetVectorArray**</span><span class="sxs-lookup"><span data-stu-id="46715-163">**SetVectorArray**</span></span>](id3dxconstanttable--setvectorarray.md)                                 | <span data-ttu-id="46715-164">設定4D 向量的陣列。</span><span class="sxs-lookup"><span data-stu-id="46715-164">Sets an array of 4D vectors.</span></span><br/>                                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="46715-165">備註</span><span class="sxs-lookup"><span data-stu-id="46715-165">Remarks</span></span>

<span data-ttu-id="46715-166">LPD3DXCONSTANTTABLE 型別定義為 **ID3DXConstantTable** 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="46715-166">The LPD3DXCONSTANTTABLE type is defined as a pointer to the **ID3DXConstantTable** interface.</span></span>


```
typedef interface ID3DXConstantTable ID3DXConstantTable;
typedef interface ID3DXConstantTable *LPD3DXCONSTANTTABLE;
```



## <a name="requirements"></a><span data-ttu-id="46715-167">規格需求</span><span class="sxs-lookup"><span data-stu-id="46715-167">Requirements</span></span>



| <span data-ttu-id="46715-168">需求</span><span class="sxs-lookup"><span data-stu-id="46715-168">Requirement</span></span> | <span data-ttu-id="46715-169">值</span><span class="sxs-lookup"><span data-stu-id="46715-169">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="46715-170">標頭</span><span class="sxs-lookup"><span data-stu-id="46715-170">Header</span></span><br/>  | <dl> <span data-ttu-id="46715-171"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="46715-171"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="46715-172">程式庫</span><span class="sxs-lookup"><span data-stu-id="46715-172">Library</span></span><br/> | <dl> <span data-ttu-id="46715-173"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="46715-173"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="46715-174">另請參閱</span><span class="sxs-lookup"><span data-stu-id="46715-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46715-175">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="46715-175">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 

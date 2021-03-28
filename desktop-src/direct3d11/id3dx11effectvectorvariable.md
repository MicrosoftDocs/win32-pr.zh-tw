---
title: 'ID3DX11EffectVectorVariable 介面 (D3dx11effect .h) '
description: 向量變數介面會存取四個元件的向量。
ms.assetid: 191d373b-0562-4d7b-ac3f-cd24abf259bc
keywords:
- ID3DX11EffectVectorVariable 介面 Direct3D 11
- ID3DX11EffectVectorVariable 介面 Direct3D 11，描述
topic_type:
- apiref
api_name:
- ID3DX11EffectVectorVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9235a4047617dd2e5ff9f14925908ae7a0dc1060
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992126"
---
# <a name="id3dx11effectvectorvariable-interface"></a><span data-ttu-id="25a20-105">ID3DX11EffectVectorVariable 介面</span><span class="sxs-lookup"><span data-stu-id="25a20-105">ID3DX11EffectVectorVariable interface</span></span>

<span data-ttu-id="25a20-106">向量變數介面會存取四個元件的向量。</span><span class="sxs-lookup"><span data-stu-id="25a20-106">A vector-variable interface accesses a four-component vector.</span></span>

## <a name="members"></a><span data-ttu-id="25a20-107">成員</span><span class="sxs-lookup"><span data-stu-id="25a20-107">Members</span></span>

<span data-ttu-id="25a20-108">**ID3DX11EffectVectorVariable** 介面繼承自 [**ID3DX11EffectVariable**](id3dx11effectvariable.md)。</span><span class="sxs-lookup"><span data-stu-id="25a20-108">The **ID3DX11EffectVectorVariable** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="25a20-109">**ID3DX11EffectVectorVariable** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="25a20-109">**ID3DX11EffectVectorVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="25a20-110">方法</span><span class="sxs-lookup"><span data-stu-id="25a20-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="25a20-111">方法</span><span class="sxs-lookup"><span data-stu-id="25a20-111">Methods</span></span>

<span data-ttu-id="25a20-112">**ID3DX11EffectVectorVariable** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="25a20-112">The **ID3DX11EffectVectorVariable** interface has these methods.</span></span>



| <span data-ttu-id="25a20-113">方法</span><span class="sxs-lookup"><span data-stu-id="25a20-113">Method</span></span>                                                                         | <span data-ttu-id="25a20-114">描述</span><span class="sxs-lookup"><span data-stu-id="25a20-114">Description</span></span>                                                                         |
|:-------------------------------------------------------------------------------|:------------------------------------------------------------------------------------|
| [<span data-ttu-id="25a20-115">**GetBoolVector**</span><span class="sxs-lookup"><span data-stu-id="25a20-115">**GetBoolVector**</span></span>](id3dx11effectvectorvariable-getboolvector.md)             | <span data-ttu-id="25a20-116">取得包含布林資料的四個元件向量。</span><span class="sxs-lookup"><span data-stu-id="25a20-116">Get a four-component vector that contains boolean data.</span></span><br/>                  |
| [<span data-ttu-id="25a20-117">**GetBoolVectorArray**</span><span class="sxs-lookup"><span data-stu-id="25a20-117">**GetBoolVectorArray**</span></span>](id3dx11effectvectorvariable-getboolvectorarray.md)   | <span data-ttu-id="25a20-118">取得四個元件向量的陣列，其中包含布林資料。</span><span class="sxs-lookup"><span data-stu-id="25a20-118">Get an array of four-component vectors that contain boolean data.</span></span><br/>        |
| [<span data-ttu-id="25a20-119">**GetFloatVector**</span><span class="sxs-lookup"><span data-stu-id="25a20-119">**GetFloatVector**</span></span>](id3dx11effectvectorvariable-getfloatvector.md)           | <span data-ttu-id="25a20-120">取得包含浮點數據的四個元件向量。</span><span class="sxs-lookup"><span data-stu-id="25a20-120">Get a four-component vector that contains floating-point data.</span></span><br/>           |
| [<span data-ttu-id="25a20-121">**GetFloatVectorArray**</span><span class="sxs-lookup"><span data-stu-id="25a20-121">**GetFloatVectorArray**</span></span>](id3dx11effectvectorvariable-getfloatvectorarray.md) | <span data-ttu-id="25a20-122">取得包含浮點數據之四個元件向量的陣列。</span><span class="sxs-lookup"><span data-stu-id="25a20-122">Get an array of four-component vectors that contain floating-point data.</span></span><br/> |
| [<span data-ttu-id="25a20-123">**GetIntVector**</span><span class="sxs-lookup"><span data-stu-id="25a20-123">**GetIntVector**</span></span>](id3dx11effectvectorvariable-getintvector.md)               | <span data-ttu-id="25a20-124">取得包含整數資料的四個元件向量。</span><span class="sxs-lookup"><span data-stu-id="25a20-124">Get a four-component vector that contains integer data.</span></span><br/>                  |
| [<span data-ttu-id="25a20-125">**GetIntVectorArray**</span><span class="sxs-lookup"><span data-stu-id="25a20-125">**GetIntVectorArray**</span></span>](id3dx11effectvectorvariable-getintvectorarray.md)     | <span data-ttu-id="25a20-126">取得四個元件向量的陣列，其中包含整數資料。</span><span class="sxs-lookup"><span data-stu-id="25a20-126">Get an array of four-component vectors that contain integer data.</span></span><br/>        |
| [<span data-ttu-id="25a20-127">**SetBoolVector**</span><span class="sxs-lookup"><span data-stu-id="25a20-127">**SetBoolVector**</span></span>](id3dx11effectvectorvariable-setboolvector.md)             | <span data-ttu-id="25a20-128">設定包含布林資料的四個元件向量。</span><span class="sxs-lookup"><span data-stu-id="25a20-128">Set a four-component vector that contains boolean data.</span></span><br/>                  |
| [<span data-ttu-id="25a20-129">**SetBoolVectorArray**</span><span class="sxs-lookup"><span data-stu-id="25a20-129">**SetBoolVectorArray**</span></span>](id3dx11effectvectorvariable-setboolvectorarray.md)   | <span data-ttu-id="25a20-130">設定包含布林資料之四個元件向量的陣列。</span><span class="sxs-lookup"><span data-stu-id="25a20-130">Set an array of four-component vectors that contain boolean data.</span></span><br/>        |
| [<span data-ttu-id="25a20-131">**SetFloatVector**</span><span class="sxs-lookup"><span data-stu-id="25a20-131">**SetFloatVector**</span></span>](id3dx11effectvectorvariable-setfloatvector.md)           | <span data-ttu-id="25a20-132">設定包含浮點數據的四個元件向量。</span><span class="sxs-lookup"><span data-stu-id="25a20-132">Set a four-component vector that contains floating-point data.</span></span><br/>           |
| [<span data-ttu-id="25a20-133">**SetFloatVectorArray**</span><span class="sxs-lookup"><span data-stu-id="25a20-133">**SetFloatVectorArray**</span></span>](id3dx11effectvectorvariable-setfloatvectorarray.md) | <span data-ttu-id="25a20-134">設定包含浮點數據之四個元件向量的陣列。</span><span class="sxs-lookup"><span data-stu-id="25a20-134">Set an array of four-component vectors that contain floating-point data.</span></span><br/> |
| [<span data-ttu-id="25a20-135">**SetIntVector**</span><span class="sxs-lookup"><span data-stu-id="25a20-135">**SetIntVector**</span></span>](id3dx11effectvectorvariable-setintvector.md)               | <span data-ttu-id="25a20-136">設定包含整數資料的四個元件向量。</span><span class="sxs-lookup"><span data-stu-id="25a20-136">Set a four-component vector that contains integer data.</span></span><br/>                  |
| [<span data-ttu-id="25a20-137">**SetIntVectorArray**</span><span class="sxs-lookup"><span data-stu-id="25a20-137">**SetIntVectorArray**</span></span>](id3dx11effectvectorvariable-setintvectorarray.md)     | <span data-ttu-id="25a20-138">設定包含整數資料之四個元件向量的陣列。</span><span class="sxs-lookup"><span data-stu-id="25a20-138">Set an array of four-component vectors that contain integer data.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="25a20-139">備註</span><span class="sxs-lookup"><span data-stu-id="25a20-139">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="25a20-140">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="25a20-140">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="25a20-141">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="25a20-141">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="25a20-142">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="25a20-142">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="25a20-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="25a20-143">Requirements</span></span>



| <span data-ttu-id="25a20-144">需求</span><span class="sxs-lookup"><span data-stu-id="25a20-144">Requirement</span></span> | <span data-ttu-id="25a20-145">值</span><span class="sxs-lookup"><span data-stu-id="25a20-145">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25a20-146">標頭</span><span class="sxs-lookup"><span data-stu-id="25a20-146">Header</span></span><br/>  | <dl> <span data-ttu-id="25a20-147"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="25a20-147"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="25a20-148">程式庫</span><span class="sxs-lookup"><span data-stu-id="25a20-148">Library</span></span><br/> | <dl> <span data-ttu-id="25a20-149"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="25a20-149"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25a20-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="25a20-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25a20-151">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="25a20-151">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="25a20-152">效果11介面</span><span class="sxs-lookup"><span data-stu-id="25a20-152">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="25a20-153">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="25a20-153">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 






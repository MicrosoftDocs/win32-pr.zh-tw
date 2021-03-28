---
title: 'ID3DX11EffectMatrixVariable 介面 (D3dx11effect .h) '
description: 矩陣變數介面會存取矩陣。
ms.assetid: 44f30d1a-3ec1-49d7-92c0-475cf2fa4d2a
keywords:
- ID3DX11EffectMatrixVariable 介面 Direct3D 11
- ID3DX11EffectMatrixVariable 介面 Direct3D 11，描述
topic_type:
- apiref
api_name:
- ID3DX11EffectMatrixVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5c4c89a231d429fc0a1f8fecbcbb4d06db35cb5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974621"
---
# <a name="id3dx11effectmatrixvariable-interface"></a><span data-ttu-id="af6a9-105">ID3DX11EffectMatrixVariable 介面</span><span class="sxs-lookup"><span data-stu-id="af6a9-105">ID3DX11EffectMatrixVariable interface</span></span>

<span data-ttu-id="af6a9-106">矩陣變數介面會存取矩陣。</span><span class="sxs-lookup"><span data-stu-id="af6a9-106">A matrix-variable interface accesses a matrix.</span></span>

## <a name="members"></a><span data-ttu-id="af6a9-107">成員</span><span class="sxs-lookup"><span data-stu-id="af6a9-107">Members</span></span>

<span data-ttu-id="af6a9-108">**ID3DX11EffectMatrixVariable** 介面繼承自 [**ID3DX11EffectVariable**](id3dx11effectvariable.md)。</span><span class="sxs-lookup"><span data-stu-id="af6a9-108">The **ID3DX11EffectMatrixVariable** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="af6a9-109">**ID3DX11EffectMatrixVariable** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="af6a9-109">**ID3DX11EffectMatrixVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="af6a9-110">方法</span><span class="sxs-lookup"><span data-stu-id="af6a9-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="af6a9-111">方法</span><span class="sxs-lookup"><span data-stu-id="af6a9-111">Methods</span></span>

<span data-ttu-id="af6a9-112">**ID3DX11EffectMatrixVariable** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="af6a9-112">The **ID3DX11EffectMatrixVariable** interface has these methods.</span></span>



| <span data-ttu-id="af6a9-113">方法</span><span class="sxs-lookup"><span data-stu-id="af6a9-113">Method</span></span>                                                                                 | <span data-ttu-id="af6a9-114">描述</span><span class="sxs-lookup"><span data-stu-id="af6a9-114">Description</span></span>                                                       |
|:---------------------------------------------------------------------------------------|:------------------------------------------------------------------|
| [<span data-ttu-id="af6a9-115">**GetMatrix**</span><span class="sxs-lookup"><span data-stu-id="af6a9-115">**GetMatrix**</span></span>](id3dx11effectmatrixvariable-getmatrix.md)                             | <span data-ttu-id="af6a9-116">取得矩陣。</span><span class="sxs-lookup"><span data-stu-id="af6a9-116">Get a matrix.</span></span><br/>                                          |
| [<span data-ttu-id="af6a9-117">**GetMatrixArray**</span><span class="sxs-lookup"><span data-stu-id="af6a9-117">**GetMatrixArray**</span></span>](id3dx11effectmatrixvariable-getmatrixarray.md)                   | <span data-ttu-id="af6a9-118">取得矩陣的陣列。</span><span class="sxs-lookup"><span data-stu-id="af6a9-118">Get an array of matrices.</span></span><br/>                              |
| [<span data-ttu-id="af6a9-119">**GetMatrixTranspose**</span><span class="sxs-lookup"><span data-stu-id="af6a9-119">**GetMatrixTranspose**</span></span>](id3dx11effectmatrixvariable-getmatrixtranspose.md)           | <span data-ttu-id="af6a9-120">調換和取得浮點數矩陣。</span><span class="sxs-lookup"><span data-stu-id="af6a9-120">Transpose and get a floating-point matrix.</span></span><br/>             |
| [<span data-ttu-id="af6a9-121">**GetMatrixTransposeArray**</span><span class="sxs-lookup"><span data-stu-id="af6a9-121">**GetMatrixTransposeArray**</span></span>](id3dx11effectmatrixvariable-getmatrixtransposearray.md) | <span data-ttu-id="af6a9-122">調換和取得浮點數矩陣的陣列。</span><span class="sxs-lookup"><span data-stu-id="af6a9-122">Transpose and get an array of floating-point matrices.</span></span><br/> |
| [<span data-ttu-id="af6a9-123">**SetMatrix**</span><span class="sxs-lookup"><span data-stu-id="af6a9-123">**SetMatrix**</span></span>](id3dx11effectmatrixvariable-setmatrix.md)                             | <span data-ttu-id="af6a9-124">設定浮點數矩陣。</span><span class="sxs-lookup"><span data-stu-id="af6a9-124">Set a floating-point matrix.</span></span><br/>                           |
| [<span data-ttu-id="af6a9-125">**SetMatrixArray**</span><span class="sxs-lookup"><span data-stu-id="af6a9-125">**SetMatrixArray**</span></span>](id3dx11effectmatrixvariable-setmatrixarray.md)                   | <span data-ttu-id="af6a9-126">設定浮點數矩陣的陣列。</span><span class="sxs-lookup"><span data-stu-id="af6a9-126">Set an array of floating-point matrices.</span></span><br/>               |
| [<span data-ttu-id="af6a9-127">**SetMatrixTranspose**</span><span class="sxs-lookup"><span data-stu-id="af6a9-127">**SetMatrixTranspose**</span></span>](id3dx11effectmatrixvariable-setmatrixtranspose.md)           | <span data-ttu-id="af6a9-128">變換並設定浮點數矩陣。</span><span class="sxs-lookup"><span data-stu-id="af6a9-128">Transpose and set a floating-point matrix.</span></span><br/>             |
| [<span data-ttu-id="af6a9-129">**SetMatrixTransposeArray**</span><span class="sxs-lookup"><span data-stu-id="af6a9-129">**SetMatrixTransposeArray**</span></span>](id3dx11effectmatrixvariable-setmatrixtransposearray.md) | <span data-ttu-id="af6a9-130">變換並設定浮點數矩陣的陣列。</span><span class="sxs-lookup"><span data-stu-id="af6a9-130">Transpose and set an array of floating-point matrices.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="af6a9-131">備註</span><span class="sxs-lookup"><span data-stu-id="af6a9-131">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="af6a9-132">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="af6a9-132">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="af6a9-133">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="af6a9-133">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="af6a9-134">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="af6a9-134">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="af6a9-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="af6a9-135">Requirements</span></span>



| <span data-ttu-id="af6a9-136">需求</span><span class="sxs-lookup"><span data-stu-id="af6a9-136">Requirement</span></span> | <span data-ttu-id="af6a9-137">值</span><span class="sxs-lookup"><span data-stu-id="af6a9-137">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af6a9-138">標頭</span><span class="sxs-lookup"><span data-stu-id="af6a9-138">Header</span></span><br/>  | <dl> <span data-ttu-id="af6a9-139"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="af6a9-139"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="af6a9-140">程式庫</span><span class="sxs-lookup"><span data-stu-id="af6a9-140">Library</span></span><br/> | <dl> <span data-ttu-id="af6a9-141"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="af6a9-141"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af6a9-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="af6a9-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af6a9-143">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="af6a9-143">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="af6a9-144">效果11介面</span><span class="sxs-lookup"><span data-stu-id="af6a9-144">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="af6a9-145">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="af6a9-145">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 






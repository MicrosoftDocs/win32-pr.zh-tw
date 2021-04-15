---
title: 'ID3DX11EffectVariable AsConstantBuffer 方法 (D3dx11effect .h) '
description: '取得常數緩衝區。 |ID3DX11EffectVariable AsConstantBuffer 方法 (D3dx11effect .h) '
ms.assetid: b8d8b43c-4626-43b6-8a49-8ffa7cb48427
keywords:
- AsConstantBuffer 方法 Direct3D 11
- AsConstantBuffer 方法 Direct3D 11，ID3DX11EffectVariable 介面
- ID3DX11EffectVariable 介面 Direct3D 11，AsConstantBuffer 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsConstantBuffer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee4caca60216df0c04a773da22150dbc6f7be717
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992218"
---
# <a name="id3dx11effectvariableasconstantbuffer-method"></a><span data-ttu-id="9c5d5-107">ID3DX11EffectVariable：： AsConstantBuffer 方法</span><span class="sxs-lookup"><span data-stu-id="9c5d5-107">ID3DX11EffectVariable::AsConstantBuffer method</span></span>

<span data-ttu-id="9c5d5-108">取得常數緩衝區。</span><span class="sxs-lookup"><span data-stu-id="9c5d5-108">Get a constant buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c5d5-109">語法</span><span class="sxs-lookup"><span data-stu-id="9c5d5-109">Syntax</span></span>


```C++
ID3DX11EffectConstantBuffer* AsConstantBuffer();
```



## <a name="parameters"></a><span data-ttu-id="9c5d5-110">參數</span><span class="sxs-lookup"><span data-stu-id="9c5d5-110">Parameters</span></span>

<span data-ttu-id="9c5d5-111">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="9c5d5-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9c5d5-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="9c5d5-112">Return value</span></span>

<span data-ttu-id="9c5d5-113">類型： **[ **ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="9c5d5-113">Type: **[**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)\***</span></span>

<span data-ttu-id="9c5d5-114">常數緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="9c5d5-114">A pointer to a constant buffer.</span></span> <span data-ttu-id="9c5d5-115">請參閱 [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)。</span><span class="sxs-lookup"><span data-stu-id="9c5d5-115">See [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9c5d5-116">備註</span><span class="sxs-lookup"><span data-stu-id="9c5d5-116">Remarks</span></span>

<span data-ttu-id="9c5d5-117">AsConstantBuffer 會傳回已特製化至常數緩衝區的效果變數版本。</span><span class="sxs-lookup"><span data-stu-id="9c5d5-117">AsConstantBuffer returns a version of the effect variable that has been specialized to a constant buffer.</span></span> <span data-ttu-id="9c5d5-118">類似于轉換，如果效果變數不包含常數緩衝區資料，則此特製化會傳回不正確物件。</span><span class="sxs-lookup"><span data-stu-id="9c5d5-118">Similar to a cast, this specialization will return an invalid object if the effect variable does not contain constant buffer data.</span></span>

<span data-ttu-id="9c5d5-119">應用程式可以藉由呼叫 [**IsValid**](id3dx11effectvariable-isvalid.md)來測試傳回的物件是否有效。</span><span class="sxs-lookup"><span data-stu-id="9c5d5-119">Applications can test the returned object for validity by calling [**IsValid**](id3dx11effectvariable-isvalid.md).</span></span>

> [!Note]  
> <span data-ttu-id="9c5d5-120">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="9c5d5-120">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="9c5d5-121">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="9c5d5-121">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="9c5d5-122">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="9c5d5-122">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9c5d5-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="9c5d5-123">Requirements</span></span>



| <span data-ttu-id="9c5d5-124">需求</span><span class="sxs-lookup"><span data-stu-id="9c5d5-124">Requirement</span></span> | <span data-ttu-id="9c5d5-125">值</span><span class="sxs-lookup"><span data-stu-id="9c5d5-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c5d5-126">標頭</span><span class="sxs-lookup"><span data-stu-id="9c5d5-126">Header</span></span><br/>  | <dl> <span data-ttu-id="9c5d5-127"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="9c5d5-127"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="9c5d5-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="9c5d5-128">Library</span></span><br/> | <dl> <span data-ttu-id="9c5d5-129"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="9c5d5-129"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c5d5-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9c5d5-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c5d5-131">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="9c5d5-131">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

 






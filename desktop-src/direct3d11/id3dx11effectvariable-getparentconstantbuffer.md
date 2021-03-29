---
title: 'ID3DX11EffectVariable GetParentConstantBuffer 方法 (D3dx11effect .h) '
description: '取得常數緩衝區。 |ID3DX11EffectVariable GetParentConstantBuffer 方法 (D3dx11effect .h) '
ms.assetid: 43b46b05-951e-4c52-8bc7-4bb5f657ea78
keywords:
- GetParentConstantBuffer 方法 Direct3D 11
- GetParentConstantBuffer 方法 Direct3D 11，ID3DX11EffectVariable 介面
- ID3DX11EffectVariable 介面 Direct3D 11，GetParentConstantBuffer 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetParentConstantBuffer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa424b91b72dca5539fd0f96a1380e86d1f23f58
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992377"
---
# <a name="id3dx11effectvariablegetparentconstantbuffer-method"></a><span data-ttu-id="44d45-107">ID3DX11EffectVariable：： GetParentConstantBuffer 方法</span><span class="sxs-lookup"><span data-stu-id="44d45-107">ID3DX11EffectVariable::GetParentConstantBuffer method</span></span>

<span data-ttu-id="44d45-108">取得常數緩衝區。</span><span class="sxs-lookup"><span data-stu-id="44d45-108">Get a constant buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="44d45-109">語法</span><span class="sxs-lookup"><span data-stu-id="44d45-109">Syntax</span></span>


```C++
ID3DX11EffectConstantBuffer* GetParentConstantBuffer();
```



## <a name="parameters"></a><span data-ttu-id="44d45-110">參數</span><span class="sxs-lookup"><span data-stu-id="44d45-110">Parameters</span></span>

<span data-ttu-id="44d45-111">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="44d45-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="44d45-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="44d45-112">Return value</span></span>

<span data-ttu-id="44d45-113">類型： **[ **ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="44d45-113">Type: **[**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)\***</span></span>

<span data-ttu-id="44d45-114">指向 [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)的指標。</span><span class="sxs-lookup"><span data-stu-id="44d45-114">A pointer to a [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="44d45-115">備註</span><span class="sxs-lookup"><span data-stu-id="44d45-115">Remarks</span></span>

<span data-ttu-id="44d45-116">效果變數是讀取或寫入常數緩衝區。</span><span class="sxs-lookup"><span data-stu-id="44d45-116">Effect variables are read-from or written-to a constant buffer.</span></span>

> [!Note]  
> <span data-ttu-id="44d45-117">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="44d45-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="44d45-118">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="44d45-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="44d45-119">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="44d45-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="44d45-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="44d45-120">Requirements</span></span>



| <span data-ttu-id="44d45-121">需求</span><span class="sxs-lookup"><span data-stu-id="44d45-121">Requirement</span></span> | <span data-ttu-id="44d45-122">值</span><span class="sxs-lookup"><span data-stu-id="44d45-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44d45-123">標頭</span><span class="sxs-lookup"><span data-stu-id="44d45-123">Header</span></span><br/>  | <dl> <span data-ttu-id="44d45-124"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="44d45-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="44d45-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="44d45-125">Library</span></span><br/> | <dl> <span data-ttu-id="44d45-126"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="44d45-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44d45-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="44d45-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44d45-128">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="44d45-128">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

 






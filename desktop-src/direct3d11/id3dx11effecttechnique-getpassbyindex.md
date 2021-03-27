---
title: 'ID3DX11EffectTechnique GetPassByIndex 方法 (D3dx11effect .h) '
description: 依索引取得傳遞。
ms.assetid: 3c9452f5-c94a-4951-bdd2-e8891b7ceb34
keywords:
- GetPassByIndex 方法 Direct3D 11
- GetPassByIndex 方法 Direct3D 11，ID3DX11EffectTechnique 介面
- ID3DX11EffectTechnique 介面 Direct3D 11，GetPassByIndex 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectTechnique.GetPassByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6af222298cc3d00ad87e5037f9de20139e4fc40
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946215"
---
# <a name="id3dx11effecttechniquegetpassbyindex-method"></a><span data-ttu-id="db7ff-106">ID3DX11EffectTechnique：： GetPassByIndex 方法</span><span class="sxs-lookup"><span data-stu-id="db7ff-106">ID3DX11EffectTechnique::GetPassByIndex method</span></span>

<span data-ttu-id="db7ff-107">依索引取得傳遞。</span><span class="sxs-lookup"><span data-stu-id="db7ff-107">Get a pass by index.</span></span>

## <a name="syntax"></a><span data-ttu-id="db7ff-108">語法</span><span class="sxs-lookup"><span data-stu-id="db7ff-108">Syntax</span></span>


```C++
ID3DX11EffectPass* GetPassByIndex(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="db7ff-109">參數</span><span class="sxs-lookup"><span data-stu-id="db7ff-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db7ff-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="db7ff-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="db7ff-111">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="db7ff-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="db7ff-112">以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="db7ff-112">A zero-based index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db7ff-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="db7ff-113">Return value</span></span>

<span data-ttu-id="db7ff-114">類型： **[ **ID3DX11EffectPass**](id3dx11effectpass.md)\***</span><span class="sxs-lookup"><span data-stu-id="db7ff-114">Type: **[**ID3DX11EffectPass**](id3dx11effectpass.md)\***</span></span>

<span data-ttu-id="db7ff-115">指向 [**ID3DX11EffectPass**](id3dx11effectpass.md)的指標。</span><span class="sxs-lookup"><span data-stu-id="db7ff-115">A pointer to a [**ID3DX11EffectPass**](id3dx11effectpass.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="db7ff-116">備註</span><span class="sxs-lookup"><span data-stu-id="db7ff-116">Remarks</span></span>

<span data-ttu-id="db7ff-117">技術包含一或多個階段;使用名稱或索引取得傳遞。</span><span class="sxs-lookup"><span data-stu-id="db7ff-117">A technique contains one or more passes; get a pass using a name or an index.</span></span>

> [!Note]  
> <span data-ttu-id="db7ff-118">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="db7ff-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="db7ff-119">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="db7ff-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="db7ff-120">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="db7ff-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="db7ff-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="db7ff-121">Requirements</span></span>



| <span data-ttu-id="db7ff-122">需求</span><span class="sxs-lookup"><span data-stu-id="db7ff-122">Requirement</span></span> | <span data-ttu-id="db7ff-123">值</span><span class="sxs-lookup"><span data-stu-id="db7ff-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db7ff-124">標頭</span><span class="sxs-lookup"><span data-stu-id="db7ff-124">Header</span></span><br/>  | <dl> <span data-ttu-id="db7ff-125"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="db7ff-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="db7ff-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="db7ff-126">Library</span></span><br/> | <dl> <span data-ttu-id="db7ff-127"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="db7ff-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db7ff-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="db7ff-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db7ff-129">ID3DX11EffectTechnique</span><span class="sxs-lookup"><span data-stu-id="db7ff-129">ID3DX11EffectTechnique</span></span>](id3dx11effecttechnique.md)
</dt> </dl>

 


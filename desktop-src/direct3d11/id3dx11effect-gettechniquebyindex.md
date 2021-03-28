---
title: 'ID3DX11Effect GetTechniqueByIndex 方法 (D3dx11effect .h) '
description: '依索引取得技術。 |ID3DX11Effect GetTechniqueByIndex 方法 (D3dx11effect .h) '
ms.assetid: ee9c0cc3-0ca1-42e8-bd37-5878fd56cff1
keywords:
- GetTechniqueByIndex 方法 Direct3D 11
- GetTechniqueByIndex 方法 Direct3D 11，ID3DX11Effect 介面
- ID3DX11Effect 介面 Direct3D 11，GetTechniqueByIndex 方法
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetTechniqueByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81d3be5ec403fb25ab3a49792ed77fd4d96bf571
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946202"
---
# <a name="id3dx11effectgettechniquebyindex-method"></a><span data-ttu-id="068c7-107">ID3DX11Effect：： GetTechniqueByIndex 方法</span><span class="sxs-lookup"><span data-stu-id="068c7-107">ID3DX11Effect::GetTechniqueByIndex method</span></span>

<span data-ttu-id="068c7-108">依索引取得技術。</span><span class="sxs-lookup"><span data-stu-id="068c7-108">Get a technique by index.</span></span>

## <a name="syntax"></a><span data-ttu-id="068c7-109">語法</span><span class="sxs-lookup"><span data-stu-id="068c7-109">Syntax</span></span>


```C++
ID3DX11EffectTechnique* GetTechniqueByIndex(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="068c7-110">參數</span><span class="sxs-lookup"><span data-stu-id="068c7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="068c7-111">*Index*</span><span class="sxs-lookup"><span data-stu-id="068c7-111">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="068c7-112">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="068c7-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="068c7-113">以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="068c7-113">A zero-based index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="068c7-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="068c7-114">Return value</span></span>

<span data-ttu-id="068c7-115">類型： **[ **ID3DX11EffectTechnique**](id3dx11effecttechnique.md)\***</span><span class="sxs-lookup"><span data-stu-id="068c7-115">Type: **[**ID3DX11EffectTechnique**](id3dx11effecttechnique.md)\***</span></span>

<span data-ttu-id="068c7-116">[**ID3DX11EffectTechnique**](id3dx11effecttechnique.md)的指標。</span><span class="sxs-lookup"><span data-stu-id="068c7-116">A pointer to an [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="068c7-117">備註</span><span class="sxs-lookup"><span data-stu-id="068c7-117">Remarks</span></span>

<span data-ttu-id="068c7-118">效果包含一或多個技術;每個技術都包含一或多個階段。</span><span class="sxs-lookup"><span data-stu-id="068c7-118">An effect contains one or more techniques; each technique contains one or more passes.</span></span> <span data-ttu-id="068c7-119">您可以使用其名稱或索引來存取技術。</span><span class="sxs-lookup"><span data-stu-id="068c7-119">You can access a technique using its name or with an index.</span></span>

> [!Note]  
> <span data-ttu-id="068c7-120">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="068c7-120">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="068c7-121">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="068c7-121">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="068c7-122">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="068c7-122">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="068c7-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="068c7-123">Requirements</span></span>



| <span data-ttu-id="068c7-124">需求</span><span class="sxs-lookup"><span data-stu-id="068c7-124">Requirement</span></span> | <span data-ttu-id="068c7-125">值</span><span class="sxs-lookup"><span data-stu-id="068c7-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="068c7-126">標頭</span><span class="sxs-lookup"><span data-stu-id="068c7-126">Header</span></span><br/>  | <dl> <span data-ttu-id="068c7-127"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="068c7-127"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="068c7-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="068c7-128">Library</span></span><br/> | <dl> <span data-ttu-id="068c7-129"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="068c7-129"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="068c7-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="068c7-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="068c7-131">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="068c7-131">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 


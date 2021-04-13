---
title: 'ID3DX11Effect GetTechniqueByName 方法 (D3dx11effect .h) '
description: '依名稱取得技術。 |ID3DX11Effect GetTechniqueByName 方法 (D3dx11effect .h) '
ms.assetid: 0f7fa02c-dfbf-4971-86ad-3429f99f84e0
keywords:
- GetTechniqueByName 方法 Direct3D 11
- GetTechniqueByName 方法 Direct3D 11，ID3DX11Effect 介面
- ID3DX11Effect 介面 Direct3D 11，GetTechniqueByName 方法
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetTechniqueByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d26b6067352d4ca898cc1fc970524040d407bda1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974656"
---
# <a name="id3dx11effectgettechniquebyname-method"></a><span data-ttu-id="9d12b-107">ID3DX11Effect：： GetTechniqueByName 方法</span><span class="sxs-lookup"><span data-stu-id="9d12b-107">ID3DX11Effect::GetTechniqueByName method</span></span>

<span data-ttu-id="9d12b-108">依名稱取得技術。</span><span class="sxs-lookup"><span data-stu-id="9d12b-108">Get a technique by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d12b-109">語法</span><span class="sxs-lookup"><span data-stu-id="9d12b-109">Syntax</span></span>


```C++
ID3DX11EffectTechnique* GetTechniqueByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="9d12b-110">參數</span><span class="sxs-lookup"><span data-stu-id="9d12b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d12b-111">*名稱*</span><span class="sxs-lookup"><span data-stu-id="9d12b-111">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="9d12b-112">類型： **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="9d12b-112">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="9d12b-113">技術的名稱。</span><span class="sxs-lookup"><span data-stu-id="9d12b-113">The name of the technique.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d12b-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="9d12b-114">Return value</span></span>

<span data-ttu-id="9d12b-115">類型： **[ **ID3DX11EffectTechnique**](id3dx11effecttechnique.md)\***</span><span class="sxs-lookup"><span data-stu-id="9d12b-115">Type: **[**ID3DX11EffectTechnique**](id3dx11effecttechnique.md)\***</span></span>

<span data-ttu-id="9d12b-116">[**ID3DX11EffectTechnique**](id3dx11effecttechnique.md)的指標。</span><span class="sxs-lookup"><span data-stu-id="9d12b-116">A pointer to an [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md).</span></span> <span data-ttu-id="9d12b-117">如果找不到具有適當名稱的技術，則會傳回不正確技巧。</span><span class="sxs-lookup"><span data-stu-id="9d12b-117">If a technique with the appropriate name is not found an invalid technique is returned.</span></span> <span data-ttu-id="9d12b-118">[**ID3DX11EffectTechnique：： IsValid**](id3dx11effecttechnique-isvalid.md) 應針對傳回的技術進行呼叫，以判斷它是否有效。</span><span class="sxs-lookup"><span data-stu-id="9d12b-118">[**ID3DX11EffectTechnique::IsValid**](id3dx11effecttechnique-isvalid.md) should be called on the returned technique to determine whether it is valid.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d12b-119">備註</span><span class="sxs-lookup"><span data-stu-id="9d12b-119">Remarks</span></span>

<span data-ttu-id="9d12b-120">效果包含一或多個技術;每個技術都包含一或多個階段。</span><span class="sxs-lookup"><span data-stu-id="9d12b-120">An effect contains one or more techniques; each technique contains one or more passes.</span></span> <span data-ttu-id="9d12b-121">您可以使用其名稱或索引來存取技術。</span><span class="sxs-lookup"><span data-stu-id="9d12b-121">You can access a technique using its name or with an index.</span></span>

> [!Note]  
> <span data-ttu-id="9d12b-122">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="9d12b-122">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="9d12b-123">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="9d12b-123">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="9d12b-124">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="9d12b-124">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9d12b-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="9d12b-125">Requirements</span></span>



| <span data-ttu-id="9d12b-126">需求</span><span class="sxs-lookup"><span data-stu-id="9d12b-126">Requirement</span></span> | <span data-ttu-id="9d12b-127">值</span><span class="sxs-lookup"><span data-stu-id="9d12b-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d12b-128">標頭</span><span class="sxs-lookup"><span data-stu-id="9d12b-128">Header</span></span><br/>  | <dl> <span data-ttu-id="9d12b-129"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="9d12b-129"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="9d12b-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="9d12b-130">Library</span></span><br/> | <dl> <span data-ttu-id="9d12b-131"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="9d12b-131"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d12b-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9d12b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d12b-133">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="9d12b-133">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 


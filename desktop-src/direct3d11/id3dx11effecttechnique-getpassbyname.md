---
title: 'ID3DX11EffectTechnique GetPassByName 方法 (D3dx11effect .h) '
description: 依名稱取得傳遞。
ms.assetid: 07c7502e-2af9-4898-8cd4-106d6814fb85
keywords:
- GetPassByName 方法 Direct3D 11
- GetPassByName 方法 Direct3D 11，ID3DX11EffectTechnique 介面
- ID3DX11EffectTechnique 介面 Direct3D 11，GetPassByName 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectTechnique.GetPassByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e84bbe9b954efff12e458ee6172665118a7b8ede
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992254"
---
# <a name="id3dx11effecttechniquegetpassbyname-method"></a><span data-ttu-id="32204-106">ID3DX11EffectTechnique：： GetPassByName 方法</span><span class="sxs-lookup"><span data-stu-id="32204-106">ID3DX11EffectTechnique::GetPassByName method</span></span>

<span data-ttu-id="32204-107">依名稱取得傳遞。</span><span class="sxs-lookup"><span data-stu-id="32204-107">Get a pass by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="32204-108">語法</span><span class="sxs-lookup"><span data-stu-id="32204-108">Syntax</span></span>


```C++
ID3DX11EffectPass* GetPassByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="32204-109">參數</span><span class="sxs-lookup"><span data-stu-id="32204-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32204-110">*名稱*</span><span class="sxs-lookup"><span data-stu-id="32204-110">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="32204-111">類型： **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="32204-111">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="32204-112">傳遞的名稱。</span><span class="sxs-lookup"><span data-stu-id="32204-112">The name of the pass.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32204-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="32204-113">Return value</span></span>

<span data-ttu-id="32204-114">類型： **[ **ID3DX11EffectPass**](id3dx11effectpass.md)\***</span><span class="sxs-lookup"><span data-stu-id="32204-114">Type: **[**ID3DX11EffectPass**](id3dx11effectpass.md)\***</span></span>

<span data-ttu-id="32204-115">[**ID3DX11EffectPass**](id3dx11effectpass.md)的指標。</span><span class="sxs-lookup"><span data-stu-id="32204-115">A pointer to an [**ID3DX11EffectPass**](id3dx11effectpass.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="32204-116">備註</span><span class="sxs-lookup"><span data-stu-id="32204-116">Remarks</span></span>

<span data-ttu-id="32204-117">技術包含一或多個階段;使用名稱或索引取得傳遞。</span><span class="sxs-lookup"><span data-stu-id="32204-117">A technique contains one or more passes; get a pass using a name or an index.</span></span>

> [!Note]  
> <span data-ttu-id="32204-118">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="32204-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="32204-119">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="32204-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="32204-120">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="32204-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="32204-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="32204-121">Requirements</span></span>



| <span data-ttu-id="32204-122">需求</span><span class="sxs-lookup"><span data-stu-id="32204-122">Requirement</span></span> | <span data-ttu-id="32204-123">值</span><span class="sxs-lookup"><span data-stu-id="32204-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32204-124">標頭</span><span class="sxs-lookup"><span data-stu-id="32204-124">Header</span></span><br/>  | <dl> <span data-ttu-id="32204-125"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="32204-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="32204-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="32204-126">Library</span></span><br/> | <dl> <span data-ttu-id="32204-127"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="32204-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32204-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="32204-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32204-129">ID3DX11EffectTechnique</span><span class="sxs-lookup"><span data-stu-id="32204-129">ID3DX11EffectTechnique</span></span>](id3dx11effecttechnique.md)
</dt> </dl>

 


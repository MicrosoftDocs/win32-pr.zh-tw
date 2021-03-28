---
title: 'ID3DX11EffectPass GetAnnotationByName 方法 (D3dx11effect .h) '
description: '依名稱取得批註。 |ID3DX11EffectPass GetAnnotationByName 方法 (D3dx11effect .h) '
ms.assetid: b54a4fb0-62c7-4d96-af30-f9ae04ff7dab
keywords:
- GetAnnotationByName 方法 Direct3D 11
- GetAnnotationByName 方法 Direct3D 11，ID3DX11EffectPass 介面
- ID3DX11EffectPass 介面 Direct3D 11，GetAnnotationByName 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.GetAnnotationByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d129f1548e7f63c47906ac736cbddb5f6b2548b2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946184"
---
# <a name="id3dx11effectpassgetannotationbyname-method"></a><span data-ttu-id="0f7fd-107">ID3DX11EffectPass：： GetAnnotationByName 方法</span><span class="sxs-lookup"><span data-stu-id="0f7fd-107">ID3DX11EffectPass::GetAnnotationByName method</span></span>

<span data-ttu-id="0f7fd-108">依名稱取得批註。</span><span class="sxs-lookup"><span data-stu-id="0f7fd-108">Get an annotation by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f7fd-109">語法</span><span class="sxs-lookup"><span data-stu-id="0f7fd-109">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetAnnotationByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="0f7fd-110">參數</span><span class="sxs-lookup"><span data-stu-id="0f7fd-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f7fd-111">*名稱*</span><span class="sxs-lookup"><span data-stu-id="0f7fd-111">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="0f7fd-112">類型： **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0f7fd-112">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="0f7fd-113">註釋的名稱。</span><span class="sxs-lookup"><span data-stu-id="0f7fd-113">The name of the annotation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f7fd-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="0f7fd-114">Return value</span></span>

<span data-ttu-id="0f7fd-115">類型： **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="0f7fd-115">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="0f7fd-116">[**ID3DX11EffectVariable**](id3dx11effectvariable.md)的指標。</span><span class="sxs-lookup"><span data-stu-id="0f7fd-116">A pointer to an [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0f7fd-117">備註</span><span class="sxs-lookup"><span data-stu-id="0f7fd-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="0f7fd-118">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="0f7fd-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="0f7fd-119">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="0f7fd-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="0f7fd-120">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="0f7fd-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0f7fd-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="0f7fd-121">Requirements</span></span>



| <span data-ttu-id="0f7fd-122">需求</span><span class="sxs-lookup"><span data-stu-id="0f7fd-122">Requirement</span></span> | <span data-ttu-id="0f7fd-123">值</span><span class="sxs-lookup"><span data-stu-id="0f7fd-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f7fd-124">標頭</span><span class="sxs-lookup"><span data-stu-id="0f7fd-124">Header</span></span><br/>  | <dl> <span data-ttu-id="0f7fd-125"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="0f7fd-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="0f7fd-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="0f7fd-126">Library</span></span><br/> | <dl> <span data-ttu-id="0f7fd-127"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="0f7fd-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f7fd-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0f7fd-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f7fd-129">ID3DX11EffectPass</span><span class="sxs-lookup"><span data-stu-id="0f7fd-129">ID3DX11EffectPass</span></span>](id3dx11effectpass.md)
</dt> </dl>

 


---
title: 'ID3DX11EffectType GetMemberTypeBySemantic 方法 (D3dx11effect .h) '
description: 依語義取得成員類型。
ms.assetid: d5fea2d9-8d08-4e02-a9c6-dbcfaaf4a7d1
keywords:
- GetMemberTypeBySemantic 方法 Direct3D 11
- GetMemberTypeBySemantic 方法 Direct3D 11，ID3DX11EffectType 介面
- ID3DX11EffectType 介面 Direct3D 11，GetMemberTypeBySemantic 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectType.GetMemberTypeBySemantic
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de5f0894c83ff2d0885ae3b951e0e324343fae8e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992362"
---
# <a name="id3dx11effecttypegetmembertypebysemantic-method"></a><span data-ttu-id="e9137-106">ID3DX11EffectType：： GetMemberTypeBySemantic 方法</span><span class="sxs-lookup"><span data-stu-id="e9137-106">ID3DX11EffectType::GetMemberTypeBySemantic method</span></span>

<span data-ttu-id="e9137-107">依語義取得成員類型。</span><span class="sxs-lookup"><span data-stu-id="e9137-107">Get a member type by semantic.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9137-108">語法</span><span class="sxs-lookup"><span data-stu-id="e9137-108">Syntax</span></span>


```C++
ID3DX11EffectType* GetMemberTypeBySemantic(
   LPCSTR Semantic
);
```



## <a name="parameters"></a><span data-ttu-id="e9137-109">參數</span><span class="sxs-lookup"><span data-stu-id="e9137-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9137-110">*語義*</span><span class="sxs-lookup"><span data-stu-id="e9137-110">*Semantic*</span></span> 
</dt> <dd>

<span data-ttu-id="e9137-111">類型： **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e9137-111">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e9137-112">語義。</span><span class="sxs-lookup"><span data-stu-id="e9137-112">A semantic.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9137-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="e9137-113">Return value</span></span>

<span data-ttu-id="e9137-114">類型： **[ **ID3DX11EffectType**](id3dx11effecttype.md)\***</span><span class="sxs-lookup"><span data-stu-id="e9137-114">Type: **[**ID3DX11EffectType**](id3dx11effecttype.md)\***</span></span>

<span data-ttu-id="e9137-115">[**ID3DX11EffectType**](id3dx11effecttype.md)的指標。</span><span class="sxs-lookup"><span data-stu-id="e9137-115">A pointer to an [**ID3DX11EffectType**](id3dx11effecttype.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e9137-116">備註</span><span class="sxs-lookup"><span data-stu-id="e9137-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e9137-117">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="e9137-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="e9137-118">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="e9137-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="e9137-119">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="e9137-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e9137-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="e9137-120">Requirements</span></span>



| <span data-ttu-id="e9137-121">需求</span><span class="sxs-lookup"><span data-stu-id="e9137-121">Requirement</span></span> | <span data-ttu-id="e9137-122">值</span><span class="sxs-lookup"><span data-stu-id="e9137-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9137-123">標頭</span><span class="sxs-lookup"><span data-stu-id="e9137-123">Header</span></span><br/>  | <dl> <span data-ttu-id="e9137-124"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="e9137-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="e9137-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="e9137-125">Library</span></span><br/> | <dl> <span data-ttu-id="e9137-126"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="e9137-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9137-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e9137-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9137-128">ID3DX11EffectType</span><span class="sxs-lookup"><span data-stu-id="e9137-128">ID3DX11EffectType</span></span>](id3dx11effecttype.md)
</dt> </dl>

 


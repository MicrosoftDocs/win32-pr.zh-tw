---
title: 'ID3DX11EffectType GetMemberTypeByIndex 方法 (D3dx11effect .h) '
description: 依索引取得成員類型。
ms.assetid: 6421f08f-0236-4d8f-b3c2-ef7ec5ffe2a1
keywords:
- GetMemberTypeByIndex 方法 Direct3D 11
- GetMemberTypeByIndex 方法 Direct3D 11，ID3DX11EffectType 介面
- ID3DX11EffectType 介面 Direct3D 11，GetMemberTypeByIndex 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectType.GetMemberTypeByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da5023e064539f57af9998c788385f2a1316433f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104514637"
---
# <a name="id3dx11effecttypegetmembertypebyindex-method"></a><span data-ttu-id="81a37-106">ID3DX11EffectType：： GetMemberTypeByIndex 方法</span><span class="sxs-lookup"><span data-stu-id="81a37-106">ID3DX11EffectType::GetMemberTypeByIndex method</span></span>

<span data-ttu-id="81a37-107">依索引取得成員類型。</span><span class="sxs-lookup"><span data-stu-id="81a37-107">Get a member type by index.</span></span>

## <a name="syntax"></a><span data-ttu-id="81a37-108">語法</span><span class="sxs-lookup"><span data-stu-id="81a37-108">Syntax</span></span>


```C++
ID3DX11EffectType* GetMemberTypeByIndex(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="81a37-109">參數</span><span class="sxs-lookup"><span data-stu-id="81a37-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81a37-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="81a37-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="81a37-111">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="81a37-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="81a37-112">以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="81a37-112">A zero-based index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81a37-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="81a37-113">Return value</span></span>

<span data-ttu-id="81a37-114">類型： **[ **ID3DX11EffectType**](id3dx11effecttype.md)\***</span><span class="sxs-lookup"><span data-stu-id="81a37-114">Type: **[**ID3DX11EffectType**](id3dx11effecttype.md)\***</span></span>

<span data-ttu-id="81a37-115">[**ID3DX11EffectType**](id3dx11effecttype.md)的指標。</span><span class="sxs-lookup"><span data-stu-id="81a37-115">A pointer to an [**ID3DX11EffectType**](id3dx11effecttype.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="81a37-116">備註</span><span class="sxs-lookup"><span data-stu-id="81a37-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="81a37-117">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="81a37-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="81a37-118">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="81a37-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="81a37-119">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="81a37-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="81a37-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="81a37-120">Requirements</span></span>



| <span data-ttu-id="81a37-121">需求</span><span class="sxs-lookup"><span data-stu-id="81a37-121">Requirement</span></span> | <span data-ttu-id="81a37-122">值</span><span class="sxs-lookup"><span data-stu-id="81a37-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81a37-123">標頭</span><span class="sxs-lookup"><span data-stu-id="81a37-123">Header</span></span><br/>  | <dl> <span data-ttu-id="81a37-124"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="81a37-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="81a37-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="81a37-125">Library</span></span><br/> | <dl> <span data-ttu-id="81a37-126"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="81a37-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81a37-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="81a37-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81a37-128">ID3DX11EffectType</span><span class="sxs-lookup"><span data-stu-id="81a37-128">ID3DX11EffectType</span></span>](id3dx11effecttype.md)
</dt> </dl>

 


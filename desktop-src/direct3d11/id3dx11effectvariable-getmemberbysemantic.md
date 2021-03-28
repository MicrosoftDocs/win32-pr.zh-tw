---
title: 'ID3DX11EffectVariable GetMemberBySemantic 方法 (D3dx11effect .h) '
description: 依語義取得結構成員。
ms.assetid: e4ae1f6a-43d2-45df-9dba-833d4f767818
keywords:
- GetMemberBySemantic 方法 Direct3D 11
- GetMemberBySemantic 方法 Direct3D 11，ID3DX11EffectVariable 介面
- ID3DX11EffectVariable 介面 Direct3D 11，GetMemberBySemantic 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetMemberBySemantic
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5af8b628247dcc89f8df99c6ffebb04d500e76a1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992369"
---
# <a name="id3dx11effectvariablegetmemberbysemantic-method"></a><span data-ttu-id="12369-106">ID3DX11EffectVariable：： GetMemberBySemantic 方法</span><span class="sxs-lookup"><span data-stu-id="12369-106">ID3DX11EffectVariable::GetMemberBySemantic method</span></span>

<span data-ttu-id="12369-107">依語義取得結構成員。</span><span class="sxs-lookup"><span data-stu-id="12369-107">Get a structure member by semantic.</span></span>

## <a name="syntax"></a><span data-ttu-id="12369-108">語法</span><span class="sxs-lookup"><span data-stu-id="12369-108">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetMemberBySemantic(
   LPCSTR Semantic
);
```



## <a name="parameters"></a><span data-ttu-id="12369-109">參數</span><span class="sxs-lookup"><span data-stu-id="12369-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12369-110">*語義*</span><span class="sxs-lookup"><span data-stu-id="12369-110">*Semantic*</span></span> 
</dt> <dd>

<span data-ttu-id="12369-111">類型： **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="12369-111">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="12369-112">語義。</span><span class="sxs-lookup"><span data-stu-id="12369-112">The semantic.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12369-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="12369-113">Return value</span></span>

<span data-ttu-id="12369-114">類型： **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="12369-114">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="12369-115">[**ID3DX11EffectVariable**](id3dx11effectvariable.md)的指標。</span><span class="sxs-lookup"><span data-stu-id="12369-115">A pointer to an [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="12369-116">備註</span><span class="sxs-lookup"><span data-stu-id="12369-116">Remarks</span></span>

<span data-ttu-id="12369-117">如果效果變數是結構，請使用這個方法來查閱附加語義的成員。</span><span class="sxs-lookup"><span data-stu-id="12369-117">If the effect variable is an structure, use this method to look up a member by attached semantic.</span></span>

> [!Note]  
> <span data-ttu-id="12369-118">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="12369-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="12369-119">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="12369-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="12369-120">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="12369-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="12369-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="12369-121">Requirements</span></span>



| <span data-ttu-id="12369-122">需求</span><span class="sxs-lookup"><span data-stu-id="12369-122">Requirement</span></span> | <span data-ttu-id="12369-123">值</span><span class="sxs-lookup"><span data-stu-id="12369-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12369-124">標頭</span><span class="sxs-lookup"><span data-stu-id="12369-124">Header</span></span><br/>  | <dl> <span data-ttu-id="12369-125"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="12369-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="12369-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="12369-126">Library</span></span><br/> | <dl> <span data-ttu-id="12369-127"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="12369-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12369-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="12369-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12369-129">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="12369-129">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 


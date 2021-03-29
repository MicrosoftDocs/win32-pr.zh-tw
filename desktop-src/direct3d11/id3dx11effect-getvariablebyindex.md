---
title: 'ID3DX11Effect GetVariableByIndex 方法 (D3dx11effect .h) '
description: 依索引取得變數。
ms.assetid: af25b945-9526-45c2-8746-8b62f8166de7
keywords:
- GetVariableByIndex 方法 Direct3D 11
- GetVariableByIndex 方法 Direct3D 11，ID3DX11Effect 介面
- ID3DX11Effect 介面 Direct3D 11，GetVariableByIndex 方法
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetVariableByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd262ea0aa778f03c2d723dec99f531f3419f3be
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992339"
---
# <a name="id3dx11effectgetvariablebyindex-method"></a><span data-ttu-id="e2f10-106">ID3DX11Effect：： GetVariableByIndex 方法</span><span class="sxs-lookup"><span data-stu-id="e2f10-106">ID3DX11Effect::GetVariableByIndex method</span></span>

<span data-ttu-id="e2f10-107">依索引取得變數。</span><span class="sxs-lookup"><span data-stu-id="e2f10-107">Get a variable by index.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2f10-108">語法</span><span class="sxs-lookup"><span data-stu-id="e2f10-108">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetVariableByIndex(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="e2f10-109">參數</span><span class="sxs-lookup"><span data-stu-id="e2f10-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2f10-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="e2f10-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="e2f10-111">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e2f10-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e2f10-112">以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="e2f10-112">A zero-based index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2f10-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="e2f10-113">Return value</span></span>

<span data-ttu-id="e2f10-114">類型： **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="e2f10-114">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="e2f10-115">指向 [**ID3DX11EffectVariable**](id3dx11effectvariable.md)的指標。</span><span class="sxs-lookup"><span data-stu-id="e2f10-115">A pointer to a [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e2f10-116">備註</span><span class="sxs-lookup"><span data-stu-id="e2f10-116">Remarks</span></span>

<span data-ttu-id="e2f10-117">效果可能包含一或多個變數。</span><span class="sxs-lookup"><span data-stu-id="e2f10-117">An effect may contain one or more variables.</span></span> <span data-ttu-id="e2f10-118">技術以外的變數會被視為所有效果的全域變數，而這些變數位於某個技術內，就是該技巧的本機變數。</span><span class="sxs-lookup"><span data-stu-id="e2f10-118">Variables outside of a technique are considered global to all effects, those located inside of a technique are local to that technique.</span></span> <span data-ttu-id="e2f10-119">您可以使用其名稱或索引來存取任何本機非靜態效果變數。</span><span class="sxs-lookup"><span data-stu-id="e2f10-119">You can access any local non-static effect variable using its name or with an index.</span></span>

<span data-ttu-id="e2f10-120">如果找不到變數，方法會傳回 [**效果變數介面**](id3dx11effectvariable.md) 的指標;您可以呼叫 [**ID3DX11Effect：： IsValid**](id3dx11effect-isvalid.md) 來確認索引是否存在。</span><span class="sxs-lookup"><span data-stu-id="e2f10-120">The method returns a pointer to an [**effect-variable interface**](id3dx11effectvariable.md) if a variable is not found; you can call [**ID3DX11Effect::IsValid**](id3dx11effect-isvalid.md) to verify whether or not the index exists.</span></span>

> [!Note]  
> <span data-ttu-id="e2f10-121">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="e2f10-121">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="e2f10-122">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="e2f10-122">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="e2f10-123">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="e2f10-123">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e2f10-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="e2f10-124">Requirements</span></span>



| <span data-ttu-id="e2f10-125">需求</span><span class="sxs-lookup"><span data-stu-id="e2f10-125">Requirement</span></span> | <span data-ttu-id="e2f10-126">值</span><span class="sxs-lookup"><span data-stu-id="e2f10-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2f10-127">標頭</span><span class="sxs-lookup"><span data-stu-id="e2f10-127">Header</span></span><br/>  | <dl> <span data-ttu-id="e2f10-128"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="e2f10-128"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="e2f10-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="e2f10-129">Library</span></span><br/> | <dl> <span data-ttu-id="e2f10-130"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="e2f10-130"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2f10-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e2f10-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2f10-132">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="e2f10-132">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 


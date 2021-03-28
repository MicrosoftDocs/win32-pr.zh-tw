---
title: 'ID3DX11Effect GetVariableByName 方法 (D3dx11effect .h) '
description: 依名稱取得變數。
ms.assetid: d20c5a85-51a5-482f-b5b0-197d8e993910
keywords:
- GetVariableByName 方法 Direct3D 11
- GetVariableByName 方法 Direct3D 11，ID3DX11Effect 介面
- ID3DX11Effect 介面 Direct3D 11，GetVariableByName 方法
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetVariableByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e6079e7f45c21d9d7326021b2c439ab12e4e031
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992335"
---
# <a name="id3dx11effectgetvariablebyname-method"></a><span data-ttu-id="41732-106">ID3DX11Effect：： GetVariableByName 方法</span><span class="sxs-lookup"><span data-stu-id="41732-106">ID3DX11Effect::GetVariableByName method</span></span>

<span data-ttu-id="41732-107">依名稱取得變數。</span><span class="sxs-lookup"><span data-stu-id="41732-107">Get a variable by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="41732-108">語法</span><span class="sxs-lookup"><span data-stu-id="41732-108">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetVariableByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="41732-109">參數</span><span class="sxs-lookup"><span data-stu-id="41732-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41732-110">*名稱*</span><span class="sxs-lookup"><span data-stu-id="41732-110">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="41732-111">類型： **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="41732-111">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="41732-112">變數名稱。</span><span class="sxs-lookup"><span data-stu-id="41732-112">The variable name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41732-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="41732-113">Return value</span></span>

<span data-ttu-id="41732-114">類型： **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="41732-114">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="41732-115">[**ID3DX11EffectVariable**](id3dx11effectvariable.md)的指標。</span><span class="sxs-lookup"><span data-stu-id="41732-115">A pointer to an [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="41732-116">如果找不到指定的名稱，則傳回不正確變數。</span><span class="sxs-lookup"><span data-stu-id="41732-116">Returns an invalid variable if the specified name cannot be found.</span></span>

## <a name="remarks"></a><span data-ttu-id="41732-117">備註</span><span class="sxs-lookup"><span data-stu-id="41732-117">Remarks</span></span>

<span data-ttu-id="41732-118">效果可能包含一或多個變數。</span><span class="sxs-lookup"><span data-stu-id="41732-118">An effect may contain one or more variables.</span></span> <span data-ttu-id="41732-119">技術以外的變數會被視為所有效果的全域變數，而這些變數位於某個技術內，就是該技巧的本機變數。</span><span class="sxs-lookup"><span data-stu-id="41732-119">Variables outside of a technique are considered global to all effects, those located inside of a technique are local to that technique.</span></span> <span data-ttu-id="41732-120">您可以使用其名稱或索引來存取效果變數。</span><span class="sxs-lookup"><span data-stu-id="41732-120">You can access an effect variable using its name or with an index.</span></span>

<span data-ttu-id="41732-121">無論是否找到變數，方法都會傳回 [**效果變數介面**](id3dx11effectvariable.md) 的指標。</span><span class="sxs-lookup"><span data-stu-id="41732-121">The method returns a pointer to an [**effect-variable interface**](id3dx11effectvariable.md) whether or not a variable is found.</span></span> <span data-ttu-id="41732-122">應呼叫 [**ID3DX11Effect：： IsValid**](id3dx11effect-isvalid.md)來確認名稱是否存在。</span><span class="sxs-lookup"><span data-stu-id="41732-122">[**ID3DX11Effect::IsValid**](id3dx11effect-isvalid.md) should be called to verify whether or not the name exists.</span></span>

> [!Note]  
> <span data-ttu-id="41732-123">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="41732-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="41732-124">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="41732-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="41732-125">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="41732-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="41732-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="41732-126">Requirements</span></span>



| <span data-ttu-id="41732-127">需求</span><span class="sxs-lookup"><span data-stu-id="41732-127">Requirement</span></span> | <span data-ttu-id="41732-128">值</span><span class="sxs-lookup"><span data-stu-id="41732-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41732-129">標頭</span><span class="sxs-lookup"><span data-stu-id="41732-129">Header</span></span><br/>  | <dl> <span data-ttu-id="41732-130"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="41732-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="41732-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="41732-131">Library</span></span><br/> | <dl> <span data-ttu-id="41732-132"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="41732-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41732-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="41732-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41732-134">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="41732-134">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 


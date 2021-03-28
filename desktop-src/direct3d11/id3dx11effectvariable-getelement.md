---
title: 'ID3DX11EffectVariable GetElement 方法 (D3dx11effect .h) '
description: 取得陣列元素。
ms.assetid: 3edf2084-570a-4423-8205-0b94a2a0cfde
keywords:
- GetElement 方法 Direct3D 11
- GetElement 方法 Direct3D 11，ID3DX11EffectVariable 介面
- ID3DX11EffectVariable 介面 Direct3D 11，GetElement 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetElement
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a5b887bb9e4c1d40f4d3eb0d36b9a7b4d2698b5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974468"
---
# <a name="id3dx11effectvariablegetelement-method"></a><span data-ttu-id="eeed0-106">ID3DX11EffectVariable：： GetElement 方法</span><span class="sxs-lookup"><span data-stu-id="eeed0-106">ID3DX11EffectVariable::GetElement method</span></span>

<span data-ttu-id="eeed0-107">取得陣列元素。</span><span class="sxs-lookup"><span data-stu-id="eeed0-107">Get an array element.</span></span>

## <a name="syntax"></a><span data-ttu-id="eeed0-108">語法</span><span class="sxs-lookup"><span data-stu-id="eeed0-108">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetElement(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="eeed0-109">參數</span><span class="sxs-lookup"><span data-stu-id="eeed0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eeed0-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="eeed0-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="eeed0-111">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="eeed0-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="eeed0-112">以零為基底的索引;否則為0。</span><span class="sxs-lookup"><span data-stu-id="eeed0-112">A zero-based index; otherwise 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eeed0-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="eeed0-113">Return value</span></span>

<span data-ttu-id="eeed0-114">類型： **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="eeed0-114">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="eeed0-115">[**ID3DX11EffectVariable**](id3dx11effectvariable.md)的指標。</span><span class="sxs-lookup"><span data-stu-id="eeed0-115">A pointer to an [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="eeed0-116">備註</span><span class="sxs-lookup"><span data-stu-id="eeed0-116">Remarks</span></span>

<span data-ttu-id="eeed0-117">如果效果變數是陣列，請使用這個方法傳回其中一個元素。</span><span class="sxs-lookup"><span data-stu-id="eeed0-117">If the effect variable is an array, use this method to return one of the elements.</span></span>

> [!Note]  
> <span data-ttu-id="eeed0-118">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="eeed0-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="eeed0-119">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="eeed0-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="eeed0-120">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="eeed0-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="eeed0-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="eeed0-121">Requirements</span></span>



| <span data-ttu-id="eeed0-122">需求</span><span class="sxs-lookup"><span data-stu-id="eeed0-122">Requirement</span></span> | <span data-ttu-id="eeed0-123">值</span><span class="sxs-lookup"><span data-stu-id="eeed0-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eeed0-124">標頭</span><span class="sxs-lookup"><span data-stu-id="eeed0-124">Header</span></span><br/>  | <dl> <span data-ttu-id="eeed0-125"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="eeed0-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="eeed0-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="eeed0-126">Library</span></span><br/> | <dl> <span data-ttu-id="eeed0-127"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="eeed0-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eeed0-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eeed0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eeed0-129">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="eeed0-129">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 


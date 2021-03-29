---
title: 'ID3DX11EffectVariable GetAnnotationByIndex 方法 (D3dx11effect .h) '
description: '依索引取得批註。 |ID3DX11EffectVariable GetAnnotationByIndex 方法 (D3dx11effect .h) '
ms.assetid: fc130098-0269-4c78-bc45-284aa0b77865
keywords:
- GetAnnotationByIndex 方法 Direct3D 11
- GetAnnotationByIndex 方法 Direct3D 11，ID3DX11EffectVariable 介面
- ID3DX11EffectVariable 介面 Direct3D 11，GetAnnotationByIndex 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetAnnotationByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e13cfcb27e94c64af132e5eec600941d0b41cd8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104116177"
---
# <a name="id3dx11effectvariablegetannotationbyindex-method"></a><span data-ttu-id="cdd5c-107">ID3DX11EffectVariable：： GetAnnotationByIndex 方法</span><span class="sxs-lookup"><span data-stu-id="cdd5c-107">ID3DX11EffectVariable::GetAnnotationByIndex method</span></span>

<span data-ttu-id="cdd5c-108">依索引取得批註。</span><span class="sxs-lookup"><span data-stu-id="cdd5c-108">Get an annotation by index.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdd5c-109">語法</span><span class="sxs-lookup"><span data-stu-id="cdd5c-109">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetAnnotationByIndex(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="cdd5c-110">參數</span><span class="sxs-lookup"><span data-stu-id="cdd5c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cdd5c-111">*Index*</span><span class="sxs-lookup"><span data-stu-id="cdd5c-111">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="cdd5c-112">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="cdd5c-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="cdd5c-113">以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="cdd5c-113">A zero-based index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cdd5c-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="cdd5c-114">Return value</span></span>

<span data-ttu-id="cdd5c-115">類型： **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="cdd5c-115">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="cdd5c-116">[**ID3DX11EffectVariable**](id3dx11effectvariable.md)的指標。</span><span class="sxs-lookup"><span data-stu-id="cdd5c-116">A pointer to an [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="cdd5c-117">備註</span><span class="sxs-lookup"><span data-stu-id="cdd5c-117">Remarks</span></span>

<span data-ttu-id="cdd5c-118">Annonations 可以附加至技術、pass 或全域變數。</span><span class="sxs-lookup"><span data-stu-id="cdd5c-118">Annonations can be attached to a technique, a pass, or a global variable.</span></span>

> [!Note]  
> <span data-ttu-id="cdd5c-119">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="cdd5c-119">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="cdd5c-120">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="cdd5c-120">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="cdd5c-121">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="cdd5c-121">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cdd5c-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="cdd5c-122">Requirements</span></span>



| <span data-ttu-id="cdd5c-123">需求</span><span class="sxs-lookup"><span data-stu-id="cdd5c-123">Requirement</span></span> | <span data-ttu-id="cdd5c-124">值</span><span class="sxs-lookup"><span data-stu-id="cdd5c-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdd5c-125">標頭</span><span class="sxs-lookup"><span data-stu-id="cdd5c-125">Header</span></span><br/>  | <dl> <span data-ttu-id="cdd5c-126"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="cdd5c-126"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="cdd5c-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="cdd5c-127">Library</span></span><br/> | <dl> <span data-ttu-id="cdd5c-128"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="cdd5c-128"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cdd5c-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cdd5c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdd5c-130">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="cdd5c-130">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 


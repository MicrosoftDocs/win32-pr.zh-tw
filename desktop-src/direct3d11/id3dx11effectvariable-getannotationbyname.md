---
title: 'ID3DX11EffectVariable GetAnnotationByName 方法 (D3dx11effect .h) '
description: '依名稱取得批註。 |ID3DX11EffectVariable GetAnnotationByName 方法 (D3dx11effect .h) '
ms.assetid: 0ca3df07-c721-48c4-9422-f6af24acbaef
keywords:
- GetAnnotationByName 方法 Direct3D 11
- GetAnnotationByName 方法 Direct3D 11，ID3DX11EffectVariable 介面
- ID3DX11EffectVariable 介面 Direct3D 11，GetAnnotationByName 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetAnnotationByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e37efcd773728e563a4112f61a7c6c965d05bad4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323024"
---
# <a name="id3dx11effectvariablegetannotationbyname-method"></a><span data-ttu-id="8dfec-107">ID3DX11EffectVariable：： GetAnnotationByName 方法</span><span class="sxs-lookup"><span data-stu-id="8dfec-107">ID3DX11EffectVariable::GetAnnotationByName method</span></span>

<span data-ttu-id="8dfec-108">依名稱取得批註。</span><span class="sxs-lookup"><span data-stu-id="8dfec-108">Get an annotation by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="8dfec-109">語法</span><span class="sxs-lookup"><span data-stu-id="8dfec-109">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetAnnotationByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="8dfec-110">參數</span><span class="sxs-lookup"><span data-stu-id="8dfec-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8dfec-111">*名稱*</span><span class="sxs-lookup"><span data-stu-id="8dfec-111">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="8dfec-112">類型： **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8dfec-112">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="8dfec-113">批註名稱。</span><span class="sxs-lookup"><span data-stu-id="8dfec-113">The annotation name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8dfec-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="8dfec-114">Return value</span></span>

<span data-ttu-id="8dfec-115">類型： **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="8dfec-115">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="8dfec-116">[**ID3DX11EffectVariable**](id3dx11effectvariable.md)的指標。</span><span class="sxs-lookup"><span data-stu-id="8dfec-116">A pointer to an [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="8dfec-117">請注意，如果找不到注釋，則傳回的 **ID3DX11EffectVariable** 會是空的。</span><span class="sxs-lookup"><span data-stu-id="8dfec-117">Note that if the annotation is not found the **ID3DX11EffectVariable** returned will be empty.</span></span> <span data-ttu-id="8dfec-118">應呼叫 [**ID3DX11EffectVariable：： IsValid**](id3dx11effectvariable-isvalid.md) 方法，以判斷是否找到注釋。</span><span class="sxs-lookup"><span data-stu-id="8dfec-118">The [**ID3DX11EffectVariable::IsValid**](id3dx11effectvariable-isvalid.md) method should be called to determine whether the annotation was found.</span></span>

## <a name="remarks"></a><span data-ttu-id="8dfec-119">備註</span><span class="sxs-lookup"><span data-stu-id="8dfec-119">Remarks</span></span>

<span data-ttu-id="8dfec-120">Annonations 可以附加至技術、pass 或全域變數。</span><span class="sxs-lookup"><span data-stu-id="8dfec-120">Annonations can be attached to a technique, a pass, or a global variable.</span></span>

> [!Note]  
> <span data-ttu-id="8dfec-121">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="8dfec-121">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="8dfec-122">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="8dfec-122">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="8dfec-123">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="8dfec-123">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8dfec-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="8dfec-124">Requirements</span></span>



| <span data-ttu-id="8dfec-125">需求</span><span class="sxs-lookup"><span data-stu-id="8dfec-125">Requirement</span></span> | <span data-ttu-id="8dfec-126">值</span><span class="sxs-lookup"><span data-stu-id="8dfec-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8dfec-127">標頭</span><span class="sxs-lookup"><span data-stu-id="8dfec-127">Header</span></span><br/>  | <dl> <span data-ttu-id="8dfec-128"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="8dfec-128"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="8dfec-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="8dfec-129">Library</span></span><br/> | <dl> <span data-ttu-id="8dfec-130"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="8dfec-130"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8dfec-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8dfec-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8dfec-132">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="8dfec-132">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 


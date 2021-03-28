---
title: 'ID3DX11EffectTechnique GetAnnotationByName 方法 (D3dx11effect .h) '
description: '依名稱取得批註。 |ID3DX11EffectTechnique GetAnnotationByName 方法 (D3dx11effect .h) '
ms.assetid: 3a9e1fa7-4586-42d6-a723-3140f29a01b4
keywords:
- GetAnnotationByName 方法 Direct3D 11
- GetAnnotationByName 方法 Direct3D 11，ID3DX11EffectTechnique 介面
- ID3DX11EffectTechnique 介面 Direct3D 11，GetAnnotationByName 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectTechnique.GetAnnotationByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cae5a7c24d392bd034dfcd69fb67723c9492f982
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323027"
---
# <a name="id3dx11effecttechniquegetannotationbyname-method"></a><span data-ttu-id="d63bd-107">ID3DX11EffectTechnique：： GetAnnotationByName 方法</span><span class="sxs-lookup"><span data-stu-id="d63bd-107">ID3DX11EffectTechnique::GetAnnotationByName method</span></span>

<span data-ttu-id="d63bd-108">依名稱取得批註。</span><span class="sxs-lookup"><span data-stu-id="d63bd-108">Get an annotation by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="d63bd-109">語法</span><span class="sxs-lookup"><span data-stu-id="d63bd-109">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetAnnotationByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="d63bd-110">參數</span><span class="sxs-lookup"><span data-stu-id="d63bd-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d63bd-111">*名稱*</span><span class="sxs-lookup"><span data-stu-id="d63bd-111">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="d63bd-112">類型： **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d63bd-112">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d63bd-113">注釋的名稱。</span><span class="sxs-lookup"><span data-stu-id="d63bd-113">Name of the annotation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d63bd-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="d63bd-114">Return value</span></span>

<span data-ttu-id="d63bd-115">類型： **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="d63bd-115">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="d63bd-116">[**ID3DX11EffectVariable**](id3dx11effectvariable.md)的指標。</span><span class="sxs-lookup"><span data-stu-id="d63bd-116">A pointer to an [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d63bd-117">備註</span><span class="sxs-lookup"><span data-stu-id="d63bd-117">Remarks</span></span>

<span data-ttu-id="d63bd-118">使用注釋，將中繼資料的片段附加至技術。</span><span class="sxs-lookup"><span data-stu-id="d63bd-118">Use an annotation to attach a piece of metadata to a technique.</span></span>

> [!Note]  
> <span data-ttu-id="d63bd-119">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="d63bd-119">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="d63bd-120">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="d63bd-120">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="d63bd-121">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="d63bd-121">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d63bd-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="d63bd-122">Requirements</span></span>



| <span data-ttu-id="d63bd-123">需求</span><span class="sxs-lookup"><span data-stu-id="d63bd-123">Requirement</span></span> | <span data-ttu-id="d63bd-124">值</span><span class="sxs-lookup"><span data-stu-id="d63bd-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d63bd-125">標頭</span><span class="sxs-lookup"><span data-stu-id="d63bd-125">Header</span></span><br/>  | <dl> <span data-ttu-id="d63bd-126"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="d63bd-126"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="d63bd-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="d63bd-127">Library</span></span><br/> | <dl> <span data-ttu-id="d63bd-128"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="d63bd-128"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d63bd-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d63bd-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d63bd-130">ID3DX11EffectTechnique</span><span class="sxs-lookup"><span data-stu-id="d63bd-130">ID3DX11EffectTechnique</span></span>](id3dx11effecttechnique.md)
</dt> </dl>

 


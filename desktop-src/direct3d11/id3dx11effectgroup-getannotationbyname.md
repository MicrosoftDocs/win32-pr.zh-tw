---
title: 'ID3DX11EffectGroup GetAnnotationByName 方法 (D3dx11effect .h) '
description: '依名稱取得批註。 |ID3DX11EffectGroup GetAnnotationByName 方法 (D3dx11effect .h) '
ms.assetid: c526a249-fb56-47bb-a0c2-b829a1da88e8
keywords:
- GetAnnotationByName 方法 Direct3D 11
- GetAnnotationByName 方法 Direct3D 11，ID3DX11EffectGroup 介面
- ID3DX11EffectGroup 介面 Direct3D 11，GetAnnotationByName 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectGroup.GetAnnotationByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a1880983785fcfea8a4cda4aa09c8baec2cfebf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992246"
---
# <a name="id3dx11effectgroupgetannotationbyname-method"></a><span data-ttu-id="e8104-107">ID3DX11EffectGroup：： GetAnnotationByName 方法</span><span class="sxs-lookup"><span data-stu-id="e8104-107">ID3DX11EffectGroup::GetAnnotationByName method</span></span>

<span data-ttu-id="e8104-108">依名稱取得批註。</span><span class="sxs-lookup"><span data-stu-id="e8104-108">Get an annotation by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8104-109">語法</span><span class="sxs-lookup"><span data-stu-id="e8104-109">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetAnnotationByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="e8104-110">參數</span><span class="sxs-lookup"><span data-stu-id="e8104-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8104-111">*名稱*</span><span class="sxs-lookup"><span data-stu-id="e8104-111">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="e8104-112">類型： **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e8104-112">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e8104-113">註釋的名稱。</span><span class="sxs-lookup"><span data-stu-id="e8104-113">The name of the annotation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8104-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="e8104-114">Return value</span></span>

<span data-ttu-id="e8104-115">類型： **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="e8104-115">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="e8104-116">[**ID3DX11EffectVariable**](id3dx11effectvariable.md)的指標。</span><span class="sxs-lookup"><span data-stu-id="e8104-116">A pointer to an [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="e8104-117">請注意，如果找不到注釋，則傳回的 **ID3DX11EffectVariable** 會是空的。</span><span class="sxs-lookup"><span data-stu-id="e8104-117">Note that if the annotation is not found the **ID3DX11EffectVariable** returned will be empty.</span></span> <span data-ttu-id="e8104-118">應呼叫 [**ID3DX11EffectVariable：： IsValid**](id3dx11effectvariable-isvalid.md) 方法，以判斷是否找到注釋。</span><span class="sxs-lookup"><span data-stu-id="e8104-118">The [**ID3DX11EffectVariable::IsValid**](id3dx11effectvariable-isvalid.md) method should be called to determine whether the annotation was found.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8104-119">備註</span><span class="sxs-lookup"><span data-stu-id="e8104-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e8104-120">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="e8104-120">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="e8104-121">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="e8104-121">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="e8104-122">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="e8104-122">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e8104-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="e8104-123">Requirements</span></span>



| <span data-ttu-id="e8104-124">需求</span><span class="sxs-lookup"><span data-stu-id="e8104-124">Requirement</span></span> | <span data-ttu-id="e8104-125">值</span><span class="sxs-lookup"><span data-stu-id="e8104-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8104-126">標頭</span><span class="sxs-lookup"><span data-stu-id="e8104-126">Header</span></span><br/>  | <dl> <span data-ttu-id="e8104-127"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="e8104-127"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="e8104-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="e8104-128">Library</span></span><br/> | <dl> <span data-ttu-id="e8104-129"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="e8104-129"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8104-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e8104-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8104-131">ID3DX11EffectGroup</span><span class="sxs-lookup"><span data-stu-id="e8104-131">ID3DX11EffectGroup</span></span>](id3dx11effectgroup.md)
</dt> </dl>

 


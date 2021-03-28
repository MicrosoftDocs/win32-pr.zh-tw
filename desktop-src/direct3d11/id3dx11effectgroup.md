---
title: 'ID3DX11EffectGroup 介面 (D3dx11effect .h) '
description: ID3DX11EffectGroup 介面會存取效果群組。ID3DX11EffectGroup 物件的存留期等於其父 ID3DX11Effect 物件的存留期。
ms.assetid: f5a35c47-0bac-4559-bd6c-5e8bc7699e10
keywords:
- ID3DX11EffectGroup 介面 Direct3D 11
- ID3DX11EffectGroup 介面 Direct3D 11，描述
topic_type:
- apiref
api_name:
- ID3DX11EffectGroup
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5970506b850d164a4018cd371e19bfab6cd3624
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974564"
---
# <a name="id3dx11effectgroup-interface"></a><span data-ttu-id="4572a-105">ID3DX11EffectGroup 介面</span><span class="sxs-lookup"><span data-stu-id="4572a-105">ID3DX11EffectGroup interface</span></span>

<span data-ttu-id="4572a-106">**ID3DX11EffectGroup** 介面會存取效果群組。</span><span class="sxs-lookup"><span data-stu-id="4572a-106">The **ID3DX11EffectGroup** interface accesses an Effect group.</span></span>

<span data-ttu-id="4572a-107">**ID3DX11EffectGroup** 物件的存留期等於其父 [**ID3DX11Effect**](id3dx11effect.md)物件的存留期。</span><span class="sxs-lookup"><span data-stu-id="4572a-107">The lifetime of an **ID3DX11EffectGroup** object is equal to the lifetime of its parent [**ID3DX11Effect**](id3dx11effect.md) object.</span></span>

-   [<span data-ttu-id="4572a-108">方法</span><span class="sxs-lookup"><span data-stu-id="4572a-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4572a-109">方法</span><span class="sxs-lookup"><span data-stu-id="4572a-109">Methods</span></span>

<span data-ttu-id="4572a-110">**ID3DX11EffectGroup** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="4572a-110">The **ID3DX11EffectGroup** interface has these methods.</span></span>



| <span data-ttu-id="4572a-111">方法</span><span class="sxs-lookup"><span data-stu-id="4572a-111">Method</span></span>                                                                  | <span data-ttu-id="4572a-112">描述</span><span class="sxs-lookup"><span data-stu-id="4572a-112">Description</span></span>                                                   |
|:------------------------------------------------------------------------|:--------------------------------------------------------------|
| [<span data-ttu-id="4572a-113">**GetAnnotationByIndex**</span><span class="sxs-lookup"><span data-stu-id="4572a-113">**GetAnnotationByIndex**</span></span>](id3dx11effectgroup-getannotationbyindex.md) | <span data-ttu-id="4572a-114">依索引取得批註。</span><span class="sxs-lookup"><span data-stu-id="4572a-114">Get an annotation by index.</span></span><br/>                        |
| [<span data-ttu-id="4572a-115">**GetAnnotationByName**</span><span class="sxs-lookup"><span data-stu-id="4572a-115">**GetAnnotationByName**</span></span>](id3dx11effectgroup-getannotationbyname.md)   | <span data-ttu-id="4572a-116">依名稱取得批註。</span><span class="sxs-lookup"><span data-stu-id="4572a-116">Get an annotation by name.</span></span><br/>                         |
| [<span data-ttu-id="4572a-117">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="4572a-117">**GetDesc**</span></span>](id3dx11effectgroup-getdesc.md)                           | <span data-ttu-id="4572a-118">取得群組描述。</span><span class="sxs-lookup"><span data-stu-id="4572a-118">Gets a group description.</span></span><br/>                          |
| [<span data-ttu-id="4572a-119">**GetTechniqueByIndex**</span><span class="sxs-lookup"><span data-stu-id="4572a-119">**GetTechniqueByIndex**</span></span>](id3dx11effectgroup-gettechniquebyindex.md)   | <span data-ttu-id="4572a-120">依索引取得技術。</span><span class="sxs-lookup"><span data-stu-id="4572a-120">Get a technique by index.</span></span><br/>                          |
| [<span data-ttu-id="4572a-121">**GetTechniqueByName**</span><span class="sxs-lookup"><span data-stu-id="4572a-121">**GetTechniqueByName**</span></span>](id3dx11effectgroup-gettechniquebyname.md)     | <span data-ttu-id="4572a-122">依名稱取得技術。</span><span class="sxs-lookup"><span data-stu-id="4572a-122">Get a technique by name.</span></span><br/>                           |
| [<span data-ttu-id="4572a-123">**IsValid**</span><span class="sxs-lookup"><span data-stu-id="4572a-123">**IsValid**</span></span>](id3dx11effectgroup-isvalid.md)                           | <span data-ttu-id="4572a-124">測試效果，以查看它是否包含有效的語法。</span><span class="sxs-lookup"><span data-stu-id="4572a-124">Test an effect to see if it contains valid syntax.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4572a-125">備註</span><span class="sxs-lookup"><span data-stu-id="4572a-125">Remarks</span></span>

<span data-ttu-id="4572a-126">若要取得 **ID3DX11EffectGroup** 介面，請呼叫方法，例如 [**ID3DX11Effect：： GetGroupByName**](id3dx11effect-getgroupbyname.md)。</span><span class="sxs-lookup"><span data-stu-id="4572a-126">To get an **ID3DX11EffectGroup** interface, call a method like [**ID3DX11Effect::GetGroupByName**](id3dx11effect-getgroupbyname.md).</span></span>

> [!Note]  
> <span data-ttu-id="4572a-127">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="4572a-127">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="4572a-128">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="4572a-128">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="4572a-129">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="4572a-129">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4572a-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="4572a-130">Requirements</span></span>



| <span data-ttu-id="4572a-131">需求</span><span class="sxs-lookup"><span data-stu-id="4572a-131">Requirement</span></span> | <span data-ttu-id="4572a-132">值</span><span class="sxs-lookup"><span data-stu-id="4572a-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4572a-133">標頭</span><span class="sxs-lookup"><span data-stu-id="4572a-133">Header</span></span><br/>  | <dl> <span data-ttu-id="4572a-134"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="4572a-134"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="4572a-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="4572a-135">Library</span></span><br/> | <dl> <span data-ttu-id="4572a-136"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="4572a-136"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4572a-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4572a-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4572a-138">效果11介面</span><span class="sxs-lookup"><span data-stu-id="4572a-138">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="4572a-139">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="4572a-139">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 






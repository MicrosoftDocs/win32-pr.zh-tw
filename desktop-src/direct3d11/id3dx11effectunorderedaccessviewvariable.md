---
title: 'ID3DX11EffectUnorderedAccessViewVariable 介面 (D3dx11effect .h) '
description: 存取未排序的存取權。
ms.assetid: f78dc8c5-c85a-48cf-b579-f2937aa5ce2a
keywords:
- ID3DX11EffectUnorderedAccessViewVariable 介面 Direct3D 11
- ID3DX11EffectUnorderedAccessViewVariable 介面 Direct3D 11，描述
topic_type:
- apiref
api_name:
- ID3DX11EffectUnorderedAccessViewVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d48161ad4d9fc1773889fab0e8a0fd9a21ec793e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992142"
---
# <a name="id3dx11effectunorderedaccessviewvariable-interface"></a><span data-ttu-id="c3e24-105">ID3DX11EffectUnorderedAccessViewVariable 介面</span><span class="sxs-lookup"><span data-stu-id="c3e24-105">ID3DX11EffectUnorderedAccessViewVariable interface</span></span>

<span data-ttu-id="c3e24-106">存取未排序的存取權。</span><span class="sxs-lookup"><span data-stu-id="c3e24-106">Accesses an unordered access view.</span></span>

## <a name="members"></a><span data-ttu-id="c3e24-107">成員</span><span class="sxs-lookup"><span data-stu-id="c3e24-107">Members</span></span>

<span data-ttu-id="c3e24-108">**ID3DX11EffectUnorderedAccessViewVariable** 介面繼承自 [**ID3DX11EffectVariable**](id3dx11effectvariable.md)。</span><span class="sxs-lookup"><span data-stu-id="c3e24-108">The **ID3DX11EffectUnorderedAccessViewVariable** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="c3e24-109">**ID3DX11EffectUnorderedAccessViewVariable** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="c3e24-109">**ID3DX11EffectUnorderedAccessViewVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="c3e24-110">方法</span><span class="sxs-lookup"><span data-stu-id="c3e24-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c3e24-111">方法</span><span class="sxs-lookup"><span data-stu-id="c3e24-111">Methods</span></span>

<span data-ttu-id="c3e24-112">**ID3DX11EffectUnorderedAccessViewVariable** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="c3e24-112">The **ID3DX11EffectUnorderedAccessViewVariable** interface has these methods.</span></span>



| <span data-ttu-id="c3e24-113">方法</span><span class="sxs-lookup"><span data-stu-id="c3e24-113">Method</span></span>                                                                                                      | <span data-ttu-id="c3e24-114">描述</span><span class="sxs-lookup"><span data-stu-id="c3e24-114">Description</span></span>                                        |
|:------------------------------------------------------------------------------------------------------------|:---------------------------------------------------|
| [<span data-ttu-id="c3e24-115">**GetUnorderedAccessView**</span><span class="sxs-lookup"><span data-stu-id="c3e24-115">**GetUnorderedAccessView**</span></span>](id3dx11effectunorderedaccessviewvariable-getunorderedaccessview.md)           | <span data-ttu-id="c3e24-116">取得未排序的存取權。</span><span class="sxs-lookup"><span data-stu-id="c3e24-116">Get an unordered-access-view.</span></span><br/>           |
| [<span data-ttu-id="c3e24-117">**GetUnorderedAccessViewArray**</span><span class="sxs-lookup"><span data-stu-id="c3e24-117">**GetUnorderedAccessViewArray**</span></span>](id3dx11effectunorderedaccessviewvariable-getunorderedaccessviewarray.md) | <span data-ttu-id="c3e24-118">取得未排序存取-views 的陣列。</span><span class="sxs-lookup"><span data-stu-id="c3e24-118">Get an array of unordered-access-views.</span></span><br/> |
| [<span data-ttu-id="c3e24-119">**SetUnorderedAccessView**</span><span class="sxs-lookup"><span data-stu-id="c3e24-119">**SetUnorderedAccessView**</span></span>](id3dx11effectunorderedaccessviewvariable-setunorderedaccessview.md)           | <span data-ttu-id="c3e24-120">設定未排序的存取權。</span><span class="sxs-lookup"><span data-stu-id="c3e24-120">Set an unordered-access-view.</span></span><br/>           |
| [<span data-ttu-id="c3e24-121">**SetUnorderedAccessViewArray**</span><span class="sxs-lookup"><span data-stu-id="c3e24-121">**SetUnorderedAccessViewArray**</span></span>](id3dx11effectunorderedaccessviewvariable-setunorderedaccessviewarray.md) | <span data-ttu-id="c3e24-122">設定未排序存取-views 的陣列。</span><span class="sxs-lookup"><span data-stu-id="c3e24-122">Set an array of unordered-access-views.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c3e24-123">備註</span><span class="sxs-lookup"><span data-stu-id="c3e24-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c3e24-124">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="c3e24-124">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="c3e24-125">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="c3e24-125">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="c3e24-126">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="c3e24-126">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c3e24-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="c3e24-127">Requirements</span></span>



| <span data-ttu-id="c3e24-128">需求</span><span class="sxs-lookup"><span data-stu-id="c3e24-128">Requirement</span></span> | <span data-ttu-id="c3e24-129">值</span><span class="sxs-lookup"><span data-stu-id="c3e24-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3e24-130">標頭</span><span class="sxs-lookup"><span data-stu-id="c3e24-130">Header</span></span><br/>  | <dl> <span data-ttu-id="c3e24-131"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="c3e24-131"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="c3e24-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="c3e24-132">Library</span></span><br/> | <dl> <span data-ttu-id="c3e24-133"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="c3e24-133"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3e24-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c3e24-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3e24-135">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="c3e24-135">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="c3e24-136">效果11介面</span><span class="sxs-lookup"><span data-stu-id="c3e24-136">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="c3e24-137">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="c3e24-137">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 






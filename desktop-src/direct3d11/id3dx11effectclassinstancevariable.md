---
title: 'ID3DX11EffectClassInstanceVariable 介面 (D3dx11effect .h) '
description: 存取類別實例。
ms.assetid: 64bbae01-1b54-4b3c-9115-80d7b8911ff8
keywords:
- ID3DX11EffectClassInstanceVariable 介面 Direct3D 11
- ID3DX11EffectClassInstanceVariable 介面 Direct3D 11，描述
topic_type:
- apiref
api_name:
- ID3DX11EffectClassInstanceVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56e8b6c7ca76dd595363fa0cd80753fce0b66b2e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323371"
---
# <a name="id3dx11effectclassinstancevariable-interface"></a><span data-ttu-id="e6ce1-105">ID3DX11EffectClassInstanceVariable 介面</span><span class="sxs-lookup"><span data-stu-id="e6ce1-105">ID3DX11EffectClassInstanceVariable interface</span></span>

<span data-ttu-id="e6ce1-106">存取類別實例。</span><span class="sxs-lookup"><span data-stu-id="e6ce1-106">Accesses a class instance.</span></span>

## <a name="members"></a><span data-ttu-id="e6ce1-107">成員</span><span class="sxs-lookup"><span data-stu-id="e6ce1-107">Members</span></span>

<span data-ttu-id="e6ce1-108">**ID3DX11EffectClassInstanceVariable** 介面繼承自 [**ID3DX11EffectVariable**](id3dx11effectvariable.md)。</span><span class="sxs-lookup"><span data-stu-id="e6ce1-108">The **ID3DX11EffectClassInstanceVariable** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="e6ce1-109">**ID3DX11EffectClassInstanceVariable** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e6ce1-109">**ID3DX11EffectClassInstanceVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="e6ce1-110">方法</span><span class="sxs-lookup"><span data-stu-id="e6ce1-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e6ce1-111">方法</span><span class="sxs-lookup"><span data-stu-id="e6ce1-111">Methods</span></span>

<span data-ttu-id="e6ce1-112">**ID3DX11EffectClassInstanceVariable** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="e6ce1-112">The **ID3DX11EffectClassInstanceVariable** interface has these methods.</span></span>



| <span data-ttu-id="e6ce1-113">方法</span><span class="sxs-lookup"><span data-stu-id="e6ce1-113">Method</span></span>                                                                          | <span data-ttu-id="e6ce1-114">描述</span><span class="sxs-lookup"><span data-stu-id="e6ce1-114">Description</span></span>                       |
|:--------------------------------------------------------------------------------|:----------------------------------|
| [<span data-ttu-id="e6ce1-115">**GetClassInstance**</span><span class="sxs-lookup"><span data-stu-id="e6ce1-115">**GetClassInstance**</span></span>](id3dx11effectclassinstancevariable-getclassinstance.md) | <span data-ttu-id="e6ce1-116">取得類別實例。</span><span class="sxs-lookup"><span data-stu-id="e6ce1-116">Gets a class instance.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e6ce1-117">備註</span><span class="sxs-lookup"><span data-stu-id="e6ce1-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e6ce1-118">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="e6ce1-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="e6ce1-119">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="e6ce1-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="e6ce1-120">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="e6ce1-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e6ce1-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="e6ce1-121">Requirements</span></span>



| <span data-ttu-id="e6ce1-122">需求</span><span class="sxs-lookup"><span data-stu-id="e6ce1-122">Requirement</span></span> | <span data-ttu-id="e6ce1-123">值</span><span class="sxs-lookup"><span data-stu-id="e6ce1-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6ce1-124">標頭</span><span class="sxs-lookup"><span data-stu-id="e6ce1-124">Header</span></span><br/>  | <dl> <span data-ttu-id="e6ce1-125"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="e6ce1-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="e6ce1-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="e6ce1-126">Library</span></span><br/> | <dl> <span data-ttu-id="e6ce1-127"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="e6ce1-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6ce1-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e6ce1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6ce1-129">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="e6ce1-129">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="e6ce1-130">效果11介面</span><span class="sxs-lookup"><span data-stu-id="e6ce1-130">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="e6ce1-131">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="e6ce1-131">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 






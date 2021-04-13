---
title: 'ID3DX11EffectStringVariable 介面 (D3dx11effect .h) '
description: 字串變數介面會存取字串變數。
ms.assetid: 8304d7cc-de30-41fe-af12-e11bf7ae32ce
keywords:
- ID3DX11EffectStringVariable 介面 Direct3D 11
- ID3DX11EffectStringVariable 介面 Direct3D 11，描述
topic_type:
- apiref
api_name:
- ID3DX11EffectStringVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a45eb5e0825bd8487396ed850c9d79665e5f1044
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992146"
---
# <a name="id3dx11effectstringvariable-interface"></a><span data-ttu-id="ea2cc-105">ID3DX11EffectStringVariable 介面</span><span class="sxs-lookup"><span data-stu-id="ea2cc-105">ID3DX11EffectStringVariable interface</span></span>

<span data-ttu-id="ea2cc-106">字串變數介面會存取字串變數。</span><span class="sxs-lookup"><span data-stu-id="ea2cc-106">A string-variable interface accesses a string variable.</span></span>

## <a name="members"></a><span data-ttu-id="ea2cc-107">成員</span><span class="sxs-lookup"><span data-stu-id="ea2cc-107">Members</span></span>

<span data-ttu-id="ea2cc-108">**ID3DX11EffectStringVariable** 介面繼承自 [**ID3DX11EffectVariable**](id3dx11effectvariable.md)。</span><span class="sxs-lookup"><span data-stu-id="ea2cc-108">The **ID3DX11EffectStringVariable** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="ea2cc-109">**ID3DX11EffectStringVariable** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="ea2cc-109">**ID3DX11EffectStringVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="ea2cc-110">方法</span><span class="sxs-lookup"><span data-stu-id="ea2cc-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ea2cc-111">方法</span><span class="sxs-lookup"><span data-stu-id="ea2cc-111">Methods</span></span>

<span data-ttu-id="ea2cc-112">**ID3DX11EffectStringVariable** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="ea2cc-112">The **ID3DX11EffectStringVariable** interface has these methods.</span></span>



| <span data-ttu-id="ea2cc-113">方法</span><span class="sxs-lookup"><span data-stu-id="ea2cc-113">Method</span></span>                                                               | <span data-ttu-id="ea2cc-114">描述</span><span class="sxs-lookup"><span data-stu-id="ea2cc-114">Description</span></span>                         |
|:---------------------------------------------------------------------|:------------------------------------|
| [<span data-ttu-id="ea2cc-115">**GetString**</span><span class="sxs-lookup"><span data-stu-id="ea2cc-115">**GetString**</span></span>](id3dx11effectstringvariable-getstring.md)           | <span data-ttu-id="ea2cc-116">取得字串。</span><span class="sxs-lookup"><span data-stu-id="ea2cc-116">Get the string.</span></span><br/>          |
| [<span data-ttu-id="ea2cc-117">**GetStringArray**</span><span class="sxs-lookup"><span data-stu-id="ea2cc-117">**GetStringArray**</span></span>](id3dx11effectstringvariable-getstringarray.md) | <span data-ttu-id="ea2cc-118">取得字串的陣列。</span><span class="sxs-lookup"><span data-stu-id="ea2cc-118">Get an array of strings.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ea2cc-119">備註</span><span class="sxs-lookup"><span data-stu-id="ea2cc-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ea2cc-120">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="ea2cc-120">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="ea2cc-121">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="ea2cc-121">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="ea2cc-122">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="ea2cc-122">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ea2cc-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="ea2cc-123">Requirements</span></span>



| <span data-ttu-id="ea2cc-124">需求</span><span class="sxs-lookup"><span data-stu-id="ea2cc-124">Requirement</span></span> | <span data-ttu-id="ea2cc-125">值</span><span class="sxs-lookup"><span data-stu-id="ea2cc-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea2cc-126">標頭</span><span class="sxs-lookup"><span data-stu-id="ea2cc-126">Header</span></span><br/>  | <dl> <span data-ttu-id="ea2cc-127"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="ea2cc-127"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="ea2cc-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="ea2cc-128">Library</span></span><br/> | <dl> <span data-ttu-id="ea2cc-129"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="ea2cc-129"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea2cc-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ea2cc-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea2cc-131">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="ea2cc-131">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="ea2cc-132">效果11介面</span><span class="sxs-lookup"><span data-stu-id="ea2cc-132">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="ea2cc-133">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="ea2cc-133">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 






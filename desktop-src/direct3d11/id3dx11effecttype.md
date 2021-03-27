---
title: 'ID3DX11EffectType 介面 (D3dx11effect .h) '
description: ID3DX11EffectType 介面會依類型存取效果變數。ID3DX11EffectType 物件的存留期等於其父 ID3DX11Effect 物件的存留期。
ms.assetid: 700076ee-a5fe-4af2-a5f4-053c05d8ddf0
keywords:
- ID3DX11EffectType 介面 Direct3D 11
- ID3DX11EffectType 介面 Direct3D 11，描述
topic_type:
- apiref
api_name:
- ID3DX11EffectType
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e3c210ca60abc9e55b8864a2b121cf92be369a3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103696599"
---
# <a name="id3dx11effecttype-interface"></a><span data-ttu-id="4a9d0-105">ID3DX11EffectType 介面</span><span class="sxs-lookup"><span data-stu-id="4a9d0-105">ID3DX11EffectType interface</span></span>

<span data-ttu-id="4a9d0-106">**ID3DX11EffectType** 介面會依類型存取效果變數。</span><span class="sxs-lookup"><span data-stu-id="4a9d0-106">The **ID3DX11EffectType** interface accesses effect variables by type.</span></span>

<span data-ttu-id="4a9d0-107">**ID3DX11EffectType** 物件的存留期等於其父 [**ID3DX11Effect**](id3dx11effect.md)物件的存留期。</span><span class="sxs-lookup"><span data-stu-id="4a9d0-107">The lifetime of an **ID3DX11EffectType** object is equal to the lifetime of its parent [**ID3DX11Effect**](id3dx11effect.md) object.</span></span>

-   [<span data-ttu-id="4a9d0-108">方法</span><span class="sxs-lookup"><span data-stu-id="4a9d0-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4a9d0-109">方法</span><span class="sxs-lookup"><span data-stu-id="4a9d0-109">Methods</span></span>

<span data-ttu-id="4a9d0-110">**ID3DX11EffectType** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="4a9d0-110">The **ID3DX11EffectType** interface has these methods.</span></span>



| <span data-ttu-id="4a9d0-111">方法</span><span class="sxs-lookup"><span data-stu-id="4a9d0-111">Method</span></span>                                                                       | <span data-ttu-id="4a9d0-112">描述</span><span class="sxs-lookup"><span data-stu-id="4a9d0-112">Description</span></span>                                       |
|:-----------------------------------------------------------------------------|:--------------------------------------------------|
| [<span data-ttu-id="4a9d0-113">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="4a9d0-113">**GetDesc**</span></span>](id3dx11effecttype-getdesc.md)                                 | <span data-ttu-id="4a9d0-114">取得效果類型描述。</span><span class="sxs-lookup"><span data-stu-id="4a9d0-114">Get an effect-type description.</span></span><br/>        |
| [<span data-ttu-id="4a9d0-115">**GetMemberName**</span><span class="sxs-lookup"><span data-stu-id="4a9d0-115">**GetMemberName**</span></span>](id3dx11effecttype-getmembername.md)                     | <span data-ttu-id="4a9d0-116">取得成員的名稱。</span><span class="sxs-lookup"><span data-stu-id="4a9d0-116">Get the name of a member.</span></span><br/>              |
| [<span data-ttu-id="4a9d0-117">**GetMemberSemantic**</span><span class="sxs-lookup"><span data-stu-id="4a9d0-117">**GetMemberSemantic**</span></span>](id3dx11effecttype-getmembersemantic.md)             | <span data-ttu-id="4a9d0-118">取得附加至成員的語義。</span><span class="sxs-lookup"><span data-stu-id="4a9d0-118">Get the semantic attached to a member.</span></span><br/> |
| [<span data-ttu-id="4a9d0-119">**GetMemberTypeByIndex**</span><span class="sxs-lookup"><span data-stu-id="4a9d0-119">**GetMemberTypeByIndex**</span></span>](id3dx11effecttype-getmembertypebyindex.md)       | <span data-ttu-id="4a9d0-120">依索引取得成員類型。</span><span class="sxs-lookup"><span data-stu-id="4a9d0-120">Get a member type by index.</span></span><br/>            |
| [<span data-ttu-id="4a9d0-121">**GetMemberTypeByName**</span><span class="sxs-lookup"><span data-stu-id="4a9d0-121">**GetMemberTypeByName**</span></span>](id3dx11effecttype-getmembertypebyname.md)         | <span data-ttu-id="4a9d0-122">依名稱取得成員類型。</span><span class="sxs-lookup"><span data-stu-id="4a9d0-122">Get an member type by name.</span></span><br/>            |
| [<span data-ttu-id="4a9d0-123">**GetMemberTypeBySemantic**</span><span class="sxs-lookup"><span data-stu-id="4a9d0-123">**GetMemberTypeBySemantic**</span></span>](id3dx11effecttype-getmembertypebysemantic.md) | <span data-ttu-id="4a9d0-124">依語義取得成員類型。</span><span class="sxs-lookup"><span data-stu-id="4a9d0-124">Get a member type by semantic.</span></span><br/>         |
| [<span data-ttu-id="4a9d0-125">**IsValid**</span><span class="sxs-lookup"><span data-stu-id="4a9d0-125">**IsValid**</span></span>](id3dx11effecttype-isvalid.md)                                 | <span data-ttu-id="4a9d0-126">測試效果類型是否有效。</span><span class="sxs-lookup"><span data-stu-id="4a9d0-126">Tests that the effect type is valid.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="4a9d0-127">備註</span><span class="sxs-lookup"><span data-stu-id="4a9d0-127">Remarks</span></span>

<span data-ttu-id="4a9d0-128">若要從效果變數取得效果類型的相關資訊，請呼叫 [**ID3DX11EffectVariable：： GetType**](id3dx11effectvariable-gettype.md)。</span><span class="sxs-lookup"><span data-stu-id="4a9d0-128">To get information about an effect type from an effect variable, call [**ID3DX11EffectVariable::GetType**](id3dx11effectvariable-gettype.md).</span></span>

> [!Note]  
> <span data-ttu-id="4a9d0-129">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="4a9d0-129">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="4a9d0-130">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="4a9d0-130">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="4a9d0-131">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="4a9d0-131">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4a9d0-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="4a9d0-132">Requirements</span></span>



| <span data-ttu-id="4a9d0-133">需求</span><span class="sxs-lookup"><span data-stu-id="4a9d0-133">Requirement</span></span> | <span data-ttu-id="4a9d0-134">值</span><span class="sxs-lookup"><span data-stu-id="4a9d0-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a9d0-135">標頭</span><span class="sxs-lookup"><span data-stu-id="4a9d0-135">Header</span></span><br/>  | <dl> <span data-ttu-id="4a9d0-136"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="4a9d0-136"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="4a9d0-137">程式庫</span><span class="sxs-lookup"><span data-stu-id="4a9d0-137">Library</span></span><br/> | <dl> <span data-ttu-id="4a9d0-138"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="4a9d0-138"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a9d0-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4a9d0-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a9d0-140">效果11介面</span><span class="sxs-lookup"><span data-stu-id="4a9d0-140">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="4a9d0-141">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="4a9d0-141">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 






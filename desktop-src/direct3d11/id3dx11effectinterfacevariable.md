---
title: 'ID3DX11EffectInterfaceVariable 介面 (D3dx11effect .h) '
description: 存取介面變數。
ms.assetid: c1d1f564-c7b8-4108-9988-972255662000
keywords:
- ID3DX11EffectInterfaceVariable 介面 Direct3D 11
- ID3DX11EffectInterfaceVariable 介面 Direct3D 11，描述
topic_type:
- apiref
api_name:
- ID3DX11EffectInterfaceVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8169afc18e6974168e9196962b3e0cf87e860e4c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974557"
---
# <a name="id3dx11effectinterfacevariable-interface"></a><span data-ttu-id="23f0e-105">ID3DX11EffectInterfaceVariable 介面</span><span class="sxs-lookup"><span data-stu-id="23f0e-105">ID3DX11EffectInterfaceVariable interface</span></span>

<span data-ttu-id="23f0e-106">存取介面變數。</span><span class="sxs-lookup"><span data-stu-id="23f0e-106">Accesses an interface variable.</span></span>

## <a name="members"></a><span data-ttu-id="23f0e-107">成員</span><span class="sxs-lookup"><span data-stu-id="23f0e-107">Members</span></span>

<span data-ttu-id="23f0e-108">**ID3DX11EffectInterfaceVariable** 介面繼承自 [**ID3DX11EffectVariable**](id3dx11effectvariable.md)。</span><span class="sxs-lookup"><span data-stu-id="23f0e-108">The **ID3DX11EffectInterfaceVariable** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="23f0e-109">**ID3DX11EffectInterfaceVariable** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="23f0e-109">**ID3DX11EffectInterfaceVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="23f0e-110">方法</span><span class="sxs-lookup"><span data-stu-id="23f0e-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="23f0e-111">方法</span><span class="sxs-lookup"><span data-stu-id="23f0e-111">Methods</span></span>

<span data-ttu-id="23f0e-112">**ID3DX11EffectInterfaceVariable** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="23f0e-112">The **ID3DX11EffectInterfaceVariable** interface has these methods.</span></span>



| <span data-ttu-id="23f0e-113">方法</span><span class="sxs-lookup"><span data-stu-id="23f0e-113">Method</span></span>                                                                      | <span data-ttu-id="23f0e-114">描述</span><span class="sxs-lookup"><span data-stu-id="23f0e-114">Description</span></span>                       |
|:----------------------------------------------------------------------------|:----------------------------------|
| [<span data-ttu-id="23f0e-115">**GetClassInstance**</span><span class="sxs-lookup"><span data-stu-id="23f0e-115">**GetClassInstance**</span></span>](id3dx11effectinterfacevariable-getclassinstance.md) | <span data-ttu-id="23f0e-116">取得類別實例。</span><span class="sxs-lookup"><span data-stu-id="23f0e-116">Get a class instance.</span></span><br/>  |
| [<span data-ttu-id="23f0e-117">**SetClassInstance**</span><span class="sxs-lookup"><span data-stu-id="23f0e-117">**SetClassInstance**</span></span>](id3dx11effectinterfacevariable-setclassinstance.md) | <span data-ttu-id="23f0e-118">設定類別實例。</span><span class="sxs-lookup"><span data-stu-id="23f0e-118">Sets a class instance.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="23f0e-119">備註</span><span class="sxs-lookup"><span data-stu-id="23f0e-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="23f0e-120">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="23f0e-120">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="23f0e-121">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="23f0e-121">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="23f0e-122">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="23f0e-122">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="23f0e-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="23f0e-123">Requirements</span></span>



| <span data-ttu-id="23f0e-124">需求</span><span class="sxs-lookup"><span data-stu-id="23f0e-124">Requirement</span></span> | <span data-ttu-id="23f0e-125">值</span><span class="sxs-lookup"><span data-stu-id="23f0e-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23f0e-126">標頭</span><span class="sxs-lookup"><span data-stu-id="23f0e-126">Header</span></span><br/>  | <dl> <span data-ttu-id="23f0e-127"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="23f0e-127"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="23f0e-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="23f0e-128">Library</span></span><br/> | <dl> <span data-ttu-id="23f0e-129"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="23f0e-129"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23f0e-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="23f0e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23f0e-131">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="23f0e-131">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="23f0e-132">效果11介面</span><span class="sxs-lookup"><span data-stu-id="23f0e-132">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="23f0e-133">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="23f0e-133">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 






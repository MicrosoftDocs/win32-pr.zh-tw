---
title: 'ID3DX11EffectBlendVariable 介面 (D3dx11effect .h) '
description: Blend 變數介面會存取 blend 狀態。
ms.assetid: 8a6e6e7e-2f1e-4e16-8d28-ffc7f3f018d6
keywords:
- ID3DX11EffectBlendVariable 介面 Direct3D 11
- ID3DX11EffectBlendVariable 介面 Direct3D 11，描述
topic_type:
- apiref
api_name:
- ID3DX11EffectBlendVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57a0a8a3ec0c2a3d92dfc9579fff8b3769dcfc5d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946257"
---
# <a name="id3dx11effectblendvariable-interface"></a><span data-ttu-id="c9faf-105">ID3DX11EffectBlendVariable 介面</span><span class="sxs-lookup"><span data-stu-id="c9faf-105">ID3DX11EffectBlendVariable interface</span></span>

<span data-ttu-id="c9faf-106">Blend 變數介面會存取 blend 狀態。</span><span class="sxs-lookup"><span data-stu-id="c9faf-106">The blend-variable interface accesses blend state.</span></span>

## <a name="members"></a><span data-ttu-id="c9faf-107">成員</span><span class="sxs-lookup"><span data-stu-id="c9faf-107">Members</span></span>

<span data-ttu-id="c9faf-108">**ID3DX11EffectBlendVariable** 介面繼承自 [**ID3DX11EffectVariable**](id3dx11effectvariable.md)。</span><span class="sxs-lookup"><span data-stu-id="c9faf-108">The **ID3DX11EffectBlendVariable** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="c9faf-109">**ID3DX11EffectBlendVariable** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="c9faf-109">**ID3DX11EffectBlendVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="c9faf-110">方法</span><span class="sxs-lookup"><span data-stu-id="c9faf-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c9faf-111">方法</span><span class="sxs-lookup"><span data-stu-id="c9faf-111">Methods</span></span>

<span data-ttu-id="c9faf-112">**ID3DX11EffectBlendVariable** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="c9faf-112">The **ID3DX11EffectBlendVariable** interface has these methods.</span></span>



| <span data-ttu-id="c9faf-113">方法</span><span class="sxs-lookup"><span data-stu-id="c9faf-113">Method</span></span>                                                                    | <span data-ttu-id="c9faf-114">描述</span><span class="sxs-lookup"><span data-stu-id="c9faf-114">Description</span></span>                                          |
|:--------------------------------------------------------------------------|:-----------------------------------------------------|
| [<span data-ttu-id="c9faf-115">**GetBackingStore**</span><span class="sxs-lookup"><span data-stu-id="c9faf-115">**GetBackingStore**</span></span>](id3dx11effectblendvariable-getbackingstore.md)     | <span data-ttu-id="c9faf-116">取得 blend 狀態變數的指標。</span><span class="sxs-lookup"><span data-stu-id="c9faf-116">Get a pointer to a blend-state variable.</span></span><br/>  |
| [<span data-ttu-id="c9faf-117">**GetBlendState**</span><span class="sxs-lookup"><span data-stu-id="c9faf-117">**GetBlendState**</span></span>](id3dx11effectblendvariable-getblendstate.md)         | <span data-ttu-id="c9faf-118">取得 blend 狀態介面的指標。</span><span class="sxs-lookup"><span data-stu-id="c9faf-118">Get a pointer to a blend-state interface.</span></span><br/> |
| [<span data-ttu-id="c9faf-119">**SetBlendState**</span><span class="sxs-lookup"><span data-stu-id="c9faf-119">**SetBlendState**</span></span>](id3dx11effectblendvariable-setblendstate.md)         | <span data-ttu-id="c9faf-120">設定效果的 blend 狀態。</span><span class="sxs-lookup"><span data-stu-id="c9faf-120">Sets an effect's blend-state.</span></span><br/>             |
| [<span data-ttu-id="c9faf-121">**UndoSetBlendState**</span><span class="sxs-lookup"><span data-stu-id="c9faf-121">**UndoSetBlendState**</span></span>](id3dx11effectblendvariable-undosetblendstate.md) | <span data-ttu-id="c9faf-122">還原先前設定的 blend 狀態。</span><span class="sxs-lookup"><span data-stu-id="c9faf-122">Reverts a previously set blend-state.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="c9faf-123">備註</span><span class="sxs-lookup"><span data-stu-id="c9faf-123">Remarks</span></span>

<span data-ttu-id="c9faf-124">當將效果讀入記憶體時，就會建立 [**ID3DX11EffectVariable**](id3dx11effectvariable.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="c9faf-124">An [**ID3DX11EffectVariable**](id3dx11effectvariable.md) interface is created when an effect is read into memory.</span></span>

<span data-ttu-id="c9faf-125">效果變數會儲存在備份存放區的記憶體中;套用技術時，備份存放區中的值會複製到裝置。</span><span class="sxs-lookup"><span data-stu-id="c9faf-125">Effect variables are saved in memory in the backing store; when a technique is applied, the values in the backing store are copied to the device.</span></span> <span data-ttu-id="c9faf-126">您可以使用其中一種方法來傳回狀態。</span><span class="sxs-lookup"><span data-stu-id="c9faf-126">You can use either of these methods to return state.</span></span>

> [!Note]  
> <span data-ttu-id="c9faf-127">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="c9faf-127">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="c9faf-128">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="c9faf-128">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="c9faf-129">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="c9faf-129">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c9faf-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="c9faf-130">Requirements</span></span>



| <span data-ttu-id="c9faf-131">需求</span><span class="sxs-lookup"><span data-stu-id="c9faf-131">Requirement</span></span> | <span data-ttu-id="c9faf-132">值</span><span class="sxs-lookup"><span data-stu-id="c9faf-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9faf-133">標頭</span><span class="sxs-lookup"><span data-stu-id="c9faf-133">Header</span></span><br/>  | <dl> <span data-ttu-id="c9faf-134"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="c9faf-134"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="c9faf-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="c9faf-135">Library</span></span><br/> | <dl> <span data-ttu-id="c9faf-136"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="c9faf-136"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9faf-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c9faf-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9faf-138">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="c9faf-138">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="c9faf-139">效果11介面</span><span class="sxs-lookup"><span data-stu-id="c9faf-139">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="c9faf-140">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="c9faf-140">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 






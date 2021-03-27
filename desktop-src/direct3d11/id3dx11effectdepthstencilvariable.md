---
title: 'ID3DX11EffectDepthStencilVariable 介面 (D3dx11effect .h) '
description: 深度樣板變數介面會存取深度樣板的狀態。
ms.assetid: 8fb1be19-eed4-4d69-bbbe-94484531eba2
keywords:
- ID3DX11EffectDepthStencilVariable 介面 Direct3D 11
- ID3DX11EffectDepthStencilVariable 介面 Direct3D 11，描述
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d7aa520df0c13c81435421d5f605f901a61da6e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946213"
---
# <a name="id3dx11effectdepthstencilvariable-interface"></a><span data-ttu-id="f5907-105">ID3DX11EffectDepthStencilVariable 介面</span><span class="sxs-lookup"><span data-stu-id="f5907-105">ID3DX11EffectDepthStencilVariable interface</span></span>

<span data-ttu-id="f5907-106">深度樣板變數介面會存取深度樣板的狀態。</span><span class="sxs-lookup"><span data-stu-id="f5907-106">A depth-stencil-variable interface accesses depth-stencil state.</span></span>

## <a name="members"></a><span data-ttu-id="f5907-107">成員</span><span class="sxs-lookup"><span data-stu-id="f5907-107">Members</span></span>

<span data-ttu-id="f5907-108">**ID3DX11EffectDepthStencilVariable** 介面繼承自 [**ID3DX11EffectVariable**](id3dx11effectvariable.md)。</span><span class="sxs-lookup"><span data-stu-id="f5907-108">The **ID3DX11EffectDepthStencilVariable** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="f5907-109">**ID3DX11EffectDepthStencilVariable** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="f5907-109">**ID3DX11EffectDepthStencilVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="f5907-110">方法</span><span class="sxs-lookup"><span data-stu-id="f5907-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f5907-111">方法</span><span class="sxs-lookup"><span data-stu-id="f5907-111">Methods</span></span>

<span data-ttu-id="f5907-112">**ID3DX11EffectDepthStencilVariable** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="f5907-112">The **ID3DX11EffectDepthStencilVariable** interface has these methods.</span></span>



| <span data-ttu-id="f5907-113">方法</span><span class="sxs-lookup"><span data-stu-id="f5907-113">Method</span></span>                                                                                         | <span data-ttu-id="f5907-114">描述</span><span class="sxs-lookup"><span data-stu-id="f5907-114">Description</span></span>                                                               |
|:-----------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------|
| [<span data-ttu-id="f5907-115">**GetBackingStore**</span><span class="sxs-lookup"><span data-stu-id="f5907-115">**GetBackingStore**</span></span>](id3dx11effectdepthstencilvariable-getbackingstore.md)                   | <span data-ttu-id="f5907-116">取得包含深度樣板狀態之變數的指標。</span><span class="sxs-lookup"><span data-stu-id="f5907-116">Get a pointer to a variable that contains depth-stencil state.</span></span><br/> |
| [<span data-ttu-id="f5907-117">**GetDepthStencilState**</span><span class="sxs-lookup"><span data-stu-id="f5907-117">**GetDepthStencilState**</span></span>](id3dx11effectdepthstencilvariable-getdepthstencilstate.md)         | <span data-ttu-id="f5907-118">取得深度樣板介面的指標。</span><span class="sxs-lookup"><span data-stu-id="f5907-118">Get a pointer to a depth-stencil interface.</span></span><br/>                    |
| [<span data-ttu-id="f5907-119">**SetDepthStencilState**</span><span class="sxs-lookup"><span data-stu-id="f5907-119">**SetDepthStencilState**</span></span>](id3dx11effectdepthstencilvariable-setdepthstencilstate.md)         | <span data-ttu-id="f5907-120">設定深度樣板的狀態。</span><span class="sxs-lookup"><span data-stu-id="f5907-120">Sets the depth stencil state.</span></span><br/>                                  |
| [<span data-ttu-id="f5907-121">**UndoSetDepthStencilState**</span><span class="sxs-lookup"><span data-stu-id="f5907-121">**UndoSetDepthStencilState**</span></span>](id3dx11effectdepthstencilvariable-undosetdepthstencilstate.md) | <span data-ttu-id="f5907-122">還原先前設定的深度樣板狀態。</span><span class="sxs-lookup"><span data-stu-id="f5907-122">Reverts a previously set depth stencil state.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="f5907-123">備註</span><span class="sxs-lookup"><span data-stu-id="f5907-123">Remarks</span></span>

<span data-ttu-id="f5907-124">當將效果讀入記憶體時，就會建立 [**ID3DX11EffectVariable**](id3dx11effectvariable.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="f5907-124">An [**ID3DX11EffectVariable**](id3dx11effectvariable.md) interface is created when an effect is read into memory.</span></span>

<span data-ttu-id="f5907-125">效果變數會儲存在備份存放區的記憶體中;套用技術時，備份存放區中的值會複製到裝置。</span><span class="sxs-lookup"><span data-stu-id="f5907-125">Effect variables are saved in memory in the backing store; when a technique is applied, the values in the backing store are copied to the device.</span></span> <span data-ttu-id="f5907-126">您可以使用其中一種方法來傳回狀態。</span><span class="sxs-lookup"><span data-stu-id="f5907-126">You can use either of these methods to return state.</span></span>

> [!Note]  
> <span data-ttu-id="f5907-127">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="f5907-127">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="f5907-128">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="f5907-128">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="f5907-129">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="f5907-129">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f5907-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="f5907-130">Requirements</span></span>



| <span data-ttu-id="f5907-131">需求</span><span class="sxs-lookup"><span data-stu-id="f5907-131">Requirement</span></span> | <span data-ttu-id="f5907-132">值</span><span class="sxs-lookup"><span data-stu-id="f5907-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5907-133">標頭</span><span class="sxs-lookup"><span data-stu-id="f5907-133">Header</span></span><br/>  | <dl> <span data-ttu-id="f5907-134"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="f5907-134"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="f5907-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="f5907-135">Library</span></span><br/> | <dl> <span data-ttu-id="f5907-136"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="f5907-136"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5907-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f5907-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5907-138">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="f5907-138">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="f5907-139">效果11介面</span><span class="sxs-lookup"><span data-stu-id="f5907-139">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="f5907-140">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="f5907-140">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 






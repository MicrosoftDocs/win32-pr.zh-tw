---
title: 'ID3DX11EffectRasterizerVariable 介面 (D3dx11effect .h) '
description: 轉譯器變數介面會存取轉譯器的狀態。
ms.assetid: d039e3c5-c066-4658-bead-92a5d705ed89
keywords:
- ID3DX11EffectRasterizerVariable 介面 Direct3D 11
- ID3DX11EffectRasterizerVariable 介面 Direct3D 11，描述
topic_type:
- apiref
api_name:
- ID3DX11EffectRasterizerVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a19c5d529d6134ebad238be6e7c6195dc628a7f6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992380"
---
# <a name="id3dx11effectrasterizervariable-interface"></a><span data-ttu-id="6dcf6-105">ID3DX11EffectRasterizerVariable 介面</span><span class="sxs-lookup"><span data-stu-id="6dcf6-105">ID3DX11EffectRasterizerVariable interface</span></span>

<span data-ttu-id="6dcf6-106">轉譯器變數介面會存取轉譯器的狀態。</span><span class="sxs-lookup"><span data-stu-id="6dcf6-106">A rasterizer-variable interface accesses rasterizer state.</span></span>

## <a name="members"></a><span data-ttu-id="6dcf6-107">成員</span><span class="sxs-lookup"><span data-stu-id="6dcf6-107">Members</span></span>

<span data-ttu-id="6dcf6-108">**ID3DX11EffectRasterizerVariable** 介面繼承自 [**ID3DX11EffectVariable**](id3dx11effectvariable.md)。</span><span class="sxs-lookup"><span data-stu-id="6dcf6-108">The **ID3DX11EffectRasterizerVariable** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="6dcf6-109">**ID3DX11EffectRasterizerVariable** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="6dcf6-109">**ID3DX11EffectRasterizerVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="6dcf6-110">方法</span><span class="sxs-lookup"><span data-stu-id="6dcf6-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6dcf6-111">方法</span><span class="sxs-lookup"><span data-stu-id="6dcf6-111">Methods</span></span>

<span data-ttu-id="6dcf6-112">**ID3DX11EffectRasterizerVariable** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="6dcf6-112">The **ID3DX11EffectRasterizerVariable** interface has these methods.</span></span>



| <span data-ttu-id="6dcf6-113">方法</span><span class="sxs-lookup"><span data-stu-id="6dcf6-113">Method</span></span>                                                                                   | <span data-ttu-id="6dcf6-114">描述</span><span class="sxs-lookup"><span data-stu-id="6dcf6-114">Description</span></span>                                                            |
|:-----------------------------------------------------------------------------------------|:-----------------------------------------------------------------------|
| [<span data-ttu-id="6dcf6-115">**GetBackingStore**</span><span class="sxs-lookup"><span data-stu-id="6dcf6-115">**GetBackingStore**</span></span>](id3dx11effectrasterizervariable-getbackingstore.md)               | <span data-ttu-id="6dcf6-116">取得包含 rasteriser 狀態之變數的指標。</span><span class="sxs-lookup"><span data-stu-id="6dcf6-116">Get a pointer to a variable that contains rasteriser state.</span></span><br/> |
| [<span data-ttu-id="6dcf6-117">**GetRasterizerState**</span><span class="sxs-lookup"><span data-stu-id="6dcf6-117">**GetRasterizerState**</span></span>](id3dx11effectrasterizervariable-getrasterizerstate.md)         | <span data-ttu-id="6dcf6-118">取得轉譯器介面的指標。</span><span class="sxs-lookup"><span data-stu-id="6dcf6-118">Get a pointer to a rasterizer interface.</span></span><br/>                    |
| [<span data-ttu-id="6dcf6-119">**SetRasterizerState**</span><span class="sxs-lookup"><span data-stu-id="6dcf6-119">**SetRasterizerState**</span></span>](id3dx11effectrasterizervariable-setrasterizerstate.md)         | <span data-ttu-id="6dcf6-120">設定轉譯器的狀態。</span><span class="sxs-lookup"><span data-stu-id="6dcf6-120">Sets the rasterizer state.</span></span><br/>                                  |
| [<span data-ttu-id="6dcf6-121">**UndoSetRasterizerState**</span><span class="sxs-lookup"><span data-stu-id="6dcf6-121">**UndoSetRasterizerState**</span></span>](id3dx11effectrasterizervariable-undosetrasterizerstate.md) | <span data-ttu-id="6dcf6-122">還原先前設定的轉譯器狀態。</span><span class="sxs-lookup"><span data-stu-id="6dcf6-122">Reverts a previously set rasterizer state.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="6dcf6-123">備註</span><span class="sxs-lookup"><span data-stu-id="6dcf6-123">Remarks</span></span>

<span data-ttu-id="6dcf6-124">當將效果讀入記憶體時，就會建立 [**ID3DX11EffectVariable**](id3dx11effectvariable.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="6dcf6-124">An [**ID3DX11EffectVariable**](id3dx11effectvariable.md) interface is created when an effect is read into memory.</span></span>

<span data-ttu-id="6dcf6-125">效果變數會儲存在備份存放區的記憶體中;套用技術時，備份存放區中的值會複製到裝置。</span><span class="sxs-lookup"><span data-stu-id="6dcf6-125">Effect variables are saved in memory in the backing store; when a technique is applied, the values in the backing store are copied to the device.</span></span> <span data-ttu-id="6dcf6-126">您可以使用其中一種方法來傳回狀態。</span><span class="sxs-lookup"><span data-stu-id="6dcf6-126">You can use either of these methods to return state.</span></span>

> [!Note]  
> <span data-ttu-id="6dcf6-127">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="6dcf6-127">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="6dcf6-128">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="6dcf6-128">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="6dcf6-129">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="6dcf6-129">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6dcf6-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="6dcf6-130">Requirements</span></span>



| <span data-ttu-id="6dcf6-131">需求</span><span class="sxs-lookup"><span data-stu-id="6dcf6-131">Requirement</span></span> | <span data-ttu-id="6dcf6-132">值</span><span class="sxs-lookup"><span data-stu-id="6dcf6-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6dcf6-133">標頭</span><span class="sxs-lookup"><span data-stu-id="6dcf6-133">Header</span></span><br/>  | <dl> <span data-ttu-id="6dcf6-134"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="6dcf6-134"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="6dcf6-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="6dcf6-135">Library</span></span><br/> | <dl> <span data-ttu-id="6dcf6-136"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="6dcf6-136"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6dcf6-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6dcf6-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6dcf6-138">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="6dcf6-138">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="6dcf6-139">效果11介面</span><span class="sxs-lookup"><span data-stu-id="6dcf6-139">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="6dcf6-140">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="6dcf6-140">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 






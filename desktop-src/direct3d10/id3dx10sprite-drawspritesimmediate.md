---
description: 繪製 sprite 的陣列。
ms.assetid: 3fcc7705-0d59-450e-b137-c9cb7ec6b1ea
title: 'ID3DX10Sprite：:D rawSpritesImmediate 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.DrawSpritesImmediate
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 7fa4012f5f589c7bc0d1f789599da142194f6e08
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323424"
---
# <a name="id3dx10spritedrawspritesimmediate-method"></a><span data-ttu-id="26530-103">ID3DX10Sprite：:D rawSpritesImmediate 方法</span><span class="sxs-lookup"><span data-stu-id="26530-103">ID3DX10Sprite::DrawSpritesImmediate method</span></span>

<span data-ttu-id="26530-104">繪製 sprite 的陣列。</span><span class="sxs-lookup"><span data-stu-id="26530-104">Draw an array of sprites.</span></span> <span data-ttu-id="26530-105">這會立即將 sprite 傳送至裝置以進行轉譯，這與 ID3DX10Sprite 不同 [**：:D rawspritesbuffered**](id3dx10sprite-drawspritesbuffered.md) ，這會在呼叫 [**ID3DX10Sprite：： Flush**](id3dx10sprite-flush.md) 時，只將 sprite 的陣列新增至要轉譯的一批 sprite。</span><span class="sxs-lookup"><span data-stu-id="26530-105">This will immediately send the sprites to the device for rendering, which is different from [**ID3DX10Sprite::DrawSpritesBuffered**](id3dx10sprite-drawspritesbuffered.md) which only adds an array of sprites to a batch of sprites to be rendered when [**ID3DX10Sprite::Flush**](id3dx10sprite-flush.md) is called.</span></span> <span data-ttu-id="26530-106">此繪製方法最適合用來繪製已在 CPU (上排序的大量 sprite，或不需要) 的排序，例如在物件中。</span><span class="sxs-lookup"><span data-stu-id="26530-106">This draw method is most useful when drawing a large number of sprites that have already been sorted on the CPU (or do not need to be sorted), such as in a particle system.</span></span> <span data-ttu-id="26530-107">必須在呼叫 [**ID3DX10Sprite：： Begin**](id3dx10sprite-begin.md) 和 [**ID3DX10Sprite：： End**](id3dx10sprite-end.md)之間呼叫這項功能。</span><span class="sxs-lookup"><span data-stu-id="26530-107">This must be called in between calls to [**ID3DX10Sprite::Begin**](id3dx10sprite-begin.md) and [**ID3DX10Sprite::End**](id3dx10sprite-end.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="26530-108">語法</span><span class="sxs-lookup"><span data-stu-id="26530-108">Syntax</span></span>


```C++
HRESULT DrawSpritesImmediate(
  [in] D3DX10_SPRITE *pSprites,
  [in] UINT          cSprites,
  [in] UINT          cbSprite,
  [in] UINT          flags
);
```



## <a name="parameters"></a><span data-ttu-id="26530-109">參數</span><span class="sxs-lookup"><span data-stu-id="26530-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26530-110">*pSprites* \[在\]</span><span class="sxs-lookup"><span data-stu-id="26530-110">*pSprites* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26530-111">類型： **[ **D3DX10 \_ SPRITE**](d3dx10-sprite.md)\***</span><span class="sxs-lookup"><span data-stu-id="26530-111">Type: **[**D3DX10\_SPRITE**](d3dx10-sprite.md)\***</span></span>

<span data-ttu-id="26530-112">要繪製之 sprite 的陣列。</span><span class="sxs-lookup"><span data-stu-id="26530-112">The array of sprites to draw.</span></span> <span data-ttu-id="26530-113">請參閱 [**D3DX10 \_ SPRITE**](d3dx10-sprite.md)。</span><span class="sxs-lookup"><span data-stu-id="26530-113">See [**D3DX10\_SPRITE**](d3dx10-sprite.md).</span></span>

</dd> <dt>

<span data-ttu-id="26530-114">*cSprites* \[在\]</span><span class="sxs-lookup"><span data-stu-id="26530-114">*cSprites* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26530-115">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="26530-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="26530-116">PSprites 中的 sprite 數目。</span><span class="sxs-lookup"><span data-stu-id="26530-116">The number of sprites in pSprites.</span></span>

</dd> <dt>

<span data-ttu-id="26530-117">*cbSprite* \[在\]</span><span class="sxs-lookup"><span data-stu-id="26530-117">*cbSprite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26530-118">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="26530-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="26530-119">您要傳遞至 pSprites 之 sprite 結構的大小。</span><span class="sxs-lookup"><span data-stu-id="26530-119">The size of the sprite structure you are passing into pSprites.</span></span> <span data-ttu-id="26530-120">傳入0相當於將 sizeof (D3DX10 \_ SPRITE) 傳入。</span><span class="sxs-lookup"><span data-stu-id="26530-120">Passing in 0 is the equivalent of passing in sizeof(D3DX10\_SPRITE).</span></span>

</dd> <dt>

<span data-ttu-id="26530-121">*旗標* \[在\]</span><span class="sxs-lookup"><span data-stu-id="26530-121">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26530-122">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="26530-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="26530-123">保留的。</span><span class="sxs-lookup"><span data-stu-id="26530-123">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26530-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="26530-124">Return value</span></span>

<span data-ttu-id="26530-125">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="26530-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="26530-126">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="26530-126">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="26530-127">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，D3DXERR \_ INVALIDDATA。</span><span class="sxs-lookup"><span data-stu-id="26530-127">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="26530-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="26530-128">Requirements</span></span>



| <span data-ttu-id="26530-129">需求</span><span class="sxs-lookup"><span data-stu-id="26530-129">Requirement</span></span> | <span data-ttu-id="26530-130">值</span><span class="sxs-lookup"><span data-stu-id="26530-130">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="26530-131">標頭</span><span class="sxs-lookup"><span data-stu-id="26530-131">Header</span></span><br/>  | <dl> <span data-ttu-id="26530-132"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="26530-132"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="26530-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="26530-133">Library</span></span><br/> | <dl> <span data-ttu-id="26530-134"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="26530-134"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26530-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="26530-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26530-136">ID3DX10Sprite</span><span class="sxs-lookup"><span data-stu-id="26530-136">ID3DX10Sprite</span></span>](id3dx10sprite.md)
</dt> <dt>

[<span data-ttu-id="26530-137">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="26530-137">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 

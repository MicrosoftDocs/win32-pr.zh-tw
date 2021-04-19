---
description: 將 sprite 的陣列新增至要轉譯的 sprite 批次。
ms.assetid: e6a9f806-7244-4139-b47e-c46dfab38a31
title: 'ID3DX10Sprite：:D rawSpritesBuffered 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.DrawSpritesBuffered
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 72893f6a8c3cf82c67f014b4bdbb9a92453de319
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106975717"
---
# <a name="id3dx10spritedrawspritesbuffered-method"></a><span data-ttu-id="398f6-103">ID3DX10Sprite：:D rawSpritesBuffered 方法</span><span class="sxs-lookup"><span data-stu-id="398f6-103">ID3DX10Sprite::DrawSpritesBuffered method</span></span>

<span data-ttu-id="398f6-104">將 sprite 的陣列新增至要轉譯的 sprite 批次。</span><span class="sxs-lookup"><span data-stu-id="398f6-104">Add an array of sprites to the batch of sprites to be rendered.</span></span> <span data-ttu-id="398f6-105">您必須在呼叫 [**ID3DX10Sprite：： Begin**](id3dx10sprite-begin.md) 和 [**ID3DX10Sprite：： end**](id3dx10sprite-end.md)之間呼叫這一點，而且必須在結束之前呼叫 [**ID3DX10Sprite：： Flush**](id3dx10sprite-flush.md) ，才能將所有批次內建的子內容傳送到裝置以進行轉譯。</span><span class="sxs-lookup"><span data-stu-id="398f6-105">This must be called in between calls to [**ID3DX10Sprite::Begin**](id3dx10sprite-begin.md) and [**ID3DX10Sprite::End**](id3dx10sprite-end.md), and [**ID3DX10Sprite::Flush**](id3dx10sprite-flush.md) must be called before End to send all of the batched sprites to the device for rendering.</span></span> <span data-ttu-id="398f6-106">這種繪製方法最適合用來繪製少量的 sprite，而您想要將它緩衝至大型批次，例如字型。</span><span class="sxs-lookup"><span data-stu-id="398f6-106">This draw method is most useful when drawing a small number of sprites that you want buffered into a large batch, such as fonts.</span></span>

## <a name="syntax"></a><span data-ttu-id="398f6-107">語法</span><span class="sxs-lookup"><span data-stu-id="398f6-107">Syntax</span></span>


```C++
HRESULT DrawSpritesBuffered(
  [in] D3DX10_SPRITE *pSprites,
  [in] UINT          cSprites
);
```



## <a name="parameters"></a><span data-ttu-id="398f6-108">參數</span><span class="sxs-lookup"><span data-stu-id="398f6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="398f6-109">*pSprites* \[在\]</span><span class="sxs-lookup"><span data-stu-id="398f6-109">*pSprites* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="398f6-110">類型： **[ **D3DX10 \_ SPRITE**](d3dx10-sprite.md)\***</span><span class="sxs-lookup"><span data-stu-id="398f6-110">Type: **[**D3DX10\_SPRITE**](d3dx10-sprite.md)\***</span></span>

<span data-ttu-id="398f6-111">要繪製之 sprite 的陣列。</span><span class="sxs-lookup"><span data-stu-id="398f6-111">The array of sprites to draw.</span></span> <span data-ttu-id="398f6-112">請參閱 [**D3DX10 \_ SPRITE**](d3dx10-sprite.md)。</span><span class="sxs-lookup"><span data-stu-id="398f6-112">See [**D3DX10\_SPRITE**](d3dx10-sprite.md).</span></span>

</dd> <dt>

<span data-ttu-id="398f6-113">*cSprites* \[在\]</span><span class="sxs-lookup"><span data-stu-id="398f6-113">*cSprites* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="398f6-114">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="398f6-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="398f6-115">PSprites 中的 sprite 數目。</span><span class="sxs-lookup"><span data-stu-id="398f6-115">The number of sprites in pSprites.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="398f6-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="398f6-116">Return value</span></span>

<span data-ttu-id="398f6-117">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="398f6-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="398f6-118">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="398f6-118">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="398f6-119">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，D3DXERR \_ INVALIDDATA。</span><span class="sxs-lookup"><span data-stu-id="398f6-119">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="398f6-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="398f6-120">Requirements</span></span>



| <span data-ttu-id="398f6-121">需求</span><span class="sxs-lookup"><span data-stu-id="398f6-121">Requirement</span></span> | <span data-ttu-id="398f6-122">值</span><span class="sxs-lookup"><span data-stu-id="398f6-122">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="398f6-123">標頭</span><span class="sxs-lookup"><span data-stu-id="398f6-123">Header</span></span><br/>  | <dl> <span data-ttu-id="398f6-124"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="398f6-124"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="398f6-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="398f6-125">Library</span></span><br/> | <dl> <span data-ttu-id="398f6-126"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="398f6-126"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="398f6-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="398f6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="398f6-128">ID3DX10Sprite</span><span class="sxs-lookup"><span data-stu-id="398f6-128">ID3DX10Sprite</span></span>](id3dx10sprite.md)
</dt> <dt>

[<span data-ttu-id="398f6-129">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="398f6-129">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 

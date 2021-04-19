---
description: 建立用來繪製2D 材質的 sprite。請注意，我們建議您不要使用這個函式，而是使用 Direct2D 和 DirectXTK library SpriteBatch 類別。
ms.assetid: 64efb8e4-da0b-4e67-874a-e0bb0083961c
title: 'D3DX10CreateSprite 函式 (D3DX10) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateSprite
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: cf40e303cb616f35ea5cd3526c263e3bd12ae428
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106999003"
---
# <a name="d3dx10createsprite-function"></a><span data-ttu-id="c8577-103">D3DX10CreateSprite 函式</span><span class="sxs-lookup"><span data-stu-id="c8577-103">D3DX10CreateSprite function</span></span>

<span data-ttu-id="c8577-104">建立用來繪製2D 材質的 sprite。</span><span class="sxs-lookup"><span data-stu-id="c8577-104">Create a sprite for drawing a 2D texture.</span></span>

> [!Note]  
> <span data-ttu-id="c8577-105">我們建議您不要使用這個函式，而是使用 [Direct2D](../direct2d/direct2d-portal.md) 和 [DirectXTK](https://github.com/Microsoft/DirectXTK) 程式庫 **SpriteBatch** 類別。</span><span class="sxs-lookup"><span data-stu-id="c8577-105">Instead of using this function, we recommend that you use [Direct2D](../direct2d/direct2d-portal.md) and the [DirectXTK](https://github.com/Microsoft/DirectXTK) library, **SpriteBatch** class.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="c8577-106">語法</span><span class="sxs-lookup"><span data-stu-id="c8577-106">Syntax</span></span>


```C++
HRESULT D3DX10CreateSprite(
  _In_  ID3D10Device   *pDevice,
  _In_  UINT           cDeviceBufferSize,
  _Out_ LPD3DX10SPRITE *ppSprite
);
```



## <a name="parameters"></a><span data-ttu-id="c8577-107">參數</span><span class="sxs-lookup"><span data-stu-id="c8577-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8577-108">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c8577-108">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8577-109">類型： **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="c8577-109">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="c8577-110">裝置的指標 (查看將繪製 sprite 的 [**ID3D10Device 介面**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) 。</span><span class="sxs-lookup"><span data-stu-id="c8577-110">A pointer to the device (see [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) that will draw the sprite.</span></span>

</dd> <dt>

<span data-ttu-id="c8577-111">*cDeviceBufferSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c8577-111">*cDeviceBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8577-112">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c8577-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c8577-113">當呼叫 [**ID3DX10Sprite：： Flush**](id3dx10sprite-flush.md) 或 [**ID3DX10Sprite：:D rawspritesimmediate**](id3dx10sprite-drawspritesimmediate.md) 時，將會傳送至裝置的頂點緩衝區大小（以 sprite 數為限）。</span><span class="sxs-lookup"><span data-stu-id="c8577-113">The size of the vertex buffer, in number of sprites, that will be sent to the device when [**ID3DX10Sprite::Flush**](id3dx10sprite-flush.md) or [**ID3DX10Sprite::DrawSpritesImmediate**](id3dx10sprite-drawspritesimmediate.md) is called.</span></span> <span data-ttu-id="c8577-114">如果您知道將會一次轉譯少量的 sprite (儲存記憶體) ，而如果您知道將會一次轉譯大量的 sprite，則這應該是很小的數位。</span><span class="sxs-lookup"><span data-stu-id="c8577-114">This should be a small number if you know you will be rendering a small number of sprites at a time (to save memory) and a large number if you know you will be rendering a large number of sprites at a time.</span></span> <span data-ttu-id="c8577-115">最大值為4096。</span><span class="sxs-lookup"><span data-stu-id="c8577-115">The maximum value is 4096.</span></span> <span data-ttu-id="c8577-116">如果指定0，則會自動將頂點緩衝區大小設定為4096。</span><span class="sxs-lookup"><span data-stu-id="c8577-116">If 0 is specified, the vertex buffer size will automatically be set to 4096.</span></span>

</dd> <dt>

<span data-ttu-id="c8577-117">*ppSprite* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c8577-117">*ppSprite* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c8577-118">類型： **[ **LPD3DX10SPRITE**](id3dx10sprite.md)\***</span><span class="sxs-lookup"><span data-stu-id="c8577-118">Type: **[**LPD3DX10SPRITE**](id3dx10sprite.md)\***</span></span>

<span data-ttu-id="c8577-119">Sprite 介面之指標的位址 (參閱 [**ID3DX10Sprite 介面**](id3dx10sprite.md)) 。</span><span class="sxs-lookup"><span data-stu-id="c8577-119">The address of a pointer to a sprite interface (see [**ID3DX10Sprite Interface**](id3dx10sprite.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8577-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="c8577-120">Return value</span></span>

<span data-ttu-id="c8577-121">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c8577-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c8577-122">如果函式成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="c8577-122">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="c8577-123">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="c8577-123">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8577-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="c8577-124">Requirements</span></span>



| <span data-ttu-id="c8577-125">需求</span><span class="sxs-lookup"><span data-stu-id="c8577-125">Requirement</span></span> | <span data-ttu-id="c8577-126">值</span><span class="sxs-lookup"><span data-stu-id="c8577-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c8577-127">標頭</span><span class="sxs-lookup"><span data-stu-id="c8577-127">Header</span></span><br/>  | <dl> <span data-ttu-id="c8577-128"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="c8577-128"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="c8577-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="c8577-129">Library</span></span><br/> | <dl> <span data-ttu-id="c8577-130"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c8577-130"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8577-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c8577-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8577-132">一般用途函數</span><span class="sxs-lookup"><span data-stu-id="c8577-132">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 

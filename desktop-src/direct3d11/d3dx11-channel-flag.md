---
title: 'D3DX11_CHANNEL_FLAG 列舉 (D3DX11tex .h) '
description: 請注意，D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 這些旗標會由函式使用，這些函式會在材質中的一或多個通道上運作。
ms.assetid: 058a0a1e-3c1b-4397-a41a-2e47d878cd92
keywords:
- D3DX11_CHANNEL_FLAG 列舉 Direct3D 11
- LPD3DX11_CHANNEL_FLAG 列舉指標 Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_CHANNEL_FLAG
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2e3097552637ce96663671dda443684ebda2b65
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104386522"
---
# <a name="d3dx11_channel_flag-enumeration"></a><span data-ttu-id="70ddf-106">D3DX11 \_ 通道 \_ 旗標列舉</span><span class="sxs-lookup"><span data-stu-id="70ddf-106">D3DX11\_CHANNEL\_FLAG enumeration</span></span>

> [!Note]  
> <span data-ttu-id="70ddf-107">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="70ddf-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="70ddf-108">這些旗標會由函式使用，這些函式會在材質中的一或多個通道上運作。</span><span class="sxs-lookup"><span data-stu-id="70ddf-108">These flags are used by functions which operate on one or more channels in a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="70ddf-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="70ddf-109">Syntax</span></span>


```C++
typedef enum D3DX11_CHANNEL_FLAG { 
  D3DX11_CHANNEL_RED        = (1 << 0),
  D3DX11_CHANNEL_BLUE       = (1 << 1),
  D3DX11_CHANNEL_GREEN      = (1 << 2),
  D3DX11_CHANNEL_ALPHA      = (1 << 3),
  D3DX11_CHANNEL_LUMINANCE  = (1 << 4)
} D3DX11_CHANNEL_FLAG, *LPD3DX11_CHANNEL_FLAG;
```



## <a name="constants"></a><span data-ttu-id="70ddf-110">常數</span><span class="sxs-lookup"><span data-stu-id="70ddf-110">Constants</span></span>

<dl> <dt>

<span data-ttu-id="70ddf-111"><span id="D3DX11_CHANNEL_RED"></span><span id="d3dx11_channel_red"></span>**D3DX11 \_ 頻道 \_ 紅色**</span><span class="sxs-lookup"><span data-stu-id="70ddf-111"><span id="D3DX11_CHANNEL_RED"></span><span id="d3dx11_channel_red"></span>**D3DX11\_CHANNEL\_RED**</span></span>
</dt> <dd>

<span data-ttu-id="70ddf-112">表示應該使用紅色通道。</span><span class="sxs-lookup"><span data-stu-id="70ddf-112">Indicates the red channel should be used.</span></span>

</dd> <dt>

<span data-ttu-id="70ddf-113"><span id="D3DX11_CHANNEL_BLUE"></span><span id="d3dx11_channel_blue"></span>**D3DX11 \_ CHANNEL \_ BLUE**</span><span class="sxs-lookup"><span data-stu-id="70ddf-113"><span id="D3DX11_CHANNEL_BLUE"></span><span id="d3dx11_channel_blue"></span>**D3DX11\_CHANNEL\_BLUE**</span></span>
</dt> <dd>

<span data-ttu-id="70ddf-114">表示應該使用藍色通道。</span><span class="sxs-lookup"><span data-stu-id="70ddf-114">Indicates the blue channel should be used.</span></span>

</dd> <dt>

<span data-ttu-id="70ddf-115"><span id="D3DX11_CHANNEL_GREEN"></span><span id="d3dx11_channel_green"></span>**D3DX11 \_ CHANNEL \_ 綠**</span><span class="sxs-lookup"><span data-stu-id="70ddf-115"><span id="D3DX11_CHANNEL_GREEN"></span><span id="d3dx11_channel_green"></span>**D3DX11\_CHANNEL\_GREEN**</span></span>
</dt> <dd>

<span data-ttu-id="70ddf-116">表示應該使用綠色通道。</span><span class="sxs-lookup"><span data-stu-id="70ddf-116">Indicates the green channel should be used.</span></span>

</dd> <dt>

<span data-ttu-id="70ddf-117"><span id="D3DX11_CHANNEL_ALPHA"></span><span id="d3dx11_channel_alpha"></span>**D3DX11 \_ 頻道 \_ ALPHA**</span><span class="sxs-lookup"><span data-stu-id="70ddf-117"><span id="D3DX11_CHANNEL_ALPHA"></span><span id="d3dx11_channel_alpha"></span>**D3DX11\_CHANNEL\_ALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="70ddf-118">表示應該使用 Alpha 色板。</span><span class="sxs-lookup"><span data-stu-id="70ddf-118">Indicates the alpha channel should be used.</span></span>

</dd> <dt>

<span data-ttu-id="70ddf-119"><span id="D3DX11_CHANNEL_LUMINANCE"></span><span id="d3dx11_channel_luminance"></span>**D3DX11 \_ 通道 \_ 亮度**</span><span class="sxs-lookup"><span data-stu-id="70ddf-119"><span id="D3DX11_CHANNEL_LUMINANCE"></span><span id="d3dx11_channel_luminance"></span>**D3DX11\_CHANNEL\_LUMINANCE**</span></span>
</dt> <dd>

<span data-ttu-id="70ddf-120">指出應該使用紅色、綠色和藍色通道的 luminaces。</span><span class="sxs-lookup"><span data-stu-id="70ddf-120">Indicates the luminaces of the red, green, and blue channels should be used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="70ddf-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="70ddf-121">Requirements</span></span>



| <span data-ttu-id="70ddf-122">需求</span><span class="sxs-lookup"><span data-stu-id="70ddf-122">Requirement</span></span> | <span data-ttu-id="70ddf-123">值</span><span class="sxs-lookup"><span data-stu-id="70ddf-123">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="70ddf-124">標頭</span><span class="sxs-lookup"><span data-stu-id="70ddf-124">Header</span></span><br/> | <dl> <span data-ttu-id="70ddf-125"><dt>D3DX11tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="70ddf-125"><dt>D3DX11tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70ddf-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="70ddf-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70ddf-127">D3DX 列舉</span><span class="sxs-lookup"><span data-stu-id="70ddf-127">D3DX Enumerations</span></span>](d3d11-graphics-reference-d3dx11-enums.md)
</dt> </dl>

 

 






---
description: 這些旗標會由函式使用，這些函式會在材質中的一或多個通道上運作。
ms.assetid: 54ecb39a-a36e-43bb-bb51-78b7375716d8
title: 'D3DX10_CHANNEL_FLAG 列舉 (D3DX10Tex .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_CHANNEL_FLAG
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: f21958ab964a70116a551c0cb8dadbce6db88f7d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323231"
---
# <a name="d3dx10_channel_flag-enumeration"></a><span data-ttu-id="cb82c-103">D3DX10 \_ 通道 \_ 旗標列舉</span><span class="sxs-lookup"><span data-stu-id="cb82c-103">D3DX10\_CHANNEL\_FLAG enumeration</span></span>

<span data-ttu-id="cb82c-104">這些旗標會由函式使用，這些函式會在材質中的一或多個通道上運作。</span><span class="sxs-lookup"><span data-stu-id="cb82c-104">These flags are used by functions which operate on one or more channels in a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb82c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cb82c-105">Syntax</span></span>


```C++
typedef enum D3DX10_CHANNEL_FLAG { 
  D3DX10_CHANNEL_RED        = (1 << 0),
  D3DX10_CHANNEL_BLUE       = (1 << 1),
  D3DX10_CHANNEL_GREEN      = (1 << 2),
  D3DX10_CHANNEL_ALPHA      = (1 << 3),
  D3DX10_CHANNEL_LUMINANCE  = (1 << 4)
} D3DX10_CHANNEL_FLAG, *LPD3DX10_CHANNEL_FLAG;
```



## <a name="constants"></a><span data-ttu-id="cb82c-106">常數</span><span class="sxs-lookup"><span data-stu-id="cb82c-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="cb82c-107"><span id="D3DX10_CHANNEL_RED"></span><span id="d3dx10_channel_red"></span>**D3DX10 \_ 頻道 \_ 紅色**</span><span class="sxs-lookup"><span data-stu-id="cb82c-107"><span id="D3DX10_CHANNEL_RED"></span><span id="d3dx10_channel_red"></span>**D3DX10\_CHANNEL\_RED**</span></span>
</dt> <dd>

<span data-ttu-id="cb82c-108">表示應該使用紅色通道。</span><span class="sxs-lookup"><span data-stu-id="cb82c-108">Indicates the red channel should be used.</span></span>

</dd> <dt>

<span data-ttu-id="cb82c-109"><span id="D3DX10_CHANNEL_BLUE"></span><span id="d3dx10_channel_blue"></span>**D3DX10 \_ CHANNEL \_ BLUE**</span><span class="sxs-lookup"><span data-stu-id="cb82c-109"><span id="D3DX10_CHANNEL_BLUE"></span><span id="d3dx10_channel_blue"></span>**D3DX10\_CHANNEL\_BLUE**</span></span>
</dt> <dd>

<span data-ttu-id="cb82c-110">表示應該使用藍色通道。</span><span class="sxs-lookup"><span data-stu-id="cb82c-110">Indicates the blue channel should be used.</span></span>

</dd> <dt>

<span data-ttu-id="cb82c-111"><span id="D3DX10_CHANNEL_GREEN"></span><span id="d3dx10_channel_green"></span>**D3DX10 \_ CHANNEL \_ 綠**</span><span class="sxs-lookup"><span data-stu-id="cb82c-111"><span id="D3DX10_CHANNEL_GREEN"></span><span id="d3dx10_channel_green"></span>**D3DX10\_CHANNEL\_GREEN**</span></span>
</dt> <dd>

<span data-ttu-id="cb82c-112">表示應該使用綠色通道。</span><span class="sxs-lookup"><span data-stu-id="cb82c-112">Indicates the green channel should be used.</span></span>

</dd> <dt>

<span data-ttu-id="cb82c-113"><span id="D3DX10_CHANNEL_ALPHA"></span><span id="d3dx10_channel_alpha"></span>**D3DX10 \_ 頻道 \_ ALPHA**</span><span class="sxs-lookup"><span data-stu-id="cb82c-113"><span id="D3DX10_CHANNEL_ALPHA"></span><span id="d3dx10_channel_alpha"></span>**D3DX10\_CHANNEL\_ALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="cb82c-114">表示應該使用 Alpha 色板。</span><span class="sxs-lookup"><span data-stu-id="cb82c-114">Indicates the alpha channel should be used.</span></span>

</dd> <dt>

<span data-ttu-id="cb82c-115"><span id="D3DX10_CHANNEL_LUMINANCE"></span><span id="d3dx10_channel_luminance"></span>**D3DX10 \_ 通道 \_ 亮度**</span><span class="sxs-lookup"><span data-stu-id="cb82c-115"><span id="D3DX10_CHANNEL_LUMINANCE"></span><span id="d3dx10_channel_luminance"></span>**D3DX10\_CHANNEL\_LUMINANCE**</span></span>
</dt> <dd>

<span data-ttu-id="cb82c-116">指出應該使用紅色、綠色和藍色通道的 luminaces。</span><span class="sxs-lookup"><span data-stu-id="cb82c-116">Indicates the luminaces of the red, green, and blue channels should be used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cb82c-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="cb82c-117">Requirements</span></span>



| <span data-ttu-id="cb82c-118">需求</span><span class="sxs-lookup"><span data-stu-id="cb82c-118">Requirement</span></span> | <span data-ttu-id="cb82c-119">值</span><span class="sxs-lookup"><span data-stu-id="cb82c-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cb82c-120">標頭</span><span class="sxs-lookup"><span data-stu-id="cb82c-120">Header</span></span><br/> | <dl> <span data-ttu-id="cb82c-121"><dt>D3DX10Tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="cb82c-121"><dt>D3DX10Tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb82c-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cb82c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb82c-123">D3DX 列舉</span><span class="sxs-lookup"><span data-stu-id="cb82c-123">D3DX Enumerations</span></span>](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 





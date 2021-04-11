---
description: 定義用於播放的動畫組迴圈模式類型。
ms.assetid: 2ce26bf0-2b33-4193-a58f-03493a051351
title: 'D3DXPLAYBACK_TYPE 列舉 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPLAYBACK_TYPE
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 0ce95b4765ec678c43c8e0ed92008deeb9927298
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103853983"
---
# <a name="d3dxplayback_type-enumeration"></a><span data-ttu-id="48e2b-103">D3DXPLAYBACK \_ 類型列舉</span><span class="sxs-lookup"><span data-stu-id="48e2b-103">D3DXPLAYBACK\_TYPE enumeration</span></span>

<span data-ttu-id="48e2b-104">定義用於播放的動畫組迴圈模式類型。</span><span class="sxs-lookup"><span data-stu-id="48e2b-104">Defines the type of animation set looping modes used for playback.</span></span>

## <a name="syntax"></a><span data-ttu-id="48e2b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="48e2b-105">Syntax</span></span>


```C++
typedef enum D3DXPLAYBACK_TYPE { 
  D3DXPLAY_LOOP         = 0,
  D3DXPLAY_ONCE         = 1,
  D3DXPLAY_PINGPONG     = 2,
  D3DXPLAY_FORCE_DWORD  = 0x7fffffff
} D3DXPLAYBACK_TYPE, *LPD3DXPLAYBACK_TYPE;
```



## <a name="constants"></a><span data-ttu-id="48e2b-106">常數</span><span class="sxs-lookup"><span data-stu-id="48e2b-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="48e2b-107"><span id="D3DXPLAY_LOOP"></span><span id="d3dxplay_loop"></span>**D3DXPLAY \_ 迴圈**</span><span class="sxs-lookup"><span data-stu-id="48e2b-107"><span id="D3DXPLAY_LOOP"></span><span id="d3dxplay_loop"></span>**D3DXPLAY\_LOOP**</span></span>
</dt> <dd>

<span data-ttu-id="48e2b-108">動畫會無限重複。</span><span class="sxs-lookup"><span data-stu-id="48e2b-108">The animation repeats endlessly.</span></span>

</dd> <dt>

<span data-ttu-id="48e2b-109"><span id="D3DXPLAY_ONCE"></span><span id="d3dxplay_once"></span>**D3DXPLAY \_ 一次**</span><span class="sxs-lookup"><span data-stu-id="48e2b-109"><span id="D3DXPLAY_ONCE"></span><span id="d3dxplay_once"></span>**D3DXPLAY\_ONCE**</span></span>
</dt> <dd>

<span data-ttu-id="48e2b-110">動畫會播放一次，然後在最後一個畫面上停止。</span><span class="sxs-lookup"><span data-stu-id="48e2b-110">The animation plays once, and then it stops on the last frame.</span></span>

</dd> <dt>

<span data-ttu-id="48e2b-111"><span id="D3DXPLAY_PINGPONG"></span><span id="d3dxplay_pingpong"></span>**D3DXPLAY \_ PINGPONG**</span><span class="sxs-lookup"><span data-stu-id="48e2b-111"><span id="D3DXPLAY_PINGPONG"></span><span id="d3dxplay_pingpong"></span>**D3DXPLAY\_PINGPONG**</span></span>
</dt> <dd>

<span data-ttu-id="48e2b-112">動畫會在向前播放和回溯播放之間無休止的改變。</span><span class="sxs-lookup"><span data-stu-id="48e2b-112">The animation alternates endlessly between playing forward and playing backward.</span></span>

</dd> <dt>

<span data-ttu-id="48e2b-113"><span id="D3DXPLAY_FORCE_DWORD"></span><span id="d3dxplay_force_dword"></span>**D3DXPLAY \_ 強制 \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="48e2b-113"><span id="D3DXPLAY_FORCE_DWORD"></span><span id="d3dxplay_force_dword"></span>**D3DXPLAY\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="48e2b-114">強制此列舉的大小編譯為32位。</span><span class="sxs-lookup"><span data-stu-id="48e2b-114">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="48e2b-115">如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。</span><span class="sxs-lookup"><span data-stu-id="48e2b-115">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="48e2b-116">不使用這個值。</span><span class="sxs-lookup"><span data-stu-id="48e2b-116">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="48e2b-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="48e2b-117">Requirements</span></span>



| <span data-ttu-id="48e2b-118">需求</span><span class="sxs-lookup"><span data-stu-id="48e2b-118">Requirement</span></span> | <span data-ttu-id="48e2b-119">值</span><span class="sxs-lookup"><span data-stu-id="48e2b-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="48e2b-120">標頭</span><span class="sxs-lookup"><span data-stu-id="48e2b-120">Header</span></span><br/> | <dl> <span data-ttu-id="48e2b-121"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="48e2b-121"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48e2b-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="48e2b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48e2b-123">D3DX 列舉</span><span class="sxs-lookup"><span data-stu-id="48e2b-123">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 





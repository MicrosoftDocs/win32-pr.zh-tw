---
title: endloop-ps
description: 迴圈結束-ps .。。endloop 組塊。
ms.assetid: 8d05d0b3-88d2-44e3-a22d-54d8a8ceb5f4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ee1a7eb10146e40a39c05bcecb99d3a7667dee2c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "103932811"
---
# <a name="endloop---ps"></a><span data-ttu-id="2f384-103">endloop-ps</span><span class="sxs-lookup"><span data-stu-id="2f384-103">endloop - ps</span></span>

<span data-ttu-id="2f384-104">[迴圈結束-ps](loop---ps.md).。。endloop 組塊。</span><span class="sxs-lookup"><span data-stu-id="2f384-104">End of a [loop - ps](loop---ps.md)...endloop block.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f384-105">備註</span><span class="sxs-lookup"><span data-stu-id="2f384-105">Remarks</span></span>



| <span data-ttu-id="2f384-106">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="2f384-106">Pixel shader versions</span></span> | <span data-ttu-id="2f384-107">1\_1</span><span class="sxs-lookup"><span data-stu-id="2f384-107">1\_1</span></span> | <span data-ttu-id="2f384-108">1\_2</span><span class="sxs-lookup"><span data-stu-id="2f384-108">1\_2</span></span> | <span data-ttu-id="2f384-109">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="2f384-109">1\_3</span></span> | <span data-ttu-id="2f384-110">1\_4</span><span class="sxs-lookup"><span data-stu-id="2f384-110">1\_4</span></span> | <span data-ttu-id="2f384-111">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2f384-111">2\_0</span></span> | <span data-ttu-id="2f384-112">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="2f384-112">2\_x</span></span> | <span data-ttu-id="2f384-113">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="2f384-113">2\_sw</span></span> | <span data-ttu-id="2f384-114">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2f384-114">3\_0</span></span> | <span data-ttu-id="2f384-115">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="2f384-115">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="2f384-116">endloop</span><span class="sxs-lookup"><span data-stu-id="2f384-116">endloop</span></span>               |      |      |      |      |      |      |       | <span data-ttu-id="2f384-117">x</span><span class="sxs-lookup"><span data-stu-id="2f384-117">x</span></span>    | <span data-ttu-id="2f384-118">x</span><span class="sxs-lookup"><span data-stu-id="2f384-118">x</span></span>     |



 

<span data-ttu-id="2f384-119">endloop 必須遵循 [迴圈 ps](loop---ps.md) 區塊的最後一個指令。</span><span class="sxs-lookup"><span data-stu-id="2f384-119">endloop must follow the last instruction of a [loop - ps](loop---ps.md) block.</span></span>

## <a name="example"></a><span data-ttu-id="2f384-120">範例</span><span class="sxs-lookup"><span data-stu-id="2f384-120">Example</span></span>


```
loop aL, i3
    add r1, r0, c2[ aL ]
endloop
```



## <a name="related-topics"></a><span data-ttu-id="2f384-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="2f384-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f384-122">圖元著色器指示</span><span class="sxs-lookup"><span data-stu-id="2f384-122">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 





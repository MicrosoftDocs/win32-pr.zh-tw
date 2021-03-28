---
title: endloop-vs
description: 迴圈結束 .。。endloop 組塊。
ms.assetid: fd7df120-a927-4a66-b152-6ce5247446e4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8a9aec4d1b2c5237a87fae2c0beab4e8d995db97
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104373691"
---
# <a name="endloop---vs"></a><span data-ttu-id="40dce-103">endloop-vs</span><span class="sxs-lookup"><span data-stu-id="40dce-103">endloop - vs</span></span>

<span data-ttu-id="40dce-104">[迴圈](loop---vs.md)結束 .。。endloop 組塊。</span><span class="sxs-lookup"><span data-stu-id="40dce-104">End of a [loop](loop---vs.md)...endloop block.</span></span>

## <a name="syntax"></a><span data-ttu-id="40dce-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="40dce-105">Syntax</span></span>



| <span data-ttu-id="40dce-106">endloop</span><span class="sxs-lookup"><span data-stu-id="40dce-106">endloop</span></span> |
|---------|



 

## <a name="remarks"></a><span data-ttu-id="40dce-107">備註</span><span class="sxs-lookup"><span data-stu-id="40dce-107">Remarks</span></span>



| <span data-ttu-id="40dce-108">頂點著色器版本</span><span class="sxs-lookup"><span data-stu-id="40dce-108">Vertex shader versions</span></span> | <span data-ttu-id="40dce-109">1\_1</span><span class="sxs-lookup"><span data-stu-id="40dce-109">1\_1</span></span> | <span data-ttu-id="40dce-110">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="40dce-110">2\_0</span></span> | <span data-ttu-id="40dce-111">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="40dce-111">2\_x</span></span> | <span data-ttu-id="40dce-112">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="40dce-112">2\_sw</span></span> | <span data-ttu-id="40dce-113">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="40dce-113">3\_0</span></span> | <span data-ttu-id="40dce-114">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="40dce-114">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="40dce-115">endloop</span><span class="sxs-lookup"><span data-stu-id="40dce-115">endloop</span></span>                |      | <span data-ttu-id="40dce-116">x</span><span class="sxs-lookup"><span data-stu-id="40dce-116">x</span></span>    | <span data-ttu-id="40dce-117">x</span><span class="sxs-lookup"><span data-stu-id="40dce-117">x</span></span>    | <span data-ttu-id="40dce-118">x</span><span class="sxs-lookup"><span data-stu-id="40dce-118">x</span></span>     | <span data-ttu-id="40dce-119">x</span><span class="sxs-lookup"><span data-stu-id="40dce-119">x</span></span>    | <span data-ttu-id="40dce-120">x</span><span class="sxs-lookup"><span data-stu-id="40dce-120">x</span></span>     |



 

<span data-ttu-id="40dce-121">此指示的運作方式如下所示。</span><span class="sxs-lookup"><span data-stu-id="40dce-121">This instruction works as shown here.</span></span>


```
LoopCounter += LoopStep;
LoopInterationCount = LoopIterationCount - 1;
if (LoopIterationCount > 0)
    Continue execution at the StartLoopOffset
```



<span data-ttu-id="40dce-122">endloop 必須遵循 [迴圈-vs](loop---vs.md) 區塊的最後一個指令。</span><span class="sxs-lookup"><span data-stu-id="40dce-122">endloop must follow the last instruction of a [loop - vs](loop---vs.md) block.</span></span>

## <a name="example"></a><span data-ttu-id="40dce-123">範例</span><span class="sxs-lookup"><span data-stu-id="40dce-123">Example</span></span>


```
loop aL, i3
    add r1, r0, c2[ aL ]
endloop
```



## <a name="related-topics"></a><span data-ttu-id="40dce-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="40dce-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40dce-125">頂點著色器指示</span><span class="sxs-lookup"><span data-stu-id="40dce-125">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 





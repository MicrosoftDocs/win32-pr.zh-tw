---
title: 亮-vs
description: 藉由計算兩個點乘積的光源係數和指數來提供光源的部分支援。
ms.assetid: e0ed1a75-6682-4d05-b0e5-dc65e201de98
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 99c25c377ff6064a704d56b9e7b31d41b37117e5
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104971569"
---
# <a name="lit---vs"></a><span data-ttu-id="6a746-103">亮-vs</span><span class="sxs-lookup"><span data-stu-id="6a746-103">lit - vs</span></span>

<span data-ttu-id="6a746-104">藉由計算兩個點乘積的光源係數和指數來提供光源的部分支援。</span><span class="sxs-lookup"><span data-stu-id="6a746-104">Provides partial support for lighting by calculating lighting coefficients from two dot products and an exponent.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a746-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6a746-105">Syntax</span></span>



| <span data-ttu-id="6a746-106">亮 dst、src</span><span class="sxs-lookup"><span data-stu-id="6a746-106">lit dst, src</span></span> |
|--------------|



 

<span data-ttu-id="6a746-107">其中</span><span class="sxs-lookup"><span data-stu-id="6a746-107">where</span></span>

-   <span data-ttu-id="6a746-108">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="6a746-108">dst is the destination register.</span></span>
-   <span data-ttu-id="6a746-109">src 是來源暫存器。</span><span class="sxs-lookup"><span data-stu-id="6a746-109">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a746-110">備註</span><span class="sxs-lookup"><span data-stu-id="6a746-110">Remarks</span></span>



| <span data-ttu-id="6a746-111">頂點著色器版本</span><span class="sxs-lookup"><span data-stu-id="6a746-111">Vertex shader versions</span></span> | <span data-ttu-id="6a746-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="6a746-112">1\_1</span></span> | <span data-ttu-id="6a746-113">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6a746-113">2\_0</span></span> | <span data-ttu-id="6a746-114">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="6a746-114">2\_x</span></span> | <span data-ttu-id="6a746-115">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="6a746-115">2\_sw</span></span> | <span data-ttu-id="6a746-116">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6a746-116">3\_0</span></span> | <span data-ttu-id="6a746-117">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="6a746-117">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="6a746-118">點燃</span><span class="sxs-lookup"><span data-stu-id="6a746-118">lit</span></span>                    | <span data-ttu-id="6a746-119">x</span><span class="sxs-lookup"><span data-stu-id="6a746-119">x</span></span>    | <span data-ttu-id="6a746-120">x</span><span class="sxs-lookup"><span data-stu-id="6a746-120">x</span></span>    | <span data-ttu-id="6a746-121">x</span><span class="sxs-lookup"><span data-stu-id="6a746-121">x</span></span>    | <span data-ttu-id="6a746-122">x</span><span class="sxs-lookup"><span data-stu-id="6a746-122">x</span></span>     | <span data-ttu-id="6a746-123">x</span><span class="sxs-lookup"><span data-stu-id="6a746-123">x</span></span>    | <span data-ttu-id="6a746-124">x</span><span class="sxs-lookup"><span data-stu-id="6a746-124">x</span></span>     |



 

<span data-ttu-id="6a746-125">假設來源向量包含下列虛擬程式碼中所示的值。</span><span class="sxs-lookup"><span data-stu-id="6a746-125">The source vector is assumed to contain the values shown in the following pseudocode.</span></span>


```
src.x = N*L        ; The dot product between normal and direction to light
src.y = N*H        ; The dot product between normal and half vector
src.z = ignored    ; This value is ignored
src.w = exponent   ; The value must be between -128.0 and 128.0
```



<span data-ttu-id="6a746-126">下列程式碼片段會顯示已執行的作業。</span><span class="sxs-lookup"><span data-stu-id="6a746-126">The following code fragment shows the operations performed.</span></span>


```
dest.x = 1;
dest.y = 0;
dest.z = 0;
dest.w = 1;

float power = src.w;
const float MAXPOWER = 127.9961f;
if (power < -MAXPOWER)
    power = -MAXPOWER;          // Fits into 8.8 fixed point format
else if (power > MAXPOWER)
    power = MAXPOWER;          // Fits into 8.8 fixed point format

if (src.x > 0)
{
    dest.y = src.x;
    if (src.y > 0)
    {
        // Allowed approximation is EXP(power * LOG(src.y))
        dest.z = (float)(pow(src.y, power));
    }
}
```



<span data-ttu-id="6a746-127">評估目的地 y 元件 (destination. y) 可接受降低精確度算術。</span><span class="sxs-lookup"><span data-stu-id="6a746-127">Reduced precision arithmetic is acceptable in evaluating the destination y component (dest.y).</span></span> <span data-ttu-id="6a746-128">執行必須在 power 引數中至少支援8個小數位。</span><span class="sxs-lookup"><span data-stu-id="6a746-128">An implementation must support at least eight fraction bits in the power argument.</span></span> <span data-ttu-id="6a746-129">點乘積以正規化向量計算，而夾具限制為-128 到128。</span><span class="sxs-lookup"><span data-stu-id="6a746-129">Dot products are calculated with normalized vectors, and clamp limits are -128 to 128.</span></span>

<span data-ttu-id="6a746-130">錯誤應該對應至 [logp-vs](logp---vs.md) 和 [exp-vs](exp---vs.md) 組合，或8位色彩元件的最多一個有效位。</span><span class="sxs-lookup"><span data-stu-id="6a746-130">Error should correspond to a [logp - vs](logp---vs.md) and [exp - vs](exp---vs.md) combination, or no more than approximately one significant bit for an 8-bit color component.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6a746-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="6a746-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a746-132">頂點著色器指示</span><span class="sxs-lookup"><span data-stu-id="6a746-132">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 





---
title: cnd-ps
description: 根據 src0 0.5 的比較，有條件地選擇 src1 和 src2 收取。
ms.assetid: 7a3b49e9-d146-47dc-99a8-4f336db7d0d5
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1fd3a14e2ac4bd283a4e67724fbb42ac965ea707
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104092453"
---
# <a name="cnd---ps"></a><span data-ttu-id="37eb3-103">cnd-ps</span><span class="sxs-lookup"><span data-stu-id="37eb3-103">cnd - ps</span></span>

<span data-ttu-id="37eb3-104">根據 > 0.5 的比較 src0，有條件地選擇 src1 和 src2 收取。</span><span class="sxs-lookup"><span data-stu-id="37eb3-104">Conditionally chooses between src1 and src2, based on the comparison src0 > 0.5.</span></span>

## <a name="syntax"></a><span data-ttu-id="37eb3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="37eb3-105">Syntax</span></span>



| <span data-ttu-id="37eb3-106">cnd dst、src0、src1、src2 收取</span><span class="sxs-lookup"><span data-stu-id="37eb3-106">cnd dst, src0, src1, src2</span></span> |
|---------------------------|



 

<span data-ttu-id="37eb3-107">其中</span><span class="sxs-lookup"><span data-stu-id="37eb3-107">where</span></span>

-   <span data-ttu-id="37eb3-108">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="37eb3-108">dst is the destination register.</span></span>
-   <span data-ttu-id="37eb3-109">src0 是來源註冊。</span><span class="sxs-lookup"><span data-stu-id="37eb3-109">src0 is a source register.</span></span>
-   <span data-ttu-id="37eb3-110">src1 是來源註冊。</span><span class="sxs-lookup"><span data-stu-id="37eb3-110">src1 is a source register.</span></span>
-   <span data-ttu-id="37eb3-111">src2 收取是來源註冊。</span><span class="sxs-lookup"><span data-stu-id="37eb3-111">src2 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="37eb3-112">備註</span><span class="sxs-lookup"><span data-stu-id="37eb3-112">Remarks</span></span>



| <span data-ttu-id="37eb3-113">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="37eb3-113">Pixel shader versions</span></span> | <span data-ttu-id="37eb3-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="37eb3-114">1\_1</span></span> | <span data-ttu-id="37eb3-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="37eb3-115">1\_2</span></span> | <span data-ttu-id="37eb3-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="37eb3-116">1\_3</span></span> | <span data-ttu-id="37eb3-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="37eb3-117">1\_4</span></span> | <span data-ttu-id="37eb3-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="37eb3-118">2\_0</span></span> | <span data-ttu-id="37eb3-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="37eb3-119">2\_x</span></span> | <span data-ttu-id="37eb3-120">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="37eb3-120">2\_sw</span></span> | <span data-ttu-id="37eb3-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="37eb3-121">3\_0</span></span> | <span data-ttu-id="37eb3-122">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="37eb3-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="37eb3-123">cnd</span><span class="sxs-lookup"><span data-stu-id="37eb3-123">cnd</span></span>                   | <span data-ttu-id="37eb3-124">x</span><span class="sxs-lookup"><span data-stu-id="37eb3-124">x</span></span>    | <span data-ttu-id="37eb3-125">x</span><span class="sxs-lookup"><span data-stu-id="37eb3-125">x</span></span>    | <span data-ttu-id="37eb3-126">x</span><span class="sxs-lookup"><span data-stu-id="37eb3-126">x</span></span>    | <span data-ttu-id="37eb3-127">x</span><span class="sxs-lookup"><span data-stu-id="37eb3-127">x</span></span>    |      |      |       |      |       |



 

<span data-ttu-id="37eb3-128">若為 1 \_ 1 到 1 \_ 3 的版本，src0 必須是 r0。</span><span class="sxs-lookup"><span data-stu-id="37eb3-128">For versions 1\_1 to 1\_3, src0 must be r0.a.</span></span>


```
// Version 1_1 to 1_3
if (r0.a > 0.5)
  dest = src1
else
  dest = src2
```



<span data-ttu-id="37eb3-129">第1版會 \_ 分別比較每個通道。</span><span class="sxs-lookup"><span data-stu-id="37eb3-129">Version 1\_4 compares each channel separately.</span></span>


```
for each component in src0
{
   if (src0.component > 0.5)
     dest.component = src1.component
   else
     dest.component = src2.component
}
```



<span data-ttu-id="37eb3-130">這些範例示範在第1版著色器中完成的四個通道比較 \_ ，以及第1版著色器中可能的單一通道比較 \_ 。</span><span class="sxs-lookup"><span data-stu-id="37eb3-130">These examples show a four-channel comparison done in a version 1\_4 shader, as well as a single-channel comparison possible in a version 1\_1 shader.</span></span>


```
ps_1_4
def c0, -0.5, 0.5, 0, 0.6
def c1,  0,0,0,0
def c2,  1,1,1,1

cnd r1, c0, c1, c2   // r0 contains 1,1,1,0 because
// r1.x = c2.x because c0.x <= 0.5
// r1.y = c2.y because c0.y <= 0.5
// r1.z = c2.z because c0.z <= 0.5
// r1.w = c1.w because c0.w >  0.5
```



<span data-ttu-id="37eb3-131">第1版 \_ 到第1版 \_ 只會與 r0 的已複寫 Alpha 通道進行比較。</span><span class="sxs-lookup"><span data-stu-id="37eb3-131">Version 1\_1 to 1\_3 compares against the replicated alpha channel of r0 only.</span></span>


```
ps_1_1
def c0, -0.5, 0.5, 0, 0.6
def c1,  0,0,0,0
def c2,  1,1,1,1
mov r0, c0
cnd r1, r0.a, c1, c2   // r1 gets assigned 0,0,0,0 because 
                       // r0.a > 0.5, therefore r1.xyzw = c1.xyzw
```



<span data-ttu-id="37eb3-132">此範例會比較兩個值： A 和 B。此範例假設將載入至 v0，並將 B 載入至 v1。</span><span class="sxs-lookup"><span data-stu-id="37eb3-132">This example compares two values, A and B. The example assumes A is loaded into v0 and B is loaded into v1.</span></span> <span data-ttu-id="37eb3-133">A 和 B 的範圍必須介於-1 到 + 1 之間，因為色彩暫存器 (vn) 定義為介於0和1之間，所以在此範例中，將會滿足此限制。</span><span class="sxs-lookup"><span data-stu-id="37eb3-133">Both A and B must be in the range of -1 to +1, and since the color registers (vₙ) are defined to be between 0 and 1, the restriction happens to be satisfied in this example.</span></span>


```
ps_1_1                // Version instruction
sub r0, v0, v1_bias   // r0 = A - (B - 0.5)
cnd r0, r0.a, c0, c1  // r0 = ( A > B ? c0 : c1 )

// r0 = c0 if A > B, otherwise, r0 = c1
```



## <a name="related-topics"></a><span data-ttu-id="37eb3-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="37eb3-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="37eb3-135">圖元著色器指示</span><span class="sxs-lookup"><span data-stu-id="37eb3-135">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 





---
title: mov-vs
description: 移動暫存器之間的浮點數據。
ms.assetid: bf013ab2-593e-4201-ba75-faebd0c9f97a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 00f207261ad8ba6ac83360c40bc6008530292816
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "103679168"
---
# <a name="mov---vs"></a><span data-ttu-id="4a236-103">mov-vs</span><span class="sxs-lookup"><span data-stu-id="4a236-103">mov - vs</span></span>

<span data-ttu-id="4a236-104">移動暫存器之間的浮點數據。</span><span class="sxs-lookup"><span data-stu-id="4a236-104">Move floating-point data between registers.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a236-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4a236-105">Syntax</span></span>



| <span data-ttu-id="4a236-106">mov dst、src</span><span class="sxs-lookup"><span data-stu-id="4a236-106">mov dst, src</span></span> |
|--------------|



 

<span data-ttu-id="4a236-107">其中</span><span class="sxs-lookup"><span data-stu-id="4a236-107">where</span></span>

-   <span data-ttu-id="4a236-108">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="4a236-108">dst is the destination register.</span></span>
-   <span data-ttu-id="4a236-109">src 是來源暫存器。</span><span class="sxs-lookup"><span data-stu-id="4a236-109">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a236-110">備註</span><span class="sxs-lookup"><span data-stu-id="4a236-110">Remarks</span></span>



| <span data-ttu-id="4a236-111">頂點著色器版本</span><span class="sxs-lookup"><span data-stu-id="4a236-111">Vertex shader versions</span></span> | <span data-ttu-id="4a236-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="4a236-112">1\_1</span></span> | <span data-ttu-id="4a236-113">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4a236-113">2\_0</span></span> | <span data-ttu-id="4a236-114">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="4a236-114">2\_x</span></span> | <span data-ttu-id="4a236-115">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="4a236-115">2\_sw</span></span> | <span data-ttu-id="4a236-116">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4a236-116">3\_0</span></span> | <span data-ttu-id="4a236-117">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="4a236-117">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="4a236-118">平均線</span><span class="sxs-lookup"><span data-stu-id="4a236-118">mov</span></span>                    | <span data-ttu-id="4a236-119">x</span><span class="sxs-lookup"><span data-stu-id="4a236-119">x</span></span>    | <span data-ttu-id="4a236-120">x</span><span class="sxs-lookup"><span data-stu-id="4a236-120">x</span></span>    | <span data-ttu-id="4a236-121">x</span><span class="sxs-lookup"><span data-stu-id="4a236-121">x</span></span>    | <span data-ttu-id="4a236-122">x</span><span class="sxs-lookup"><span data-stu-id="4a236-122">x</span></span>     | <span data-ttu-id="4a236-123">x</span><span class="sxs-lookup"><span data-stu-id="4a236-123">x</span></span>    | <span data-ttu-id="4a236-124">x</span><span class="sxs-lookup"><span data-stu-id="4a236-124">x</span></span>     |



 

<span data-ttu-id="4a236-125">可以用於浮點數據。</span><span class="sxs-lookup"><span data-stu-id="4a236-125">Can be used for floating point data.</span></span> <span data-ttu-id="4a236-126">針對版本與 \_ 1 \_ 1，也可以使用它來寫入位址註冊。</span><span class="sxs-lookup"><span data-stu-id="4a236-126">For version vs\_1\_1, it can also be used to write the address register.</span></span> <span data-ttu-id="4a236-127">當用來更新位址暫存器時，會使用四捨五入到最接近的位置，從浮點數轉換值。</span><span class="sxs-lookup"><span data-stu-id="4a236-127">When used to update address registers, the values are converted from floating point using rounding to nearest.</span></span>

<span data-ttu-id="4a236-128">下列程式碼片段會顯示已執行的作業。</span><span class="sxs-lookup"><span data-stu-id="4a236-128">The following code fragment shows the operations performed.</span></span>


```
if(dest is an integer register)
{
    int intSrc = RoundToNearest(src.w);
    dest = intSrc;
}
else
{
    dest = src;
}
```



## <a name="related-topics"></a><span data-ttu-id="4a236-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="4a236-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a236-130">頂點著色器指示</span><span class="sxs-lookup"><span data-stu-id="4a236-130">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 





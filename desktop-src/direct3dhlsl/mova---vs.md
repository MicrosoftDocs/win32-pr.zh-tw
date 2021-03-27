---
title: mova-vs
description: 將資料從浮點暫存器移至位址暫存器（a0）。
ms.assetid: 929a0670-f337-4d6d-a7e7-d285e7dc8ae1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9ac29bf0d74b4eb2cb6cb86bdf6b070cf56823eb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104971609"
---
# <a name="mova---vs"></a><span data-ttu-id="5c76f-103">mova-vs</span><span class="sxs-lookup"><span data-stu-id="5c76f-103">mova - vs</span></span>

<span data-ttu-id="5c76f-104">將資料從浮點暫存器移至 [位址](dx9-graphics-reference-asm-vs-registers-address.md)暫存器（a0）。</span><span class="sxs-lookup"><span data-stu-id="5c76f-104">Move data from a floating point register to the [Address Register](dx9-graphics-reference-asm-vs-registers-address.md), a0.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c76f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5c76f-105">Syntax</span></span>



| <span data-ttu-id="5c76f-106">mova dst、src</span><span class="sxs-lookup"><span data-stu-id="5c76f-106">mova dst, src</span></span> |
|---------------|



 

<span data-ttu-id="5c76f-107">其中</span><span class="sxs-lookup"><span data-stu-id="5c76f-107">where</span></span>

-   <span data-ttu-id="5c76f-108">dst 必須是 [位址](dx9-graphics-reference-asm-vs-registers-address.md)暫存器（a0）。</span><span class="sxs-lookup"><span data-stu-id="5c76f-108">dst must be the [Address Register](dx9-graphics-reference-asm-vs-registers-address.md), a0.</span></span>
-   <span data-ttu-id="5c76f-109">src 是來源暫存器。</span><span class="sxs-lookup"><span data-stu-id="5c76f-109">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c76f-110">備註</span><span class="sxs-lookup"><span data-stu-id="5c76f-110">Remarks</span></span>



| <span data-ttu-id="5c76f-111">頂點著色器版本</span><span class="sxs-lookup"><span data-stu-id="5c76f-111">Vertex shader versions</span></span> | <span data-ttu-id="5c76f-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="5c76f-112">1\_1</span></span> | <span data-ttu-id="5c76f-113">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5c76f-113">2\_0</span></span> | <span data-ttu-id="5c76f-114">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="5c76f-114">2\_x</span></span> | <span data-ttu-id="5c76f-115">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="5c76f-115">2\_sw</span></span> | <span data-ttu-id="5c76f-116">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5c76f-116">3\_0</span></span> | <span data-ttu-id="5c76f-117">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="5c76f-117">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="5c76f-118">mova</span><span class="sxs-lookup"><span data-stu-id="5c76f-118">mova</span></span>                   |      | <span data-ttu-id="5c76f-119">x</span><span class="sxs-lookup"><span data-stu-id="5c76f-119">x</span></span>    | <span data-ttu-id="5c76f-120">x</span><span class="sxs-lookup"><span data-stu-id="5c76f-120">x</span></span>    | <span data-ttu-id="5c76f-121">x</span><span class="sxs-lookup"><span data-stu-id="5c76f-121">x</span></span>     | <span data-ttu-id="5c76f-122">x</span><span class="sxs-lookup"><span data-stu-id="5c76f-122">x</span></span>    | <span data-ttu-id="5c76f-123">x</span><span class="sxs-lookup"><span data-stu-id="5c76f-123">x</span></span>     |



 

<span data-ttu-id="5c76f-124">將浮點數據移至整數暫存器。</span><span class="sxs-lookup"><span data-stu-id="5c76f-124">Moves floating point data to an integer register.</span></span> <span data-ttu-id="5c76f-125">這些值會使用四捨五入到最接近的位置從浮點轉換。</span><span class="sxs-lookup"><span data-stu-id="5c76f-125">The values are converted from floating point using rounding to nearest.</span></span>

<span data-ttu-id="5c76f-126">Address register 是唯一允許的目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="5c76f-126">The address register is the only destination register allowed.</span></span>

<span data-ttu-id="5c76f-127">下列程式碼片段會顯示已執行的作業。</span><span class="sxs-lookup"><span data-stu-id="5c76f-127">The following code fragment shows the operations performed.</span></span>


```
if(dest is an integer register)
{
    int intSrc = RoundToNearest(src);
    dest = intSrc;
}
else
{
    dest = src;
}
```



<span data-ttu-id="5c76f-128">如果是 2 \_ x 以上的版本，位址暫存器是元件向量。</span><span class="sxs-lookup"><span data-stu-id="5c76f-128">For versions 2\_x and above, the address register is a component vector.</span></span> <span data-ttu-id="5c76f-129">因此，允許任何寫入遮罩。</span><span class="sxs-lookup"><span data-stu-id="5c76f-129">Therefore, any write mask is allowed.</span></span>


```
mova a0.xz, r0
```



## <a name="related-topics"></a><span data-ttu-id="5c76f-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="5c76f-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c76f-131">頂點著色器指示</span><span class="sxs-lookup"><span data-stu-id="5c76f-131">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 





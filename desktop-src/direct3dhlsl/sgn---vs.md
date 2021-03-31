---
title: 登錄-vs
description: 計算輸入的正負號。
ms.assetid: b03530d1-c621-483e-bd94-31abafeb2e6e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8573ff7e33a127d7c30af1fe512fbd3da298d0eb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104373806"
---
# <a name="sgn---vs"></a><span data-ttu-id="e3e00-103">登錄-vs</span><span class="sxs-lookup"><span data-stu-id="e3e00-103">sgn - vs</span></span>

<span data-ttu-id="e3e00-104">計算輸入的正負號。</span><span class="sxs-lookup"><span data-stu-id="e3e00-104">Computes the sign of the input.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3e00-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e3e00-105">Syntax</span></span>



| <span data-ttu-id="e3e00-106">登錄 dst、src0、src1、src2 收取</span><span class="sxs-lookup"><span data-stu-id="e3e00-106">sgn dst, src0, src1, src2</span></span> |
|---------------------------|



 

<span data-ttu-id="e3e00-107">其中</span><span class="sxs-lookup"><span data-stu-id="e3e00-107">where</span></span>

-   <span data-ttu-id="e3e00-108">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="e3e00-108">dst is the destination register.</span></span>
-   <span data-ttu-id="e3e00-109">src0 是來源註冊。</span><span class="sxs-lookup"><span data-stu-id="e3e00-109">src0 is a source register.</span></span>
-   <span data-ttu-id="e3e00-110">src1 是保存中繼結果的臨時暫存器。</span><span class="sxs-lookup"><span data-stu-id="e3e00-110">src1 is a temporary register that holds intermediate results.</span></span> <span data-ttu-id="e3e00-111">執行之後，內容是未定義的。</span><span class="sxs-lookup"><span data-stu-id="e3e00-111">Following execution, contents are undefined.</span></span>
-   <span data-ttu-id="e3e00-112">src2 收取是保存中繼結果的臨時暫存器。</span><span class="sxs-lookup"><span data-stu-id="e3e00-112">src2 is a temporary register that holds intermediate results.</span></span> <span data-ttu-id="e3e00-113">執行之後，內容是未定義的。</span><span class="sxs-lookup"><span data-stu-id="e3e00-113">Following execution, contents are undefined.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3e00-114">備註</span><span class="sxs-lookup"><span data-stu-id="e3e00-114">Remarks</span></span>



| <span data-ttu-id="e3e00-115">頂點著色器版本</span><span class="sxs-lookup"><span data-stu-id="e3e00-115">Vertex shader versions</span></span> | <span data-ttu-id="e3e00-116">1\_1</span><span class="sxs-lookup"><span data-stu-id="e3e00-116">1\_1</span></span> | <span data-ttu-id="e3e00-117">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e3e00-117">2\_0</span></span> | <span data-ttu-id="e3e00-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="e3e00-118">2\_x</span></span> | <span data-ttu-id="e3e00-119">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="e3e00-119">2\_sw</span></span> | <span data-ttu-id="e3e00-120">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e3e00-120">3\_0</span></span> | <span data-ttu-id="e3e00-121">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="e3e00-121">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="e3e00-122">登錄</span><span class="sxs-lookup"><span data-stu-id="e3e00-122">sgn</span></span>                    |      | <span data-ttu-id="e3e00-123">x</span><span class="sxs-lookup"><span data-stu-id="e3e00-123">x</span></span>    | <span data-ttu-id="e3e00-124">x</span><span class="sxs-lookup"><span data-stu-id="e3e00-124">x</span></span>    | <span data-ttu-id="e3e00-125">x</span><span class="sxs-lookup"><span data-stu-id="e3e00-125">x</span></span>     | <span data-ttu-id="e3e00-126">x</span><span class="sxs-lookup"><span data-stu-id="e3e00-126">x</span></span>    | <span data-ttu-id="e3e00-127">x</span><span class="sxs-lookup"><span data-stu-id="e3e00-127">x</span></span>     |



 

<span data-ttu-id="e3e00-128">此指示的運作方式如下所示。</span><span class="sxs-lookup"><span data-stu-id="e3e00-128">This instruction works as shown below.</span></span>


```
for each component in src0
{
   if (src0.component < 0) 
       dest.component = -1; 
   else
       if (src0.component == 0) 
           dest.component = 0; 
       else 
           dest.component = 1;
}
```



<span data-ttu-id="e3e00-129">src1 和 src2 收取必須是不同的 [臨時](dx9-graphics-reference-asm-vs-registers-temporary.md)暫存器。</span><span class="sxs-lookup"><span data-stu-id="e3e00-129">src1 and src2 must be different [Temporary Register](dx9-graphics-reference-asm-vs-registers-temporary.md)s.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e3e00-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="e3e00-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3e00-131">頂點著色器指示</span><span class="sxs-lookup"><span data-stu-id="e3e00-131">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 





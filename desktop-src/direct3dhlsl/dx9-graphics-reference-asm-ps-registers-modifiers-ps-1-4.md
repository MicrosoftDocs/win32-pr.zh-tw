---
title: '\_ \_ 適用于 texld、texcrd 的 ps 1 4 來源登錄修飾詞'
description: 雙圖元著色器第1版 \_ 的材質位址指示（texld-ps \_ 1 \_ 4 和 texcrd-ps）有自訂語法。
ms.assetid: bbc8074f-882e-4b67-ae4d-1641ceb7f3ad
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: af2097ee682aec7da0ca36df9e4b465fb360f814
ms.sourcegitcommit: b95a94ffffda33f9ebbdd41787c01866444b4cf4
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/27/2019
ms.locfileid: "104092483"
---
# <a name="ps_1_4-source-register-modifiers-for-texld-texcrd"></a><span data-ttu-id="39e5a-103">\_ \_ 適用于 texld、texcrd 的 ps 1 4 來源登錄修飾詞</span><span class="sxs-lookup"><span data-stu-id="39e5a-103">ps\_1\_4 source register modifiers for texld, texcrd</span></span>

<span data-ttu-id="39e5a-104">雙圖元著色器第1版 \_ 的材質位址指示（ [texld-ps \_ 1 \_ 4](texld---ps-1-4.md) 和 [texcrd-ps](texcrd---ps.md)）有自訂語法。</span><span class="sxs-lookup"><span data-stu-id="39e5a-104">Two pixel shader version 1\_4 texture address instructions, [texld - ps\_1\_4](texld---ps-1-4.md) and [texcrd - ps](texcrd---ps.md), have custom syntax.</span></span> <span data-ttu-id="39e5a-105">這些指示支援自己的一組來源登錄修飾詞、來源登錄選取器，以及目的地登錄寫入遮罩，如下所示。</span><span class="sxs-lookup"><span data-stu-id="39e5a-105">These instructions support their own set of source register modifiers, source register selectors, and destination-register write masks, as shown here.</span></span>

## <a name="source-register-modifiers-for-texld-and-texcrd"></a><span data-ttu-id="39e5a-106">Texld 和 texcrd 的來源登錄修飾詞</span><span class="sxs-lookup"><span data-stu-id="39e5a-106">Source Register Modifiers for texld and texcrd</span></span>

<span data-ttu-id="39e5a-107">這些修飾詞會將 x 和 y 值除以 z 或 w 值，以提供 projective 分割功能。</span><span class="sxs-lookup"><span data-stu-id="39e5a-107">These modifiers provide projective divide functionality by dividing the x and y values by either the z or w values.</span></span>



| <span data-ttu-id="39e5a-108">來源暫存器修飾符</span><span class="sxs-lookup"><span data-stu-id="39e5a-108">Source register modifiers</span></span> | <span data-ttu-id="39e5a-109">描述</span><span class="sxs-lookup"><span data-stu-id="39e5a-109">Description</span></span>                | <span data-ttu-id="39e5a-110">語法</span><span class="sxs-lookup"><span data-stu-id="39e5a-110">Syntax</span></span>       |
|---------------------------|----------------------------|--------------|
| <span data-ttu-id="39e5a-111">\_Dz</span><span class="sxs-lookup"><span data-stu-id="39e5a-111">\_dz</span></span>                      | <span data-ttu-id="39e5a-112">以 z 分隔 x、y 元件</span><span class="sxs-lookup"><span data-stu-id="39e5a-112">Divide x,y components by z</span></span> | <span data-ttu-id="39e5a-113">註冊 \_ dz</span><span class="sxs-lookup"><span data-stu-id="39e5a-113">register\_dz</span></span> |
| <span data-ttu-id="39e5a-114">\_db</span><span class="sxs-lookup"><span data-stu-id="39e5a-114">\_db</span></span>                      | <span data-ttu-id="39e5a-115">以 z 分隔 x、y 元件</span><span class="sxs-lookup"><span data-stu-id="39e5a-115">Divide x,y components by z</span></span> | <span data-ttu-id="39e5a-116">註冊 \_ db</span><span class="sxs-lookup"><span data-stu-id="39e5a-116">register\_db</span></span> |
| <span data-ttu-id="39e5a-117">\_dw</span><span class="sxs-lookup"><span data-stu-id="39e5a-117">\_dw</span></span>                      | <span data-ttu-id="39e5a-118">將 x、y 元件除以 w</span><span class="sxs-lookup"><span data-stu-id="39e5a-118">Divide x,y components by w</span></span> | <span data-ttu-id="39e5a-119">註冊 \_ dw</span><span class="sxs-lookup"><span data-stu-id="39e5a-119">register\_dw</span></span> |
| <span data-ttu-id="39e5a-120">\_大</span><span class="sxs-lookup"><span data-stu-id="39e5a-120">\_da</span></span>                      | <span data-ttu-id="39e5a-121">將 x、y 元件除以 w</span><span class="sxs-lookup"><span data-stu-id="39e5a-121">Divide x,y components by w</span></span> | <span data-ttu-id="39e5a-122">註冊 \_ da</span><span class="sxs-lookup"><span data-stu-id="39e5a-122">register\_da</span></span> |



 

### <a name="remarks"></a><span data-ttu-id="39e5a-123">備註</span><span class="sxs-lookup"><span data-stu-id="39e5a-123">Remarks</span></span>

<span data-ttu-id="39e5a-124">\_Dz 或 \_ db 修飾詞會執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="39e5a-124">The \_dz or \_db modifier does the following:</span></span>


```
x' = x/z ( x' = 1.0 if z == 0)
y' = y/z ( y' = 1.0 if z == 0)
z' is undefined
w' is undefined
```



<span data-ttu-id="39e5a-125">\_Dw 或 \_ da 修飾詞會執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="39e5a-125">The \_dw or \_da modifier does the following:</span></span>


```
x' = x/w ( x' = 1.0 if w == 0)
y' = y/w ( y' = 1.0 if w == 0)
z' is undefined
w' is undefined
```



## <a name="related-topics"></a><span data-ttu-id="39e5a-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="39e5a-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39e5a-127">圖元著色器來源登錄修飾詞</span><span class="sxs-lookup"><span data-stu-id="39e5a-127">Pixel Shader Source Register Modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 





---
title: '暫時註冊 (HLSL PS 參考) '
description: 圖元著色器輸入暫存登錄用來保存中繼結果。
ms.assetid: e61daaa1-0a9b-4b1c-b91c-56573be59ed9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7aebee99a693ac629d9cc8a372fba7589a9e29ef
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/23/2019
ms.locfileid: "103841716"
---
# <a name="temporary-register-hlsl-ps-reference"></a><span data-ttu-id="035f9-103">暫時註冊 (HLSL PS 參考) </span><span class="sxs-lookup"><span data-stu-id="035f9-103">Temporary register (HLSL PS reference)</span></span>

<span data-ttu-id="035f9-104">圖元著色器輸入暫存登錄用來保存中繼結果。</span><span class="sxs-lookup"><span data-stu-id="035f9-104">Pixel shader input temporary registers are used to hold intermediate results.</span></span>

<span data-ttu-id="035f9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="035f9-105">Syntax</span></span>


```
no declaration is required
```





| <span data-ttu-id="035f9-106">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="035f9-106">Pixel shader versions</span></span> | <span data-ttu-id="035f9-107">1\_1</span><span class="sxs-lookup"><span data-stu-id="035f9-107">1\_1</span></span> | <span data-ttu-id="035f9-108">1\_2</span><span class="sxs-lookup"><span data-stu-id="035f9-108">1\_2</span></span> | <span data-ttu-id="035f9-109">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="035f9-109">1\_3</span></span> | <span data-ttu-id="035f9-110">1\_4</span><span class="sxs-lookup"><span data-stu-id="035f9-110">1\_4</span></span> | <span data-ttu-id="035f9-111">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="035f9-111">2\_0</span></span> | <span data-ttu-id="035f9-112">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="035f9-112">2\_sw</span></span> | <span data-ttu-id="035f9-113">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="035f9-113">2\_x</span></span> | <span data-ttu-id="035f9-114">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="035f9-114">3\_0</span></span> | <span data-ttu-id="035f9-115">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="035f9-115">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|-------|------|------|-------|
| <span data-ttu-id="035f9-116">暫時註冊</span><span class="sxs-lookup"><span data-stu-id="035f9-116">Temporary Register</span></span>    |      |      |      |      | <span data-ttu-id="035f9-117">x</span><span class="sxs-lookup"><span data-stu-id="035f9-117">x</span></span>    | <span data-ttu-id="035f9-118">x</span><span class="sxs-lookup"><span data-stu-id="035f9-118">x</span></span>     | <span data-ttu-id="035f9-119">x</span><span class="sxs-lookup"><span data-stu-id="035f9-119">x</span></span>    | <span data-ttu-id="035f9-120">x</span><span class="sxs-lookup"><span data-stu-id="035f9-120">x</span></span>    | <span data-ttu-id="035f9-121">x</span><span class="sxs-lookup"><span data-stu-id="035f9-121">x</span></span>     |



 

-   <span data-ttu-id="035f9-122">有12個圖元著色器暫存暫存器： r0 至 r11。</span><span class="sxs-lookup"><span data-stu-id="035f9-122">There are 12 pixel-shader temporary registers: r0 to r11.</span></span>
-   <span data-ttu-id="035f9-123">這些暫存器是用來在計算期間儲存中繼結果。</span><span class="sxs-lookup"><span data-stu-id="035f9-123">These registers are used for storing intermediate results during computations.</span></span>
-   <span data-ttu-id="035f9-124">如果暫存登錄使用先前程式碼未定義的元件，著色器驗證將會失敗。</span><span class="sxs-lookup"><span data-stu-id="035f9-124">If a temporary register uses components that are not defined in previous code, shader validation will fail.</span></span>
-   <span data-ttu-id="035f9-125">這些至少是浮點精確度。</span><span class="sxs-lookup"><span data-stu-id="035f9-125">These are at least floating-point precision.</span></span>
-   <span data-ttu-id="035f9-126">最多可以在單一指令中使用三個。</span><span class="sxs-lookup"><span data-stu-id="035f9-126">A maximum of three can be used in a single instruction.</span></span>

## <a name="related-topics"></a><span data-ttu-id="035f9-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="035f9-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="035f9-128">寄存 器</span><span class="sxs-lookup"><span data-stu-id="035f9-128">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 





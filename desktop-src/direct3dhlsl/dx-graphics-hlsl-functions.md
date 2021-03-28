---
title: '函數 (HLSL 參考) '
description: 函數會封裝 HLSL 語句。
ms.assetid: b6f934e5-eac7-4859-b1d0-698632011e1d
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 59b0bfcb2079329d4d7ad7c02e7e5a326d22c236
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/23/2019
ms.locfileid: "104313773"
---
# <a name="functions-hlsl-reference"></a><span data-ttu-id="b2e64-103">函數 (HLSL 參考) </span><span class="sxs-lookup"><span data-stu-id="b2e64-103">Functions (HLSL reference)</span></span>

<span data-ttu-id="b2e64-104">函數會封裝 HLSL 語句。</span><span class="sxs-lookup"><span data-stu-id="b2e64-104">Functions encapsulate HLSL statements.</span></span> <span data-ttu-id="b2e64-105">這可讓您先對一組函數進行偵錯工具，然後在著色器或效果之間重複使用它們。</span><span class="sxs-lookup"><span data-stu-id="b2e64-105">This enables you to debug a set of functions and then reuse them across shaders or effects.</span></span> <span data-ttu-id="b2e64-106">您可能會想要建立一個函式，以封裝頂點著色器、圖元著色器或紋理著色器的功能。</span><span class="sxs-lookup"><span data-stu-id="b2e64-106">You may want to create a function that encapsulates the functionality of a vertex shader, pixel shader or texture shader.</span></span> <span data-ttu-id="b2e64-107">有時候，您可能會想要撰寫 helper 函式來執行一些常用的工作，然後從您的著色器函式呼叫該 helper 函式。</span><span class="sxs-lookup"><span data-stu-id="b2e64-107">Other times, you may want to write a helper function that performs some commonly used task, and then call that helper function from your shader function.</span></span> <span data-ttu-id="b2e64-108">針對 HLSL 撰寫著色器函式的規則，與撰寫 C 函數非常類似。</span><span class="sxs-lookup"><span data-stu-id="b2e64-108">The rules for writing shader functions for HLSL are very similar to writing C functions.</span></span>

-   [<span data-ttu-id="b2e64-109">語法</span><span class="sxs-lookup"><span data-stu-id="b2e64-109">Syntax</span></span>](dx-graphics-hlsl-function-syntax.md)
-   [<span data-ttu-id="b2e64-110">參數</span><span class="sxs-lookup"><span data-stu-id="b2e64-110">Parameters</span></span>](dx-graphics-hlsl-function-parameters.md)
-   [<span data-ttu-id="b2e64-111">Return 陳述式</span><span class="sxs-lookup"><span data-stu-id="b2e64-111">Return Statement</span></span>](dx-graphics-hlsl-return.md)
-   [<span data-ttu-id="b2e64-112">簽章</span><span class="sxs-lookup"><span data-stu-id="b2e64-112">Signatures</span></span>](dx-graphics-hlsl-signatures.md)

<span data-ttu-id="b2e64-113">HLSL 也有一些內建的 [**內建函式 (DIRECTX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)。</span><span class="sxs-lookup"><span data-stu-id="b2e64-113">HLSL also has a number of built-in [**Intrinsic Functions (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md).</span></span> <span data-ttu-id="b2e64-114">因為所有內建函式都會經過測試且效能優化，所以最好盡可能使用內建函式，而不是建立自己的函式。</span><span class="sxs-lookup"><span data-stu-id="b2e64-114">Because all intrinsic functions are tested and performance optimized, it is good practice to use an intrinsic function where possible instead of creating your own function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b2e64-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="b2e64-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2e64-116"> (DirectX HLSL 的語言語法) </span><span class="sxs-lookup"><span data-stu-id="b2e64-116">Language Syntax (DirectX HLSL)</span></span>](dx-graphics-hlsl-language-syntax.md)
</dt> </dl>

 

 





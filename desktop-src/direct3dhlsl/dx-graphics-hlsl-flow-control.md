---
title: 流量控制
description: 大部分的硬體都設計為逐行執行著色器程式碼，並執行每個 HLSL 語句一次。
ms.assetid: 94f22e39-8e71-424b-8ca1-bafc843f843f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 70bb7706e520818c86286947acfba6cae0759b4d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300507"
---
# <a name="flow-control"></a><span data-ttu-id="66244-103">流量控制</span><span class="sxs-lookup"><span data-stu-id="66244-103">Flow Control</span></span>

<span data-ttu-id="66244-104">大部分的硬體都設計為逐行執行著色器程式碼，並執行每個 HLSL 語句一次。</span><span class="sxs-lookup"><span data-stu-id="66244-104">Most hardware is designed to run shader code line by line, executing each HLSL statement once.</span></span> <span data-ttu-id="66244-105">流程式控制制語句會在執行時間決定要執行下一個 HLSL 語句的區塊。</span><span class="sxs-lookup"><span data-stu-id="66244-105">A flow-control statement determines at run time which block of HLSL statements to execute next.</span></span> <span data-ttu-id="66244-106">著色器可以使用流程式控制制語句，在一組語句中執行迴圈，或將 (分支) 到下一行的指令以外的指令。</span><span class="sxs-lookup"><span data-stu-id="66244-106">Using a flow-control statement, a shader can loop through a set of statements, or jump (branch) to an instruction other than the one on the next line.</span></span> <span data-ttu-id="66244-107">某些流程式控制制語句支援在編譯時期指定的靜態控制項;其他則提供前提控制項，這是在執行時間進行的每個元件決策，而其他人則支援動態控制項，也就是在執行時間根據變數的內容進行決策。</span><span class="sxs-lookup"><span data-stu-id="66244-107">Some flow-control statements support static control that is specified at compile time; others offer predicated control which is a per-component decision made at runtime, and still others support dynamic control which is a decision made at run time based on the contents of a variable.</span></span>

<span data-ttu-id="66244-108">HLSL 支援下列流程式控制制語句。</span><span class="sxs-lookup"><span data-stu-id="66244-108">HLSL supports the following flow-control statements.</span></span>

-   [<span data-ttu-id="66244-109">break</span><span class="sxs-lookup"><span data-stu-id="66244-109">break</span></span>](dx-graphics-hlsl-break.md)
-   [<span data-ttu-id="66244-110">繼續</span><span class="sxs-lookup"><span data-stu-id="66244-110">continue</span></span>](dx-graphics-hlsl-continue.md)
-   [<span data-ttu-id="66244-111">丟棄</span><span class="sxs-lookup"><span data-stu-id="66244-111">discard</span></span>](dx-graphics-hlsl-discard.md)
-   [<span data-ttu-id="66244-112">do</span><span class="sxs-lookup"><span data-stu-id="66244-112">do</span></span>](dx-graphics-hlsl-do.md)
-   [<span data-ttu-id="66244-113">for</span><span class="sxs-lookup"><span data-stu-id="66244-113">for</span></span>](dx-graphics-hlsl-for.md)
-   [<span data-ttu-id="66244-114">if</span><span class="sxs-lookup"><span data-stu-id="66244-114">if</span></span>](dx-graphics-hlsl-if.md)
-   [<span data-ttu-id="66244-115">switch</span><span class="sxs-lookup"><span data-stu-id="66244-115">switch</span></span>](dx-graphics-hlsl-switch.md)
-   [<span data-ttu-id="66244-116">而</span><span class="sxs-lookup"><span data-stu-id="66244-116">while</span></span>](dx-graphics-hlsl-while.md)

## <a name="related-topics"></a><span data-ttu-id="66244-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="66244-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="66244-118"> (DirectX HLSL 的語言語法) </span><span class="sxs-lookup"><span data-stu-id="66244-118">Language Syntax (DirectX HLSL)</span></span>](dx-graphics-hlsl-language-syntax.md)
</dt> </dl>

 

 





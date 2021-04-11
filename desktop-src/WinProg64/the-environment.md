---
title: 環境
description: 針對64位 Windows 的應用程式開發人員，會發現開發環境與32位 Windows 的開發環境幾乎完全相同。
ms.assetid: 49b2b952-f771-4721-a9b0-01eb67a98007
keywords:
- 開發環境64位 Windows 程式設計
- 環境64位 Windows 程式設計
- 64位 Windows 程式設計指南64位 Windows 程式設計，開發環境
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 104ea1bdacbb478eaa0abcf46d04c3d772540f26
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021117"
---
# <a name="the-environment"></a><span data-ttu-id="65866-106">環境</span><span class="sxs-lookup"><span data-stu-id="65866-106">The Environment</span></span>

<span data-ttu-id="65866-107">針對64位 Windows 的應用程式開發人員，會發現開發環境與32位 Windows 的開發環境幾乎完全相同。</span><span class="sxs-lookup"><span data-stu-id="65866-107">Developers working on applications for 64-bit Windows will find the development environment virtually identical to the development environment for 32-bit Windows.</span></span> <span data-ttu-id="65866-108">在必要時已修改現有的 Api，以允許它們反映其執行所在平臺的精確度。</span><span class="sxs-lookup"><span data-stu-id="65866-108">The existing APIs have been modified where necessary to allow them to reflect the precision of the platform on which they are running.</span></span> <span data-ttu-id="65866-109">結果是簡單的，而且是開發人員的簡短學習曲線，撰寫64位 Windows 的程式碼就像撰寫32位 Windows 的程式碼一樣。</span><span class="sxs-lookup"><span data-stu-id="65866-109">The result is simplicity and a short learning curve for the developer—writing code for 64-bit Windows is just like writing code for 32-bit Windows.</span></span>

<span data-ttu-id="65866-110">Windows 標頭檔支援新的資料類型，可讓指標和指標相關聯的變數反映平臺的精確度。</span><span class="sxs-lookup"><span data-stu-id="65866-110">The Windows header files support new data types that allow pointers and pointer-associated variables to reflect the precision of the platform.</span></span> <span data-ttu-id="65866-111">這表示開發人員可以編譯單一來源基底，以原生方式在32位 Windows 或64位的 Windows 上執行。</span><span class="sxs-lookup"><span data-stu-id="65866-111">This means that developers can compile a single source base to run natively on either 32-bit Windows or 64-bit Windows.</span></span> <span data-ttu-id="65866-112">這項策略可降低開發應用程式的成本，這些應用程式會利用64位硬體，例如 AMD 皓龍或 Athlon64 處理器或 Intel Itanium 處理器。</span><span class="sxs-lookup"><span data-stu-id="65866-112">This strategy reduces the cost of developing applications that leverage 64-bit hardware such as AMD Opteron or Athlon64 processors or Intel Itanium processors.</span></span>

<span data-ttu-id="65866-113">如果您盡速採用新的資料類型慣例，您將有更多時間讓應用程式64位就緒。</span><span class="sxs-lookup"><span data-stu-id="65866-113">You will have more time to make your applications 64-bit ready if you adopt the new data-type conventions as soon as possible.</span></span> <span data-ttu-id="65866-114">如果您要變更程式碼，您應該同時變更資料定義。</span><span class="sxs-lookup"><span data-stu-id="65866-114">If you are changing your code, you should change the data definitions at the same time.</span></span> <span data-ttu-id="65866-115">在32位的 Windows 上測試應用程式、透過64位編譯器執行， ([[工具](the-tools.md) ]) 中所述，而且當您有適當的64位硬體時，應用程式就可以開始測試。</span><span class="sxs-lookup"><span data-stu-id="65866-115">Test the application on 32-bit Windows, run it through the 64-bit compiler (described in [The Tools](the-tools.md)), and the application will be ready to test when you have the appropriate 64-bit hardware.</span></span>

 

 





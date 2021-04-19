---
description: 根據預設，系統會關閉所有 FP 例外狀況。
ms.assetid: efbea036-de9c-4f92-865a-494161da375e
title: 浮點例外狀況
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6a4db92a13a0215bb372db12d30bb11a749a0fc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106984542"
---
# <a name="floating-point-exceptions"></a><span data-ttu-id="79e04-103">浮點例外狀況</span><span class="sxs-lookup"><span data-stu-id="79e04-103">Floating-Point Exceptions</span></span>

<span data-ttu-id="79e04-104">根據預設，系統會關閉所有 FP 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="79e04-104">By default, the system has all FP exceptions turned off.</span></span> <span data-ttu-id="79e04-105">因此，計算結果會是 NAN 或無限大，而不是例外狀況。</span><span class="sxs-lookup"><span data-stu-id="79e04-105">Therefore, computations result in NAN or INFINITY, rather than an exception.</span></span> <span data-ttu-id="79e04-106">在您可以使用結構化例外狀況處理來捕捉浮點數 (FP) 例外狀況之前，您必須呼叫[ \_ controlfp \_ ](/previous-versions/visualstudio/visual-studio-2010/c9676k6h(v=vs.100))的 C 執行時間程式庫函式，以開啟所有可能的 FP 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="79e04-106">Before you can trap floating-point (FP) exceptions using structured exception handling, you must call the [\_controlfp\_s](/previous-versions/visualstudio/visual-studio-2010/c9676k6h(v=vs.100)) C run-time library function to turn on all possible FP exceptions.</span></span> <span data-ttu-id="79e04-107">若只要攔截特定的例外狀況，請只使用對應至要攔截之例外狀況的旗標。</span><span class="sxs-lookup"><span data-stu-id="79e04-107">To trap only particular exceptions, use only the flags that correspond to the exceptions to be trapped.</span></span> <span data-ttu-id="79e04-108">請注意，FP 錯誤的任何處理程式都應該呼叫[ \_ clearfp](/cpp/c-runtime-library/reference/clear87-clearfp?view=vs-2019)做為它的第一個 FP 指令。</span><span class="sxs-lookup"><span data-stu-id="79e04-108">Note that any handler for FP errors should call [\_clearfp](/cpp/c-runtime-library/reference/clear87-clearfp?view=vs-2019) as its first FP instruction.</span></span> <span data-ttu-id="79e04-109">此函式會清除浮點例外狀況。</span><span class="sxs-lookup"><span data-stu-id="79e04-109">This function clears floating-point exceptions.</span></span>

 

 

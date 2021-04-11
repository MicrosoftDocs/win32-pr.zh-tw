---
description: 若要釋放進程的符號處理常式所使用的所有記憶體，請使用 SymCleanup 函數。
ms.assetid: d442b2f2-9225-43fd-bd25-274322857834
title: 符號處理常式清除
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0daea96e780f7e3a685b408c7c774e91b2795b84
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847194"
---
# <a name="symbol-handler-cleanup"></a><span data-ttu-id="bd533-103">符號處理常式清除</span><span class="sxs-lookup"><span data-stu-id="bd533-103">Symbol Handler Cleanup</span></span>

<span data-ttu-id="bd533-104">若要釋放進程的符號處理常式所使用的所有記憶體，請使用 [**SymCleanup**](/windows/desktop/api/Dbghelp/nf-dbghelp-symcleanup) 函數。</span><span class="sxs-lookup"><span data-stu-id="bd533-104">To free all the memory used by the symbol handler for a process, use the [**SymCleanup**](/windows/desktop/api/Dbghelp/nf-dbghelp-symcleanup) function.</span></span> <span data-ttu-id="bd533-105">此函式會列舉所有載入的模組、釋出每個模組，並釋出配置給模組清單的記憶體。</span><span class="sxs-lookup"><span data-stu-id="bd533-105">This function enumerates all loaded modules, frees each module, and frees the memory allocated for the list of modules.</span></span> <span data-ttu-id="bd533-106">呼叫 **SymCleanup** 之後，您就無法在符號處理函式中使用進程控制碼，直到您呼叫 [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) 函式為止。</span><span class="sxs-lookup"><span data-stu-id="bd533-106">After you call **SymCleanup**, you cannot use the process handle in the symbol handling functions until you call the [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) function.</span></span>

 

 




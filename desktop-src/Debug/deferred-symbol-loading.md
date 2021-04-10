---
description: 若要在處理許多符號檔時節省時間和記憶體，請使用 SymSetOptions 函式來設定延遲的符號載入 (SYMOPT \_ 延後 \_ 載入) 選項。
ms.assetid: 40c9384f-00ed-40cd-9687-b76b69e74f87
title: 延遲的符號載入
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d64d05a3ad7ad0fe4017f1ba6fa99625af33c2cc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936044"
---
# <a name="deferred-symbol-loading"></a><span data-ttu-id="4443b-103">延遲的符號載入</span><span class="sxs-lookup"><span data-stu-id="4443b-103">Deferred Symbol Loading</span></span>

<span data-ttu-id="4443b-104">若要節省處理許多符號檔時的時間和記憶體，請使用 [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) 函式來設定延遲的符號載入 (SYMOPT \_ 延 \_ 後載入) 選項，然後使用 [**SymLoadModuleEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) 或 [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) 函式來載入針對所有模組延後的符號。</span><span class="sxs-lookup"><span data-stu-id="4443b-104">To conserve time and memory when working with many symbol files, use the [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) function to set the deferred symbol loading (SYMOPT\_DEFERRED\_LOADS) option, then use the [**SymLoadModuleEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) or [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) function to load symbols deferred for all modules.</span></span> <span data-ttu-id="4443b-105">符號處理常式會列出可用於模組的符號，但在要求之前，不會將偵錯工具資訊對應到記憶體。</span><span class="sxs-lookup"><span data-stu-id="4443b-105">The symbol handler will list symbols that are available for the modules, but will not map the debug information into memory until it is requested.</span></span> <span data-ttu-id="4443b-106">這是有效率地使用偵錯工具符號的慣用方法。</span><span class="sxs-lookup"><span data-stu-id="4443b-106">This is the preferred method to efficiently use debugging symbols.</span></span> <span data-ttu-id="4443b-107">所有使用符號的函式都會受到延遲符號載入的影響。</span><span class="sxs-lookup"><span data-stu-id="4443b-107">All functions that use symbols are affected by deferred symbol loading.</span></span>

 

 




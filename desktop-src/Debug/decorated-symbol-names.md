---
description: 裝飾的符號名稱包含可區分如何宣告公用符號的字元。
ms.assetid: f02fa21d-3fe9-4838-a938-3136c34bc0e8
title: 裝飾符號名稱
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 791fe2220b24dfb73b314a91d1797edd739cb74f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104467952"
---
# <a name="decorated-symbol-names"></a><span data-ttu-id="0dce3-103">裝飾符號名稱</span><span class="sxs-lookup"><span data-stu-id="0dce3-103">Decorated Symbol Names</span></span>

<span data-ttu-id="0dce3-104">裝飾的符號名稱包含可區分如何宣告公用符號的字元。</span><span class="sxs-lookup"><span data-stu-id="0dce3-104">A decorated symbol name includes characters that distinguish how a public symbol has been declared.</span></span> <span data-ttu-id="0dce3-105">針對 stdcall 函式 \_ \_ ，名稱包含 "@" 字元，以及指定其函式參數中位元組數目的十進位數。</span><span class="sxs-lookup"><span data-stu-id="0dce3-105">For \_\_stdcall functions, names include the "@" character and a decimal number that specifies the number of bytes in its function parameters.</span></span> <span data-ttu-id="0dce3-106">例如， [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 函式的裝飾名稱為 LoadLibrary@4 。</span><span class="sxs-lookup"><span data-stu-id="0dce3-106">For example, the decorated name of the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) function is LoadLibrary@4.</span></span> <span data-ttu-id="0dce3-107">針對 c + + 函式，名稱裝飾比較複雜，而且會因編譯器而異。</span><span class="sxs-lookup"><span data-stu-id="0dce3-107">For C++ functions the name decoration is more complex and varies from compiler to compiler.</span></span>

<span data-ttu-id="0dce3-108">若要取出未裝飾的符號名稱，請使用 [**UnDecorateSymbolName**](/windows/desktop/api/Dbghelp/nf-dbghelp-undecoratesymbolname) 函式。</span><span class="sxs-lookup"><span data-stu-id="0dce3-108">To retrieve the undecorated symbol name, use the [**UnDecorateSymbolName**](/windows/desktop/api/Dbghelp/nf-dbghelp-undecoratesymbolname) function.</span></span> <span data-ttu-id="0dce3-109">或者，您也可以呼叫 [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) 函式，要求符號處理常式一律顯示具有未裝飾名稱稱的符號。</span><span class="sxs-lookup"><span data-stu-id="0dce3-109">Alternatively, you can call the [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) function to request that the symbol handler always present symbols with undecorated names.</span></span> <span data-ttu-id="0dce3-110">您必須在載入符號之前設定這個選項，因為符號處理常式會在載入時建立符號名稱資料表。</span><span class="sxs-lookup"><span data-stu-id="0dce3-110">You must set this option before loading the symbols because the symbol handler creates the symbol name tables at load time.</span></span>

 

 

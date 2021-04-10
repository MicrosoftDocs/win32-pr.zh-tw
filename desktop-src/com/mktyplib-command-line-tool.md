---
title: Mktyplib.exe Command-Line 工具
description: Mktyplib.exe 是一種命令列應用程式，可處理 IDL 檔案以產生類型程式庫。 它也可以用來產生 C 或 c + + 標頭檔。
ms.assetid: 883d380d-1d73-439b-9f11-ee89fc62fdfd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abc392351327124777c2d52d0bbe0653853dcb52
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103683192"
---
# <a name="mktyplib-command-line-tool"></a><span data-ttu-id="a4cb5-104">Mktyplib.exe Command-Line 工具</span><span class="sxs-lookup"><span data-stu-id="a4cb5-104">MkTypLib Command-Line Tool</span></span>

<span data-ttu-id="a4cb5-105">\[Mktyplib.exe 工具已淘汰。</span><span class="sxs-lookup"><span data-stu-id="a4cb5-105">\[The Mktyplib.exe tool is obsolete.</span></span> <span data-ttu-id="a4cb5-106">請改用 MIDL 編譯器。</span><span class="sxs-lookup"><span data-stu-id="a4cb5-106">Use the MIDL compiler instead.</span></span> <span data-ttu-id="a4cb5-107">如果您需要與舊有 Automation 程式的回溯相容性，請使用 MIDL 編譯器搭配 **/mktyplib203** 選項。\]</span><span class="sxs-lookup"><span data-stu-id="a4cb5-107">If you need backward compatibility with old Automation programs, use the MIDL compiler with the **/mktyplib203** option.\]</span></span>

<span data-ttu-id="a4cb5-108">Mktyplib.exe 是一種命令列應用程式，可處理 IDL 檔案以產生類型程式庫。</span><span class="sxs-lookup"><span data-stu-id="a4cb5-108">MkTypLib is a command-line application that processes an IDL file to produce a type library.</span></span> <span data-ttu-id="a4cb5-109">它也可以用來產生 C 或 c + + 標頭檔。</span><span class="sxs-lookup"><span data-stu-id="a4cb5-109">It can also be used to generate a C or C++ header file.</span></span>

<span data-ttu-id="a4cb5-110">若要從 ODL 檔產生類型程式庫：</span><span class="sxs-lookup"><span data-stu-id="a4cb5-110">To generate a type library from a ODL file:</span></span>

-   <span data-ttu-id="a4cb5-111">從命令提示字元中，執行下列命令：</span><span class="sxs-lookup"><span data-stu-id="a4cb5-111">From the command prompt, run the following command:</span></span>

    <span data-ttu-id="a4cb5-112">\**mktyplibÂ \* \* \* 檔案名*</span><span class="sxs-lookup"><span data-stu-id="a4cb5-112">\**mktyplibÂ \*\*\*filename*</span></span>

    <span data-ttu-id="a4cb5-113">其中 *filename* 是 ODL 檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="a4cb5-113">where *filename* is the name of the ODL file.</span></span>

<span data-ttu-id="a4cb5-114">Mktyplib.exe 也支援數個選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="a4cb5-114">MkTypLib also supports several optional parameters.</span></span> <span data-ttu-id="a4cb5-115">如需完整清單，請執行下列命令列：</span><span class="sxs-lookup"><span data-stu-id="a4cb5-115">For a complete list, run the following command line:</span></span>

<span data-ttu-id="a4cb5-116">**mktyplib.exe/？**</span><span class="sxs-lookup"><span data-stu-id="a4cb5-116">**mktyplib /?**</span></span>

<span data-ttu-id="a4cb5-117">由於 Mktyplib.exe 是過時的應用程式，因此無法剖析 IDL 檔案或具有在連結 [**庫**](/windows/desktop/Midl/library) 語句之外定義之介面的檔案。</span><span class="sxs-lookup"><span data-stu-id="a4cb5-117">Because MkTypLib is an obsolete application, it cannot parse IDL files or files with interfaces defined outside of a [**library**](/windows/desktop/Midl/library) statement.</span></span> <span data-ttu-id="a4cb5-118">如需詳細資訊，請參閱 [MIDL 與 Mktyplib.exe 之間的差異](/windows/desktop/Midl/differences-between-midl-and-mktyplib)。</span><span class="sxs-lookup"><span data-stu-id="a4cb5-118">For more information, see [Differences Between MIDL and MkTypLib](/windows/desktop/Midl/differences-between-midl-and-mktyplib).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a4cb5-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="a4cb5-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4cb5-120">轉換成 c + +</span><span class="sxs-lookup"><span data-stu-id="a4cb5-120">Translating to C++</span></span>](translating-to-c--.md)
</dt> </dl>

 

 
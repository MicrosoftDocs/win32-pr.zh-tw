---
description: 下列主題描述項號檔和 DbgHelp 函數所提供的功能。
ms.assetid: 1bae2f0a-94a4-4152-bccc-b4deb1291a09
title: 關於 DbgHelp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 634633d44d0c9e8202d99fd16140dd0a506453ec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110332"
---
# <a name="about-dbghelp"></a><span data-ttu-id="c73cb-103">關於 DbgHelp</span><span class="sxs-lookup"><span data-stu-id="c73cb-103">About DbgHelp</span></span>

<span data-ttu-id="c73cb-104">下列主題描述項號檔和 [DbgHelp 函數](dbghelp-functions.md)所提供的功能。</span><span class="sxs-lookup"><span data-stu-id="c73cb-104">The following topics describe symbol files and the functionality provided by the [DbgHelp functions](dbghelp-functions.md).</span></span>

-   [<span data-ttu-id="c73cb-105">DbgHelp 版本</span><span class="sxs-lookup"><span data-stu-id="c73cb-105">DbgHelp Versions</span></span>](dbghelp-versions.md)
-   [<span data-ttu-id="c73cb-106">符號檔</span><span class="sxs-lookup"><span data-stu-id="c73cb-106">Symbol Files</span></span>](symbol-files.md)
-   [<span data-ttu-id="c73cb-107">符號處理</span><span class="sxs-lookup"><span data-stu-id="c73cb-107">Symbol Handling</span></span>](symbol-handling.md)
-   [<span data-ttu-id="c73cb-108">符號伺服器和符號存放區</span><span class="sxs-lookup"><span data-stu-id="c73cb-108">Symbol Servers and Symbol Stores</span></span>](symbol-servers-and-symbol-stores.md)
-   [<span data-ttu-id="c73cb-109">小型傾印檔案</span><span class="sxs-lookup"><span data-stu-id="c73cb-109">Minidump Files</span></span>](minidump-files.md)
-   [<span data-ttu-id="c73cb-110">來源伺服器</span><span class="sxs-lookup"><span data-stu-id="c73cb-110">Source Server</span></span>](source-server-and-source-indexing.md)
-   [<span data-ttu-id="c73cb-111">更新的平臺支援</span><span class="sxs-lookup"><span data-stu-id="c73cb-111">Updated Platform Support</span></span>](updated-platform-support.md)

<span data-ttu-id="c73cb-112">請注意，所有 [DbgHelp 函數](dbghelp-functions.md) 都是單一執行緒。</span><span class="sxs-lookup"><span data-stu-id="c73cb-112">Note that all [DbgHelp functions](dbghelp-functions.md) are single threaded.</span></span> <span data-ttu-id="c73cb-113">因此，從多個執行緒到此函式的呼叫可能會導致非預期的行為或記憶體損毀。</span><span class="sxs-lookup"><span data-stu-id="c73cb-113">Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption.</span></span> <span data-ttu-id="c73cb-114">若要避免這種情況，您必須將多個執行緒的所有並行呼叫，同步處理至此函式。</span><span class="sxs-lookup"><span data-stu-id="c73cb-114">To avoid this, you must synchronize all concurrent calls from more than one thread to this function.</span></span>

 

 




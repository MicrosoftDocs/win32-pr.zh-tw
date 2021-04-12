---
description: 正確設定要進行偵錯工具的符號可能是一項具挑戰性的工作，尤其是針對內核偵錯工具。
ms.assetid: 96b2c9db-58fb-4c28-b17c-3b1cc06ed96b
title: "  符號伺服器和符號存放區"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 644410fcb929308a259c5fc752f55742bfb23bae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104187672"
---
# <a name="symbol-server-and-symbol-stores"></a><span data-ttu-id="a7821-103">  符號伺服器和符號存放區</span><span class="sxs-lookup"><span data-stu-id="a7821-103">Symbol Server and Symbol Stores</span></span>

<span data-ttu-id="a7821-104">正確設定要進行偵錯工具的符號可能是一項具挑戰性的工作，尤其是針對內核偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="a7821-104">Setting up symbols correctly for debugging can be a challenging task, particularly for kernel debugging.</span></span> <span data-ttu-id="a7821-105">它通常會要求您知道電腦上所有產品的名稱和版本。</span><span class="sxs-lookup"><span data-stu-id="a7821-105">It often requires that you know the names and releases of all products on your computer.</span></span> <span data-ttu-id="a7821-106">偵錯工具必須能夠找出對應于每個產品版本和 service pack 的符號檔。</span><span class="sxs-lookup"><span data-stu-id="a7821-106">The debugger must be able to locate the symbol files that correspond to each product release and service pack.</span></span> <span data-ttu-id="a7821-107">這可能會產生非常長的符號路徑，其中包含長清單的目錄。</span><span class="sxs-lookup"><span data-stu-id="a7821-107">This can result in an extremely long symbol path consisting of a long list of directories.</span></span>

<span data-ttu-id="a7821-108">若要簡化協調符號檔的這些問題，請使用 *符號伺服器*。</span><span class="sxs-lookup"><span data-stu-id="a7821-108">To simplify these difficulties in coordinating symbol files, use the *symbol server*.</span></span> <span data-ttu-id="a7821-109">符號伺服器可讓偵錯工具自動取得正確的符號檔，而不包含產品名稱、版本或組建編號。</span><span class="sxs-lookup"><span data-stu-id="a7821-109">The symbol server enables the debuggers to automatically retrieve the correct symbol files without product names, releases, or build numbers.</span></span> <span data-ttu-id="a7821-110">適用于 Windows 的偵錯工具包含 SymSrv 符號伺服器。</span><span class="sxs-lookup"><span data-stu-id="a7821-110">Debugging Tools for Windows contains the SymSrv symbol server.</span></span>

<span data-ttu-id="a7821-111">符號伺服器的啟用方式是在符號路徑中包含特定文字字串。</span><span class="sxs-lookup"><span data-stu-id="a7821-111">The symbol server is activated by including a certain text string in the symbol path.</span></span> <span data-ttu-id="a7821-112">每次偵錯工具需要載入新載入模組的符號時，就會呼叫符號伺服器以找出適當的符號檔。</span><span class="sxs-lookup"><span data-stu-id="a7821-112">Each time the debugger needs to load symbols for a newly loaded module, it calls the symbol server to locate the appropriate symbol files.</span></span> <span data-ttu-id="a7821-113">符號伺服器會在 *符號存放區* 中尋找檔案。</span><span class="sxs-lookup"><span data-stu-id="a7821-113">The symbol server locates the files in a *symbol store*.</span></span> <span data-ttu-id="a7821-114">這是符號檔、索引和工具的集合，可供系統管理員用來新增及刪除檔案。</span><span class="sxs-lookup"><span data-stu-id="a7821-114">This is a collection of symbol files, an index, and a tool that can be used by an administrator to add and delete files.</span></span> <span data-ttu-id="a7821-115">這些檔案會根據唯一的參數（例如時間戳記和影像大小）進行索引。</span><span class="sxs-lookup"><span data-stu-id="a7821-115">The files are indexed according to unique parameters such as the time stamp and image size.</span></span> <span data-ttu-id="a7821-116">適用于 Windows 的偵錯工具包含名為 SymStore 的符號存放區工具。</span><span class="sxs-lookup"><span data-stu-id="a7821-116">Debugging Tools for Windows contains a symbol store tool called SymStore.</span></span>

<span data-ttu-id="a7821-117">如需詳細資訊，請參閱</span><span class="sxs-lookup"><span data-stu-id="a7821-117">For more information, see:</span></span>

-   [<span data-ttu-id="a7821-118">使用 SymSrv</span><span class="sxs-lookup"><span data-stu-id="a7821-118">Using SymSrv</span></span>](using-symsrv.md)
-   [<span data-ttu-id="a7821-119">使用 SymStore</span><span class="sxs-lookup"><span data-stu-id="a7821-119">Using SymStore</span></span>](using-symstore.md)
-   [<span data-ttu-id="a7821-120">使用其他符號存放區</span><span class="sxs-lookup"><span data-stu-id="a7821-120">Using Other Symbol Stores</span></span>](using-other-symbol-stores.md)
-   [<span data-ttu-id="a7821-121">SymStore Command-Line 選項</span><span class="sxs-lookup"><span data-stu-id="a7821-121">SymStore Command-Line Options</span></span>](symstore-command-line-options.md)
-   [<span data-ttu-id="a7821-122">符號伺服器和網際網路防火牆</span><span class="sxs-lookup"><span data-stu-id="a7821-122">Symbol Server and Internet Firewalls</span></span>](symbol-servers-and-internet-firewalls.md)

## <a name="related-topics"></a><span data-ttu-id="a7821-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="a7821-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a7821-124">符號檔</span><span class="sxs-lookup"><span data-stu-id="a7821-124">Symbol Files</span></span>](symbol-files.md)
</dt> </dl>

 

 




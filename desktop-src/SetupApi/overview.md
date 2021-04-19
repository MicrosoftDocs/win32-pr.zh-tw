---
description: " (API) 的設定應用程式開發介面提供一組功能，讓您的安裝應用程式可以呼叫這些函式來執行安裝作業。 這些安裝函式適用于 Windows INF 檔案，以提供下列安裝程式功能。"
ms.assetid: 58201596-cb8c-480a-abef-896c1f9ef098
title: 概觀
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a32b99c6079fdb61fd6bfd0033ffccb9ebb7b922
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971847"
---
# <a name="overview"></a><span data-ttu-id="83e0a-104">概觀</span><span class="sxs-lookup"><span data-stu-id="83e0a-104">Overview</span></span>

<span data-ttu-id="83e0a-105"> (API) 的設定應用程式開發介面提供一組功能，讓您的安裝應用程式可以呼叫這些函式來執行安裝作業。</span><span class="sxs-lookup"><span data-stu-id="83e0a-105">The Setup application programming interface (API) provides a set of functions that your setup application can call to perform installation operations.</span></span> <span data-ttu-id="83e0a-106">這些安裝函式適用于 Windows INF 檔案，以提供下列安裝程式功能。</span><span class="sxs-lookup"><span data-stu-id="83e0a-106">These setup functions work with Windows INF files to provide the following setup functionality.</span></span>



| <span data-ttu-id="83e0a-107">如需下列資訊</span><span class="sxs-lookup"><span data-stu-id="83e0a-107">For information about</span></span>                       | <span data-ttu-id="83e0a-108">請參閱</span><span class="sxs-lookup"><span data-stu-id="83e0a-108">See</span></span>                                                                                                                                                                         |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83e0a-109">佇列檔</span><span class="sxs-lookup"><span data-stu-id="83e0a-109">Queuing files</span></span>                               | [<span data-ttu-id="83e0a-110">檔案佇列</span><span class="sxs-lookup"><span data-stu-id="83e0a-110">File Queues</span></span>](file-queues.md)                                                                                                                                              |
| <span data-ttu-id="83e0a-111">安裝檔案</span><span class="sxs-lookup"><span data-stu-id="83e0a-111">Installing files</span></span>                            | [<span data-ttu-id="83e0a-112">檔案佇列</span><span class="sxs-lookup"><span data-stu-id="83e0a-112">File Queues</span></span>](file-queues.md)<br/> [<span data-ttu-id="83e0a-113">設定應用程式</span><span class="sxs-lookup"><span data-stu-id="83e0a-113">Setup Applications</span></span>](setup-applications.md)<br/> [<span data-ttu-id="83e0a-114">建立安裝程式應用程式</span><span class="sxs-lookup"><span data-stu-id="83e0a-114">Creating Setup Applications</span></span>](creating-setup-applications.md)<br/> |
| <span data-ttu-id="83e0a-115">處理錯誤並提示媒體</span><span class="sxs-lookup"><span data-stu-id="83e0a-115">Handling errors and prompting for media</span></span>     | [<span data-ttu-id="83e0a-116">磁片提示和錯誤處理</span><span class="sxs-lookup"><span data-stu-id="83e0a-116">Disk Prompting and Error Handling</span></span>](disk-prompting-and-error-handling.md)                                                                                                  |
| <span data-ttu-id="83e0a-117">更新登錄專案</span><span class="sxs-lookup"><span data-stu-id="83e0a-117">Updating registry entries</span></span>                   | [<span data-ttu-id="83e0a-118">設定應用程式</span><span class="sxs-lookup"><span data-stu-id="83e0a-118">Setup Applications</span></span>](setup-applications.md)                                                                                                                                |
| <span data-ttu-id="83e0a-119">記錄已安裝的檔案</span><span class="sxs-lookup"><span data-stu-id="83e0a-119">Logging installed files</span></span>                     | [<span data-ttu-id="83e0a-120">檔案記錄檔</span><span class="sxs-lookup"><span data-stu-id="83e0a-120">File Log</span></span>](file-log.md)                                                                                                                                                    |
| <span data-ttu-id="83e0a-121">儲存最近使用的來源路徑</span><span class="sxs-lookup"><span data-stu-id="83e0a-121">Storing the most recently used source paths</span></span> | [<span data-ttu-id="83e0a-122">MRU 來源清單</span><span class="sxs-lookup"><span data-stu-id="83e0a-122">MRU Source List</span></span>](mru-source-list.md)                                                                                                                                      |



 

<span data-ttu-id="83e0a-123">Unicode 和 ANSI 版本適用于大部分的設定函數。</span><span class="sxs-lookup"><span data-stu-id="83e0a-123">Unicode and ANSI versions are available for most setup functions.</span></span> <span data-ttu-id="83e0a-124">Unicode 文字檔應該包含標準0xFEFF 位元組順序標記，才能讓安裝函式將檔案識別為 Unicode 文字。</span><span class="sxs-lookup"><span data-stu-id="83e0a-124">Unicode text files should contain the standard 0xFEFF byte-order mark to enable setup functions to identify the file as Unicode text.</span></span>

<span data-ttu-id="83e0a-125">雖然安裝程式 API 支援提示輸入新的媒體和基本的錯誤處理對話方塊，但安裝函式不會提供 wizard 功能或一般使用者介面。</span><span class="sxs-lookup"><span data-stu-id="83e0a-125">Although the Setup API supports prompting for new media and basic error-handling dialog boxes, the setup functions do not provide wizard functionality or a generic user interface.</span></span>

<span data-ttu-id="83e0a-126">開發人員應考慮是否可以使用 [Windows Installer](/windows/desktop/Msi/windows-installer-portal) 安裝其應用程式，而不是安裝程式 API。</span><span class="sxs-lookup"><span data-stu-id="83e0a-126">Developers should consider whether they can use [Windows Installer](/windows/desktop/Msi/windows-installer-portal) to install their applications rather than the Setup API.</span></span> <span data-ttu-id="83e0a-127">Windows Installer 藉由讓客戶有效率地安裝及設定您的產品和應用程式，以降低其擁有權 (TCO) 的擁有權總成本。</span><span class="sxs-lookup"><span data-stu-id="83e0a-127">Windows Installer reduces the total cost of ownership (TCO) for your customers by enabling them to efficiently install and configure your products and applications.</span></span> <span data-ttu-id="83e0a-128">安裝程式也可以為您的產品提供新功能，以在不安裝的情況下通告功能、隨選安裝產品，以及新增使用者自訂。</span><span class="sxs-lookup"><span data-stu-id="83e0a-128">The installer can also provide your product with new capabilities to advertise features without installing them, to install products on-demand, and to add user customizations.</span></span>

 


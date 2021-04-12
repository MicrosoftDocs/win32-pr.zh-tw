---
description: Windows Installer 會使用 Microsoft .NET Framework 將 common language runtime 元件安裝到全域組件快取中。
ms.assetid: 21d535d5-f05b-411a-8719-2662e6046fbd
title: 將元件安裝到全域組件快取
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 719be313ad74374950092936bbd6124da779a0db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191741"
---
# <a name="installation-of-assemblies-to-the-global-assembly-cache"></a><span data-ttu-id="72295-103">將元件安裝到全域組件快取</span><span class="sxs-lookup"><span data-stu-id="72295-103">Installation of Assemblies to the Global Assembly Cache</span></span>

<span data-ttu-id="72295-104">Windows Installer 會使用 Microsoft .NET Framework 將 common language runtime 元件安裝到全域組件快取中。</span><span class="sxs-lookup"><span data-stu-id="72295-104">The Windows Installer installs common language runtime assemblies into the global assembly cache using the Microsoft .NET Framework.</span></span> <span data-ttu-id="72295-105">將元件安裝到全域組件快取時，安裝程式在安裝一般 Windows Installer 元件時，無法使用它所使用的相同目錄結構和檔案版本規則。</span><span class="sxs-lookup"><span data-stu-id="72295-105">When installing assemblies to the global assembly cache, the installer cannot use the same directory structure and file version rules it uses when installing regular Windows Installer components.</span></span> <span data-ttu-id="72295-106">標準 Windows Installer 元件可能會依不同的產品安裝到多個目錄位置。</span><span class="sxs-lookup"><span data-stu-id="72295-106">Regular Windows Installer components may be installed into multiple directory locations by different products.</span></span> <span data-ttu-id="72295-107">元件只能存在於組件快取中。</span><span class="sxs-lookup"><span data-stu-id="72295-107">Assemblies can exist only once in the assembly cache.</span></span> <span data-ttu-id="72295-108">每個元件都會從元件快取中新增和移除，以做為不可分割的整體;因此，一律會同時安裝或移除組成元件的所有檔案。</span><span class="sxs-lookup"><span data-stu-id="72295-108">Each assembly is added and removed from the assembly cache as an indivisible whole; therefore, all the files comprising an assembly are always installed or removed together.</span></span>

<span data-ttu-id="72295-109">標準 Windows Installer 元件和 common language runtime 元件的磁片成本，會以不同的方式計算。</span><span class="sxs-lookup"><span data-stu-id="72295-109">The disk cost of regular Windows Installer components and common language runtime assemblies are calculated differently.</span></span> <span data-ttu-id="72295-110">一般 Windows Installer 元件的總磁片成本包括本地成本、來源成本和移除成本。</span><span class="sxs-lookup"><span data-stu-id="72295-110">The total disk cost of a regular Windows Installer component includes local costs, source costs, and removal costs.</span></span> <span data-ttu-id="72295-111">如需詳細資訊，請參閱檔案 [成本](file-costing.md)。</span><span class="sxs-lookup"><span data-stu-id="72295-111">For details, see [File Costing](file-costing.md).</span></span> <span data-ttu-id="72295-112">這個方法不能用來產生 common language runtime 元件的成本，因為這些元件可能會有 Windows Installer 以外的用戶端。</span><span class="sxs-lookup"><span data-stu-id="72295-112">This method cannot be used to cost common language runtime assemblies because these may have clients other than the Windows Installer.</span></span> <span data-ttu-id="72295-113">Common language runtime 元件的成本必須透過查詢 Microsoft .NET Framework common language runtime 來決定。</span><span class="sxs-lookup"><span data-stu-id="72295-113">The cost of common language runtime assemblies must be determined by querying the Microsoft .NET Framework common language runtime.</span></span>

<span data-ttu-id="72295-114">Windows Installer 會使用兩步驟的交易式程式來安裝包含 common language runtime 元件的產品。</span><span class="sxs-lookup"><span data-stu-id="72295-114">The Windows Installer uses a two-step transactional process to install products containing common language runtime assemblies.</span></span> <span data-ttu-id="72295-115">這會啟用元件安裝和移除的復原。</span><span class="sxs-lookup"><span data-stu-id="72295-115">This enables the rollback of assembly installation and removal.</span></span> <span data-ttu-id="72295-116">如需詳細資訊，請參閱 [全域組件快取中的元件回復](rollback-of-assemblies-in-the-global-assembly-cache.md)。</span><span class="sxs-lookup"><span data-stu-id="72295-116">For more information, see [Rollback of Assemblies in the Global Assembly Cache](rollback-of-assemblies-in-the-global-assembly-cache.md).</span></span>

<span data-ttu-id="72295-117">請注意，安裝在每個使用者 [安裝內容](installation-context.md) 中之全域組件快取的元件，不受 Windows 檔案保護的保護。</span><span class="sxs-lookup"><span data-stu-id="72295-117">Note that assemblies installed to the global assembly cache by an installation in the per-user [installation context](installation-context.md) are not protected by Windows File Protection.</span></span> <span data-ttu-id="72295-118">在每部電腦安裝內容中，安裝安裝到全域組件快取的元件會受到 [Windows 資源保護](../wfp/windows-resource-protection-portal.md)的保護。</span><span class="sxs-lookup"><span data-stu-id="72295-118">Assemblies that are installed to the global assembly cache by an installation in the per-machine installation context are protected by [Windows Resource Protection](../wfp/windows-resource-protection-portal.md).</span></span>

 

 

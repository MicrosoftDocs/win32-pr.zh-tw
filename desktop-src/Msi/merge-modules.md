---
description: 合併模組提供一種標準方法，讓開發人員將共用 Windows Installer 元件和設定邏輯提供給其應用程式。
ms.assetid: 673de3ff-e58c-4153-9c8d-c3baebba5eb1
title: 合併模組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3499368b309909bcb06da45476d43d8cac28e205
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195088"
---
# <a name="merge-modules"></a><span data-ttu-id="bcc42-103">合併模組</span><span class="sxs-lookup"><span data-stu-id="bcc42-103">Merge Modules</span></span>

<span data-ttu-id="bcc42-104">合併模組提供一種標準方法，讓開發人員將共用 Windows Installer [*元件*](c-gly.md) 和設定邏輯提供給其應用程式。</span><span class="sxs-lookup"><span data-stu-id="bcc42-104">Merge modules provide a standard method by which developers deliver shared Windows Installer [*components*](c-gly.md) and setup logic to their applications.</span></span> <span data-ttu-id="bcc42-105">合併模組是用來將共用程式碼、檔案、資源、登錄專案和安裝程式邏輯傳遞給應用程式，做為單一複合檔案。</span><span class="sxs-lookup"><span data-stu-id="bcc42-105">Merge modules are used to deliver shared code, files, resources, registry entries, and setup logic to applications as a single compound file.</span></span> <span data-ttu-id="bcc42-106">撰寫新合併模組或使用現有合併模組的開發人員，應該遵循本節所述的標準。</span><span class="sxs-lookup"><span data-stu-id="bcc42-106">Developers authoring new merge modules or using existing merge modules should follow the standard outlined in this section.</span></span>

<span data-ttu-id="bcc42-107">合併模組在結構上類似于簡化的 Windows Installer [*.msi*](m-gly.md)檔。</span><span class="sxs-lookup"><span data-stu-id="bcc42-107">A merge module is similar in structure to a simplified Windows Installer [*.msi file*](m-gly.md).</span></span> <span data-ttu-id="bcc42-108">不過，合併模組無法單獨安裝，它必須使用合併工具合併到安裝套件中。</span><span class="sxs-lookup"><span data-stu-id="bcc42-108">However, a merge module cannot be installed alone, it must be merged into an installation package using a merge tool.</span></span> <span data-ttu-id="bcc42-109">想要使用合併模組的開發人員必須取得其中一個自由散發的合併工具，例如 Mergemod.dll，或向獨立軟體廠商購買合併工具。</span><span class="sxs-lookup"><span data-stu-id="bcc42-109">Developers wanting to use merge modules must obtain one of the freely distributed merge tools, such as Mergemod.dll, or purchase a merge tool from an independent software vendor.</span></span> <span data-ttu-id="bcc42-110">開發人員可以使用許多用來建立 Windows Installer 安裝套件的相同軟體工具來建立新的合併模組，例如 Windows Installer SDK 所提供的資料庫資料表編輯器 Orca。</span><span class="sxs-lookup"><span data-stu-id="bcc42-110">Developers can create new merge modules by using many of the same software tools used to create a Windows Installer installation package, such as the database table editor Orca provided with the Windows Installer SDK.</span></span>

<span data-ttu-id="bcc42-111">合併模組合併到應用程式的 .msi 檔案時，安裝合併模組所提供的元件所需的所有資訊和資源都會併入應用程式的 .msi 檔案中。</span><span class="sxs-lookup"><span data-stu-id="bcc42-111">When a merge module is merged into the .msi file of an application, all the information and resources required to install the components delivered by the merge module are incorporated into the application's .msi file.</span></span> <span data-ttu-id="bcc42-112">然後再也不需要合併模組來安裝這些元件，而且使用者不需要再存取合併模組。</span><span class="sxs-lookup"><span data-stu-id="bcc42-112">The merge module is then no longer required to install these components and the merge module does not need to be accessible to a user.</span></span> <span data-ttu-id="bcc42-113">由於安裝元件所需的所有資訊都是以單一檔案的形式提供，因此使用合併模組可以排除許多版本衝突實例、遺失登錄專案，以及不正確安裝的檔案。</span><span class="sxs-lookup"><span data-stu-id="bcc42-113">Because all the information needed to install the components is delivered as a single file, the use of merge modules can eliminate many instances of version conflicts, missing registry entries, and improperly installed files.</span></span>

<span data-ttu-id="bcc42-114">如需合併模組的詳細資訊，請參閱：</span><span class="sxs-lookup"><span data-stu-id="bcc42-114">For more information about merge modules, see:</span></span>

-   [<span data-ttu-id="bcc42-115">關於合併模組</span><span class="sxs-lookup"><span data-stu-id="bcc42-115">About Merge Modules</span></span>](about-merge-modules.md)
-   [<span data-ttu-id="bcc42-116">使用合併模組</span><span class="sxs-lookup"><span data-stu-id="bcc42-116">Using Merge Modules</span></span>](using-merge-modules.md)
-   [<span data-ttu-id="bcc42-117">合併模組參考</span><span class="sxs-lookup"><span data-stu-id="bcc42-117">Merge Module Reference</span></span>](merge-module-reference.md)

 

 




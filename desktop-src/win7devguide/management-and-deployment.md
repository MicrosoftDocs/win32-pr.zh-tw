---
title: 管理和部署
description: 準備部署 Windows 7 的 IT 專業人員或開發人員將獲得更高的信心，並體驗較短的評估週期，因為映射功能和工具的改進。
ms.assetid: 217090c4-6385-4333-a380-f75f2c80e369
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 105b19ad01cb9208d05e77871be637fdadcb0532
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933386"
---
# <a name="management-and-deployment"></a><span data-ttu-id="87fdc-103">管理和部署</span><span class="sxs-lookup"><span data-stu-id="87fdc-103">Management and Deployment</span></span>

<span data-ttu-id="87fdc-104">準備部署 Windows 7 的 IT 專業人員或開發人員將獲得更高的信心，並體驗較短的評估週期，因為映射功能和工具的改進。</span><span class="sxs-lookup"><span data-stu-id="87fdc-104">IT professionals or developers preparing to deploy Windows 7 will have increased confidence and experience a shorter evaluation cycle because of improvements in imaging features and tools.</span></span> <span data-ttu-id="87fdc-105">這些功能包括支援管理離線影像檔案中的應用程式、驅動程式和作業系統。</span><span class="sxs-lookup"><span data-stu-id="87fdc-105">These include support for managing applications, drivers, and operating systems in offline image files.</span></span> <span data-ttu-id="87fdc-106">此外，映射的建立和管理作業也比較簡單，而且可供更廣泛的 IT 組織使用。</span><span class="sxs-lookup"><span data-stu-id="87fdc-106">Additionally, image creation and management will be easier and will be available to a broader range of IT organizations.</span></span> <span data-ttu-id="87fdc-107">因為新的 IT 遷移工具和自動化的部署技術，所以將 Windows 7 部署到商務電腦也變得更容易且更快。</span><span class="sxs-lookup"><span data-stu-id="87fdc-107">Deploying Windows 7 to business computers will also be easier and faster because of new IT migration tools and automated deployment technologies.</span></span>

## <a name="windows-powershell-20"></a><span data-ttu-id="87fdc-108">Windows PowerShell 2.0</span><span class="sxs-lookup"><span data-stu-id="87fdc-108">Windows PowerShell 2.0</span></span>

<span data-ttu-id="87fdc-109">PowerShell 是一種完整的 Microsoft .NET managed 指令碼語言，同時具有互動式命令列介面和圖形化的腳本環境 (ISE) 。</span><span class="sxs-lookup"><span data-stu-id="87fdc-109">PowerShell is a complete Microsoft .NET managed scripting language that has both an interactive command line shell and a graphical Integrated Scripting Environment (ISE).</span></span> <span data-ttu-id="87fdc-110">它支援分支、迴圈、函數、調試、例外狀況處理和國際化。</span><span class="sxs-lookup"><span data-stu-id="87fdc-110">It supports branching, looping, functions, debugging, exception handling, and internationalization.</span></span> <span data-ttu-id="87fdc-111">PowerShell 2.0 是 Windows 7 的一部分，可針對 Windows 診斷、Microsoft Active Directory、Microsoft Internet Information Services (IIS) 等，提供許多增強功能和一組持續成長的 *Cmdlet* 。</span><span class="sxs-lookup"><span data-stu-id="87fdc-111">PowerShell 2.0 is part of Windows 7 and delivers many enhancements and a growing set of *cmdlets* for Windows Diagnostics, Microsoft Active Directory, Microsoft Internet Information Services (IIS) and more.</span></span>

<span data-ttu-id="87fdc-112">PowerShell 2.0 遠端功能現在可讓使用者在一部或多部遠端電腦上，從執行 PowerShell 的單一電腦上執行命令。</span><span class="sxs-lookup"><span data-stu-id="87fdc-112">The PowerShell 2.0 remoting feature now allows users to run commands on one or more remote computers from a single computer that is running PowerShell.</span></span> <span data-ttu-id="87fdc-113">開發人員也可以在 IIS 上裝載 PowerShell 來存取及管理其伺服器。</span><span class="sxs-lookup"><span data-stu-id="87fdc-113">Developers can also host PowerShell on IIS to access and manage their servers.</span></span>

<span data-ttu-id="87fdc-114">PowerShell 2.0 支援使用模組來分割和組織 PowerShell 腳本，這些模組可以散發和部署為獨立、可重複使用的單位。</span><span class="sxs-lookup"><span data-stu-id="87fdc-114">PowerShell 2.0 supports partitioning and organizing PowerShell scripts by using modules that can be distributed and deployed as self-contained, reusable units.</span></span> <span data-ttu-id="87fdc-115">它也包含 PowerShell 引擎和 Api 中的交易支援，這表示開發人員可以使用內建的交易 *Cmdlet* 來啟動、認可和回復交易。</span><span class="sxs-lookup"><span data-stu-id="87fdc-115">It also includes transactions support in the PowerShell engine and APIs, which means that developers can start, commit, and rollback transactions by using built-in transaction *cmdlets*.</span></span> <span data-ttu-id="87fdc-116">此外，PowerShell 引擎包含事件支援來接聽、轉送和處理管理和系統事件。</span><span class="sxs-lookup"><span data-stu-id="87fdc-116">Further, the PowerShell engine includes eventing support for listening, forwarding, and acting on management and system events.</span></span> <span data-ttu-id="87fdc-117">您可以撰寫 PowerShell 應用程式來訂閱特定事件以進行同步或非同步處理。</span><span class="sxs-lookup"><span data-stu-id="87fdc-117">PowerShell applications can be written to subscribe to certain events for synchronous or asynchronous processing.</span></span> <span data-ttu-id="87fdc-118"> (參閱 [Windows PowerShell](https://msdn.microsoft.com/library/bb905330.aspx)。 ) </span><span class="sxs-lookup"><span data-stu-id="87fdc-118">(See [Windows PowerShell](https://msdn.microsoft.com/library/bb905330.aspx).)</span></span>

![windows powershell ise 螢幕擷取畫面](images/windows7-devguide-solidfig1-powershell.jpg)

<span data-ttu-id="87fdc-120">圖 1.</span><span class="sxs-lookup"><span data-stu-id="87fdc-120">Figure 1.</span></span> <span data-ttu-id="87fdc-121">Windows PowerShell 是完整的 .NET managed 指令碼語言，同時具有互動式命令列 shell 和圖形 ISE</span><span class="sxs-lookup"><span data-stu-id="87fdc-121">Windows PowerShell is a complete .NET managed scripting language that has both an interactive command line shell and a graphical ISE</span></span>

## <a name="windows-installer"></a><span data-ttu-id="87fdc-122">Windows Installer</span><span class="sxs-lookup"><span data-stu-id="87fdc-122">Windows Installer</span></span>

<span data-ttu-id="87fdc-123">Windows Installer 已更新，藉由減少建立安裝套件所需的自訂程式碼數量，並建立真正的每個使用者軟體安裝，來提高開發人員的效率。</span><span class="sxs-lookup"><span data-stu-id="87fdc-123">Windows Installer has been updated to increase developer efficiency by reducing the amount of custom code that is required to create an installation package and create true per-user software installations.</span></span>

<span data-ttu-id="87fdc-124">多個封裝交易可讓開發人員使用 ' chainer '，以動態方式將封裝包含在交易中，以從多個封裝建立單一交易。</span><span class="sxs-lookup"><span data-stu-id="87fdc-124">Multiple Package Transaction allows developers to create a single transaction from multiple packages by using a 'chainer' to dynamically include packages in the transaction.</span></span> <span data-ttu-id="87fdc-125">如果有一或多個套件未如預期般安裝，只要復原安裝即可。</span><span class="sxs-lookup"><span data-stu-id="87fdc-125">If one or more of the packages do not install as expected, just roll back the installation.</span></span>

<span data-ttu-id="87fdc-126">內嵌 UI 處理常式使自訂 Ui 更容易整合，方法是在 Windows Installer 套件中內嵌自訂使用者介面處理常式。</span><span class="sxs-lookup"><span data-stu-id="87fdc-126">Embedded UI Handler makes custom UIs easier to integrate by embedding a custom user interface handler in the Windows Installer package.</span></span>

<span data-ttu-id="87fdc-127">內嵌的多套件 Chainer 可讓開發人員在多個套件之間啟用安裝事件。</span><span class="sxs-lookup"><span data-stu-id="87fdc-127">Embedded Multiple Package Chainer allows developers to enable installation events across multiple packages.</span></span> <span data-ttu-id="87fdc-128">例如，他們可以啟用隨選安裝事件、修復事件，以及在多個套件之間卸載事件。</span><span class="sxs-lookup"><span data-stu-id="87fdc-128">For example, they can enable install-on-demand events, repair events, and uninstall events across multiple packages.</span></span>

<span data-ttu-id="87fdc-129">新功能也可讓您建立真正的每一使用者安裝，包括支援每個使用者的程式檔案和「立即提升」功能，並透過部署映射服務與管理提供離線軟體清查和修補適用性檢查的支援。</span><span class="sxs-lookup"><span data-stu-id="87fdc-129">New features also enable the creation of true per-user installations, including support for per-user program files and "elevate now" functionality, and provide support for offline software inventory and patch applicability checks through Deployment Image Servicing and Management.</span></span> <span data-ttu-id="87fdc-130"> (瞭解 [Windows Installer 5.0 中的新功能](../msi/what-s-new-in-windows-installer-5-0.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="87fdc-130">(See [What's New in Windows Installer 5.0](../msi/what-s-new-in-windows-installer-5-0.md).)</span></span>

 

 
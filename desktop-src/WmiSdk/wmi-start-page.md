---
description: Windows Management Instrumentation (WMI) 是在以 Windows 為基礎的作業系統上管理資料和作業的基礎結構。
ms.assetid: 4804152f-2042-4c6a-83c6-75c5e1ab7a04
ms.tgt_platform: multiple
title: Windows Management Instrumentation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ec2313ca7ee744ebe6f14be42a33e2e5878960b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983427"
---
# <a name="windows-management-instrumentation"></a><span data-ttu-id="8fcb3-103">Windows Management Instrumentation</span><span class="sxs-lookup"><span data-stu-id="8fcb3-103">Windows Management Instrumentation</span></span>

## <a name="purpose"></a><span data-ttu-id="8fcb3-104">目的</span><span class="sxs-lookup"><span data-stu-id="8fcb3-104">Purpose</span></span>

<span data-ttu-id="8fcb3-105">Windows Management Instrumentation (WMI) 是在以 Windows 為基礎的作業系統上管理資料和作業的基礎結構。</span><span class="sxs-lookup"><span data-stu-id="8fcb3-105">Windows Management Instrumentation (WMI) is the infrastructure for management data and operations on Windows-based operating systems.</span></span> <span data-ttu-id="8fcb3-106">您可以撰寫 WMI 腳本或應用程式將遠端電腦上的系統管理工作自動化，但是 WMI 也會提供管理資料給作業系統和產品的其他部分，例如 System Center Operations Manager、先前 Microsoft Operations Manager (MOM) 或 Windows 遠端管理 [WinRM](/windows/desktop/WinRM/portal) (。</span><span class="sxs-lookup"><span data-stu-id="8fcb3-106">You can write WMI scripts or applications to automate administrative tasks on remote computers but WMI also supplies management data to other parts of the operating system and products, for example System Center Operations Manager, formerly Microsoft Operations Manager (MOM), or Windows Remote Management ([WinRM](/windows/desktop/WinRM/portal)).</span></span>

> [!Note]  
> <span data-ttu-id="8fcb3-107">下列檔的目標是開發人員和 IT 系統管理員。</span><span class="sxs-lookup"><span data-stu-id="8fcb3-107">The following documentation is targeted for developers and IT administrators.</span></span> <span data-ttu-id="8fcb3-108">如果您是遇到關於 WMI 的錯誤訊息的使用者，您應該移至 [Microsoft 支援服務](https://support.microsoft.com/) 並搜尋錯誤訊息上所看到的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="8fcb3-108">If you are an end-user that has experienced an error message concerning WMI, you should go to [Microsoft Support](https://support.microsoft.com/) and search for the error code you see on the error message.</span></span> <span data-ttu-id="8fcb3-109">如需有關疑難排解 WMI 腳本和 WMI 服務問題的詳細資訊，請參閱 [Wmi 無法運作！](/previous-versions/tn-archive/ff406382(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="8fcb3-109">For more information about troubleshooting problems with WMI scripts and the WMI service, see [WMI Isn't Working!](/previous-versions/tn-archive/ff406382(v=msdn.10))</span></span>

 

> [!Note]  
> <span data-ttu-id="8fcb3-110">Microsoft 完全支援 WMI;不過，您可以透過 Windows 管理基礎結構 (MI) 來取得最新版本的系統管理腳本和控制項。</span><span class="sxs-lookup"><span data-stu-id="8fcb3-110">WMI is fully supported by Microsoft; however, the latest version of administrative scripting and control is available through the Windows Management Infrastructure (MI).</span></span> <span data-ttu-id="8fcb3-111">MI 與舊版 WMI 完全相容，並提供一系列的功能和優點，讓設計和開發提供者和用戶端比以往更容易。</span><span class="sxs-lookup"><span data-stu-id="8fcb3-111">MI is fully compatible with previous versions of WMI, and provides a host of features and benefits that make designing and developing providers and clients easier than ever.</span></span> <span data-ttu-id="8fcb3-112">如需詳細資訊，請參閱 [Windows 管理基礎結構 (MI) ](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure)。</span><span class="sxs-lookup"><span data-stu-id="8fcb3-112">For more information, see [Windows Management Infrastructure (MI)](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure).</span></span>

 

## <a name="where-applicable"></a><span data-ttu-id="8fcb3-113">適用時</span><span class="sxs-lookup"><span data-stu-id="8fcb3-113">Where applicable</span></span>

<span data-ttu-id="8fcb3-114">WMI 可以用在所有 Windows 應用程式中，最適合用於企業應用程式和系統管理腳本。</span><span class="sxs-lookup"><span data-stu-id="8fcb3-114">WMI can be used in all Windows-based applications, and is most useful in enterprise applications and administrative scripts.</span></span>

<span data-ttu-id="8fcb3-115">系統管理員可以在 TechNet [ScriptCenter](https://www.microsoft.com/technet/scriptcenter/default.mspx)找到有關使用 wmi 的資訊，以及有關 wmi 的各種書籍。</span><span class="sxs-lookup"><span data-stu-id="8fcb3-115">System administrators can find information about using WMI at the TechNet [ScriptCenter](https://www.microsoft.com/technet/scriptcenter/default.mspx), and in various books about WMI.</span></span> <span data-ttu-id="8fcb3-116">如需詳細資訊，請參閱 [進一步的資訊](further-information.md)。</span><span class="sxs-lookup"><span data-stu-id="8fcb3-116">For more information, see [Further Information](further-information.md).</span></span>

## <a name="developer-audience"></a><span data-ttu-id="8fcb3-117">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="8fcb3-117">Developer audience</span></span>

<span data-ttu-id="8fcb3-118">WMI 是設計給使用 C/c + +、Microsoft Visual Basic 應用程式的程式設計人員，或是在 Windows 上具有引擎的指令碼語言，並處理 Microsoft ActiveX 物件。</span><span class="sxs-lookup"><span data-stu-id="8fcb3-118">WMI is designed for programmers who use C/C++, the Microsoft Visual Basic application, or a scripting language that has an engine on Windows and handles Microsoft ActiveX objects.</span></span> <span data-ttu-id="8fcb3-119">雖然對 COM 程式設計的熟悉程度很有説明，但是撰寫應用程式的 c + + 開發人員可以找到良好的範例，讓您開始 [使用 c + + 建立 WMI 應用程式](creating-a-wmi-application-using-c-.md)。</span><span class="sxs-lookup"><span data-stu-id="8fcb3-119">While some familiarity with COM programming is helpful, C++ developers who are writing applications can find good examples for getting started at [Creating a WMI Application Using C++](creating-a-wmi-application-using-c-.md).</span></span>

<span data-ttu-id="8fcb3-120">若要使用 .NET Framework 來開發 c # 或 Visual Basic .NET 中的 managed 程式碼提供者或應用程式，請參閱 [.NET Framework 中的 WMI](/previous-versions/dotnet/netframework-1.1/aa720264(v=vs.71))。</span><span class="sxs-lookup"><span data-stu-id="8fcb3-120">To develop managed code providers or applications in C# or Visual Basic .NET using the .NET Framework, see [WMI in .NET Framework](/previous-versions/dotnet/netframework-1.1/aa720264(v=vs.71)).</span></span>

<span data-ttu-id="8fcb3-121">許多系統管理員和 IT 專業人員透過 PowerShell 存取 WMI。</span><span class="sxs-lookup"><span data-stu-id="8fcb3-121">Many administrators and IT professionals access WMI through PowerShell.</span></span> <span data-ttu-id="8fcb3-122">適用于 PowerShell 的 Get-WMI 指令程式可讓您取得本機或遠端 WMI 儲存機制的資訊。</span><span class="sxs-lookup"><span data-stu-id="8fcb3-122">The Get-WMI cmdlet for PowerShell enables you to retrieve information for a local or remote WMI repository.</span></span> <span data-ttu-id="8fcb3-123">因此，許多主題和類別（特別是在 [建立 WMI 用戶端](creating-wmi-clients.md) 一節中）包含 PowerShell 範例。</span><span class="sxs-lookup"><span data-stu-id="8fcb3-123">As such, a number of topics and classes, especially in the [Creating WMI Clients](creating-wmi-clients.md) section, contain PowerShell examples.</span></span> <span data-ttu-id="8fcb3-124">如需使用 PowerShell 的詳細資訊，請參閱使用 Windows PowerShell [Windows PowerShell](https://msdn.microsoft.com/library/dd835506.aspx) 和 [腳本](https://technet.microsoft.com/library/bb978526.aspx)。</span><span class="sxs-lookup"><span data-stu-id="8fcb3-124">For additional information on using PowerShell, see [Windows PowerShell](https://msdn.microsoft.com/library/dd835506.aspx) and [Scripting with Windows PowerShell](https://technet.microsoft.com/library/bb978526.aspx).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="8fcb3-125">執行階段需求求</span><span class="sxs-lookup"><span data-stu-id="8fcb3-125">Run-time requirements</span></span>

<span data-ttu-id="8fcb3-126">如需有關使用特定 API 元素或 WMI 類別之作業系統的詳細資訊，請參閱 WMI 檔中每個主題的需求一節。</span><span class="sxs-lookup"><span data-stu-id="8fcb3-126">For more information about which operating system is required to use a specific API element or WMI class, see the Requirements section of each topic in the WMI documentation.</span></span>

<span data-ttu-id="8fcb3-127">如果預期的元件似乎遺失，請參閱 [WMI 元件的作業系統可用性](operating-system-availability-of-wmi-components.md)。</span><span class="sxs-lookup"><span data-stu-id="8fcb3-127">If an expected component appears to be missing, see [Operating System Availability of WMI Components](operating-system-availability-of-wmi-components.md).</span></span>

<span data-ttu-id="8fcb3-128">您不需要下載或安裝特定軟體發展 (SDK) ，就能建立 WMI 的腳本或應用程式。</span><span class="sxs-lookup"><span data-stu-id="8fcb3-128">You do not need to download or install a specific software development (SDK) in order to create scripts or applications for WMI.</span></span> <span data-ttu-id="8fcb3-129">不過，有一些 WMI 系統管理工具可讓開發人員覺得有用。</span><span class="sxs-lookup"><span data-stu-id="8fcb3-129">However, there are some WMI administrative tools that developers find useful.</span></span> <span data-ttu-id="8fcb3-130">如需詳細資訊，請參閱「下載」一節中的詳細 [資訊](further-information.md)。</span><span class="sxs-lookup"><span data-stu-id="8fcb3-130">For more information, see the Downloads section in [Further Information](further-information.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="8fcb3-131">本節內容</span><span class="sxs-lookup"><span data-stu-id="8fcb3-131">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="8fcb3-132">關於 WMI</span><span class="sxs-lookup"><span data-stu-id="8fcb3-132">About WMI</span></span>](about-wmi.md)
</dt> <dd>

<span data-ttu-id="8fcb3-133">WMI 的一般資訊。</span><span class="sxs-lookup"><span data-stu-id="8fcb3-133">General information about WMI.</span></span>

</dd> <dt>

[<span data-ttu-id="8fcb3-134">使用 WMI</span><span class="sxs-lookup"><span data-stu-id="8fcb3-134">Using WMI</span></span>](using-wmi.md)
</dt> <dd>

<span data-ttu-id="8fcb3-135">有關如何開發應用程式以使用 WMI 的資訊，其中包括工具的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="8fcb3-135">Information about how to develop applications to use WMI, which includes information about tools.</span></span>

</dd> <dt>

[<span data-ttu-id="8fcb3-136">WMI 參考</span><span class="sxs-lookup"><span data-stu-id="8fcb3-136">WMI Reference</span></span>](wmi-reference.md)
</dt> <dd>

<span data-ttu-id="8fcb3-137">WMI 類別、WMI c + + 類別、WMI COM API、腳本 API 和其他 WMI 參考資料的相關檔。</span><span class="sxs-lookup"><span data-stu-id="8fcb3-137">Documentation about the WMI classes, WMI C++ classes, WMI COM API, Scripting API, and other WMI reference material.</span></span>

</dd> </dl>

 

 

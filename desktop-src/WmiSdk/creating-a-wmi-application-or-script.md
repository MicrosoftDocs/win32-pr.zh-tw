---
description: 任何搭配 ActiveX 物件使用的指令碼語言（如 VBScript）都可以存取 WMI 資料。 應用程式可以在 c + + 中使用適用于 WMI 的 COM API 或 Visual Basic 中的 wmi，使用 >wbemdisp.tlb .tlb 類型程式庫和適用于 WMI 的腳本 API 來存取 WMI。 .
ms.assetid: c0d18827-6b36-4817-8cd9-06cd0f267b28
ms.tgt_platform: multiple
title: 建立 WMI 應用程式或腳本
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b27e3cffd7e4d9bea4ce36e7c0da77ae5d72cdb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996936"
---
# <a name="creating-a-wmi-application-or-script"></a><span data-ttu-id="7f491-105">建立 WMI 應用程式或腳本</span><span class="sxs-lookup"><span data-stu-id="7f491-105">Creating a WMI Application or Script</span></span>

<span data-ttu-id="7f491-106">任何搭配 ActiveX 物件使用的指令碼語言（如 VBScript）都可以存取 WMI 資料。</span><span class="sxs-lookup"><span data-stu-id="7f491-106">Any scripting language, such as VBScript, that works with ActiveX objects can access WMI data.</span></span> <span data-ttu-id="7f491-107">應用程式可以在 c + + 中使用 [適用于 wmi 的 COM API](com-api-for-wmi.md) 或 Visual Basic 中的 wmi，使用 >wbemdisp.tlb .tlb [類型程式庫](using-the-wmi-scripting-type-library.md) 和 [適用于 wmi 的腳本 API](scripting-api-for-wmi.md)來存取 wmi。</span><span class="sxs-lookup"><span data-stu-id="7f491-107">Applications can access WMI in C++, using the [COM API for WMI](com-api-for-wmi.md) or in Visual Basic, using the Wbemdisp.tlb [type library](using-the-wmi-scripting-type-library.md) and the [Scripting API for WMI](scripting-api-for-wmi.md).</span></span> <span data-ttu-id="7f491-108">.</span><span class="sxs-lookup"><span data-stu-id="7f491-108">.</span></span> <span data-ttu-id="7f491-109">您可以撰寫腳本、使用中的伺服器頁 (ASP) ，或 (HTA) 的 HTML 應用程式，以透過 WMI 取得資料。</span><span class="sxs-lookup"><span data-stu-id="7f491-109">You can obtain data through WMI by writing a script, an Active Server Page (ASP), or an HTML application (HTA).</span></span> <span data-ttu-id="7f491-110">您也可以使用 Windows PowerShell 來取得資料或撰寫腳本。</span><span class="sxs-lookup"><span data-stu-id="7f491-110">You can also use Windows PowerShell to obtain data or write scripts.</span></span> <span data-ttu-id="7f491-111">如需詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script) 和 [使用 Windows PowerShell 的開始使用](/powershell/scripting/getting-started/getting-started-with-windows-powershell?view=powershell-7&preserve-view=true)。</span><span class="sxs-lookup"><span data-stu-id="7f491-111">For more information, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script) and [Getting Started with Windows PowerShell](/powershell/scripting/getting-started/getting-started-with-windows-powershell?view=powershell-7&preserve-view=true).</span></span> <span data-ttu-id="7f491-112">TechNet ScriptCenter [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) 包含上百個腳本範例。</span><span class="sxs-lookup"><span data-stu-id="7f491-112">The TechNet ScriptCenter at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) contains hundreds of scripting examples.</span></span> <span data-ttu-id="7f491-113">如需列印和線上資源的詳細資訊，請參閱 [進一步的資訊](further-information.md)。</span><span class="sxs-lookup"><span data-stu-id="7f491-113">For more information about print and online resources, see [Further Information](further-information.md).</span></span>

<span data-ttu-id="7f491-114">下列程式說明如何連接至 WMI 服務和資料存放區。</span><span class="sxs-lookup"><span data-stu-id="7f491-114">The following procedure describes how to connect to the WMI service and data store.</span></span>

<span data-ttu-id="7f491-115">**連接到 WMI 服務和資料存放區**</span><span class="sxs-lookup"><span data-stu-id="7f491-115">**To connect to the WMI service and data store**</span></span>

1.  <span data-ttu-id="7f491-116">在特定電腦上找出 WMI 服務。</span><span class="sxs-lookup"><span data-stu-id="7f491-116">Locate the WMI service on a specific machine.</span></span>
2.  <span data-ttu-id="7f491-117">連接至一或多個 WMI 命名空間。</span><span class="sxs-lookup"><span data-stu-id="7f491-117">Connect to one or more WMI namespaces.</span></span>

<span data-ttu-id="7f491-118">在 c + +、Visual Basic、.NET Framework 語言或使用腳本時，這些作業會有所不同。</span><span class="sxs-lookup"><span data-stu-id="7f491-118">These operations are different in C++, Visual Basic, .NET Framework languages, or when using a script.</span></span> <span data-ttu-id="7f491-119">腳本和 Visual Basic 應用程式必須存取類別，而這些類別的實例是由現有提供者提供資料。</span><span class="sxs-lookup"><span data-stu-id="7f491-119">Scripts and Visual Basic applications must access classes whose instances are supplied with data by existing providers.</span></span> <span data-ttu-id="7f491-120">但以 c + + 撰寫的應用程式可以達成更多目的。</span><span class="sxs-lookup"><span data-stu-id="7f491-120">But applications written in C++ can do more.</span></span> <span data-ttu-id="7f491-121">例如，以 c + + 撰寫的應用程式可以傳送事件，但是 WMI 腳本只能訂閱接收事件。</span><span class="sxs-lookup"><span data-stu-id="7f491-121">For example, an application written in C++ can send events, but a WMI script can only subscribe to receive events.</span></span>

<span data-ttu-id="7f491-122">WMI 提供者只能使用 c + + 或 .NET Framework 來撰寫。</span><span class="sxs-lookup"><span data-stu-id="7f491-122">A WMI provider can be written only in C++ or using the .NET Framework.</span></span> <span data-ttu-id="7f491-123">如需有關以 c # 或 Visual Basic .NET 撰寫應用程式的詳細資訊，請參閱 [WMI .Net 總覽](/previous-versions/bb404655(v=vs.90))。</span><span class="sxs-lookup"><span data-stu-id="7f491-123">For more information about writing applications in C# or Visual Basic .NET, see [WMI .NET Overview](/previous-versions/bb404655(v=vs.90)).</span></span>

<span data-ttu-id="7f491-124">如需建立 WMI 應用程式和腳本的詳細資訊，請參閱：</span><span class="sxs-lookup"><span data-stu-id="7f491-124">For more information about creating applications and scripts for WMI, see:</span></span>

-   [<span data-ttu-id="7f491-125">使用 c + + 建立 WMI 應用程式</span><span class="sxs-lookup"><span data-stu-id="7f491-125">Creating a WMI Application Using C++</span></span>](creating-a-wmi-application-using-c-.md)
-   [<span data-ttu-id="7f491-126">建立 WMI 腳本</span><span class="sxs-lookup"><span data-stu-id="7f491-126">Creating a WMI Script</span></span>](creating-a-wmi-script.md)
-   [<span data-ttu-id="7f491-127">建立受控 WMI 用戶端</span><span class="sxs-lookup"><span data-stu-id="7f491-127">Creating a Managed WMI Client</span></span>](creating-a-managed-wmi-client.md)

<span data-ttu-id="7f491-128">若要執行大部分的工作，請使用預先安裝的 [WMI 類別](wmi-classes.md)。</span><span class="sxs-lookup"><span data-stu-id="7f491-128">To perform most tasks, use the preinstalled [WMI classes](wmi-classes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7f491-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="7f491-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7f491-130">使用 WMI</span><span class="sxs-lookup"><span data-stu-id="7f491-130">Using WMI</span></span>](using-wmi.md)
</dt> </dl>

 

 

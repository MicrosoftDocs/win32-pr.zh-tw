---
description: 使用 WMI 取得用戶端腳本和應用程式資料，或從應用程式提供資料給 WMI 的藍圖。
ms.assetid: d9a3741c-313f-4b63-8588-696a10d370f5
ms.tgt_platform: multiple
title: 使用 WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31878b41de0f44a70c31c2134f0a611a9309a321
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115856"
---
# <a name="using-wmi"></a><span data-ttu-id="75086-103">使用 WMI</span><span class="sxs-lookup"><span data-stu-id="75086-103">Using WMI</span></span>

<span data-ttu-id="75086-104">您可以從用戶端應用程式和腳本使用 WMI。</span><span class="sxs-lookup"><span data-stu-id="75086-104">You can use WMI from client applications and scripts.</span></span> <span data-ttu-id="75086-105">它提供的基礎結構可讓您輕鬆地探索和執行管理工作。</span><span class="sxs-lookup"><span data-stu-id="75086-105">It provides an infrastructure that makes it easy to both discover and perform management tasks.</span></span> <span data-ttu-id="75086-106">此外，您可以藉由建立自己的 WMI 提供者，新增至一組可能的管理工作。</span><span class="sxs-lookup"><span data-stu-id="75086-106">In addition, you can add to the set of possible management tasks by creating your own WMI providers.</span></span>

> [!Note]  
> <span data-ttu-id="75086-107">下一代的 WMI 可用來撰寫應用程式和腳本，可透過 Windows 管理基礎結構 (MI) 取得。</span><span class="sxs-lookup"><span data-stu-id="75086-107">The next-generation version of WMI for writing applications and scripts is available through the Windows Management Infrastructure (MI).</span></span> <span data-ttu-id="75086-108">如需詳細資訊，請參閱 [MI 提供者和用戶端](/previous-versions/windows/desktop/wmi_v2/mi-providers-and-clients-node-page)。</span><span class="sxs-lookup"><span data-stu-id="75086-108">For more information, see [MI Providers and Clients](/previous-versions/windows/desktop/wmi_v2/mi-providers-and-clients-node-page).</span></span>

 

<span data-ttu-id="75086-109">本節將討論下列主題：</span><span class="sxs-lookup"><span data-stu-id="75086-109">The following topics are discussed in this section:</span></span>

-   [<span data-ttu-id="75086-110">從 WMI 取得資料</span><span class="sxs-lookup"><span data-stu-id="75086-110">Obtaining Data from WMI</span></span>](#obtaining-data-from-wmi)
-   [<span data-ttu-id="75086-111">將資料提供給 WMI</span><span class="sxs-lookup"><span data-stu-id="75086-111">Providing Data to WMI</span></span>](#providing-data-to-wmi)
-   [<span data-ttu-id="75086-112">WMI 的重要工作</span><span class="sxs-lookup"><span data-stu-id="75086-112">Important Tasks for WMI</span></span>](#important-tasks-for-wmi)

## <a name="obtaining-data-from-wmi"></a><span data-ttu-id="75086-113">從 WMI 取得資料</span><span class="sxs-lookup"><span data-stu-id="75086-113">Obtaining Data from WMI</span></span>

<span data-ttu-id="75086-114">下列程式描述如何藉由撰寫腳本或應用程式，從 WMI 取得資料。</span><span class="sxs-lookup"><span data-stu-id="75086-114">The following procedure describes how to obtain data from WMI by writing a script or application.</span></span>

<span data-ttu-id="75086-115">**藉由撰寫腳本或應用程式從 WMI 取得資料**</span><span class="sxs-lookup"><span data-stu-id="75086-115">**To obtain data from WMI by writing a script or application**</span></span>

1.  <span data-ttu-id="75086-116">決定要使用的語言。</span><span class="sxs-lookup"><span data-stu-id="75086-116">Decide which language to use.</span></span> <span data-ttu-id="75086-117">如需腳本的詳細資訊，請參閱 [建立 WMI 腳本](creating-a-wmi-script.md)。</span><span class="sxs-lookup"><span data-stu-id="75086-117">For more information about scripting, see [Creating a WMI Script](creating-a-wmi-script.md).</span></span> <span data-ttu-id="75086-118">如需 c + + 的詳細資訊，請參閱 [使用 c + + 建立 WMI 應用程式](creating-a-wmi-application-using-c-.md)。</span><span class="sxs-lookup"><span data-stu-id="75086-118">For more information about C++, see [Creating a WMI Application Using C++](creating-a-wmi-application-using-c-.md).</span></span> <span data-ttu-id="75086-119">如需使用 c # 或 WMI .NET 的詳細資訊，請參閱 [WMI .Net 總覽](/previous-versions/)。</span><span class="sxs-lookup"><span data-stu-id="75086-119">For using more information about C# or WMI .NET, see [WMI .NET Overview](/previous-versions/).</span></span>

    <span data-ttu-id="75086-120">您可以用多種語言來查看或操作 WMI 資料。</span><span class="sxs-lookup"><span data-stu-id="75086-120">You can view or manipulate WMI data in many languages.</span></span> <span data-ttu-id="75086-121">下表列出的主題描述如何使用腳本和應用程式語言來取得資料。</span><span class="sxs-lookup"><span data-stu-id="75086-121">The following table lists the topics that describe how to use the scripting and application languages to obtain data.</span></span>

    

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="75086-122">應用程式語言</span><span class="sxs-lookup"><span data-stu-id="75086-122">Application language</span></span></th>
    <th><span data-ttu-id="75086-123">主題</span><span class="sxs-lookup"><span data-stu-id="75086-123">Topic</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="75086-124">以 Microsoft ActiveX script 裝載撰寫的腳本，包括 Visual Basic Scripting Edition (VBScript) 和 Perl</span><span class="sxs-lookup"><span data-stu-id="75086-124">Scripts written in Microsoft ActiveX script hosting, including Visual Basic Scripting Edition (VBScript) and Perl</span></span><br/></td>
    <td><span data-ttu-id="75086-125"><a href="scripting-api-for-wmi.md">適用于 WMI 的腳本 API</a>。</span><span class="sxs-lookup"><span data-stu-id="75086-125"><a href="scripting-api-for-wmi.md">Scripting API for WMI</a>.</span></span><br/> <span data-ttu-id="75086-126">從 <a href="creating-a-wmi-script.md">建立 WMI 腳本</a>開始。</span><span class="sxs-lookup"><span data-stu-id="75086-126">Start with <a href="creating-a-wmi-script.md">Creating a WMI Script</a>.</span></span><br/> <span data-ttu-id="75086-127">如需腳本範例，請參閱 <a href="wmi-tasks-for-scripts-and-applications.md">腳本和應用程式的 WMI</a> 工作和 TechNet <a href="https://www.microsoft.com/technet/scriptcenter">ScriptCenter</a> 腳本存放庫。</span><span class="sxs-lookup"><span data-stu-id="75086-127">For script code examples, see <a href="wmi-tasks-for-scripts-and-applications.md">WMI Tasks for Scripts and Applications</a> and the TechNet <a href="https://www.microsoft.com/technet/scriptcenter">ScriptCenter</a> Script Repository.</span></span><br/></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="75086-128">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="75086-128">Windows PowerShell</span></span><br/></td>
    <td><span data-ttu-id="75086-129"><a href="/powershell/scripting/getting-started/getting-started-with-windows-powershell?view=powershell-7">使用 Windows PowerShell 開始使用</a></span><span class="sxs-lookup"><span data-stu-id="75086-129"><a href="/powershell/scripting/getting-started/getting-started-with-windows-powershell?view=powershell-7">Getting Started with Windows PowerShell</a></span></span><br/> <span data-ttu-id="75086-130">WMI PowerShell Cmdlet，例如 <a href="/previous-versions//dd315295(v=technet.10)">>get-wmiobject</a>。</span><span class="sxs-lookup"><span data-stu-id="75086-130">WMI PowerShell Cmdlets, such as <a href="/previous-versions//dd315295(v=technet.10)">Get-WmiObject</a>.</span></span><br/></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="75086-131">Visual Basic 應用程式</span><span class="sxs-lookup"><span data-stu-id="75086-131">Visual Basic applications</span></span><br/></td>
    <td><span data-ttu-id="75086-132"><a href="scripting-api-for-wmi.md">適用于 WMI 的腳本 API</a>。</span><span class="sxs-lookup"><span data-stu-id="75086-132"><a href="scripting-api-for-wmi.md">Scripting API for WMI</a>.</span></span><br/></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="75086-133">Active Server Page</span><span class="sxs-lookup"><span data-stu-id="75086-133">Active Server Pages</span></span><br/></td>
    <td><span data-ttu-id="75086-134"><a href="scripting-api-for-wmi.md">適用于 WMI 的腳本 API</a>。</span><span class="sxs-lookup"><span data-stu-id="75086-134"><a href="scripting-api-for-wmi.md">Scripting API for WMI</a>.</span></span><br/> <span data-ttu-id="75086-135">從 <a href="creating-active-server-pages-for-wmi.md">建立 WMI 的 Active Server 頁面</a>開始。</span><span class="sxs-lookup"><span data-stu-id="75086-135">Start with <a href="creating-active-server-pages-for-wmi.md">Creating Active Server Pages for WMI</a>.</span></span><br/></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="75086-136">C++ 應用程式</span><span class="sxs-lookup"><span data-stu-id="75086-136">C++ applications</span></span><br/></td>
    <td><span data-ttu-id="75086-137"><a href="com-api-for-wmi.md">適用于 WMI 的 COM API</a>。</span><span class="sxs-lookup"><span data-stu-id="75086-137"><a href="com-api-for-wmi.md">COM API for WMI</a>.</span></span><br/> <span data-ttu-id="75086-138">首先，使用 c + + 和<a href="wmi-c---application-examples.md">Wmi c + + 應用程式範例</a><a href="creating-a-wmi-application-using-c-.md">來建立 wmi 應用程式</a> (包含) 的範例。</span><span class="sxs-lookup"><span data-stu-id="75086-138">Start with <a href="creating-a-wmi-application-using-c-.md">Creating a WMI Application Using C++</a> and <a href="wmi-c---application-examples.md">WMI C++ Application Examples</a> (contains examples).</span></span><br/></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="75086-139">.NET Framework 以 c #、Visual Basic .NET 或 J 撰寫的應用程式#</span><span class="sxs-lookup"><span data-stu-id="75086-139">.NET Framework applications written in C#, Visual Basic .NET, or J#</span></span><br/></td>
    <td><span data-ttu-id="75086-140">在「 <a href="/previous-versions//hh872326(v=vs.85)"><strong>管理基礎結構</strong></a> 」命名空間中的類別。</span><span class="sxs-lookup"><span data-stu-id="75086-140">Classes in the <a href="/previous-versions//hh872326(v=vs.85)"><strong>Microsoft.Management.Infrastructure</strong></a> namespace.</span></span><br/>
    <blockquote>
    [!Note]<br /><span data-ttu-id="75086-141">
    <strong>System. Management</strong> 是涵蓋 WMI managed 程式碼的原始命名空間。</span><span class="sxs-lookup"><span data-stu-id="75086-141">
    <strong>System.Management</strong> was the original namespace that covered managed code for WMI.</span></span> <span data-ttu-id="75086-142">但是， <strong>管理系統</strong> 的基礎技術通常會比更慢，而且也不會調整及 <a href="/previous-versions//hh872326(v=vs.85)"><strong>管理基礎結構</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="75086-142">However, the underlying technology for <strong>System.Management</strong> is generally slower than, and does not scale as well as, <a href="/previous-versions//hh872326(v=vs.85)"><strong>Microsoft.Management.Infrastructure</strong></a>.</span></span> <span data-ttu-id="75086-143">因此，不建議您針對新的專案使用 [ <strong>系統管理</strong> ]。</span><span class="sxs-lookup"><span data-stu-id="75086-143">As such, it is not recommended that you use <strong>System.Management</strong> for new projects.</span></span> <span data-ttu-id="75086-144"> (如需有關 <strong>系統管理</strong>的詳細資訊，請參閱 <a href="/previous-versions/bb404655(v=vs.90)">WMI .net 總覽</a>。 ) </span><span class="sxs-lookup"><span data-stu-id="75086-144">(For more information on <strong>System.Management</strong>, see <a href="/previous-versions/bb404655(v=vs.90)">WMI .NET Overview</a>.)</span></span> </blockquote>
    <br/></td>
    </tr>
    </tbody>
    </table>

    

     

2.  <span data-ttu-id="75086-145">確定您與遠端電腦的連線可以運作。</span><span class="sxs-lookup"><span data-stu-id="75086-145">Ensure that your connections to remote computers work.</span></span>

    <span data-ttu-id="75086-146">如需詳細資訊，請參閱 [連接到遠端電腦上的 WMI](connecting-to-wmi-on-a-remote-computer.md)。</span><span class="sxs-lookup"><span data-stu-id="75086-146">For more information, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>

3.  <span data-ttu-id="75086-147">連接至遠端電腦上的 WMI 需要正確的安全性設定，如 [維護 WMI 安全性](maintaining-wmi-security.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="75086-147">Connecting to WMI on remote computers requires the correct security settings, as explained in [Maintaining WMI Security](maintaining-wmi-security.md).</span></span> <span data-ttu-id="75086-148">下表列出的主題描述如何使用腳本和應用程式語言來設定安全性設定。</span><span class="sxs-lookup"><span data-stu-id="75086-148">The following table lists the topics that describe how to configure security settings with the scripting and application languages.</span></span>

    

    | <span data-ttu-id="75086-149">語言</span><span class="sxs-lookup"><span data-stu-id="75086-149">Language</span></span>                                                      | <span data-ttu-id="75086-150">主題</span><span class="sxs-lookup"><span data-stu-id="75086-150">Topic</span></span>                                                                                                                                                                                                                                                 |
    |---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="75086-151">任何語言的腳本，Visual Basic 應用程式</span><span class="sxs-lookup"><span data-stu-id="75086-151">Scripts in any language, Visual Basic applications</span></span><br/> | [<span data-ttu-id="75086-152">使用 VBScript 設定預設進程安全性等級</span><span class="sxs-lookup"><span data-stu-id="75086-152">Setting the Default Process Security Level Using VBScript</span></span>](setting-the-default-process-security-level-using-vbscript.md)<br/>                                                                                                                 |
    | <span data-ttu-id="75086-153">Active Server Page</span><span class="sxs-lookup"><span data-stu-id="75086-153">Active Server Pages</span></span><br/>                                | [<span data-ttu-id="75086-154">針對 WMI ASP 腳本設定 IIS 5 和更新版本</span><span class="sxs-lookup"><span data-stu-id="75086-154">Configuring IIS 5 and Later for WMI ASP Scripting</span></span>](configuring-iis-5-for-wmi-asp-scripting.md)<br/>                                                                                                                                           |
    | <span data-ttu-id="75086-155">C++</span><span class="sxs-lookup"><span data-stu-id="75086-155">C++</span></span><br/>                                                | <span data-ttu-id="75086-156">[使用 c + + 設定預設進程安全性等級](setting-the-default-process-security-level-using-c-.md) ，並 [設定 IWbemServices 和其他 proxy 的安全性](setting-the-security-on-iwbemservices-and-other-proxies.md)</span><span class="sxs-lookup"><span data-stu-id="75086-156">[Setting the Default Process Security Level Using C++](setting-the-default-process-security-level-using-c-.md) and [Setting the Security on IWbemServices and Other Proxies](setting-the-security-on-iwbemservices-and-other-proxies.md)</span></span><br/> |

    

     

4.  <span data-ttu-id="75086-157">連接到 WMI 之後，您可以透過查詢和列舉來取得資料。</span><span class="sxs-lookup"><span data-stu-id="75086-157">After connecting to WMI, you can obtain data through queries and enumerations.</span></span>

    <span data-ttu-id="75086-158">如需詳細資訊，請參閱[使用 WQL](querying-with-wql.md)[操作類別和實例資訊](manipulating-class-and-instance-information.md)和查詢。</span><span class="sxs-lookup"><span data-stu-id="75086-158">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md) and [Querying with WQL](querying-with-wql.md).</span></span>

5.  <span data-ttu-id="75086-159">登錄資料可透過 WMI 取得，而您可以建立新的索引鍵和值，或是修改現有的金鑰和值。</span><span class="sxs-lookup"><span data-stu-id="75086-159">Registry data is available through WMI and you can create new keys and values or modify existing ones.</span></span>

    <span data-ttu-id="75086-160">如需詳細資訊，請參閱 [修改系統登錄](modifying-the-system-registry.md)。</span><span class="sxs-lookup"><span data-stu-id="75086-160">For more information, see [Modifying the System Registry](modifying-the-system-registry.md).</span></span>

6.  <span data-ttu-id="75086-161">您可以透過 WMI （在系統重新開機或永久）之間暫時訂閱事件通知。</span><span class="sxs-lookup"><span data-stu-id="75086-161">You can subscribe to event notifications through WMI, either temporarily between system reboots or permanently.</span></span>

    <span data-ttu-id="75086-162">如需詳細資訊，請參閱 [監視事件](monitoring-events.md) 和 [接收 WMI 事件](receiving-a-wmi-event.md)。</span><span class="sxs-lookup"><span data-stu-id="75086-162">For more information, see [Monitoring Events](monitoring-events.md) and [Receiving a WMI Event](receiving-a-wmi-event.md).</span></span>

7.  <span data-ttu-id="75086-163">您可以透過 WMI 取得系統的效能計數器資料。</span><span class="sxs-lookup"><span data-stu-id="75086-163">Performance counter data for a system is available through WMI.</span></span>

    <span data-ttu-id="75086-164">系統效能程式庫計數器會轉換成 WMI 類別。</span><span class="sxs-lookup"><span data-stu-id="75086-164">The system performance library counters are converted to WMI classes.</span></span> <span data-ttu-id="75086-165">如需詳細資訊，請參閱 [監視效能資料](monitoring-performance-data.md)。</span><span class="sxs-lookup"><span data-stu-id="75086-165">For more information, see [Monitoring Performance Data](monitoring-performance-data.md).</span></span>

8.  <span data-ttu-id="75086-166">[腳本和應用程式的 wmi](wmi-tasks-for-scripts-and-applications.md) 工作說明如何使用 wmi 進行許多系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="75086-166">[WMI Tasks for Scripts and Applications](wmi-tasks-for-scripts-and-applications.md) describes how to do many administrative tasks with WMI.</span></span>

## <a name="providing-data-to-wmi"></a><span data-ttu-id="75086-167">將資料提供給 WMI</span><span class="sxs-lookup"><span data-stu-id="75086-167">Providing Data to WMI</span></span>

<span data-ttu-id="75086-168">下列程式描述如何藉由撰寫提供者，將資料提供給 WMI。</span><span class="sxs-lookup"><span data-stu-id="75086-168">The following procedure describes how to supply data to WMI by writing a provider.</span></span>

<span data-ttu-id="75086-169">**撰寫提供者以將資料提供給 WMI**</span><span class="sxs-lookup"><span data-stu-id="75086-169">**To supply data to WMI by writing a provider**</span></span>

-   <span data-ttu-id="75086-170">決定要寫入的提供者類型。</span><span class="sxs-lookup"><span data-stu-id="75086-170">Decide on the type of provider to write.</span></span>

    <span data-ttu-id="75086-171">您無法在 VBScript 中寫入 WMI 提供者。</span><span class="sxs-lookup"><span data-stu-id="75086-171">You cannot write a WMI provider in VBScript.</span></span> <span data-ttu-id="75086-172">不過，您可以採取數種其他方法來撰寫 WMI COM 提供者：</span><span class="sxs-lookup"><span data-stu-id="75086-172">However, you can take several other approaches to writing a WMI COM provider:</span></span>

    -   <span data-ttu-id="75086-173">使用 Visual Studio 中的 WMI ATL Wizard。</span><span class="sxs-lookup"><span data-stu-id="75086-173">Using the WMI ATL Wizard in Visual Studio.</span></span>

        <span data-ttu-id="75086-174">這種方法會建立非受控 COM 提供者。</span><span class="sxs-lookup"><span data-stu-id="75086-174">This approach creates an unmanaged COM provider.</span></span> <span data-ttu-id="75086-175">如需詳細資訊，請參閱 [新增 Wmi 執行個體提供者](./writing-an-instance-provider.md) 和 [新增 Wmi 事件提供者](./writing-an-event-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="75086-175">For more information, see [Adding a WMI Instance Provider](./writing-an-instance-provider.md) and [Adding a WMI Event Provider](./writing-an-event-provider.md).</span></span>

    -   <span data-ttu-id="75086-176">直接在任何整合式開發環境中使用 COM。</span><span class="sxs-lookup"><span data-stu-id="75086-176">Using COM directly in any integrated development environment.</span></span>

        <span data-ttu-id="75086-177">這種方法會建立非受控 COM 提供者。</span><span class="sxs-lookup"><span data-stu-id="75086-177">This approach creates an unmanaged COM provider.</span></span>

    -   <span data-ttu-id="75086-178">使用 .NET Framework 中的 WMI 來建立 managed 程式碼提供者。</span><span class="sxs-lookup"><span data-stu-id="75086-178">Using WMI in the .NET Framework to create a managed code provider.</span></span>

        <span data-ttu-id="75086-179">這種方法會建立 managed 程式碼提供者。</span><span class="sxs-lookup"><span data-stu-id="75086-179">This approach creates a managed code provider.</span></span> <span data-ttu-id="75086-180">Managed 程式碼提供者可以用任何 .NET Framework 語言撰寫，比 WMI COM 提供者更容易撰寫，並可從 WMI [*CIM*](gloss-c.md)型類別（例如 [Win32 類別](/windows/desktop/CIMWin32Prov/win32-provider)）取得資料。</span><span class="sxs-lookup"><span data-stu-id="75086-180">Managed code providers can be written in any .NET Framework language, are simpler to write than WMI COM providers, and can obtain data from the WMI [*CIM*](gloss-c.md)-based classes such as [Win32 Classes](/windows/desktop/CIMWin32Prov/win32-provider).</span></span> <span data-ttu-id="75086-181">不過，.NET Framework WMI 提供者有一些限制。</span><span class="sxs-lookup"><span data-stu-id="75086-181">However, the .NET Framework WMI provider has some limitations.</span></span> <span data-ttu-id="75086-182">如需詳細資訊，請參閱 [使用 WMI 管理應用程式](/previous-versions/dotnet/netframework-1.1/aa720264(v=vs.71))。</span><span class="sxs-lookup"><span data-stu-id="75086-182">For more information, see [Managing Applications Using WMI](/previous-versions/dotnet/netframework-1.1/aa720264(v=vs.71)).</span></span>

    -   <span data-ttu-id="75086-183">不建議使用 [提供者架構類別](wmi-c-classes.md) 。</span><span class="sxs-lookup"><span data-stu-id="75086-183">Using the [provider framework classes](wmi-c-classes.md) is not recommended.</span></span>

        <span data-ttu-id="75086-184">提供者架構已被 WMI ATL 嚮導取代，直接使用 COM 或 .NET Framework 提供者。</span><span class="sxs-lookup"><span data-stu-id="75086-184">The provider framework has been superseded by the WMI ATL wizards, using COM directly, or .NET Framework providers.</span></span> <span data-ttu-id="75086-185">不再建議使用提供者架構類別建立 WMI COM 提供者。</span><span class="sxs-lookup"><span data-stu-id="75086-185">Creating a WMI COM provider with the provider framework classes is no longer recommended.</span></span> <span data-ttu-id="75086-186">下表列出說明如何使用 COM 或 .NET Framework 提供者的主題。</span><span class="sxs-lookup"><span data-stu-id="75086-186">The following table lists the topics that describe how to use COM or .NET Framework providers.</span></span>

    

    | <span data-ttu-id="75086-187">提供者</span><span class="sxs-lookup"><span data-stu-id="75086-187">Provider</span></span>                                                      | <span data-ttu-id="75086-188">主題</span><span class="sxs-lookup"><span data-stu-id="75086-188">Topic</span></span>                                                                                                   |
    |---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="75086-189">與 WMI 相同的進程中的 COM 提供者</span><span class="sxs-lookup"><span data-stu-id="75086-189">COM provider in the same process as WMI</span></span><br/>            | [<span data-ttu-id="75086-190">將資料提供給 WMI</span><span class="sxs-lookup"><span data-stu-id="75086-190">Providing Data to WMI</span></span>](providing-data-to-wmi.md)<br/>                                           |
    | <span data-ttu-id="75086-191">COM 低耦合提供者</span><span class="sxs-lookup"><span data-stu-id="75086-191">COM decoupled provider</span></span><br/>                             | [<span data-ttu-id="75086-192">將提供者併入應用程式中</span><span class="sxs-lookup"><span data-stu-id="75086-192">Incorporating a Provider in an Application</span></span>](incorporating-a-provider-in-an-application.md)<br/> |
    | <span data-ttu-id="75086-193">C # 或 Visual Basic.NET 中的 .NET Framework 提供者</span><span class="sxs-lookup"><span data-stu-id="75086-193">.NET Framework provider in C# or Visual Basic.NET</span></span><br/> | <span data-ttu-id="75086-194">[使用 WMI 管理應用程式](/previous-versions/dotnet/netframework-1.1/aa720264(v=vs.71))</span><span class="sxs-lookup"><span data-stu-id="75086-194">[Managing Applications Using WMI](/previous-versions/dotnet/netframework-1.1/aa720264(v=vs.71))</span></span><br/>            |

    

     

## <a name="important-tasks-for-wmi"></a><span data-ttu-id="75086-195">WMI 的重要工作</span><span class="sxs-lookup"><span data-stu-id="75086-195">Important Tasks for WMI</span></span>

<span data-ttu-id="75086-196">下列主題提供有關使用 WMI 來監視和控制企業元件的資訊。</span><span class="sxs-lookup"><span data-stu-id="75086-196">The following topics provide information about using WMI to monitor and control enterprise components.</span></span>



| <span data-ttu-id="75086-197">主題</span><span class="sxs-lookup"><span data-stu-id="75086-197">Topic</span></span>                                                                                                                                           | <span data-ttu-id="75086-198">描述</span><span class="sxs-lookup"><span data-stu-id="75086-198">Description</span></span>                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="75086-199">腳本和應用程式的 WMI 工作</span><span class="sxs-lookup"><span data-stu-id="75086-199">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)<br/>                                                 | <span data-ttu-id="75086-200">描述如何在執行一般電腦和網路管理工作的腳本和應用程式中，尋找要使用的正確 WMI 類別和程式，例如為遠端電腦新增新的印表機連線，或尋找電腦上所有已安裝的修補程式。</span><span class="sxs-lookup"><span data-stu-id="75086-200">Describes how to find the correct WMI class and procedures to use in scripts and applications that perform common computer and network administration tasks, such as adding a new printer connection for a remote computer or finding all the installed hotfixes on a computer.</span></span><br/>                                                                            |
| [<span data-ttu-id="75086-201">建立 WMI 應用程式或腳本</span><span class="sxs-lookup"><span data-stu-id="75086-201">Creating a WMI Application or Script</span></span>](creating-a-wmi-application-or-script.md)<br/>                                                     | <span data-ttu-id="75086-202">任何搭配 ActiveX 物件使用的指令碼語言，例如 VBScript 或 Perl 都可以存取 WMI 資料。</span><span class="sxs-lookup"><span data-stu-id="75086-202">Any scripting language, such as VBScript or Perl, that works with ActiveX objects can access WMI data.</span></span> <span data-ttu-id="75086-203">應用程式可以在 c + + 中使用 [適用于 wmi 的 COM API](com-api-for-wmi.md) 或 Visual Basic 中的 wmi，使用 >wbemdisp.tlb .tlb[類型程式庫](using-the-wmi-scripting-type-library.md) 和 [適用于 wmi 的腳本 API](scripting-api-for-wmi.md)來存取 wmi。</span><span class="sxs-lookup"><span data-stu-id="75086-203">Applications can access WMI in C++, using the [COM API for WMI](com-api-for-wmi.md) or in Visual Basic, using the Wbemdisp.tlb[type library](using-the-wmi-scripting-type-library.md) and the [Scripting API for WMI](scripting-api-for-wmi.md).</span></span><br/> |
| [<span data-ttu-id="75086-204">連接至遠端電腦上的 WMI</span><span class="sxs-lookup"><span data-stu-id="75086-204">Connecting to WMI on a Remote Computer</span></span>](connecting-to-wmi-on-a-remote-computer.md)<br/>                                                 | <span data-ttu-id="75086-205">描述腳本、應用程式和提供者如何在遠端電腦上建立與 WMI 的連接，以取得資料或控制硬體和軟體。</span><span class="sxs-lookup"><span data-stu-id="75086-205">Describes how scripts, applications, and providers can establish connections to WMI on remote computers to obtain data or control hardware and software.</span></span><br/>                                                                                                                                                                                                   |
| [<span data-ttu-id="75086-206">使用 Windows PowerShell 連接到遠端電腦上的 WMI</span><span class="sxs-lookup"><span data-stu-id="75086-206">Connecting to WMI on a Remote Computer by Using Windows PowerShell</span></span>](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md)<br/> | <span data-ttu-id="75086-207">說明如何使用 Windows PowerShell 在遠端電腦上建立與 WMI 的連接，以取得資料或控制硬體和軟體。</span><span class="sxs-lookup"><span data-stu-id="75086-207">Describes how to use Windows PowerShell to establish connections to WMI on remote computers to obtain data or to control hardware and software.</span></span><br/>                                                                                                                                                                                                            |
| [<span data-ttu-id="75086-208">監視事件</span><span class="sxs-lookup"><span data-stu-id="75086-208">Monitoring Events</span></span>](monitoring-events.md)<br/>                                                                                           | <span data-ttu-id="75086-209">說明如何藉由建立暫時或永久的 WMI 事件取用者來取得事件通知。</span><span class="sxs-lookup"><span data-stu-id="75086-209">Describes how to get event notifications by creating temporary or permanent WMI event consumers.</span></span><br/>                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="75086-210">將資料提供給 WMI</span><span class="sxs-lookup"><span data-stu-id="75086-210">Providing Data to WMI</span></span>](providing-data-to-wmi.md)<br/>                                                                                   | <span data-ttu-id="75086-211">WMI 會將動態管理資料提供給用戶端腳本和應用程式，方法是從提供者取得它。</span><span class="sxs-lookup"><span data-stu-id="75086-211">WMI supplies dynamic management data to client scripts and applications by obtaining it from providers.</span></span><br/>                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="75086-212">在64位電腦上取得和提供資料</span><span class="sxs-lookup"><span data-stu-id="75086-212">Getting and Providing Data on a 64-bit Computer</span></span>](getting-and-providing-data-on-a-64-bit-computer.md)<br/>                               | <span data-ttu-id="75086-213">描述如何在64位系統上存取提供者寫入器的非預設提供者和考慮。</span><span class="sxs-lookup"><span data-stu-id="75086-213">Describes how to access nondefault providers and considerations for provider writers on 64-bit systems.</span></span><br/>                                                                                                                                                                                                                                                    |




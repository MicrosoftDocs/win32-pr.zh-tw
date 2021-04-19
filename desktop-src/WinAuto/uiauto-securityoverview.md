---
title: 輔助技術的安全性考慮
description: 輔助技術是在 Windows 桌面上執行的應用程式，可協助協助工具使用者與作業系統和電腦上執行的其他應用程式（包括新的 Windows UI 中的應用程式）互動。
ms.assetid: 0c3689e1-2124-4142-b0bd-233e95ee1285
f1_keywords:
- vs.debug.error.launch_elevation_requirements
keywords:
- uiAccess 屬性
- 消費者介面自動化，uiAccess 屬性
- security、uiAccess 屬性
- 並無 requestedexecutionlevel 標記
- 消費者介面自動化，並無 requestedexecutionlevel 標記
- 消費者介面自動化，安全性考慮
- 消費者介面自動化，資訊清單檔
- 資訊清單檔
- 使用者帳戶控制
- 安全性，使用者帳戶控制
- 安全性，資訊清單檔
- 安全性，並無 requestedexecutionlevel 標記
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12f2f5cf006c0adaf9b170a4ed11abd9afd52012
ms.sourcegitcommit: 4e4f9e7c90d25af0774deec1d44bd49fa9b6daa9
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2020
ms.locfileid: "106993737"
---
# <a name="security-considerations-for-assistive-technologies"></a><span data-ttu-id="4f511-115">輔助技術的安全性考慮</span><span class="sxs-lookup"><span data-stu-id="4f511-115">Security Considerations for Assistive Technologies</span></span>

<span data-ttu-id="4f511-116">輔助技術是在 Windows 桌面上執行的應用程式，可協助協助工具使用者與作業系統和電腦上執行的其他應用程式互動，包括新的 Windows UI 中的應用程式。</span><span class="sxs-lookup"><span data-stu-id="4f511-116">Assistive technologies are applications that run on the Windows desktop and help accessibility users interact with the operating system and other applications running on the computer, including applications in the new Windows UI.</span></span> <span data-ttu-id="4f511-117">輔助技術應用程式的運作方式是從作業系統和其他應用程式中取出資訊，然後以使用者可存取的方式來呈現資訊。</span><span class="sxs-lookup"><span data-stu-id="4f511-117">Assistive technology applications work by retrieving information from the operating system and other applications, and then presenting the information in a way that is accessible to the user.</span></span> <span data-ttu-id="4f511-118">輔助技術應用程式也可以根據使用者的輸入，以程式設計方式「驅動」作業系統和其他應用程式。</span><span class="sxs-lookup"><span data-stu-id="4f511-118">An assistive technology application can also programmatically "drive" the operating system and other applications based on input from the user.</span></span>

<span data-ttu-id="4f511-119">輔助技術應用程式的本質需要它們跨進程界限，而且它們可以存取以較高完整性層級執行的進程， (IL) 。</span><span class="sxs-lookup"><span data-stu-id="4f511-119">The nature of assistive technology applications requires that they cross process boundaries, and that they have access to processes that run at a higher integrity level (IL) than themselves.</span></span> <span data-ttu-id="4f511-120"> (在中 IL 執行的輔助技術應用程式。 ) 例如，當使用者嘗試執行需要系統管理許可權的工作時，Windows 會顯示對話方塊，詢問使用者是否同意繼續進行。</span><span class="sxs-lookup"><span data-stu-id="4f511-120">(An assistive technology application runs at medium IL.) For example, when the user attempts to perform a task that requires administrative privileges, Windows presents a dialog box asking the user for consent to continue.</span></span> <span data-ttu-id="4f511-121">此對話方塊會在較高的 IL 上執行，以保護它免于跨進程通訊，讓惡意軟體無法模擬使用者輸入。</span><span class="sxs-lookup"><span data-stu-id="4f511-121">This dialog box runs at a higher IL to protect it from cross-process communication, so that malicious software cannot simulate user input.</span></span> <span data-ttu-id="4f511-122">同樣地，桌面登入畫面會在較高的 IL 上執行，以防止其他進程存取。</span><span class="sxs-lookup"><span data-stu-id="4f511-122">Similarly, the desktop logon screen runs at a higher IL to prevent it from being accessed by other processes.</span></span>

<span data-ttu-id="4f511-123">輔助技術應用程式通常需要存取受保護的系統 UI 元素或其他可能以較高許可權層級執行的進程。</span><span class="sxs-lookup"><span data-stu-id="4f511-123">Assistive technology applications typically need access to the protected system UI elements, or to other processes that might be running at a higher privilege level.</span></span> <span data-ttu-id="4f511-124">因此，輔助技術應用程式必須受系統信任，且必須以特殊許可權執行。</span><span class="sxs-lookup"><span data-stu-id="4f511-124">Therefore, assistive technology applications must be trusted by the system, and must run with special privileges.</span></span>

<span data-ttu-id="4f511-125">若要取得更高 IL 程式的存取權，輔助技術應用程式必須在應用程式資訊清單中設定 UIAccess 旗標，並由具有系統管理員許可權的使用者啟動。</span><span class="sxs-lookup"><span data-stu-id="4f511-125">To get access to higher IL processes, an assistive technology application must set the UIAccess flag in the application's manifest and be launched by a user with administrator privileges.</span></span>

> [!NOTE]
> <span data-ttu-id="4f511-126">存取權限的限制如下：</span><span class="sxs-lookup"><span data-stu-id="4f511-126">Access privileges are constrained as follows:</span></span>
>
> - <span data-ttu-id="4f511-127">在資訊清單中沒有 UIAccess 的應用程式是以 medium IL 開頭，且無法存取提升的 ( "medium +" IL) 進程 UI。</span><span class="sxs-lookup"><span data-stu-id="4f511-127">An application that doesn't have UIAccess in the manifest starts with medium IL and cannot access elevated ("medium+" IL) process UI.</span></span>
> - <span data-ttu-id="4f511-128">在資訊清單中具有 UIAccess 的應用程式，以及不在 administrators 群組中的使用者啟動的應用程式，會以「中 +」 IL 的形式啟動，而且無法存取提升許可權的 UI (不會以「高」 IL 的形式執行，例如透過以 **滑鼠右鍵按一下 > 以系統管理員身分執行的** 應用程式) 。</span><span class="sxs-lookup"><span data-stu-id="4f511-128">An application that has UIAccess in the manifest and is launched by a user who is not in the administrators group, starts as "medium+" IL and cannot access elevated UI (nothing running as "high" IL, such as apps launched through a **Right click -> Run as administrator**).</span></span>
> - <span data-ttu-id="4f511-129">應用程式具有 UI 存取權，且由系統管理員使用者啟動為「高」 IL，並且可以存取提高許可權的 UI，因為它具有相同的 IL。</span><span class="sxs-lookup"><span data-stu-id="4f511-129">An application has UI Access and is launched by an admin user starts as "high" IL and can access elevated UI because it has the same IL.</span></span>
>
> <span data-ttu-id="4f511-130">UIAccess 沒有足夠的進程，無法在 IL 界限中向上移動。</span><span class="sxs-lookup"><span data-stu-id="4f511-130">UIAccess is not enough for a process to move up through the IL boundary.</span></span>

<span data-ttu-id="4f511-131">除了可以存取更高 IL 程式之外，具有這些許可權的輔助技術應用程式可以隨時以 z 順序的最上層應用程式執行，這表示在使用者需要時，可以看到輔助技術應用程式並可供使用。</span><span class="sxs-lookup"><span data-stu-id="4f511-131">In addition to having access to higher IL processes, an assistive technology application with these privileges can run as the topmost application in the z-order at any time, meaning that an assistive technology application can be visible and available whenever the user needs it.</span></span>

> [!Important]
> <span data-ttu-id="4f511-132">先前所列的案例都沒有提供在 system IL 下執行之 UI 的存取權。</span><span class="sxs-lookup"><span data-stu-id="4f511-132">None of the previously listed scenarios provide access to UI running under the system IL.</span></span> <span data-ttu-id="4f511-133">只有在使用者帳戶控制中啟動進程時，才可能這樣做， (在 SYSTEM (和 system IL) 下的 UAC) desktop。</span><span class="sxs-lookup"><span data-stu-id="4f511-133">This is only possible if the process is launched in the user account control (UAC) desktop under SYSTEM (and system IL).</span></span> <span data-ttu-id="4f511-134">在此情況下，設定 UIAccess 沒有任何作用。</span><span class="sxs-lookup"><span data-stu-id="4f511-134">In this case, setting UIAccess has no effect.</span></span>

## <a name="uiaccess-requirements-for-assistive-technology-applications"></a><span data-ttu-id="4f511-135">輔助技術應用程式的 UIAccess 需求</span><span class="sxs-lookup"><span data-stu-id="4f511-135">UIAccess Requirements for Assistive Technology Applications</span></span>

<span data-ttu-id="4f511-136">輔助技術應用程式是 Windows Windows 傳統型應用程式，可與桌面上和新的 Windows UI 中執行的其他進程互動，以從系統和應用程式取得資訊。</span><span class="sxs-lookup"><span data-stu-id="4f511-136">An assistive technology application is a Windows Windows desktop application that interacts with other processes running on the desktop and in the new Windows UI to get information from the system and applications.</span></span> <span data-ttu-id="4f511-137">輔助技術應用程式接著可以提供資訊給協助工具使用者。</span><span class="sxs-lookup"><span data-stu-id="4f511-137">The assistive technology application can then provide the information to accessibility users.</span></span>

<span data-ttu-id="4f511-138">輔助技術應用程式會在應用程式資訊清單中設定 UIAccess 旗標，以取得其他進程的存取權。</span><span class="sxs-lookup"><span data-stu-id="4f511-138">An assistive technology application gets access to other processes by setting the UIAccess flag in the application manifest.</span></span> <span data-ttu-id="4f511-139">若要使用 UIAccess 旗標，輔助技術應用程式必須符合下列需求。</span><span class="sxs-lookup"><span data-stu-id="4f511-139">To use the UIAccess flag, an assistive technology application must meet the following requirements.</span></span>

-   <span data-ttu-id="4f511-140">需要顯示、與其他應用程式互動或反映資訊，以提供協助工具案例的資訊，以及/或</span><span class="sxs-lookup"><span data-stu-id="4f511-140">Require to display, interact with, or reflect information from another application to provide information for an accessibility scenario, and/or</span></span>
-   <span data-ttu-id="4f511-141">需要以最上層視窗的形式執行，才能取得或顯示此資訊。</span><span class="sxs-lookup"><span data-stu-id="4f511-141">Require running as the top-most window to obtain or display this information.</span></span>

<span data-ttu-id="4f511-142">若要使用 UIAccess，輔助技術應用程式必須：</span><span class="sxs-lookup"><span data-stu-id="4f511-142">To use UIAccess, an assistive technology application needs to:</span></span>

-   <span data-ttu-id="4f511-143">使用憑證進行簽署，以與以較高許可權層級執行的應用程式互動。</span><span class="sxs-lookup"><span data-stu-id="4f511-143">Be signed with a certificate to interact with applications running at a higher privilege level.</span></span>
-   <span data-ttu-id="4f511-144">由系統信任。</span><span class="sxs-lookup"><span data-stu-id="4f511-144">Be trusted by the system.</span></span> <span data-ttu-id="4f511-145">應用程式必須安裝在需要使用者帳戶控制 (UAC) 提示進行存取的安全位置。</span><span class="sxs-lookup"><span data-stu-id="4f511-145">The application must be installed in a secure location that requires a user account control (UAC) prompt for access.</span></span> <span data-ttu-id="4f511-146">例如，[Program Files] 資料夾。</span><span class="sxs-lookup"><span data-stu-id="4f511-146">For example, the Program Files folder.</span></span>
-   <span data-ttu-id="4f511-147">使用包含 uiAccess 旗標的資訊清單檔來建立。</span><span class="sxs-lookup"><span data-stu-id="4f511-147">Be built with a manifest file that includes the uiAccess flag.</span></span>

<span data-ttu-id="4f511-148">不應使用 UIAccess：</span><span class="sxs-lookup"><span data-stu-id="4f511-148">UIAccess should not be used:</span></span>

-   <span data-ttu-id="4f511-149">不是輔助技術的應用程式。</span><span class="sxs-lookup"><span data-stu-id="4f511-149">By applications that are not assistive technologies.</span></span>
-   <span data-ttu-id="4f511-150">由輔助技術應用程式顯示與其目標的協助工具案例無關的資訊或 UI。</span><span class="sxs-lookup"><span data-stu-id="4f511-150">By assistive technology applications that display information or UI that is not relevant to the accessibility scenario they target.</span></span>
-   <span data-ttu-id="4f511-151">由只想顯示新的 Windows UI 中其他應用程式的應用程式。</span><span class="sxs-lookup"><span data-stu-id="4f511-151">By applications that just want to appear above other applications in the new Windows UI.</span></span>
    > [!Note]  
    > <span data-ttu-id="4f511-152">針對新的 Windows UI 開發的應用程式沒有 UIAccess 作為可用的選項。</span><span class="sxs-lookup"><span data-stu-id="4f511-152">Applications developed for the new Windows UI do not have UIAccess as an available option.</span></span>

     

## <a name="setting-uiaccess-in-the-application-manifest-file"></a><span data-ttu-id="4f511-153">在應用程式資訊清單檔中設定 UIAccess</span><span class="sxs-lookup"><span data-stu-id="4f511-153">Setting UIAccess in the Application Manifest File</span></span>

<span data-ttu-id="4f511-154">若要取得受保護系統 UI 的存取權，您必須使用資訊清單檔案來建立應用程式，而資訊清單檔中必須包含特殊屬性。</span><span class="sxs-lookup"><span data-stu-id="4f511-154">To gain access to the protected system UI, applications must be built with a manifest file that includes a special attribute in the manifest file.</span></span> <span data-ttu-id="4f511-155">此 **uiAccess** 屬性包含在 **並無 requestedexecutionlevel** 標記中，如下列程式碼範例所示。</span><span class="sxs-lookup"><span data-stu-id="4f511-155">This **uiAccess** attribute is included in the **requestedExecutionLevel** tag, as shown in the following code example.</span></span>


```XML
<trustInfo xmlns="urn:schemas-microsoft-com:asm.v3"> 
    <security> 
        <requestedPrivileges> 
        <requestedExecutionLevel 
            level="highestAvailable" 
            uiAccess="true" /> 
        </requestedPrivileges> 
    </security> 
</trustInfo> 
```



<span data-ttu-id="4f511-156">此程式碼中的 **level** 屬性值僅為範例。</span><span class="sxs-lookup"><span data-stu-id="4f511-156">The value of the **level** attribute in this code is an example only.</span></span>

<span data-ttu-id="4f511-157">**UIAccess** 預設為 "false"。</span><span class="sxs-lookup"><span data-stu-id="4f511-157">**UIAccess** is "false" by default.</span></span> <span data-ttu-id="4f511-158">如果省略此屬性，或沒有資訊清單，應用程式將無法取得受保護 UI 的存取權。</span><span class="sxs-lookup"><span data-stu-id="4f511-158">If the attribute is omitted, or if there is no manifest, the application cannot gain access to the protected UI.</span></span>

<span data-ttu-id="4f511-159">如需有關 Windows 安全性、簽署應用程式以及建立資訊清單的詳細資訊，請參閱[Windows vista 和 Windows Server 2008 開發人員故事： MSDN 上的 Windows Vista 應用程式開發需求 (UAC) 的使用者帳戶控制](/previous-versions/aa905330(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="4f511-159">For more information on Windows security, on signing applications, and on creating manifests, see [The Windows Vista and Windows Server 2008 Developer Story: Windows Vista Application Development Requirements for User Account Control (UAC)](/previous-versions/aa905330(v=msdn.10)) on MSDN.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4f511-160">相關主題</span><span class="sxs-lookup"><span data-stu-id="4f511-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4f511-161">UI 自動化基礎</span><span class="sxs-lookup"><span data-stu-id="4f511-161">UI Automation Fundamentals</span></span>](entry-uiautocore-overview.md)
</dt> </dl>

 

 
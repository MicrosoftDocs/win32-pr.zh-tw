---
description: 在 Windows 8.1 和 Windows 10 中，GetVersion 和 GetVersionEx 函數已被取代。
ms.assetid: E7A1A16A-95B3-4B45-81AD-A19E33F15AE4
title: 以適用于 Windows 的應用程式為目標
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0bd280451e5a1dd6a5162dd7b9ccb34495d22be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320359"
---
# <a name="targeting-your-application-for-windows"></a><span data-ttu-id="18812-103">以適用于 Windows 的應用程式為目標</span><span class="sxs-lookup"><span data-stu-id="18812-103">Targeting your application for Windows</span></span>

<span data-ttu-id="18812-104">在 Windows 8.1 和 Windows 10 中， [**GetVersion**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversion) 和 [**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa) 函數已被取代。</span><span class="sxs-lookup"><span data-stu-id="18812-104">In Windows 8.1 and Windows 10, the [**GetVersion**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversion) and [**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa) functions have been deprecated.</span></span> <span data-ttu-id="18812-105">在 Windows 10 中， [**VerifyVersionInfo**](/windows/win32/api/winbase/nf-winbase-verifyversioninfoa) 函數也已被取代。</span><span class="sxs-lookup"><span data-stu-id="18812-105">In Windows 10, the [**VerifyVersionInfo**](/windows/win32/api/winbase/nf-winbase-verifyversioninfoa) function has also been deprecated.</span></span> <span data-ttu-id="18812-106">雖然您仍然可以呼叫已被取代的函式，但如果您的應用程式並未特別以 Windows 8.1 或 Windows 10 為目標，則函式會傳回 (6.2) 的 Windows 8 版本。</span><span class="sxs-lookup"><span data-stu-id="18812-106">While you can still call the deprecated functions, if your application does not specifically target Windows 8.1 or Windows 10, the functions will return the Windows 8 version (6.2).</span></span>

> [!Note]  
> <span data-ttu-id="18812-107">[**GetVersion**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversion)、 [**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa)、 [**VerifyVersionInfo**](/windows/win32/api/winbase/nf-winbase-verifyversioninfoa)和 [Version Helper](version-helper-apis.md) 函式僅適用于桌面應用程式。</span><span class="sxs-lookup"><span data-stu-id="18812-107">[**GetVersion**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversion), [**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa), [**VerifyVersionInfo**](/windows/win32/api/winbase/nf-winbase-verifyversioninfoa), and the [Version Helper functions](version-helper-apis.md) are for desktop apps only.</span></span> <span data-ttu-id="18812-108">通用 Windows 應用程式可以使用 [**AnalyticsInfo VersionInfo**](/uwp/api/windows.system.profile.analyticsinfo.versioninfo) 屬性來取得遙測和診斷記錄。</span><span class="sxs-lookup"><span data-stu-id="18812-108">Universal Windows apps can use the [**AnalyticsInfo.VersionInfo**](/uwp/api/windows.system.profile.analyticsinfo.versioninfo) property for telemetry and diagnostic logs.</span></span>

<span data-ttu-id="18812-109">為了讓您的應用程式以 Windows 8.1 或 Windows 10 為目標，您必須將 [應用程式 (可執行檔) 資訊清單](/windows/compatibility/application-executable-manifest) 包含在應用程式的可執行檔中。</span><span class="sxs-lookup"><span data-stu-id="18812-109">In order for your app to target Windows 8.1 or Windows 10, you'll need to include an [app (executable) manifest](/windows/compatibility/application-executable-manifest) for the app's executable.</span></span> <span data-ttu-id="18812-110">然後，在資訊清單的 [ [ **&lt; 相容性 &gt;** ] 區段](../SbsCs/application-manifests.md#compatibility)中，您必須為您想要宣告應用程式支援的每個 Windows 版本新增 **&lt; supportedOS &gt;** 元素。</span><span class="sxs-lookup"><span data-stu-id="18812-110">Then, in the [**&lt;compatibility&gt;** section](../SbsCs/application-manifests.md#compatibility) of the manifest, you'll need to add a **&lt;supportedOS&gt;** element for each Windows version you want to declare that your app supports.</span></span>

<span data-ttu-id="18812-111">下列範例會顯示應用程式的應用程式資訊清單檔，以支援從 Windows Vista 到 Windows 10 的所有 Windows 版本：</span><span class="sxs-lookup"><span data-stu-id="18812-111">The following example shows an app manifest file for an app that supports all versions of Windows from Windows Vista to Windows 10:</span></span>

```XML
<!-- example.exe.manifest -->
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly manifestVersion="1.0" xmlns="urn:schemas-microsoft-com:asm.v1" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
    <assemblyIdentity
        type="win32"
        name="Contoso.ExampleApplication.ExampleBinary"
        version="1.2.3.4"
        processorArchitecture="x86"
    />
    <description>Contoso Example Application</description>
    <compatibility xmlns="urn:schemas-microsoft-com:compatibility.v1">
        <application>
            <!-- Windows 10 -->
            <supportedOS Id="{8e0f7a12-bfb3-4fe8-b9a5-48fd50a15a9a}"/>
            <!-- Windows 8.1 -->
            <supportedOS Id="{1f676c76-80e1-4239-95bb-83d0f6d0da78}"/>
            <!-- Windows 8 -->
            <supportedOS Id="{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}"/>
            <!-- Windows 7 -->
            <supportedOS Id="{35138b9a-5d96-4fbd-8e2d-a2440225f93a}"/>
            <!-- Windows Vista -->
            <supportedOS Id="{e2011457-1546-43c5-a5fe-008deee3d3f0}"/> 
        </application>
    </compatibility>
    <trustInfo xmlns="urn:schemas-microsoft-com:asm.v3">
        <security>
            <requestedPrivileges>
                <!--
                  UAC settings:
                  - app should run at same integrity level as calling process
                  - app does not need to manipulate windows belonging to
                    higher-integrity-level processes
                  -->
                <requestedExecutionLevel
                    level="asInvoker"
                    uiAccess="false"
                />   
            </requestedPrivileges>
        </security>
    </trustInfo>
</assembly>
```

<span data-ttu-id="18812-112">在舊版作業系統上執行您的應用程式時，在您的應用程式資訊清單中宣告 Windows 8.1 或 Windows 10 的支援將不會有任何作用。</span><span class="sxs-lookup"><span data-stu-id="18812-112">Declaring support for Windows 8.1 or Windows 10 in your app manifest will not have any effect when running your app on previous operating systems.</span></span>

<span data-ttu-id="18812-113">上述的應用程式資訊清單也包含 [ **&lt; trustInfo &gt;** 區段](/previous-versions/bb756929(v=msdn.10))，此區段會指定系統應如何將它視為 [使用者帳戶控制的相關 (UAC)](/windows/security/identity-protection/user-account-control/how-user-account-control-works)。</span><span class="sxs-lookup"><span data-stu-id="18812-113">The above app manifest also includes a [**&lt;trustInfo&gt;** section](/previous-versions/bb756929(v=msdn.10)), which specifies how the system should treat it with respect to [User Account Control (UAC)](/windows/security/identity-protection/user-account-control/how-user-account-control-works).</span></span> <span data-ttu-id="18812-114">新增 **trustInfo** 並不重要，但強烈建議使用，即使您的應用程式不需要任何特定的 UAC 相關行為也是如此。</span><span class="sxs-lookup"><span data-stu-id="18812-114">Adding **trustInfo** isn't essential, but it is highly recommended, even when your app doesn't need any particular UAC-related behavior.</span></span> <span data-ttu-id="18812-115">尤其是，如果您根本未新增 **trustInfo** ，則應用程式的32位 x86 版本將受限於 [UAC 檔案虛擬化](/windows/security/identity-protection/user-account-control/how-user-account-control-works#virtualization)，如此可讓系統管理員許可權的資料夾（例如 Windows 系統資料夾）在失敗時進行寫入，但是會將它們重新導向至使用者特定的 "VirtualStore" 資料夾。</span><span class="sxs-lookup"><span data-stu-id="18812-115">In particular, if you don't add **trustInfo** at all, then 32-bit x86 versions of your app will be subject to [UAC file virtualization](/windows/security/identity-protection/user-account-control/how-user-account-control-works#virtualization), which allows writes to administrator-privileged folders like the Windows system folders to succeed when they would otherwise fail, but redirects them to a user-specific "VirtualStore" folder.</span></span>

## <a name="related-topics"></a><span data-ttu-id="18812-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="18812-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="18812-117">取得系統版本</span><span class="sxs-lookup"><span data-stu-id="18812-117">Getting the system version</span></span>](getting-the-system-version.md)
</dt> <dt>

[<span data-ttu-id="18812-118">版本 Helper 函數</span><span class="sxs-lookup"><span data-stu-id="18812-118">Version Helper functions</span></span>](version-helper-apis.md)
</dt> <dt>

[<span data-ttu-id="18812-119">OSVERSIONINFO</span><span class="sxs-lookup"><span data-stu-id="18812-119">OSVERSIONINFO</span></span>](/windows/desktop/api/winnt/ns-winnt-osversioninfoa)
</dt> <dt>

[<span data-ttu-id="18812-120">OSVERSIONINFOEX</span><span class="sxs-lookup"><span data-stu-id="18812-120">OSVERSIONINFOEX</span></span>](/windows/desktop/api/winnt/ns-winnt-osversioninfoexa)
</dt> </dl>

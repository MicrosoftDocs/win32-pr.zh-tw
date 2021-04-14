---
title: Windows 8.1 和 Windows Server 2012 R2 中的作業系統版本變更
description: Windows 8.1 和 Windows Server 2012 R2 中的作業系統版本變更
ms.assetid: 3040262A-85EB-4F26-BE34-D2BBD5886E9E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0078ba918c675bbc8b9b9bbaf76660388f05bda9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382702"
---
# <a name="operating-system-version-changes-in-windows-81-and-windows-server-2012-r2"></a><span data-ttu-id="8f8e4-103">Windows 8.1 和 Windows Server 2012 R2 中的作業系統版本變更</span><span class="sxs-lookup"><span data-stu-id="8f8e4-103">Operating system version changes in Windows 8.1 and Windows Server 2012 R2</span></span>

## <a name="platforms"></a><span data-ttu-id="8f8e4-104">平台</span><span class="sxs-lookup"><span data-stu-id="8f8e4-104">Platforms</span></span>

<span data-ttu-id="8f8e4-105">**用戶端-** Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="8f8e4-105">**Clients -** Windows 8.1</span></span>

<span data-ttu-id="8f8e4-106">**伺服器-** Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="8f8e4-106">**Servers -** Windows Server 2012 R2</span></span>

## <a name="description"></a><span data-ttu-id="8f8e4-107">Description</span><span class="sxs-lookup"><span data-stu-id="8f8e4-107">Description</span></span>

<span data-ttu-id="8f8e4-108">我們對 GetVersion (的) Api 在 Windows 8.1 中的運作方式有所重大變更，是因為在過去的 GetVersion (範例) Api 的使用方式所造成的不良客戶行為。</span><span class="sxs-lookup"><span data-stu-id="8f8e4-108">We have made some significant changes in how the GetVersion(Ex) APIs work in Windows 8.1 due to undesirable customer behaviors resulting from how the GetVersion(Ex) APIs have been used in the past.</span></span>

<span data-ttu-id="8f8e4-109">在舊版的 Windows 中，呼叫 GetVersion (例如) Api 會傳回實際版本的作業系統 (OS) ，除非應用程式相容性填充碼已減輕進程，以提供不同的版本。</span><span class="sxs-lookup"><span data-stu-id="8f8e4-109">In previous versions of Windows, calling the GetVersion(Ex) APIs would return the actual version of the operating system (OS), unless the process had been mitigated by an app compat shim to give it a different version.</span></span> <span data-ttu-id="8f8e4-110">這是以暫時性的方式完成，而且相對於 Microsoft 在版本中可合理填充碼的進程數目。</span><span class="sxs-lookup"><span data-stu-id="8f8e4-110">This was done on a provisional basis and was relatively incomplete in terms of the number of processes that Microsoft could reasonably shim in a release.</span></span> <span data-ttu-id="8f8e4-111">許多應用程式會因為版本檢查的設計不佳而無法填充，所以會有許多應用程式被破解。</span><span class="sxs-lookup"><span data-stu-id="8f8e4-111">Many applications fell through the cracks because they didn’t get shimmed due to poorly designed version checks.</span></span>

<span data-ttu-id="8f8e4-112">進行版本檢查的其中一個原因是要警告使用者應用程式必須在較新版本的 OS 上執行。</span><span class="sxs-lookup"><span data-stu-id="8f8e4-112">The number one reason to do a version check is to warn the user that the application needs to run on a newer version of the OS.</span></span> <span data-ttu-id="8f8e4-113">不過，由於檢查不佳，應用程式通常會錯誤地警告他們需要在 Windows XP 或更新版本上執行，這當然是最新的作業系統。</span><span class="sxs-lookup"><span data-stu-id="8f8e4-113">However due to poor checks, apps would often incorrectly warn that they needed to be run on Windows XP or later, which of course the newest OS is.</span></span> <span data-ttu-id="8f8e4-114">比起，最新的 OS 會在沒有任何問題的情況下執行應用程式（如果沒有這些檢查的話）。</span><span class="sxs-lookup"><span data-stu-id="8f8e4-114">More often than not, the newest OS would run the application without any issues if not for these checks.</span></span>

## <a name="manifestation"></a><span data-ttu-id="8f8e4-115">表現</span><span class="sxs-lookup"><span data-stu-id="8f8e4-115">Manifestation</span></span>

<span data-ttu-id="8f8e4-116">在 Windows 8.1 中，GetVersion (例如) Api 已被取代。</span><span class="sxs-lookup"><span data-stu-id="8f8e4-116">In Windows 8.1, the GetVersion(Ex) APIs have been deprecated.</span></span> <span data-ttu-id="8f8e4-117">這表示，雖然您仍可呼叫這些 API 函式，但如果您的應用程式並未特別以 Windows 8.1 為目標，則函式會傳回 Windows 8 版本 (6.2) 。</span><span class="sxs-lookup"><span data-stu-id="8f8e4-117">That means that while you can still call these API functions, if your app does not specifically target Windows 8.1, the functions will return the Windows 8 version (6.2).</span></span>

## <a name="solution"></a><span data-ttu-id="8f8e4-118">解決方法</span><span class="sxs-lookup"><span data-stu-id="8f8e4-118">Solution</span></span>

### <a name="adding-an-app-manifest"></a><span data-ttu-id="8f8e4-119">新增應用程式資訊清單</span><span class="sxs-lookup"><span data-stu-id="8f8e4-119">Adding an app manifest</span></span>

<span data-ttu-id="8f8e4-120">為了讓您的應用程式以 Windows 8.1 為目標，您必須在應用程式的可執行檔 [) 資訊清單中包含應用程式 (可執行檔](/windows/compatibility/application-executable-manifest) 。</span><span class="sxs-lookup"><span data-stu-id="8f8e4-120">In order for your app to target Windows 8.1, you'll need to include an [app (executable) manifest](/windows/compatibility/application-executable-manifest) for the app's executable.</span></span> <span data-ttu-id="8f8e4-121">然後，在資訊清單的 [ [ **&lt; 相容性 &gt;** ] 區段](../SbsCs/application-manifests.md#compatibility)中，您必須為您想要宣告應用程式支援的每個 Windows 版本新增 **&lt; supportedOS &gt;** 元素。</span><span class="sxs-lookup"><span data-stu-id="8f8e4-121">Then, in the [**&lt;compatibility&gt;** section](../SbsCs/application-manifests.md#compatibility) of the manifest, you'll need to add a **&lt;supportedOS&gt;** element for each Windows version you want to declare that your app supports.</span></span>

<span data-ttu-id="8f8e4-122">下列範例會顯示應用程式的應用程式資訊清單檔，以支援從 Windows Vista 到 Windows 8.1 的所有 Windows 版本：</span><span class="sxs-lookup"><span data-stu-id="8f8e4-122">The following example shows an app manifest file for an app that supports all versions of Windows from Windows Vista to Windows 8.1:</span></span>

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
            <!-- Windows 8.1 -->
            <supportedOS Id="{1f676c76-80e1-4239-95bb-83d0f6d0da78}"/> <!-- * ADD THIS LINE * -->
            <!-- Windows 8 -->
            <supportedOS Id="{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}"/>
            <!-- Windows 7 -->
            <supportedOS Id="{35138b9a-5d96-4fbd-8e2d-a2440225f93a}"/>
            <!-- Windows Vista -->
            <supportedOS Id="{e2011457-1546-43c5-a5fe-008deee3d3f0}"/> 
        </application>
    </compatibility>
</assembly>
```

<span data-ttu-id="8f8e4-123">上方標示的 `* ADD THIS LINE *` 程式碼顯示如何正確地以應用程式為目標，以進行 Windows 8.1。</span><span class="sxs-lookup"><span data-stu-id="8f8e4-123">The line above marked `* ADD THIS LINE *` shows how to accurately target your application for Windows 8.1.</span></span>

<span data-ttu-id="8f8e4-124">在舊版作業系統上執行您的應用程式時，在您的應用程式資訊清單中宣告 Windows 8.1 的支援將不會有任何作用。</span><span class="sxs-lookup"><span data-stu-id="8f8e4-124">Declaring support for Windows 8.1 in your app manifest will not have any effect when running your app on previous operating systems.</span></span>

### <a name="using-versionhelpers-instead-of-getversionex"></a><span data-ttu-id="8f8e4-125">使用 VersionHelpers 而非 GetVersion (例如) </span><span class="sxs-lookup"><span data-stu-id="8f8e4-125">Using VersionHelpers instead of GetVersion(Ex)</span></span>

<span data-ttu-id="8f8e4-126">Windows 8.1 引進適用于 GetVersion 的新取代 API 函數 (例如) ，稱為 VersionHelpers。</span><span class="sxs-lookup"><span data-stu-id="8f8e4-126">Windows 8.1 introduces new replacement API functions for GetVersion(Ex), known as VersionHelpers.</span></span> <span data-ttu-id="8f8e4-127">它們非常容易使用;您只需要這麼做 `#include <VersionHelpers.h>` 。</span><span class="sxs-lookup"><span data-stu-id="8f8e4-127">They are extremely easy to use; all you have to do is `#include <VersionHelpers.h>`.</span></span> <span data-ttu-id="8f8e4-128">VersionHelpers .h 標頭檔中提供的內嵌函式可讓您的程式碼詢問作業系統是指定的 Windows 版本或更新版本。</span><span class="sxs-lookup"><span data-stu-id="8f8e4-128">The inline functions available in the VersionHelpers.h header file allow your code to ask whether the operating system is a given version of Windows or later.</span></span>

<span data-ttu-id="8f8e4-129">**範例** 例如，如果您的應用程式需要 Windows 8 或更新版本，請使用下列測試：</span><span class="sxs-lookup"><span data-stu-id="8f8e4-129">**Example** For example, if your application requires Windows 8 or later, use the following test:</span></span>

```cpp
#include <VersionHelpers.h>
// ...
    if (!IsWindows8OrGreater())
    {
       MessageBox(NULL, "You need at least Windows 8", "Version Not Supported", MB_OK);
    }
```

<span data-ttu-id="8f8e4-130">可用的 VersionHelper API 函數包括：</span><span class="sxs-lookup"><span data-stu-id="8f8e4-130">The available VersionHelper API functions are:</span></span>

```c
#define VERSIONHELPERAPI FORCEINLINE BOOL
VERSIONHELPERAPI IsWindowsXPOrGreater();
VERSIONHELPERAPI IsWindowsXPSP1OrGreater();
VERSIONHELPERAPI IsWindowsXPSP2OrGreater();
VERSIONHELPERAPI IsWindowsXPSP3OrGreater();
VERSIONHELPERAPI IsWindowsVistaOrGreater();
VERSIONHELPERAPI IsWindowsVistaSP1OrGreater();
VERSIONHELPERAPI IsWindowsVistaSP2OrGreater();
VERSIONHELPERAPI IsWindows7OrGreater();
VERSIONHELPERAPI IsWindows7SP1OrGreater();
VERSIONHELPERAPI IsWindows8OrGreater();
VERSIONHELPERAPI IsWindows8Point1OrGreater();
VERSIONHELPERAPI IsWindowsServer();
```

<span data-ttu-id="8f8e4-131">根據您提出的問題，這些值會傳回 TRUE 或 FALSE，而您只需要定義所支援的最低層級作業系統。</span><span class="sxs-lookup"><span data-stu-id="8f8e4-131">They will return TRUE or FALSE depending on the question you are asking, and you only need to define the minimum level operating system that you support.</span></span>

## <a name="resources"></a><span data-ttu-id="8f8e4-132">資源</span><span class="sxs-lookup"><span data-stu-id="8f8e4-132">Resources</span></span>

-   [<span data-ttu-id="8f8e4-133">應用程式相容性工具組下載</span><span class="sxs-lookup"><span data-stu-id="8f8e4-133">Application Compatibility Toolkit Download</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyId=24DA89E9-B581-47B0-B45E-492DD6DA2971)
-   <span data-ttu-id="8f8e4-134">[已知的相容性修正程式、相容性模式和 AppHelp 訊息](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="8f8e4-134">[Known Compatibility Fixes, Compatibility Modes, and AppHelp Messages](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))</span></span>
-   [<span data-ttu-id="8f8e4-135">VersionHelpers Api</span><span class="sxs-lookup"><span data-stu-id="8f8e4-135">VersionHelpers APIs</span></span>](../sysinfo/version-helper-apis.md)
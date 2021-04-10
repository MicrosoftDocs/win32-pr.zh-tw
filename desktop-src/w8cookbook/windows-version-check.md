---
title: Windows 版本檢查
description: 作業系統版本已隨著 Windows 10 作業系統版本而遞增。
ms.assetid: 55BB7B44-1AFD-456D-9380-38B4D26E5EF6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93ea1e65ed97859486bdd0a18fe53ee44a653faf
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/09/2020
ms.locfileid: "104093451"
---
# <a name="windows-version-check"></a><span data-ttu-id="34809-103">Windows 版本檢查</span><span class="sxs-lookup"><span data-stu-id="34809-103">Windows version check</span></span>

<span data-ttu-id="34809-104">作業系統版本已隨著 Windows 10 作業系統版本而遞增。</span><span class="sxs-lookup"><span data-stu-id="34809-104">The OS version has been incremented with the Windows 10 OS release.</span></span> <span data-ttu-id="34809-105">這表示 Windows 10 的內部版本號碼也已變更為10.0。</span><span class="sxs-lookup"><span data-stu-id="34809-105">This means that the internal version number for Windows 10 has also been changed to 10.0.</span></span> <span data-ttu-id="34809-106">在過去，於 OS 版本變更之後，我們需要竭盡全力地維持應用程式與裝置相容性。</span><span class="sxs-lookup"><span data-stu-id="34809-106">As in the past, we go to great lengths to maintain application and device compatibility after an OS version change.</span></span> <span data-ttu-id="34809-107">對於大部分的應用程式類別 (沒有任何核心相依性) 變更將不會對應用程式功能造成負面影響，而且現有的應用程式在 Windows 10 上將繼續正常運作。</span><span class="sxs-lookup"><span data-stu-id="34809-107">For most app categories (without any kernel dependencies) the change will not negatively impact app functionality, and existing apps will continue to work fine on Windows 10.</span></span>

## <a name="manifestations"></a><span data-ttu-id="34809-108">表現</span><span class="sxs-lookup"><span data-stu-id="34809-108">Manifestations</span></span>

<span data-ttu-id="34809-109">此變更的表現是依 App 而定。</span><span class="sxs-lookup"><span data-stu-id="34809-109">The manifestation of this change is app-specific.</span></span> <span data-ttu-id="34809-110">這表示任何會特別檢查 OS 版本的 app 將會取得較高的版本號碼，這可能導致下列一或多種情況：</span><span class="sxs-lookup"><span data-stu-id="34809-110">This means any app that specifically checks for the OS version will get a higher version number, which can lead to one or more of the following situations:</span></span>

-   <span data-ttu-id="34809-111">App 安裝程式可能無法安裝 app，且 app 可能無法啟動。</span><span class="sxs-lookup"><span data-stu-id="34809-111">App installers might not be able to install the app, and apps might not be able to start.</span></span>
-   <span data-ttu-id="34809-112">App 可能會不穩定或當機。</span><span class="sxs-lookup"><span data-stu-id="34809-112">Apps might become unstable or crash.</span></span>
-   <span data-ttu-id="34809-113">App 可能會產生錯誤訊息，但會繼續正常運作。</span><span class="sxs-lookup"><span data-stu-id="34809-113">Apps might generate error messages, but continue to function properly.</span></span>

<span data-ttu-id="34809-114">某些 app 會執行版本檢查，並傳遞警告給使用者。</span><span class="sxs-lookup"><span data-stu-id="34809-114">Some apps perform a version check and simply pass a warning to users.</span></span> <span data-ttu-id="34809-115">不過，有些 app 會與版本檢查緊密繫結 (於驅動程式或是核心模式中以避免偵測)。</span><span class="sxs-lookup"><span data-stu-id="34809-115">However, there are apps that are bound very tightly to a version check (in the drivers, or in kernel mode to avoid detection).</span></span> <span data-ttu-id="34809-116">在這些情況中，如果找到不正確的版本，app 將會失敗。</span><span class="sxs-lookup"><span data-stu-id="34809-116">In these cases, the app will fail if an incorrect version is found.</span></span> <span data-ttu-id="34809-117">相較於版本檢查，我們建議下列其中一種方法：</span><span class="sxs-lookup"><span data-stu-id="34809-117">Rather than a version check, we recommend one of the following approaches:</span></span>

-   <span data-ttu-id="34809-118">如果 app 依存於特定的 API 功能，請確定您有將正確的 API 版本作為目標。</span><span class="sxs-lookup"><span data-stu-id="34809-118">If the app is dependent on specific API functionality, ensure you target the correct API version.</span></span>
-   <span data-ttu-id="34809-119">NTDDI (NT 設備磁碟機介面) 版本號碼會在 API 中的目標功能變更時遞增。</span><span class="sxs-lookup"><span data-stu-id="34809-119">NTDDI (NT device driver interface) version number will increment only if target functionality in the API changes.</span></span> <span data-ttu-id="34809-120">請確定您透過 APISet 或功能小組所建立的其他公開 API 偵測到變更，而且不使用版本作為某些功能或修正的 proxy。</span><span class="sxs-lookup"><span data-stu-id="34809-120">Ensure you detect the change via APISet or other exposed API as created by the feature team, and do not use the version as a proxy for some feature or fix.</span></span> <span data-ttu-id="34809-121">如果有重大變更，且並未適當檢查，該變更就會變成是錯誤。</span><span class="sxs-lookup"><span data-stu-id="34809-121">If there are breaking changes and a proper check is not exposed, then that is a bug.</span></span>
-   <span data-ttu-id="34809-122">確定應用程式不會以奇怪的方式檢查版本，例如透過登錄、檔案版本、位移、核心模式、驅動程式或其他方式。</span><span class="sxs-lookup"><span data-stu-id="34809-122">Ensure the app does NOT check for version in odd ways, such as via the registry, file versions, offsets, kernel mode, drivers or other means.</span></span> <span data-ttu-id="34809-123">如果應用程式確實需要檢查版本，請使用 GetVersion Api，這應該會傳回主要、次要和組建編號。</span><span class="sxs-lookup"><span data-stu-id="34809-123">If the app absolutely needs to check the version, use the GetVersion APIs, which should return the major, minor and build number.</span></span>
-   <span data-ttu-id="34809-124">如果您使用 GetVersion API 或其他版本協助程式函式（例如 [VerifyVersionInfo](/windows/desktop/api/winbase/nf-winbase-verifyversioninfoa)），請記住此 API 的行為已從 Windows 8.1 開始變更。</span><span class="sxs-lookup"><span data-stu-id="34809-124">If you are using the GetVersion API or other Version Helper functions such as [VerifyVersionInfo](/windows/desktop/api/winbase/nf-winbase-verifyversioninfoa), remember that the behavior of this API has changed starting with Windows 8.1.</span></span> <span data-ttu-id="34809-125">如需詳細資訊，請參閱 [API 檔](../SysInfo/version-helper-apis.md) 。</span><span class="sxs-lookup"><span data-stu-id="34809-125">Please refer to [the API documentation](../SysInfo/version-helper-apis.md) for more details.</span></span>
-   <span data-ttu-id="34809-126">如果您擁有像是反惡意程式碼或防火牆的應用程式，則應該透過 Windows 測試人員程式來完成您一般的意見反應通道。</span><span class="sxs-lookup"><span data-stu-id="34809-126">If you own apps such as antimalware or firewall, you should work through your usual feedback channels and via the Windows Insider program.</span></span>

## <a name="declaring-windows-10-compatibility-with-an-app-manifest"></a><span data-ttu-id="34809-127">宣告與應用程式資訊清單 Windows 10 的相容性</span><span class="sxs-lookup"><span data-stu-id="34809-127">Declaring Windows 10 Compatibility With An App Manifest</span></span>

<span data-ttu-id="34809-128">如果您的應用程式與 Windows 10 相容，則可在應用程式的可 [執行檔) 資訊清單](/windows/compatibility/application-executable-manifest) 中宣告這項事實 (可執行檔。</span><span class="sxs-lookup"><span data-stu-id="34809-128">If your app is compatible with Windows 10, it can declare this fact in the [app (executable) manifest](/windows/compatibility/application-executable-manifest) for the app's executable.</span></span> <span data-ttu-id="34809-129">這會告訴系統您的應用程式瞭解 Windows 10 的系統版本號碼 10.0 (因此，GetVersion API 不會傳回舊版) ，也可讓系統關閉未宣告 Windows 10 相容性之應用程式的其他相容性行為。</span><span class="sxs-lookup"><span data-stu-id="34809-129">This tells the system that your app understands Windows 10's system version number of 10.0 (so the GetVersion API does not return an earlier version), and also lets the system turn off other compatibility behaviors applied to apps that don't declare Windows 10 compatibility.</span></span>

<span data-ttu-id="34809-130">若要在應用程式資訊清單中宣告 Windows 10 相容性，您必須加入資訊清單的 [ **&lt; 相容性 &gt;** 區段](../SbsCs/application-manifests.md#compatibility)（如果尚未存在），然後 Windows 10 為您要宣告的應用程式所支援的每個 Windows 版本新增 **&lt; supportedOS &gt;** 元素。</span><span class="sxs-lookup"><span data-stu-id="34809-130">To declare Windows 10 compatibility in an app manifest, you'll need to add a [**&lt;compatibility&gt;** section](../SbsCs/application-manifests.md#compatibility) of the manifest if one does not already exist, and then add **&lt;supportedOS&gt;** elements for Windows 10 and every other Windows version you want to declare that your app supports.</span></span>

<span data-ttu-id="34809-131">下列範例會顯示應用程式的應用程式資訊清單檔，以支援從 Windows Vista 到 Windows 10 的所有 Windows 版本：</span><span class="sxs-lookup"><span data-stu-id="34809-131">The following example shows an app manifest file for an app that supports all versions of Windows from Windows Vista to Windows 10:</span></span>

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
            <supportedOS Id="{8e0f7a12-bfb3-4fe8-b9a5-48fd50a15a9a}"/> <!-- * ADD THIS LINE * -->
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
</assembly>
```

<span data-ttu-id="34809-132">上方標示的 `* ADD THIS LINE *` 程式碼顯示如何正確地以應用程式為目標，以進行 Windows 10。</span><span class="sxs-lookup"><span data-stu-id="34809-132">The line above marked `* ADD THIS LINE *` shows how to accurately target your application for Windows 10.</span></span>

<span data-ttu-id="34809-133">在舊版作業系統上執行您的應用程式時，在您的應用程式資訊清單中宣告 Windows 10 的支援將不會有任何作用。</span><span class="sxs-lookup"><span data-stu-id="34809-133">Declaring support for Windows 10 in your app manifest will not have any effect when running your app on previous operating systems.</span></span>

## <a name="resources"></a><span data-ttu-id="34809-134">資源</span><span class="sxs-lookup"><span data-stu-id="34809-134">Resources</span></span>

-   [<span data-ttu-id="34809-135">應用程式相容性工具組下載：下載適用于 Windows 10 的 Windows ADK</span><span class="sxs-lookup"><span data-stu-id="34809-135">Application Compatibility Toolkit Download: Download the Windows ADK for Windows 10</span></span>](https://download.microsoft.com/download/9/A/E/9AE69DD5-BA93-44E0-864E-180F5E700AB4/adk/adksetup.exe)
-   <span data-ttu-id="34809-136">[已知的相容性修正程式、相容性模式和 AppHelp 訊息](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="34809-136">[Known Compatibility Fixes, Compatibility Modes, and AppHelp Messages](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))</span></span>
-   [<span data-ttu-id="34809-137">版本協助程式 API</span><span class="sxs-lookup"><span data-stu-id="34809-137">Version Helpers API</span></span>](../sysinfo/version-helper-apis.md)
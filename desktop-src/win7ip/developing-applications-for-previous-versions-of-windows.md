---
title: 開發舊版 Windows 的應用程式
description: 說明如何開發在舊版 Windows 上執行的應用程式，並利用適用于 Windows Vista 的平臺更新所支援的 API，以及 Windows Server 2008 的平臺更新。
ms.assetid: 9c46f894-e5cd-46a1-81c8-f63b09504735
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 299d4c61b0e2b931c3833934c843bf964fc3fa7c
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/06/2021
ms.locfileid: "104386340"
---
# <a name="developing-applications-for-previous-versions-of-windows"></a><span data-ttu-id="94230-103">開發舊版 Windows 的應用程式</span><span class="sxs-lookup"><span data-stu-id="94230-103">Developing Applications for Previous Versions of Windows</span></span>

<span data-ttu-id="94230-104">說明如何開發在舊版 Windows 上執行的應用程式，並利用適用于 Windows Vista 的平臺更新所支援的 API，以及 Windows Server 2008 的平臺更新。</span><span class="sxs-lookup"><span data-stu-id="94230-104">Explains what to do to develop applications that run on previous versions of Windows and take advantage of the API that are supported with the Platform Update for Windows Vista and the Platform Update for Windows Server 2008.</span></span>

## <a name="required-downloads"></a><span data-ttu-id="94230-105">必要的下載</span><span class="sxs-lookup"><span data-stu-id="94230-105">Required Downloads</span></span>

<span data-ttu-id="94230-106">如果您想要開發的應用程式使用 Microsoft Windows 軟體開發套件 (SDK) （適用于 Windows 7）所引進的 API，則需要下載並安裝下列各節所述的套件。</span><span class="sxs-lookup"><span data-stu-id="94230-106">Download and installation of the packages described in the following sections is required if you want to develop applications that use API that are introduced with the Microsoft Windows Software Development Kit (SDK) for Windows 7.</span></span>

### <a name="microsoft-windows-sdk"></a><span data-ttu-id="94230-107">Microsoft Windows SDK</span><span class="sxs-lookup"><span data-stu-id="94230-107">Microsoft Windows SDK</span></span>

<span data-ttu-id="94230-108">需要 Windows 7 的 Windows SDK，才能建立應用程式，以使用適用于 Windows Vista 的平臺更新所支援的 Api 和 Windows Server 2008 的平臺更新。</span><span class="sxs-lookup"><span data-stu-id="94230-108">The Windows SDK for Windows 7 is required for creating applications that use APIs supported with the Platform Update for Windows Vista and the Platform Update for Windows Server 2008.</span></span>

<span data-ttu-id="94230-109">如需存取其他資源和資訊，例如下載、論壇文章和 Windows SDK team blog，請參閱 [Windows SDK 開發人員中心](https://msdn.microsoft.com/bb980924.aspx) (https://msdn.microsoft.com/bb980924.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="94230-109">For access to additional resources and information, such as downloads, forum posts, and the Windows SDK team blog, see the [Windows SDK Developer Center](https://msdn.microsoft.com/bb980924.aspx) (https://msdn.microsoft.com/bb980924.aspx).</span></span>

### <a name="net-framework"></a><span data-ttu-id="94230-110">.NET Framework</span><span class="sxs-lookup"><span data-stu-id="94230-110">.NET Framework</span></span>

<span data-ttu-id="94230-111">若要建立應用程式，以使用適用于 Windows Vista 的平臺更新和 Windows Server 2008 的平臺更新所支援的 Api，則需要 .NET Framework 3.5 Service Pack 1。</span><span class="sxs-lookup"><span data-stu-id="94230-111">The .NET Framework 3.5 Service Pack 1 is required for creating applications that use APIs supported by the Platform Update for Windows Vista and the Platform Update for Windows Server 2008.</span></span>

<span data-ttu-id="94230-112">如需其他資源和資訊，請參閱 [.NET Framework 開發人員中心](https://msdn.microsoft.com/netframework/default.aspx) (https://msdn.microsoft.com/netframework/default.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="94230-112">For additional resources and information, see the [.NET Framework Developer Center](https://msdn.microsoft.com/netframework/default.aspx) (https://msdn.microsoft.com/netframework/default.aspx).</span></span>

### <a name="directx-sdk-required-when-using-direct3d"></a><span data-ttu-id="94230-113">使用 Direct3D 時需要 DirectX SDK</span><span class="sxs-lookup"><span data-stu-id="94230-113">DirectX SDK Required When Using Direct3D</span></span>

<span data-ttu-id="94230-114">如果您建立使用 Direct3D 的應用程式，則需要 [DIRECTX SDK](/previous-versions/windows/apps/hh452744(v=win.10)) (， https://msdn.microsoft.com/directx/aa937788.aspx) 才能建立使用 Windows Vista 平臺更新所支援 api 的應用程式，以及適用于 windows Server 2008 的平臺更新。</span><span class="sxs-lookup"><span data-stu-id="94230-114">If you create applications that use Direct3D, the [DirectX SDK](/previous-versions/windows/apps/hh452744(v=win.10)) (https://msdn.microsoft.com/directx/aa937788.aspx) is required for creating applications that use APIs supported by the Platform Update for Windows Vista and the Platform Update for Windows Server 2008.</span></span>

### <a name="update-your-development-computer"></a><span data-ttu-id="94230-115">更新您的開發電腦</span><span class="sxs-lookup"><span data-stu-id="94230-115">Update Your Development Computer</span></span>

<span data-ttu-id="94230-116">確定您的開發電腦具有來自 Windows Update 的所有最新更新。</span><span class="sxs-lookup"><span data-stu-id="94230-116">Ensure that your development computer has all of the latest updates from Windows Update.</span></span>

<span data-ttu-id="94230-117">如果您是在舊版的 Windows 上開發應用程式，您必須從 Windows Update 取得 Windows Vista 的平臺更新或 Windows Server 2008 更新的平臺更新。</span><span class="sxs-lookup"><span data-stu-id="94230-117">If you are developing applications on a previous version of Windows, you must obtain the Platform Update for Windows Vista or the Platform Update for Windows Server 2008 update from Windows Update.</span></span> <span data-ttu-id="94230-118">安裝其中一個更新可讓您利用 Windows 7 的 Windows SDK 所提供的新 API。</span><span class="sxs-lookup"><span data-stu-id="94230-118">Installing either of these updates will enable you to take advantage of the new API provided by the Windows SDK for Windows 7.</span></span>

<span data-ttu-id="94230-119">如需有關如何從 Windows Update 取得更新的詳細資訊，請參閱知識庫檔， [瞭解 Windows Vista 的平臺更新 (KB 971644) ](https://support.microsoft.com/kb/971644) (https://support.microsoft.com/kb/971644) 。</span><span class="sxs-lookup"><span data-stu-id="94230-119">For more information about how to obtain updates from Windows Update see the [Knowledge Base article about the Platform Update for Windows Vista (KB 971644)](https://support.microsoft.com/kb/971644) (https://support.microsoft.com/kb/971644).</span></span>

## <a name="development-environment"></a><span data-ttu-id="94230-120">開發環境</span><span class="sxs-lookup"><span data-stu-id="94230-120">Development Environment</span></span>

### <a name="set-the-build-target-to-windows-7"></a><span data-ttu-id="94230-121">將組建目標設定為 Windows 7</span><span class="sxs-lookup"><span data-stu-id="94230-121">Set the Build Target to Windows 7</span></span>

<span data-ttu-id="94230-122">在 Windows Vista 的平臺更新中使用程式庫的所有應用程式都必須針對 Windows 7 目標平臺建立。</span><span class="sxs-lookup"><span data-stu-id="94230-122">All applications that use libraries in the Platform Update for Windows Vista must be built against the Windows 7 target platform.</span></span>

<span data-ttu-id="94230-123">將 WINVER 設定為 [Windows 7 目標平臺] 值，可讓您開發應用程式，在執行 Windows Vista 的開發電腦上，使用適用于 Windows Vista 的平臺更新或 Windows Server 2008 平臺更新所支援的 Api。</span><span class="sxs-lookup"><span data-stu-id="94230-123">Setting WINVER to the Windows 7 target platform value enables you to develop applications that use APIs supported with the Platform Update for Windows Vista or the Platform Update for Windows Server 2008 on a development machine running Windows Vista.</span></span>

<span data-ttu-id="94230-124">您可以在原始程式碼中，或使用/D 選項搭配 Visual Studio 編譯器，將目標平臺設定為 Windows 7。</span><span class="sxs-lookup"><span data-stu-id="94230-124">You can set the target platform to Windows 7 either in your source code or by using the /D option with the Visual Studio compiler.</span></span>

<span data-ttu-id="94230-125">下列範例顯示如何在原始程式碼中設定 WINVER。</span><span class="sxs-lookup"><span data-stu-id="94230-125">The following example shows how to set WINVER in your source code.</span></span>


```C++
#define WINVER 0x0601
```



<span data-ttu-id="94230-126">下列範例顯示如何使用/D 編譯器選項設定 WINVER。</span><span class="sxs-lookup"><span data-stu-id="94230-126">The following example shows how to set WINVER using the /D compiler option.</span></span>

``` syntax
/DWINVER=0x0601
```

## <a name="application-deployment"></a><span data-ttu-id="94230-127">應用程式部署</span><span class="sxs-lookup"><span data-stu-id="94230-127">Application Deployment</span></span>

<span data-ttu-id="94230-128">如果您使用 Windows 7 的 Windows SDK 所提供的標頭和程式庫來建立應用程式，支援的 Api 將會在已安裝 Windows Vista 或 Windows Server 2008 平臺更新的任何 Windows 版本上執行。</span><span class="sxs-lookup"><span data-stu-id="94230-128">If you build your application using the headers and libraries provided by the Windows SDK for Windows 7, supported APIs will run on any Windows version that has the Platform Update for Windows Vista or the Platform Update for Windows Server 2008 installed.</span></span>

> [!Note]  
> <span data-ttu-id="94230-129">適用于 Windows Vista 的平臺更新或 Windows Server 2008 平臺更新所支援之某些 Api 的行為、效能或需求可能會因不同的 Windows 版本而異。</span><span class="sxs-lookup"><span data-stu-id="94230-129">The behavior, performance, or requirements for some APIs that are supported with the Platform Update for Windows Vista or the Platform Update for Windows Server 2008 may vary across different versions of Windows.</span></span> <span data-ttu-id="94230-130">如需有關更新所支援之特定 API 的詳細資訊，請參閱 [關於 Windows Vista 的平臺更新](platform-update-for-windows-vista-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="94230-130">For details about a specific API that is supported by the updates, see [About Platform Update for Windows Vista](platform-update-for-windows-vista-overview.md).</span></span>

 

### <a name="no-redistributable-components"></a><span data-ttu-id="94230-131">沒有可轉散發元件</span><span class="sxs-lookup"><span data-stu-id="94230-131">No Redistributable Components</span></span>

<span data-ttu-id="94230-132">您的應用程式不需要安裝可轉散發元件，例如 Dll 或其他執行時間檔案。</span><span class="sxs-lookup"><span data-stu-id="94230-132">Your application does not need to install redistributable components, such as DLLs or other run-time files.</span></span>

### <a name="requires-updated-end-user-computer"></a><span data-ttu-id="94230-133">需要更新的 End-User 電腦</span><span class="sxs-lookup"><span data-stu-id="94230-133">Requires Updated End-User Computer</span></span>

<span data-ttu-id="94230-134">由於 Windows Vista 的平臺更新和 Windows Server 2008 的平臺更新是由 Windows Update 所裝載，因此啟用自動更新的使用者很有可能已經有這些更新以及必要的 service pack。</span><span class="sxs-lookup"><span data-stu-id="94230-134">Because Platform Update for Windows Vista and Platform Update for Windows Server 2008 are hosted by Windows Update, end-users with automatic updates enabled are highly likely to already have these updates as well as the required service packs.</span></span>

<span data-ttu-id="94230-135">如果使用者的電腦未安裝 Windows Vista 或 Windows Server 2008 的平臺更新，且您的應用程式需要支援這些更新的 Api，則您的應用程式可能無法在終端使用者的電腦上執行，或在執行期間可能會發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="94230-135">If the end-user's computer does not have Platform Update for Windows Vista or Platform Update for Windows Server 2008 installed and your application requires APIs that are supported with these updates, your application may not be able to run on the end-user's computer or may encounter errors during execution.</span></span>

<span data-ttu-id="94230-136">為了避免使用者電腦過期所造成的問題，您想要在應用程式安裝期間，確認您的使用者電腦具有適用于 Windows Vista 的平臺更新或 Windows Server 2008 更新的平臺更新。</span><span class="sxs-lookup"><span data-stu-id="94230-136">To avoid the problems that could be caused by your user's computer being out-of-date, you want to verify that your user's computer has the Platform Update for Windows Vista or the Platform Update for Windows Server 2008 update during the installation of your application.</span></span> <span data-ttu-id="94230-137">您可以使用 [Windows Update AGENT API](/windows/desktop/Wua_Sdk/portal-client) 來檢查終端使用者的電腦是否有安裝的更新。</span><span class="sxs-lookup"><span data-stu-id="94230-137">You can use the [Windows Update Agent API](/windows/desktop/Wua_Sdk/portal-client) to check your end-user's computer for installed updates.</span></span> <span data-ttu-id="94230-138">如果使用者尚未安裝更新，您也可以在應用程式安裝期間使用 Windows Update Agent API 來下載並安裝必要的更新。</span><span class="sxs-lookup"><span data-stu-id="94230-138">You can also use the Windows Update Agent API to download and install required updates during application installation if the end-user has not already installed the updates.</span></span>

<span data-ttu-id="94230-139">如需示範如何使用[Windows Update 代理程式 API](/windows/desktop/Wua_Sdk/portal-client)的安裝程式範例，請參閱[DirectX SDK](/previous-versions/windows/apps/hh452744(v=win.10)) (中[適用于遊戲開發人員的 Direct3D 11 部署](../direct3darticles/direct3d11-deployment.md) https://msdn.microsoft.com/directx/aa937788.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="94230-139">For an example of an installer that demonstrates how to use the [Windows Update Agent API](/windows/desktop/Wua_Sdk/portal-client), see [Direct3D 11 Deployment for Game Developers](../direct3darticles/direct3d11-deployment.md) in the [DirectX SDK](/previous-versions/windows/apps/hh452744(v=win.10)) (https://msdn.microsoft.com/directx/aa937788.aspx).</span></span>

<span data-ttu-id="94230-140">雖然適用于 [遊戲開發人員的 Direct3D 11 部署](../direct3darticles/direct3d11-deployment.md)中所討論的 D3D11InstallHelper 安裝程式範例是針對使用 direct3d 11 的應用程式所撰寫，但它提供了一個很好的範例，說明如何與 [Windows Update Agent API](/windows/desktop/Wua_Sdk/portal-client) 互動，以起始和追蹤 Windows Update 所裝載的更新下載與安裝。</span><span class="sxs-lookup"><span data-stu-id="94230-140">Although the D3D11InstallHelper installer sample that is discussed in [Direct3D 11 Deployment for Game Developers](../direct3darticles/direct3d11-deployment.md), was written for applications that use Direct3D 11, it provides a good example of how to interact with the [Windows Update Agent API](/windows/desktop/Wua_Sdk/portal-client) to initiate and track the download and installation of updates that are hosted by Windows Update.</span></span> <span data-ttu-id="94230-141">編譯此範例可能需要適用于 Windows 7 的 Windows SDK。</span><span class="sxs-lookup"><span data-stu-id="94230-141">Compiling this sample may require the Windows SDK for Windows 7.</span></span> <span data-ttu-id="94230-142">如需 D3D11InstallHelper 範例的詳細資訊，包括已知問題，請參閱2009年8月的 [DIRECTX SDK](/previous-versions/windows/apps/hh452744(v=win.10)) (https://msdn.microsoft.com/directx/aa937788.aspx) 版本資訊。 Windows Vista 的平臺更新</span><span class="sxs-lookup"><span data-stu-id="94230-142">For additional information about the D3D11InstallHelper sample, including known issues, see the [DirectX SDK](/previous-versions/windows/apps/hh452744(v=win.10)) (https://msdn.microsoft.com/directx/aa937788.aspx) Release Notes for August 2009.Platform Update for Windows Vista</span></span>

## <a name="related-topics"></a><span data-ttu-id="94230-143">相關主題</span><span class="sxs-lookup"><span data-stu-id="94230-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94230-144">Windows Vista 的平臺更新</span><span class="sxs-lookup"><span data-stu-id="94230-144">Platform Update for Windows Vista</span></span>](platform-update-for-windows-vista-portal.md)
</dt> <dt>

<span data-ttu-id="94230-145">**概觀**</span><span class="sxs-lookup"><span data-stu-id="94230-145">**Overviews**</span></span>
</dt> <dt>

[<span data-ttu-id="94230-146">關於 Windows Vista 的平臺更新</span><span class="sxs-lookup"><span data-stu-id="94230-146">About Platform Update for Windows Vista</span></span>](platform-update-for-windows-vista-overview.md)
</dt> <dt>

[<span data-ttu-id="94230-147">適用于 Windows Vista 的平臺更新 (KB 971644) 的知識庫文章 </span><span class="sxs-lookup"><span data-stu-id="94230-147">Knowledge Base article about the Platform Update for Windows Vista (KB 971644)</span></span>](https://support.microsoft.com/kb/971644)
</dt> </dl>

 

 
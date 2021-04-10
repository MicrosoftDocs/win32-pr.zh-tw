---
title: 遊戲開發人員的 Direct3D 11 部署
description: 本文說明如何在必要時，將 Direct3D 11 元件部署到系統上。
ms.assetid: 1fd43638-0d67-4a94-3be6-8789095f491e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd935aedee23ba731bc74e52c0773e6f02e5b5fc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104186063"
---
# <a name="direct3d-11-deployment-for-game-developers"></a><span data-ttu-id="aa547-103">遊戲開發人員的 Direct3D 11 部署</span><span class="sxs-lookup"><span data-stu-id="aa547-103">Direct3D 11 deployment for game developers</span></span>

<span data-ttu-id="aa547-104">本文說明如何在必要時，將 Direct3D 11 元件部署到系統上。</span><span class="sxs-lookup"><span data-stu-id="aa547-104">This article describes how to deploy the Direct3D 11 components on a system if necessary.</span></span>

-   [<span data-ttu-id="aa547-105">概觀</span><span class="sxs-lookup"><span data-stu-id="aa547-105">Overview</span></span>](#overview)
-   [<span data-ttu-id="aa547-106">Direct3D 11。3</span><span class="sxs-lookup"><span data-stu-id="aa547-106">Direct3D 11.3</span></span>](#direct3d-113)
-   [<span data-ttu-id="aa547-107">Direct3D 11。2</span><span class="sxs-lookup"><span data-stu-id="aa547-107">Direct3D 11.2</span></span>](#direct3d-112)
-   [<span data-ttu-id="aa547-108">Direct3D 11。1</span><span class="sxs-lookup"><span data-stu-id="aa547-108">Direct3D 11.1</span></span>](#direct3d-111)
-   [<span data-ttu-id="aa547-109">D3D11InstallHelper.dll</span><span class="sxs-lookup"><span data-stu-id="aa547-109">D3D11InstallHelper.dll</span></span>](#d3d11installhelperdll)
-   [<span data-ttu-id="aa547-110">D3D11Install.exe</span><span class="sxs-lookup"><span data-stu-id="aa547-110">D3D11Install.exe</span></span>](#d3d11installexe)
-   [<span data-ttu-id="aa547-111">整合至安裝程式</span><span class="sxs-lookup"><span data-stu-id="aa547-111">Integrating into Installation Programs</span></span>](#integrating-into-installation-programs)
    -   [<span data-ttu-id="aa547-112">整合至 InstallShield</span><span class="sxs-lookup"><span data-stu-id="aa547-112">Integrating into InstallShield</span></span>](#integrating-into-installshield)
    -   [<span data-ttu-id="aa547-113">整合至 MSI 套件</span><span class="sxs-lookup"><span data-stu-id="aa547-113">Integrating into an MSI Package</span></span>](#integrating-into-an-msi-package)
-   [<span data-ttu-id="aa547-114">調試秘訣</span><span class="sxs-lookup"><span data-stu-id="aa547-114">Debugging Tips</span></span>](#debugging-tips)
-   [<span data-ttu-id="aa547-115">公司設定</span><span class="sxs-lookup"><span data-stu-id="aa547-115">Corporate Settings</span></span>](#corporate-settings)
-   [<span data-ttu-id="aa547-116">相關文章</span><span class="sxs-lookup"><span data-stu-id="aa547-116">Related Articles</span></span>](#related-articles)

## <a name="overview"></a><span data-ttu-id="aa547-117">概觀</span><span class="sxs-lookup"><span data-stu-id="aa547-117">Overview</span></span>

<span data-ttu-id="aa547-118">Direct3D 11 API 透過動態著色器連結，擴充了現有的 Direct3D 10.1 API，並支援多執行緒轉譯和資源建立、計算著色器、硬體鑲嵌、BC6H/BC7 材質壓縮和 HLSL 著色器模型5.0。</span><span class="sxs-lookup"><span data-stu-id="aa547-118">The Direct3D 11 API extends the existing Direct3D 10.1 API with support for multithreaded rendering and resource creation, Compute Shader, hardware tessellation, BC6H/BC7 texture compression, and HLSL Shader Model 5.0 with Dynamic Shader Linkage.</span></span> <span data-ttu-id="aa547-119">除了 Direct3D 11 元件之外，DirectX 11 執行時間還包含一些額外的圖形元件： Direct3D 11、DXGI 1.1、10level9 功能層級、WARP10 software 轉譯裝置、Direct2D、DirectWrite，以及支援10level9 和 WARP10 的更新 Direct3D 10.1。</span><span class="sxs-lookup"><span data-stu-id="aa547-119">In addition to the Direct3D 11 component, a number of additional graphics components are included in the DirectX 11 runtime: Direct3D 11, DXGI 1.1, 10level9 feature levels, WARP10 software rendering device, Direct2D, DirectWrite, and an updated Direct3D 10.1 with support for 10level9 and WARP10.</span></span> <span data-ttu-id="aa547-120">如需這些和其他 Windows 圖形元件的詳細資訊，請參閱 [Windows 中的圖形 api](graphics-apis-in-windows-vista.md)。</span><span class="sxs-lookup"><span data-stu-id="aa547-120">For information on these and other Windows graphics components, see [Graphics APIs in Windows](graphics-apis-in-windows-vista.md).</span></span>

<span data-ttu-id="aa547-121">所有這些新的圖形元件都內建于 Windows 7 和 Windows Server 2008 R2 作業系統中。</span><span class="sxs-lookup"><span data-stu-id="aa547-121">All of these new graphics components are built into the Windows 7 and Windows Server 2008 R2 operating systems.</span></span> <span data-ttu-id="aa547-122">您也可以使用 Windows Update 中的系統更新，在 Windows Vista 上安裝 Direct3D 11 API 和相關元件。請參閱知識庫文章 [KB 971644](https://support.microsoft.com/kb/971644)。</span><span class="sxs-lookup"><span data-stu-id="aa547-122">The Direct3D 11 API and related components can also be installed on Windows Vista by using a system update from Windows Update; see Knowledge Base article [KB 971644](https://support.microsoft.com/kb/971644).</span></span> <span data-ttu-id="aa547-123">此更新需要 Windows Vista 和 Service Pack 2。</span><span class="sxs-lookup"><span data-stu-id="aa547-123">This update requires Windows Vista and Service Pack 2.</span></span> <span data-ttu-id="aa547-124">如此一來，已啟用自動更新的使用者就可能已安裝 Direct3D 11 元件，如同所有 Windows 7 使用者。</span><span class="sxs-lookup"><span data-stu-id="aa547-124">End-users with automatic updates enabled will, therefore, likely already have the Direct3D 11 components installed, as will all Windows 7 users.</span></span>

<span data-ttu-id="aa547-125">D3D11InstallHelper 範例的設計目的是為了簡化 Direct3D 11 API 的偵測、自動安裝系統更新（如果適用于使用者的電腦），並在需要更新的 Service Pack 時，為使用者提供適當的訊息以手動程式進行。</span><span class="sxs-lookup"><span data-stu-id="aa547-125">The D3D11InstallHelper sample is designed to simplify detection of the Direct3D 11 API, automatically install the system update if applicable to an end-user's computer, and to provide appropriate messages to the end-user on manual procedure if a newer Service Pack is required.</span></span>

> [!Note]  
> <span data-ttu-id="aa547-126">HLSL 編譯器 (D3DCompile \*) 和 Direct3D 11 (D3DX11 的 D3DX 公用程式 \*) 程式庫不會內建于任何版本的 Windows 作業系統中，但是可以使用現有的 DirectSetup 技術將它們部署為應用程式安裝程式的一部分; 如需使用 DirectSetup 的詳細資訊，請參閱 [遊戲開發人員的 DirectX 安裝](/windows/desktop/DxTechArts/directx-setup-for-game-developers)。</span><span class="sxs-lookup"><span data-stu-id="aa547-126">The HLSL compiler (D3DCompile\*.dll) and the D3DX utility library for Direct3D 11 (D3DX11\*.dll) are not built into any version of the Windows operating system, but they can be deployed as part of an application's installer by using the existing DirectSetup technology; for more information about using DirectSetup, see [DirectX Installation for Game Developers](/windows/desktop/DxTechArts/directx-setup-for-game-developers).</span></span> <span data-ttu-id="aa547-127">「效果11」可作為 [Direct3D 11 更新效果](https://github.com/Microsoft/FX11)的共用來源支援程式庫，而且您可以直接將它包含在應用程式中， (與 DXUT 公用程式程式庫) 很類似。</span><span class="sxs-lookup"><span data-stu-id="aa547-127">"Effects 11" is available as a shared source support library at [Effects for Direct3D 11 Update](https://github.com/Microsoft/FX11), and you can include it directly into an app (much like the DXUT utility library).</span></span> <span data-ttu-id="aa547-128">因此，它不會有任何額外的執行時間轉散發需求。</span><span class="sxs-lookup"><span data-stu-id="aa547-128">Thus, it doesn't have any additional run-time redistribution requirements.</span></span>

## <a name="direct3d-113"></a><span data-ttu-id="aa547-129">Direct3D 11。3</span><span class="sxs-lookup"><span data-stu-id="aa547-129">Direct3D 11.3</span></span>

<span data-ttu-id="aa547-130">Windows 10 隨附于內建的 Direct3D 11.3 API。</span><span class="sxs-lookup"><span data-stu-id="aa547-130">Windows 10 ships with the Direct3D 11.3 API built in.</span></span> <span data-ttu-id="aa547-131">如需 Direct3D 11.3 API 的新功能清單，請參閱 [direct3d 11.3 功能](/windows/desktop/direct3d11/direct3d-11-3-features) 。</span><span class="sxs-lookup"><span data-stu-id="aa547-131">See [Direct3D 11.3 Features](/windows/desktop/direct3d11/direct3d-11-3-features) for a list of new features in the Direct3D 11.3 API.</span></span>

## <a name="direct3d-112"></a><span data-ttu-id="aa547-132">Direct3D 11。2</span><span class="sxs-lookup"><span data-stu-id="aa547-132">Direct3D 11.2</span></span>

<span data-ttu-id="aa547-133">Windows 8.1 和 Windows Server 2012 R2 隨附內建的 Direct3D 11.2 API。</span><span class="sxs-lookup"><span data-stu-id="aa547-133">Windows 8.1 and Windows Server 2012 R2 ship with the Direct3D 11.2 API built in.</span></span> <span data-ttu-id="aa547-134">如需 Direct3D 11.2 API 的新功能清單，請參閱 [direct3d 11.2 功能](/windows/desktop/direct3d11/direct3d-11-2-features) 。</span><span class="sxs-lookup"><span data-stu-id="aa547-134">See [Direct3D 11.2 Features](/windows/desktop/direct3d11/direct3d-11-2-features) for a list of new features in the Direct3D 11.2 API.</span></span>

## <a name="direct3d-111"></a><span data-ttu-id="aa547-135">Direct3D 11。1</span><span class="sxs-lookup"><span data-stu-id="aa547-135">Direct3D 11.1</span></span>

<span data-ttu-id="aa547-136">Windows 8 和 Windows Server 2012 隨附于內建的 [Direct3D 11.1 API](/windows/desktop/direct3d11/direct3d-11-1-features) 。</span><span class="sxs-lookup"><span data-stu-id="aa547-136">Windows 8 and Windows Server 2012 ship with the [Direct3D 11.1 API](/windows/desktop/direct3d11/direct3d-11-1-features) built in.</span></span> <span data-ttu-id="aa547-137">您可以在 Windows 7 或 Windows Server 2008 R2 上，安裝適用于 [windows 7 的平臺更新](https://support.microsoft.com/kb/2670838) ，來取得 DIRECT3D 11.1 API 的部分支援。</span><span class="sxs-lookup"><span data-stu-id="aa547-137">Partial support for the Direct3D 11.1 API is available on Windows 7 or Windows Server 2008 R2 with the [Platform Update for Windows 7](https://support.microsoft.com/kb/2670838) installed.</span></span> <span data-ttu-id="aa547-138">如需 Windows 7 平臺更新的詳細資訊，請參閱 [windows 7 的平臺更新](platform-update-for-windows-7.md)。</span><span class="sxs-lookup"><span data-stu-id="aa547-138">For more info about the Platform Update for Windows 7, see [Platform Update for Windows 7](platform-update-for-windows-7.md).</span></span>

## <a name="d3d11installhelperdll"></a><span data-ttu-id="aa547-139">D3D11InstallHelper.dll</span><span class="sxs-lookup"><span data-stu-id="aa547-139">D3D11InstallHelper.dll</span></span>

<span data-ttu-id="aa547-140">D3D11InstallHelper.dll 裝載偵測 Direct3D 11 元件的核心功能，並透過 Windows Update 服務執行系統更新（如果適用）。</span><span class="sxs-lookup"><span data-stu-id="aa547-140">D3D11InstallHelper.dll hosts the core functionality for detecting Direct3D 11 components, and performing the system update through the Windows Update service if applicable.</span></span> <span data-ttu-id="aa547-141">DLL 不會直接顯示任何訊息或對話方塊。</span><span class="sxs-lookup"><span data-stu-id="aa547-141">The DLL displays no messages or dialog boxes directly.</span></span>

<span data-ttu-id="aa547-142">DLL 包含下列進入點：</span><span class="sxs-lookup"><span data-stu-id="aa547-142">The DLL consists of the following entry points:</span></span>

<dl> <dt>

<span data-ttu-id="aa547-143"><span id="CheckDirect3D11Status"></span><span id="checkdirect3d11status"></span><span id="CHECKDIRECT3D11STATUS"></span>CheckDirect3D11Status</span><span class="sxs-lookup"><span data-stu-id="aa547-143"><span id="CheckDirect3D11Status"></span><span id="checkdirect3d11status"></span><span id="CHECKDIRECT3D11STATUS"></span>CheckDirect3D11Status</span></span>
</dt> <dd>

<span data-ttu-id="aa547-144">此函式會執行必要的檢查，並傳回這部電腦上 Direct3D 11 的狀態。</span><span class="sxs-lookup"><span data-stu-id="aa547-144">This function performs the necessary checks and returns the status of Direct3D 11 on this computer.</span></span> <span data-ttu-id="aa547-145">此函數不需要系統管理員許可權。</span><span class="sxs-lookup"><span data-stu-id="aa547-145">This function does not require administrator rights.</span></span>

-   <span data-ttu-id="aa547-146">已安裝的 D3D11IH \_ 狀態狀態 \_ 表示已在電腦上安裝 Direct3D 11，並已可供使用。</span><span class="sxs-lookup"><span data-stu-id="aa547-146">A status of D3D11IH\_STATUS\_INSTALLED indicates that Direct3D 11 is already installed on the computer and is ready for use.</span></span>
-   <span data-ttu-id="aa547-147">\_不支援的 D3D11IH 狀態 \_ \_ 表示此版本的 Windows 不支援 Direct3D 11 或相關技術。</span><span class="sxs-lookup"><span data-stu-id="aa547-147">D3D11IH\_STATUS\_NOT\_SUPPORTED indicates that this version of Windows does not support Direct3D 11 or related technologies.</span></span>
-   <span data-ttu-id="aa547-148">D3D11IH 狀態的狀態 \_ \_ 需要 \_ 最新的 \_ SP，表示使用者必須安裝最新的 Windows Vista Service Pack。</span><span class="sxs-lookup"><span data-stu-id="aa547-148">A status of D3D11IH\_STATUS\_NEED\_LATEST\_SP indicates that the latest Windows Vista Service Pack should be installed by the user.</span></span>
-   <span data-ttu-id="aa547-149">最後，D3D11IH 狀態的狀態 \_ \_ 需要 \_ 更新，表示系統未安裝 Direct3D 11，但系統更新適用于此版本的 Windows。</span><span class="sxs-lookup"><span data-stu-id="aa547-149">Finally, a status of D3D11IH\_STATUS\_REQUIRES\_UPDATE indicates that the system does not have Direct3D 11 installed, but that the system update does apply to this version of Windows.</span></span>

</dd> <dt>

<span data-ttu-id="aa547-150"><span id="DoUpdateForDirect3D11"></span><span id="doupdatefordirect3d11"></span><span id="DOUPDATEFORDIRECT3D11"></span>DoUpdateForDirect3D11</span><span class="sxs-lookup"><span data-stu-id="aa547-150"><span id="DoUpdateForDirect3D11"></span><span id="doupdatefordirect3d11"></span><span id="DOUPDATEFORDIRECT3D11"></span>DoUpdateForDirect3D11</span></span>
</dt> <dd>

<span data-ttu-id="aa547-151">此函式會使用 Windows Update API，在此系統上執行安裝 Direct3D 11 的系統更新（如果適用）。</span><span class="sxs-lookup"><span data-stu-id="aa547-151">This function uses the Windows Update API to perform the system update for installing Direct3D 11 on this system, if applicable.</span></span> <span data-ttu-id="aa547-152">請注意，此功能需要 Windows Update 的網路連線才能成功，以及系統管理許可權。</span><span class="sxs-lookup"><span data-stu-id="aa547-152">Note that this function requires network connectivity to Windows Update to succeed, as well as administrative rights.</span></span> <span data-ttu-id="aa547-153">它會採用選擇性的進度回呼函式和使用者內容指標，並在完成時傳回最終的結果碼。</span><span class="sxs-lookup"><span data-stu-id="aa547-153">It takes an optional progress callback function and user-context pointer, and returns a final result code when complete.</span></span>

-   <span data-ttu-id="aa547-154">D3D11IH \_ 結果 \_ 成功結果指出已套用系統更新並可供使用，而 D3D11IH \_ 結果 \_ 成功 \_ 重新開機表示系統更新需要電腦在完成前重新開機。</span><span class="sxs-lookup"><span data-stu-id="aa547-154">The D3D11IH\_RESULT\_SUCCESS result indicates that the system update was applied and is ready for use, while D3D11IH\_RESULT\_SUCCESS\_REBOOT indicates that the system update requires the computer is restarted before it is complete.</span></span> <span data-ttu-id="aa547-155">請注意，此函式不會排程系統重新開機。</span><span class="sxs-lookup"><span data-stu-id="aa547-155">Note that this function does not schedule a system restart.</span></span>
-   <span data-ttu-id="aa547-156">\_ \_ 不 \_ 支援的 D3D11IH 結果表示系統更新不適用於此版本的 Windows。</span><span class="sxs-lookup"><span data-stu-id="aa547-156">D3D11IH\_RESULT\_NOT\_SUPPORTED indicates that the system update does not apply to this version of Windows.</span></span> <span data-ttu-id="aa547-157">如果只有在取得 D3D11IH 狀態時，才會呼叫此函式， \_ 則 \_ 需要 \_ 來自 CheckDirect3D11Status 的更新狀態。</span><span class="sxs-lookup"><span data-stu-id="aa547-157">This result should not occur if this function is only called after getting a D3D11IH\_STATUS\_REQUIRES\_UPDATE status from CheckDirect3D11Status.</span></span>
-   <span data-ttu-id="aa547-158">找不到 D3D11IH \_ 結果 \_ 更新的結果 \_ \_ 指出 Windows Update 伺服器上找不到系統更新套件。</span><span class="sxs-lookup"><span data-stu-id="aa547-158">A result of D3D11IH\_RESULT\_UPDATE\_NOT\_FOUND indicates that the system update package was not found on the Windows Update servers.</span></span>
-   <span data-ttu-id="aa547-159">如果 Windows Update 下載或安裝失敗，則 \_ \_ 會傳回 D3D11IH 結果更新 \_ 下載 \_ 失敗或 D3D11IH \_ 結果 \_ 更新 \_ 安裝 \_ 失敗的結果。</span><span class="sxs-lookup"><span data-stu-id="aa547-159">If the Windows Update download or installation fails, then D3D11IH\_RESULT\_UPDATE\_DOWNLOAD\_FAILED or D3D11IH\_RESULT\_UPDATE\_INSTALL\_FAILED will be returned as the result.</span></span>
-   <span data-ttu-id="aa547-160">如果 Windows Update API 傳回網路連線錯誤，則 \_ \_ 會傳回 D3D11IH 結果 WU \_ 服務 \_ 錯誤結果，指出問題可能是間歇性的或與網路設定或防火牆設定相關的問題。</span><span class="sxs-lookup"><span data-stu-id="aa547-160">If a network connectivity error is returned from the Windows Update API, then the D3D11IH\_RESULT\_WU\_SERVICE\_ERROR result is returned, indicating that the problem might be intermittent or related to network configuration or firewall settings.</span></span> <span data-ttu-id="aa547-161">再次嘗試更新功能可能會成功。</span><span class="sxs-lookup"><span data-stu-id="aa547-161">Trying the update function again may succeed.</span></span>

</dd> </dl>

<span data-ttu-id="aa547-162">如需有關 Windows Update API 的詳細資訊，請參閱 [Windows Update AGENT API](/windows/desktop/Wua_Sdk/portal-client)。</span><span class="sxs-lookup"><span data-stu-id="aa547-162">For more information on the Windows Update API, see [Windows Update Agent API](/windows/desktop/Wua_Sdk/portal-client).</span></span>

## <a name="d3d11installexe"></a><span data-ttu-id="aa547-163">D3D11Install.exe</span><span class="sxs-lookup"><span data-stu-id="aa547-163">D3D11Install.exe</span></span>

> [!Note]  
> <span data-ttu-id="aa547-164">D3D11Install.exe 需要 D3D11InstallHelper.dll 才能執行。</span><span class="sxs-lookup"><span data-stu-id="aa547-164">D3D11Install.exe requires D3D11InstallHelper.dll to execute.</span></span>

<span data-ttu-id="aa547-165">D3D11Install.exe 是一種工具，可讓您以 UI 和使用者訊息的形式使用 D3D11InstallHelper.dll 作為獨立安裝程式，也可以做為適當使用 DLL 的範例。</span><span class="sxs-lookup"><span data-stu-id="aa547-165">D3D11Install.exe is a tool for using D3D11InstallHelper.dll as a stand-alone installer complete with UI and end-user messages, as well as acting as an example for proper use of the DLL.</span></span> <span data-ttu-id="aa547-166">如果已安裝 Direct3D 11，則程式會結束，如果系統更新在不需要重新開機系統的情況下成功套用，則需要安裝 Service Pack，或這部電腦不支援 Direct3D 11。</span><span class="sxs-lookup"><span data-stu-id="aa547-166">The process exits with a 0 if Direct3D 11 is already installed, if the system update applies successfully without requiring a system restart, if a Service Pack installation is required, or if Direct3D 11 is not supported by this computer.</span></span> <span data-ttu-id="aa547-167">如果成功套用系統更新，且需要重新開機系統才能完成，則會傳回1。</span><span class="sxs-lookup"><span data-stu-id="aa547-167">A 1 is returned if the system update is applied successfully and requires a system restart to complete.</span></span> <span data-ttu-id="aa547-168">針對其他錯誤狀況，則會傳回2。</span><span class="sxs-lookup"><span data-stu-id="aa547-168">A 2 is returned for other error conditions.</span></span> <span data-ttu-id="aa547-169">請注意，這個可執行檔需要系統管理員許可權才能執行，而且它的資訊清單會在啟用 UAC 的 Windows Vista 或 Windows 7 上執行時要求提升許可權。</span><span class="sxs-lookup"><span data-stu-id="aa547-169">Note that this executable file requires administrator rights to run, and it has a manifest that requests elevation when run on Windows Vista or Windows 7 with UAC enabled.</span></span> <span data-ttu-id="aa547-170">D3D11Install.exe 可以用來作為獨立工具來部署 Direct3D 11 更新，也可以直接由安裝程式使用。</span><span class="sxs-lookup"><span data-stu-id="aa547-170">D3D11Install.exe can be used as a stand-alone tool for deploying the Direct3D 11 update, or it can be used directly by installers.</span></span>

<span data-ttu-id="aa547-171">它支援下列命令列參數：</span><span class="sxs-lookup"><span data-stu-id="aa547-171">It supports the following command-line switches:</span></span>

<dl> <dt>

<span data-ttu-id="aa547-172"><span id="_quiet__"></span><span id="_QUIET__"></span>/quiet</span><span class="sxs-lookup"><span data-stu-id="aa547-172"><span id="_quiet__"></span><span id="_QUIET__"></span>/quiet</span></span> 
</dt> <dd>

<span data-ttu-id="aa547-173">不顯示任何訊息、提示、進度對話方塊或錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="aa547-173">Displays no messages, prompts, progress dialog boxes, or error messages.</span></span>

</dd> <dt>

<span data-ttu-id="aa547-174"><span id="_passive__"></span><span id="_PASSIVE__"></span>/passive</span><span class="sxs-lookup"><span data-stu-id="aa547-174"><span id="_passive__"></span><span id="_PASSIVE__"></span>/passive</span></span> 
</dt> <dd>

<span data-ttu-id="aa547-175">不顯示任何訊息、提示或錯誤訊息，但會顯示 [進度] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="aa547-175">Displays no messages, prompts, or error messages, but will show the progress dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="aa547-176"><span id="_minimal__"></span><span id="_MINIMAL__"></span>/minimal</span><span class="sxs-lookup"><span data-stu-id="aa547-176"><span id="_minimal__"></span><span id="_MINIMAL__"></span>/minimal</span></span> 
</dt> <dd>

<span data-ttu-id="aa547-177">只顯示較短的提示。</span><span class="sxs-lookup"><span data-stu-id="aa547-177">Shows only minimal prompts.</span></span>

</dd> <dt>

<span data-ttu-id="aa547-178"><span id="_y__"></span><span id="_Y__"></span>/y</span><span class="sxs-lookup"><span data-stu-id="aa547-178"><span id="_y__"></span><span id="_Y__"></span>/y</span></span> 
</dt> <dd>

<span data-ttu-id="aa547-179">針對標準和最短的安裝，隱藏提示以確認安裝更新（如有需要）。</span><span class="sxs-lookup"><span data-stu-id="aa547-179">Suppresses prompting to confirm installing the update, if needed and applicable, for a standard and minimal installation.</span></span>

</dd> <dt>

<span data-ttu-id="aa547-180"><span id="_langid_decimal__"></span><span id="_LANGID_DECIMAL__"></span>/langid decimal</span><span class="sxs-lookup"><span data-stu-id="aa547-180"><span id="_langid_decimal__"></span><span id="_LANGID_DECIMAL__"></span>/langid decimal</span></span> 
</dt> <dd>

<span data-ttu-id="aa547-181">強制顯示使用者訊息和對話方塊資源時要使用的語言識別項代碼。</span><span class="sxs-lookup"><span data-stu-id="aa547-181">Forces which language identifier code to use when displaying end-user messages and dialog box resources.</span></span> <span data-ttu-id="aa547-182">預設值是1024，它會使用系統預設語言設定。</span><span class="sxs-lookup"><span data-stu-id="aa547-182">The default value is 1024, which uses the system default language setting.</span></span>

</dd> <dt>

<span data-ttu-id="aa547-183"><span id="_wu__"></span><span id="_WU__"></span>/wu</span><span class="sxs-lookup"><span data-stu-id="aa547-183"><span id="_wu__"></span><span id="_WU__"></span>/wu</span></span> 
</dt> <dd>

<span data-ttu-id="aa547-184">強制使用 Windows Update 而不是系統預設值，這可能是在受管理的伺服器上執行的 (WSUS) 或其他非標準的設定 Windows Server Update Services。</span><span class="sxs-lookup"><span data-stu-id="aa547-184">Forces use of Windows Update rather than the system default, which may be Windows Server Update Services (WSUS) running on a managed server or some other non-standard configuration.</span></span>

</dd> </dl>

## <a name="integrating-into-installation-programs"></a><span data-ttu-id="aa547-185">整合至安裝程式</span><span class="sxs-lookup"><span data-stu-id="aa547-185">Integrating into installation programs</span></span>

<span data-ttu-id="aa547-186">為了符合支援的簡易安裝，適用于 [Windows 遊戲的技術需求 3.1](/windows/desktop/DxTechArts/games-for-windows-technical-requirements-1-1-0006)，必須小心，讓任何使用者提示都能在安裝程式初期出現，並確保不會有多個與 UAC 相關的提高許可權提示。</span><span class="sxs-lookup"><span data-stu-id="aa547-186">To comply with Support Easy Installation, [Technical Requirement 3.1 for Games for Windows](/windows/desktop/DxTechArts/games-for-windows-technical-requirements-1-1-0006), care needs to be taken so that any end-user prompts are presented early in the installation process, and to ensure that there are not multiple UAC-related elevation prompts.</span></span> <span data-ttu-id="aa547-187">有三個可達成此目標的基本選擇：</span><span class="sxs-lookup"><span data-stu-id="aa547-187">There are three basic choices for achieving this goal:</span></span>

1.  <span data-ttu-id="aa547-188">最基本的方法是使用命令列參數 **/minimal** 來執行 D3D11Install.exe。</span><span class="sxs-lookup"><span data-stu-id="aa547-188">The most basic method is to execute the D3D11Install.exe with the command-line switch **/minimal**.</span></span> <span data-ttu-id="aa547-189">這應該在安裝程式 Q&中提早完成，而且安裝應使用傳回值1，表示應該在安裝結束時排定重新開機。</span><span class="sxs-lookup"><span data-stu-id="aa547-189">This should be done early in the installer Q&A, and the installation should use the return value of 1 to indicate that a restart should be scheduled at the end of the installation.</span></span> <span data-ttu-id="aa547-190">執行程式需要系統管理許可權。</span><span class="sxs-lookup"><span data-stu-id="aa547-190">Executing the program requires administrative rights.</span></span>
2.  <span data-ttu-id="aa547-191">您可以直接使用 D3D11InstallHelper.dll 來偵測更新的需求，並提供狀態 D3D11IH 狀態需要最新的 SP 所需的任何使用者訊息，而 \_ \_ \_ \_ 解決方案需要手動使用者操作。</span><span class="sxs-lookup"><span data-stu-id="aa547-191">Use D3D11InstallHelper.dll directly to detect the need for the update, providing any end-user messages necessary for the status D3D11IH\_STATUS\_NEED\_LATEST\_SP, where the resolution requires manual user operations.</span></span> <span data-ttu-id="aa547-192">[不支援的 D3D11IH 狀態] 狀態結果 \_ \_ \_ 可用來控制安裝 direct3d 11 相關的資產，或做為僅限 direct3d 11 （僅限應用程式）的錯誤情況，但不一定是有用的終端使用者訊息。</span><span class="sxs-lookup"><span data-stu-id="aa547-192">The status result of D3D11IH\_STATUS\_NOT\_SUPPORTED could be used to control installation of Direct3D 11–related assets, or as an error condition for Direct3D 11–only applications, but it is otherwise not necessarily a useful end-user message.</span></span> <span data-ttu-id="aa547-193">針對狀態 D3D11IH \_ 狀態 \_ 需要 \_ 更新，安裝程式可以直接使用 DLL 進入點 DoUpdateForDirect3D11 來執行更新，並處理各種產生的終端使用者訊息。</span><span class="sxs-lookup"><span data-stu-id="aa547-193">For the status D3D11IH\_STATUS\_REQUIRES\_UPDATE, the installer can directly use the DLL entry point DoUpdateForDirect3D11 to perform the update and handle the various resulting end-user messages.</span></span> <span data-ttu-id="aa547-194">您可以檢查 D3D11Install.exe 對話方塊和字串資料表資源，找到標準訊息的範例。</span><span class="sxs-lookup"><span data-stu-id="aa547-194">Examples of standard messages can be found by examining the D3D11Install.exe dialog box and string table resources.</span></span> <span data-ttu-id="aa547-195">更新進入點需要系統管理員許可權。</span><span class="sxs-lookup"><span data-stu-id="aa547-195">The update entry point requires administrator rights.</span></span>
3.  <span data-ttu-id="aa547-196">混合式方法是使用 D3D11InstallHelper.dll 檢查狀態，如果狀態碼 D3D11IH \_ 狀態 \_ 需要 \_ 最新的 \_ SP 或 D3D11IH \_ 狀態需要 \_ \_ 更新，可以使用參數 **/minimal** 和 **/y** 來執行 D3D11Install.exe，以顯示對話方塊或視需要執行更新。</span><span class="sxs-lookup"><span data-stu-id="aa547-196">A hybrid approach is to check status with D3D11InstallHelper.dll, and in the case of the status code D3D11IH\_STATUS\_NEED\_LATEST\_SP or D3D11IH\_STATUS\_REQUIRES\_UPDATE, D3D11Install.exe can be executed with the switches **/minimal** and **/y** to display the dialog box or to perform the update, as needed.</span></span> <span data-ttu-id="aa547-197">這些步驟應該在安裝程式早期執行（通常是在 Q&A 之後立即執行，而且執行可執行檔需要系統管理許可權）。</span><span class="sxs-lookup"><span data-stu-id="aa547-197">These steps should be performed early in the installation process, usually immediately after the Q&A, and running the executable requires administrative rights.</span></span>

### <a name="integrating-into-installshield"></a><span data-ttu-id="aa547-198">整合至 InstallShield</span><span class="sxs-lookup"><span data-stu-id="aa547-198">Integrating into InstallShield</span></span>

<span data-ttu-id="aa547-199">使用 D3D11InstallHelper 範例，即可輕鬆地從 InstallShield 的 InstallScript 處理 Direct3D 11 部署。</span><span class="sxs-lookup"><span data-stu-id="aa547-199">Handling the Direct3D 11 deployment from InstallShield's InstallScript is easily done using the D3D11InstallHelper sample.</span></span> <span data-ttu-id="aa547-200">使用 InstallScript 與 InstallShield 整合所需的步驟如下所示 (使用方法3，如下一節所述) ：</span><span class="sxs-lookup"><span data-stu-id="aa547-200">The steps required to integrate with InstallShield using InstallScript are as follows (using method 3, described in the previous section):</span></span>

1.  <span data-ttu-id="aa547-201">在 InstallShield 編輯器中開啟 InstallScript 專案。</span><span class="sxs-lookup"><span data-stu-id="aa547-201">Open an InstallScript project in the InstallShield editor.</span></span>
2.  <span data-ttu-id="aa547-202">在 **支援** 檔案中新增 D3D11InstallHelper.dll 並 D3D11Install.exe 至專案。</span><span class="sxs-lookup"><span data-stu-id="aa547-202">Add D3D11InstallHelper.dll and D3D11Install.exe to the project in **Support Files**.</span></span>

    <span data-ttu-id="aa547-203">**將檔案新增至 InstallShield 專案**</span><span class="sxs-lookup"><span data-stu-id="aa547-203">**To add the files to the InstallShield Project**</span></span>

    1.  <span data-ttu-id="aa547-204">在 [**安裝設計** 工具] 索引標籤的左側導覽窗格中，按一下 [**行為和邏輯**] 下的 [支援檔案] **/[公告欄**]。</span><span class="sxs-lookup"><span data-stu-id="aa547-204">On the **Installation Designer** tab, click **Support Files/Billboards** under **Behavior and Logic** in the navigation pane on the left.</span></span>
    2.  <span data-ttu-id="aa547-205">按一下 [**語言獨立**]，然後以滑鼠右鍵按一下 [檔案] 視窗並選取 [**插入** 檔案]。</span><span class="sxs-lookup"><span data-stu-id="aa547-205">Click **Language Independent**, then right-click in the **Files** window and select **Insert Files**.</span></span> <span data-ttu-id="aa547-206">流覽以新增 D3D11InstallHelper.dll 和 D3D11Install.exe。</span><span class="sxs-lookup"><span data-stu-id="aa547-206">Browse to add D3D11InstallHelper.dll and D3D11Install.exe.</span></span> <span data-ttu-id="aa547-207">這些檔案的預設位置為： SDK 根 \\ 範例 \\ c + + \\ 其他 \\ Bin \\ x86</span><span class="sxs-lookup"><span data-stu-id="aa547-207">The default location for these files is: SDK root\\Samples\\C++\\Misc\\Bin\\x86</span></span>

3.  <span data-ttu-id="aa547-208">在 [InstallScript explorer] 中，按一下 [InstallScript] 檔案， (通常是 rul) 將呼叫 DLL 或可執行檔（位於左側導覽窗格中的 [ **行為] 和 [邏輯** ] 下）。</span><span class="sxs-lookup"><span data-stu-id="aa547-208">In the InstallScript explorer, click the InstallScript file (usually Setup.rul) that will call the DLL or executable, located under **Behavior and Logic** in the navigation pane on the left.</span></span>
4.  <span data-ttu-id="aa547-209">將下列 InstallScript 貼到靠近頂端的檔案中：</span><span class="sxs-lookup"><span data-stu-id="aa547-209">Paste the following InstallScript into the file near the top:</span></span>

    ``` syntax
#define D3D11IH_STATUS_INSTALLED       0
#define D3D11IH_STATUS_NOT_SUPPORTED   1
#define D3D11IH_STATUS_REQUIRES_UPDATE 2
#define D3D11IH_STATUS_NEED_LATEST_SP  3
#define D3D11IH_STATUS_ERROR           -1
    prototype NUMBER D3D11InstallHelper.CheckDirect3D11StatusIS();

#define D3D11IH_RESULT_SUCCESS                0
#define D3D11IH_RESULT_SUCCESS_REBOOT         1
#define D3D11IH_RESULT_NOT_SUPPORTED          2
#define D3D11IH_RESULT_UPDATE_NOT_FOUND       3
#define D3D11IH_RESULT_UPDATE_DOWNLOAD_FAILED 4
#define D3D11IH_RESULT_UPDATE_INSTALL_FAILED  5
#define D3D11IH_RESULT_WU_SERVICE_ERROR       6
#define D3D11IH_RESULT_ERROR                  -1
    prototype NUMBER D3D11InstallHelper.DoUpdateForDirect3D11IS(BOOL);
    ```

5.  <span data-ttu-id="aa547-210">將下列 InstallScript 貼入 **OnFirstUIBefore** 函式中的檔案，在傳回0之前：</span><span class="sxs-lookup"><span data-stu-id="aa547-210">Paste the following InstallScript into the file in the **OnFirstUIBefore** function, just before the return 0:</span></span>

    ``` syntax
    Dlg_D3D11:
        UseDLL( SUPPORTDIR ^ "D3D11InstallHelper.DLL" );
        nResult = D3D11InstallHelper.CheckDirect3D11StatusIS();   
        UnUseDLL( SUPPORTDIR ^ "D3D11InstallHelper.DLL" );
        
        if ( nResult = D3D11IH_STATUS_REQUIRES_UPDATE
             || nResult = D3D11IH_STATUS_NEED_LATEST_SP) then
            nResult = LaunchAppAndWait(
    SUPPORTDIR^"D3D11Install.exe",
    "/minimal /y", WAIT);
            if ( nResult < 0 ) then
                MessageBox("Unable to launch D3D11Install.exe",
     SEVERE);
            elseif ( nResult == 1 ) then
                BATCH_INSTALL = 1;
            endif;          
        endif;
    ```

### <a name="integrating-into-an-msi-package"></a><span data-ttu-id="aa547-211">整合至 MSI 套件</span><span class="sxs-lookup"><span data-stu-id="aa547-211">Integrating into an MSI package</span></span>

<span data-ttu-id="aa547-212">以下是使用 MSI 自訂動作整合 Direct3D 11 部署所需步驟的高階描述， (使用) 本主題稍早所述的方法3：</span><span class="sxs-lookup"><span data-stu-id="aa547-212">The following is a high-level description of the steps required to integrate Direct3D 11 deployment using MSI custom actions (using method 3, described earlier in this topic):</span></span>

1.  <span data-ttu-id="aa547-213">將屬性新增至名為 **RelativePathToD3D11IH** 的 MSI 屬性工作表，其中包含在安裝期間 D3D11Install.exe 和 D3D11InstallHelper.dll 的相對路徑 (這通常會在媒體影像) 中。</span><span class="sxs-lookup"><span data-stu-id="aa547-213">Add a property to the MSI Property table called **RelativePathToD3D11IH** that contains the relative path to D3D11Install.exe and D3D11InstallHelper.dll during installation (this is typically in the media image).</span></span> <span data-ttu-id="aa547-214">這也會將 MSI 屬性 D3D11IH \_ 狀態設定為 CheckDirect3D11Status 所傳回的狀態 (字串屬性等於列舉符號或「錯誤」 ) 。</span><span class="sxs-lookup"><span data-stu-id="aa547-214">This also sets an MSI property D3D11IH\_STATUS to the status returned by CheckDirect3D11Status (a string property equal to the enumeration symbol or "ERROR").</span></span>
2.  <span data-ttu-id="aa547-215">在 CostFinalize 動作之後，以立即自訂動作的形式呼叫 D3D11InstallHelper.dll 函式 **SetD3D11InstallMSIProperties** ，以針對其他自訂動作設定適當的 MSI 屬性。</span><span class="sxs-lookup"><span data-stu-id="aa547-215">After the CostFinalize action, call the D3D11InstallHelper.dll function **SetD3D11InstallMSIProperties** as an immediate custom action to set the appropriate MSI properties for the other custom actions.</span></span>
3.  <span data-ttu-id="aa547-216">安裝時，會在呼叫 D3D11InstallHelper.dll 函式 **DoD3D11InstallUsingMSI** 的 InstallFiles 動作之後，觸發延遲的自訂動作。</span><span class="sxs-lookup"><span data-stu-id="aa547-216">Upon installation, trigger a deferred custom action after the InstallFiles action that calls the D3D11InstallHelper.dll function **DoD3D11InstallUsingMSI**.</span></span> <span data-ttu-id="aa547-217">自訂動作必須將旗標 msidbCustomActionTypeNoImpersonate 設定為在提高許可權的內容中執行。</span><span class="sxs-lookup"><span data-stu-id="aa547-217">The custom action must set the flag msidbCustomActionTypeNoImpersonate to run in an elevated context.</span></span>
4.  <span data-ttu-id="aa547-218">在 InstallFinalize 動作之後，如有需要，請以立即自訂動作的形式呼叫 D3D11InstallHelper.dll 函數 **FinishD3D11InstallUsingMSI** ，以處理成功的重新開機要求結果碼。</span><span class="sxs-lookup"><span data-stu-id="aa547-218">After the InstallFinalize action, call the D3D11InstallHelper.dll function **FinishD3D11InstallUsingMSI** as an immediate custom action to handle the successful reboot request result code, if needed.</span></span>

<span data-ttu-id="aa547-219">下列指示會詳細說明此程式，其描述可使用 MSI 編輯器（例如 [Orca 編輯器](/windows/desktop/Msi/orca-exe)）完成的程式。</span><span class="sxs-lookup"><span data-stu-id="aa547-219">This procedure is described in detail in the following instructions, which describe a process that can be done using an MSI editor, such as the [Orca editor](/windows/desktop/Msi/orca-exe).</span></span> <span data-ttu-id="aa547-220">有些 MSI 編輯器具有可簡化其中一些設定步驟的嚮導。</span><span class="sxs-lookup"><span data-stu-id="aa547-220">Some MSI editors have wizards that simplify some of these configuration steps.</span></span>

<span data-ttu-id="aa547-221">**設定 MSI 套件以與 D3D11InstallHelper.dll整合**</span><span class="sxs-lookup"><span data-stu-id="aa547-221">**To configure an MSI package for integration with D3D11InstallHelper.dll**</span></span>

1.  <span data-ttu-id="aa547-222">以 Orca 開啟 MSI 套件。</span><span class="sxs-lookup"><span data-stu-id="aa547-222">Open the MSI package in Orca.</span></span>
2.  <span data-ttu-id="aa547-223">將下表中顯示的資料列加入至 MSI 封裝中的二進位資料表。</span><span class="sxs-lookup"><span data-stu-id="aa547-223">Add the row shown in the following table to the Binary table in the MSI package.</span></span>

    | <span data-ttu-id="aa547-224">Name</span><span class="sxs-lookup"><span data-stu-id="aa547-224">Name</span></span>    | <span data-ttu-id="aa547-225">資料</span><span class="sxs-lookup"><span data-stu-id="aa547-225">Data</span></span>                                         |
    |---------|----------------------------------------------|
    | <span data-ttu-id="aa547-226">D3D11IH</span><span class="sxs-lookup"><span data-stu-id="aa547-226">D3D11IH</span></span> | <span data-ttu-id="aa547-227">DLL 的檔案路徑 \\D3D11InstallHelper.dll</span><span class="sxs-lookup"><span data-stu-id="aa547-227">File path to the DLL\\D3D11InstallHelper.dll</span></span> |

    

     

    > [!Note]  
    > <span data-ttu-id="aa547-228">此檔案將內嵌在 MSI 套件中，因此您必須在每次重新編譯 D3D11InstallHelper.dll 時執行此步驟。</span><span class="sxs-lookup"><span data-stu-id="aa547-228">This file will be embedded in the MSI package, so you must do this step every time that you recompile D3D11InstallHelper.dll.</span></span>

     

3.  <span data-ttu-id="aa547-229">將下表中顯示的資料列加入至 MSI 封裝中的 CustomAction 資料表。</span><span class="sxs-lookup"><span data-stu-id="aa547-229">Add the rows shown in the following table to the CustomAction table in the MSI package.</span></span> 

    | <span data-ttu-id="aa547-230">動作</span><span class="sxs-lookup"><span data-stu-id="aa547-230">Action</span></span>              | <span data-ttu-id="aa547-231">類型</span><span class="sxs-lookup"><span data-stu-id="aa547-231">Type</span></span>                                                                                                                                                                   | <span data-ttu-id="aa547-232">來源</span><span class="sxs-lookup"><span data-stu-id="aa547-232">Source</span></span>  | <span data-ttu-id="aa547-233">目標</span><span class="sxs-lookup"><span data-stu-id="aa547-233">Target</span></span>                       |
    |---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------|------------------------------|
    | <span data-ttu-id="aa547-234">Direct3D11SetProps</span><span class="sxs-lookup"><span data-stu-id="aa547-234">Direct3D11SetProps</span></span>  | <span data-ttu-id="aa547-235">msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue = 65</span><span class="sxs-lookup"><span data-stu-id="aa547-235">msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue = 65</span></span>                                                                        | <span data-ttu-id="aa547-236">D3D11IH</span><span class="sxs-lookup"><span data-stu-id="aa547-236">D3D11IH</span></span> | <span data-ttu-id="aa547-237">SetD3D11InstallMSIProperties</span><span class="sxs-lookup"><span data-stu-id="aa547-237">SetD3D11InstallMSIProperties</span></span> |
    | <span data-ttu-id="aa547-238">Direct3D11DoInstall</span><span class="sxs-lookup"><span data-stu-id="aa547-238">Direct3D11DoInstall</span></span> | <span data-ttu-id="aa547-239">msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3137</span><span class="sxs-lookup"><span data-stu-id="aa547-239">msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3137</span></span> | <span data-ttu-id="aa547-240">D3D11IH</span><span class="sxs-lookup"><span data-stu-id="aa547-240">D3D11IH</span></span> | <span data-ttu-id="aa547-241">DoD3D11InstallUsingMSI</span><span class="sxs-lookup"><span data-stu-id="aa547-241">DoD3D11InstallUsingMSI</span></span>       |
    | <span data-ttu-id="aa547-242">Direct3D11Finish</span><span class="sxs-lookup"><span data-stu-id="aa547-242">Direct3D11Finish</span></span>    | <span data-ttu-id="aa547-243">msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue = 65</span><span class="sxs-lookup"><span data-stu-id="aa547-243">msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue = 65</span></span>                                                                        | <span data-ttu-id="aa547-244">D3D11IH</span><span class="sxs-lookup"><span data-stu-id="aa547-244">D3D11IH</span></span> | <span data-ttu-id="aa547-245">FinishD3D11InstallUsingMSI</span><span class="sxs-lookup"><span data-stu-id="aa547-245">FinishD3D11InstallUsingMSI</span></span>   |

    

     

4.  <span data-ttu-id="aa547-246">將下表中的 [動作]、[條件] 和 [順序] 所顯示的值，加入至 MSI 封裝中的 InstallExecuteSequence 資料表。</span><span class="sxs-lookup"><span data-stu-id="aa547-246">Add the values shown for Action, Condition, and Sequence in the following table to the InstallExecuteSequence table in the MSI package.</span></span> 

    | <span data-ttu-id="aa547-247">動作</span><span class="sxs-lookup"><span data-stu-id="aa547-247">Action</span></span>              | <span data-ttu-id="aa547-248">條件</span><span class="sxs-lookup"><span data-stu-id="aa547-248">Condition</span></span>     | <span data-ttu-id="aa547-249">順序</span><span class="sxs-lookup"><span data-stu-id="aa547-249">Sequence</span></span> | <span data-ttu-id="aa547-250">備註</span><span class="sxs-lookup"><span data-stu-id="aa547-250">Notes</span></span>                                                                                                                                                          |
    |---------------------|---------------|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="aa547-251">Direct3D11SetProps</span><span class="sxs-lookup"><span data-stu-id="aa547-251">Direct3D11SetProps</span></span>  |               | <span data-ttu-id="aa547-252">1016</span><span class="sxs-lookup"><span data-stu-id="aa547-252">1016</span></span>     | <span data-ttu-id="aa547-253">序號會在 CostFinalize 之後立即放置動作。</span><span class="sxs-lookup"><span data-stu-id="aa547-253">The sequence number places the action soon after CostFinalize.</span></span>                                                                                                 |
    | <span data-ttu-id="aa547-254">Direct3D11DoInstall</span><span class="sxs-lookup"><span data-stu-id="aa547-254">Direct3D11DoInstall</span></span> | <span data-ttu-id="aa547-255">未安裝</span><span class="sxs-lookup"><span data-stu-id="aa547-255">NOT Installed</span></span> | <span data-ttu-id="aa547-256">4004</span><span class="sxs-lookup"><span data-stu-id="aa547-256">4004</span></span>     | <span data-ttu-id="aa547-257">此自訂動作只會在所有使用者的新安裝期間發生。</span><span class="sxs-lookup"><span data-stu-id="aa547-257">This custom action will only happen during a new installation for all users.</span></span> <span data-ttu-id="aa547-258">序號會將動作放在 InstallFiles 之後和復原之後。</span><span class="sxs-lookup"><span data-stu-id="aa547-258">The sequence number places the action after InstallFiles and after the rollbacks.</span></span> |
    | <span data-ttu-id="aa547-259">Direct3D11Finish</span><span class="sxs-lookup"><span data-stu-id="aa547-259">Direct3D11Finish</span></span>    |               | <span data-ttu-id="aa547-260">6615</span><span class="sxs-lookup"><span data-stu-id="aa547-260">6615</span></span>     | <span data-ttu-id="aa547-261">序號會在 InstallFinalize 之後立即放置動作。</span><span class="sxs-lookup"><span data-stu-id="aa547-261">The sequence number places the action soon after InstallFinalize.</span></span>                                                                                              |

    

     

5.  <span data-ttu-id="aa547-262">將下表中顯示的資料列加入至 MSI 封裝中的 **屬性** 資料表。</span><span class="sxs-lookup"><span data-stu-id="aa547-262">Add the row shown in the following table to the **Property** table in the MSI package.</span></span> 

    | <span data-ttu-id="aa547-263">屬性</span><span class="sxs-lookup"><span data-stu-id="aa547-263">Property</span></span>              | <span data-ttu-id="aa547-264">值</span><span class="sxs-lookup"><span data-stu-id="aa547-264">Value</span></span>                                                                        |
    |-----------------------|------------------------------------------------------------------------------|
    | <span data-ttu-id="aa547-265">RelativePathToD3D11IH</span><span class="sxs-lookup"><span data-stu-id="aa547-265">RelativePathToD3D11IH</span></span> | <span data-ttu-id="aa547-266">包含 D3D11Install.exe 和 D3D11InstallHelper.dll 的相對檔案路徑</span><span class="sxs-lookup"><span data-stu-id="aa547-266">relative file path that contains D3D11Install.exe and D3D11InstallHelper.dll</span></span> |

    

     

    > [!Note]  
    > <span data-ttu-id="aa547-267">路徑所指定的位置是相對於安裝路徑所指定的位置，例如「可轉散發套件」 \\ 。</span><span class="sxs-lookup"><span data-stu-id="aa547-267">The location specified by the path is relative to the location specified by the installation path—for example, "redist\\".</span></span>

     

6.  <span data-ttu-id="aa547-268">儲存 MSI 套件。</span><span class="sxs-lookup"><span data-stu-id="aa547-268">Save the MSI package.</span></span> <span data-ttu-id="aa547-269">如需有關 MSI 封裝和 Windows Installer 的詳細資訊，請參閱 [Windows Installer](/windows/desktop/Msi/windows-installer-portal)。</span><span class="sxs-lookup"><span data-stu-id="aa547-269">For more detailed information about MSI packages and Windows Installer, see [Windows Installer](/windows/desktop/Msi/windows-installer-portal).</span></span>

## <a name="debugging-tips"></a><span data-ttu-id="aa547-270">偵錯秘訣</span><span class="sxs-lookup"><span data-stu-id="aa547-270">Debugging tips</span></span>

<span data-ttu-id="aa547-271">D3D11InstallHelper.dll 和 D3D11Install.exe 都可以使用 Visual Studio 中的 Debug 設定來建立，而這些版本會將訊息列印至標準的 Windows 調試輸出機制。</span><span class="sxs-lookup"><span data-stu-id="aa547-271">Both D3D11InstallHelper.dll and D3D11Install.exe can be built with the Debug configuration in Visual Studio, and these versions will print messages to the standard Windows debug output mechanism.</span></span>

## <a name="corporate-settings"></a><span data-ttu-id="aa547-272">公司設定</span><span class="sxs-lookup"><span data-stu-id="aa547-272">Corporate settings</span></span>

<span data-ttu-id="aa547-273">D3D11InstallHelper 範例是針對透過 Windows Update 的標準部署而設計，這是使用消費者安裝遊戲的最常見案例。</span><span class="sxs-lookup"><span data-stu-id="aa547-273">The D3D11InstallHelper sample is designed for standard deployment through Windows Update, which is the most common scenario for installation of a game by consumers.</span></span> <span data-ttu-id="aa547-274">不過，許多遊戲開發人員都是使用發行者和開發工作室，在具有本機受控伺服器的企業設定中，使用 Windows Server Update Services (WSUS) 技術來提供軟體更新。</span><span class="sxs-lookup"><span data-stu-id="aa547-274">However, Many game developers, working for publishers and in development studios, do so in enterprise settings that have a locally managed server providing software updates by using Windows Server Update Services (WSUS) technology.</span></span> <span data-ttu-id="aa547-275">在這種環境中，本機 IT 系統管理員可以核准控制公司網路內的電腦可以使用哪些更新，且無法使用標準取用者版本的 update KB 971644。</span><span class="sxs-lookup"><span data-stu-id="aa547-275">In this type of environment, the local IT administrator has approval control over which updates are made available to computers within the corporate network, and the standard consumer version of update KB 971644 is not available.</span></span>

<span data-ttu-id="aa547-276">在公司/企業設定中部署 DirectX 11 的基本解決方案有三種：</span><span class="sxs-lookup"><span data-stu-id="aa547-276">There are three basic solutions for deploying DirectX 11 in corporate/enterprise settings:</span></span>

-   <span data-ttu-id="aa547-277">在某些設定中，您可以直接檢查 Windows Update，而不是使用本機管理的 WSUS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="aa547-277">In some configurations, it is possible to directly check Windows Update rather than use the locally managed WSUS server.</span></span> <span data-ttu-id="aa547-278">基於這個理由，D3D11InstallHelper 支援 **/wu** 命令列參數。</span><span class="sxs-lookup"><span data-stu-id="aa547-278">For this reason, D3D11InstallHelper supports the **/wu** command-line switch.</span></span> <span data-ttu-id="aa547-279">不過，並非所有的公司網路都允許與公用 Microsoft 伺服器的連線。</span><span class="sxs-lookup"><span data-stu-id="aa547-279">However, not all corporate networks allow connections to the public Microsoft servers.</span></span>
-   <span data-ttu-id="aa547-280">本機 IT 系統管理員可以核准 KB 971512，這是從 WSUS 部署且包含 Direct3D 11 API 的企業支援更新。</span><span class="sxs-lookup"><span data-stu-id="aa547-280">The local IT administrator can approve KB 971512, an enterprise-supported update deployed from WSUS, that includes the Direct3D 11 API.</span></span> <span data-ttu-id="aa547-281">這是標準使用者在完全鎖定的環境中取得 Direct3D 11 更新的唯一選項。</span><span class="sxs-lookup"><span data-stu-id="aa547-281">This is the only option for a Standard User to obtain the Direct3D 11 update in an environment that is fully locked down.</span></span>
-   <span data-ttu-id="aa547-282">或者，您可以手動安裝 [KB 971512](https://support.microsoft.com/kb/971512/) 。</span><span class="sxs-lookup"><span data-stu-id="aa547-282">Alternatively, [KB 971512](https://support.microsoft.com/kb/971512/) can be manually installed.</span></span>

<span data-ttu-id="aa547-283">玩家的電腦很罕見只能從本機管理的 WSUS 伺服器取得更新，而這只是大型組織中可能在這類環境中的開發人員。</span><span class="sxs-lookup"><span data-stu-id="aa547-283">It is very rare that a gamer's computer can only get updates from a locally managed WSUS server, and it is only developers in large organizations who are likely to be in such environments.</span></span>

## <a name="related-articles"></a><span data-ttu-id="aa547-284">相關文章</span><span class="sxs-lookup"><span data-stu-id="aa547-284">Related articles</span></span>

[<span data-ttu-id="aa547-285">適用于遊戲開發人員的 Windows 防火牆</span><span class="sxs-lookup"><span data-stu-id="aa547-285">Windows Firewall for Game Developers</span></span>](/windows/desktop/DxTechArts/games-and-firewalls)

[<span data-ttu-id="aa547-286">適用于遊戲開發人員的 Windows 遊戲瀏覽器</span><span class="sxs-lookup"><span data-stu-id="aa547-286">Windows Games Explorer for Game Developers</span></span>](/windows/desktop/DxTechArts/windows-game-explorer-integration)
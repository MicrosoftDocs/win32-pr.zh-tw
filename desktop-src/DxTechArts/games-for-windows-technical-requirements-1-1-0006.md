---
title: 適用於 Windows 的遊戲技術需求：Windows XP、Windows Vista、Windows 7 和 Windows 8 上遊戲的最佳作法
description: 本文提供在 Windows 上執行之遊戲的技術需求和最佳作法。
ms.assetid: 8b816e9f-de68-cf84-1501-a9c36c6b75d8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e38b9476a4ab2aad5edc6210f55bc4d2b85845f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103683044"
---
# <a name="games-for-windows-technical-requirements-best-practices-for-games-on-windows-xp-windows-vista-windows-7-and-windows-8"></a><span data-ttu-id="a03c5-103">Windows 技術需求的遊戲： Windows XP、Windows Vista、Windows 7 和 Windows 8 遊戲的最佳作法</span><span class="sxs-lookup"><span data-stu-id="a03c5-103">Games for Windows Technical Requirements: Best Practices for Games on Windows XP, Windows Vista, Windows 7, and Windows 8</span></span>

<span data-ttu-id="a03c5-104">本文提供在 Windows 上執行之遊戲的技術需求和最佳作法。</span><span class="sxs-lookup"><span data-stu-id="a03c5-104">This article provides technical requirements and best practices for games that run on Windows.</span></span> <span data-ttu-id="a03c5-105">我們寫了這些技術需求和最佳作法，主要是用來涵蓋 Windows Vista 和 Windows 7，以及舊版 Windows XP 作業系統。</span><span class="sxs-lookup"><span data-stu-id="a03c5-105">We wrote these technical requirements and best practices primarily to cover Windows Vista and Windows 7, as well as the legacy Windows XP operating system.</span></span> <span data-ttu-id="a03c5-106">這些最佳作法通常也適用于 Windows 8 上的桌面 Win32 遊戲。</span><span class="sxs-lookup"><span data-stu-id="a03c5-106">These best practices also generally apply to desktop Win32 games on Windows 8.</span></span>

<span data-ttu-id="a03c5-107">此文章包含下列各節：</span><span class="sxs-lookup"><span data-stu-id="a03c5-107">This articles contains these sections:</span></span>

-   [<span data-ttu-id="a03c5-108">Windows 8 的差異</span><span class="sxs-lookup"><span data-stu-id="a03c5-108">Differences for Windows 8</span></span>](#differences-for-windows-8)
    -   [<span data-ttu-id="a03c5-109">其他資訊</span><span class="sxs-lookup"><span data-stu-id="a03c5-109">Additional Information</span></span>](#additional-information)
-   [<span data-ttu-id="a03c5-110">適用於 Windows 的遊戲</span><span class="sxs-lookup"><span data-stu-id="a03c5-110">Games for Windows</span></span>](#games-for-windows-technical-requirements-best-practices-for-games-on-windows-xp-windows-vista-windows-7-and-windows-8)
    -   [<span data-ttu-id="a03c5-111">1.1 遊戲瀏覽器整合</span><span class="sxs-lookup"><span data-stu-id="a03c5-111">1.1 Games Explorer Integration</span></span>](#11-games-explorer-integration)
    -   [<span data-ttu-id="a03c5-112">1.2 支援家族安全性/家長監護控制項</span><span class="sxs-lookup"><span data-stu-id="a03c5-112">1.2 Support Family Safety / Parental Controls</span></span>](/windows)
    -   [<span data-ttu-id="a03c5-113">1.3 支援豐富的儲存遊戲</span><span class="sxs-lookup"><span data-stu-id="a03c5-113">1.3 Support Rich Saved Games</span></span>](#13-support-rich-saved-games)
    -   <span data-ttu-id="a03c5-114">[1.4 支援 Windows 條件式需求的 Xbox 360 通用控制器 \[\]](#14-support-the-xbox-360-common-controller-for-windows-conditional-requirement)</span><span class="sxs-lookup"><span data-stu-id="a03c5-114">[1.4 Support the Xbox 360 Common Controller for Windows \[Conditional Requirement\]](#14-support-the-xbox-360-common-controller-for-windows-conditional-requirement)</span></span>
    -   [<span data-ttu-id="a03c5-115">1.5 支援多種外觀比例和解析度</span><span class="sxs-lookup"><span data-stu-id="a03c5-115">1.5 Support Multiple Aspect Ratios and Resolutions</span></span>](#15-support-multiple-aspect-ratios-and-resolutions)
    -   [<span data-ttu-id="a03c5-116">1.6 支援從 Windows Media Center 啟動</span><span class="sxs-lookup"><span data-stu-id="a03c5-116">1.6 Support Launch from Windows Media Center</span></span>](#16-support-launch-from-windows-media-center)
    -   [<span data-ttu-id="a03c5-117">1.7 Direct3D 支援</span><span class="sxs-lookup"><span data-stu-id="a03c5-117">1.7 Direct3D Support</span></span>](#17-direct3d-support)
    -   [<span data-ttu-id="a03c5-118">1.8 啟用高 DPI 感知</span><span class="sxs-lookup"><span data-stu-id="a03c5-118">1.8 Enable High-DPI-Aware</span></span>](#18-enable-high-dpi-aware)
-   [<span data-ttu-id="a03c5-119">安全性與相容性</span><span class="sxs-lookup"><span data-stu-id="a03c5-119">Security and Compatibility</span></span>](#security-and-compatibility)
    -   [<span data-ttu-id="a03c5-120">2.1 遵循使用者帳戶控制指導方針</span><span class="sxs-lookup"><span data-stu-id="a03c5-120">2.1 Follow User Account Control Guidelines</span></span>](#21-follow-user-account-control-guidelines)
    -   [<span data-ttu-id="a03c5-121">2.2 支援 Windows x64 版本</span><span class="sxs-lookup"><span data-stu-id="a03c5-121">2.2 Support Windows x64 Versions</span></span>](#22-support-windows-x64-versions)
    -   [<span data-ttu-id="a03c5-122">2.3 簽署檔案</span><span class="sxs-lookup"><span data-stu-id="a03c5-122">2.3 Sign Files</span></span>](#23-sign-files)
    -   [<span data-ttu-id="a03c5-123">2.4 簽署驅動程式</span><span class="sxs-lookup"><span data-stu-id="a03c5-123">2.4 Sign Drivers</span></span>](#24-sign-drivers)
    -   [<span data-ttu-id="a03c5-124">2.5 執行適當的版本檢查</span><span class="sxs-lookup"><span data-stu-id="a03c5-124">2.5 Perform Proper Version Checking</span></span>](#25-perform-proper-version-checking)
    -   [<span data-ttu-id="a03c5-125">2.6 支援並行使用者會話</span><span class="sxs-lookup"><span data-stu-id="a03c5-125">2.6 Support Concurrent User Sessions</span></span>](#26-support-concurrent-user-sessions)
    -   [<span data-ttu-id="a03c5-126">2.7 支援長名稱</span><span class="sxs-lookup"><span data-stu-id="a03c5-126">2.7 Support Long Names</span></span>](#27-support-long-names)
-   [<span data-ttu-id="a03c5-127">安裝</span><span class="sxs-lookup"><span data-stu-id="a03c5-127">Installation</span></span>](#32-support-user-account-control-for-installation)
    -   [<span data-ttu-id="a03c5-128">3.1 支援輕鬆安裝</span><span class="sxs-lookup"><span data-stu-id="a03c5-128">3.1 Support Easy Installation</span></span>](#31-support-easy-installation)
    -   [<span data-ttu-id="a03c5-129">3.2 支援安裝的使用者帳戶控制</span><span class="sxs-lookup"><span data-stu-id="a03c5-129">3.2 Support User Account Control for Installation</span></span>](#32-support-user-account-control-for-installation)
    -   [<span data-ttu-id="a03c5-130">3.3 安裝到正確的資料夾</span><span class="sxs-lookup"><span data-stu-id="a03c5-130">3.3 Install to Correct Folders</span></span>](#33-install-to-correct-folders)
    -   [<span data-ttu-id="a03c5-131">3.4 正確安裝 Windows 資源</span><span class="sxs-lookup"><span data-stu-id="a03c5-131">3.4 Install Windows Resources Properly</span></span>](#34-install-windows-resources-properly)
    -   [<span data-ttu-id="a03c5-132">3.5 避免在安裝期間重新開機</span><span class="sxs-lookup"><span data-stu-id="a03c5-132">3.5 Avoid Reboots During Installation</span></span>](#35-avoid-reboots-during-installation)
    -   [<span data-ttu-id="a03c5-133">3.6 使用正確的檔案版本控制</span><span class="sxs-lookup"><span data-stu-id="a03c5-133">3.6 Use File Versioning Correctly</span></span>](#36-use-file-versioning-correctly)
    -   <span data-ttu-id="a03c5-134">[3.7 支援自動運行 \[ 條件需求\]](#37-support-autorun-conditional-requirement)</span><span class="sxs-lookup"><span data-stu-id="a03c5-134">[3.7 Support Autorun \[Conditional Requirement\]](#37-support-autorun-conditional-requirement)</span></span>
-   [<span data-ttu-id="a03c5-135">可靠性</span><span class="sxs-lookup"><span data-stu-id="a03c5-135">Reliability</span></span>](#reliability)
    -   [<span data-ttu-id="a03c5-136">4.1 消除不必要的重新開機</span><span class="sxs-lookup"><span data-stu-id="a03c5-136">4.1 Eliminate Unnecessary Reboots</span></span>](#41-eliminate-unnecessary-reboots)
    -   [<span data-ttu-id="a03c5-137">4.2 消除應用程式驗證器失敗</span><span class="sxs-lookup"><span data-stu-id="a03c5-137">4.2 Eliminate Application Verifier Failures</span></span>](#42-eliminate-application-verifier-failures)
    -   [<span data-ttu-id="a03c5-138">4.3 支援 Windows 錯誤報告和檔案版本資訊</span><span class="sxs-lookup"><span data-stu-id="a03c5-138">4.3 Support Windows Error Reporting and File Version Information</span></span>](#43-support-windows-error-reporting-and-file-version-information)
-   [<span data-ttu-id="a03c5-139">適用于 Windows 的通用控制器 Xbox 360 術語</span><span class="sxs-lookup"><span data-stu-id="a03c5-139">Xbox 360 Common Controller for Windows Terminology</span></span>](#xbox-360-common-controller-for-windows-terminology)
-   [<span data-ttu-id="a03c5-140">遊戲中介軟體產品的指導方針</span><span class="sxs-lookup"><span data-stu-id="a03c5-140">Guidelines for Game Middleware Products</span></span>](#guidelines-for-game-middleware-products)
    -   [<span data-ttu-id="a03c5-141">簡介</span><span class="sxs-lookup"><span data-stu-id="a03c5-141">Introduction</span></span>](#introduction)
    -   [<span data-ttu-id="a03c5-142">其他建議</span><span class="sxs-lookup"><span data-stu-id="a03c5-142">Additional Recommendations</span></span>](#additional-recommendations)
    -   [<span data-ttu-id="a03c5-143">Windows 遊戲展示</span><span class="sxs-lookup"><span data-stu-id="a03c5-143">Games for Windows Showcases</span></span>](#games-for-windows-showcases)
-   [<span data-ttu-id="a03c5-144">資源</span><span class="sxs-lookup"><span data-stu-id="a03c5-144">Resources</span></span>](#resources)

## <a name="differences-for-windows-8"></a><span data-ttu-id="a03c5-145">Windows 8 的差異</span><span class="sxs-lookup"><span data-stu-id="a03c5-145">Differences for Windows 8</span></span>

<span data-ttu-id="a03c5-146">以下是將這些技術需求和最佳作法套用 Windows 8 時的主要差異摘要。</span><span class="sxs-lookup"><span data-stu-id="a03c5-146">Here is a summary of the key differences when applying these technical requirements and best practices to Windows 8.</span></span>

<dl> <dt>

<span data-ttu-id="a03c5-147"><span id="The_Games_Explorer_UI_is_not_visible"></span><span id="the_games_explorer_ui_is_not_visible"></span><span id="THE_GAMES_EXPLORER_UI_IS_NOT_VISIBLE"></span>**不顯示遊戲瀏覽器 UI**</span><span class="sxs-lookup"><span data-stu-id="a03c5-147"><span id="The_Games_Explorer_UI_is_not_visible"></span><span id="the_games_explorer_ui_is_not_visible"></span><span id="THE_GAMES_EXPLORER_UI_IS_NOT_VISIBLE"></span>**The Games Explorer UI is not visible**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-148">您在 [ [遊戲瀏覽器](/previous-versions/windows/desktop/legacy/hh437965(v=vs.85)) ] 中註冊的所有遊戲都會顯示為新的 Windows UI 中的圖格，但不會再顯示與該標題相關聯的許多中繼資料。</span><span class="sxs-lookup"><span data-stu-id="a03c5-148">All games that you register with the [Games Explorer](/previous-versions/windows/desktop/legacy/hh437965(v=vs.85)) are surfaced as tiles in new Windows UI, but much of the metadata that is associated with the title is no longer visible.</span></span> <span data-ttu-id="a03c5-149">您仍然可以使用「遊戲定義檔案製造者」工具 (GDFMAKER.EXE) （現在可在 Windows 軟體開發套件 (SDK) 中取得）來撰寫中繼資料。</span><span class="sxs-lookup"><span data-stu-id="a03c5-149">You still use the Games Definition File Maker tool (GDFMAKER.EXE), which is now available in the Windows Software Development Kit (SDK), to author the metadata.</span></span> <span data-ttu-id="a03c5-150">您也可以使用現有的機制來部署中繼資料。</span><span class="sxs-lookup"><span data-stu-id="a03c5-150">You also use the existing mechanisms for deploying the metadata.</span></span> <span data-ttu-id="a03c5-151">繼續使用 Windows 7 測試您的遊戲瀏覽器註冊，然後確認新的 Windows UI 圖格會在安裝時出現 Windows 8 (請參閱 [1.1 遊戲瀏覽器整合](#11-games-explorer-integration)) 。</span><span class="sxs-lookup"><span data-stu-id="a03c5-151">Continue to test your Games Explorer registration by using Windows 7, and verify that the new Windows UI tile shows up when you install it on Windows 8 (see [1.1 Games Explorer Integration](#11-games-explorer-integration)).</span></span>

<span data-ttu-id="a03c5-152">若要下載 Windows 8 SDK，請參閱 [開發桌面應用程式的下載](https://msdn.microsoft.com/windows/desktop/aa904949)。</span><span class="sxs-lookup"><span data-stu-id="a03c5-152">To download the Windows 8 SDK, see [Downloads for developing desktop apps](https://msdn.microsoft.com/windows/desktop/aa904949).</span></span>

</dd> <dt>

<span data-ttu-id="a03c5-153"><span id="Registration_with_the_Game_Explorer_APIs_continues_to_be_the_mechanism_for_registering_your_game_with_Windows_Parental_Controls"></span><span id="registration_with_the_game_explorer_apis_continues_to_be_the_mechanism_for_registering_your_game_with_windows_parental_controls"></span><span id="REGISTRATION_WITH_THE_GAME_EXPLORER_APIS_CONTINUES_TO_BE_THE_MECHANISM_FOR_REGISTERING_YOUR_GAME_WITH_WINDOWS_PARENTAL_CONTROLS"></span>**使用遊戲瀏覽器 Api 進行註冊，仍是使用 Windows 家長監護註冊遊戲的機制**</span><span class="sxs-lookup"><span data-stu-id="a03c5-153"><span id="Registration_with_the_Game_Explorer_APIs_continues_to_be_the_mechanism_for_registering_your_game_with_Windows_Parental_Controls"></span><span id="registration_with_the_game_explorer_apis_continues_to_be_the_mechanism_for_registering_your_game_with_windows_parental_controls"></span><span id="REGISTRATION_WITH_THE_GAME_EXPLORER_APIS_CONTINUES_TO_BE_THE_MECHANISM_FOR_REGISTERING_YOUR_GAME_WITH_WINDOWS_PARENTAL_CONTROLS"></span>**Registration with the Game Explorer APIs continues to be the mechanism for registering your game with Windows Parental Controls**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-154">建議您在發行版本的 Windows 8 上執行 Windows SDK 版本的 GDFMAKER，以確保它可以填入所有目前支援的評等系統。</span><span class="sxs-lookup"><span data-stu-id="a03c5-154">We recommend that you run the Windows SDK version of GDFMAKER on the released version of Windows 8 to ensure that it can populate all currently supported rating systems.</span></span>

> [!Note]  
> <span data-ttu-id="a03c5-155">此版本的 GDFMAKER 需要 .NET 4.0。</span><span class="sxs-lookup"><span data-stu-id="a03c5-155">This version of GDFMAKER requires .NET 4.0.</span></span>

 

<span data-ttu-id="a03c5-156">請參閱 [1.2 支援系列的安全性/家長監護控制項](/windows)。</span><span class="sxs-lookup"><span data-stu-id="a03c5-156">See [1.2 Support Family Safety / Parental Controls](/windows).</span></span>

</dd> <dt>

<span data-ttu-id="a03c5-157"><span id="There_are_now_three_choices_for_using_the_XINPUT_API_depending_on_your_requirements"></span><span id="there_are_now_three_choices_for_using_the_xinput_api_depending_on_your_requirements"></span><span id="THERE_ARE_NOW_THREE_CHOICES_FOR_USING_THE_XINPUT_API_DEPENDING_ON_YOUR_REQUIREMENTS"></span>**根據您的需求，現在有三個選項可供您使用 XINPUT API**</span><span class="sxs-lookup"><span data-stu-id="a03c5-157"><span id="There_are_now_three_choices_for_using_the_XINPUT_API_depending_on_your_requirements"></span><span id="there_are_now_three_choices_for_using_the_xinput_api_depending_on_your_requirements"></span><span id="THERE_ARE_NOW_THREE_CHOICES_FOR_USING_THE_XINPUT_API_DEPENDING_ON_YOUR_REQUIREMENTS"></span>**There are now three choices for using the XINPUT API depending on your requirements**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-158">XINPUT 1.4 內建于 Windows 8。</span><span class="sxs-lookup"><span data-stu-id="a03c5-158">XINPUT 1.4 is built into Windows 8.</span></span> <span data-ttu-id="a03c5-159">Windows Store 應用程式和桌面 Win32 應用程式都可以使用 XINPUT 1.4。</span><span class="sxs-lookup"><span data-stu-id="a03c5-159">Both Windows Store apps and desktop Win32 apps can use XINPUT 1.4.</span></span> <span data-ttu-id="a03c5-160">所有版本的 Windows 都可以針對簡化的通用控制器使用 XINPUT 9.1.0，但不含 XINPUT 9.1.0 的轉散發套件。</span><span class="sxs-lookup"><span data-stu-id="a03c5-160">All versions of Windows can use XINPUT 9.1.0 for simplified common controllers, but there is no redistribution package with XINPUT 9.1.0.</span></span> <span data-ttu-id="a03c5-161">所有版本的 Windows 也都可以使用現有的 DirectX SDK 版本 XINPUT 1.3，這需要 DirectSetup 來部署。</span><span class="sxs-lookup"><span data-stu-id="a03c5-161">All versions of Windows can also use the existing DirectX SDK version XINPUT 1.3, which requires DirectSetup to deploy.</span></span>

<span data-ttu-id="a03c5-162">請參閱 [1.4 支援適用于 Windows 的 Xbox 360 通用控制器](#14-support-the-xbox-360-common-controller-for-windows-conditional-requirement)。</span><span class="sxs-lookup"><span data-stu-id="a03c5-162">See [1.4 Support the Xbox 360 Common Controller for Windows](#14-support-the-xbox-360-common-controller-for-windows-conditional-requirement).</span></span>

</dd> <dt>

<span data-ttu-id="a03c5-163"><span id="Only_a_limited_set_of_desktop_Win32_apps_are_supported_on_"></span><span id="only_a_limited_set_of_desktop_win32_apps_are_supported_on_"></span><span id="ONLY_A_LIMITED_SET_OF_DESKTOP_WIN32_APPS_ARE_SUPPORTED_ON_"></span>**Windows RT 僅支援一組有限的桌面 Win32 應用程式**</span><span class="sxs-lookup"><span data-stu-id="a03c5-163"><span id="Only_a_limited_set_of_desktop_Win32_apps_are_supported_on_"></span><span id="only_a_limited_set_of_desktop_win32_apps_are_supported_on_"></span><span id="ONLY_A_LIMITED_SET_OF_DESKTOP_WIN32_APPS_ARE_SUPPORTED_ON_"></span>**Only a limited set of desktop Win32 apps are supported on Windows RT**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-164">在 Windows 7 上執行的遊戲可以，而且應該在 Windows 8 x86 和 x64 平臺上正確執行。</span><span class="sxs-lookup"><span data-stu-id="a03c5-164">Games that run on Windows 7 can and should run correctly on Windows 8 x86 and x64 platforms.</span></span>

<span data-ttu-id="a03c5-165">請參閱 [2.2 支援 Windows X64 版本](#22-support-windows-x64-versions)。</span><span class="sxs-lookup"><span data-stu-id="a03c5-165">See [2.2 Support Windows x64 Versions](#22-support-windows-x64-versions).</span></span>

</dd> <dt>

<span data-ttu-id="a03c5-166"><span id="Ensure_any_OS_checks_are_done_correctly"></span><span id="ensure_any_os_checks_are_done_correctly"></span><span id="ENSURE_ANY_OS_CHECKS_ARE_DONE_CORRECTLY"></span>**確定已正確完成任何作業系統檢查**</span><span class="sxs-lookup"><span data-stu-id="a03c5-166"><span id="Ensure_any_OS_checks_are_done_correctly"></span><span id="ensure_any_os_checks_are_done_correctly"></span><span id="ENSURE_ANY_OS_CHECKS_ARE_DONE_CORRECTLY"></span>**Ensure any OS checks are done correctly**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-167">Windows 8 作業系統版本為6.2。</span><span class="sxs-lookup"><span data-stu-id="a03c5-167">The Windows 8 OS version is  6.2 .</span></span> <span data-ttu-id="a03c5-168">Windows 8 會傳遞我們建議用於遊戲部署的最小條碼測試。</span><span class="sxs-lookup"><span data-stu-id="a03c5-168">Windows 8 passes the current  minimum bar  tests that we recommend for game deployment.</span></span>

</dd> <dt>

<span data-ttu-id="a03c5-169"><span id="The__DirectX_End-User_Redistribution__package_runs_successfully_on_Windows_8__as_it_does_on_Windows_7__to_deploy_D3DX9__D3DX10__D3DX11__XINPUT_1.3__XAUDIO_2.7__XACTEngine__and_so_on"></span><span id="the__directx_end-user_redistribution__package_runs_successfully_on_windows_8__as_it_does_on_windows_7__to_deploy_d3dx9__d3dx10__d3dx11__xinput_1.3__xaudio_2.7__xactengine__and_so_on"></span><span id="THE__DIRECTX_END-USER_REDISTRIBUTION__PACKAGE_RUNS_SUCCESSFULLY_ON_WINDOWS_8__AS_IT_DOES_ON_WINDOWS_7__TO_DEPLOY_D3DX9__D3DX10__D3DX11__XINPUT_1.3__XAUDIO_2.7__XACTENGINE__AND_SO_ON"></span>**DirectX End-User 轉散發套件會在 Windows 8 上順利執行，就像在 Windows 7 上一樣，以部署 D3DX9、D3DX10、D3DX11、XINPUT 1.3、XAUDIO 2.7、XACTEngine 等等。**</span><span class="sxs-lookup"><span data-stu-id="a03c5-169"><span id="The__DirectX_End-User_Redistribution__package_runs_successfully_on_Windows_8__as_it_does_on_Windows_7__to_deploy_D3DX9__D3DX10__D3DX11__XINPUT_1.3__XAUDIO_2.7__XACTEngine__and_so_on"></span><span id="the__directx_end-user_redistribution__package_runs_successfully_on_windows_8__as_it_does_on_windows_7__to_deploy_d3dx9__d3dx10__d3dx11__xinput_1.3__xaudio_2.7__xactengine__and_so_on"></span><span id="THE__DIRECTX_END-USER_REDISTRIBUTION__PACKAGE_RUNS_SUCCESSFULLY_ON_WINDOWS_8__AS_IT_DOES_ON_WINDOWS_7__TO_DEPLOY_D3DX9__D3DX10__D3DX11__XINPUT_1.3__XAUDIO_2.7__XACTENGINE__AND_SO_ON"></span>**The  DirectX End-User Redistribution  package runs successfully on Windows 8, as it does on Windows 7, to deploy D3DX9, D3DX10, D3DX11, XINPUT 1.3, XAUDIO 2.7, XACTEngine, and so on**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-170">但是，DirectSetup 在僅安裝 .NET 4.0 的系統上有一個已知的問題，因為部署處理舊版受管理的 DirectX 1.1 元件。</span><span class="sxs-lookup"><span data-stu-id="a03c5-170">But, a known issue exists with DirectSetup on systems with only .NET 4.0 installed due to the deployment handling of the legacy Managed DirectX 1.1 assemblies.</span></span> <span data-ttu-id="a03c5-171">此問題適用于預設的 Windows 8 （預設為 .NET 4.5），以及已安裝 .NET 4.0 執行時間的全新 Windows XP 電腦。</span><span class="sxs-lookup"><span data-stu-id="a03c5-171">This issue applies to both Windows 8, which comes with .NET 4.5 by default, and  fresh  Windows XP computers with the .NET 4.0 runtime installed.</span></span> <span data-ttu-id="a03c5-172">但是，這個問題並不適用于 .NET 4.0 之前的任何 .NET 版本。</span><span class="sxs-lookup"><span data-stu-id="a03c5-172">But, this issue does not apply to any version of .NET prior to .NET 4.0.</span></span> <span data-ttu-id="a03c5-173">雖然 Windows 8 具有應用程式相容性行為，可自動解決此問題 (需要網路存取) ，但我們建議在2010年6月) 重新發行的可轉散發檔案版本中繼續部署 DirectSetup (更新的遊戲。</span><span class="sxs-lookup"><span data-stu-id="a03c5-173">While Windows 8 has an application compatibility behavior to resolve this issue automatically (which requires network access), we recommend that games that continue to deploy DirectSetup update to the DirectX SDK (June 2010) refreshed version of the REDIST files.</span></span> <span data-ttu-id="a03c5-174">同樣地，如果您將 DirectSetup 用於您的標題，請將您的標題向下修剪為所需的最小一組 Cab。</span><span class="sxs-lookup"><span data-stu-id="a03c5-174">As always, if you use DirectSetup for your title, trim your title down to the minimum required set of CABs.</span></span>

<span data-ttu-id="a03c5-175">請參閱 [3.4 正確安裝 Windows 資源](#34-install-windows-resources-properly)。</span><span class="sxs-lookup"><span data-stu-id="a03c5-175">See [3.4 Install Windows Resources Properly](#34-install-windows-resources-properly).</span></span>

</dd> <dt>

<span data-ttu-id="a03c5-176"><span id="Games_that_require_the_.NET__2.0__compatible_runtime__2.0__3.0__3.5__continue_to_use_existing_deployment_mechanisms"></span><span id="games_that_require_the_.net__2.0__compatible_runtime__2.0__3.0__3.5__continue_to_use_existing_deployment_mechanisms"></span><span id="GAMES_THAT_REQUIRE_THE_.NET__2.0__COMPATIBLE_RUNTIME__2.0__3.0__3.5__CONTINUE_TO_USE_EXISTING_DEPLOYMENT_MECHANISMS"></span>**需要 .NET 2.0 相容執行時間的遊戲 (2.0、3.0、3.5) 繼續使用現有的部署機制**</span><span class="sxs-lookup"><span data-stu-id="a03c5-176"><span id="Games_that_require_the_.NET__2.0__compatible_runtime__2.0__3.0__3.5__continue_to_use_existing_deployment_mechanisms"></span><span id="games_that_require_the_.net__2.0__compatible_runtime__2.0__3.0__3.5__continue_to_use_existing_deployment_mechanisms"></span><span id="GAMES_THAT_REQUIRE_THE_.NET__2.0__COMPATIBLE_RUNTIME__2.0__3.0__3.5__CONTINUE_TO_USE_EXISTING_DEPLOYMENT_MECHANISMS"></span>**Games that require the .NET  2.0  compatible runtime (2.0, 3.0, 3.5) continue to use existing deployment mechanisms**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-177">這些遊戲會在 Windows 8 上觸發應用程式相容性行為，以自動啟用 .NET 3.5 執行時間 (需要網路存取) 。</span><span class="sxs-lookup"><span data-stu-id="a03c5-177">These games trigger an application compatibility behavior on Windows 8 to enable the .NET 3.5 runtime automatically (which requires network access).</span></span> <span data-ttu-id="a03c5-178">但是，我們建議 .NET 開發人員移至 .NET 4.0 執行時間。</span><span class="sxs-lookup"><span data-stu-id="a03c5-178">But, we recommend that .NET developers move to the .NET 4.0 runtime.</span></span>

> [!Note]  
> <span data-ttu-id="a03c5-179">舊版受控 DirectX 1.1 元件與 .NET 4.x 執行時間不相容。</span><span class="sxs-lookup"><span data-stu-id="a03c5-179">The legacy Managed DirectX 1.1 assemblies are not compatible with the .NET 4.x runtime.</span></span>

 

<span data-ttu-id="a03c5-180">請參閱 [3.4 正確安裝 Windows 資源](#34-install-windows-resources-properly)。</span><span class="sxs-lookup"><span data-stu-id="a03c5-180">See [3.4 Install Windows Resources Properly](#34-install-windows-resources-properly).</span></span>

</dd> <dt>

<span data-ttu-id="a03c5-181"><span id="Use_of_an__autorunner__or_other_pre-install_technology_that_relies_on_.NET_is_not_recommended"></span><span id="use_of_an__autorunner__or_other_pre-install_technology_that_relies_on_.net_is_not_recommended"></span><span id="USE_OF_AN__AUTORUNNER__OR_OTHER_PRE-INSTALL_TECHNOLOGY_THAT_RELIES_ON_.NET_IS_NOT_RECOMMENDED"></span>**不建議使用依賴 .NET 的 autorunner 或其他預先安裝技術**</span><span class="sxs-lookup"><span data-stu-id="a03c5-181"><span id="Use_of_an__autorunner__or_other_pre-install_technology_that_relies_on_.NET_is_not_recommended"></span><span id="use_of_an__autorunner__or_other_pre-install_technology_that_relies_on_.net_is_not_recommended"></span><span id="USE_OF_AN__AUTORUNNER__OR_OTHER_PRE-INSTALL_TECHNOLOGY_THAT_RELIES_ON_.NET_IS_NOT_RECOMMENDED"></span>**Use of an  autorunner  or other pre-install technology that relies on .NET is not recommended**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-182">您可以假設只有 .NET 2.0 相容的執行時間 (2.0、3.0、3.5) 出現在 Windows Vista 和 Windows 7 上。</span><span class="sxs-lookup"><span data-stu-id="a03c5-182">You can assume that only .NET 2.0 compatible runtimes (2.0, 3.0, 3.5) are present on Windows Vista and Windows 7.</span></span> <span data-ttu-id="a03c5-183">根據預設，Windows 8 只有 .NET 4.0 相容的執行時間存在於。</span><span class="sxs-lookup"><span data-stu-id="a03c5-183">Only the .NET 4.0 compatible runtime is present on Windows 8 by default.</span></span>

<span data-ttu-id="a03c5-184">請參閱 [3.7 支援自動運行](#37-support-autorun-conditional-requirement)。</span><span class="sxs-lookup"><span data-stu-id="a03c5-184">See [3.7 Support Autorun](#37-support-autorun-conditional-requirement).</span></span>

</dd> <dt>

<span data-ttu-id="a03c5-185"><span id="There_is_an_updated_Application_Verifier_for_Windows_8"></span><span id="there_is_an_updated_application_verifier_for_windows_8"></span><span id="THERE_IS_AN_UPDATED_APPLICATION_VERIFIER_FOR_WINDOWS_8"></span>**Windows 8 有更新的應用程式驗證器**</span><span class="sxs-lookup"><span data-stu-id="a03c5-185"><span id="There_is_an_updated_Application_Verifier_for_Windows_8"></span><span id="there_is_an_updated_application_verifier_for_windows_8"></span><span id="THERE_IS_AN_UPDATED_APPLICATION_VERIFIER_FOR_WINDOWS_8"></span>**There is an updated Application Verifier for Windows 8**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-186">Windows 8 SDK 包含這個更新的應用程式驗證器。</span><span class="sxs-lookup"><span data-stu-id="a03c5-186">The Windows 8 SDK includes this updated Application Verifier.</span></span>

<span data-ttu-id="a03c5-187">請參閱 [4.2 消除應用程式驗證器失敗](#42-eliminate-application-verifier-failures)。</span><span class="sxs-lookup"><span data-stu-id="a03c5-187">See [4.2 Eliminate Application Verifier Failures](#42-eliminate-application-verifier-failures).</span></span>

</dd> </dl>

### <a name="additional-information"></a><span data-ttu-id="a03c5-188">其他資訊</span><span class="sxs-lookup"><span data-stu-id="a03c5-188">Additional Information</span></span>

<dl>

[<span data-ttu-id="a03c5-189">Windows 8 和 Windows Server 2012 相容性操作手冊</span><span class="sxs-lookup"><span data-stu-id="a03c5-189">Windows 8 and Windows Server 2012 compatibility cookbook</span></span>](/windows/desktop/w8cookbook/windows-8-and-windows-server-8-compatibility-cookbook-portal)  
[<span data-ttu-id="a03c5-190">DirectX SDK 在哪裡？</span><span class="sxs-lookup"><span data-stu-id="a03c5-190">Where is the DirectX SDK?</span></span>](/windows/desktop/directx-sdk--august-2009-)  
</dl>

## <a name="games-for-windows"></a><span data-ttu-id="a03c5-191">適用於 Windows 的遊戲</span><span class="sxs-lookup"><span data-stu-id="a03c5-191">Games for Windows</span></span>

<span data-ttu-id="a03c5-192">**遊戲需求摘要**</span><span class="sxs-lookup"><span data-stu-id="a03c5-192">**Summary of Games Requirements**</span></span>

<span data-ttu-id="a03c5-193">**客戶權益**</span><span class="sxs-lookup"><span data-stu-id="a03c5-193">**Customer Benefits**</span></span>

<span data-ttu-id="a03c5-194">電腦遊戲是 Windows 的重要娛樂經驗，但容易使用的考慮導致客戶挫折多年。</span><span class="sxs-lookup"><span data-stu-id="a03c5-194">Computer games are a key entertainment experience on Windows, but ease-of-use concerns have caused customer frustration over the years.</span></span> <span data-ttu-id="a03c5-195">傳統上，遊戲的安裝就像應用程式一樣，但使用的方式更像娛樂媒體 (電影或歌曲，例如) 。</span><span class="sxs-lookup"><span data-stu-id="a03c5-195">Traditionally, games are installed like applications, but they are utilized more like entertainment media (movies or songs, for example).</span></span> <span data-ttu-id="a03c5-196">創新，例如遊戲瀏覽器，以與標準應用程式不同的一致方式來公開遊戲。</span><span class="sxs-lookup"><span data-stu-id="a03c5-196">Innovations, such as Games Explorer, expose games in a consistent manner that is different from standard applications.</span></span> <span data-ttu-id="a03c5-197">這些創新也會在 Windows 中提供遊戲的第一級公民狀態，以及音樂和圖片。</span><span class="sxs-lookup"><span data-stu-id="a03c5-197">These innovations also give games first-class citizen status in Windows, together with Music and Pictures.</span></span> <span data-ttu-id="a03c5-198">下列需求有助於確保 Windows Vista 和 Windows 7 提供改良、更容易存取且整合的遊戲體驗。</span><span class="sxs-lookup"><span data-stu-id="a03c5-198">The following requirements help ensure that Windows Vista and Windows 7 provide an improved, more accessible, and unified gaming experience.</span></span> <span data-ttu-id="a03c5-199">同時也可確保與 Windows XP 的相容性。</span><span class="sxs-lookup"><span data-stu-id="a03c5-199">At the same time, they ensure compatibility with Windows XP.</span></span>

### <a name="11-games-explorer-integration"></a><span data-ttu-id="a03c5-200">1.1 遊戲瀏覽器整合</span><span class="sxs-lookup"><span data-stu-id="a03c5-200">1.1 Games Explorer Integration</span></span>

<dl> <dt>

<span data-ttu-id="a03c5-201"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**要求**</span><span class="sxs-lookup"><span data-stu-id="a03c5-201"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requirement**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-202">您必須在 Windows Vista 和 Windows 7 上的 [遊戲] 資料夾中，才能看到遊戲 **的 [遊戲** ] () 的遊戲。</span><span class="sxs-lookup"><span data-stu-id="a03c5-202">The game must be visible within Games Explorer (the **Games** folder) on Windows Vista and Windows 7.</span></span> <span data-ttu-id="a03c5-203">選取時，遊戲也必須顯示正確的中繼資料，其中包括發行者、開發人員、發行日期、版本、Windows 體驗指數分數、評等 (適用的) 以及相關聯的超連結。</span><span class="sxs-lookup"><span data-stu-id="a03c5-203">When selected, the game must also display correct meta data, which includes publisher, developer, release date, version, Windows Experience Index scores, rating (if applicable), and associated hyperlinks.</span></span>

<span data-ttu-id="a03c5-204">如果遊戲是透過線上遊戲服務進行數位分配，則服務提供者也應該會出現在 [遊戲] Explorer 中。</span><span class="sxs-lookup"><span data-stu-id="a03c5-204">If the game is digitally distributed through an online game service, then the service provider should also appear in Games Explorer.</span></span> <span data-ttu-id="a03c5-205">若要確保正確處理提供者並啟用 RSS 摘要，請使用第2版的遊戲定義檔架構 (GDFs) 應該使用。</span><span class="sxs-lookup"><span data-stu-id="a03c5-205">To ensure proper handling of the provider and to enable use of RSS feeds, version 2 of the schema for game definition files (GDFs) should be used.</span></span> <span data-ttu-id="a03c5-206"> (需 GDFs 的詳細資訊，請參閱其他資訊。 ) </span><span class="sxs-lookup"><span data-stu-id="a03c5-206">(For more information about GDFs, see Additional Information.)</span></span>

<span data-ttu-id="a03c5-207">此外，當遊戲安裝程式在 Windows Vista 和 Windows 7 上執行時，必須遵守下列規則：</span><span class="sxs-lookup"><span data-stu-id="a03c5-207">In addition, game installers must observe the following rules when they run on Windows Vista and Windows 7:</span></span>

-   <span data-ttu-id="a03c5-208">安裝不能建立快捷方式來啟動桌面、[開始] 功能表或任何其他位置中的遊戲。</span><span class="sxs-lookup"><span data-stu-id="a03c5-208">The installation must not create a shortcut to launch the game on the desktop, in the Start menu, or in any other location.</span></span>
-   <span data-ttu-id="a03c5-209">不得建立移除的工作和快捷方式。</span><span class="sxs-lookup"><span data-stu-id="a03c5-209">Tasks and shortcuts for removal must not be created.</span></span>
-   <span data-ttu-id="a03c5-210">使用者必須能夠使用 Windows Vista 和 Windows 7 主控台的 [程式和功能] 來移除遊戲，或在 Windows XP 主控台的 [新增或移除程式] 中新增或移除程式。</span><span class="sxs-lookup"><span data-stu-id="a03c5-210">Users must be able to remove the game by using Programs and Features in Control Panel on Windows Vista and Windows 7, or Add or Remove Programs in Control Panel on Windows XP.</span></span>

<span data-ttu-id="a03c5-211">在 Windows XP 和舊版的 Windows 上，遊戲安裝程式可以視需要建立程式群組、桌面圖示或快捷方式。</span><span class="sxs-lookup"><span data-stu-id="a03c5-211">On Windows XP, and on previous versions of Windows, the game installer is free to create program groups, desktop icons, or shortcuts as needed.</span></span>

</dd> <dt>

<span data-ttu-id="a03c5-212"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**理由**</span><span class="sxs-lookup"><span data-stu-id="a03c5-212"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Rationale**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-213">Windows 遊戲瀏覽器的概念類似于 Windows XP 資料夾 **我的檔** 或 **我的圖片**。</span><span class="sxs-lookup"><span data-stu-id="a03c5-213">Windows Games Explorer is similar in concept to the Windows XP folders **My Documents** or **My Pictures**.</span></span> <span data-ttu-id="a03c5-214">其構想是將類似的內容集中在同一處，並讓組織和內容相關的活動更容易。</span><span class="sxs-lookup"><span data-stu-id="a03c5-214">The idea is to centralize similar content in one place and allow for easier organization and context-sensitive activities.</span></span> <span data-ttu-id="a03c5-215">遊戲瀏覽器透過允許更豐富的組織和對遊戲的掌控，來擴充 **我的檔** 或 **我的圖片** 概念。</span><span class="sxs-lookup"><span data-stu-id="a03c5-215">Games Explorer extends the **My Documents** or **My Pictures** concept by allowing richer organization and control over games.</span></span> <span data-ttu-id="a03c5-216">遊戲 Explorer 讓玩家能夠觀賞、組織及與系統上安裝的所有遊戲互動。</span><span class="sxs-lookup"><span data-stu-id="a03c5-216">Games Explorer allows gamers to view, organize, and interact with all the games installed on their systems.</span></span> <span data-ttu-id="a03c5-217">它也可讓遊戲發行者更有效率地傳達重要的遊戲資訊。</span><span class="sxs-lookup"><span data-stu-id="a03c5-217">It also allows game publishers to communicate important game information more effectively.</span></span> <span data-ttu-id="a03c5-218">系統是資料驅動的，讓遊戲發行者很容易就能在產品的存留期更新遊戲資訊。</span><span class="sxs-lookup"><span data-stu-id="a03c5-218">The system is data-driven, making it easy for a game publisher to update game information over the life of the product.</span></span>

</dd> <dt>

<span data-ttu-id="a03c5-219"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**其他資訊**</span><span class="sxs-lookup"><span data-stu-id="a03c5-219"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Additional Information**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-220">您必須撰寫遊戲定義檔案 (GDF) ，此檔案是內嵌于二進位檔案中的 XML 文字檔 (可執行檔或 DLL) 作為資源，以及 Windows 圖示。</span><span class="sxs-lookup"><span data-stu-id="a03c5-220">Integration with Games Explorer requires that you author a game definition file (GDF), which is an XML text file that is embedded within a binary file (an executable file or a DLL) as a resource, along with a Windows icon.</span></span> <span data-ttu-id="a03c5-221">然後遊戲必須向遊戲瀏覽器註冊。</span><span class="sxs-lookup"><span data-stu-id="a03c5-221">The game must then be registered with Games Explorer.</span></span> <span data-ttu-id="a03c5-222">GDF 也可讓您公開提供的資訊，例如遊戲標題、發行者、開發人員、網站連結和選擇性工作。</span><span class="sxs-lookup"><span data-stu-id="a03c5-222">The GDF also enables the exposure of supplied information such as the game title, publisher, developer, links to websites and optional tasks.</span></span> <span data-ttu-id="a03c5-223">請注意，支援工作只能是網站的連結，但播放工作也可以用於選擇性的支援工作。</span><span class="sxs-lookup"><span data-stu-id="a03c5-223">Note that support tasks can be only links to Web sites, but play tasks can be used for optional support tasks as well.</span></span>

<span data-ttu-id="a03c5-224">遊戲瀏覽器可以利用縮圖點陣圖影像，但建議您改為提供具有大型圖示的 Windows 圖示資源 (256 256) 。</span><span class="sxs-lookup"><span data-stu-id="a03c5-224">Games Explorer can make use of a thumbnail bitmap image, but it is recommended that, instead, you provide a Windows icon resource with large icons (256 256).</span></span> <span data-ttu-id="a03c5-225">圖示資源應包含 256 256 48 48、32 32 和 16 16 的影像大小（以24位 (True 色彩) 和8位 (256) 色深度）。</span><span class="sxs-lookup"><span data-stu-id="a03c5-225">The icon resource should include image sizes of 256 256 48 48, 32 32, and 16 16 in both 24-bit (True Color) and 8-bit (256) color depths.</span></span> <span data-ttu-id="a03c5-226">Visual Studio 2008 和2010中提供的圖示編輯器支援這些大型圖示格式，就像 IconWorkshop Lite 一樣。</span><span class="sxs-lookup"><span data-stu-id="a03c5-226">The icon editor provided in Visual Studio 2008 and 2010 supports these large icon formats, as does IconWorkshop Lite.</span></span>

<span data-ttu-id="a03c5-227">DirectX SDK 提供與 **Windows 遊戲瀏覽器** 整合的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="a03c5-227">Details on integrating with **Windows Games Explorer** are provided in the DirectX SDK.</span></span> <span data-ttu-id="a03c5-228">DirectX SDK 包含遊戲定義檔 (GDF) 編輯器，以及 GDFExampleBinary 中包含的範例 GDF 範例。</span><span class="sxs-lookup"><span data-stu-id="a03c5-228">The DirectX SDK includes a game definition file (GDF) editor, as well as an example GDF that is included in GDFExampleBinary, a sample.</span></span> <span data-ttu-id="a03c5-229">另一個範例 GameUxInstallHelper，提供將所需功能整合到現有安裝系統的常式。</span><span class="sxs-lookup"><span data-stu-id="a03c5-229">Another sample, GameUxInstallHelper, provides routines for integrating the required functionality into existing installation systems.</span></span> <span data-ttu-id="a03c5-230">遊戲定義檔驗證程式 (gdftrace.exe) 提供評估 GDF 的偵錯工具支援。</span><span class="sxs-lookup"><span data-stu-id="a03c5-230">The Game Definition File Validator (gdftrace.exe) provides debugging support for evaluating a GDF.</span></span> <span data-ttu-id="a03c5-231">另請參閱 c + + 的 DirectX SDK 檔中的「Windows 遊戲瀏覽器整合」。</span><span class="sxs-lookup"><span data-stu-id="a03c5-231">Also see "Windows Games Explorer Integration" in the DirectX SDK Documentation for C++.</span></span>

<span data-ttu-id="a03c5-232">Windows 7 針對 GDF 檔案的架構推出了第二個版本的支援。</span><span class="sxs-lookup"><span data-stu-id="a03c5-232">Windows 7 introduces support for the second version of a schema for GDF files.</span></span> <span data-ttu-id="a03c5-233">新的版本包含一種簡化的方法，可用於建立播放工作和支援更新通知、遊戲服務提供者、遊戲統計資料，以及適用于遊戲服務提供者的 RSS 摘要。</span><span class="sxs-lookup"><span data-stu-id="a03c5-233">The new version includes a simplified method for creating play tasks and support for update notifications, game service providers, game statistics, and RSS feeds for game service providers.</span></span> <span data-ttu-id="a03c5-234">最新版本的 GameUxInstallHelper 會處理搭配 Windows Vista 使用第2版 GDF 檔案所需的所有註冊和舊版支援。</span><span class="sxs-lookup"><span data-stu-id="a03c5-234">The latest version of GameUxInstallHelper handles all of the registration and legacy support needed to use a version 2 GDF file with Windows Vista.</span></span> <span data-ttu-id="a03c5-235">從2009年8月或更新版本的 DirectX SDK 使用工具和範例程式碼。</span><span class="sxs-lookup"><span data-stu-id="a03c5-235">Use the tools and sample code from the DirectX SDK from August 2009 or later.</span></span> <span data-ttu-id="a03c5-236">建議使用第2版 GDF 檔案來啟用 RSS 摘要、遊戲統計資料和更新通知的支援。</span><span class="sxs-lookup"><span data-stu-id="a03c5-236">Using a version 2 GDF file is recommended to enable support for RSS feeds, game statistics, and update notifications.</span></span> <span data-ttu-id="a03c5-237">另請參閱範例 ProviderGDFExampleBinary 和 GameStatisticsExample。</span><span class="sxs-lookup"><span data-stu-id="a03c5-237">Also, see the samples ProviderGDFExampleBinary and GameStatisticsExample.</span></span>

<span data-ttu-id="a03c5-238">在 windows Vista Business Edition、Windows 7 Professional Edition 及 Windows Vista 和 Windows 7 的企業版上，[開始] 功能表上的 [遊戲] 連結是隱藏的。</span><span class="sxs-lookup"><span data-stu-id="a03c5-238">On Windows Vista Business Edition, Windows 7 Professional Edition, and Enterprise Edition of both Windows Vista and Windows 7, the Games link on the Start menu is hidden.</span></span> <span data-ttu-id="a03c5-239">您仍然可以按一下 [ **所有程式**]，然後按一下 [ **遊戲**]，以在 [開始] 功能表上使用 [遊戲] Explorer。</span><span class="sxs-lookup"><span data-stu-id="a03c5-239">Games Explorer is still available on the Start menu by clicking **All Programs**, and then clicking **Games**.</span></span>

<span data-ttu-id="a03c5-240">對於隨遊戲安裝的相關聯應用程式，而不是自己的遊戲，您可以在所有 Windows 版本上自由建立 [開始] 功能表程式群組、快捷方式和桌面圖示，包括 Windows Vista 和 Windows 7。</span><span class="sxs-lookup"><span data-stu-id="a03c5-240">For associated applications that are installed with your game, but not themselves games, you are free to create Start menu program groups, shortcuts, and desktop icons on all versions of Windows, including Windows Vista and Windows 7.</span></span> <span data-ttu-id="a03c5-241">這類相關聯的應用程式應通過適用于 Windows 需求的遊戲;如需詳細資訊，請參閱 [遊戲中介軟體產品的指導方針](#guidelines-for-game-middleware-products)。</span><span class="sxs-lookup"><span data-stu-id="a03c5-241">Such associated applications should pass applicable Games for Windows requirements; for details, see [Guidelines for Game Middleware Products](#guidelines-for-game-middleware-products).</span></span> <span data-ttu-id="a03c5-242">建議您將遊戲服務註冊為 Windows 7 的遊戲提供者。</span><span class="sxs-lookup"><span data-stu-id="a03c5-242">Game services are encouraged to register with Games Explorer as a Game Provider for Windows 7.</span></span> <span data-ttu-id="a03c5-243">1</span><span class="sxs-lookup"><span data-stu-id="a03c5-243">1</span></span>

</dd> </dl>

### <a name="12-support-family-safety--parental-controls"></a><span data-ttu-id="a03c5-244">1.2 支援家族安全性/家長監護控制項</span><span class="sxs-lookup"><span data-stu-id="a03c5-244">1.2 Support Family Safety / Parental Controls</span></span>

<dl> <dt>

<span data-ttu-id="a03c5-245"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**要求**</span><span class="sxs-lookup"><span data-stu-id="a03c5-245"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requirement**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-246">遊戲必須遵守下列規則，以完全支援 Windows 家庭安全：</span><span class="sxs-lookup"><span data-stu-id="a03c5-246">Games must fully support Windows Family Safety by adhering to the following rules:</span></span>

-   <span data-ttu-id="a03c5-247">遊戲不需要使用者具有系統管理認證即可播放。</span><span class="sxs-lookup"><span data-stu-id="a03c5-247">Games must not require that the user have administrative credentials to play.</span></span> <span data-ttu-id="a03c5-248">安裝、修補和移除可能需要系統管理認證，受限於第3節中的需求。</span><span class="sxs-lookup"><span data-stu-id="a03c5-248">Installation, patching, and removal can require administrative credentials, subject to the requirements in section 3.</span></span> <span data-ttu-id="a03c5-249"> (與此相關的是需求2.1，請遵循使用者帳戶控制指導方針。 ) </span><span class="sxs-lookup"><span data-stu-id="a03c5-249">(Related to this is requirement 2.1, Follow User Account Control Guidelines.)</span></span>
-   <span data-ttu-id="a03c5-250">以 Windows 支援的評等面板（例如 ESRB 和 PEGI）分級的遊戲，必須在其遊戲定義檔中包含其指派的評等資訊 (GDF) 。</span><span class="sxs-lookup"><span data-stu-id="a03c5-250">Games rated by Windows-supported ratings boards, such as ESRB and PEGI, must include their assigned ratings information in their game definition file (GDF).</span></span> <span data-ttu-id="a03c5-251">所有可用的評等資料都必須包含在每個當地語系化版本的 GDF 中，也必須包含在非語言相關的版本中。</span><span class="sxs-lookup"><span data-stu-id="a03c5-251">All available ratings data must be included in every localized version of the GDF, as well as in the language-neutral version.</span></span>
-   <span data-ttu-id="a03c5-252">遊戲必須在 GDF 中列出他們的可執行檔，以提供一般應用程式限制的良好使用者體驗，除非遊戲使用反盜版技術，在執行時間建立隨機命名的可執行檔。</span><span class="sxs-lookup"><span data-stu-id="a03c5-252">Games must list their executables in the GDF to provide a good user experience for General Application Restrictions, unless the game uses an anti-piracy technology that creates randomly named executables at runtime.</span></span>
-   <span data-ttu-id="a03c5-253">遊戲必須在啟動時呼叫遊戲瀏覽器介面的 **VerifyAccess** 方法（如果有的話），並在其傳回 \* pfHasAccess 為 FALSE 時結束。</span><span class="sxs-lookup"><span data-stu-id="a03c5-253">Games must call the **VerifyAccess** method of the Games Explorer interface during startup, if available, and exit if it returns \*pfHasAccess as FALSE.</span></span>

</dd> <dt>

<span data-ttu-id="a03c5-254"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**理由**</span><span class="sxs-lookup"><span data-stu-id="a03c5-254"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Rationale**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-255">所有遊戲都必須在標準使用者帳戶的內容中執行，以允許由 Windows 家長監護控制的帳戶播放遊戲。</span><span class="sxs-lookup"><span data-stu-id="a03c5-255">All games must execute within the context of a Standard User account to allow accounts that are controlled by Windows Parental Controls to play the game.</span></span> <span data-ttu-id="a03c5-256">家長希望能夠監視和控制其子系對遊戲的存取。</span><span class="sxs-lookup"><span data-stu-id="a03c5-256">Parents want the ability to monitor and control their children's access to games.</span></span> <span data-ttu-id="a03c5-257">此外，許多產業、政府和倡議團隊希望有更好的方式來允許家長監視和控制其子女所公開的遊戲。</span><span class="sxs-lookup"><span data-stu-id="a03c5-257">Moreover, numerous industry, government and advocacy groups desire better ways to allow parents to monitor and control the games to which their children are exposed.</span></span> <span data-ttu-id="a03c5-258">Microsoft 與遊戲瀏覽器所提供的架構結合，提供了透過 Windows 家長監護的這項功能。</span><span class="sxs-lookup"><span data-stu-id="a03c5-258">In conjunction with the architecture offered by Games Explorer, Microsoft provides parents this ability through Windows Parental Controls.</span></span>

<span data-ttu-id="a03c5-259">即使是未參與評等的遊戲，也需要較高的許可權，才能為大部分的使用者帳戶建立不佳的播放體驗。</span><span class="sxs-lookup"><span data-stu-id="a03c5-259">Even for games that do not participate in a ratings board program, requiring elevated privileges creates a poor play experience for the majority of user accounts.</span></span> <span data-ttu-id="a03c5-260">尤其是在啟用家長監護的情況下，在每次啟動遊戲時都需要父系輸入系統管理員密碼。</span><span class="sxs-lookup"><span data-stu-id="a03c5-260">This is particularly the case if Parental Controls are enabled, which would require the parent to enter the administrator password every time the game is launched.</span></span>

<span data-ttu-id="a03c5-261">Windows 家長監護系統可讓父系選取他們認為適用于其子系的評等。</span><span class="sxs-lookup"><span data-stu-id="a03c5-261">The Windows Parental Controls system allows parents to select the ratings that they believe are appropriate for their children.</span></span> <span data-ttu-id="a03c5-262">家長監護支援許多全球評量系統。</span><span class="sxs-lookup"><span data-stu-id="a03c5-262">Parental Controls support many of the worldwide ratings systems.</span></span> <span data-ttu-id="a03c5-263">家長監護也可讓家長根據內容描述項來限制對遊戲的存取 (如果適用的評等系統支援) ，並允許或禁止存取個別的遊戲。</span><span class="sxs-lookup"><span data-stu-id="a03c5-263">Parental Controls also allow parents to restrict access to games based on Content Descriptors (if the applicable rating system supports them) and to allow or disallow access to individual games.</span></span>

<span data-ttu-id="a03c5-264">Windows 家長監護的預設分級系統選項是以系統的地區設定為基礎，但可由使用者在 **主控台** 的 [**地區及語言選項**] 中進行修改。</span><span class="sxs-lookup"><span data-stu-id="a03c5-264">The default choice of rating system for Windows Parental Controls is based on the system's locale setting, but can be modified by the user in **Regional and Language Options** in **Control Panel**.</span></span> <span data-ttu-id="a03c5-265">因此，每個支援的語言都應該提供所有可用的分級資料，讓使用者可以自由地選取他們想要的任何評等面板。</span><span class="sxs-lookup"><span data-stu-id="a03c5-265">Therefore, every supported language should provide all available ratings data so that the user has the freedom to select whatever ratings board they desire.</span></span>

</dd> <dt>

<span data-ttu-id="a03c5-266"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**其他資訊**</span><span class="sxs-lookup"><span data-stu-id="a03c5-266"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Additional Information**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-267">沒有評等的遊戲仍然必須符合需求，才能以標準使用者的形式播放和呼叫 **VerifyAccess**。</span><span class="sxs-lookup"><span data-stu-id="a03c5-267">Games without a rating must still meet the requirements to support play as a Standard User and to call **VerifyAccess**.</span></span> <span data-ttu-id="a03c5-268">這類遊戲預設為未分級的類別，在 [遊戲瀏覽器] 中顯示「未提供評等」文字，並且受限於未分級遊戲之 **家長** 監護中的 **遊戲限制** 設定。</span><span class="sxs-lookup"><span data-stu-id="a03c5-268">Such games default to the Unrated category, display the text "No Rating Provided" in Games Explorer, and are subject to the **Game Restrictions** setting in **Parental Controls** for unrated games.</span></span> <span data-ttu-id="a03c5-269">預設 **限制** 設定為 [允許]。</span><span class="sxs-lookup"><span data-stu-id="a03c5-269">The default **Restrictions** setting is Allow.</span></span>

<span data-ttu-id="a03c5-270">如果包含的二進位檔未經過正確的 Authenticode 簽署，則會忽略 GDF 中的評等資訊。</span><span class="sxs-lookup"><span data-stu-id="a03c5-270">Rating information in the GDF will be ignored if the containing binary is not properly Authenticode signed.</span></span> <span data-ttu-id="a03c5-271">請參閱需求2.3。</span><span class="sxs-lookup"><span data-stu-id="a03c5-271">See requirement 2.3.</span></span>

<span data-ttu-id="a03c5-272">DirectX SDK 中的遊戲定義檔編輯器包含所有支援的評等系統，並會正確地將此資訊複寫到 GDF 的所有當地語系化版本，以及非語言相關版本。</span><span class="sxs-lookup"><span data-stu-id="a03c5-272">The Game Definition File Editor in the DirectX SDK includes all supported ratings systems and will correctly replicate this information to all localized versions of the GDF, as well as a language neutral version.</span></span> <span data-ttu-id="a03c5-273">GDFTrace 工具將會解碼並確認目前有所有評等資訊。</span><span class="sxs-lookup"><span data-stu-id="a03c5-273">The GDFTrace tool will decode and verify all ratings information present.</span></span> <span data-ttu-id="a03c5-274">使用這些工具的2009年8月版本或更新版本。</span><span class="sxs-lookup"><span data-stu-id="a03c5-274">Use the August 2009 version or later of these tools.</span></span>

<span data-ttu-id="a03c5-275">遊戲提供者的 GDF 通常不會包含評等資訊，而且會受限於未分級內容的設定。</span><span class="sxs-lookup"><span data-stu-id="a03c5-275">The GDF for a game provider typically contains no rating information, and it is subject to the settings for unrated content.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a03c5-276">作業系統</span><span class="sxs-lookup"><span data-stu-id="a03c5-276">Operating System</span></span></th>
<th><span data-ttu-id="a03c5-277">支援的評等系統</span><span class="sxs-lookup"><span data-stu-id="a03c5-277">Supported rating systems</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a03c5-278">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a03c5-278">Windows Vista</span></span></td>
<td><ul>
<li><span data-ttu-id="a03c5-279">CERO (日本) </span><span class="sxs-lookup"><span data-stu-id="a03c5-279">CERO (Japan)</span></span></li>
<li><span data-ttu-id="a03c5-280">ESRB (USA) </span><span class="sxs-lookup"><span data-stu-id="a03c5-280">ESRB (USA)</span></span></li>
<li><span data-ttu-id="a03c5-281">OFLC (澳大利亞) </span><span class="sxs-lookup"><span data-stu-id="a03c5-281">OFLC (Australia)</span></span></li>
<li><span data-ttu-id="a03c5-282">PEGI (歐洲) </span><span class="sxs-lookup"><span data-stu-id="a03c5-282">PEGI (Europe)</span></span></li>
<li><span data-ttu-id="a03c5-283">PEGI 芬蘭 (已淘汰) </span><span class="sxs-lookup"><span data-stu-id="a03c5-283">PEGI Finland (deprecated)</span></span></li>
<li><span data-ttu-id="a03c5-284">PEGI 葡萄牙</span><span class="sxs-lookup"><span data-stu-id="a03c5-284">PEGI Portugal</span></span></li>
<li><span data-ttu-id="a03c5-285">PEGI/BBFC (英國) </span><span class="sxs-lookup"><span data-stu-id="a03c5-285">PEGI/BBFC (United Kingdom)</span></span></li>
<li><span data-ttu-id="a03c5-286">USK (德國) </span><span class="sxs-lookup"><span data-stu-id="a03c5-286">USK (Germany)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a03c5-287">Windows Vista （含 service pack）</span><span class="sxs-lookup"><span data-stu-id="a03c5-287">Windows Vista with a service pack</span></span></td>
<td><span data-ttu-id="a03c5-288">適用于 Windows Vista 的 Service pack 新增下列支援：</span><span class="sxs-lookup"><span data-stu-id="a03c5-288">Service packs for Windows Vista add support for the following:</span></span><br/>
<ul>
<li><span data-ttu-id="a03c5-289">GRB (南韓國) </span><span class="sxs-lookup"><span data-stu-id="a03c5-289">GRB (South Korea)</span></span></li>
<li><span data-ttu-id="a03c5-290">ESRB &quot; 輕度的 &quot; 變異內容描述項</span><span class="sxs-lookup"><span data-stu-id="a03c5-290">ESRB &quot;Mild&quot; variant content descriptors</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a03c5-291">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a03c5-291">Windows 7</span></span></td>
<td><span data-ttu-id="a03c5-292">Windows 7 支援 Windows Vista 支援的分級系統，並新增下列支援：</span><span class="sxs-lookup"><span data-stu-id="a03c5-292">Windows 7 supports the ratings systems supported by Windows Vista and adds support for the following:</span></span> <br/>
<ul>
<li><span data-ttu-id="a03c5-293">CSRR (臺灣) </span><span class="sxs-lookup"><span data-stu-id="a03c5-293">CSRR (Taiwan)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a03c5-294">Windows 8</span><span class="sxs-lookup"><span data-stu-id="a03c5-294">Windows 8</span></span></td>
<td><span data-ttu-id="a03c5-295">Windows 8 支援先前的分級系統，並新增下列支援：</span><span class="sxs-lookup"><span data-stu-id="a03c5-295">Windows 8 supports the previous ratings systems and adds support for the following:</span></span><br/>
<ul>
<li><span data-ttu-id="a03c5-296">COB-澳大利亞 (澳大利亞) </span><span class="sxs-lookup"><span data-stu-id="a03c5-296">COB-AU (Australia)</span></span></li>
<li><span data-ttu-id="a03c5-297">DJCTQ (巴西) </span><span class="sxs-lookup"><span data-stu-id="a03c5-297">DJCTQ (Brazil)</span></span></li>
<li><span data-ttu-id="a03c5-298">PFB (南非) </span><span class="sxs-lookup"><span data-stu-id="a03c5-298">PFB (South Africa)</span></span></li>
<li><span data-ttu-id="a03c5-299">OFLC-NZ (紐西蘭) </span><span class="sxs-lookup"><span data-stu-id="a03c5-299">OFLC-NZ (New Zealand)</span></span></li>
</ul>
<span data-ttu-id="a03c5-300">Windows 8 淘汰下列現已淘汰的系統支援：</span><span class="sxs-lookup"><span data-stu-id="a03c5-300">Windows 8 retires support for the following now deprecated systems:</span></span><br/>
<ul>
<li><span data-ttu-id="a03c5-301">PEGI-FI (芬蘭) </span><span class="sxs-lookup"><span data-stu-id="a03c5-301">PEGI-FI (Finland)</span></span></li>
<li><span data-ttu-id="a03c5-302">OFLC (澳大利亞) </span><span class="sxs-lookup"><span data-stu-id="a03c5-302">OFLC (Australia)</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="a03c5-303">包含新 ESRB 的 Windows Vista Service Pack 1 (SP1) 內容描述項的任何標題，在不含 Service Pack 的 Windows Vista 上會顯示為未分級。</span><span class="sxs-lookup"><span data-stu-id="a03c5-303">Any title that includes new ESRB Windows Vista Service Pack 1 (SP1) content descriptors will show as  Unrated  on Windows Vista without a service pack.</span></span>

 

<span data-ttu-id="a03c5-304">在不支援的作業系統版本上，會忽略較新的分級資料。</span><span class="sxs-lookup"><span data-stu-id="a03c5-304">Newer ratings data are ignored on versions of operating systems without support for them.</span></span> <span data-ttu-id="a03c5-305">PEGI (芬蘭) 變異現在已被取代為標準 PEGI (歐洲) 評等系統。</span><span class="sxs-lookup"><span data-stu-id="a03c5-305">The PEGI (Finland) variant is now deprecated in favor of the standard PEGI (Europe) rating system.</span></span> <span data-ttu-id="a03c5-306">OFLC 系統現在已淘汰，可改用適用于澳大利亞的 COB-AU。</span><span class="sxs-lookup"><span data-stu-id="a03c5-306">The OFLC system is now deprecated in favor of COB-AU for Australia.</span></span>

<span data-ttu-id="a03c5-307">如需有關使遊戲與標準使用者權限相容的詳細資訊，請參閱 [適用于遊戲開發人員的 DirectX 文章使用者帳戶控制](/windows/desktop/DxTechArts/user-account-control-for-game-developers)。</span><span class="sxs-lookup"><span data-stu-id="a03c5-307">For more information about making a game compatible with standard user privileges, see the DirectX article [User Account Control for Game Developers](/windows/desktop/DxTechArts/user-account-control-for-game-developers).</span></span>

<span data-ttu-id="a03c5-308">如需遊戲定義檔 (GDF) 的詳細資訊，請參閱需求1.1。</span><span class="sxs-lookup"><span data-stu-id="a03c5-308">See requirement 1.1 for more details on the game definition file (GDF).</span></span>

</dd> </dl>

### <a name="13-support-rich-saved-games"></a><span data-ttu-id="a03c5-309">1.3 支援豐富的儲存遊戲</span><span class="sxs-lookup"><span data-stu-id="a03c5-309">1.3 Support Rich Saved Games</span></span>

<span data-ttu-id="a03c5-310">\[這項需求已淘汰\]</span><span class="sxs-lookup"><span data-stu-id="a03c5-310">\[This requirement has been retired\]</span></span>

### <a name="14-support-the-xbox-360-common-controller-for-windows-conditional-requirement"></a><span data-ttu-id="a03c5-311">1.4 支援 Windows 條件式需求的 Xbox 360 通用控制器 \[\]</span><span class="sxs-lookup"><span data-stu-id="a03c5-311">1.4 Support the Xbox 360 Common Controller for Windows \[Conditional Requirement\]</span></span>

<dl> <dt>

<span data-ttu-id="a03c5-312"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**要求**</span><span class="sxs-lookup"><span data-stu-id="a03c5-312"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requirement**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-313">支援遊戲台控制器的遊戲必須支援使用 [XInput](/windows/desktop/xinput/xinput-game-controller-apis-portal) API 的適用于 Windows 的 Xbox 360 控制器。</span><span class="sxs-lookup"><span data-stu-id="a03c5-313">Games that support gamepad controllers must support the Xbox 360 Controller for Windows using the [XInput](/windows/desktop/xinput/xinput-game-controller-apis-portal) API.</span></span> <span data-ttu-id="a03c5-314">如果也支援 DirectInput 周邊，則也可以使用 DirectInput。</span><span class="sxs-lookup"><span data-stu-id="a03c5-314">If DirectInput peripherals are also supported, then DirectInput can also be used.</span></span> <span data-ttu-id="a03c5-315">但是，如果使用 Xbox 360 相容裝置，XInput 必須是預設的 API。</span><span class="sxs-lookup"><span data-stu-id="a03c5-315">However, XInput must be the default API if an Xbox 360 compatible device is used.</span></span>

<span data-ttu-id="a03c5-316">所有對通用控制器觸發程式和按鈕的參考都必須使用 Xbox 360 名稱。</span><span class="sxs-lookup"><span data-stu-id="a03c5-316">All references to common controller triggers and buttons must use the Xbox 360 names.</span></span> <span data-ttu-id="a03c5-317">如需詳細資訊，請參閱 [Xbox 360 Windows 術語的通用控制器](#xbox-360-common-controller-for-windows-terminology) 清單。</span><span class="sxs-lookup"><span data-stu-id="a03c5-317">See the [Xbox 360 Common Controller for Windows Terminology](#xbox-360-common-controller-for-windows-terminology) list for details.</span></span>

<span data-ttu-id="a03c5-318">當遊戲處於暫停或暫停狀態時，控制器振動必須關閉。</span><span class="sxs-lookup"><span data-stu-id="a03c5-318">Controller vibration must be turned off when the game is in a paused or suspended state.</span></span>

<span data-ttu-id="a03c5-319">滑鼠/鍵盤控制項隨時都不能完全停用。</span><span class="sxs-lookup"><span data-stu-id="a03c5-319">Mouse/keyboard control cannot be fully disabled at any time.</span></span> <span data-ttu-id="a03c5-320">至少要有一個選項可用來返回遊戲功能表。</span><span class="sxs-lookup"><span data-stu-id="a03c5-320">At a minimum, an option to return to game menus must be available.</span></span>

</dd> <dt>

<span data-ttu-id="a03c5-321"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**理由**</span><span class="sxs-lookup"><span data-stu-id="a03c5-321"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Rationale**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-322">這項需求讓玩家可以自由選擇使用 Xbox 360 控制器或鍵盤和滑鼠，這取決於哪些輸入方法是更自然且直覺的介面。</span><span class="sxs-lookup"><span data-stu-id="a03c5-322">This requirement gives gamers freedom of choice to use either the Xbox 360 controller or the keyboard and mouse, depending on which input method is more natural and intuitive interface.</span></span>

</dd> <dt>

<span data-ttu-id="a03c5-323"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**其他資訊**</span><span class="sxs-lookup"><span data-stu-id="a03c5-323"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Additional Information**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-324">這項需求並不適用于使用滑鼠和/或鍵盤的遊戲。</span><span class="sxs-lookup"><span data-stu-id="a03c5-324">This requirement does not apply to games that use only the mouse and/or the keyboard.</span></span>

<span data-ttu-id="a03c5-325">建議您將功能表導覽實作為使用廣泛接受的標準控制器按鈕：</span><span class="sxs-lookup"><span data-stu-id="a03c5-325">We recommend that menu navigation be implemented to use the widely accepted standard controller buttons:</span></span>

-   <span data-ttu-id="a03c5-326">A-接受</span><span class="sxs-lookup"><span data-stu-id="a03c5-326">A - Accept</span></span>
-   <span data-ttu-id="a03c5-327">B-取消</span><span class="sxs-lookup"><span data-stu-id="a03c5-327">B - Cancel</span></span>
-   <span data-ttu-id="a03c5-328">開始-接受或暫停</span><span class="sxs-lookup"><span data-stu-id="a03c5-328">Start - Accept or pause</span></span>
-   <span data-ttu-id="a03c5-329">返回-取消、返回一個畫面或開啟功能表層級</span><span class="sxs-lookup"><span data-stu-id="a03c5-329">Back - Cancel, back one screen or up a menu level</span></span>

<span data-ttu-id="a03c5-330">如需詳細資訊，請參閱 [XInput](/windows/desktop/xinput/xinput-game-controller-apis-portal)。</span><span class="sxs-lookup"><span data-stu-id="a03c5-330">For more info, see [XInput](/windows/desktop/xinput/xinput-game-controller-apis-portal).</span></span>

<span data-ttu-id="a03c5-331">[XInput 和 DirectInput](/windows/desktop/xinput/xinput-and-directinput)主題會討論同時使用這兩個 api 的問題。</span><span class="sxs-lookup"><span data-stu-id="a03c5-331">The topic [XInput and DirectInput](/windows/desktop/xinput/xinput-and-directinput) discusses issues with using both APIs at the same time.</span></span>

<span data-ttu-id="a03c5-332">建議您不要使用 DirectInput 來執行鍵盤或滑鼠控制項。</span><span class="sxs-lookup"><span data-stu-id="a03c5-332">It is recommended that DirectInput not be used to implement keyboard or mouse controls.</span></span> <span data-ttu-id="a03c5-333">鍵盤和滑鼠控制項應僅使用 Windows 訊息和 Win32 Api 來執行。</span><span class="sxs-lookup"><span data-stu-id="a03c5-333">Keyboard and mouse controls should only be implemented using Windows messages and Win32 APIs.</span></span> <span data-ttu-id="a03c5-334">如需有關如何在不使用 DirectInput 的情況下取得高解析度滑鼠移動資訊的詳細資訊，請參閱 [利用 High-Definition 滑鼠移動](/windows/desktop/DxTechArts/taking-advantage-of-high-dpi-mouse-movement)。</span><span class="sxs-lookup"><span data-stu-id="a03c5-334">For details on getting high-resolution mouse movement information without using DirectInput, see [Taking Advantage of High-Definition Mouse Movement](/windows/desktop/DxTechArts/taking-advantage-of-high-dpi-mouse-movement).</span></span>

</dd> </dl>

### <a name="15-support-multiple-aspect-ratios-and-resolutions"></a><span data-ttu-id="a03c5-335">1.5 支援多種外觀比例和解析度</span><span class="sxs-lookup"><span data-stu-id="a03c5-335">1.5 Support Multiple Aspect Ratios and Resolutions</span></span>

<dl> <dt>

<span data-ttu-id="a03c5-336"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**要求**</span><span class="sxs-lookup"><span data-stu-id="a03c5-336"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requirement**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-337">遊戲必須至少支援下列外觀比例和相關聯的螢幕解析度：</span><span class="sxs-lookup"><span data-stu-id="a03c5-337">The game must support at least the following aspect ratios and associated screen resolutions:</span></span>

-   <span data-ttu-id="a03c5-338">4:3 標準 (800 600 或 1024 768) </span><span class="sxs-lookup"><span data-stu-id="a03c5-338">4:3 normal (800 600 or 1024 768)</span></span>
-   <span data-ttu-id="a03c5-339">16:9 寬銀幕 (1280 720) </span><span class="sxs-lookup"><span data-stu-id="a03c5-339">16:9 widescreen (1280 720)</span></span>
-   <span data-ttu-id="a03c5-340">16:10 寬銀幕 (1152 720 或 1680 1050 或 800 480) </span><span class="sxs-lookup"><span data-stu-id="a03c5-340">16:10 widescreen (1152 720 or 1680 1050 or 800 480)</span></span>

<span data-ttu-id="a03c5-341">若要進行螢幕解析度設定和偵測，遊戲必須遵守下列規則：</span><span class="sxs-lookup"><span data-stu-id="a03c5-341">For screen resolution configuration and detection, the game must adhere to the following rules:</span></span>

-   <span data-ttu-id="a03c5-342">如果是支援的解決方案，遊戲預設會使用顯示裝置的桌面解析度。</span><span class="sxs-lookup"><span data-stu-id="a03c5-342">The game uses the desktop resolution of the display device by default if it is a supported resolution.</span></span> <span data-ttu-id="a03c5-343">如果遊戲選擇不同的預設解析度，就必須使用桌面外觀比例作為搜尋準則。</span><span class="sxs-lookup"><span data-stu-id="a03c5-343">The desktop aspect ratio must be used as a search criterion if the game chooses a different default resolution.</span></span>
-   <span data-ttu-id="a03c5-344">當進行變更時，遊戲必須提示使用者確認新的顯示設定。</span><span class="sxs-lookup"><span data-stu-id="a03c5-344">The game must prompt the user to confirm new display settings when a change is made.</span></span> <span data-ttu-id="a03c5-345">如果使用者未在15秒內接受，則顯示必須還原為先前的設定。</span><span class="sxs-lookup"><span data-stu-id="a03c5-345">If the user does not accept within 15 seconds, the display must revert to the previous setting.</span></span>
-   <span data-ttu-id="a03c5-346">遊戲不得延展圖元或置中4:3 轉譯視窗，以支援寬螢幕外觀比例。</span><span class="sxs-lookup"><span data-stu-id="a03c5-346">The game must not stretch pixels or center a 4:3 render window to support widescreen aspect ratios.</span></span> <span data-ttu-id="a03c5-347">不過，上下黑邊縮是可接受的。</span><span class="sxs-lookup"><span data-stu-id="a03c5-347">However, letterboxing is acceptable.</span></span>

</dd> <dt>

<span data-ttu-id="a03c5-348"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**理由**</span><span class="sxs-lookup"><span data-stu-id="a03c5-348"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Rationale**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-349">使用 Windows 3D desktop 時，無法假設特定的外觀比例或解析度，原因如下：</span><span class="sxs-lookup"><span data-stu-id="a03c5-349">With the Windows 3D desktop, a particular aspect ratio or resolution cannot be assumed, because of the following factors:</span></span>

-   <span data-ttu-id="a03c5-350">支援高詳細資料顯示。</span><span class="sxs-lookup"><span data-stu-id="a03c5-350">Support for high-detail displays.</span></span>
-   <span data-ttu-id="a03c5-351">增加寬螢幕顯示器的市場份額。</span><span class="sxs-lookup"><span data-stu-id="a03c5-351">Increased market share of widescreen monitors.</span></span>
-   <span data-ttu-id="a03c5-352">Windows Media Center 的 HDTV 部署。</span><span class="sxs-lookup"><span data-stu-id="a03c5-352">HDTV deployments for Windows Media Center.</span></span>
-   <span data-ttu-id="a03c5-353">協助工具需求。</span><span class="sxs-lookup"><span data-stu-id="a03c5-353">Accessibility requirements.</span></span>

</dd> <dt>

<span data-ttu-id="a03c5-354"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**其他資訊**</span><span class="sxs-lookup"><span data-stu-id="a03c5-354"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Additional Information**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-355">在理想的情況下，遊戲預設為顯示的原生外觀比例。</span><span class="sxs-lookup"><span data-stu-id="a03c5-355">Ideally, the game defaults to the native aspect ratio of the display.</span></span> <span data-ttu-id="a03c5-356">不過，可靠地取得這項資訊可能是一項挑戰，因此，如果是更一般的解決方案，遊戲可以假設桌面是以原生的外觀比例執行。</span><span class="sxs-lookup"><span data-stu-id="a03c5-356">However, obtaining this information reliably can be a challenge, so as a more general solution the game can assume that the desktop is running at the native aspect ratio.</span></span> <span data-ttu-id="a03c5-357">藉由呼叫 [**EnumDisplaySettings**](/windows/desktop/api/winuser/nf-winuser-enumdisplaysettingsa) 與列舉登錄設定，即可取得桌面解析度 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="a03c5-357">The desktop resolution can be obtained by calling [**EnumDisplaySettings**](/windows/desktop/api/winuser/nf-winuser-enumdisplaysettingsa) with ENUM\_REGISTRY\_SETTINGS.</span></span>

<span data-ttu-id="a03c5-358">如需更多詳細資訊，請參閱 DirectX 文章的外觀比例和寬螢幕區段， [介紹 Windows 遊戲開發人員的10英尺體驗](/windows/desktop/DxTechArts/introduction-to-the-10-foot-experience-for-windows-game-developers)。</span><span class="sxs-lookup"><span data-stu-id="a03c5-358">For more details, see the Aspect Ratio and Widescreen sections of the DirectX article [Introduction to the 10-Foot Experience for Windows Game Developers](/windows/desktop/DxTechArts/introduction-to-the-10-foot-experience-for-windows-game-developers).</span></span>

</dd> </dl>

### <a name="16-support-launch-from-windows-media-center"></a><span data-ttu-id="a03c5-359">1.6 支援從 Windows Media Center 啟動</span><span class="sxs-lookup"><span data-stu-id="a03c5-359">1.6 Support Launch from Windows Media Center</span></span>

<span data-ttu-id="a03c5-360">\[這項需求已淘汰。\]</span><span class="sxs-lookup"><span data-stu-id="a03c5-360">\[This requirement has been retired.\]</span></span>

### <a name="17-direct3d-support"></a><span data-ttu-id="a03c5-361">1.7 Direct3D 支援</span><span class="sxs-lookup"><span data-stu-id="a03c5-361">1.7 Direct3D Support</span></span>

<dl> <dt>

<span data-ttu-id="a03c5-362"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**要求**</span><span class="sxs-lookup"><span data-stu-id="a03c5-362"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requirement**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-363">如果遊戲使用 Direct3D，則支援的最低版本必須是 Direct3D 9，而且 Direct3D 必須是選取的預設轉譯器。</span><span class="sxs-lookup"><span data-stu-id="a03c5-363">If the game uses Direct3D, then the minimum version supported must be Direct3D 9, and Direct3D must be the default renderer selected.</span></span>

</dd> <dt>

<span data-ttu-id="a03c5-364"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**理由**</span><span class="sxs-lookup"><span data-stu-id="a03c5-364"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Rationale**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-365">Windows Vista 和 Windows 7 core 圖形架構是以 Direct3D 為中心所設計。</span><span class="sxs-lookup"><span data-stu-id="a03c5-365">The Windows Vista and Windows 7 core graphics architecture is designed around Direct3D.</span></span> <span data-ttu-id="a03c5-366">重新對應舊版介面可支援 Direct3D 8 和更早版本。</span><span class="sxs-lookup"><span data-stu-id="a03c5-366">Direct3D 8 and earlier versions are supported by remapping legacy interfaces.</span></span>

<span data-ttu-id="a03c5-367">強烈建議使用比 Direct3D 9 更新的 Direct3D 版本。</span><span class="sxs-lookup"><span data-stu-id="a03c5-367">Use of versions of Direct3D newer than Direct3D 9 is strongly encouraged.</span></span> <span data-ttu-id="a03c5-368">查看 Windows 展示的遊戲。1。</span><span class="sxs-lookup"><span data-stu-id="a03c5-368">See the Games for Windows Showcase S.1.</span></span> <span data-ttu-id="a03c5-369">需要 Direct3D 10 或 Direct3D 11 完全符合需求1.7 的規範。</span><span class="sxs-lookup"><span data-stu-id="a03c5-369">Requiring Direct3D 10 or Direct3D 11 is fully compliant with requirement 1.7.</span></span>

</dd> </dl>

### <a name="18-enable-high-dpi-aware"></a><span data-ttu-id="a03c5-370">1.8 啟用高 DPI 感知</span><span class="sxs-lookup"><span data-stu-id="a03c5-370">1.8 Enable High-DPI-Aware</span></span>

<dl> <dt>

<span data-ttu-id="a03c5-371"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**要求**</span><span class="sxs-lookup"><span data-stu-id="a03c5-371"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requirement**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-372">)  (當您在 Windows Vista 和 Windows 7 上以 1600 1200) 的顯示解析度進行調整時，遊戲及其安裝 144 (程式必須在沒有視覺問題150的情況下正確執行。</span><span class="sxs-lookup"><span data-stu-id="a03c5-372">Games and their installers must run correctly without visual problems when dots-per-inch (DPI) scaling is enabled (tested with 144 DPI for 150% scaling at display resolution of 1600 1200) on Windows Vista and Windows 7.</span></span>

<span data-ttu-id="a03c5-373">這通常需要遊戲可執行檔宣告為 DPI 感知。</span><span class="sxs-lookup"><span data-stu-id="a03c5-373">This typically requires the game executable to declare being DPI-aware.</span></span> <span data-ttu-id="a03c5-374">這是藉由內嵌資訊清單元素來達成： <dpiAware> true <dpiAware> 。</span><span class="sxs-lookup"><span data-stu-id="a03c5-374">This is accomplished by embedding a manifest element: <dpiAware>true<dpiAware> .</span></span>

</dd> <dt>

<span data-ttu-id="a03c5-375"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**理由**</span><span class="sxs-lookup"><span data-stu-id="a03c5-375"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Rationale**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-376">高品質的 LCD 監視器在電腦顯示時很常見，而且在以原生解析度驅動的情況下，它們的外觀最好 (通常是 1280 1024、1600 1200 等) 。</span><span class="sxs-lookup"><span data-stu-id="a03c5-376">High-quality LCD monitors are commonplace as computer displays, and they look best when driven at their native resolutions (typically 1280 1024, 1600 1200, and so on).</span></span> <span data-ttu-id="a03c5-377">如果客戶難以閱讀文字，並以此解析度查看影像，通常會將其電腦桌面設定為較低的解析度，並讓視覺構件免于 LCD 調整。</span><span class="sxs-lookup"><span data-stu-id="a03c5-377">Customers who have difficulty reading text and seeing images at this resolution often set their computer desktops to a lower resolution and suffer visual artifacts from LCD scaling.</span></span> <span data-ttu-id="a03c5-378">相反地，客戶可以保留原生大小的解析度，並變更 Windows 顯示器的 DPI，使專案和文字外觀更大，而不會犧牲影像品質。</span><span class="sxs-lookup"><span data-stu-id="a03c5-378">Instead, customers can leave the resolution at the native size and change the DPI of the Windows display, thus making item and text appearance larger without sacrificing image quality.</span></span>

<span data-ttu-id="a03c5-379">雖然這項功能在 Windows XP 之後已經以某種形式提供，但是客戶或 Oem 很少會啟用它。</span><span class="sxs-lookup"><span data-stu-id="a03c5-379">While this feature has been available in some form since Windows XP, it is seldom enabled by customers or by OEMs.</span></span> <span data-ttu-id="a03c5-380">現今所有電腦顯示的一半，會根據客戶的意見反應，設定為比監視器原生解析度更低的解析度。</span><span class="sxs-lookup"><span data-stu-id="a03c5-380">More than half of all computer displays today are set to a lower resolution than the monitor's native resolution, based on customer feedback.</span></span> <span data-ttu-id="a03c5-381">在初始設定期間，以及變更顯示設定時，Windows 7 會讓客戶更容易看到這項功能，而不需要變更桌面解析度。</span><span class="sxs-lookup"><span data-stu-id="a03c5-381">Windows 7 makes this feature much more visible to customers during initial setup and when changing display settings, encouraging them to use DPI scaling rather than change the desktop resolution.</span></span>

</dd> <dt>

<span data-ttu-id="a03c5-382"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**其他資訊**</span><span class="sxs-lookup"><span data-stu-id="a03c5-382"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Additional Information**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-383">如果在處理常式啟動程式碼中提早呼叫 [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) 函式，則可以改為使用。</span><span class="sxs-lookup"><span data-stu-id="a03c5-383">The [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) function can be used instead, if called early in the process startup code.</span></span> <span data-ttu-id="a03c5-384">建議您將新增至資訊清單，以確保在呼叫主要進入點之前，可能會初始化的 (的) 軟體元素沒有任何競爭情形。</span><span class="sxs-lookup"><span data-stu-id="a03c5-384">Adding to the manifest is preferred, to ensure there are no race conditions with software elements (such as DLLs) that might initialize before the main entry point is called.</span></span> <span data-ttu-id="a03c5-385">請注意， **SetProcessDPIAware** 只存在於 windows Vista 和 windows 7。</span><span class="sxs-lookup"><span data-stu-id="a03c5-385">Note that **SetProcessDPIAware** is only present on Windows Vista and Windows 7.</span></span>

<span data-ttu-id="a03c5-386">使用 Visual Studio 2005 和2008可輕鬆地新增資訊清單元素;建立名為 DPIaware 的檔案，其中包含下列文字：</span><span class="sxs-lookup"><span data-stu-id="a03c5-386">Adding the manifest element is easy to do with Visual Studio 2005 and 2008; create a file named dpiaware.manifest that contains the following text:</span></span>

``` syntax
            <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
            <asmv3:application>
            <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2005/WindowsSettings">
            <dpiAware>true</dpiAware>
            </asmv3:windowsSettings>
            </asmv3:application>
            </assembly>
```

<span data-ttu-id="a03c5-387">然後，在 Visual Studio 中，將 DPIware 加入至專案。</span><span class="sxs-lookup"><span data-stu-id="a03c5-387">Then, inside Visual Studio, add dpiware.manifest to the project.</span></span> <span data-ttu-id="a03c5-388">確定專案屬性中的 **內嵌資訊清單** 設定為 **[是]** 。</span><span class="sxs-lookup"><span data-stu-id="a03c5-388">Ensure that **Embed Manifest** is set to **Yes** in the project's properties.</span></span> <span data-ttu-id="a03c5-389">請注意，舊版的資訊清單工具 (Mt.exe) 將會使用 DPI 感知的資訊清單元素來產生假警告。</span><span class="sxs-lookup"><span data-stu-id="a03c5-389">Note that older versions of the Manifest Tool (Mt.exe) will generate a spurious warning with the DPI-aware manifest elements.</span></span> <span data-ttu-id="a03c5-390">若要解決此問題，請從 Windows SDK 將 Mt.exe 更新為最新版本。</span><span class="sxs-lookup"><span data-stu-id="a03c5-390">To resolve this, update Mt.exe to the latest version from the Windows SDK.</span></span>

<span data-ttu-id="a03c5-391">Visual Studio 2010 包含專案屬性中的設定，名為 **啟用 DPI 感知**，因此不需要 DPIaware 檔案。</span><span class="sxs-lookup"><span data-stu-id="a03c5-391">Visual Studio 2010 includes a setting in the project properties, named **Enable DPI Awareness**, that eliminates the need for a file like dpiaware.manifest.</span></span> <span data-ttu-id="a03c5-392">展開 [設定 **屬性**] 和 [**資訊清單] 工具**，然後選取 [**輸入 & 輸出**]，即可尋找 **啟用 DPI 感知**。</span><span class="sxs-lookup"><span data-stu-id="a03c5-392">Find **Enable DPI Awareness** by expanding **Configuration Properties** and **Manifest Tool**, and then selecting **Input & Output**.</span></span>

<span data-ttu-id="a03c5-393">在 Windows 上，傳統顯示模式的預設值為 96 DPI，這常見於 CRT 監視器。</span><span class="sxs-lookup"><span data-stu-id="a03c5-393">On Windows, the traditional display mode defaults to 96 DPI, which was common for CRT monitors.</span></span>

<span data-ttu-id="a03c5-394">當全螢幕應用程式變更顯示解析度時，它們通常會在設定緩衝區和顯示矩形時使用視窗訊息和度量。</span><span class="sxs-lookup"><span data-stu-id="a03c5-394">While full-screen applications change the display resolution, they often use window messages and metrics when setting up buffers and display rectangles.</span></span> <span data-ttu-id="a03c5-395">DPI 虛擬化會將這些全螢幕顯示模式顯示為已裁剪，並宣告 DPI 感知，以防止這些問題。</span><span class="sxs-lookup"><span data-stu-id="a03c5-395">DPI virtualization causes these full-screen display modes to appear cropped, and declaring DPI-aware will prevent these problems.</span></span> <span data-ttu-id="a03c5-396">如需詳細資訊，請參閱 [撰寫 DPI-Aware 的 Win32 應用程式](../hidpi/high-dpi-desktop-application-development-on-windows.md)。</span><span class="sxs-lookup"><span data-stu-id="a03c5-396">For more information, see [Writing DPI-Aware Win32 Applications](../hidpi/high-dpi-desktop-application-development-on-windows.md).</span></span>

</dd> </dl>

## <a name="security-and-compatibility"></a><span data-ttu-id="a03c5-397">安全性與相容性</span><span class="sxs-lookup"><span data-stu-id="a03c5-397">Security and Compatibility</span></span>

<span data-ttu-id="a03c5-398">**安全性與相容性需求的摘要**</span><span class="sxs-lookup"><span data-stu-id="a03c5-398">**Summary of Security and Compatibility Requirements**</span></span>

<span data-ttu-id="a03c5-399">**客戶權益**</span><span class="sxs-lookup"><span data-stu-id="a03c5-399">**Customer Benefits**</span></span>

<span data-ttu-id="a03c5-400">下列需求可改善遊戲的整體安全性，並協助確保它們能在不同的架構上、不同的設定下和不同的模式下使用 Windows。</span><span class="sxs-lookup"><span data-stu-id="a03c5-400">The following requirements improve the overall security of games and help ensure that they work with Windows on different architectures, under different configurations, and in different modes.</span></span>

### <a name="21-follow-user-account-control-guidelines"></a><span data-ttu-id="a03c5-401">2.1 遵循使用者帳戶控制指導方針</span><span class="sxs-lookup"><span data-stu-id="a03c5-401">2.1 Follow User Account Control Guidelines</span></span>

<dl> <dt>

<span data-ttu-id="a03c5-402"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**要求**</span><span class="sxs-lookup"><span data-stu-id="a03c5-402"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requirement**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-403">每個可執行檔 (也就是說，副檔名為 .exe) 的每個檔案都必須包含內嵌的資訊清單，藉由包含下列標記來定義其執行層級：</span><span class="sxs-lookup"><span data-stu-id="a03c5-403">Every executable file (that is, every file that has a .exe extension) must contain an embedded manifest that defines its execution level by including the following tag:</span></span>

``` syntax
            <requestedExecutionLevel>
```

<span data-ttu-id="a03c5-404">根據需求1.2，主要遊戲和自動執行執行檔必須具有 asInvoker 的執行層級，才能支援標準使用者內容。</span><span class="sxs-lookup"><span data-stu-id="a03c5-404">Per requirement 1.2, the main game and Autorun executable must have the execution level of asInvoker to support Standard User contexts.</span></span>

<span data-ttu-id="a03c5-405">具有向 **檔案總管** 註冊之檔案關聯的使用者資料檔案，必須放在 CSIDL PERSONAL (所指定的資料夾子資料夾中，也稱為 [檔] \_ 或 [**我的檔**) ]。 </span><span class="sxs-lookup"><span data-stu-id="a03c5-405">User data files that have file associations registered with **File Explorer** must be placed in a subfolder of the folder that is specified by CSIDL\_PERSONAL (also called **Documents** or **My Documents**).</span></span> <span data-ttu-id="a03c5-406">所有其他的使用者資料檔案都必須儲存在 CSIDL \_ LOCAL \_ APPDATA 或 CSIDL \_ COMMON APPDATA 所指定之資料夾的子資料夾中 \_ 。</span><span class="sxs-lookup"><span data-stu-id="a03c5-406">All other user data files must be stored in a subfolder of the folders that are specified by CSIDL\_LOCAL\_APPDATA or CSIDL\_COMMON\_APPDATA.</span></span> <span data-ttu-id="a03c5-407">針對個別使用者和所有使用者，預設會隱藏這些目錄 (。 ) </span><span class="sxs-lookup"><span data-stu-id="a03c5-407">(These directories are hidden by default for individual users and for all users.)</span></span>

</dd> <dt>

<span data-ttu-id="a03c5-408"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**理由**</span><span class="sxs-lookup"><span data-stu-id="a03c5-408"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Rationale**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-409">如果應用程式只執行所需的許可權，則使用者的 Windows 體驗會更安全。</span><span class="sxs-lookup"><span data-stu-id="a03c5-409">A user's Windows experience is more secure if applications run only with the permissions needed.</span></span>

</dd> <dt>

<span data-ttu-id="a03c5-410"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**其他資訊**</span><span class="sxs-lookup"><span data-stu-id="a03c5-410"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Additional Information**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-411">如果應用程式中只有幾項功能需要系統管理許可權 (例如，需要設定防火牆) 的應用程式，則必須使用標準使用者權限來執行應用程式的主要處理常式。</span><span class="sxs-lookup"><span data-stu-id="a03c5-411">If only a few features in an application require administrative privileges (for example, an application that needs to configure a firewall), the main process of the application must still be run by using standard user privileges.</span></span> <span data-ttu-id="a03c5-412">需要系統管理許可權的功能必須移至個別的進程，例如安裝程式或設定公用程式。</span><span class="sxs-lookup"><span data-stu-id="a03c5-412">Features that require administrative privileges must be moved into a separate process, such as an installer or configuration utility.</span></span>

<span data-ttu-id="a03c5-413">如果不需要系統管理許可權，內嵌的資訊清單 XML 應該包含下列內容：</span><span class="sxs-lookup"><span data-stu-id="a03c5-413">If administrative privileges are not required, the embedded manifest XML should include the following:</span></span>

``` syntax
            <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
            <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
            <ms_asmv2:trustInfo xmlns:ms_asmv2="urn:schemas-microsoft-com:asm.v2">
            <ms_asmv2:security>
            <ms_asmv2:requestedPrivileges>
            <ms_asmv2:requestedExecutionLevel level="asInvoker" uiAccess="false" />
            </ms_asmv2:requestedPrivileges>
            </ms_asmv2:security>
            </ms_asmv2:trustInfo>
            </assembly>
```

<span data-ttu-id="a03c5-414">如果需要系統管理許可權，內嵌的資訊清單 XML 應該包含下列內容：</span><span class="sxs-lookup"><span data-stu-id="a03c5-414">If administrative privileges are required, the embedded manifest XML should include the following:</span></span>

``` syntax
            <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
            <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
            <ms_asmv2:trustInfo xmlns:ms_asmv2="urn:schemas-microsoft-com:asm.v2">
            <ms_asmv2:security>
            <ms_asmv2:requestedPrivileges>
            <ms_asmv2:requestedExecutionLevel level="requireAdministrator" uiAccess="false" />
            </ms_asmv2:requestedPrivileges>
            </ms_asmv2:security>
            </ms_asmv2:trustInfo>
            </assembly>
```

<span data-ttu-id="a03c5-415">使用 Visual Studio 2005，只要將包含上述其中一個區塊的資訊清單 () 資訊清單新增至專案，即可輕鬆地內嵌，並確保在資訊清單工具的專案屬性中， **內嵌資訊清單** 設定為 **[是]** 。</span><span class="sxs-lookup"><span data-stu-id="a03c5-415">With Visual Studio 2005 this is easily embedded by just adding a manifest (.manifest) file that contains one of the preceding blocks to the project, and ensuring that **Embed Manifest** is set to **Yes** in the project properties for Manifest Tool.</span></span> <span data-ttu-id="a03c5-416">針對 Visual Studio 2008 和2010，可以直接在 **資訊清單** 檔案頁面上連結器的專案屬性中設定 UAC 屬性。</span><span class="sxs-lookup"><span data-stu-id="a03c5-416">For Visual Studio 2008 and 2010, UAC properties can be set directly in the project properties for the linker on the **Manifest File** page.</span></span> <span data-ttu-id="a03c5-417">請注意，舊版的資訊清單工具 (Mt.exe) 會產生含有 UAC 資訊清單元素的偽造警告。</span><span class="sxs-lookup"><span data-stu-id="a03c5-417">Note that older versions of the Manifest Tool (Mt.exe) generate a spurious warning with the UAC manifest elements.</span></span> <span data-ttu-id="a03c5-418">若要解決此問題，請從 Windows SDK 將 Mt.exe 更新為最新版本。</span><span class="sxs-lookup"><span data-stu-id="a03c5-418">To resolve this, update Mt.exe to the latest version from the Windows SDK.</span></span>

<span data-ttu-id="a03c5-419">如需安裝、修補和移除等特殊案例的詳細資訊，請參閱需求3.1。</span><span class="sxs-lookup"><span data-stu-id="a03c5-419">See requirement 3.1 for details on the special cases of installation, patching, and removal.</span></span>

<span data-ttu-id="a03c5-420">動態連結程式庫 (Dll) 不需要這類資訊清單。</span><span class="sxs-lookup"><span data-stu-id="a03c5-420">Dynamic Link Libraries (DLLs) do not require such manifests.</span></span>

<span data-ttu-id="a03c5-421">如需使用者帳戶控制的詳細資訊，請參閱 [遊戲開發人員的使用者帳戶控制](/windows/desktop/DxTechArts/user-account-control-for-game-developers)。</span><span class="sxs-lookup"><span data-stu-id="a03c5-421">For more information about User Account Control, see [User Account Control for Game Developers](/windows/desktop/DxTechArts/user-account-control-for-game-developers).</span></span>

</dd> </dl>

### <a name="22-support-windows-x64-versions"></a><span data-ttu-id="a03c5-422">2.2 支援 Windows x64 版本</span><span class="sxs-lookup"><span data-stu-id="a03c5-422">2.2 Support Windows x64 Versions</span></span>

<dl> <dt>

<span data-ttu-id="a03c5-423"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**要求**</span><span class="sxs-lookup"><span data-stu-id="a03c5-423"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requirement**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-424">為了維持與64位 Windows 版本的相容性，遊戲應符合下列需求。</span><span class="sxs-lookup"><span data-stu-id="a03c5-424">To maintain compatibility with 64-bit editions of Windows, games should meet the following requirements.</span></span>

-   <span data-ttu-id="a03c5-425">標題和標題安裝程式不得包含任何16位程式碼，或依賴任何16位元件。</span><span class="sxs-lookup"><span data-stu-id="a03c5-425">Titles and title installers must not contain any 16-bit code or rely on any 16-bit component.</span></span>
-   <span data-ttu-id="a03c5-426">如果遊戲相依于操作的核心模式驅動程式，則必須提供這些驅動程式的 x64 版本。</span><span class="sxs-lookup"><span data-stu-id="a03c5-426">If the game is dependent on kernel-mode drivers for operation, x64 versions of these drivers must be available.</span></span> <span data-ttu-id="a03c5-427">遊戲安裝程式必須偵測並安裝適用于64位版本 Windows 的適當驅動程式和元件。</span><span class="sxs-lookup"><span data-stu-id="a03c5-427">The game setup must detect and install the proper drivers and components for the 64-bit editions of Windows.</span></span>

</dd> <dt>

<span data-ttu-id="a03c5-428"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**理由**</span><span class="sxs-lookup"><span data-stu-id="a03c5-428"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Rationale**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-429">許多 Windows Vista 和 Windows 7 使用者將會在產品的存留期內執行64位版本的作業系統，因此應用程式必須與此作業系統相容。</span><span class="sxs-lookup"><span data-stu-id="a03c5-429">Many Windows Vista and Windows 7 users will run 64-bit editions of the operating system over the life of the product, so it is crucial for applications to be compatible with this operating system.</span></span>

</dd> <dt>

<span data-ttu-id="a03c5-430"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**其他資訊**</span><span class="sxs-lookup"><span data-stu-id="a03c5-430"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Additional Information**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-431">Windows on Windows 64 (WOW64) 可讓32位程式碼在64位版本的 Windows 上執行，因此應用程式不需要在 Windows 的64版本上為原生64位程式碼。</span><span class="sxs-lookup"><span data-stu-id="a03c5-431">Windows on Windows 64 (WOW64) allows 32-bit code to run on 64-bit editions of Windows, so it is not necessary that the application be native 64-bit code on 64-bit editions of Windows.</span></span> <span data-ttu-id="a03c5-432">十六位程式碼不會在64位版本的 Windows 上執行。</span><span class="sxs-lookup"><span data-stu-id="a03c5-432">Sixteen-bit code does not run on 64-bit editions of Windows.</span></span>

<span data-ttu-id="a03c5-433">維持與 Windows XP Professional x64 Edition 的相容性並不是必要的，但強烈建議您這樣做。</span><span class="sxs-lookup"><span data-stu-id="a03c5-433">Maintaining compatibility with Windows XP Professional x64 Edition is not required, but it is strongly encouraged.</span></span>

<span data-ttu-id="a03c5-434">如需詳細資訊，請參閱 [遊戲開發人員的64位程式設計](/windows/desktop/DxTechArts/sixty-four-bit-programming-for-game-developers)。</span><span class="sxs-lookup"><span data-stu-id="a03c5-434">For details, see [64-bit programming for Game Developers](/windows/desktop/DxTechArts/sixty-four-bit-programming-for-game-developers).</span></span>

</dd> </dl>

### <a name="23-sign-files"></a><span data-ttu-id="a03c5-435">2.3 簽署檔案</span><span class="sxs-lookup"><span data-stu-id="a03c5-435">2.3 Sign Files</span></span>

<dl> <dt>

<span data-ttu-id="a03c5-436"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**要求**</span><span class="sxs-lookup"><span data-stu-id="a03c5-436"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requirement**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-437">所有的可執行程式碼檔案通常 (，副檔名為 .exe 或 .dll) 的檔案必須使用公開有效的 Authenticode 憑證來簽署，而且必須具有有效的時間戳記伺服器 URL，才能進行生產簽署。</span><span class="sxs-lookup"><span data-stu-id="a03c5-437">All executable code files (typically, files with the extension .exe or .dll) must be signed with a publicly valid Authenticode certificate, and must have a valid timestamp server URL for production signing.</span></span>

<span data-ttu-id="a03c5-438">如果您的遊戲使用 Windows Installer，) 必須簽署 ( .msi 檔案的安裝程式套件檔案。</span><span class="sxs-lookup"><span data-stu-id="a03c5-438">If your game uses Windows Installer, the installer package files (.msi files) must be signed.</span></span>

</dd> <dt>

<span data-ttu-id="a03c5-439"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**理由**</span><span class="sxs-lookup"><span data-stu-id="a03c5-439"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Rationale**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-440">簽署檔案可協助使用者決定是否信任應用程式，並確保使用者不會遭篡改。</span><span class="sxs-lookup"><span data-stu-id="a03c5-440">Signing a file helps users decide whether to trust an application, and assures users that files have not been tampered with.</span></span> <span data-ttu-id="a03c5-441">它也可讓應用程式在鎖定的環境中正確執行。</span><span class="sxs-lookup"><span data-stu-id="a03c5-441">It also allows applications to run properly in locked-down environments.</span></span>

</dd> <dt>

<span data-ttu-id="a03c5-442"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**其他資訊**</span><span class="sxs-lookup"><span data-stu-id="a03c5-442"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Additional Information**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-443">如需詳細資訊，請參閱 [遊戲開發人員的 Authenticode 簽署](/windows/desktop/DxTechArts/authenticode-signing-for-game-developers)。</span><span class="sxs-lookup"><span data-stu-id="a03c5-443">For details, see [Authenticode Signing for Game Developers](/windows/desktop/DxTechArts/authenticode-signing-for-game-developers).</span></span>

<span data-ttu-id="a03c5-444">如果您的遊戲使用 Windows Installer，建議您加入 MsiPatchCertificate 資料表，以啟用 UAC/LUA 修補。</span><span class="sxs-lookup"><span data-stu-id="a03c5-444">If your game uses Windows Installer, we recommend that you enable UAC/LUA patching, by including an MsiPatchCertificate table.</span></span> <span data-ttu-id="a03c5-445">如需詳細資訊，請參閱 [ (UAC) 修補的使用者帳戶控制](/windows/desktop/Msi/user-account-control--uac--patching)。</span><span class="sxs-lookup"><span data-stu-id="a03c5-445">For more information, see [User Account Control (UAC) Patching](/windows/desktop/Msi/user-account-control--uac--patching).</span></span>

<span data-ttu-id="a03c5-446">除非封包 ( .cab) 檔案相對較小，否則不建議您將其簽章 (小於 100 MB 的) 。</span><span class="sxs-lookup"><span data-stu-id="a03c5-446">We do not recommend signing cabinet (.cab) files, unless they are relatively small (less than 100 MB).</span></span>

</dd> </dl>

### <a name="24-sign-drivers"></a><span data-ttu-id="a03c5-447">2.4 簽署驅動程式</span><span class="sxs-lookup"><span data-stu-id="a03c5-447">2.4 Sign Drivers</span></span>

<dl> <dt>

<span data-ttu-id="a03c5-448"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**要求**</span><span class="sxs-lookup"><span data-stu-id="a03c5-448"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requirement**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-449">遊戲所安裝的任何核心模式驅動程式都必須使用公開有效的 Authenticode 憑證進行簽署。</span><span class="sxs-lookup"><span data-stu-id="a03c5-449">Any kernel-mode driver that is installed by the game must be signed with a publicly valid Authenticode certificate.</span></span>

<span data-ttu-id="a03c5-450">遊戲所安裝的任何核心模式硬體設備磁碟機都必須有 Microsoft 簽章，您可以從 Windows 硬體品質實驗室 (WHQL) 或從驅動程式可靠性簽章 (DRS) 程式取得該簽章。</span><span class="sxs-lookup"><span data-stu-id="a03c5-450">Any kernel-mode hardware device driver that is installed by the game must have a Microsoft signature, which can be obtained from the Windows Hardware Quality Labs (WHQL) or from the Driver Reliability Signature (DRS) program.</span></span>

</dd> <dt>

<span data-ttu-id="a03c5-451"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**理由**</span><span class="sxs-lookup"><span data-stu-id="a03c5-451"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Rationale**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-452">寫入不良或惡意程式碼的驅動程式可能會嚴重影響系統的穩定性和安全性。</span><span class="sxs-lookup"><span data-stu-id="a03c5-452">Poorly written or malware drivers can severely affect the stability and security of a system.</span></span> <span data-ttu-id="a03c5-453">在 Windows Vista 和 Windows 7 的64位版本上，不會載入未簽署的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="a03c5-453">On 64-bit editions of Windows Vista and Windows 7, unsigned drivers do not load.</span></span> <span data-ttu-id="a03c5-454">這項原則也可以針對32位版本的 Windows Vista 和 Windows 7 啟用。</span><span class="sxs-lookup"><span data-stu-id="a03c5-454">This policy can also be enabled for 32-bit editions of Windows Vista and Windows 7.</span></span>

</dd> <dt>

<span data-ttu-id="a03c5-455"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**其他資訊**</span><span class="sxs-lookup"><span data-stu-id="a03c5-455"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Additional Information**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-456">每項需求2.2 都需要32位和64位原生版本的所有核心模式驅動程式。</span><span class="sxs-lookup"><span data-stu-id="a03c5-456">Both 32-bit and 64-bit native versions of all kernel-mode drivers are needed per requirement 2.2.</span></span>

<span data-ttu-id="a03c5-457">如需 Microsoft 驅動程式簽署計畫的詳細資訊，請參閱 [Windows 硬體開發人員入口網站](https://www.microsoft.com/whdc/winlogo/hwrequirements.mspx)。</span><span class="sxs-lookup"><span data-stu-id="a03c5-457">More information about Microsoft driver signing programs can be found at the [Windows Hardware Developer portal](https://www.microsoft.com/whdc/winlogo/hwrequirements.mspx).</span></span>

</dd> </dl>

### <a name="25-perform-proper-version-checking"></a><span data-ttu-id="a03c5-458">2.5 執行適當的版本檢查</span><span class="sxs-lookup"><span data-stu-id="a03c5-458">2.5 Perform Proper Version Checking</span></span>

<dl> <dt>

<span data-ttu-id="a03c5-459"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**要求**</span><span class="sxs-lookup"><span data-stu-id="a03c5-459"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requirement**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-460">除非使用者授權合約禁止在未來的作業系統上使用，否則遊戲不能在未來的作業系統上執行，如 Windows 版本號碼的變更所述。</span><span class="sxs-lookup"><span data-stu-id="a03c5-460">Games must not fail to run on future operating systems as indicated by changes in the Windows version number, unless the End User License Agreement prohibits use on future operating systems.</span></span> <span data-ttu-id="a03c5-461">如果遊戲應該會失敗，就必須向使用者顯示適當的訊息，以正常方式進行。</span><span class="sxs-lookup"><span data-stu-id="a03c5-461">If the game is supposed to fail, it must do so gracefully by displaying an appropriate message to the user.</span></span>

<span data-ttu-id="a03c5-462">如果進行 Windows 版本檢查，則必須使用版本檢查 Api ([**GetVersionEx**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getversionexa) 或 [**VerifyVersionInfo**](/windows/desktop/api/winbase/nf-winbase-verifyversioninfoa)) 來檢查作業系統版本。</span><span class="sxs-lookup"><span data-stu-id="a03c5-462">If Windows version checks are made, the version-checking APIs ([**GetVersionEx**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getversionexa) or [**VerifyVersionInfo**](/windows/desktop/api/winbase/nf-winbase-verifyversioninfoa)) must be used to check the operating system version.</span></span> <span data-ttu-id="a03c5-463">不得讀取登錄機碼來判斷版本。</span><span class="sxs-lookup"><span data-stu-id="a03c5-463">Registry keys must not be read to determine the version.</span></span>

<span data-ttu-id="a03c5-464">DirectX 執行時間的明確版本檢查不能出現在遊戲中。</span><span class="sxs-lookup"><span data-stu-id="a03c5-464">Explicit version checks for the DirectX runtime must not be present in the game.</span></span> <span data-ttu-id="a03c5-465">這些版本檢查不能出現在啟動 DirectX runtime 安裝程式 (DirectSetup) 的安裝中。</span><span class="sxs-lookup"><span data-stu-id="a03c5-465">These version checks must not be present in the installation that launches the DirectX runtime setup (DirectSetup).</span></span>

</dd> <dt>

<span data-ttu-id="a03c5-466"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**理由**</span><span class="sxs-lookup"><span data-stu-id="a03c5-466"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Rationale**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-467">當 Windows 使用者升級其作業系統時，不應該將它們封鎖為無法播放目前的遊戲，因為 Windows 版本號碼已增加。</span><span class="sxs-lookup"><span data-stu-id="a03c5-467">When Windows users upgrade their operating systems, they should not be blocked from playing current games simply because the Windows version number has increased.</span></span> <span data-ttu-id="a03c5-468">撰寫不當的版本檢查程式會繼續產生軟體的問題，否則，在較新版本的 Windows 上，或只是加入 Windows service pack，都能正常運作。</span><span class="sxs-lookup"><span data-stu-id="a03c5-468">Poorly written version checkers continue to create problems for software that, otherwise, works fine on newer versions of Windows or simply with the addition of a Windows service pack.</span></span>

<span data-ttu-id="a03c5-469">在不同版本的 Windows 上執行時，DirectX runtime 的脆弱版本檢查比較邏輯已建立許多失敗的安裝。</span><span class="sxs-lookup"><span data-stu-id="a03c5-469">Fragile version check comparison logic for the DirectX runtime has created numerous failed installations when it is run on different versions of Windows.</span></span> <span data-ttu-id="a03c5-470">DirectX 版本號碼只適用于核心作業系統元件。</span><span class="sxs-lookup"><span data-stu-id="a03c5-470">The DirectX version number applies only to the core operating system components.</span></span> <span data-ttu-id="a03c5-471">它並不適用于許多遊戲所使用的並存 DirectX SDK 元件。</span><span class="sxs-lookup"><span data-stu-id="a03c5-471">It does not apply to the side-by-side DirectX SDK components that are used by many games.</span></span>

</dd> <dt>

<span data-ttu-id="a03c5-472"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**其他資訊**</span><span class="sxs-lookup"><span data-stu-id="a03c5-472"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Additional Information**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-473">最常見的情況是查看安裝程式檢查是否有最低的 OS 版本。</span><span class="sxs-lookup"><span data-stu-id="a03c5-473">It is quite common to see installers check for a minimum OS version.</span></span> <span data-ttu-id="a03c5-474">不過，這項檢查必須小心完成，以確保其測試是否大於或等於，而不是簡單相等，進而鎖定特定版本的作業系統。</span><span class="sxs-lookup"><span data-stu-id="a03c5-474">This check, however, needs to be done with care to ensure that it tests for greater than or equal to, rather than simple equality, thereby locking to a specific version of the operating system.</span></span> <span data-ttu-id="a03c5-475">使用應用程式驗證器的 **HighVersionLie** 測試是一種快速又簡單的方式，可判斷安裝程式將如何回應作業系統版本號碼的重大變更。</span><span class="sxs-lookup"><span data-stu-id="a03c5-475">Using Application Verifier's **HighVersionLie** test is a quick and easy way to determine how your installer will react to a significant change in the OS version number.</span></span>

<span data-ttu-id="a03c5-476"> (DirectX 安裝程式) 適當地使用 DirectX 執行時間轉散發套件時，必須在安裝期間一律啟動它，最好是以無訊息模式執行。</span><span class="sxs-lookup"><span data-stu-id="a03c5-476">Proper use of the DirectX runtime redistribution package (DirectX Setup) involves always launching it during installation, preferably in silent mode.</span></span> <span data-ttu-id="a03c5-477">這可讓 Microsoft 提供的程式碼執行任何必要的版本更新。</span><span class="sxs-lookup"><span data-stu-id="a03c5-477">This allows the code that is provided by Microsoft to perform any required version updates.</span></span> <span data-ttu-id="a03c5-478">它也可讓您安裝任何選用的並存 DirectX SDK 元件，例如 D3DX、交易、MDX 或 XInput。</span><span class="sxs-lookup"><span data-stu-id="a03c5-478">It also allows installation of any optional side-by-side DirectX SDK components, such as D3DX, XACT, MDX, or XInput.</span></span>

<span data-ttu-id="a03c5-479">如需部署 DirectX 執行時間的最佳作法，請參閱 [遊戲開發人員的 Directx 安裝](/windows/desktop/DxTechArts/directx-setup-for-game-developers)。</span><span class="sxs-lookup"><span data-stu-id="a03c5-479">For best practices for deploying the DirectX runtime, see [DirectX Installation for Game Developers](/windows/desktop/DxTechArts/directx-setup-for-game-developers).</span></span>

<span data-ttu-id="a03c5-480">建議支援 Windows XP 的遊戲檢查2或更高版本的 service pack 層級，因為 Service Pack 2 (SP2) 和 Service Pack 3 (SP3) 提供大幅的安全性改良功能、簡化的 DirectX 執行時間轉散發需求，以及極廣泛的部署。</span><span class="sxs-lookup"><span data-stu-id="a03c5-480">It is recommended that games that support Windows XP check for a service pack level of 2 or higher, because Service Pack 2 (SP2) and Service Pack 3 (SP3) provide significant security improvements, a simplified DirectX Runtime Redistribution requirement, and extremely broad deployment.</span></span> <span data-ttu-id="a03c5-481">大部分支援 Windows XP 的新式 Microsoft 技術都需要 SP2 或 SP3 (XAudio2、Windows LIVE 的遊戲，以及) 。</span><span class="sxs-lookup"><span data-stu-id="a03c5-481">Most modern Microsoft technologies that support Windows XP require SP2 or SP3 (XAudio2, Games for Windows - LIVE, and so on).</span></span>

</dd> </dl>

### <a name="26-support-concurrent-user-sessions"></a><span data-ttu-id="a03c5-482">2.6 支援並行使用者會話</span><span class="sxs-lookup"><span data-stu-id="a03c5-482">2.6 Support Concurrent User Sessions</span></span>

<dl> <dt>

<span data-ttu-id="a03c5-483"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**要求**</span><span class="sxs-lookup"><span data-stu-id="a03c5-483"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requirement**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-484">依賴3D 圖形的遊戲不需要透過遠端桌面連線來運作，但使用者必須在遊戲失敗時收到警示。</span><span class="sxs-lookup"><span data-stu-id="a03c5-484">Games that rely on 3D graphics are not required to work over a remote desktop connection, but the user must be alerted when the game fails.</span></span>

<span data-ttu-id="a03c5-485">遊戲必須遵守下列規則，以支援標準 Windows 多工案例：</span><span class="sxs-lookup"><span data-stu-id="a03c5-485">Games must support standard Windows multitasking scenarios by adhering to the following rules:</span></span>

-   <span data-ttu-id="a03c5-486">遊戲不得封鎖並行使用者會話的使用。</span><span class="sxs-lookup"><span data-stu-id="a03c5-486">Games must not block the use of concurrent user sessions.</span></span>
-   <span data-ttu-id="a03c5-487">當遊戲已在另一個會話中執行時，必須在新的使用者會話中執行遊戲。</span><span class="sxs-lookup"><span data-stu-id="a03c5-487">A game must run in a new user session when it is already running in another session.</span></span>
-   <span data-ttu-id="a03c5-488">當另一個使用者在不同的會話中處於作用中狀態時，就不能聽到一個使用者會話中的遊戲音效。</span><span class="sxs-lookup"><span data-stu-id="a03c5-488">Game sound in one user session must not be heard when another user is active in a different session.</span></span>
-   <span data-ttu-id="a03c5-489">遊戲必須支援快速切換使用者。</span><span class="sxs-lookup"><span data-stu-id="a03c5-489">Games must support Fast User Switching.</span></span>
-   <span data-ttu-id="a03c5-490">遊戲不得嘗試停用標準工作切換。</span><span class="sxs-lookup"><span data-stu-id="a03c5-490">Games must not attempt to disable standard task switching.</span></span> <span data-ttu-id="a03c5-491">遊戲不得停用 ALT + TAB 鍵盤快捷方式。</span><span class="sxs-lookup"><span data-stu-id="a03c5-491">Games must not disable the ALT+TAB keyboard shortcut.</span></span> <span data-ttu-id="a03c5-492">允許遊戲停用輔助功能鍵盤快捷方式，如在 [遊戲中停用快速鍵](/windows/desktop/DxTechArts/disabling-shortcut-keys-in-games)所述。</span><span class="sxs-lookup"><span data-stu-id="a03c5-492">Games are allowed to disable accessibility keyboard shortcuts, as described in [Disabling Shortcut Keys in Games](/windows/desktop/DxTechArts/disabling-shortcut-keys-in-games).</span></span>

</dd> <dt>

<span data-ttu-id="a03c5-493"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**理由**</span><span class="sxs-lookup"><span data-stu-id="a03c5-493"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Rationale**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-494">Windows 使用者應該能夠在不發生衝突或中斷的情況下執行並行會話。</span><span class="sxs-lookup"><span data-stu-id="a03c5-494">Windows users should be able to run concurrent sessions without conflict or disruption.</span></span> <span data-ttu-id="a03c5-495">這是家庭、室友或其他人共用之 Windows 電腦的常見案例。</span><span class="sxs-lookup"><span data-stu-id="a03c5-495">This is a common scenario for a Windows computer that is shared by a family, roommates, or others.</span></span>

</dd> <dt>

<span data-ttu-id="a03c5-496"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**其他資訊**</span><span class="sxs-lookup"><span data-stu-id="a03c5-496"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Additional Information**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-497">若要測試遊戲是否在遠端會話中啟動，請 ([](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) SM \_ REMOTESESSION) 呼叫 GetSystemMetrics。</span><span class="sxs-lookup"><span data-stu-id="a03c5-497">To test whether the game is launched in a remote session, call [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics)(SM\_REMOTESESSION).</span></span> <span data-ttu-id="a03c5-498">非零值表示會話為遠端。</span><span class="sxs-lookup"><span data-stu-id="a03c5-498">A nonzero value indicates that the session is remote.</span></span>

<span data-ttu-id="a03c5-499">如需詳細資訊，請參閱 [快速切換使用者](/windows-hardware/drivers/display/fast-user-switching)。</span><span class="sxs-lookup"><span data-stu-id="a03c5-499">For more information, see [Fast User Switching](/windows-hardware/drivers/display/fast-user-switching).</span></span> <span data-ttu-id="a03c5-500">請注意，如果在使用者的時間已啟動時，[家長監護] 會啟用 [快速切換使用者]。</span><span class="sxs-lookup"><span data-stu-id="a03c5-500">Note that Fast User Switching occurs if Parental Controls time restrictions are enabled when the user's time is up.</span></span> <span data-ttu-id="a03c5-501">如需詳細資訊，請參閱需求1.2。</span><span class="sxs-lookup"><span data-stu-id="a03c5-501">See requirement 1.2 for more details.</span></span>

</dd> </dl>

### <a name="27-support-long-names"></a><span data-ttu-id="a03c5-502">2.7 支援長名稱</span><span class="sxs-lookup"><span data-stu-id="a03c5-502">2.7 Support Long Names</span></span>

<dl> <dt>

<span data-ttu-id="a03c5-503"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**要求**</span><span class="sxs-lookup"><span data-stu-id="a03c5-503"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requirement**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-504">如果遊戲支援儲存檔案，它必須能夠儲存具有完整名稱和路徑的檔案。</span><span class="sxs-lookup"><span data-stu-id="a03c5-504">If a game supports saving files, it must be able to save files that have long names and paths.</span></span> <span data-ttu-id="a03c5-505">遊戲必須適當地處理特殊檔案系統字元，例如 \\ /： \* ？</span><span class="sxs-lookup"><span data-stu-id="a03c5-505">The game must properly handle special file system characters, such as \\ / : \* ?</span></span> <span data-ttu-id="a03c5-506">" < >，在用來建立檔案名或路徑的任何使用者輸入欄位中。</span><span class="sxs-lookup"><span data-stu-id="a03c5-506">" < >, in any user input fields that are used to create file names or paths.</span></span>

<span data-ttu-id="a03c5-507">當使用者具有較長的使用者名稱時，遊戲必須能夠正常運作。</span><span class="sxs-lookup"><span data-stu-id="a03c5-507">Games must work properly when a user has a long user name.</span></span>

</dd> <dt>

<span data-ttu-id="a03c5-508"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**理由**</span><span class="sxs-lookup"><span data-stu-id="a03c5-508"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Rationale**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-509">播放程式習慣在基礎作業系統所支援的深層路徑上使用完整名稱。</span><span class="sxs-lookup"><span data-stu-id="a03c5-509">Players are accustomed to using long names on deep paths that are supported by the underlying operating system.</span></span>

</dd> <dt>

<span data-ttu-id="a03c5-510"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**其他資訊**</span><span class="sxs-lookup"><span data-stu-id="a03c5-510"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Additional Information**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-511">完整名稱定義為包含 Windows SDK 中定義之最大值的名稱。</span><span class="sxs-lookup"><span data-stu-id="a03c5-511">Long names are defined as those that contain the maximum values that are defined in the Windows SDK.</span></span>

</dd> </dl>

## <a name="installation"></a><span data-ttu-id="a03c5-512">安裝</span><span class="sxs-lookup"><span data-stu-id="a03c5-512">Installation</span></span>

<span data-ttu-id="a03c5-513">**安全性與相容性需求的摘要**</span><span class="sxs-lookup"><span data-stu-id="a03c5-513">**Summary of Security and Compatibility Requirements**</span></span>

<span data-ttu-id="a03c5-514">**客戶權益**</span><span class="sxs-lookup"><span data-stu-id="a03c5-514">**Customer Benefits**</span></span>

<span data-ttu-id="a03c5-515">客戶可以放心地在 Windows 上安裝應用程式，而不會降低作業系統或其他應用程式（如果應用程式使用官方系統元件散發方法）。</span><span class="sxs-lookup"><span data-stu-id="a03c5-515">Customers can be confident that applications will install on Windows without degrading the operating system or other applications if applications use official system component distribution methods.</span></span> <span data-ttu-id="a03c5-516">簡化的安裝體驗可為遊戲提供更容易存取和無障礙的現成體驗。</span><span class="sxs-lookup"><span data-stu-id="a03c5-516">A streamlined installation experience provides a more accessible and trouble-free out-of-box experience for games.</span></span>

### <a name="31-support-easy-installation"></a><span data-ttu-id="a03c5-517">3.1 支援輕鬆安裝</span><span class="sxs-lookup"><span data-stu-id="a03c5-517">3.1 Support Easy Installation</span></span>

<dl> <dt>

<span data-ttu-id="a03c5-518"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**要求**</span><span class="sxs-lookup"><span data-stu-id="a03c5-518"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requirement**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-519">遊戲必須執行下列動作，在安裝程式使用者介面中提供簡化的路徑：</span><span class="sxs-lookup"><span data-stu-id="a03c5-519">Games must provide a simplified path in the setup user interface by implementing the following:</span></span>

-   <span data-ttu-id="a03c5-520">顯示最多一個 EULA 提示字元。</span><span class="sxs-lookup"><span data-stu-id="a03c5-520">Display a maximum of one EULA prompt.</span></span>
-   <span data-ttu-id="a03c5-521">預設安裝路徑必須略過安裝 (的所有選取專案，例如安裝資料夾或元件選項) 、假設預設選項，然後在安裝成功時執行遊戲或啟動器，而不需要額外的提示。</span><span class="sxs-lookup"><span data-stu-id="a03c5-521">The default installation path must bypass all selections for the installation (such as installation folder or component selections), assume the default selections, and then run the game or launcher upon successful installation, without additional prompts.</span></span> <span data-ttu-id="a03c5-522">如有需要，可以為 advanced configuration 選項提供自訂安裝選項。</span><span class="sxs-lookup"><span data-stu-id="a03c5-522">If desired, a custom installation option can be provided for advanced configuration options.</span></span>
-   <span data-ttu-id="a03c5-523">安裝任何必要的作業系統元件 (例如 DirectX 和 Visual C 執行時間，) 使用正確的 Microsoft 轉散發套件。</span><span class="sxs-lookup"><span data-stu-id="a03c5-523">Install any required operating system components (such as the DirectX and Visual C runtimes) using the correct Microsoft redistribution packages.</span></span> <span data-ttu-id="a03c5-524">安裝應該以無訊息模式執行，而不需要提示，也不會受到元件版本檢查的保護。</span><span class="sxs-lookup"><span data-stu-id="a03c5-524">The installation should be performed silently, without prompting and without being guarded by component version checks.</span></span>
-   <span data-ttu-id="a03c5-525">透過 **主控台** 中的 **程式和功能**，為遊戲應用程式和產生的工作檔案提供移除。</span><span class="sxs-lookup"><span data-stu-id="a03c5-525">Provide removal through **Programs and Features** in **Control Panel** for both the game application and generated working files.</span></span> <span data-ttu-id="a03c5-526">建議刪除使用者所建立之任何資料檔案的選項。</span><span class="sxs-lookup"><span data-stu-id="a03c5-526">An option for deleting any data files that are created by the user is recommended.</span></span> <span data-ttu-id="a03c5-527">移除程式必須確定已移除所有已安裝的檔案，而且所有設定 (例如，已清除防火牆例外清單專案和登錄機碼) 。</span><span class="sxs-lookup"><span data-stu-id="a03c5-527">The removal process must ensure that all installed files are removed and all settings (for example, firewall exception list entries and registry keys) are cleared.</span></span> <span data-ttu-id="a03c5-528">重新發佈的作業系統元件不得移除。</span><span class="sxs-lookup"><span data-stu-id="a03c5-528">Redistributed operating system components must not be removed.</span></span>
-   <span data-ttu-id="a03c5-529">如果遊戲需要將例外狀況新增至 Windows 防火牆，安裝程式會提示您通知使用者需要進行這項變更。</span><span class="sxs-lookup"><span data-stu-id="a03c5-529">If the game requires exceptions to be added to the Windows Firewall, the setup process can prompt to inform users that this change is required.</span></span> <span data-ttu-id="a03c5-530">安裝開始之前，應該會出現此提示。</span><span class="sxs-lookup"><span data-stu-id="a03c5-530">This prompt should appear before installation begins.</span></span>

<span data-ttu-id="a03c5-531">安裝和移除可能需要系統管理許可權。</span><span class="sxs-lookup"><span data-stu-id="a03c5-531">Installation and removal can require administrative rights.</span></span> <span data-ttu-id="a03c5-532">視更新的頻率而定，修補程式可能需要提示輸入系統管理認證。</span><span class="sxs-lookup"><span data-stu-id="a03c5-532">Patching can require prompting for administrative credentials, depending on frequency of update.</span></span> <span data-ttu-id="a03c5-533">遊戲的正常播放不得要求系統管理許可權，每項需求2.1 都遵循使用者帳戶控制指導方針。</span><span class="sxs-lookup"><span data-stu-id="a03c5-533">Normal play of the game must not require administrative rights, per requirement 2.1 Follow User Account Control Guidelines.</span></span>

</dd> <dt>

<span data-ttu-id="a03c5-534"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**理由**</span><span class="sxs-lookup"><span data-stu-id="a03c5-534"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Rationale**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-535">Easy 安裝是以 Windows 為中心的遊戲開發原理，其設計目的是要簡化並簡化在執行 Windows 作業系統的電腦上安裝遊戲的繁瑣和混淆程式。</span><span class="sxs-lookup"><span data-stu-id="a03c5-535">Easy installation is a Windows-centric game development philosophy that is designed to simplify and streamline the sometimes tedious and confusing process of installing games on computers that are running Windows operating systems.</span></span> <span data-ttu-id="a03c5-536">您可以利用一組技術和最佳作法來啟用輕鬆安裝，以降低在 Windows 電腦上安裝遊戲的不必要複雜度和認知風險。</span><span class="sxs-lookup"><span data-stu-id="a03c5-536">Easy installation is enabled by utilizing a set of technologies and best practices that reduce the unnecessary complexity and perceived risk of installing games on Windows computers.</span></span>

<span data-ttu-id="a03c5-537">主要目標是：</span><span class="sxs-lookup"><span data-stu-id="a03c5-537">The key goals are to:</span></span>

-   <span data-ttu-id="a03c5-538">縮短進入遊戲的時間，然後開始玩遊戲。</span><span class="sxs-lookup"><span data-stu-id="a03c5-538">Reduce the amount of time to get into the game and begin play.</span></span>
-   <span data-ttu-id="a03c5-539">將對話方塊和選項數目減少為極少或無，以簡化遊戲安裝體驗。</span><span class="sxs-lookup"><span data-stu-id="a03c5-539">Reduce the number of dialog boxes and choices to very few, or none, in order to simplify the game installation experience.</span></span>

<span data-ttu-id="a03c5-540">某些傳統安裝具有允許非功能性安裝的提示，即使應用程式看似成功安裝也一樣。</span><span class="sxs-lookup"><span data-stu-id="a03c5-540">Some traditional installations have prompts that allow non-functional installations, even though the application appears to be successfully installed.</span></span> <span data-ttu-id="a03c5-541">例如，遊戲可能需要使用者接受 EULA。</span><span class="sxs-lookup"><span data-stu-id="a03c5-541">For example, a game can require a user to accept a EULA.</span></span> <span data-ttu-id="a03c5-542">接著會安裝該遊戲，然後會出現 DirectX EULA。</span><span class="sxs-lookup"><span data-stu-id="a03c5-542">The game is then installed, and then the DirectX EULA appears.</span></span> <span data-ttu-id="a03c5-543">此 EULA 可讓使用者拒絕安裝 DirectX 執行時間，並因此略過安裝。</span><span class="sxs-lookup"><span data-stu-id="a03c5-543">This EULA allows users to decline, and thus skip installation of the DirectX runtime.</span></span> <span data-ttu-id="a03c5-544">這種情況可能會導致遊戲因為遺失元件而無法執行。</span><span class="sxs-lookup"><span data-stu-id="a03c5-544">This scenario can result in a game that fails to run because of missing components.</span></span>

</dd> <dt>

<span data-ttu-id="a03c5-545"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**其他資訊**</span><span class="sxs-lookup"><span data-stu-id="a03c5-545"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Additional Information**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-546">如需有關遊戲安裝、非傳統的遊戲安裝技術、UAC 相容的修補解決方案，以及處理頻繁修補的詳細資訊，請參閱下列 DirectX 文章：</span><span class="sxs-lookup"><span data-stu-id="a03c5-546">For more information about game installation, non-traditional game installation techniques, UAC-compatible patching solutions, and handling frequent patching, see the following DirectX articles:</span></span>

-   [<span data-ttu-id="a03c5-547">簡化遊戲安裝</span><span class="sxs-lookup"><span data-stu-id="a03c5-547">Simplifying Game Installation</span></span>](/windows/desktop/DxTechArts/simplifying-game-installation)
-   [<span data-ttu-id="a03c5-548">適用于遊戲的隨選安裝</span><span class="sxs-lookup"><span data-stu-id="a03c5-548">Install-on-Demand for Games</span></span>](/windows/desktop/DxTechArts/install-on-demand-for-games)
-   [<span data-ttu-id="a03c5-549">在 Windows XP、Windows Vista 和 Windows 7 中修補遊戲軟體</span><span class="sxs-lookup"><span data-stu-id="a03c5-549">Patching Game Software in Windows XP, Windows Vista, and Windows 7</span></span>](/windows/desktop/DxTechArts/patching-methods-in-windows-xp-and-vista)
-   [<span data-ttu-id="a03c5-550">大量多人連線遊戲的安裝最佳做法</span><span class="sxs-lookup"><span data-stu-id="a03c5-550">Installation Best Practices for Massively Multiplayer Online Games</span></span>](/windows/desktop/DxTechArts/mmo-installation-best-practices)

> [!Note]  
> <span data-ttu-id="a03c5-551">只應針對目前的使用者和一般的共用使用者位置，移除使用者特定產生的資料檔案。</span><span class="sxs-lookup"><span data-stu-id="a03c5-551">Removing user-specific generated data files should be performed only for the current user and for common shared user locations.</span></span> <span data-ttu-id="a03c5-552">即使移除需要系統管理認證，仍沒有健全的方式可掃描系統，以移除其他使用者的使用者特定檔案。</span><span class="sxs-lookup"><span data-stu-id="a03c5-552">There is no robust way to scan the system to remove user-specific files for other users, even if the removal requires administrative credentials.</span></span>

 

</dd> </dl>

### <a name="32-support-user-account-control-for-installation"></a><span data-ttu-id="a03c5-553">3.2 支援安裝的使用者帳戶控制</span><span class="sxs-lookup"><span data-stu-id="a03c5-553">3.2 Support User Account Control for Installation</span></span>

<dl> <dt>

<span data-ttu-id="a03c5-554"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**要求**</span><span class="sxs-lookup"><span data-stu-id="a03c5-554"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requirement**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-555">遊戲安裝程式不得假設它是在與使用者相同的內容中執行。</span><span class="sxs-lookup"><span data-stu-id="a03c5-555">The game installer must not assume that it is running in the same context as the user.</span></span> <span data-ttu-id="a03c5-556">使用者專屬的位置會與安裝程式和播放機不同，即使是針對單一使用者系統，也是因為系統管理員認證提高許可權。</span><span class="sxs-lookup"><span data-stu-id="a03c5-556">User-specific locations will be different from the installer and the player even for single-user systems due to administrator credentials elevation.</span></span> <span data-ttu-id="a03c5-557">因此，當遊戲第一次執行時，它必須與安裝程式分開執行使用者特定的工作。</span><span class="sxs-lookup"><span data-stu-id="a03c5-557">Therefore, when a game runs for the first time, it must perform user-specific tasks, separately from the installation process.</span></span>

<span data-ttu-id="a03c5-558">當使用者裝載或加入多人遊戲時，不能出現 [Windows 防火牆例外] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="a03c5-558">The Windows Firewall exception dialog box must not appear when a user hosts or joins a multiplayer game.</span></span> <span data-ttu-id="a03c5-559">您必須在安裝時完成任何必要的設定。</span><span class="sxs-lookup"><span data-stu-id="a03c5-559">Any required configuration must be done at installation time.</span></span> <span data-ttu-id="a03c5-560">安裝指示應該會通知使用者，這項作業將會在安裝過程中發生。</span><span class="sxs-lookup"><span data-stu-id="a03c5-560">The setup instructions should inform the user that this operation will occur as part of the setup.</span></span>

<span data-ttu-id="a03c5-561">遊戲安裝程式必須提供內嵌的資訊清單，以根據需求2.1 遵循使用者帳戶控制指導方針，來指定所需的執行層級。</span><span class="sxs-lookup"><span data-stu-id="a03c5-561">The game installer must provide an embedded manifest that designates the required execution level, per requirement 2.1 Follow User Account Control Guidelines.</span></span>

<span data-ttu-id="a03c5-562">如果安裝程式完成之後，安裝程式啟動遊戲，則必須在原始使用者的內容中啟動。</span><span class="sxs-lookup"><span data-stu-id="a03c5-562">If the game is launched by the installer after installation is complete, it must be launched in the context of the original user.</span></span>

</dd> <dt>

<span data-ttu-id="a03c5-563"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**理由**</span><span class="sxs-lookup"><span data-stu-id="a03c5-563"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Rationale**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-564">Windows Vista 中的 Windows 作業系統最大的變更之一，就是新增使用者帳戶控制 (UAC) ，預設會以較少的許可權來執行應用程式。</span><span class="sxs-lookup"><span data-stu-id="a03c5-564">One of the largest changes to the Windows operating system in Windows Vista is the addition of User Account Control (UAC), which runs applications with reduced privileges by default.</span></span> <span data-ttu-id="a03c5-565">因此，安裝程式必須據以管理許可權等級。</span><span class="sxs-lookup"><span data-stu-id="a03c5-565">As a result, installers need to manage privilege levels accordingly.</span></span> <span data-ttu-id="a03c5-566">Windows 7 也會大量使用 UAC。</span><span class="sxs-lookup"><span data-stu-id="a03c5-566">Windows 7 also makes extensive use of UAC.</span></span> <span data-ttu-id="a03c5-567">雖然 Windows 7 改善了 UAC 的使用者體驗，但安裝程式仍然必須符合 Windows Vista 的相同需求，才能正常運作，而不需要依賴可能混淆的虛擬化行為。</span><span class="sxs-lookup"><span data-stu-id="a03c5-567">While Windows 7 improves the user experience of UAC, installers must still meet the same requirements as on Windows Vista to function properly, without relying on potentially confusing virtualization behavior.</span></span>

<span data-ttu-id="a03c5-568">在 Windows Vista 和 Windows 7 上，UAC 預設為使用中，而大部分的客戶 (88% 或更多，根據意見反應) 讓此功能保持啟用狀態。</span><span class="sxs-lookup"><span data-stu-id="a03c5-568">UAC is active by default on Windows Vista and Windows 7, and the vast majority of customers (88% or more, based on feedback) leave this feature enabled.</span></span>

</dd> <dt>

<span data-ttu-id="a03c5-569"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**其他資訊**</span><span class="sxs-lookup"><span data-stu-id="a03c5-569"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Additional Information**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-570">如需設定 Windows 防火牆的詳細資訊，請參閱 [適用于遊戲開發人員的 Windows 防火牆](/windows/desktop/DxTechArts/games-and-firewalls) 和 FirewallInstallHelper 範例的 DirectX 文章。</span><span class="sxs-lookup"><span data-stu-id="a03c5-570">For more details on configuring the Windows Firewall, see the DirectX article [Windows Firewall for Game Developers](/windows/desktop/DxTechArts/games-and-firewalls) and the FirewallInstallHelper sample.</span></span>

<span data-ttu-id="a03c5-571">如果安裝是由標準使用者啟動，而且安裝程式需要系統管理許可權 (也就是，在安裝程式結束時，標準啟動遊戲無法符合此需求的最後一個部分，也就是提示您輸入系統管理員認證) 。</span><span class="sxs-lookup"><span data-stu-id="a03c5-571">Standard launch of the game at the end of the installation process fails to meet the last aspect of this requirement if the installation is launched by a standard user, and if the setup process requires administrative privileges (that is, prompts for a administrator credentials).</span></span> <span data-ttu-id="a03c5-572">它也會繼承系統管理許可權，這是潛在的安全性風險。</span><span class="sxs-lookup"><span data-stu-id="a03c5-572">It also inherits administrative privileges, which is a potential security risk.</span></span> <span data-ttu-id="a03c5-573">相反地，安裝程式啟動載入器應該會在從安裝程式成功調用後啟動遊戲。</span><span class="sxs-lookup"><span data-stu-id="a03c5-573">Instead, a setup bootstrap loader should launch the game after returning from a successful invocation of the installer.</span></span> <span data-ttu-id="a03c5-574">如需詳細資訊，請參閱 MSDN 雜誌文章： [教您的應用程式使用 Windows Vista 使用者帳戶控制順利播放](/archive/msdn-magazine/2007/january/teach-your-apps-to-work-with-windows-vista-user-account-control)。</span><span class="sxs-lookup"><span data-stu-id="a03c5-574">For more information, see the MSDN Magazine article [Teach Your Apps to Play Nicely with Windows Vista User Account Control](/archive/msdn-magazine/2007/january/teach-your-apps-to-work-with-windows-vista-user-account-control).</span></span>

</dd> </dl>

### <a name="33-install-to-correct-folders"></a><span data-ttu-id="a03c5-575">3.3 安裝到正確的資料夾</span><span class="sxs-lookup"><span data-stu-id="a03c5-575">3.3 Install to Correct Folders</span></span>

<dl> <dt>

<span data-ttu-id="a03c5-576"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**要求**</span><span class="sxs-lookup"><span data-stu-id="a03c5-576"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requirement**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-577">依預設，針對所有使用者安裝的遊戲都必須安裝至 Program Files 資料夾。</span><span class="sxs-lookup"><span data-stu-id="a03c5-577">Games that are installed for all users must be installed to the Program Files folder by default.</span></span> <span data-ttu-id="a03c5-578">當遊戲第一次執行時，您必須撰寫使用者資料，而不是在安裝期間寫入。</span><span class="sxs-lookup"><span data-stu-id="a03c5-578">User data must be written when the game runs for the first time, not during the installation.</span></span>

</dd> <dt>

<span data-ttu-id="a03c5-579"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**理由**</span><span class="sxs-lookup"><span data-stu-id="a03c5-579"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Rationale**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-580">使用者應該能夠彈性地在需要的位置安裝應用程式。</span><span class="sxs-lookup"><span data-stu-id="a03c5-580">Users should have the flexibility to install applications where they need them.</span></span> <span data-ttu-id="a03c5-581">它們也應該具有一致且安全的體驗，以及檔案的預設位置。</span><span class="sxs-lookup"><span data-stu-id="a03c5-581">They should also have a consistent and secure experience with the default location of files.</span></span>

</dd> <dt>

<span data-ttu-id="a03c5-582"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**其他資訊**</span><span class="sxs-lookup"><span data-stu-id="a03c5-582"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Additional Information**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-583">遊戲可利用各種已知的資料夾位置 (例如，CSIDL \_ LOCAL \_ APPDATA 和 CSIDL COMMON) APPDATA 所指定的位置， \_ \_ 以儲存大量的遊戲資料和支援的可執行檔，以執行先進的隨選安裝和修補案例。</span><span class="sxs-lookup"><span data-stu-id="a03c5-583">Games can make use of the various known folder locations (such as those specified by CSIDL\_LOCAL\_APPDATA and CSIDL\_COMMON\_APPDATA) to store significant amounts of game data and supporting executable files to implement advanced install-on-demand and patching scenarios.</span></span>

<span data-ttu-id="a03c5-584">因為安裝可能需要在所有使用者安裝程式期間提升至不同的使用者帳戶，所以在安裝時不會有正確的使用者位置來儲存資料。</span><span class="sxs-lookup"><span data-stu-id="a03c5-584">Because installation can require elevation to a different user account during the all users installation process, there is no correct user location in which to store data at installation time.</span></span> <span data-ttu-id="a03c5-585">此外，如果已啟用檔案加密，加密的檔案只能由建立它們的使用者帳戶存取。</span><span class="sxs-lookup"><span data-stu-id="a03c5-585">Also, if file encryption is enabled, encrypted files can be only accessed by the user account that created them.</span></span>

</dd> </dl>

### <a name="34-install-windows-resources-properly"></a><span data-ttu-id="a03c5-586">3.4 正確安裝 Windows 資源</span><span class="sxs-lookup"><span data-stu-id="a03c5-586">3.4 Install Windows Resources Properly</span></span>

<dl> <dt>

<span data-ttu-id="a03c5-587"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**要求**</span><span class="sxs-lookup"><span data-stu-id="a03c5-587"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requirement**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-588">應用程式不能嘗試安裝受 Windows 資源保護 (WRP) 保護的檔案或登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="a03c5-588">Applications must not attempt to install files or registry keys that are protected by Windows Resource Protection (WRP).</span></span> <span data-ttu-id="a03c5-589">如果應用程式需要較新版本的系統元件，則必須使用 Microsoft Service Pack 或包含系統元件的 Microsoft 核准安裝套件來更新這些元件。</span><span class="sxs-lookup"><span data-stu-id="a03c5-589">If the application requires newer versions of system components, it must update these components by using a Microsoft Service Pack or a Microsoft-approved installation package that contains the system component.</span></span> <span data-ttu-id="a03c5-590">系統元件絕對不能重新封裝。</span><span class="sxs-lookup"><span data-stu-id="a03c5-590">System components must never be repackaged.</span></span>

</dd> <dt>

<span data-ttu-id="a03c5-591"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**理由**</span><span class="sxs-lookup"><span data-stu-id="a03c5-591"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Rationale**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-592">Windows 資源保護 (WRP) 的設計目的，是要確保只有使用 Microsoft 核准的安裝或更新機制，才能更新受保護的系統資源。</span><span class="sxs-lookup"><span data-stu-id="a03c5-592">Windows Resource Protection (WRP) is designed to ensure that protected system resources are updated only by using Microsoft-approved installation or update mechanisms.</span></span> <span data-ttu-id="a03c5-593">WRP 可確保安裝的結果是可預測的，藉以改善系統可靠性。</span><span class="sxs-lookup"><span data-stu-id="a03c5-593">WRP improves system reliability by ensuring that the results of an installation are predictable.</span></span>

</dd> <dt>

<span data-ttu-id="a03c5-594"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**其他資訊**</span><span class="sxs-lookup"><span data-stu-id="a03c5-594"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Additional Information**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-595">WRP 是 Windows 檔案保護的後續版本，可保護 Windows 資料夾中安裝的大部分系統元件。</span><span class="sxs-lookup"><span data-stu-id="a03c5-595">WRP is the successor to Windows File Protection, which protects the majority of the system components that are installed in the Windows folder.</span></span> <span data-ttu-id="a03c5-596">WRP 可保護大部分儲存 COM 物件建立設定的登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="a03c5-596">WRP protects most registry keys that store settings for COM object creation.</span></span> <span data-ttu-id="a03c5-597">它也會保留特定的資料夾，以供作業系統獨佔使用。</span><span class="sxs-lookup"><span data-stu-id="a03c5-597">It also reserves certain folders for use exclusively by the operating system.</span></span> <span data-ttu-id="a03c5-598">嘗試存取受保護的資源通常會導致存取拒絕錯誤。</span><span class="sxs-lookup"><span data-stu-id="a03c5-598">Attempts to access protected resources typically result in an access denial error.</span></span>

<span data-ttu-id="a03c5-599">如需有關使用遊戲部署 DirectX 執行時間的最佳作法詳細資訊，請參閱 [適用于遊戲開發人員](/windows/desktop/DxTechArts/directx-setup-for-game-developers)的 Directx 文章 directx 安裝。</span><span class="sxs-lookup"><span data-stu-id="a03c5-599">For details of best practices when the DirectX runtime is deployed with a game, see the DirectX article [DirectX Installation for Game Developers](/windows/desktop/DxTechArts/directx-setup-for-game-developers).</span></span>

</dd> </dl>

### <a name="35-avoid-reboots-during-installation"></a><span data-ttu-id="a03c5-600">3.5 避免在安裝期間重新開機</span><span class="sxs-lookup"><span data-stu-id="a03c5-600">3.5 Avoid Reboots During Installation</span></span>

<dl> <dt>

<span data-ttu-id="a03c5-601"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**要求**</span><span class="sxs-lookup"><span data-stu-id="a03c5-601"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requirement**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-602">遊戲安裝程式不應假設重新發佈套件的 Windows 元件安裝需要重新開機，除非重新開機是由傳回結果或 Microsoft 檔所表示。</span><span class="sxs-lookup"><span data-stu-id="a03c5-602">The game installer should not assume that installation of Windows components from redistribution packages requires a reboot, unless the reboot is indicated by a return result or by Microsoft documentation.</span></span>

<span data-ttu-id="a03c5-603">如果遊戲安裝程式一律強制重新開機，則必須由 Microsoft 核准。</span><span class="sxs-lookup"><span data-stu-id="a03c5-603">If the game installer always forces a reboot, this must be approved by Microsoft.</span></span>

<span data-ttu-id="a03c5-604">Windows Installer 套件中包含的 [檔案使用中] 對話方塊，必須包含可自動關閉應用程式，並在安裝程式完成後嘗試重新開機應用程式的選項。</span><span class="sxs-lookup"><span data-stu-id="a03c5-604">Files-in-use dialog boxes that are included in Windows Installer packages must contain an option to automatically close applications and attempt to restart them after setup is complete.</span></span>

</dd> <dt>

<span data-ttu-id="a03c5-605"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**理由**</span><span class="sxs-lookup"><span data-stu-id="a03c5-605"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Rationale**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-606">在安裝之後重新開機系統，對使用者來說是不方便的，而且通常不需要。</span><span class="sxs-lookup"><span data-stu-id="a03c5-606">Rebooting the system after an installation is an inconvenient disruption for users and is usually unnecessary.</span></span>

</dd> <dt>

<span data-ttu-id="a03c5-607"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**其他資訊**</span><span class="sxs-lookup"><span data-stu-id="a03c5-607"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Additional Information**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-608">如需詳細資訊，請參閱搭配 [使用 Windows Installer 與重新開機管理員](/windows/desktop/Msi/using-windows-installer-with-restart-manager)。</span><span class="sxs-lookup"><span data-stu-id="a03c5-608">For more information, see [Using Windows Installer with Restart Manager](/windows/desktop/Msi/using-windows-installer-with-restart-manager).</span></span>

</dd> </dl>

### <a name="36-use-file-versioning-correctly"></a><span data-ttu-id="a03c5-609">3.6 使用正確的檔案版本控制</span><span class="sxs-lookup"><span data-stu-id="a03c5-609">3.6 Use File Versioning Correctly</span></span>

<dl> <dt>

<span data-ttu-id="a03c5-610"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**要求**</span><span class="sxs-lookup"><span data-stu-id="a03c5-610"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requirement**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-611">遊戲安裝程式必須正確檢查，以確定已安裝最新的檔案版本。</span><span class="sxs-lookup"><span data-stu-id="a03c5-611">The game installation program must properly check to ensure that the latest file versions are installed.</span></span> <span data-ttu-id="a03c5-612">安裝遊戲絕不能回歸您不會產生的任何檔案，或是由您未產生的應用程式所共用的檔案。</span><span class="sxs-lookup"><span data-stu-id="a03c5-612">Installing a game must never regress any files that you do not produce or that are shared by applications that you do not produce.</span></span>

</dd> <dt>

<span data-ttu-id="a03c5-613"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**理由**</span><span class="sxs-lookup"><span data-stu-id="a03c5-613"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Rationale**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-614">共用元件和系統元件通常會更新安全性修正和擴充功能。</span><span class="sxs-lookup"><span data-stu-id="a03c5-614">Shared components and system components are often updated for security fixes and expanded functionality.</span></span> <span data-ttu-id="a03c5-615">包含舊版更新元件的安裝應該不會導致遺失已套用的更新和修正程式。</span><span class="sxs-lookup"><span data-stu-id="a03c5-615">An installation that includes an older version of updated components should not result in the loss of updates and fixes that already have been applied.</span></span>

</dd> </dl>

### <a name="37-support-autorun-conditional-requirement"></a><span data-ttu-id="a03c5-616">3.7 支援自動運行 \[ 條件需求\]</span><span class="sxs-lookup"><span data-stu-id="a03c5-616">3.7 Support Autorun \[Conditional Requirement\]</span></span>

<dl> <dt>

<span data-ttu-id="a03c5-617"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**要求**</span><span class="sxs-lookup"><span data-stu-id="a03c5-617"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requirement**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-618">針對在 CD、DVD 或其他支援自動執行的卸載式媒體上散佈的遊戲，第一次插入光碟時，除非使用者已停用自動執行功能，否則應用程式必須自動執行或提示使用者安裝遊戲。</span><span class="sxs-lookup"><span data-stu-id="a03c5-618">For games distributed on CD, DVD, or other removable media that support Autorun, when the disc is inserted for the first time, the application must automatically run or prompt the user to install the game, unless the user has disabled the Autorun feature.</span></span>

<span data-ttu-id="a03c5-619">成功安裝應用程式之後，重新插入磁片磁碟機中的光碟時，不會自動重新開始安裝。</span><span class="sxs-lookup"><span data-stu-id="a03c5-619">After the application is successfully installed, re-inserting the disc in the drive must not cause installation to automatically begin again.</span></span> <span data-ttu-id="a03c5-620">如果使用者想要更新或變更其安裝選項，可以接受要求。</span><span class="sxs-lookup"><span data-stu-id="a03c5-620">It is acceptable to ask users if they want to update or change their installation choices.</span></span>

<span data-ttu-id="a03c5-621">自動運行應用程式不能提示提高許可權 (也就是說，它必須在資訊清單中依需求 2.1 asInvoker，不過它可以啟動安裝程式或其他需要系統管理許可權的公用程式。</span><span class="sxs-lookup"><span data-stu-id="a03c5-621">The autorun application must not prompt for elevation (that is, it must have asInvoker in the manifest, per requirement 2.1, although it can launch the setup program or another utility that requires administrative rights.</span></span> <span data-ttu-id="a03c5-622">只有在未安裝遊戲或使用者明確選取時，才會發生提高許可權。</span><span class="sxs-lookup"><span data-stu-id="a03c5-622">Elevation should occur only if the game is not installed, or if the user specifically selects it.</span></span>

</dd> <dt>

<span data-ttu-id="a03c5-623"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**理由**</span><span class="sxs-lookup"><span data-stu-id="a03c5-623"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Rationale**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-624">自動運行可簡化使用媒體分散式應用程式的體驗，例如通常需要光碟存在於磁片磁碟機才能播放遊戲的遊戲。</span><span class="sxs-lookup"><span data-stu-id="a03c5-624">Autorun simplifies the experience of using media-distributed applications, such as games that typically require the disc to be present in the drive in order to play the game.</span></span>

</dd> <dt>

<span data-ttu-id="a03c5-625"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**其他資訊**</span><span class="sxs-lookup"><span data-stu-id="a03c5-625"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Additional Information**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-626">要求使用者在檔案總管中流覽，以從 CD 或 DVD 開機安裝是不可接受的。</span><span class="sxs-lookup"><span data-stu-id="a03c5-626">It is not acceptable to require the user to navigate in File Explorer to launch the installation from the CD or DVD.</span></span>

<span data-ttu-id="a03c5-627">針對分散在多張光碟上的遊戲，在理想的情況下，最好是使用自動執行功能或繼續安裝，而不提示使用者按下按鍵或採取其他動作。</span><span class="sxs-lookup"><span data-stu-id="a03c5-627">For games that are distributed on multiple discs, subsequent discs should ideally either use the Autorun feature or continue installation without prompting the user to press a key or take other action.</span></span>

<span data-ttu-id="a03c5-628">撰寫自動安裝程式時，請確定 Windows 的全新安裝中有所有必要的元件。</span><span class="sxs-lookup"><span data-stu-id="a03c5-628">When authoring an Autorun program, ensure all required components are present on fresh installs of Windows.</span></span> <span data-ttu-id="a03c5-629">一般的應用程式會依賴安裝程式所安裝的技術，但自動執行本身會在任何這類設定發生之前執行。</span><span class="sxs-lookup"><span data-stu-id="a03c5-629">Typical applications rely on technologies installed by the setup, but Autorun itself executes before any such setup occurs.</span></span> <span data-ttu-id="a03c5-630">其中一個常見的範例就是自動安裝程式失敗，因為 Visual C Runtime Dll 並未包含在 Windows 安裝程式中。</span><span class="sxs-lookup"><span data-stu-id="a03c5-630">One common example is the failure of Autorun programs because the Visual C Runtime DLLs were not included as part of the Windows setup.</span></span> <span data-ttu-id="a03c5-631">因此，自動執行程式必須使用應用程式本機 CRT 部署，或必須以靜態方式連結 CRT。</span><span class="sxs-lookup"><span data-stu-id="a03c5-631">The Autorun program, therefore, must use application local CRT deployment or must statically link the CRT.</span></span>

<span data-ttu-id="a03c5-632">針對 windows Vista 之前的 Windows 版本所撰寫的自動執行程式，不應該使用 .NET 執行時間，因為這項技術並不包含在 Windows XP 或舊版的 Windows 中。</span><span class="sxs-lookup"><span data-stu-id="a03c5-632">Autorun programs written for use on versions of Windows before Windows Vista should not use the .NET runtime because this technology is not included with Windows XP or older versions of Windows.</span></span> <span data-ttu-id="a03c5-633">Windows Server 2003 和 Windows Vista 是 Windows 的第一個版本，可將 .NET 執行時間納入為作業系統的一部分。</span><span class="sxs-lookup"><span data-stu-id="a03c5-633">Windows Server 2003 and Windows Vista are the first versions of Windows to include .NET runtime as part of their operating system.</span></span>

<span data-ttu-id="a03c5-634">基於類似的原因，自動運行程式不需要有 DirectX SDK 選用的並存元件，例如 D3DX9、D3DX10、D3DX11、XAudio2、X3DAudio、交易、XINPUT 和 MDX 1.1。</span><span class="sxs-lookup"><span data-stu-id="a03c5-634">For similar reasons, Autorun programs cannot require the presence of DirectX SDK optional side-by-side components such as D3DX9, D3DX10, D3DX11, XAudio2, X3DAudio, XACT, XINPUT, and MDX 1.1.</span></span>

<span data-ttu-id="a03c5-635">如需使用自動運行的範例，請參閱自動運行範例。</span><span class="sxs-lookup"><span data-stu-id="a03c5-635">For an example of using Autorun, see AutoRun Sample.</span></span>

</dd> </dl>

## <a name="reliability"></a><span data-ttu-id="a03c5-636">可靠性</span><span class="sxs-lookup"><span data-stu-id="a03c5-636">Reliability</span></span>

<span data-ttu-id="a03c5-637">**安全性與相容性需求的摘要**</span><span class="sxs-lookup"><span data-stu-id="a03c5-637">**Summary of Security and Compatibility Requirements**</span></span>

<span data-ttu-id="a03c5-638">**客戶權益**</span><span class="sxs-lookup"><span data-stu-id="a03c5-638">**Customer Benefits**</span></span>

<span data-ttu-id="a03c5-639">這些需求會將損毀、停止回應和重新開機的次數降到最低，讓應用程式更可靠。</span><span class="sxs-lookup"><span data-stu-id="a03c5-639">These requirements make an application more reliable by minimizing the number of crashes, hangs, and reboots.</span></span> <span data-ttu-id="a03c5-640">可靠性需求有助於確保軟體的可預測性、可維護性、彈性和可復原性。</span><span class="sxs-lookup"><span data-stu-id="a03c5-640">The reliability requirements can help ensure that software is more predictable, maintainable, resilient, and recoverable.</span></span>

### <a name="41-eliminate-unnecessary-reboots"></a><span data-ttu-id="a03c5-641">4.1 消除不必要的重新開機</span><span class="sxs-lookup"><span data-stu-id="a03c5-641">4.1 Eliminate Unnecessary Reboots</span></span>

<dl> <dt>

<span data-ttu-id="a03c5-642"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**要求**</span><span class="sxs-lookup"><span data-stu-id="a03c5-642"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requirement**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-643">所有應用程式安裝程式都必須利用重新開機管理員 Api 來避免系統重新開機 (請參閱需求 3.5) 。</span><span class="sxs-lookup"><span data-stu-id="a03c5-643">All application installers must take advantage of the restart manager APIs to avoid system reboots (see requirement 3.5).</span></span>

<span data-ttu-id="a03c5-644">遊戲不得封鎖關機。</span><span class="sxs-lookup"><span data-stu-id="a03c5-644">Games must not block shutdown.</span></span>

<span data-ttu-id="a03c5-645">所有應用程式都必須接聽並回應下列關機訊息，以回應重新開機管理員：</span><span class="sxs-lookup"><span data-stu-id="a03c5-645">All applications must respond to the restart manager by listening and responding to the following shutdown messages:</span></span>

<dl> <dt>

<span data-ttu-id="a03c5-646"><span id="WM_QUERYENDSESSION_with_LPARAM___ENDSESSION_CLOSEAPP__0x1___"></span><span id="wm_queryendsession_with_lparam___endsession_closeapp__0x1___"></span><span id="WM_QUERYENDSESSION_WITH_LPARAM___ENDSESSION_CLOSEAPP__0X1___"></span>\_具有 LPARAM = ENDSESSION \_ CLOSEAPP (0x1) 的 WM QUERYENDSESSION</span><span class="sxs-lookup"><span data-stu-id="a03c5-646"><span id="WM_QUERYENDSESSION_with_LPARAM___ENDSESSION_CLOSEAPP__0x1___"></span><span id="wm_queryendsession_with_lparam___endsession_closeapp__0x1___"></span><span id="WM_QUERYENDSESSION_WITH_LPARAM___ENDSESSION_CLOSEAPP__0X1___"></span>WM\_QUERYENDSESSION with LPARAM = ENDSESSION\_CLOSEAPP (0x1)</span></span> 
</dt> <dd>

<span data-ttu-id="a03c5-647">GUI 應用程式必須在準備重新開機時，立即回應 (TRUE) 。</span><span class="sxs-lookup"><span data-stu-id="a03c5-647">GUI applications must respond (TRUE) immediately in preparation for a restart.</span></span>

</dd> <dt>

<span data-ttu-id="a03c5-648"><span id="WM_ENDSESSION_with_LPARAM___ENDSESSION_CLOSEAPP__0x1___"></span><span id="wm_endsession_with_lparam___endsession_closeapp__0x1___"></span><span id="WM_ENDSESSION_WITH_LPARAM___ENDSESSION_CLOSEAPP__0X1___"></span>\_具有 LPARAM = ENDSESSION \_ CLOSEAPP (0x1) 的 WM ENDSESSION</span><span class="sxs-lookup"><span data-stu-id="a03c5-648"><span id="WM_ENDSESSION_with_LPARAM___ENDSESSION_CLOSEAPP__0x1___"></span><span id="wm_endsession_with_lparam___endsession_closeapp__0x1___"></span><span id="WM_ENDSESSION_WITH_LPARAM___ENDSESSION_CLOSEAPP__0X1___"></span>WM\_ENDSESSION with LPARAM = ENDSESSION\_CLOSEAPP (0x1)</span></span> 
</dt> <dd>

<span data-ttu-id="a03c5-649">應用程式必須在5秒內傳回0值，然後關閉。</span><span class="sxs-lookup"><span data-stu-id="a03c5-649">Applications must return a 0 value within 5 seconds, and then close.</span></span>

</dd> <dt>

<span data-ttu-id="a03c5-650"><span id="CTRL_C__"></span><span id="ctrl_c__"></span>CTRL + C</span><span class="sxs-lookup"><span data-stu-id="a03c5-650"><span id="CTRL_C__"></span><span id="ctrl_c__"></span>CTRL+C</span></span> 
</dt> <dd>

<span data-ttu-id="a03c5-651">接收此訊息的主控台應用程式必須立即關閉。</span><span class="sxs-lookup"><span data-stu-id="a03c5-651">Console applications that receive this message must close immediately.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="a03c5-652"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**理由**</span><span class="sxs-lookup"><span data-stu-id="a03c5-652"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Rationale**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-653">系統重新開機是嚴重的中斷。</span><span class="sxs-lookup"><span data-stu-id="a03c5-653">System reboots are a major disruption.</span></span> <span data-ttu-id="a03c5-654">他們會導致使用者體驗不佳，而且應該將其最小化。</span><span class="sxs-lookup"><span data-stu-id="a03c5-654">They lead to a bad user experience, and should be minimized.</span></span> <span data-ttu-id="a03c5-655">某些作業（例如重要的系統更新）可能需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="a03c5-655">Some operations, such as critical system updates can require reboots.</span></span> <span data-ttu-id="a03c5-656">藉由聆聽關機訊息，遊戲和其他應用程式可以立即回應重新開機管理員的要求。</span><span class="sxs-lookup"><span data-stu-id="a03c5-656">By listening to shutdown messages, the game and other applications can react promptly to requests from restart manager.</span></span> <span data-ttu-id="a03c5-657">如此一來，即可避免在有效的重新開機要求中發生不必要的延遲。</span><span class="sxs-lookup"><span data-stu-id="a03c5-657">In this way, they can avoid unnecessarily delays in valid reboot requests.</span></span>

</dd> <dt>

<span data-ttu-id="a03c5-658"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**其他資訊**</span><span class="sxs-lookup"><span data-stu-id="a03c5-658"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Additional Information**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-659">如果遊戲安裝程式在沒有任何自訂動作的情況下使用 Windows Installer 技術 (MSI) ，則會自動提供這項功能。</span><span class="sxs-lookup"><span data-stu-id="a03c5-659">If a game installer uses the Windows Installer technology (MSI) without any custom actions, this functionality is provided automatically.</span></span> <span data-ttu-id="a03c5-660">Microsoft 轉散發套件也支援重新開機管理員。</span><span class="sxs-lookup"><span data-stu-id="a03c5-660">Microsoft redistribution packages also support the Restart Manager.</span></span>

<span data-ttu-id="a03c5-661">如需重新開機管理員的詳細資訊，請參閱 MSDN 文章中的 [重新開機管理員](/windows/desktop/RstMgr/about-restart-manager)。</span><span class="sxs-lookup"><span data-stu-id="a03c5-661">For more information about the Restart Manager, see the MSDN article [About Restart Manager](/windows/desktop/RstMgr/about-restart-manager).</span></span>

</dd> </dl>

### <a name="42-eliminate-application-verifier-failures"></a><span data-ttu-id="a03c5-662">4.2 消除應用程式驗證器失敗</span><span class="sxs-lookup"><span data-stu-id="a03c5-662">4.2 Eliminate Application Verifier Failures</span></span>

<dl> <dt>

<span data-ttu-id="a03c5-663"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**要求**</span><span class="sxs-lookup"><span data-stu-id="a03c5-663"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requirement**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-664">在下列測試中，遊戲必須不會在 Microsoft 應用程式驗證器 (AppVerifier) 4.0 版或更新版本下產生任何失敗：</span><span class="sxs-lookup"><span data-stu-id="a03c5-664">The game must generate no failures running under Microsoft Application Verifier (AppVerifier), version 4.0 or later, in the following tests:</span></span>

-   <span data-ttu-id="a03c5-665">基本概念：控制碼、堆積、鎖定、記憶體、TLS</span><span class="sxs-lookup"><span data-stu-id="a03c5-665">Basics: Handles, Heaps, Locks, Memory, TLS</span></span>
-   <span data-ttu-id="a03c5-666">其他： DangerousAPIs、DirtyStacks</span><span class="sxs-lookup"><span data-stu-id="a03c5-666">Miscellaneous: DangerousAPIs, DirtyStacks</span></span>

</dd> <dt>

<span data-ttu-id="a03c5-667"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**理由**</span><span class="sxs-lookup"><span data-stu-id="a03c5-667"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Rationale**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-668">AppVerifier 會測試許多在 Windows 應用程式中造成當機和停止回應的已知問題，以及已知的安全性弱點。</span><span class="sxs-lookup"><span data-stu-id="a03c5-668">AppVerifier tests for many known issues that cause crashes and hangs in Windows applications, as well as known security vulnerabilities.</span></span>

</dd> <dt>

<span data-ttu-id="a03c5-669"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**其他資訊**</span><span class="sxs-lookup"><span data-stu-id="a03c5-669"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Additional Information**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-670">如需應用程式驗證器的詳細資訊，請參閱 MSDN 上的 [應用程式驗證器](/previous-versions/ms220948(v=vs.80)) 和 [使用軟體發展生命週期中的應用程式驗證器](/previous-versions/aa480483(v=msdn.10)) 。</span><span class="sxs-lookup"><span data-stu-id="a03c5-670">For more information about Application Verifier, see [Application Verifier](/previous-versions/ms220948(v=vs.80)) and [Using Application Verifier Within Your Software Development Lifecycle](/previous-versions/aa480483(v=msdn.10)) on MSDN.</span></span> <span data-ttu-id="a03c5-671">您可以從 [下載詳細資料](https://www.microsoft.com/downloads/details.aspx?familyid=c4a25ab9-649d-4a1b-b4a7-c9d8b095df18) 下載應用程式驗證器： Microsoft 下載中心上的應用程式驗證器。</span><span class="sxs-lookup"><span data-stu-id="a03c5-671">You can download Application Verifier from [Download details: Application Verifier](https://www.microsoft.com/downloads/details.aspx?familyid=c4a25ab9-649d-4a1b-b4a7-c9d8b095df18) on Microsoft Download Center.</span></span>

<span data-ttu-id="a03c5-672">這項需求不適用於沒有原生 interop 的純受控應用程式。</span><span class="sxs-lookup"><span data-stu-id="a03c5-672">This requirement does not apply to pure managed applications without native interop.</span></span>

<span data-ttu-id="a03c5-673">這些測試應該在發行組建上執行。</span><span class="sxs-lookup"><span data-stu-id="a03c5-673">These tests should be run on a release build.</span></span> <span data-ttu-id="a03c5-674">調試組建可能會產生錯誤的錯誤。</span><span class="sxs-lookup"><span data-stu-id="a03c5-674">Debugging builds can generate false failures.</span></span> <span data-ttu-id="a03c5-675">某些反盜版和反相關的技術可能會干擾 AppVerifier 的執行。</span><span class="sxs-lookup"><span data-stu-id="a03c5-675">Some anti-piracy and anti-cheat technologies can interfere with the execution of AppVerifier.</span></span> <span data-ttu-id="a03c5-676">因此，您應該執行這些測試，而不會啟用反盜版和防功能的技術。</span><span class="sxs-lookup"><span data-stu-id="a03c5-676">Therefore, these tests should be performed without anti-piracy and anti-cheat technologies enabled.</span></span>

<span data-ttu-id="a03c5-677">您可能必須將基本概念：堆積測試的完整屬性設為 FALSE，因為完整 PageHeap 會大幅增加執行中應用程式的記憶體壓力。</span><span class="sxs-lookup"><span data-stu-id="a03c5-677">It may be necessary to set the Full property of the Basics:Heaps test to FALSE, because the full PageHeap greatly increases the memory pressure of the running application.</span></span> <span data-ttu-id="a03c5-678">仍會偵測到失敗，但如果您只使用部分 PageHeap，可能會比較難追蹤。</span><span class="sxs-lookup"><span data-stu-id="a03c5-678">Failures will still be detected, but they might be more difficult to track down if you use only partial PageHeap.</span></span>

<span data-ttu-id="a03c5-679">如果您在應用程式驗證器中使用 UAC/LUA 相關的測試以符合使用者帳戶控制需求2.1 和3.2，您應該使用 [標準使用者分析器](/windows/desktop/Win7AppQual/standard-user-analyzer--sua--tool-and-standard-user-analyzer-wizard--sua-wizard-) 來檢查結果。</span><span class="sxs-lookup"><span data-stu-id="a03c5-679">If you use the UAC/LUA-related tests in Application Verifier to meet the User Account Control requirements 2.1 and 3.2, you should use the [Standard User Analyzer](/windows/desktop/Win7AppQual/standard-user-analyzer--sua--tool-and-standard-user-analyzer-wizard--sua-wizard-) to review the results.</span></span> <span data-ttu-id="a03c5-680">此外，也有許多其他有用的測試，這些測試是由您強烈建議用於開發和測試的應用程式驗證器，以確保與目前和未來版本的 Windows 相容。</span><span class="sxs-lookup"><span data-stu-id="a03c5-680">There are also numerous other useful tests provided by Application Verifier which you are strongly encouraged to use in development and testing to ensure a high level of compatibility with current and future versions of Windows.</span></span> <span data-ttu-id="a03c5-681">**HighVersionLie** 測試用來確認符合需求2.5 的合規性。</span><span class="sxs-lookup"><span data-stu-id="a03c5-681">The **HighVersionLie** test is used to verify compliance with requirement 2.5.</span></span>

<span data-ttu-id="a03c5-682">Visual Studio Team System 包含已整合至偵錯工具環境的 AppVerifier 功能子集。</span><span class="sxs-lookup"><span data-stu-id="a03c5-682">Visual Studio Team System includes a subset of the AppVerifier functionality that is integrated into the debugging environment.</span></span> <span data-ttu-id="a03c5-683">這可能有助於追蹤和解決基本概念的問題：堆積、控制碼和鎖定測試。</span><span class="sxs-lookup"><span data-stu-id="a03c5-683">This may prove useful for tracking down and resolving issues with Basics: Heaps, Handles, and Locks tests.</span></span>

</dd> </dl>

### <a name="43-support-windows-error-reporting-and-file-version-information"></a><span data-ttu-id="a03c5-684">4.3 支援 Windows 錯誤報告和檔案版本資訊</span><span class="sxs-lookup"><span data-stu-id="a03c5-684">4.3 Support Windows Error Reporting and File Version Information</span></span>

<dl> <dt>

<span data-ttu-id="a03c5-685"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**要求**</span><span class="sxs-lookup"><span data-stu-id="a03c5-685"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requirement**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-686">若要啟用 Windows 錯誤報告支援，遊戲必須符合下列需求：</span><span class="sxs-lookup"><span data-stu-id="a03c5-686">To enable support of Windows Error Reporting, games must meet the following requirements:</span></span>

-   <span data-ttu-id="a03c5-687">遊戲必須只處理已知和預期的例外狀況。</span><span class="sxs-lookup"><span data-stu-id="a03c5-687">Games must handle only exceptions that are known and expected.</span></span> <span data-ttu-id="a03c5-688">Windows 錯誤報告不得停用。</span><span class="sxs-lookup"><span data-stu-id="a03c5-688">Windows Error Reporting must not be disabled.</span></span> <span data-ttu-id="a03c5-689">如果遊戲中出現錯誤（例如存取違規），則必須允許 Windows 錯誤報告報告損毀。</span><span class="sxs-lookup"><span data-stu-id="a03c5-689">If a fault such as an Access Violation appears in a game, it must allow Windows Error Reporting to report the crash.</span></span>
-   <span data-ttu-id="a03c5-690">所有可執行檔 (例如，.exe 檔案或 Dll) 都必須包含正確的產品名稱、公司名稱和檔案版本。</span><span class="sxs-lookup"><span data-stu-id="a03c5-690">All executable files (for example, .exe files or DLLs) must contain an accurate product name, company name, and file version.</span></span>
-   <span data-ttu-id="a03c5-691">正常結束遊戲時，不能造成不明的例外狀況錯誤。</span><span class="sxs-lookup"><span data-stu-id="a03c5-691">Normal exit of the game must not result in an unknown exception fault.</span></span>

</dd> <dt>

<span data-ttu-id="a03c5-692"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**理由**</span><span class="sxs-lookup"><span data-stu-id="a03c5-692"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Rationale**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-693">Windows 錯誤報告 Api 提供對 Microsoft 的重要意見反應，以偵測應用程式中的廣泛當機和停止回應。</span><span class="sxs-lookup"><span data-stu-id="a03c5-693">The Windows Error Reporting APIs provide vital feedback to Microsoft for detecting widespread crashes and hangs in applications.</span></span> <span data-ttu-id="a03c5-694">這可讓 Microsoft 及其合作夥伴快速偵測並解決導致應用程式失敗的系統和驅動程式問題。</span><span class="sxs-lookup"><span data-stu-id="a03c5-694">This allows Microsoft and its partners to quickly detect and resolve system and driver issues that lead to application failures quickly.</span></span>

</dd> <dt>

<span data-ttu-id="a03c5-695"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**其他資訊**</span><span class="sxs-lookup"><span data-stu-id="a03c5-695"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Additional Information**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-696">遊戲可以包含自訂的未處理例外狀況處理常式，以執行自訂支援和報告功能，但必須將任何錯誤傳遞至 **ReportFault** 或 **WerReportSubmit** 函數。</span><span class="sxs-lookup"><span data-stu-id="a03c5-696">Games can include custom unhandled exception handlers to perform custom support and reporting functionality, but they must pass any error on to the **ReportFault** or **WerReportSubmit** functions.</span></span>

<span data-ttu-id="a03c5-697">您可以在 Windows 桌面 UI 中查看檔案屬性，並檢查 [版本] 屬性頁，以驗證適當的檔案版本資訊。</span><span class="sxs-lookup"><span data-stu-id="a03c5-697">Proper file version information can be verified by viewing the file properties in the Windows desktop UI and checking the Version property page.</span></span>

<span data-ttu-id="a03c5-698">如需有關 Windows 錯誤報告 Api 的詳細資訊，以及如何分析當您使用此服務時所產生的損毀傾印，請參閱 DirectX 文章損毀傾印 [分析](/windows/desktop/DxTechArts/crash-dump-analysis)。</span><span class="sxs-lookup"><span data-stu-id="a03c5-698">For more information about the Windows Error Reporting APIs, and how to analyze the crash dumps that are generated when you use this service, see the DirectX article [Crash Dump Analysis](/windows/desktop/DxTechArts/crash-dump-analysis).</span></span>

</dd> </dl>

## <a name="xbox-360-common-controller-for-windows-terminology"></a><span data-ttu-id="a03c5-699">適用于 Windows 的通用控制器 Xbox 360 術語</span><span class="sxs-lookup"><span data-stu-id="a03c5-699">Xbox 360 Common Controller for Windows Terminology</span></span>



|                                          |                                                                                                  |
|------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a03c5-700">A</span><span class="sxs-lookup"><span data-stu-id="a03c5-700">A</span></span>                                        | <span data-ttu-id="a03c5-701">按鈕</span><span class="sxs-lookup"><span data-stu-id="a03c5-701">The A button</span></span>                                                                                     |
| <span data-ttu-id="a03c5-702">B</span><span class="sxs-lookup"><span data-stu-id="a03c5-702">B</span></span>                                        | <span data-ttu-id="a03c5-703">B 按鈕</span><span class="sxs-lookup"><span data-stu-id="a03c5-703">The B button</span></span>                                                                                     |
| <span data-ttu-id="a03c5-704">返回</span><span class="sxs-lookup"><span data-stu-id="a03c5-704">BACK</span></span>                                     | <span data-ttu-id="a03c5-705">[上一頁] 按鈕</span><span class="sxs-lookup"><span data-stu-id="a03c5-705">The Back button</span></span>                                                                                  |
| <span data-ttu-id="a03c5-706"> (右/左) 的緩衝器</span><span class="sxs-lookup"><span data-stu-id="a03c5-706">(right/left) bumper</span></span>                      | <span data-ttu-id="a03c5-707">位於控制器右上方和左邊緣的按鈕。</span><span class="sxs-lookup"><span data-stu-id="a03c5-707">The button at the top right and left edge of the controller.</span></span> <span data-ttu-id="a03c5-708">相當於肩按鈕。</span><span class="sxs-lookup"><span data-stu-id="a03c5-708">Equivalent to a shoulder button.</span></span>    |
| <span data-ttu-id="a03c5-709">方向板</span><span class="sxs-lookup"><span data-stu-id="a03c5-709">directional pad</span></span>                          | <span data-ttu-id="a03c5-710">控制器方向面板</span><span class="sxs-lookup"><span data-stu-id="a03c5-710">The controller directional pad</span></span>                                                                   |
| <span data-ttu-id="a03c5-711">D-pad</span><span class="sxs-lookup"><span data-stu-id="a03c5-711">D-pad</span></span>                                    | <span data-ttu-id="a03c5-712">已接受的方向板縮寫</span><span class="sxs-lookup"><span data-stu-id="a03c5-712">Accepted abbreviation of directional pad</span></span>                                                         |
| <span data-ttu-id="a03c5-713">DP</span><span class="sxs-lookup"><span data-stu-id="a03c5-713">DP</span></span>                                       | <span data-ttu-id="a03c5-714">方向板縮寫和控制器標籤</span><span class="sxs-lookup"><span data-stu-id="a03c5-714">Directional pad abbreviation and controller label</span></span>                                                |
| <span data-ttu-id="a03c5-715">RB、LB</span><span class="sxs-lookup"><span data-stu-id="a03c5-715">RB, LB</span></span>                                   | <span data-ttu-id="a03c5-716">右與左的緩衝器縮寫和控制器標籤</span><span class="sxs-lookup"><span data-stu-id="a03c5-716">Right and left bumper abbreviations and controller labels</span></span>                                        |
| <span data-ttu-id="a03c5-717">RS、LS</span><span class="sxs-lookup"><span data-stu-id="a03c5-717">RS, LS</span></span>                                   | <span data-ttu-id="a03c5-718">靠右和向左的縮寫和控制器標籤</span><span class="sxs-lookup"><span data-stu-id="a03c5-718">Right and left stick abbreviations and controller labels</span></span>                                         |
| <span data-ttu-id="a03c5-719">RT、LT</span><span class="sxs-lookup"><span data-stu-id="a03c5-719">RT, LT</span></span>                                   | <span data-ttu-id="a03c5-720">右邊和左方觸發程式縮寫和控制器標籤</span><span class="sxs-lookup"><span data-stu-id="a03c5-720">Right and left trigger abbreviations and controller labels</span></span>                                       |
| <span data-ttu-id="a03c5-721">RSB、LSB</span><span class="sxs-lookup"><span data-stu-id="a03c5-721">RSB, LSB</span></span>                                 | <span data-ttu-id="a03c5-722">靠右和向左的縮寫和控制器標籤</span><span class="sxs-lookup"><span data-stu-id="a03c5-722">Right and left stick abbreviations and controller labels</span></span>                                         |
| <span data-ttu-id="a03c5-723">START</span><span class="sxs-lookup"><span data-stu-id="a03c5-723">START</span></span>                                    | <span data-ttu-id="a03c5-724">[啟動] 按鈕</span><span class="sxs-lookup"><span data-stu-id="a03c5-724">The Start button</span></span>                                                                                 |
| <span data-ttu-id="a03c5-725"> (右/左) 杆</span><span class="sxs-lookup"><span data-stu-id="a03c5-725">(right/left) stick</span></span>                       | <span data-ttu-id="a03c5-726">控制器杆。</span><span class="sxs-lookup"><span data-stu-id="a03c5-726">The controller stick.</span></span> <span data-ttu-id="a03c5-727">先前為操縱杆。</span><span class="sxs-lookup"><span data-stu-id="a03c5-727">Formerly thumbstick.</span></span>                                                       |
| <span data-ttu-id="a03c5-728"> (右/左) 駕駛按鈕</span><span class="sxs-lookup"><span data-stu-id="a03c5-728">(right/left) stick button</span></span>                | <span data-ttu-id="a03c5-729">控制器杆按鈕。</span><span class="sxs-lookup"><span data-stu-id="a03c5-729">The controller stick button.</span></span> <span data-ttu-id="a03c5-730">先前為操縱杆按鈕。</span><span class="sxs-lookup"><span data-stu-id="a03c5-730">Formerly thumbstick button.</span></span>                                         |
| <span data-ttu-id="a03c5-731"> (右/左) 觸發程式</span><span class="sxs-lookup"><span data-stu-id="a03c5-731">(right/left) trigger</span></span>                     | <span data-ttu-id="a03c5-732">控制器觸發程式。</span><span class="sxs-lookup"><span data-stu-id="a03c5-732">The controller trigger.</span></span>                                                                          |
| <span data-ttu-id="a03c5-733">震動</span><span class="sxs-lookup"><span data-stu-id="a03c5-733">Vibration</span></span>                                | <span data-ttu-id="a03c5-734">遊戲控制器馬達產生的意見反應。</span><span class="sxs-lookup"><span data-stu-id="a03c5-734">Gameplay feedback produced by the controller motor.</span></span> <span data-ttu-id="a03c5-735">請勿使用 rumble。</span><span class="sxs-lookup"><span data-stu-id="a03c5-735">Do not use rumble.</span></span>                           |
| <span data-ttu-id="a03c5-736">X</span><span class="sxs-lookup"><span data-stu-id="a03c5-736">X</span></span>                                        | <span data-ttu-id="a03c5-737">X 按鈕</span><span class="sxs-lookup"><span data-stu-id="a03c5-737">The X button</span></span>                                                                                     |
| <span data-ttu-id="a03c5-738">Y</span><span class="sxs-lookup"><span data-stu-id="a03c5-738">Y</span></span>                                        | <span data-ttu-id="a03c5-739">Y 按鈕</span><span class="sxs-lookup"><span data-stu-id="a03c5-739">The Y button</span></span>                                                                                     |
| <span data-ttu-id="a03c5-740">適用于 Windows 的 Xbox 360 控制器</span><span class="sxs-lookup"><span data-stu-id="a03c5-740">Xbox 360 Controller for Windows</span></span>          | <span data-ttu-id="a03c5-741">Xbox 360 的遊戲台銷售為電腦硬體 SKU，包括 Windows 設備磁碟機光碟。</span><span class="sxs-lookup"><span data-stu-id="a03c5-741">The Xbox 360 gamepad sold as a PC hardware SKU, including a Windows device driver disc.</span></span>          |
| <span data-ttu-id="a03c5-742">適用于 Windows 的 Xbox 360 無線控制器</span><span class="sxs-lookup"><span data-stu-id="a03c5-742">Xbox 360 Wireless Controller for Windows</span></span> | <span data-ttu-id="a03c5-743">Xbox 360 的無線遊戲台銷售為電腦硬體 SKU，包括 Windows 設備磁碟機光碟。</span><span class="sxs-lookup"><span data-stu-id="a03c5-743">The Xbox 360 wireless gamepad sold as a PC hardware SKU, including a Windows device driver disc.</span></span> |



 

## <a name="guidelines-for-game-middleware-products"></a><span data-ttu-id="a03c5-744">遊戲中介軟體產品的指導方針</span><span class="sxs-lookup"><span data-stu-id="a03c5-744">Guidelines for Game Middleware Products</span></span>

### <a name="introduction"></a><span data-ttu-id="a03c5-745">簡介</span><span class="sxs-lookup"><span data-stu-id="a03c5-745">Introduction</span></span>

<span data-ttu-id="a03c5-746">針對 Windows 方案適用的遊戲，遊戲必須符合技術需求清單。</span><span class="sxs-lookup"><span data-stu-id="a03c5-746">For games to qualify for the Games for Windows program, they must meet a list of technical requirements.</span></span> <span data-ttu-id="a03c5-747">任何隨附于標題 (可執行檔、Dll、驅動程式等的協力廠商元件，) 也必須符合這些需求，才能讓遊戲符合資格。</span><span class="sxs-lookup"><span data-stu-id="a03c5-747">Any third-party components that are shipped with a title (executable files, DLLs, drivers, and so forth) must also meet these requirements for the game to qualify.</span></span> <span data-ttu-id="a03c5-748">本檔著重于協力廠商元件必須符合的最常見需求，讓遊戲通過合規性測試。</span><span class="sxs-lookup"><span data-stu-id="a03c5-748">This document highlights the most common requirements that must also be met by the third-party components for the game to pass the compliance tests.</span></span> <span data-ttu-id="a03c5-749">安裝程式和完整的遊戲引擎/生產套件應該回顧 Windows 技術需求檔的完整遊戲，因為這些工具當中有許多需求受到影響。</span><span class="sxs-lookup"><span data-stu-id="a03c5-749">Installers and complete game engine/production packages should review the full Games for Windows technical requirements document, because many of these requirements are affected by these tools.</span></span>

### <a name="additional-recommendations"></a><span data-ttu-id="a03c5-750">其他建議</span><span class="sxs-lookup"><span data-stu-id="a03c5-750">Additional Recommendations</span></span>

<span data-ttu-id="a03c5-751">除了確保您的元件支援建立符合 Windows 遊戲需求的標題，在設計和部署 Windows 遊戲的程式庫或支援公用程式時，還有一些其他考慮需要考慮。</span><span class="sxs-lookup"><span data-stu-id="a03c5-751">Beyond ensuring that your component supports the creation of titles that are compliant with the requirements for Games for Windows, there are a number of other considerations you should take into account when designing and deploying a library or support utility for a Windows game.</span></span>

-   <span data-ttu-id="a03c5-752">為了支援使用64位原生 x64 應用程式的開發人員，請提供您程式庫的32位和64位原生版本。</span><span class="sxs-lookup"><span data-stu-id="a03c5-752">To support developers working on 64-bit native x64 applications, provide both 32-bit and 64-bit native versions of your libraries.</span></span> <span data-ttu-id="a03c5-753">32位版本必須是每 2.2 64 位相容的版本。</span><span class="sxs-lookup"><span data-stu-id="a03c5-753">The 32-bit version must be 64-bit compatible per 2.2.</span></span> <span data-ttu-id="a03c5-754">32位應用程式的程式庫不應假設沒有任何32位位址的高位可支援在 LARGEADDRESSAWARE x86 應用程式內使用。</span><span class="sxs-lookup"><span data-stu-id="a03c5-754">Libraries for 32-bit applications should not assume that the high bit of any 32-bit address is unused in order to support use within LARGEADDRESSAWARE x86 applications.</span></span>
-   <span data-ttu-id="a03c5-755">如果您提供原生程式碼 (C/c + +) 標頭，請使用標準注釋語言 (SAL) 屬性語法來裝飾您的公用 API 常式。</span><span class="sxs-lookup"><span data-stu-id="a03c5-755">If you provide native code (C/C++) headers, use Standard Annotation Language (SAL) attribute syntax to decorate your public API routines.</span></span> <span data-ttu-id="a03c5-756">這可讓您文件庫的使用者獲得使用靜態程式碼分析的最大效益 (/analyze) ，此是 Visual Studio Team System 2005、Visual Studio Team System 2008、Visual Studio 2010 Premium 和 Visual Studio 2010 旗艦版，以及公開可用的 Windows SDK 編譯器工具的一部分。</span><span class="sxs-lookup"><span data-stu-id="a03c5-756">This will allow users of your library to get the maximum benefit of using Static Code Analysis (/analyze), which is part of Visual Studio Team System 2005, Visual Studio Team System 2008, Visual Studio 2010 Premium, and Visual Studio 2010 Ultimate, as well as the publicly available Windows SDK compiler tools.</span></span>
-   <span data-ttu-id="a03c5-757">如果您的產品在使用者進程中建立執行緒，請務必將每個執行緒命名為，讓偵錯工具能夠適當地批註執行中的執行緒。</span><span class="sxs-lookup"><span data-stu-id="a03c5-757">If your product creates threads within the user's process, be sure to name each thread so that debugging tools can properly annotate running threads.</span></span>
-   <span data-ttu-id="a03c5-758">如果您撰寫的常式是要在遊戲的主要迴圈內呼叫，請使用 D3DX 常式 D3DPERF \_ BeginEvent/EndEvent 和 D3DPERF \_ SetMarker 來標注高階作業，以便使用適用于 WINDOWS 的 PIX 來更輕鬆地識別瓶頸。</span><span class="sxs-lookup"><span data-stu-id="a03c5-758">If you write routines that are intended to be called within a game's main loop, use the D3DX routines D3DPERF\_BeginEvent/EndEvent and D3DPERF\_SetMarker to annotate high-level operations for easier identification of bottlenecks using PIX for Windows.</span></span>
    > [!Note]  
    > <span data-ttu-id="a03c5-759">針對 Visual Studio 2012 圖形診斷功能，這些 D3DX 和 PIX 常式會由 [**ID3DUserDefinedAnnotation**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3duserdefinedannotation) 介面取代。</span><span class="sxs-lookup"><span data-stu-id="a03c5-759">For the Visual Studio 2012 graphics diagnostics functionality, these D3DX and PIX routines are replaced by the [**ID3DUserDefinedAnnotation**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3duserdefinedannotation) interface.</span></span>

     

-   <span data-ttu-id="a03c5-760">針對網路程式庫，請提供 IP 中立的執行，並避免已淘汰的僅限 IPv4 常式，以支援 Windows XP Service Pack 2、Windows Vista 和 Windows 7 中的 IPv6 和 Teredo 技術。</span><span class="sxs-lookup"><span data-stu-id="a03c5-760">For networking libraries, provide IP-neutral implementations and avoid deprecated IPv4 only routines to support the IPv6 and Teredo technologies in Windows XP with Service Pack 2, Windows Vista, and Windows 7.</span></span>
-   <span data-ttu-id="a03c5-761">遊戲服務提供者應該使用第2版的 GDF 架構向遊戲瀏覽器註冊，並使用 RSS 功能提供與服務相關的新聞。</span><span class="sxs-lookup"><span data-stu-id="a03c5-761">Game service providers should register themselves with Games Explorer using version 2 of the GDF schema, and make use of the RSS feature to provide service-related news.</span></span>

### <a name="games-for-windows-showcases"></a><span data-ttu-id="a03c5-762">Windows 遊戲展示</span><span class="sxs-lookup"><span data-stu-id="a03c5-762">Games for Windows Showcases</span></span>

### <a name="introduction"></a><span data-ttu-id="a03c5-763">簡介</span><span class="sxs-lookup"><span data-stu-id="a03c5-763">Introduction</span></span>

<span data-ttu-id="a03c5-764">Windows 展示的遊戲超越了在 Windows 電腦上提供穩固的遊戲體驗。</span><span class="sxs-lookup"><span data-stu-id="a03c5-764">Games for Windows showcases go beyond providing a solid gaming experience on Windows PCs.</span></span> <span data-ttu-id="a03c5-765">藉由實行這些功能，遊戲可為最新 Windows 平臺上的使用者體驗增加更多驚喜。</span><span class="sxs-lookup"><span data-stu-id="a03c5-765">By implementing these features, games can add more excitement to the user experience on the latest Windows platforms.</span></span>

<span data-ttu-id="a03c5-766">Windows 標題的遊戲必須符合本文所列的所有技術需求，但是展示功能是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="a03c5-766">Games for Windows titles must fulfill all technical requirements listed in this article, but showcase features are optional.</span></span> <span data-ttu-id="a03c5-767">這些標題可自由地實行一些、無或所有展示。</span><span class="sxs-lookup"><span data-stu-id="a03c5-767">These titles are free to implement some, none, or all of these showcases.</span></span>

### <a name="s1-exploit-direct3d-11"></a><span data-ttu-id="a03c5-768">S 1 惡意探索 Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="a03c5-768">S.1 Exploit Direct3D 11</span></span>

<dl> <dt>

<span data-ttu-id="a03c5-769"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**要求**</span><span class="sxs-lookup"><span data-stu-id="a03c5-769"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requirement**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-770">Direct3D 11 是適用于 Windows Vista 和 Windows 7 的新一代轉譯 API。</span><span class="sxs-lookup"><span data-stu-id="a03c5-770">Direct3D 11 is the next-generation rendering API for Windows Vista and Windows 7.</span></span> <span data-ttu-id="a03c5-771">利用 Direct3D 11 的遊戲使用優化的內容、先進的轉譯技巧，以及新的硬體功能，在支援10、10.1 和11的硬體上建立引人注目的體驗。</span><span class="sxs-lookup"><span data-stu-id="a03c5-771">Games exploiting Direct3D 11 use optimized content, advanced rendering techniques, and new hardware features to create a compelling experience on hardware that supports 10, 10.1, and 11.</span></span>

<span data-ttu-id="a03c5-772">如果遊戲也實行 Direct3D 9，並存的比較應該會針對 Direct3D 11 的內容品質、視覺精確度、效能、場景複雜性和其他區域圖形精確度，示範可察覺的改進。</span><span class="sxs-lookup"><span data-stu-id="a03c5-772">If the game also implements Direct3D 9, a side-by-side comparison should demonstrate a perceptible improvement in content quality, visual fidelity, performance, scene complexity, and other areas of graphics fidelity for Direct3D 11.</span></span> <span data-ttu-id="a03c5-773">這項支援受限於 Windows 技術需求1.7 的遊戲。</span><span class="sxs-lookup"><span data-stu-id="a03c5-773">This support is subject to the Games for Windows Technical Requirement 1.7.</span></span>

<span data-ttu-id="a03c5-774">Direct3D 10level9 技術可以用來支援 Windows Vista 和 Windows 7 上的著色器模型 2.0/3.0 Direct3D 9 類別的影片硬體，而不是使用並存的 Direct3D 9 實作為廣泛的硬體支援。</span><span class="sxs-lookup"><span data-stu-id="a03c5-774">Direct3D 10level9 technology can be used to support Shader Model 2.0/3.0 Direct3D 9-class video hardware on Windows Vista and Windows 7, rather than using a side-by-side Direct3D 9 implementation for broad hardware support.</span></span> <span data-ttu-id="a03c5-775">不過，這並不足以示範此展示。</span><span class="sxs-lookup"><span data-stu-id="a03c5-775">However, this is not sufficient to demonstrate this showcase.</span></span>

<span data-ttu-id="a03c5-776">在執行 Windows Vista 或已安裝 Direct3D 11 的 Windows 7 的電腦上，遊戲應該預設為使用 Direct3D 11。</span><span class="sxs-lookup"><span data-stu-id="a03c5-776">On computers running Windows Vista or Windows 7 with Direct3D 11 installed, the game should default to using Direct3D 11.</span></span>

</dd> <dt>

<span data-ttu-id="a03c5-777"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**理由**</span><span class="sxs-lookup"><span data-stu-id="a03c5-777"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Rationale**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-778">Direct3D 11 API 建基於 Windows 顯示驅動程式模型 (WDDM) 和 Direct3D 10.1 基礎結構，以支援新的功能：硬體鑲嵌、計算著色器、多執行緒轉譯和資源建立、新的材質壓縮格式，以及更有彈性的著色器語言。</span><span class="sxs-lookup"><span data-stu-id="a03c5-778">The Direct3D 11 API builds on the Windows Display Driver Model (WDDM) and Direct3D 10.1 infrastructure to support new capabilities: hardware tessellation, compute shaders, multithreaded rendering and resource creation, new texture compression formats, and a more flexible shader language.</span></span> <span data-ttu-id="a03c5-779">Direct3D 11 提供新式視訊卡的統一硬體支援，包括最新一代的 Direct3D 11 元件、所有 Direct3D 10 和10.1 視訊卡，以及許多著色器模型 2.0/3.0 Direct3D 9 視訊卡，也就是 Aero 3D 桌面所需的最小影片硬體。</span><span class="sxs-lookup"><span data-stu-id="a03c5-779">Direct3D 11 provides unified hardware support for modern video cards, including the latest generation Direct3D 11 parts, all Direct3D 10 and 10.1 video cards, and many Shader Model 2.0/3.0 Direct3D 9 video cards, which is the minimum video hardware required for the Aero 3D desktop.</span></span>

</dd> <dt>

<span data-ttu-id="a03c5-780"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**其他資訊**</span><span class="sxs-lookup"><span data-stu-id="a03c5-780"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Additional Information**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-781">遷移 Direct3D 9 轉譯引擎以使用新的 Direct3D 11 介面是一項妥善定義的工作：</span><span class="sxs-lookup"><span data-stu-id="a03c5-781">Migrating a Direct3D 9 rendering engine to use the new Direct3D 11 interface is a well-defined task:</span></span>

-   <span data-ttu-id="a03c5-782">消除所有固定函式的作業，以改用可程式化著色器。</span><span class="sxs-lookup"><span data-stu-id="a03c5-782">Eliminate all fixed-function operations in favor of programmable shaders.</span></span>
-   <span data-ttu-id="a03c5-783">將所有現有的著色器更新為著色器模型 4.x/5 的新語法。</span><span class="sxs-lookup"><span data-stu-id="a03c5-783">Update all existing shaders to the new syntax of Shader Model 4.x/5.</span></span>
-   <span data-ttu-id="a03c5-784">更新資源管理以支援新的視圖模型。</span><span class="sxs-lookup"><span data-stu-id="a03c5-784">Update resource management to support the new view model.</span></span>
-   <span data-ttu-id="a03c5-785">將所有資產轉換為使用新的可用格式清單。</span><span class="sxs-lookup"><span data-stu-id="a03c5-785">Convert all assets to use a new list of available formats.</span></span>
-   <span data-ttu-id="a03c5-786">更新轉譯狀態處理以使用不可變的狀態欄塊，然後將著色器常數重新提交到常數緩衝區。</span><span class="sxs-lookup"><span data-stu-id="a03c5-786">Update render state handling to use immutable state blocks, and rework shader constants into constant buffers.</span></span>

<span data-ttu-id="a03c5-787">這項轉換對於啟用 Direct3D 11 展示是不可或缺的，但結果不符合利用新 API 的展示需求。</span><span class="sxs-lookup"><span data-stu-id="a03c5-787">This conversion is essential to enable the Direct3D 11 showcase, although the result does not meet the showcase requirement of exploiting the new API.</span></span>

<span data-ttu-id="a03c5-788">新的 API 和相關聯的 HLSL 程式設計模型提供許多提高內容的機會：</span><span class="sxs-lookup"><span data-stu-id="a03c5-788">The new API and associated HLSL programming model offers many opportunities for enhanced content:</span></span>

-   <span data-ttu-id="a03c5-789">運用現有的 Direct3D 10 硬體功能，例如幾何著色器、串流輸出、材質陣列，以及 BC4/BC5 壓縮的材質格式。</span><span class="sxs-lookup"><span data-stu-id="a03c5-789">Leveraging existing Direct3D 10 hardware features, such as Geometry Shader, Stream Out, texture arrays, and the BC4/BC5 compressed texture formats.</span></span>
-   <span data-ttu-id="a03c5-790">運用現有的 Direct3D 10.1 硬體功能，例如獨立的每一轉譯目標 blend 模式、MSAA 深度取回、MSAA 每個範例的著色器存取、cube 地圖陣列，以及轉譯成區塊壓縮的 (BC) 格式。</span><span class="sxs-lookup"><span data-stu-id="a03c5-790">Leveraging existing Direct3D 10.1 hardware features, such as independent per-render-target blend modes, MSAA depth read back, MSAA per-sample shader access, cube map arrays, and rendering to block-compressed (BC) formats.</span></span>
-   <span data-ttu-id="a03c5-791">在現有的 Direct3D 10/10.1 視訊卡上使用計算著色器搭配 CS4 來實行先進的 GPU 演算法 (由更新的影片驅動程式) 或在下一代 Direct3D 11 視訊卡上的 CS 5.0 來啟用。</span><span class="sxs-lookup"><span data-stu-id="a03c5-791">Implementing advanced GPU algorithms using Compute Shader with CS4.x on existing Direct3D 10/10.1 video cards (enabled by updated video drivers) or CS 5.0 on next-generation Direct3D 11 video cards.</span></span>
-   <span data-ttu-id="a03c5-792">使用無限制執行緒資源建立和多個裝置內容，在多個執行緒上轉譯，以改善多核心系統的效能， (使用更新的視頻驅動程式) 。</span><span class="sxs-lookup"><span data-stu-id="a03c5-792">Rendering on multiple threads using free-threaded resource creation and multiple device contexts for improved performance on multicore systems (with updated video drivers).</span></span> <span data-ttu-id="a03c5-793">如需詳細資訊，請參閱 Windows 展示的遊戲。3。</span><span class="sxs-lookup"><span data-stu-id="a03c5-793">For more information, see the Games for Windows Showcase S.3.</span></span>
-   <span data-ttu-id="a03c5-794">使用 Direct3D 11 類別影片硬體的新功能，例如使用輪廓和網域著色器進行硬體鑲嵌、著色器模型 5.0 HLSL 著色器硬體功能 BC6HBC7 壓縮的材質格式，以及動態著色器連結。</span><span class="sxs-lookup"><span data-stu-id="a03c5-794">Utilizing new features of Direct3D 11-class video hardware, such as hardware tessellation with hull and domain shaders, Shader Model 5.0 HLSL shader hardware features BC6HBC7 compressed texture formats, and Dynamic Shader Linkage.</span></span>

<span data-ttu-id="a03c5-795">可以使用 Direct3D 9 來執行的技術，主要是透過高 CPU 成本來 () 可以使用有效率的方式將其載入至 GPU，進而釋出 CPU 資源以支援其他遊戲需求。</span><span class="sxs-lookup"><span data-stu-id="a03c5-795">Techniques that can be implemented with Direct3D 9 (largely through high CPU cost) can be off loaded to the GPU in an efficient manner, thus freeing CPU resources to support other game demands.</span></span>

<span data-ttu-id="a03c5-796">您可以從 DirectX SDK 取得 Direct3D 11 Api、支援工具和範例。</span><span class="sxs-lookup"><span data-stu-id="a03c5-796">Direct3D 11 APIs, supporting tools, and samples are available in the DirectX SDK.</span></span> <span data-ttu-id="a03c5-797">另請參閱 Windows 中的圖形 Api。</span><span class="sxs-lookup"><span data-stu-id="a03c5-797">Also see Graphics APIs in Windows.</span></span>

</dd> </dl>

### <a name="s2-exploit-x64-native"></a><span data-ttu-id="a03c5-798">S. 2 惡意探索 x64 原生</span><span class="sxs-lookup"><span data-stu-id="a03c5-798">S.2 Exploit x64 Native</span></span>

<dl> <dt>

<span data-ttu-id="a03c5-799"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**要求**</span><span class="sxs-lookup"><span data-stu-id="a03c5-799"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requirement**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-800">此遊戲包含64位原生可執行檔，可提供在 x64 支援的硬體上執行的 x64 版 Windows 所啟用的強大新體驗。</span><span class="sxs-lookup"><span data-stu-id="a03c5-800">The game includes a 64-bit native executable that delivers a compelling new experience enabled by x64 editions of Windows running on x64-capable hardware.</span></span> <span data-ttu-id="a03c5-801">與32位版本的遊戲並存比較，應會在內容複雜度、降低整體載入時間和效能方面提供可察覺改進。</span><span class="sxs-lookup"><span data-stu-id="a03c5-801">A side-by-side comparison with the 32-bit version of the game should show a perceptible improvement in content complexity, reduced overall load times, and performance.</span></span>

<span data-ttu-id="a03c5-802">在 Windows 的64位版本中，安裝程式應一律將64位原生版本設定為遊戲瀏覽器和 Windows XP Professional x64 Edition 中快速鍵的預設值。</span><span class="sxs-lookup"><span data-stu-id="a03c5-802">On 64-bit editions of Windows, installation should always set up the 64-bit native version of the game as the default for shortcuts in Games Explorer and Windows XP Professional x64 Edition.</span></span> <span data-ttu-id="a03c5-803">如果需要雙重安裝，則可以為 Windows Vista 和 Windows 7 上的遊戲瀏覽器指定可指向32位版本的額外播放工作，但預設值應該保持64位原生版本。</span><span class="sxs-lookup"><span data-stu-id="a03c5-803">If dual installation is desired, then an additional play task can be specified for Games Explorer on Windows Vista and Windows 7 that points to the 32-bit version, but the default should remain the 64-bit native version.</span></span>

<span data-ttu-id="a03c5-804">請注意，此遊戲應支援 Windows Vista 和 Windows 7 的64位版本，以符合此展示建議。</span><span class="sxs-lookup"><span data-stu-id="a03c5-804">Note that the game should support the 64-bit editions of Windows Vista and Windows 7 to meet this showcase recommendation.</span></span> <span data-ttu-id="a03c5-805">建議 Windows XP Professional x64 Edition 的支援，但不是必要的。</span><span class="sxs-lookup"><span data-stu-id="a03c5-805">Support for Windows XP Professional x64 Edition is encouraged, but not required.</span></span>

</dd> <dt>

<span data-ttu-id="a03c5-806"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**理由**</span><span class="sxs-lookup"><span data-stu-id="a03c5-806"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Rationale**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-807">x64 技術為消費者和伺服器市場提供64位的定址功能，包括現有應用程式的全速32位反向相容性。</span><span class="sxs-lookup"><span data-stu-id="a03c5-807">x64 technology provides 64-bit addressing capabilities for both the consumer and server markets that includes full-speed 32-bit backwards compatibly for existing applications.</span></span> <span data-ttu-id="a03c5-808">x64 是適用于 AMD (AMD64) 和 Intel (EMT64) 的藍圖主要部分，除了超行動 Cpu 之外，還支援所有目前和未來世代處理器的技術。</span><span class="sxs-lookup"><span data-stu-id="a03c5-808">x64 is a key part of the roadmap for both AMD (AMD64) and Intel (EMT64), and, with the exception of ultra-mobile CPUs, support the technology for all current and future generation processors.</span></span>

<span data-ttu-id="a03c5-809">Windows XP Professional x64 Edition 是第一個取用者導向的 Windows 作業系統 (作業系統) 支援 x64 技術，而 Windows Vista 和 Windows 7 則大幅擴充了 OS 的可用性，以供64位的取用者計算之用。</span><span class="sxs-lookup"><span data-stu-id="a03c5-809">Windows XP Professional x64 Edition was the first consumer-oriented Windows operating system (OS) to support x64 technology, and Windows Vista and Windows 7 greatly expand the availability of the OS-enablement for 64-bit consumer computing.</span></span> <span data-ttu-id="a03c5-810">在許多新電腦上使用 2 GB 的 RAM 作為標準時，記憶體調整的進一步改進將無法受益于32位個別應用程式，而這些應用程式無法處理超過 2 GB 的實體 RAM。</span><span class="sxs-lookup"><span data-stu-id="a03c5-810">With 2 GB of RAM as standard on many new computers, further improvements in memory scaling will not benefit 32-bit individual applications that are unable to address more than 2 GB of physical RAM.</span></span> <span data-ttu-id="a03c5-811">現今許多遊戲都面臨挑戰，將所有可用的內容納入 2 GB 的虛擬位址空間的限制，尤其是在與高階 Gpu 上提供的大型影片可用的大型影片，以及轉換成 x64 技術時，都能大幅增加支援層級的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="a03c5-811">Many games today are facing challenges fitting all of the available content into the constraints of 2 GB of virtual address space, especially when combined with the large video memories available on high-end GPUs, and moving to x64 technology greatly increases the supportable levels of detail.</span></span>

<span data-ttu-id="a03c5-812">32位遊戲的 x64 相容性是 Windows 技術需求 (2.2) 的遊戲，但充分利用新的技術需要64位原生執行。</span><span class="sxs-lookup"><span data-stu-id="a03c5-812">x64 compatibility for 32-bit games is a Games for Windows technical requirement (2.2), but taking full advantage of the new technologies requires a 64-bit native implementation.</span></span>

</dd> <dt>

<span data-ttu-id="a03c5-813"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**其他資訊**</span><span class="sxs-lookup"><span data-stu-id="a03c5-813"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Additional Information**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-814">64位定址的主要優點是能夠直接存取 2 GB 以上的實體和虛擬記憶體。</span><span class="sxs-lookup"><span data-stu-id="a03c5-814">The primary benefit of 64-bit addressing is the ability to directly access more than 2 GB of physical and virtual memory.</span></span> <span data-ttu-id="a03c5-815">大型虛擬記憶體位址空間可廣泛地使用記憶體對應 i/o，而不需要擔心32位程式設計中常見的 VM 位址空間耗盡問題。</span><span class="sxs-lookup"><span data-stu-id="a03c5-815">The large virtual memory address space allows for extensive use of memory-mapped I/O without concern for VM address space exhaustion problems prevalent in 32-bit programming.</span></span> <span data-ttu-id="a03c5-816">遊戲可以利用新的空間來大幅改善載入時間，或在某些情況下，消除載入內容的暫停。</span><span class="sxs-lookup"><span data-stu-id="a03c5-816">Games can take advantage of the new space to greatly improve load times or, in some instances, to eliminate pauses for loading content.</span></span>

<span data-ttu-id="a03c5-817">現有的32位應用程式可從 x64 版本獲益，方法是在使用 [啟用大型位址] (**/LARGEADDRESSAWARE**) 連結器選項來處理具有完整32位資料的位址時。</span><span class="sxs-lookup"><span data-stu-id="a03c5-817">Existing 32-bit applications can benefit from x64 editions by having the capability to process addresses with full 32-bit data when built with the Enable Large Addresses (**/LARGEADDRESSAWARE**) linker option.</span></span> <span data-ttu-id="a03c5-818">在32位版本的 Windows XP 上，特殊的開機模式允許這類應用程式處理最多 3 GB 的 RAM，而 x64 版可讓您存取最多 4 GB 的 RAM，以用於感知 (LAA) 應用程式的大型位址。</span><span class="sxs-lookup"><span data-stu-id="a03c5-818">On 32-bit versions of Windows XP, special boot modes allowed such applications to address up to 3 GB of RAM, and x64 editions provide access up to 4 GB of RAM for Large Address Aware (LAA) apps.</span></span> <span data-ttu-id="a03c5-819">雖然在32位應用程式中使用 LAA 並不符合這項展示需求，但是這項橋樑技術是在 x64 版本的 Windows 上提供額外的調整優勢，而不會完全符合此展示需求的方式。</span><span class="sxs-lookup"><span data-stu-id="a03c5-819">While use of LAA in a 32-bit application does not meet this showcase requirement, this bridge technology is an extremely useful way of providing additional scaling benefits on x64 versions of Windows for those not fully implementing this showcase requirement.</span></span>

<span data-ttu-id="a03c5-820">如需詳細資訊，請參閱遊戲開發人員和[ram、VRAM 和更多 ram](https://www.gamasutra.com/view/feature/3602/sponsored_feature_ram_vram_and_.php) [的64位程式設計](/windows/desktop/DxTechArts/sixty-four-bit-programming-for-game-developers)：64位遊戲位於 Gamasutra。</span><span class="sxs-lookup"><span data-stu-id="a03c5-820">For more information, see [64-bit programming for Game Developers](/windows/desktop/DxTechArts/sixty-four-bit-programming-for-game-developers) and [RAM, VRAM, and More RAM: 64-bit Gaming Is Here](https://www.gamasutra.com/view/feature/3602/sponsored_feature_ram_vram_and_.php) in Gamasutra.</span></span>

> [!Note]  
> <span data-ttu-id="a03c5-821">此展示的主要挑戰，是確保您的遊戲所依賴的任何協力廠商程式庫或元件都可用於64位原生開發。</span><span class="sxs-lookup"><span data-stu-id="a03c5-821">A key challenge for this showcase is ensuring any third-party libraries or components your game relies on are available for 64-bit native development.</span></span> <span data-ttu-id="a03c5-822">許多舊版的 Microsoft Api 也已從64位的原生環境中消除，這可能會對引擎程式碼基底（包含較舊的重要系統執行）產生挑戰。</span><span class="sxs-lookup"><span data-stu-id="a03c5-822">Many legacy Microsoft APIs also have been eliminated from the 64-bit native environment, which can prove a challenge for engine code bases containing older implementations of key systems.</span></span>

 

</dd> </dl>

### <a name="s3-exploit-many-core-processors"></a><span data-ttu-id="a03c5-823">S. 3 惡意探索 Many-Core 處理器</span><span class="sxs-lookup"><span data-stu-id="a03c5-823">S.3 Exploit Many-Core Processors</span></span>

<dl> <dt>

<span data-ttu-id="a03c5-824"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**要求**</span><span class="sxs-lookup"><span data-stu-id="a03c5-824"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requirement**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-825">這項遊戲所實行的功能，可利用多核心處理器、調整為3、4或更多核心（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="a03c5-825">The game implements features that take advantage of multicore processors, scaling to 3, 4, or more cores, when available.</span></span>

<span data-ttu-id="a03c5-826">如果遊戲支援單處理器或雙核心系統，則與四核心系統並存的比較，應該會展示可察覺的新功能、其他引人注目的效果、內容品質的改進，以及/或改善的效能。</span><span class="sxs-lookup"><span data-stu-id="a03c5-826">If the game supports single-processor or dual-core systems, a side-by-side comparison with a quad-core system should demonstrate perceptible new features, additional compelling effects, improvement in content quality, and/or improved performance.</span></span>

<span data-ttu-id="a03c5-827">因為遊戲已經廣泛支援雙核心調整，而且各種 Direct3D 驅動程式增強功能都會自動利用雙核心調整，所以雙核心調整不足以示範此展示。</span><span class="sxs-lookup"><span data-stu-id="a03c5-827">Because dual-core scaling is already widely supported by games, as well as automatically utilized by various Direct3D driver enhancements, dual-core scaling is not sufficient to demonstrate this showcase.</span></span>

</dd> <dt>

<span data-ttu-id="a03c5-828"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**理由**</span><span class="sxs-lookup"><span data-stu-id="a03c5-828"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Rationale**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-829">Cpu 的效能持續成長已從時脈速率的增強功能切換到加法運算核心。</span><span class="sxs-lookup"><span data-stu-id="a03c5-829">The continuing growth in performance for CPUs has switched from clock rate improvements to the addition of computational cores.</span></span> <span data-ttu-id="a03c5-830">AMD 和 Intel 藍圖都是以可擴充的多核心設計為基礎。</span><span class="sxs-lookup"><span data-stu-id="a03c5-830">Both AMD and Intel roadmaps are based on scalable, multicore designs.</span></span> <span data-ttu-id="a03c5-831">所有新一代遊戲平臺都有多核心 Cpu，因為這是處理器演進的基礎轉變。</span><span class="sxs-lookup"><span data-stu-id="a03c5-831">All next-generation game platforms have multicore CPUs because of this fundamental shift in the evolution of processors.</span></span> <span data-ttu-id="a03c5-832">單一執行緒應用程式不再會看到下一代 Cpu 的顯著增益。</span><span class="sxs-lookup"><span data-stu-id="a03c5-832">Single-threaded applications no longer will see significant gains from next-generation CPUs.</span></span> <span data-ttu-id="a03c5-833">簡單的多執行緒也將無法調整，因為一般使用中的 CPU 核心數目會成長到三個以上。</span><span class="sxs-lookup"><span data-stu-id="a03c5-833">Simple multithreading also will fail to scale as the number of CPU cores in common use grows to three or more.</span></span>

</dd> <dt>

<span data-ttu-id="a03c5-834"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**其他資訊**</span><span class="sxs-lookup"><span data-stu-id="a03c5-834"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Additional Information**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-835">請注意，核心計數不需要是2的乘冪，因此遊戲應以線性方式調整，並處理核心計數3、4、5、6、7、8等等。</span><span class="sxs-lookup"><span data-stu-id="a03c5-835">Note that core counts need not be a power of two, so games should scale linearly and handle core counts of 3, 4, 5, 6, 7, 8, and so on.</span></span>

<span data-ttu-id="a03c5-836">藉由增加應用程式中的執行緒數目來進行調整，只會在檢查中保存通訊和執行緒同步處理的成本時提供傳回。</span><span class="sxs-lookup"><span data-stu-id="a03c5-836">Scaling by increasing the number of threads in an application only provides a return if the cost of communication and thread synchronization are kept in check.</span></span> <span data-ttu-id="a03c5-837">以功能為基礎的調整可能會在短期內證明更簡單的解決方案，讓遊戲正常運作，而不需要在單一核心系統上使用額外的執行緒，並在可用的額外 CPU 電源時啟用它們。</span><span class="sxs-lookup"><span data-stu-id="a03c5-837">Feature-based scaling may prove an easier solution in the short-term, allowing the game to operate normally without the additional threads on single-core systems and enabling them when the additional CPU power is available.</span></span>

<span data-ttu-id="a03c5-838">如需詳細資訊，請參閱在 [Xbox 360 和 Microsoft windows 上撰寫多核心的程式碼](/windows/desktop/DxTechArts/coding-for-multiple-cores) ，以及 DXUTLockFreePipe 公用程式和 CoreDetection 範例中的 [Xbox 360 和 microsoft Windows 的程式設計考慮 Lockless](/windows/desktop/DxTechArts/lockless-programming) 。</span><span class="sxs-lookup"><span data-stu-id="a03c5-838">For more information, see [Coding For Multiple Cores on Xbox 360 and Microsoft Windows](/windows/desktop/DxTechArts/coding-for-multiple-cores) and [Lockless Programming Considerations for Xbox 360 and Microsoft Windows](/windows/desktop/DxTechArts/lockless-programming) in the DirectX articles, as well as the DXUTLockFreePipe utility and the CoreDetection sample.</span></span>

<span data-ttu-id="a03c5-839">使用 Direct3D 11 無線程資源建立和裝置內容，有助於在轉譯和載入圖形資源時達到多核心的擴充性。</span><span class="sxs-lookup"><span data-stu-id="a03c5-839">Making use of the Direct3D 11 free-threaded resource creation and device contexts is useful in achieving many-core scalability in rendering and loading graphics resources.</span></span> <span data-ttu-id="a03c5-840">查看 Windows 展示的遊戲。1。</span><span class="sxs-lookup"><span data-stu-id="a03c5-840">See Games for Windows Showcase S.1.</span></span>

<span data-ttu-id="a03c5-841">請注意，直接使用 CPU 指令 rdtsc，而不是使用 Windows Api 來計算多核心系統的時間，可能會導致某些硬體和 OS 設定發生問題;請參閱 DirectX 文章中的 [遊戲時間和多核心處理器](/windows/desktop/DxTechArts/game-timing-and-multicore-processors) 。</span><span class="sxs-lookup"><span data-stu-id="a03c5-841">Note that using the CPU instruction rdtsc directly, instead of using Windows APIs to compute timing on multicore systems, can lead to problems on some hardware and OS configurations; see [Game Timing and Multicore Processors](/windows/desktop/DxTechArts/game-timing-and-multicore-processors) in the DirectX articles.</span></span>

</dd> </dl>

### <a name="s4-support-games-for-windows---live"></a><span data-ttu-id="a03c5-842">S：4支援 Windows-LIVE 的遊戲</span><span class="sxs-lookup"><span data-stu-id="a03c5-842">S.4 Support Games for Windows - LIVE</span></span>

<span data-ttu-id="a03c5-843">Microsoft 不再支援 Windows LIVE 的遊戲。</span><span class="sxs-lookup"><span data-stu-id="a03c5-843">Games for Windows - LIVE is no longer supported by Microsoft.</span></span>

### <a name="s5-support-windows-touch"></a><span data-ttu-id="a03c5-844">Windows Touch 的5個支援</span><span class="sxs-lookup"><span data-stu-id="a03c5-844">S.5 Support Windows Touch</span></span>

<dl> <dt>

<span data-ttu-id="a03c5-845"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**要求**</span><span class="sxs-lookup"><span data-stu-id="a03c5-845"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requirement**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-846">Windows 觸控式遊戲可在執行 Windows 7 的電腦上使用觸控和/或手勢播放，並具有觸控顯示功能。</span><span class="sxs-lookup"><span data-stu-id="a03c5-846">Windows touch-capable games are playable using touch and/or gestures on computers running Windows 7 with a touch display.</span></span> <span data-ttu-id="a03c5-847">您也可以使用鍵盤輸入，但主要 play 介面必須以觸控式為基礎。</span><span class="sxs-lookup"><span data-stu-id="a03c5-847">Keyboard input can be used as well, but the primary play interface must be touch-based.</span></span>

<span data-ttu-id="a03c5-848">啟用觸控不應防止使用滑鼠或一般控制器，受限於技術需求1.4。</span><span class="sxs-lookup"><span data-stu-id="a03c5-848">Enabling touch should not prevent the use of the mouse or common controller, subject to Technical Requirement 1.4.</span></span>

<span data-ttu-id="a03c5-849">遊戲的安裝程式不應支援 Windows Touch 功能。</span><span class="sxs-lookup"><span data-stu-id="a03c5-849">The game's installer is not expected to support Windows Touch functionality.</span></span>

</dd> <dt>

<span data-ttu-id="a03c5-850"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**理由**</span><span class="sxs-lookup"><span data-stu-id="a03c5-850"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Rationale**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-851">膝上型電腦和桌上型電腦都可以使用多點觸控功能的電腦，它們代表 Windows 7 發行版本升級的主要硬體功能。</span><span class="sxs-lookup"><span data-stu-id="a03c5-851">Multi-touch-capable displays for computers are available for laptops and desktops, and they represent a key hardware feature being promoted with the release of Windows 7.</span></span> <span data-ttu-id="a03c5-852">Windows 7 支援整個桌面和通用控制項介面的 Windows Touch。</span><span class="sxs-lookup"><span data-stu-id="a03c5-852">Windows 7 supports Windows Touch throughout the desktop and common controls interfaces.</span></span>

</dd> <dt>

<span data-ttu-id="a03c5-853"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**其他資訊**</span><span class="sxs-lookup"><span data-stu-id="a03c5-853"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Additional Information**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-854">原生程式碼應用程式可以搭配 RegisterTouchWindow 函式，透過 WM 觸控訊息來存取多點觸控 \_ 。 [](/windows/desktop/api/winuser/nf-winuser-registertouchwindow)</span><span class="sxs-lookup"><span data-stu-id="a03c5-854">Native code applications can access multi-touch through the WM\_TOUCH messages, in combination with the [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow) function.</span></span> <span data-ttu-id="a03c5-855">另請參閱操作和慣性 API。</span><span class="sxs-lookup"><span data-stu-id="a03c5-855">See also the Manipulations and Inertia API.</span></span>

<span data-ttu-id="a03c5-856">Windows Presentation Foundation (WPF) 4.0 提供多點觸控介面的受控解決方案。</span><span class="sxs-lookup"><span data-stu-id="a03c5-856">Windows Presentation Foundation (WPF) 4.0 provides a managed solution for multi-touch interfaces.</span></span>

<span data-ttu-id="a03c5-857">如需詳細資訊，請參閱 Windows Touch SDK。</span><span class="sxs-lookup"><span data-stu-id="a03c5-857">For more information, see the Windows Touch SDK.</span></span>

</dd> </dl>

### <a name="s6-support-high-color"></a><span data-ttu-id="a03c5-858">S 6 支援高色彩</span><span class="sxs-lookup"><span data-stu-id="a03c5-858">S.6 Support High Color</span></span>

<dl> <dt>

<span data-ttu-id="a03c5-859"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**要求**</span><span class="sxs-lookup"><span data-stu-id="a03c5-859"><span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Requirement**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-860">支援高彩的遊戲會使用 10:10:10:2 (DXGI \_ 格式 \_ R10G10B10A2、D3DFMT \_ A2B10G10R10) 或 16:16:16:16 (DXGI \_ 格式 \_ R16G16B16A16、D3DFMT \_ A16B16G16R16) 格式來呈現背景緩衝區和全螢幕顯示模式。</span><span class="sxs-lookup"><span data-stu-id="a03c5-860">Games that support High Color use a 10:10:10:2 (DXGI\_FORMAT\_R10G10B10A2, D3DFMT\_A2B10G10R10) or a 16:16:16:16 (DXGI\_FORMAT\_R16G16B16A16, D3DFMT\_A16B16G16R16) format for the rendering back-buffer and full-screen display mode.</span></span>

<span data-ttu-id="a03c5-861">藉由使用高色彩轉譯目標，在執行10位或16位範圍的色調對應時，可以使用延伸或寬範圍來轉譯 High-Dynamic 範圍 (HDR) 內容。</span><span class="sxs-lookup"><span data-stu-id="a03c5-861">By using a  High Color  render target, High-Dynamic Range (HDR) content can be rendered with an extended or wide gamut when performing tone mapping to a 10-bit or 16-bit range.</span></span>

</dd> <dt>

<span data-ttu-id="a03c5-862"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**理由**</span><span class="sxs-lookup"><span data-stu-id="a03c5-862"><span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Rationale**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-863">監視器在許多年份中都能夠顯示超過256色層級，即使 CRT 顯示器普遍出現也是如此。</span><span class="sxs-lookup"><span data-stu-id="a03c5-863">Monitors have been capable of displaying more than 256 color levels per channel for many years, even when CRT displays were prevalent.</span></span> <span data-ttu-id="a03c5-864">掃描視訊卡上的硬體是限制因素。</span><span class="sxs-lookup"><span data-stu-id="a03c5-864">The scan out hardware on video cards has been the limiting factor.</span></span> <span data-ttu-id="a03c5-865">新式 Gpu （包括大部分的 Direct3D 9 類別硬體以及所有 Direct3D 10 類別和更佳的硬體）具有每個通道至少能有10位的掃描後的硬體，而硬體功能則是設定為在未來的每個顏色通道成長至16位。</span><span class="sxs-lookup"><span data-stu-id="a03c5-865">Modern GPUs, including most Direct3D 9-class hardware and all Direct3D 10-class and better hardware, have scan-out hardware capable of at least 10-bits per channel, and hardware capability is set to grow to 16-bits per color channel in the future.</span></span> <span data-ttu-id="a03c5-866">HD TV 互連系統 (HDMI、DisplayPort) 設計為每個通道處理超過8位，而且類比 VGA 已經有這類信號。</span><span class="sxs-lookup"><span data-stu-id="a03c5-866">HD TV interconnect systems (HDMI, DisplayPort) have been designed to handle more than 8-bits per channel as well, and analog VGA will already carry such signals.</span></span>

</dd> <dt>

<span data-ttu-id="a03c5-867"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**其他資訊**</span><span class="sxs-lookup"><span data-stu-id="a03c5-867"><span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Additional Information**</span></span>
</dt> <dd>

<span data-ttu-id="a03c5-868">請注意，在過去，高彩或嗨的色彩是指從 256 (8 位) 色彩顯示為15或16位色彩顯示。</span><span class="sxs-lookup"><span data-stu-id="a03c5-868">Note that High Color, or Hi Color, historically refers to moving from 256 (8-bit) color displays to 15- or 16-bit color displays.</span></span> <span data-ttu-id="a03c5-869">大部分的顯示器系統自移至真正的色彩，也就是24位色彩，或是紅色、綠色和藍色的每個色彩頻道都有8位。</span><span class="sxs-lookup"><span data-stu-id="a03c5-869">Most display systems have long since moved on to True Color which is 24-bit color, or 8-bits per color channel for red, green, and blue.</span></span> <span data-ttu-id="a03c5-870">在這裡，我們表示新一代的顯示器系統，可在每個個別色頻中使用超過8個位的方式運作。</span><span class="sxs-lookup"><span data-stu-id="a03c5-870">By High Color here we mean a new generation of displays systems that can operate with more than 8-bits per individual color channel.</span></span> <span data-ttu-id="a03c5-871">也稱為深度色彩。</span><span class="sxs-lookup"><span data-stu-id="a03c5-871">The is also referred to as Deep Color.</span></span>

</dd> </dl>

### <a name="recommended-best-practices"></a><span data-ttu-id="a03c5-872">建議的最佳作法</span><span class="sxs-lookup"><span data-stu-id="a03c5-872">Recommended Best Practices</span></span>

### <a name="introduction"></a><span data-ttu-id="a03c5-873">簡介</span><span class="sxs-lookup"><span data-stu-id="a03c5-873">Introduction</span></span>

<span data-ttu-id="a03c5-874">除了符合技術需求，並在您的標題中採用一或多個展示，所有 Windows 遊戲都應遵循一些最佳作法。</span><span class="sxs-lookup"><span data-stu-id="a03c5-874">In addition to meeting the Technical Requirements and adopting one or more Showcases in your title, there are a number of best practices that should be followed for all Windows games.</span></span> <span data-ttu-id="a03c5-875">雖然這些建議落在核心技術需求的範圍之外，但強烈建議您針對 Windows 標題的所有遊戲採用這些建議。</span><span class="sxs-lookup"><span data-stu-id="a03c5-875">While these recommendations fall outside the scope of the core Technical Requirements, you are strongly encouraged to employ them for all Games for Windows titles.</span></span>

### <a name="additional-recommendations"></a><span data-ttu-id="a03c5-876">其他建議</span><span class="sxs-lookup"><span data-stu-id="a03c5-876">Additional Recommendations</span></span>

-   <span data-ttu-id="a03c5-877">使用最新的 Visual Studio 編譯器和執行時間。</span><span class="sxs-lookup"><span data-stu-id="a03c5-877">Use the most recent Visual Studio compiler and runtime.</span></span> <span data-ttu-id="a03c5-878">較新版本的編譯器會針對所產生的程式碼品質和安全性問題，執行大幅的改進，並採用新式的處理器優化策略。</span><span class="sxs-lookup"><span data-stu-id="a03c5-878">Newer versions of the compiler implement significant improvements for the quality of code generated and for security issues, and they employ modern processor optimization strategies.</span></span> <span data-ttu-id="a03c5-879">更新編譯器和使用最新的 C 執行時間是遷移至新式程式碼撰寫實務的簡單方法。</span><span class="sxs-lookup"><span data-stu-id="a03c5-879">Updating the compiler and using the latest C Runtime is an easy way to migrate to modern coding practices.</span></span>
-   <span data-ttu-id="a03c5-880">使用動態連結程式庫 (DLL) 版本的 C 執行時間，而不是靜態連結，並利用安全 CRT。</span><span class="sxs-lookup"><span data-stu-id="a03c5-880">Use the dynamic-link library (DLL) version of the C Runtime, rather than static linking, and make use of Secure CRT.</span></span> <span data-ttu-id="a03c5-881"> (例外狀況可以在特殊的預先安裝案例中進行，例如自動執行程式或安裝程式本身) 。</span><span class="sxs-lookup"><span data-stu-id="a03c5-881">(Exceptions can be made in special pre-installation cases, like for an Autorun program or for the installer itself).</span></span>
-   <span data-ttu-id="a03c5-882">若為遊戲音訊，請使用 XAudio2、X3DAudio 及（或）交易，而不是 DirectSound。</span><span class="sxs-lookup"><span data-stu-id="a03c5-882">For game audio, use XAudio2, X3DAudio, and/or XACT, rather than DirectSound.</span></span> <span data-ttu-id="a03c5-883">針對執行所有混合和來源速率轉換的音訊引擎，以及只需要低延遲的音訊輸出解決方案，請使用 Windows XP (上的 DirectSound，只在 Windows Vista 和 Windows 7 上使用) 和 WASAPI。</span><span class="sxs-lookup"><span data-stu-id="a03c5-883">For audio engines that do all mixing and source-rate conversion and need only a low-latency solution for audio output, use DirectSound on Windows XP (only) and WASAPI on Windows Vista and Windows 7.</span></span>
-   <span data-ttu-id="a03c5-884">避免使用舊版和已淘汰的 Api： DirectDraw、DirectSound、DirectPlay、DirectMusic 的效能層級、DirectPlay 語音和 Direct3D 保留模式。</span><span class="sxs-lookup"><span data-stu-id="a03c5-884">Avoid using legacy and deprecated APIs: DirectDraw, DirectSound, DirectPlay, DirectMusic's performance layer, DirectPlay Voice, and Direct3D Retained Mode.</span></span> <span data-ttu-id="a03c5-885">請注意，Windows Vista 或 Windows 7 上都不提供 [DirectPlay 語音] 和 [Direct3D 保留] 模式。</span><span class="sxs-lookup"><span data-stu-id="a03c5-885">Note that DirectPlay Voice and Direct3D Retained Mode are not available at all on Windows Vista or Windows 7.</span></span> <span data-ttu-id="a03c5-886">X64 原生應用程式無法使用 DirectPlay 和 DirectMusic 的效能層級。</span><span class="sxs-lookup"><span data-stu-id="a03c5-886">DirectPlay and DirectMusic's performance layer are not available to x64-native applications.</span></span>
-   <span data-ttu-id="a03c5-887">使用 SSE/SSE2 SIMD 指令集進行優化。</span><span class="sxs-lookup"><span data-stu-id="a03c5-887">Optimize using SSE/SSE2 SIMD instruction sets.</span></span> <span data-ttu-id="a03c5-888">請參閱 Windows SDK 中的 [DirectXMath](/windows/desktop/dxmath/directxmath-portal) API，作為 SIMD 優化數學運算作業的跨平臺解決方案。</span><span class="sxs-lookup"><span data-stu-id="a03c5-888">See the [DirectXMath](/windows/desktop/dxmath/directxmath-portal) API in the Windows SDK as a cross-platform solution for SIMD-optimized math operations.</span></span>
-   <span data-ttu-id="a03c5-889">使用 Windows 安全性的新式最佳作法 (包括編譯器和連結器選項，例如 **/NXCOMPAT**、 **/gs**、 **/SAFESEH**、 **/DYNAMICBASE**、 **/SDL** 等) 。</span><span class="sxs-lookup"><span data-stu-id="a03c5-889">Use modern best practices for Windows security (including compiler and linker options like **/NXCOMPAT**, **/GS**, **/SAFESEH**, **/DYNAMICBASE**, **/SDL**, and so on).</span></span> <span data-ttu-id="a03c5-890">如需詳細資訊，請參閱 [遊戲開發的最佳安全性作法](/windows/desktop/DxTechArts/best-security-practices-in-game-development)。</span><span class="sxs-lookup"><span data-stu-id="a03c5-890">For more information, see [Best Security Practices in Game Development](/windows/desktop/DxTechArts/best-security-practices-in-game-development).</span></span>
-   <span data-ttu-id="a03c5-891">使用最新的 Windows SDK 元件和程式庫。</span><span class="sxs-lookup"><span data-stu-id="a03c5-891">Use the latest Windows SDK components and libraries.</span></span> <span data-ttu-id="a03c5-892">移除舊版 DirectSetup 的相依性，例如 D3DX9、D3DX10 和 D3DX11。</span><span class="sxs-lookup"><span data-stu-id="a03c5-892">Remove dependencies on the legacy DirectSetup deployed out-of-band components such as D3DX9, D3DX10, and D3DX11.</span></span> <span data-ttu-id="a03c5-893">請考慮使用 [DirectXTex](https://github.com/Microsoft/DirectXTex) 或 [DirectXTK](https://github.com/Microsoft/DirectXTK) 或兩者。</span><span class="sxs-lookup"><span data-stu-id="a03c5-893">Consider using [DirectXTex](https://github.com/Microsoft/DirectXTex) or [DirectXTK](https://github.com/Microsoft/DirectXTK) or both.</span></span>
-   <span data-ttu-id="a03c5-894">請避免使用較舊的 HLSL 編譯器，而改為使用新式 HLSL 編譯器。</span><span class="sxs-lookup"><span data-stu-id="a03c5-894">Avoid using the older HLSL compiler, and instead, use the modern HLSL compiler.</span></span> <span data-ttu-id="a03c5-895">如果您的應用程式需要圖元著色器1.x 的支援，請使用著色器元件而非 HLSL，或將較舊的編譯器限制為只使用這些案例。</span><span class="sxs-lookup"><span data-stu-id="a03c5-895">If support for Pixel Shader 1.x is required by your application, use shader assembly rather than HLSL, or limit the use of the older compiler to just those scenarios.</span></span>

## <a name="resources"></a><span data-ttu-id="a03c5-896">資源</span><span class="sxs-lookup"><span data-stu-id="a03c5-896">Resources</span></span>



| <span data-ttu-id="a03c5-897">詞彙</span><span class="sxs-lookup"><span data-stu-id="a03c5-897">Term</span></span>                                                                                                                                                                                                                         | <span data-ttu-id="a03c5-898">描述</span><span class="sxs-lookup"><span data-stu-id="a03c5-898">Description</span></span>                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a03c5-899"><span id="Games_for_Windows__Test_Cases__"></span><span id="games_for_windows__test_cases__"></span><span id="GAMES_FOR_WINDOWS__TEST_CASES__"></span>適用于 Windows 的遊戲：測試案例</span><span class="sxs-lookup"><span data-stu-id="a03c5-899"><span id="Games_for_Windows__Test_Cases__"></span><span id="games_for_windows__test_cases__"></span><span id="GAMES_FOR_WINDOWS__TEST_CASES__"></span>Games for Windows: Test Cases</span></span> <br/>                              | <span data-ttu-id="a03c5-900">Windows XP、Windows Vista 和 Windows 7 遊戲的最佳作法</span><span class="sxs-lookup"><span data-stu-id="a03c5-900">Best Practices for Games on Windows XP, Windows Vista, and Windows 7</span></span><br/>                                                                               |
| <span data-ttu-id="a03c5-901"><span id="Windows_SDK__"></span><span id="windows_sdk__"></span><span id="WINDOWS_SDK__"></span>Windows SDK</span><span class="sxs-lookup"><span data-stu-id="a03c5-901"><span id="Windows_SDK__"></span><span id="windows_sdk__"></span><span id="WINDOWS_SDK__"></span>Windows SDK</span></span> <br/>                                                                                                      | [<span data-ttu-id="a03c5-902">Windows Sdk</span><span class="sxs-lookup"><span data-stu-id="a03c5-902">Windows SDKs</span></span>](https://msdn.microsoft.com/bb980924.aspx)<br/>                                                                                      |
| <span data-ttu-id="a03c5-903"><span id="User_Account_Control_Guidelines__"></span><span id="user_account_control_guidelines__"></span><span id="USER_ACCOUNT_CONTROL_GUIDELINES__"></span>使用者帳戶控制指導方針</span><span class="sxs-lookup"><span data-stu-id="a03c5-903"><span id="User_Account_Control_Guidelines__"></span><span id="user_account_control_guidelines__"></span><span id="USER_ACCOUNT_CONTROL_GUIDELINES__"></span>User Account Control Guidelines</span></span> <br/>                      | <span data-ttu-id="a03c5-904">[使用者帳戶控制相容性的 Windows Vista 應用程式開發需求](/previous-versions/dotnet/articles/bb530410(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="a03c5-904">[Windows Vista Application Development Requirements for User Account Control Compatibility](/previous-versions/dotnet/articles/bb530410(v=msdn.10))</span></span><br/> |
| <span data-ttu-id="a03c5-905"><span id="WinQual_Developer_Portal__"></span><span id="winqual_developer_portal__"></span><span id="WINQUAL_DEVELOPER_PORTAL__"></span>WinQual 開發人員入口網站</span><span class="sxs-lookup"><span data-stu-id="a03c5-905"><span id="WinQual_Developer_Portal__"></span><span id="winqual_developer_portal__"></span><span id="WINQUAL_DEVELOPER_PORTAL__"></span>WinQual Developer Portal</span></span> <br/>                                                  | [<span data-ttu-id="a03c5-906">Windows Quality Online Services (Winqual) </span><span class="sxs-lookup"><span data-stu-id="a03c5-906">Windows Quality Online Services (Winqual)</span></span>](/windows-hardware/drivers/dashboard/winqual-submission-tool--winqualexe-)<br/>                                                                         |
| <span data-ttu-id="a03c5-907"><span id="DirectX_Developer_Portal__"></span><span id="directx_developer_portal__"></span><span id="DIRECTX_DEVELOPER_PORTAL__"></span>DirectX 開發人員入口網站</span><span class="sxs-lookup"><span data-stu-id="a03c5-907"><span id="DirectX_Developer_Portal__"></span><span id="directx_developer_portal__"></span><span id="DIRECTX_DEVELOPER_PORTAL__"></span>DirectX Developer Portal</span></span> <br/>                                                  | <span data-ttu-id="a03c5-908">[Directx 開發人員中心](/previous-versions/windows/apps/hh452744(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="a03c5-908">[Directx Developer Center](/previous-versions/windows/apps/hh452744(v=win.10))</span></span><br/>                                                                               |
| <span data-ttu-id="a03c5-909"><span id="Games_for_Windows_and_DirectX_SDK_Blog"></span><span id="games_for_windows_and_directx_sdk_blog"></span><span id="GAMES_FOR_WINDOWS_AND_DIRECTX_SDK_BLOG"></span>Windows 和 DirectX SDK Blog 的遊戲</span><span class="sxs-lookup"><span data-stu-id="a03c5-909"><span id="Games_for_Windows_and_DirectX_SDK_Blog"></span><span id="games_for_windows_and_directx_sdk_blog"></span><span id="GAMES_FOR_WINDOWS_AND_DIRECTX_SDK_BLOG"></span>Games for Windows and DirectX SDK Blog</span></span><br/> | [<span data-ttu-id="a03c5-910">適用於 Windows 與 DirectX SDK 的遊戲</span><span class="sxs-lookup"><span data-stu-id="a03c5-910">Games for Windows and the DirectX SDK</span></span>](https://walbourn.github.io/)<br/>                                                                           |
| <span data-ttu-id="a03c5-911"><span id="Additional_DirectX_Articles"></span><span id="additional_directx_articles"></span><span id="ADDITIONAL_DIRECTX_ARTICLES"></span>其他 DirectX 文章</span><span class="sxs-lookup"><span data-stu-id="a03c5-911"><span id="Additional_DirectX_Articles"></span><span id="additional_directx_articles"></span><span id="ADDITIONAL_DIRECTX_ARTICLES"></span>Additional DirectX Articles</span></span><br/>                                             | [<span data-ttu-id="a03c5-912">DirectX 技術文章</span><span class="sxs-lookup"><span data-stu-id="a03c5-912">DirectX Technical Articles</span></span>](/windows/desktop/DxTechArts/dx9-technical-articles)<br/>                                                                                    |



 

 


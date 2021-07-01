---
title: 適用於 Windows 的遊戲技術需求：Windows XP、Windows Vista、Windows 7 和 Windows 8 上遊戲的最佳作法
description: 本文提供在 Windows 上執行之遊戲的技術需求和最佳作法。
ms.assetid: 8b816e9f-de68-cf84-1501-a9c36c6b75d8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60c7a0f52685b0b99247ebfd86af3727d834ca63
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120303"
---
# <a name="games-for-windows-technical-requirements-best-practices-for-games-on-windows-xp-windows-vista-windows-7-and-windows-8"></a>Windows 技術需求的遊戲： Windows XP、Windows Vista、Windows 7 和 Windows 8 遊戲的最佳作法

本文提供在 Windows 上執行之遊戲的技術需求和最佳作法。 我們寫了這些技術需求和最佳作法，主要是用來涵蓋 Windows Vista 和 Windows 7，以及舊版 Windows XP 作業系統。 這些最佳作法通常也適用于 Windows 8 上的桌面 Win32 遊戲。

此文章包含下列各節：

-   [Windows 8 的差異](#differences-for-windows-8)
    -   [其他資訊](#additional-information)
-   [適用於 Windows 的遊戲](#games-for-windows-technical-requirements-best-practices-for-games-on-windows-xp-windows-vista-windows-7-and-windows-8)
    -   [1.1 遊戲瀏覽器整合](#11-games-explorer-integration)
    -   [1.2 支援家族安全性/家長監護控制項](/windows)
    -   [1.3 支援豐富的儲存遊戲](#13-support-rich-saved-games)
    -   [1.4 支援 Windows 條件式需求的 Xbox 360 通用控制器 \[\]](#14-support-the-xbox-360-common-controller-for-windows-conditional-requirement)
    -   [1.5 支援多種外觀比例和解析度](#15-support-multiple-aspect-ratios-and-resolutions)
    -   [1.6 支援從 Windows Media Center 啟動](#16-support-launch-from-windows-media-center)
    -   [1.7 Direct3D 支援](#17-direct3d-support)
    -   [1.8 啟用高 DPI 感知](#18-enable-high-dpi-aware)
-   [安全性與相容性](#security-and-compatibility)
    -   [2.1 遵循使用者帳戶控制指導方針](#21-follow-user-account-control-guidelines)
    -   [2.2 支援 Windows x64 版本](#22-support-windows-x64-versions)
    -   [2.3 簽署檔案](#23-sign-files)
    -   [2.4 簽署驅動程式](#24-sign-drivers)
    -   [2.5 執行適當的版本檢查](#25-perform-proper-version-checking)
    -   [2.6 支援並行使用者會話](#26-support-concurrent-user-sessions)
    -   [2.7 支援長名稱](#27-support-long-names)
-   [安裝](#32-support-user-account-control-for-installation)
    -   [3.1 支援輕鬆安裝](#31-support-easy-installation)
    -   [3.2 支援安裝的使用者帳戶控制](#32-support-user-account-control-for-installation)
    -   [3.3 安裝到正確的資料夾](#33-install-to-correct-folders)
    -   [3.4 正確安裝 Windows 資源](#34-install-windows-resources-properly)
    -   [3.5 避免在安裝期間重新開機](#35-avoid-reboots-during-installation)
    -   [3.6 使用正確的檔案版本控制](#36-use-file-versioning-correctly)
    -   [3.7 支援自動運行 \[ 條件需求\]](#37-support-autorun-conditional-requirement)
-   [可靠性](#reliability)
    -   [4.1 消除不必要的重新開機](#41-eliminate-unnecessary-reboots)
    -   [4.2 消除應用程式驗證器失敗](#42-eliminate-application-verifier-failures)
    -   [4.3 支援 Windows 錯誤報告和檔案版本資訊](#43-support-windows-error-reporting-and-file-version-information)
-   [適用于 Windows 的通用控制器 Xbox 360 術語](#xbox-360-common-controller-for-windows-terminology)
-   [遊戲中介軟體產品的指導方針](#guidelines-for-game-middleware-products)
    -   [簡介](#introduction)
    -   [其他建議](#additional-recommendations)
    -   [Windows 遊戲展示](#games-for-windows-showcases)
-   [資源](#resources)

## <a name="differences-for-windows-8"></a>Windows 8 的差異

以下是將這些技術需求和最佳作法套用 Windows 8 時的主要差異摘要。

<dl> <dt>

<span id="The_Games_Explorer_UI_is_not_visible"></span><span id="the_games_explorer_ui_is_not_visible"></span><span id="THE_GAMES_EXPLORER_UI_IS_NOT_VISIBLE"></span>**不顯示遊戲瀏覽器 UI**
</dt> <dd>

您在 [ [遊戲瀏覽器](/previous-versions/windows/desktop/legacy/hh437965(v=vs.85)) ] 中註冊的所有遊戲都會顯示為新的 Windows UI 中的圖格，但不會再顯示與該標題相關聯的許多中繼資料。 您仍然可以使用「遊戲定義檔案製造者」工具 (GDFMAKER.EXE) （現在可在 Windows 軟體開發套件 (SDK) 中取得）來撰寫中繼資料。 您也可以使用現有的機制來部署中繼資料。 繼續使用 Windows 7 測試您的遊戲瀏覽器註冊，然後確認新的 Windows UI 圖格會在安裝時出現 Windows 8 (請參閱 [1.1 遊戲瀏覽器整合](#11-games-explorer-integration)) 。

若要下載 Windows 8 SDK，請參閱 [開發桌面應用程式的下載](https://msdn.microsoft.com/windows/desktop/aa904949)。

</dd> <dt>

<span id="Registration_with_the_Game_Explorer_APIs_continues_to_be_the_mechanism_for_registering_your_game_with_Windows_Parental_Controls"></span><span id="registration_with_the_game_explorer_apis_continues_to_be_the_mechanism_for_registering_your_game_with_windows_parental_controls"></span><span id="REGISTRATION_WITH_THE_GAME_EXPLORER_APIS_CONTINUES_TO_BE_THE_MECHANISM_FOR_REGISTERING_YOUR_GAME_WITH_WINDOWS_PARENTAL_CONTROLS"></span>**使用遊戲瀏覽器 Api 進行註冊，仍是使用 Windows 家長監護註冊遊戲的機制**
</dt> <dd>

建議您在發行版本的 Windows 8 上執行 Windows SDK 版本的 GDFMAKER，以確保它可以填入所有目前支援的評等系統。

> [!Note]  
> 此版本的 GDFMAKER 需要 .NET 4.0。

 

請參閱 [1.2 支援系列的安全性/家長監護控制項](/windows)。

</dd> <dt>

<span id="There_are_now_three_choices_for_using_the_XINPUT_API_depending_on_your_requirements"></span><span id="there_are_now_three_choices_for_using_the_xinput_api_depending_on_your_requirements"></span><span id="THERE_ARE_NOW_THREE_CHOICES_FOR_USING_THE_XINPUT_API_DEPENDING_ON_YOUR_REQUIREMENTS"></span>**根據您的需求，現在有三個選項可供您使用 XINPUT API**
</dt> <dd>

XINPUT 1.4 內建于 Windows 8。 Windows Store 應用程式和桌面 Win32 應用程式都可以使用 XINPUT 1.4。 所有版本的 Windows 都可以針對簡化的通用控制器使用 XINPUT 9.1.0，但不含 XINPUT 9.1.0 的轉散發套件。 所有版本的 Windows 也都可以使用現有的 DirectX SDK 版本 XINPUT 1.3，這需要 DirectSetup 來部署。

請參閱 [1.4 支援適用于 Windows 的 Xbox 360 通用控制器](#14-support-the-xbox-360-common-controller-for-windows-conditional-requirement)。

</dd> <dt>

<span id="Only_a_limited_set_of_desktop_Win32_apps_are_supported_on_"></span><span id="only_a_limited_set_of_desktop_win32_apps_are_supported_on_"></span><span id="ONLY_A_LIMITED_SET_OF_DESKTOP_WIN32_APPS_ARE_SUPPORTED_ON_"></span>**Windows RT 僅支援一組有限的桌面 Win32 應用程式**
</dt> <dd>

在 Windows 7 上執行的遊戲可以，而且應該在 Windows 8 x86 和 x64 平臺上正確執行。

請參閱 [2.2 支援 Windows X64 版本](#22-support-windows-x64-versions)。

</dd> <dt>

<span id="Ensure_any_OS_checks_are_done_correctly"></span><span id="ensure_any_os_checks_are_done_correctly"></span><span id="ENSURE_ANY_OS_CHECKS_ARE_DONE_CORRECTLY"></span>**確定已正確完成任何作業系統檢查**
</dt> <dd>

Windows 8 作業系統版本為6.2。 Windows 8 會傳遞我們建議用於遊戲部署的最小條碼測試。

</dd> <dt>

<span id="The__DirectX_End-User_Redistribution__package_runs_successfully_on_Windows_8__as_it_does_on_Windows_7__to_deploy_D3DX9__D3DX10__D3DX11__XINPUT_1.3__XAUDIO_2.7__XACTEngine__and_so_on"></span><span id="the__directx_end-user_redistribution__package_runs_successfully_on_windows_8__as_it_does_on_windows_7__to_deploy_d3dx9__d3dx10__d3dx11__xinput_1.3__xaudio_2.7__xactengine__and_so_on"></span><span id="THE__DIRECTX_END-USER_REDISTRIBUTION__PACKAGE_RUNS_SUCCESSFULLY_ON_WINDOWS_8__AS_IT_DOES_ON_WINDOWS_7__TO_DEPLOY_D3DX9__D3DX10__D3DX11__XINPUT_1.3__XAUDIO_2.7__XACTENGINE__AND_SO_ON"></span>**DirectX End-User 轉散發套件會在 Windows 8 上順利執行，就像在 Windows 7 上一樣，以部署 D3DX9、D3DX10、D3DX11、XINPUT 1.3、XAUDIO 2.7、XACTEngine 等等。**
</dt> <dd>

但是，DirectSetup 在僅安裝 .NET 4.0 的系統上有一個已知的問題，因為部署處理舊版受管理的 DirectX 1.1 元件。 此問題適用于預設的 Windows 8 （預設為 .NET 4.5），以及已安裝 .NET 4.0 執行時間的全新 Windows XP 電腦。 但是，這個問題並不適用于 .NET 4.0 之前的任何 .NET 版本。 雖然 Windows 8 具有應用程式相容性行為，可自動解決此問題 (需要網路存取) ，但我們建議在2010年6月) 重新發行的可轉散發檔案版本中繼續部署 DirectSetup (更新的遊戲。 同樣地，如果您將 DirectSetup 用於您的標題，請將您的標題向下修剪為所需的最小一組 Cab。

請參閱 [3.4 正確安裝 Windows 資源](#34-install-windows-resources-properly)。

</dd> <dt>

<span id="Games_that_require_the_.NET__2.0__compatible_runtime__2.0__3.0__3.5__continue_to_use_existing_deployment_mechanisms"></span><span id="games_that_require_the_.net__2.0__compatible_runtime__2.0__3.0__3.5__continue_to_use_existing_deployment_mechanisms"></span><span id="GAMES_THAT_REQUIRE_THE_.NET__2.0__COMPATIBLE_RUNTIME__2.0__3.0__3.5__CONTINUE_TO_USE_EXISTING_DEPLOYMENT_MECHANISMS"></span>**需要 .NET 2.0 相容執行時間的遊戲 (2.0、3.0、3.5) 繼續使用現有的部署機制**
</dt> <dd>

這些遊戲會在 Windows 8 上觸發應用程式相容性行為，以自動啟用 .NET 3.5 執行時間 (需要網路存取) 。 但是，我們建議 .NET 開發人員移至 .NET 4.0 執行時間。

> [!Note]  
> 舊版受控 DirectX 1.1 元件與 .NET 4.x 執行時間不相容。

 

請參閱 [3.4 正確安裝 Windows 資源](#34-install-windows-resources-properly)。

</dd> <dt>

<span id="Use_of_an__autorunner__or_other_pre-install_technology_that_relies_on_.NET_is_not_recommended"></span><span id="use_of_an__autorunner__or_other_pre-install_technology_that_relies_on_.net_is_not_recommended"></span><span id="USE_OF_AN__AUTORUNNER__OR_OTHER_PRE-INSTALL_TECHNOLOGY_THAT_RELIES_ON_.NET_IS_NOT_RECOMMENDED"></span>**不建議使用依賴 .NET 的 autorunner 或其他預先安裝技術**
</dt> <dd>

您可以假設只有 .NET 2.0 相容的執行時間 (2.0、3.0、3.5) 出現在 Windows Vista 和 Windows 7 上。 根據預設，Windows 8 只有 .NET 4.0 相容的執行時間存在於。

請參閱 [3.7 支援自動運行](#37-support-autorun-conditional-requirement)。

</dd> <dt>

<span id="There_is_an_updated_Application_Verifier_for_Windows_8"></span><span id="there_is_an_updated_application_verifier_for_windows_8"></span><span id="THERE_IS_AN_UPDATED_APPLICATION_VERIFIER_FOR_WINDOWS_8"></span>**Windows 8 有更新的應用程式驗證器**
</dt> <dd>

Windows 8 SDK 包含這個更新的應用程式驗證器。

請參閱 [4.2 消除應用程式驗證器失敗](#42-eliminate-application-verifier-failures)。

</dd> </dl>

### <a name="additional-information"></a>其他資訊

<dl>

[Windows 8 和 Windows Server 2012 相容性操作手冊](/windows/desktop/w8cookbook/windows-8-and-windows-server-8-compatibility-cookbook-portal)  
[DirectX SDK 在哪裡？](/windows/desktop/directx-sdk--august-2009-)  
</dl>

## <a name="games-for-windows"></a>適用於 Windows 的遊戲

**遊戲需求摘要**

**客戶權益**

電腦遊戲是 Windows 的重要娛樂經驗，但容易使用的考慮導致客戶挫折多年。 傳統上，遊戲的安裝就像應用程式一樣，但使用的方式更像娛樂媒體 (電影或歌曲，例如) 。 創新，例如遊戲瀏覽器，以與標準應用程式不同的一致方式來公開遊戲。 這些創新也會在 Windows 中提供遊戲的第一級公民狀態，以及音樂和圖片。 下列需求有助於確保 Windows Vista 和 Windows 7 提供改良、更容易存取且整合的遊戲體驗。 同時也可確保與 Windows XP 的相容性。

### <a name="11-games-explorer-integration"></a>1.1 遊戲瀏覽器整合

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**要求**
</dt> <dd>

您必須在 Windows Vista 和 Windows 7 上的 [遊戲] 資料夾中，才能看到遊戲 **的 [遊戲** ] () 的遊戲。 選取時，遊戲也必須顯示正確的中繼資料，其中包括發行者、開發人員、發行日期、版本、Windows 體驗指數分數、評等 (適用的) 以及相關聯的超連結。

如果遊戲是透過線上遊戲服務進行數位分配，則服務提供者也應該會出現在 [遊戲] Explorer 中。 若要確保正確處理提供者並啟用 RSS 摘要，請使用第2版的遊戲定義檔架構 (GDFs) 應該使用。  (需 GDFs 的詳細資訊，請參閱其他資訊。 ) 

此外，當遊戲安裝程式在 Windows Vista 和 Windows 7 上執行時，必須遵守下列規則：

-   安裝不能建立快捷方式來啟動桌面、[開始] 功能表或任何其他位置中的遊戲。
-   不得建立移除的工作和快捷方式。
-   使用者必須能夠使用 Windows Vista 和 Windows 7 主控台的 [程式和功能] 來移除遊戲，或在 Windows XP 主控台的 [新增或移除程式] 中新增或移除程式。

在 Windows XP 和舊版的 Windows 上，遊戲安裝程式可以視需要建立程式群組、桌面圖示或快捷方式。

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**理由**
</dt> <dd>

Windows 遊戲瀏覽器的概念類似于 Windows XP 資料夾 **我的檔** 或 **我的圖片**。 其構想是將類似的內容集中在同一處，並讓組織和內容相關的活動更容易。 遊戲瀏覽器透過允許更豐富的組織和對遊戲的掌控，來擴充 **我的檔** 或 **我的圖片** 概念。 遊戲 Explorer 讓玩家能夠觀賞、組織及與系統上安裝的所有遊戲互動。 它也可讓遊戲發行者更有效率地傳達重要的遊戲資訊。 系統是資料驅動的，讓遊戲發行者很容易就能在產品的存留期更新遊戲資訊。

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**其他資訊**
</dt> <dd>

您必須撰寫遊戲定義檔案 (GDF) ，此檔案是內嵌于二進位檔案中的 XML 文字檔 (可執行檔或 DLL) 作為資源，以及 Windows 圖示。 然後遊戲必須向遊戲瀏覽器註冊。 GDF 也可讓您公開提供的資訊，例如遊戲標題、發行者、開發人員、網站連結和選擇性工作。 請注意，支援工作只能是網站的連結，但播放工作也可以用於選擇性的支援工作。

遊戲瀏覽器可以利用縮圖點陣圖影像，但建議您改為提供具有大型圖示的 Windows 圖示資源 (256 256) 。 圖示資源應包含 256 256 48 48、32 32 和 16 16 的影像大小（以24位 (True 色彩) 和8位 (256) 色深度）。 Visual Studio 2008 和2010中提供的圖示編輯器支援這些大型圖示格式，就像 IconWorkshop Lite 一樣。

DirectX SDK 提供與 **Windows 遊戲瀏覽器** 整合的詳細資料。 DirectX SDK 包含遊戲定義檔 (GDF) 編輯器，以及 GDFExampleBinary 中包含的範例 GDF 範例。 另一個範例 GameUxInstallHelper，提供將所需功能整合到現有安裝系統的常式。 遊戲定義檔驗證程式 (gdftrace.exe) 提供評估 GDF 的偵錯工具支援。 另請參閱 c + + 的 DirectX SDK 檔中的「Windows 遊戲瀏覽器整合」。

Windows 7 針對 GDF 檔案的架構推出了第二個版本的支援。 新的版本包含一種簡化的方法，可用於建立播放工作和支援更新通知、遊戲服務提供者、遊戲統計資料，以及適用于遊戲服務提供者的 RSS 摘要。 最新版本的 GameUxInstallHelper 會處理搭配 Windows Vista 使用第2版 GDF 檔案所需的所有註冊和舊版支援。 從2009年8月或更新版本的 DirectX SDK 使用工具和範例程式碼。 建議使用第2版 GDF 檔案來啟用 RSS 摘要、遊戲統計資料和更新通知的支援。 另請參閱範例 ProviderGDFExampleBinary 和 GameStatisticsExample。

在 windows Vista Business Edition、Windows 7 Professional Edition 及 Windows Vista 和 Windows 7 的企業版上，[開始] 功能表上的 [遊戲] 連結是隱藏的。 您仍然可以按一下 [ **所有程式**]，然後按一下 [ **遊戲**]，以在 [開始] 功能表上使用 [遊戲] Explorer。

對於隨遊戲安裝的相關聯應用程式，而不是自己的遊戲，您可以在所有 Windows 版本上自由建立 [開始] 功能表程式群組、快捷方式和桌面圖示，包括 Windows Vista 和 Windows 7。 這類相關聯的應用程式應通過適用于 Windows 需求的遊戲;如需詳細資訊，請參閱 [遊戲中介軟體產品的指導方針](#guidelines-for-game-middleware-products)。 建議您將遊戲服務註冊為 Windows 7 的遊戲提供者。 1

</dd> </dl>

### <a name="12-support-family-safety--parental-controls"></a>1.2 支援家族安全性/家長監護控制項

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**要求**
</dt> <dd>

遊戲必須遵守下列規則，以完全支援 Windows 家庭安全：

-   遊戲不需要使用者具有系統管理認證即可播放。 安裝、修補和移除可能需要系統管理認證，受限於第3節中的需求。  (與此相關的是需求2.1，請遵循使用者帳戶控制指導方針。 ) 
-   以 Windows 支援的評等面板（例如 ESRB 和 PEGI）分級的遊戲，必須在其遊戲定義檔中包含其指派的評等資訊 (GDF) 。 所有可用的評等資料都必須包含在每個當地語系化版本的 GDF 中，也必須包含在非語言相關的版本中。
-   遊戲必須在 GDF 中列出他們的可執行檔，以提供一般應用程式限制的良好使用者體驗，除非遊戲使用反盜版技術，在執行時間建立隨機命名的可執行檔。
-   遊戲必須在啟動時呼叫遊戲瀏覽器介面的 **VerifyAccess** 方法（如果有的話），並在其傳回 \* pfHasAccess 為 FALSE 時結束。

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**理由**
</dt> <dd>

所有遊戲都必須在標準使用者帳戶的內容中執行，以允許由 Windows 家長監護控制的帳戶播放遊戲。 家長希望能夠監視和控制其子系對遊戲的存取。 此外，許多產業、政府和倡議團隊希望有更好的方式來允許家長監視和控制其子女所公開的遊戲。 Microsoft 與遊戲瀏覽器所提供的架構結合，提供了透過 Windows 家長監護的這項功能。

即使是未參與評等的遊戲，也需要較高的許可權，才能為大部分的使用者帳戶建立不佳的播放體驗。 尤其是在啟用家長監護的情況下，在每次啟動遊戲時都需要父系輸入系統管理員密碼。

Windows 家長監護系統可讓父系選取他們認為適用于其子系的評等。 家長監護支援許多全球評量系統。 家長監護也可讓家長根據內容描述項來限制對遊戲的存取 (如果適用的評等系統支援) ，並允許或禁止存取個別的遊戲。

Windows 家長監護的預設分級系統選項是以系統的地區設定為基礎，但可由使用者在 **主控台** 的 [**地區及語言選項**] 中進行修改。 因此，每個支援的語言都應該提供所有可用的分級資料，讓使用者可以自由地選取他們想要的任何評等面板。

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**其他資訊**
</dt> <dd>

沒有評等的遊戲仍然必須符合需求，才能以標準使用者的形式播放和呼叫 **VerifyAccess**。 這類遊戲預設為未分級的類別，在 [遊戲瀏覽器] 中顯示「未提供評等」文字，並且受限於未分級遊戲之 **家長** 監護中的 **遊戲限制** 設定。 預設 **限制** 設定為 [允許]。

如果包含的二進位檔未經過正確的 Authenticode 簽署，則會忽略 GDF 中的評等資訊。 請參閱需求2.3。

DirectX SDK 中的遊戲定義檔編輯器包含所有支援的評等系統，並會正確地將此資訊複寫到 GDF 的所有當地語系化版本，以及非語言相關版本。 GDFTrace 工具將會解碼並確認目前有所有評等資訊。 使用這些工具的2009年8月版本或更新版本。

遊戲提供者的 GDF 通常不會包含評等資訊，而且會受限於未分級內容的設定。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>作業系統</th>
<th>支援的評等系統</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Windows Vista</td>
<td><ul>
<li>CERO (日本) </li>
<li>ESRB (USA) </li>
<li>OFLC (澳大利亞) </li>
<li>PEGI (歐洲) </li>
<li>PEGI 芬蘭 (已淘汰) </li>
<li>PEGI 葡萄牙</li>
<li>PEGI/BBFC (英國) </li>
<li>USK (德國) </li>
</ul></td>
</tr>
<tr class="even">
<td>Windows Vista （含 service pack）</td>
<td>適用于 Windows Vista 的 Service pack 新增下列支援：<br/>
<ul>
<li>GRB (南韓國) </li>
<li>ESRB &quot; 輕度的 &quot; 變異內容描述項</li>
</ul></td>
</tr>
<tr class="odd">
<td>Windows 7</td>
<td>Windows 7 支援 Windows Vista 支援的分級系統，並新增下列支援： <br/>
<ul>
<li>CSRR (臺灣) </li>
</ul></td>
</tr>
<tr class="even">
<td>Windows 8</td>
<td>Windows 8 支援先前的分級系統，並新增下列支援：<br/>
<ul>
<li>COB-澳大利亞 (澳大利亞) </li>
<li>DJCTQ (巴西) </li>
<li>PFB (南非) </li>
<li>OFLC-NZ (紐西蘭) </li>
</ul>
Windows 8 淘汰下列現已淘汰的系統支援：<br/>
<ul>
<li>PEGI-FI (芬蘭) </li>
<li>OFLC (澳大利亞) </li>
</ul></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> 包含新 ESRB 的 Windows Vista Service Pack 1 (SP1) 內容描述項的任何標題，在不含 Service Pack 的 Windows Vista 上會顯示為未分級。

 

在不支援的作業系統版本上，會忽略較新的分級資料。 PEGI (芬蘭) 變異現在已被取代為標準 PEGI (歐洲) 評等系統。 OFLC 系統現在已淘汰，可改用適用于澳大利亞的 COB-AU。

如需有關使遊戲與標準使用者權限相容的詳細資訊，請參閱 [適用于遊戲開發人員的 DirectX 文章使用者帳戶控制](/windows/desktop/DxTechArts/user-account-control-for-game-developers)。

如需遊戲定義檔 (GDF) 的詳細資訊，請參閱需求1.1。

</dd> </dl>

### <a name="13-support-rich-saved-games"></a>1.3 支援豐富的儲存遊戲

\[這項需求已淘汰\]

### <a name="14-support-the-xbox-360-common-controller-for-windows-conditional-requirement"></a>1.4 支援 Windows 條件式需求的 Xbox 360 通用控制器 \[\]

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**要求**
</dt> <dd>

支援遊戲台控制器的遊戲必須支援使用 [XInput](/windows/desktop/xinput/xinput-game-controller-apis-portal) API 的適用于 Windows 的 Xbox 360 控制器。 如果也支援 DirectInput 周邊，則也可以使用 DirectInput。 但是，如果使用 Xbox 360 相容裝置，XInput 必須是預設的 API。

所有對通用控制器觸發程式和按鈕的參考都必須使用 Xbox 360 名稱。 如需詳細資訊，請參閱 [Xbox 360 Windows 術語的通用控制器](#xbox-360-common-controller-for-windows-terminology) 清單。

當遊戲處於暫停或暫停狀態時，控制器振動必須關閉。

滑鼠/鍵盤控制項隨時都不能完全停用。 至少要有一個選項可用來返回遊戲功能表。

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**理由**
</dt> <dd>

這項需求讓玩家可以自由選擇使用 Xbox 360 控制器或鍵盤和滑鼠，這取決於哪些輸入方法是更自然且直覺的介面。

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**其他資訊**
</dt> <dd>

這項需求並不適用于使用滑鼠和/或鍵盤的遊戲。

建議您將功能表導覽實作為使用廣泛接受的標準控制器按鈕：

-   A-接受
-   B-取消
-   開始-接受或暫停
-   返回-取消、返回一個畫面或開啟功能表層級

如需詳細資訊，請參閱 [XInput](/windows/desktop/xinput/xinput-game-controller-apis-portal)。

[XInput 和 DirectInput](/windows/desktop/xinput/xinput-and-directinput)主題會討論同時使用這兩個 api 的問題。

建議您不要使用 DirectInput 來執行鍵盤或滑鼠控制項。 鍵盤和滑鼠控制項應僅使用 Windows 訊息和 Win32 Api 來執行。 如需有關如何在不使用 DirectInput 的情況下取得高解析度滑鼠移動資訊的詳細資訊，請參閱 [利用 High-Definition 滑鼠移動](/windows/desktop/DxTechArts/taking-advantage-of-high-dpi-mouse-movement)。

</dd> </dl>

### <a name="15-support-multiple-aspect-ratios-and-resolutions"></a>1.5 支援多種外觀比例和解析度

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**要求**
</dt> <dd>

遊戲必須至少支援下列外觀比例和相關聯的螢幕解析度：

-   4:3 標準 (800 600 或 1024 768) 
-   16:9 寬銀幕 (1280 720) 
-   16:10 寬銀幕 (1152 720 或 1680 1050 或 800 480) 

若要進行螢幕解析度設定和偵測，遊戲必須遵守下列規則：

-   如果是支援的解決方案，遊戲預設會使用顯示裝置的桌面解析度。 如果遊戲選擇不同的預設解析度，就必須使用桌面外觀比例作為搜尋準則。
-   當進行變更時，遊戲必須提示使用者確認新的顯示設定。 如果使用者未在15秒內接受，則顯示必須還原為先前的設定。
-   遊戲不得延展圖元或置中4:3 轉譯視窗，以支援寬螢幕外觀比例。 不過，上下黑邊縮是可接受的。

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**理由**
</dt> <dd>

使用 Windows 3D desktop 時，無法假設特定的外觀比例或解析度，原因如下：

-   支援高詳細資料顯示。
-   增加寬螢幕顯示器的市場份額。
-   Windows Media Center 的 HDTV 部署。
-   協助工具需求。

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**其他資訊**
</dt> <dd>

在理想的情況下，遊戲預設為顯示的原生外觀比例。 不過，可靠地取得這項資訊可能是一項挑戰，因此，如果是更一般的解決方案，遊戲可以假設桌面是以原生的外觀比例執行。 藉由呼叫 [**EnumDisplaySettings**](/windows/desktop/api/winuser/nf-winuser-enumdisplaysettingsa) 與列舉登錄設定，即可取得桌面解析度 \_ \_ 。

如需更多詳細資訊，請參閱 DirectX 文章的外觀比例和寬螢幕區段， [介紹 Windows 遊戲開發人員的10英尺體驗](/windows/desktop/DxTechArts/introduction-to-the-10-foot-experience-for-windows-game-developers)。

</dd> </dl>

### <a name="16-support-launch-from-windows-media-center"></a>1.6 支援從 Windows Media Center 啟動

\[這項需求已淘汰。\]

### <a name="17-direct3d-support"></a>1.7 Direct3D 支援

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**要求**
</dt> <dd>

如果遊戲使用 Direct3D，則支援的最低版本必須是 Direct3D 9，而且 Direct3D 必須是選取的預設轉譯器。

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**理由**
</dt> <dd>

Windows Vista 和 Windows 7 core 圖形架構是以 Direct3D 為中心所設計。 重新對應舊版介面可支援 Direct3D 8 和更早版本。

強烈建議使用比 Direct3D 9 更新的 Direct3D 版本。 查看 Windows 展示的遊戲。1。 需要 Direct3D 10 或 Direct3D 11 完全符合需求1.7 的規範。

</dd> </dl>

### <a name="18-enable-high-dpi-aware"></a>1.8 啟用高 DPI 感知

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**要求**
</dt> <dd>

)  (當您在 Windows Vista 和 Windows 7 上以 1600 1200) 的顯示解析度進行調整時，遊戲及其安裝 144 (程式必須在沒有視覺問題150的情況下正確執行。

這通常需要遊戲可執行檔宣告為 DPI 感知。 這是藉由內嵌資訊清單元素來達成： <dpiAware> true <dpiAware> 。

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**理由**
</dt> <dd>

高品質的 LCD 監視器在電腦顯示時很常見，而且在以原生解析度驅動的情況下，它們的外觀最好 (通常是 1280 1024、1600 1200 等) 。 如果客戶難以閱讀文字，並以此解析度查看影像，通常會將其電腦桌面設定為較低的解析度，並讓視覺構件免于 LCD 調整。 相反地，客戶可以保留原生大小的解析度，並變更 Windows 顯示器的 DPI，使專案和文字外觀更大，而不會犧牲影像品質。

雖然這項功能在 Windows XP 之後已經以某種形式提供，但是客戶或 Oem 很少會啟用它。 現今所有電腦顯示的一半，會根據客戶的意見反應，設定為比監視器原生解析度更低的解析度。 在初始設定期間，以及變更顯示設定時，Windows 7 會讓客戶更容易看到這項功能，而不需要變更桌面解析度。

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**其他資訊**
</dt> <dd>

如果在處理常式啟動程式碼中提早呼叫 [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) 函式，則可以改為使用。 建議您將新增至資訊清單，以確保在呼叫主要進入點之前，可能會初始化的 (的) 軟體元素沒有任何競爭情形。 請注意， **SetProcessDPIAware** 只存在於 windows Vista 和 windows 7。

使用 Visual Studio 2005 和2008可輕鬆地新增資訊清單元素;建立名為 DPIaware 的檔案，其中包含下列文字：

``` syntax
            <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
            <asmv3:application>
            <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2005/WindowsSettings">
            <dpiAware>true</dpiAware>
            </asmv3:windowsSettings>
            </asmv3:application>
            </assembly>
```

然後，在 Visual Studio 中，將 DPIware 加入至專案。 確定專案屬性中的 **內嵌資訊清單** 設定為 **[是]** 。 請注意，舊版的資訊清單工具 (Mt.exe) 將會使用 DPI 感知的資訊清單元素來產生假警告。 若要解決此問題，請從 Windows SDK 將 Mt.exe 更新為最新版本。

Visual Studio 2010 包含專案屬性中的設定，名為 **啟用 DPI 感知**，因此不需要 DPIaware 檔案。 展開 [設定 **屬性**] 和 [**資訊清單] 工具**，然後選取 [**輸入 & 輸出**]，即可尋找 **啟用 DPI 感知**。

在 Windows 上，傳統顯示模式的預設值為 96 DPI，這常見於 CRT 監視器。

當全螢幕應用程式變更顯示解析度時，它們通常會在設定緩衝區和顯示矩形時使用視窗訊息和度量。 DPI 虛擬化會將這些全螢幕顯示模式顯示為已裁剪，並宣告 DPI 感知，以防止這些問題。 如需詳細資訊，請參閱 [撰寫 DPI-Aware 的 Win32 應用程式](../hidpi/high-dpi-desktop-application-development-on-windows.md)。

</dd> </dl>

## <a name="security-and-compatibility"></a>安全性與相容性

**安全性與相容性需求的摘要**

**客戶權益**

下列需求可改善遊戲的整體安全性，並協助確保它們能在不同的架構上、不同的設定下和不同的模式下使用 Windows。

### <a name="21-follow-user-account-control-guidelines"></a>2.1 遵循使用者帳戶控制指導方針

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**要求**
</dt> <dd>

每個可執行檔 (也就是每個具有 .exe 副檔名) 的檔案都必須包含內嵌的資訊清單，藉由包含下列標記來定義其執行層級：

``` syntax
            <requestedExecutionLevel>
```

根據需求1.2，主要遊戲和自動執行執行檔必須具有 asInvoker 的執行層級，才能支援標準使用者內容。

具有向 **檔案總管** 註冊之檔案關聯的使用者資料檔案，必須放在 CSIDL PERSONAL (所指定的資料夾子資料夾中，也稱為 [檔] \_ 或 [**我的檔**) ]。  所有其他的使用者資料檔案都必須儲存在 CSIDL \_ LOCAL \_ APPDATA 或 CSIDL \_ COMMON APPDATA 所指定之資料夾的子資料夾中 \_ 。 針對個別使用者和所有使用者，預設會隱藏這些目錄 (。 ) 

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**理由**
</dt> <dd>

如果應用程式只執行所需的許可權，則使用者的 Windows 體驗會更安全。

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**其他資訊**
</dt> <dd>

如果應用程式中只有幾項功能需要系統管理許可權 (例如，需要設定防火牆) 的應用程式，則必須使用標準使用者權限來執行應用程式的主要處理常式。 需要系統管理許可權的功能必須移至個別的進程，例如安裝程式或設定公用程式。

如果不需要系統管理許可權，內嵌的資訊清單 XML 應該包含下列內容：

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

如果需要系統管理許可權，內嵌的資訊清單 XML 應該包含下列內容：

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

使用 Visual Studio 2005，只要將包含上述其中一個區塊的資訊清單 () 資訊清單新增至專案，即可輕鬆地內嵌，並確保在資訊清單工具的專案屬性中， **內嵌資訊清單** 設定為 **[是]** 。 針對 Visual Studio 2008 和2010，可以直接在 **資訊清單** 檔案頁面上連結器的專案屬性中設定 UAC 屬性。 請注意，舊版的資訊清單工具 (Mt.exe) 會產生含有 UAC 資訊清單元素的偽造警告。 若要解決此問題，請從 Windows SDK 將 Mt.exe 更新為最新版本。

如需安裝、修補和移除等特殊案例的詳細資訊，請參閱需求3.1。

動態連結程式庫 (Dll) 不需要這類資訊清單。

如需使用者帳戶控制的詳細資訊，請參閱 [遊戲開發人員的使用者帳戶控制](/windows/desktop/DxTechArts/user-account-control-for-game-developers)。

</dd> </dl>

### <a name="22-support-windows-x64-versions"></a>2.2 支援 Windows x64 版本

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**要求**
</dt> <dd>

為了維持與64位 Windows 版本的相容性，遊戲應符合下列需求。

-   標題和標題安裝程式不得包含任何16位程式碼，或依賴任何16位元件。
-   如果遊戲相依于操作的核心模式驅動程式，則必須提供這些驅動程式的 x64 版本。 遊戲安裝程式必須偵測並安裝適用于64位版本 Windows 的適當驅動程式和元件。

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**理由**
</dt> <dd>

許多 Windows Vista 和 Windows 7 使用者將會在產品的存留期內執行64位版本的作業系統，因此應用程式必須與此作業系統相容。

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**其他資訊**
</dt> <dd>

Windows on Windows 64 (WOW64) 可讓32位程式碼在64位版本的 Windows 上執行，因此應用程式不需要在 Windows 的64版本上為原生64位程式碼。 十六位程式碼不會在64位版本的 Windows 上執行。

維持與 Windows XP Professional x64 Edition 的相容性並不是必要的，但強烈建議您這樣做。

如需詳細資訊，請參閱 [遊戲開發人員的64位程式設計](/windows/desktop/DxTechArts/sixty-four-bit-programming-for-game-developers)。

</dd> </dl>

### <a name="23-sign-files"></a>2.3 簽署檔案

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**要求**
</dt> <dd>

所有可執行程式碼檔案 (通常是具有副檔名 .exe 或 .dll) 的檔案必須使用公開有效的 Authenticode 憑證進行簽署，而且必須具有有效的時間戳記伺服器 URL，才能進行生產簽署。

如果您的遊戲使用 Windows Installer，) 必須簽署安裝程式套件檔案 (.msi 檔案。

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**理由**
</dt> <dd>

簽署檔案可協助使用者決定是否信任應用程式，並確保使用者不會遭篡改。 它也可讓應用程式在鎖定的環境中正確執行。

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**其他資訊**
</dt> <dd>

如需詳細資訊，請參閱 [遊戲開發人員的 Authenticode 簽署](/windows/desktop/DxTechArts/authenticode-signing-for-game-developers)。

如果您的遊戲使用 Windows Installer，建議您加入 MsiPatchCertificate 資料表，以啟用 UAC/LUA 修補。 如需詳細資訊，請參閱 [ (UAC) 修補的使用者帳戶控制](/windows/desktop/Msi/user-account-control--uac--patching)。

除非 (.cab) 的檔案相對較 100 (小，否則我們不建議將它簽署檔案，) 。

</dd> </dl>

### <a name="24-sign-drivers"></a>2.4 簽署驅動程式

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**要求**
</dt> <dd>

遊戲所安裝的任何核心模式驅動程式都必須使用公開有效的 Authenticode 憑證進行簽署。

遊戲所安裝的任何核心模式硬體設備磁碟機都必須有 Microsoft 簽章，您可以從 Windows 硬體品質實驗室 (WHQL) 或從驅動程式可靠性簽章 (DRS) 程式取得該簽章。

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**理由**
</dt> <dd>

寫入不良或惡意程式碼的驅動程式可能會嚴重影響系統的穩定性和安全性。 在 Windows Vista 和 Windows 7 的64位版本上，不會載入未簽署的驅動程式。 這項原則也可以針對32位版本的 Windows Vista 和 Windows 7 啟用。

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**其他資訊**
</dt> <dd>

每項需求2.2 都需要32位和64位原生版本的所有核心模式驅動程式。

如需 Microsoft 驅動程式簽署計畫的詳細資訊，請參閱 [Windows 硬體開發人員入口網站](https://www.microsoft.com/whdc/winlogo/hwrequirements.mspx)。

</dd> </dl>

### <a name="25-perform-proper-version-checking"></a>2.5 執行適當的版本檢查

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**要求**
</dt> <dd>

除非使用者授權合約禁止在未來的作業系統上使用，否則遊戲不能在未來的作業系統上執行，如 Windows 版本號碼的變更所述。 如果遊戲應該會失敗，就必須向使用者顯示適當的訊息，以正常方式進行。

如果進行 Windows 版本檢查，則必須使用版本檢查 Api ([**GetVersionEx**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getversionexa) 或 [**VerifyVersionInfo**](/windows/desktop/api/winbase/nf-winbase-verifyversioninfoa)) 來檢查作業系統版本。 不得讀取登錄機碼來判斷版本。

DirectX 執行時間的明確版本檢查不能出現在遊戲中。 這些版本檢查不能出現在啟動 DirectX runtime 安裝程式 (DirectSetup) 的安裝中。

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**理由**
</dt> <dd>

當 Windows 使用者升級其作業系統時，不應該將它們封鎖為無法播放目前的遊戲，因為 Windows 版本號碼已增加。 撰寫不當的版本檢查程式會繼續產生軟體的問題，否則，在較新版本的 Windows 上，或只是加入 Windows service pack，都能正常運作。

在不同版本的 Windows 上執行時，DirectX runtime 的脆弱版本檢查比較邏輯已建立許多失敗的安裝。 DirectX 版本號碼只適用于核心作業系統元件。 它並不適用于許多遊戲所使用的並存 DirectX SDK 元件。

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**其他資訊**
</dt> <dd>

最常見的情況是查看安裝程式檢查是否有最低的 OS 版本。 不過，這項檢查必須小心完成，以確保其測試是否大於或等於，而不是簡單相等，進而鎖定特定版本的作業系統。 使用應用程式驗證器的 **HighVersionLie** 測試是一種快速又簡單的方式，可判斷安裝程式將如何回應作業系統版本號碼的重大變更。

 (DirectX 安裝程式) 適當地使用 DirectX 執行時間轉散發套件時，必須在安裝期間一律啟動它，最好是以無訊息模式執行。 這可讓 Microsoft 提供的程式碼執行任何必要的版本更新。 它也可讓您安裝任何選用的並存 DirectX SDK 元件，例如 D3DX、交易、MDX 或 XInput。

如需部署 DirectX 執行時間的最佳作法，請參閱 [遊戲開發人員的 Directx 安裝](/windows/desktop/DxTechArts/directx-setup-for-game-developers)。

建議支援 Windows XP 的遊戲檢查2或更高版本的 service pack 層級，因為 Service Pack 2 (SP2) 和 Service Pack 3 (SP3) 提供大幅的安全性改良功能、簡化的 DirectX 執行時間轉散發需求，以及極廣泛的部署。 大部分支援 Windows XP 的新式 Microsoft 技術都需要 SP2 或 SP3 (XAudio2、Windows LIVE 的遊戲，以及) 。

</dd> </dl>

### <a name="26-support-concurrent-user-sessions"></a>2.6 支援並行使用者會話

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**要求**
</dt> <dd>

依賴3D 圖形的遊戲不需要透過遠端桌面連線來運作，但使用者必須在遊戲失敗時收到警示。

遊戲必須遵守下列規則，以支援標準 Windows 多工案例：

-   遊戲不得封鎖並行使用者會話的使用。
-   當遊戲已在另一個會話中執行時，必須在新的使用者會話中執行遊戲。
-   當另一個使用者在不同的會話中處於作用中狀態時，就不能聽到一個使用者會話中的遊戲音效。
-   遊戲必須支援快速切換使用者。
-   遊戲不得嘗試停用標準工作切換。 遊戲不得停用 ALT + TAB 鍵盤快捷方式。 允許遊戲停用輔助功能鍵盤快捷方式，如在 [遊戲中停用快速鍵](/windows/desktop/DxTechArts/disabling-shortcut-keys-in-games)所述。

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**理由**
</dt> <dd>

Windows 使用者應該能夠在不發生衝突或中斷的情況下執行並行會話。 這是家庭、室友或其他人共用之 Windows 電腦的常見案例。

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**其他資訊**
</dt> <dd>

若要測試遊戲是否在遠端會話中啟動，請 ([](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) SM \_ REMOTESESSION) 呼叫 GetSystemMetrics。 非零值表示會話為遠端。

如需詳細資訊，請參閱 [快速切換使用者](/windows-hardware/drivers/display/fast-user-switching)。 請注意，如果在使用者的時間已啟動時，[家長監護] 會啟用 [快速切換使用者]。 如需詳細資訊，請參閱需求1.2。

</dd> </dl>

### <a name="27-support-long-names"></a>2.7 支援長名稱

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**要求**
</dt> <dd>

如果遊戲支援儲存檔案，它必須能夠儲存具有完整名稱和路徑的檔案。 遊戲必須適當地處理特殊檔案系統字元，例如 \\ /： \* ？ " < >，在用來建立檔案名或路徑的任何使用者輸入欄位中。

當使用者具有較長的使用者名稱時，遊戲必須能夠正常運作。

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**理由**
</dt> <dd>

播放程式習慣在基礎作業系統所支援的深層路徑上使用完整名稱。

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**其他資訊**
</dt> <dd>

完整名稱定義為包含 Windows SDK 中定義之最大值的名稱。

</dd> </dl>

## <a name="installation"></a>安裝

**安全性與相容性需求的摘要**

**客戶權益**

客戶可以放心地在 Windows 上安裝應用程式，而不會降低作業系統或其他應用程式（如果應用程式使用官方系統元件散發方法）。 簡化的安裝體驗可為遊戲提供更容易存取和無障礙的現成體驗。

### <a name="31-support-easy-installation"></a>3.1 支援輕鬆安裝

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**要求**
</dt> <dd>

遊戲必須執行下列動作，在安裝程式使用者介面中提供簡化的路徑：

-   顯示最多一個 EULA 提示字元。
-   預設安裝路徑必須略過安裝 (的所有選取專案，例如安裝資料夾或元件選項) 、假設預設選項，然後在安裝成功時執行遊戲或啟動器，而不需要額外的提示。 如有需要，可以為 advanced configuration 選項提供自訂安裝選項。
-   安裝任何必要的作業系統元件 (例如 DirectX 和 Visual C 執行時間，) 使用正確的 Microsoft 轉散發套件。 安裝應該以無訊息模式執行，而不需要提示，也不會受到元件版本檢查的保護。
-   透過 **主控台** 中的 **程式和功能**，為遊戲應用程式和產生的工作檔案提供移除。 建議刪除使用者所建立之任何資料檔案的選項。 移除程式必須確定已移除所有已安裝的檔案，而且所有設定 (例如，已清除防火牆例外清單專案和登錄機碼) 。 重新發佈的作業系統元件不得移除。
-   如果遊戲需要將例外狀況新增至 Windows 防火牆，安裝程式會提示您通知使用者需要進行這項變更。 安裝開始之前，應該會出現此提示。

安裝和移除可能需要系統管理許可權。 視更新的頻率而定，修補程式可能需要提示輸入系統管理認證。 遊戲的正常播放不得要求系統管理許可權，每項需求2.1 都遵循使用者帳戶控制指導方針。

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**理由**
</dt> <dd>

Easy 安裝是以 Windows 為中心的遊戲開發原理，其設計目的是要簡化並簡化在執行 Windows 作業系統的電腦上安裝遊戲的繁瑣和混淆程式。 您可以利用一組技術和最佳作法來啟用輕鬆安裝，以降低在 Windows 電腦上安裝遊戲的不必要複雜度和認知風險。

主要目標是：

-   縮短進入遊戲的時間，然後開始玩遊戲。
-   將對話方塊和選項數目減少為極少或無，以簡化遊戲安裝體驗。

某些傳統安裝具有允許非功能性安裝的提示，即使應用程式看似成功安裝也一樣。 例如，遊戲可能需要使用者接受 EULA。 接著會安裝該遊戲，然後會出現 DirectX EULA。 此 EULA 可讓使用者拒絕安裝 DirectX 執行時間，並因此略過安裝。 這種情況可能會導致遊戲因為遺失元件而無法執行。

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**其他資訊**
</dt> <dd>

如需有關遊戲安裝、非傳統的遊戲安裝技術、UAC 相容的修補解決方案，以及處理頻繁修補的詳細資訊，請參閱下列 DirectX 文章：

-   [簡化遊戲安裝](/windows/desktop/DxTechArts/simplifying-game-installation)
-   [適用于遊戲的隨選安裝](/windows/desktop/DxTechArts/install-on-demand-for-games)
-   [在 Windows XP、Windows Vista 和 Windows 7 中修補遊戲軟體](/windows/desktop/DxTechArts/patching-methods-in-windows-xp-and-vista)
-   [大量多人連線遊戲的安裝最佳做法](/windows/desktop/DxTechArts/mmo-installation-best-practices)

> [!Note]  
> 只應針對目前的使用者和一般的共用使用者位置，移除使用者特定產生的資料檔案。 即使移除需要系統管理認證，仍沒有健全的方式可掃描系統，以移除其他使用者的使用者特定檔案。

 

</dd> </dl>

### <a name="32-support-user-account-control-for-installation"></a>3.2 支援安裝的使用者帳戶控制

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**要求**
</dt> <dd>

遊戲安裝程式不得假設它是在與使用者相同的內容中執行。 使用者專屬的位置會與安裝程式和播放機不同，即使是針對單一使用者系統，也是因為系統管理員認證提高許可權。 因此，當遊戲第一次執行時，它必須與安裝程式分開執行使用者特定的工作。

當使用者裝載或加入多人遊戲時，不能出現 [Windows 防火牆例外] 對話方塊。 您必須在安裝時完成任何必要的設定。 安裝指示應該會通知使用者，這項作業將會在安裝過程中發生。

遊戲安裝程式必須提供內嵌的資訊清單，以根據需求2.1 遵循使用者帳戶控制指導方針，來指定所需的執行層級。

如果安裝程式完成之後，安裝程式啟動遊戲，則必須在原始使用者的內容中啟動。

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**理由**
</dt> <dd>

Windows Vista 中的 Windows 作業系統最大的變更之一，就是新增使用者帳戶控制 (UAC) ，預設會以較少的許可權來執行應用程式。 因此，安裝程式必須據以管理許可權等級。 Windows 7 也會大量使用 UAC。 雖然 Windows 7 改善了 UAC 的使用者體驗，但安裝程式仍然必須符合 Windows Vista 的相同需求，才能正常運作，而不需要依賴可能混淆的虛擬化行為。

在 Windows Vista 和 Windows 7 上，UAC 預設為使用中，而大部分的客戶 (88% 或更多，根據意見反應) 讓此功能保持啟用狀態。

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**其他資訊**
</dt> <dd>

如需設定 Windows 防火牆的詳細資訊，請參閱 [適用于遊戲開發人員的 Windows 防火牆](/windows/desktop/DxTechArts/games-and-firewalls) 和 FirewallInstallHelper 範例的 DirectX 文章。

如果安裝是由標準使用者啟動，而且安裝程式需要系統管理許可權 (也就是，在安裝程式結束時，標準啟動遊戲無法符合此需求的最後一個部分，也就是提示您輸入系統管理員認證) 。 它也會繼承系統管理許可權，這是潛在的安全性風險。 相反地，安裝程式啟動載入器應該會在從安裝程式成功調用後啟動遊戲。 如需詳細資訊，請參閱 MSDN 雜誌文章： [教您的應用程式使用 Windows Vista 使用者帳戶控制順利播放](/archive/msdn-magazine/2007/january/teach-your-apps-to-work-with-windows-vista-user-account-control)。

</dd> </dl>

### <a name="33-install-to-correct-folders"></a>3.3 安裝到正確的資料夾

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**要求**
</dt> <dd>

依預設，針對所有使用者安裝的遊戲都必須安裝至 Program Files 資料夾。 當遊戲第一次執行時，您必須撰寫使用者資料，而不是在安裝期間寫入。

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**理由**
</dt> <dd>

使用者應該能夠彈性地在需要的位置安裝應用程式。 它們也應該具有一致且安全的體驗，以及檔案的預設位置。

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**其他資訊**
</dt> <dd>

遊戲可利用各種已知的資料夾位置 (例如，CSIDL \_ LOCAL \_ APPDATA 和 CSIDL COMMON) APPDATA 所指定的位置， \_ \_ 以儲存大量的遊戲資料和支援的可執行檔，以執行先進的隨選安裝和修補案例。

因為安裝可能需要在所有使用者安裝程式期間提升至不同的使用者帳戶，所以在安裝時不會有正確的使用者位置來儲存資料。 此外，如果已啟用檔案加密，加密的檔案只能由建立它們的使用者帳戶存取。

</dd> </dl>

### <a name="34-install-windows-resources-properly"></a>3.4 正確安裝 Windows 資源

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**要求**
</dt> <dd>

應用程式不能嘗試安裝受 Windows 資源保護 (WRP) 保護的檔案或登錄機碼。 如果應用程式需要較新版本的系統元件，則必須使用 Microsoft Service Pack 或包含系統元件的 Microsoft 核准安裝套件來更新這些元件。 系統元件絕對不能重新封裝。

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**理由**
</dt> <dd>

Windows 資源保護 (WRP) 的設計目的，是要確保只有使用 Microsoft 核准的安裝或更新機制，才能更新受保護的系統資源。 WRP 可確保安裝的結果是可預測的，藉以改善系統可靠性。

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**其他資訊**
</dt> <dd>

WRP 是 Windows 檔案保護的後續版本，可保護 Windows 資料夾中安裝的大部分系統元件。 WRP 可保護大部分儲存 COM 物件建立設定的登錄機碼。 它也會保留特定的資料夾，以供作業系統獨佔使用。 嘗試存取受保護的資源通常會導致存取拒絕錯誤。

如需有關使用遊戲部署 DirectX 執行時間的最佳作法詳細資訊，請參閱 [適用于遊戲開發人員](/windows/desktop/DxTechArts/directx-setup-for-game-developers)的 Directx 文章 directx 安裝。

</dd> </dl>

### <a name="35-avoid-reboots-during-installation"></a>3.5 避免在安裝期間重新開機

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**要求**
</dt> <dd>

遊戲安裝程式不應假設重新發佈套件的 Windows 元件安裝需要重新開機，除非重新開機是由傳回結果或 Microsoft 檔所表示。

如果遊戲安裝程式一律強制重新開機，則必須由 Microsoft 核准。

Windows Installer 套件中包含的 [檔案使用中] 對話方塊，必須包含可自動關閉應用程式，並在安裝程式完成後嘗試重新開機應用程式的選項。

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**理由**
</dt> <dd>

在安裝之後重新開機系統，對使用者來說是不方便的，而且通常不需要。

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**其他資訊**
</dt> <dd>

如需詳細資訊，請參閱搭配 [使用 Windows Installer 與重新開機管理員](/windows/desktop/Msi/using-windows-installer-with-restart-manager)。

</dd> </dl>

### <a name="36-use-file-versioning-correctly"></a>3.6 使用正確的檔案版本控制

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**要求**
</dt> <dd>

遊戲安裝程式必須正確檢查，以確定已安裝最新的檔案版本。 安裝遊戲絕不能回歸您不會產生的任何檔案，或是由您未產生的應用程式所共用的檔案。

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**理由**
</dt> <dd>

共用元件和系統元件通常會更新安全性修正和擴充功能。 包含舊版更新元件的安裝應該不會導致遺失已套用的更新和修正程式。

</dd> </dl>

### <a name="37-support-autorun-conditional-requirement"></a>3.7 支援自動運行 \[ 條件需求\]

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**要求**
</dt> <dd>

針對在 CD、DVD 或其他支援自動執行的卸載式媒體上散佈的遊戲，第一次插入光碟時，除非使用者已停用自動執行功能，否則應用程式必須自動執行或提示使用者安裝遊戲。

成功安裝應用程式之後，重新插入磁片磁碟機中的光碟時，不會自動重新開始安裝。 如果使用者想要更新或變更其安裝選項，可以接受要求。

自動運行應用程式不能提示提高許可權 (也就是說，它必須在資訊清單中依需求 2.1 asInvoker，不過它可以啟動安裝程式或其他需要系統管理許可權的公用程式。 只有在未安裝遊戲或使用者明確選取時，才會發生提高許可權。

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**理由**
</dt> <dd>

自動運行可簡化使用媒體分散式應用程式的體驗，例如通常需要光碟存在於磁片磁碟機才能播放遊戲的遊戲。

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**其他資訊**
</dt> <dd>

要求使用者在檔案總管中流覽，以從 CD 或 DVD 開機安裝是不可接受的。

針對分散在多張光碟上的遊戲，在理想的情況下，最好是使用自動執行功能或繼續安裝，而不提示使用者按下按鍵或採取其他動作。

撰寫自動安裝程式時，請確定 Windows 的全新安裝中有所有必要的元件。 一般的應用程式會依賴安裝程式所安裝的技術，但自動執行本身會在任何這類設定發生之前執行。 其中一個常見的範例就是自動安裝程式失敗，因為 Visual C Runtime Dll 並未包含在 Windows 安裝程式中。 因此，自動執行程式必須使用應用程式本機 CRT 部署，或必須以靜態方式連結 CRT。

針對 windows Vista 之前的 Windows 版本所撰寫的自動執行程式，不應該使用 .NET 執行時間，因為這項技術並不包含在 Windows XP 或舊版的 Windows 中。 Windows Server 2003 和 Windows Vista 是 Windows 的第一個版本，可將 .NET 執行時間納入為作業系統的一部分。

基於類似的原因，自動運行程式不需要有 DirectX SDK 選用的並存元件，例如 D3DX9、D3DX10、D3DX11、XAudio2、X3DAudio、交易、XINPUT 和 MDX 1.1。

如需使用自動運行的範例，請參閱自動運行範例。

</dd> </dl>

## <a name="reliability"></a>可靠性

**安全性與相容性需求的摘要**

**客戶權益**

這些需求會將損毀、停止回應和重新開機的次數降到最低，讓應用程式更可靠。 可靠性需求有助於確保軟體的可預測性、可維護性、彈性和可復原性。

### <a name="41-eliminate-unnecessary-reboots"></a>4.1 消除不必要的重新開機

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**要求**
</dt> <dd>

所有應用程式安裝程式都必須利用重新開機管理員 Api 來避免系統重新開機 (請參閱需求 3.5) 。

遊戲不得封鎖關機。

所有應用程式都必須接聽並回應下列關機訊息，以回應重新開機管理員：

<dl> <dt>

<span id="WM_QUERYENDSESSION_with_LPARAM___ENDSESSION_CLOSEAPP__0x1___"></span><span id="wm_queryendsession_with_lparam___endsession_closeapp__0x1___"></span><span id="WM_QUERYENDSESSION_WITH_LPARAM___ENDSESSION_CLOSEAPP__0X1___"></span>\_具有 LPARAM = ENDSESSION \_ CLOSEAPP (0x1) 的 WM QUERYENDSESSION 
</dt> <dd>

GUI 應用程式必須在準備重新開機時，立即回應 (TRUE) 。

</dd> <dt>

<span id="WM_ENDSESSION_with_LPARAM___ENDSESSION_CLOSEAPP__0x1___"></span><span id="wm_endsession_with_lparam___endsession_closeapp__0x1___"></span><span id="WM_ENDSESSION_WITH_LPARAM___ENDSESSION_CLOSEAPP__0X1___"></span>\_具有 LPARAM = ENDSESSION \_ CLOSEAPP (0x1) 的 WM ENDSESSION 
</dt> <dd>

應用程式必須在5秒內傳回0值，然後關閉。

</dd> <dt>

<span id="CTRL_C__"></span><span id="ctrl_c__"></span>CTRL + C 
</dt> <dd>

接收此訊息的主控台應用程式必須立即關閉。

</dd> </dl> </dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**理由**
</dt> <dd>

系統重新開機是嚴重的中斷。 他們會導致使用者體驗不佳，而且應該將其最小化。 某些作業（例如重要的系統更新）可能需要重新開機。 藉由聆聽關機訊息，遊戲和其他應用程式可以立即回應重新開機管理員的要求。 如此一來，即可避免在有效的重新開機要求中發生不必要的延遲。

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**其他資訊**
</dt> <dd>

如果遊戲安裝程式在沒有任何自訂動作的情況下使用 Windows Installer 技術 (MSI) ，則會自動提供這項功能。 Microsoft 轉散發套件也支援重新開機管理員。

如需重新開機管理員的詳細資訊，請參閱 MSDN 文章中的 [重新開機管理員](/windows/desktop/RstMgr/about-restart-manager)。

</dd> </dl>

### <a name="42-eliminate-application-verifier-failures"></a>4.2 消除應用程式驗證器失敗

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**要求**
</dt> <dd>

在下列測試中，遊戲必須不會在 Microsoft 應用程式驗證器 (AppVerifier) 4.0 版或更新版本下產生任何失敗：

-   基本概念：控制碼、堆積、鎖定、記憶體、TLS
-   其他： DangerousAPIs、DirtyStacks

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**理由**
</dt> <dd>

AppVerifier 會測試許多在 Windows 應用程式中造成當機和停止回應的已知問題，以及已知的安全性弱點。

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**其他資訊**
</dt> <dd>

如需應用程式驗證器的詳細資訊，請參閱 MSDN 上的 [應用程式驗證器](/previous-versions/ms220948(v=vs.80)) 和 [使用軟體發展生命週期中的應用程式驗證器](/previous-versions/aa480483(v=msdn.10)) 。 您可以從 [下載詳細資料](https://www.microsoft.com/downloads/details.aspx?familyid=c4a25ab9-649d-4a1b-b4a7-c9d8b095df18) 下載應用程式驗證器： Microsoft 下載中心上的應用程式驗證器。

這項需求不適用於沒有原生 interop 的純受控應用程式。

這些測試應該在發行組建上執行。 調試組建可能會產生錯誤的錯誤。 某些反盜版和反相關的技術可能會干擾 AppVerifier 的執行。 因此，您應該執行這些測試，而不會啟用反盜版和防功能的技術。

您可能必須將基本概念：堆積測試的完整屬性設為 FALSE，因為完整 PageHeap 會大幅增加執行中應用程式的記憶體壓力。 仍會偵測到失敗，但如果您只使用部分 PageHeap，可能會比較難追蹤。

如果您在應用程式驗證器中使用 UAC/LUA 相關的測試以符合使用者帳戶控制需求2.1 和3.2，您應該使用 [標準使用者分析器](/windows/desktop/Win7AppQual/standard-user-analyzer--sua--tool-and-standard-user-analyzer-wizard--sua-wizard-) 來檢查結果。 此外，也有許多其他有用的測試，這些測試是由您強烈建議用於開發和測試的應用程式驗證器，以確保與目前和未來版本的 Windows 相容。 **HighVersionLie** 測試用來確認符合需求2.5 的合規性。

Visual Studio Team System 包含已整合至偵錯工具環境的 AppVerifier 功能子集。 這可能有助於追蹤和解決基本概念的問題：堆積、控制碼和鎖定測試。

</dd> </dl>

### <a name="43-support-windows-error-reporting-and-file-version-information"></a>4.3 支援 Windows 錯誤報告和檔案版本資訊

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**要求**
</dt> <dd>

若要啟用 Windows 錯誤報告支援，遊戲必須符合下列需求：

-   遊戲必須只處理已知和預期的例外狀況。 Windows 錯誤報告不得停用。 如果遊戲中出現錯誤（例如存取違規），則必須允許 Windows 錯誤報告報告損毀。
-   所有可執行檔 (例如 .exe 檔案或 Dll) 必須包含正確的產品名稱、公司名稱和檔案版本。
-   正常結束遊戲時，不能造成不明的例外狀況錯誤。

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**理由**
</dt> <dd>

Windows 錯誤報告 Api 提供對 Microsoft 的重要意見反應，以偵測應用程式中的廣泛當機和停止回應。 這可讓 Microsoft 及其合作夥伴快速偵測並解決導致應用程式失敗的系統和驅動程式問題。

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**其他資訊**
</dt> <dd>

遊戲可以包含自訂的未處理例外狀況處理常式，以執行自訂支援和報告功能，但必須將任何錯誤傳遞至 **ReportFault** 或 **WerReportSubmit** 函數。

您可以在 Windows 桌面 UI 中查看檔案屬性，並檢查 [版本] 屬性頁，以驗證適當的檔案版本資訊。

如需有關 Windows 錯誤報告 Api 的詳細資訊，以及如何分析當您使用此服務時所產生的損毀傾印，請參閱 DirectX 文章損毀傾印 [分析](/windows/desktop/DxTechArts/crash-dump-analysis)。

</dd> </dl>

## <a name="xbox-360-common-controller-for-windows-terminology"></a>適用于 Windows 的通用控制器 Xbox 360 術語



| Name                                          | 描述                                                                                                 |
|------------------------------------------|--------------------------------------------------------------------------------------------------|
| A                                        | 按鈕。                                                                                     |
| B                                        | B 按鈕。                                                                                     |
| 返回                                     | [上一步] 按鈕。                                                                                  |
|  (右/左) 的緩衝器                      | 位於控制器右上方和左邊緣的按鈕。 相當於肩按鈕。    |
| 方向板                          | 控制器方向面板。                                                                   |
| D-pad                                    | 已接受的方向板縮寫。                                                         |
| DP                                       | 方向板縮寫和控制器標籤。                                                |
| RB、LB                                   | 靠右和左的緩衝器縮寫和控制器標籤。                                        |
| RS、LS                                   | 靠右和向左的縮寫和控制器標籤。                                         |
| RT、LT                                   | 靠右和向左觸發程式縮寫和控制器標籤。                                       |
| RSB、LSB                                 | 靠右和向左的縮寫和控制器標籤。                                         |
| START                                    | [開始] 按鈕。                                                                                 |
|  (右/左) 杆                       | 控制器杆。 先前為操縱杆。                                                       |
|  (右/左) 駕駛按鈕                | 控制器杆按鈕。 先前為操縱杆按鈕。                                         |
|  (右/左) 觸發程式                     | 控制器觸發程式。                                                                          |
| 震動                                | 遊戲控制器馬達產生的意見反應。 請勿使用 rumble。                           |
| X                                        | X 按鈕。                                                                                     |
| Y                                        | Y 按鈕。                                                                                     |
| 適用于 Windows 的 Xbox 360 控制器          | Xbox 360 的遊戲台銷售為電腦硬體 SKU，包括 Windows 設備磁碟機光碟。          |
| 適用于 Windows 的 Xbox 360 無線控制器 | Xbox 360 的無線遊戲台銷售為電腦硬體 SKU，包括 Windows 設備磁碟機光碟。 |



 

## <a name="guidelines-for-game-middleware-products"></a>遊戲中介軟體產品的指導方針

### <a name="introduction"></a>簡介

針對 Windows 方案適用的遊戲，遊戲必須符合技術需求清單。 任何隨附于標題 (可執行檔、Dll、驅動程式等的協力廠商元件，) 也必須符合這些需求，才能讓遊戲符合資格。 本檔著重于協力廠商元件必須符合的最常見需求，讓遊戲通過合規性測試。 安裝程式和完整的遊戲引擎/生產套件應該回顧 Windows 技術需求檔的完整遊戲，因為這些工具當中有許多需求受到影響。

### <a name="additional-recommendations"></a>其他建議

除了確保您的元件支援建立符合 Windows 遊戲需求的標題，在設計和部署 Windows 遊戲的程式庫或支援公用程式時，還有一些其他考慮需要考慮。

-   為了支援使用64位原生 x64 應用程式的開發人員，請提供您程式庫的32位和64位原生版本。 32位版本必須是每 2.2 64 位相容的版本。 32位應用程式的程式庫不應假設沒有任何32位位址的高位可支援在 LARGEADDRESSAWARE x86 應用程式內使用。
-   如果您提供原生程式碼 (C/c + +) 標頭，請使用標準注釋語言 (SAL) 屬性語法來裝飾您的公用 API 常式。 這可讓您文件庫的使用者獲得使用靜態程式碼分析的最大效益 (/analyze) ，此是 Visual Studio Team System 2005、Visual Studio Team System 2008、Visual Studio 2010 Premium 和 Visual Studio 2010 旗艦版，以及公開可用的 Windows SDK 編譯器工具的一部分。
-   如果您的產品在使用者進程中建立執行緒，請務必將每個執行緒命名為，讓偵錯工具能夠適當地批註執行中的執行緒。
-   如果您撰寫的常式是要在遊戲的主要迴圈內呼叫，請使用 D3DX 常式 D3DPERF \_ BeginEvent/EndEvent 和 D3DPERF \_ SetMarker 來標注高階作業，以便使用適用于 WINDOWS 的 PIX 來更輕鬆地識別瓶頸。
    > [!Note]  
    > 針對 Visual Studio 2012 圖形診斷功能，這些 D3DX 和 PIX 常式會由 [**ID3DUserDefinedAnnotation**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3duserdefinedannotation) 介面取代。

     

-   針對網路程式庫，請提供 IP 中立的執行，並避免已淘汰的僅限 IPv4 常式，以支援 Windows XP Service Pack 2、Windows Vista 和 Windows 7 中的 IPv6 和 Teredo 技術。
-   遊戲服務提供者應該使用第2版的 GDF 架構向遊戲瀏覽器註冊，並使用 RSS 功能提供與服務相關的新聞。

### <a name="games-for-windows-showcases"></a>Windows 遊戲展示

### <a name="introduction"></a>簡介

Windows 展示的遊戲超越了在 Windows 電腦上提供穩固的遊戲體驗。 藉由實行這些功能，遊戲可為最新 Windows 平臺上的使用者體驗增加更多驚喜。

Windows 標題的遊戲必須符合本文所列的所有技術需求，但是展示功能是選擇性的。 這些標題可自由地實行一些、無或所有展示。

### <a name="s1-exploit-direct3d-11"></a>S 1 惡意探索 Direct3D 11

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**要求**
</dt> <dd>

Direct3D 11 是適用于 Windows Vista 和 Windows 7 的新一代轉譯 API。 利用 Direct3D 11 的遊戲使用優化的內容、先進的轉譯技巧，以及新的硬體功能，在支援10、10.1 和11的硬體上建立引人注目的體驗。

如果遊戲也實行 Direct3D 9，並存的比較應該會針對 Direct3D 11 的內容品質、視覺精確度、效能、場景複雜性和其他區域圖形精確度，示範可察覺的改進。 這項支援受限於 Windows 技術需求1.7 的遊戲。

Direct3D 10level9 技術可以用來支援 Windows Vista 和 Windows 7 上的著色器模型 2.0/3.0 Direct3D 9 類別的影片硬體，而不是使用並存的 Direct3D 9 實作為廣泛的硬體支援。 不過，這並不足以示範此展示。

在執行 Windows Vista 或已安裝 Direct3D 11 的 Windows 7 的電腦上，遊戲應該預設為使用 Direct3D 11。

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**理由**
</dt> <dd>

Direct3D 11 API 建基於 Windows 顯示驅動程式模型 (WDDM) 和 Direct3D 10.1 基礎結構，以支援新的功能：硬體鑲嵌、計算著色器、多執行緒轉譯和資源建立、新的材質壓縮格式，以及更有彈性的著色器語言。 Direct3D 11 提供新式視訊卡的統一硬體支援，包括最新一代的 Direct3D 11 元件、所有 Direct3D 10 和10.1 視訊卡，以及許多著色器模型 2.0/3.0 Direct3D 9 視訊卡，也就是 Aero 3D 桌面所需的最小影片硬體。

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**其他資訊**
</dt> <dd>

遷移 Direct3D 9 轉譯引擎以使用新的 Direct3D 11 介面是一項妥善定義的工作：

-   消除所有固定函式的作業，以改用可程式化著色器。
-   將所有現有的著色器更新為著色器模型 4.x/5 的新語法。
-   更新資源管理以支援新的視圖模型。
-   將所有資產轉換為使用新的可用格式清單。
-   更新轉譯狀態處理以使用不可變的狀態欄塊，然後將著色器常數重新提交到常數緩衝區。

這項轉換對於啟用 Direct3D 11 展示是不可或缺的，但結果不符合利用新 API 的展示需求。

新的 API 和相關聯的 HLSL 程式設計模型提供許多提高內容的機會：

-   運用現有的 Direct3D 10 硬體功能，例如幾何著色器、串流輸出、材質陣列，以及 BC4/BC5 壓縮的材質格式。
-   運用現有的 Direct3D 10.1 硬體功能，例如獨立的每一轉譯目標 blend 模式、MSAA 深度取回、MSAA 每個範例的著色器存取、cube 地圖陣列，以及轉譯成區塊壓縮的 (BC) 格式。
-   在現有的 Direct3D 10/10.1 視訊卡上使用計算著色器搭配 CS4 來實行先進的 GPU 演算法 (由更新的影片驅動程式) 或在下一代 Direct3D 11 視訊卡上的 CS 5.0 來啟用。
-   使用無限制執行緒資源建立和多個裝置內容，在多個執行緒上轉譯，以改善多核心系統的效能， (使用更新的視頻驅動程式) 。 如需詳細資訊，請參閱 Windows 展示的遊戲。3。
-   使用 Direct3D 11 類別影片硬體的新功能，例如使用輪廓和網域著色器進行硬體鑲嵌、著色器模型 5.0 HLSL 著色器硬體功能 BC6HBC7 壓縮的材質格式，以及動態著色器連結。

可以使用 Direct3D 9 來執行的技術，主要是透過高 CPU 成本來 () 可以使用有效率的方式將其載入至 GPU，進而釋出 CPU 資源以支援其他遊戲需求。

您可以從 DirectX SDK 取得 Direct3D 11 Api、支援工具和範例。 另請參閱 Windows 中的圖形 Api。

</dd> </dl>

### <a name="s2-exploit-x64-native"></a>S. 2 惡意探索 x64 原生

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**要求**
</dt> <dd>

此遊戲包含64位原生可執行檔，可提供在 x64 支援的硬體上執行的 x64 版 Windows 所啟用的強大新體驗。 與32位版本的遊戲並存比較，應會在內容複雜度、降低整體載入時間和效能方面提供可察覺改進。

在 Windows 的64位版本中，安裝程式應一律將64位原生版本設定為遊戲瀏覽器和 Windows XP Professional x64 Edition 中快速鍵的預設值。 如果需要雙重安裝，則可以為 Windows Vista 和 Windows 7 上的遊戲瀏覽器指定可指向32位版本的額外播放工作，但預設值應該保持64位原生版本。

請注意，此遊戲應支援 Windows Vista 和 Windows 7 的64位版本，以符合此展示建議。 建議 Windows XP Professional x64 Edition 的支援，但不是必要的。

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**理由**
</dt> <dd>

x64 技術為消費者和伺服器市場提供64位的定址功能，包括現有應用程式的全速32位反向相容性。 x64 是適用于 AMD (AMD64) 和 Intel (EMT64) 的藍圖主要部分，除了超行動 Cpu 之外，還支援所有目前和未來世代處理器的技術。

Windows XP Professional x64 Edition 是第一個取用者導向的 Windows 作業系統 (作業系統) 支援 x64 技術，而 Windows Vista 和 Windows 7 則大幅擴充了 OS 的可用性，以供64位的取用者計算之用。 在許多新電腦上使用 2 GB 的 RAM 作為標準時，記憶體調整的進一步改進將無法受益于32位個別應用程式，而這些應用程式無法處理超過 2 GB 的實體 RAM。 現今許多遊戲都面臨挑戰，將所有可用的內容納入 2 GB 的虛擬位址空間的限制，尤其是在與高階 Gpu 上提供的大型影片可用的大型影片，以及轉換成 x64 技術時，都能大幅增加支援層級的詳細資料。

32位遊戲的 x64 相容性是 Windows 技術需求 (2.2) 的遊戲，但充分利用新的技術需要64位原生執行。

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**其他資訊**
</dt> <dd>

64位定址的主要優點是能夠直接存取 2 GB 以上的實體和虛擬記憶體。 大型虛擬記憶體位址空間可廣泛地使用記憶體對應 i/o，而不需要擔心32位程式設計中常見的 VM 位址空間耗盡問題。 遊戲可以利用新的空間來大幅改善載入時間，或在某些情況下，消除載入內容的暫停。

現有的32位應用程式可從 x64 版本獲益，方法是在使用 [啟用大型位址] (**/LARGEADDRESSAWARE**) 連結器選項來處理具有完整32位資料的位址時。 在32位版本的 Windows XP 上，特殊的開機模式允許這類應用程式處理最多 3 GB 的 RAM，而 x64 版可讓您存取最多 4 GB 的 RAM，以用於感知 (LAA) 應用程式的大型位址。 雖然在32位應用程式中使用 LAA 並不符合這項展示需求，但是這項橋樑技術是在 x64 版本的 Windows 上提供額外的調整優勢，而不會完全符合此展示需求的方式。

如需詳細資訊，請參閱遊戲開發人員和[ram、VRAM 和更多 ram](https://www.gamasutra.com/view/feature/3602/sponsored_feature_ram_vram_and_.php) [的64位程式設計](/windows/desktop/DxTechArts/sixty-four-bit-programming-for-game-developers)：64位遊戲位於 Gamasutra。

> [!Note]  
> 此展示的主要挑戰，是確保您的遊戲所依賴的任何協力廠商程式庫或元件都可用於64位原生開發。 許多舊版的 Microsoft Api 也已從64位的原生環境中消除，這可能會對引擎程式碼基底（包含較舊的重要系統執行）產生挑戰。

 

</dd> </dl>

### <a name="s3-exploit-many-core-processors"></a>S. 3 惡意探索 Many-Core 處理器

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**要求**
</dt> <dd>

這項遊戲所實行的功能，可利用多核心處理器、調整為3、4或更多核心（如果有的話）。

如果遊戲支援單處理器或雙核心系統，則與四核心系統並存的比較，應該會展示可察覺的新功能、其他引人注目的效果、內容品質的改進，以及/或改善的效能。

因為遊戲已經廣泛支援雙核心調整，而且各種 Direct3D 驅動程式增強功能都會自動利用雙核心調整，所以雙核心調整不足以示範此展示。

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**理由**
</dt> <dd>

Cpu 的效能持續成長已從時脈速率的增強功能切換到加法運算核心。 AMD 和 Intel 藍圖都是以可擴充的多核心設計為基礎。 所有新一代遊戲平臺都有多核心 Cpu，因為這是處理器演進的基礎轉變。 單一執行緒應用程式不再會看到下一代 Cpu 的顯著增益。 簡單的多執行緒也將無法調整，因為一般使用中的 CPU 核心數目會成長到三個以上。

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**其他資訊**
</dt> <dd>

請注意，核心計數不需要是2的乘冪，因此遊戲應以線性方式調整，並處理核心計數3、4、5、6、7、8等等。

藉由增加應用程式中的執行緒數目來進行調整，只會在檢查中保存通訊和執行緒同步處理的成本時提供傳回。 以功能為基礎的調整可能會在短期內證明更簡單的解決方案，讓遊戲正常運作，而不需要在單一核心系統上使用額外的執行緒，並在可用的額外 CPU 電源時啟用它們。

如需詳細資訊，請參閱在 [Xbox 360 和 Microsoft windows 上撰寫多核心的程式碼](/windows/desktop/DxTechArts/coding-for-multiple-cores) ，以及 DXUTLockFreePipe 公用程式和 CoreDetection 範例中的 [Xbox 360 和 microsoft Windows 的程式設計考慮 Lockless](/windows/desktop/DxTechArts/lockless-programming) 。

使用 Direct3D 11 無線程資源建立和裝置內容，有助於在轉譯和載入圖形資源時達到多核心的擴充性。 查看 Windows 展示的遊戲。1。

請注意，直接使用 CPU 指令 rdtsc，而不是使用 Windows Api 來計算多核心系統的時間，可能會導致某些硬體和 OS 設定發生問題;請參閱 DirectX 文章中的 [遊戲時間和多核心處理器](/windows/desktop/DxTechArts/game-timing-and-multicore-processors) 。

</dd> </dl>

### <a name="s4-support-games-for-windows---live"></a>S：4支援 Windows-LIVE 的遊戲

Microsoft 不再支援 Windows LIVE 的遊戲。

### <a name="s5-support-windows-touch"></a>Windows Touch 的5個支援

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**要求**
</dt> <dd>

Windows 觸控式遊戲可在執行 Windows 7 的電腦上使用觸控和/或手勢播放，並具有觸控顯示功能。 您也可以使用鍵盤輸入，但主要 play 介面必須以觸控式為基礎。

啟用觸控不應防止使用滑鼠或一般控制器，受限於技術需求1.4。

遊戲的安裝程式不應支援 Windows Touch 功能。

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**理由**
</dt> <dd>

膝上型電腦和桌上型電腦都可以使用多點觸控功能的電腦，它們代表 Windows 7 發行版本升級的主要硬體功能。 Windows 7 支援整個桌面和通用控制項介面的 Windows Touch。

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**其他資訊**
</dt> <dd>

原生程式碼應用程式可以搭配 RegisterTouchWindow 函式，透過 WM 觸控訊息來存取多點觸控 \_ 。 [](/windows/desktop/api/winuser/nf-winuser-registertouchwindow) 另請參閱操作和慣性 API。

Windows Presentation Foundation (WPF) 4.0 提供多點觸控介面的受控解決方案。

如需詳細資訊，請參閱 Windows Touch SDK。

</dd> </dl>

### <a name="s6-support-high-color"></a>S 6 支援高色彩

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**要求**
</dt> <dd>

支援高彩的遊戲會使用 10:10:10:2 (DXGI \_ 格式 \_ R10G10B10A2、D3DFMT \_ A2B10G10R10) 或 16:16:16:16 (DXGI \_ 格式 \_ R16G16B16A16、D3DFMT \_ A16B16G16R16) 格式來呈現背景緩衝區和全螢幕顯示模式。

藉由使用高色彩轉譯目標，在執行10位或16位範圍的色調對應時，可以使用延伸或寬範圍來轉譯 High-Dynamic 範圍 (HDR) 內容。

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**理由**
</dt> <dd>

監視器在許多年份中都能夠顯示超過256色層級，即使 CRT 顯示器普遍出現也是如此。 掃描視訊卡上的硬體是限制因素。 新式 Gpu （包括大部分的 Direct3D 9 類別硬體以及所有 Direct3D 10 類別和更佳的硬體）具有每個通道至少能有10位的掃描後的硬體，而硬體功能則是設定為在未來的每個顏色通道成長至16位。 HD TV 互連系統 (HDMI、DisplayPort) 設計為每個通道處理超過8位，而且類比 VGA 已經有這類信號。

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**其他資訊**
</dt> <dd>

請注意，在過去，高彩或嗨的色彩是指從 256 (8 位) 色彩顯示為15或16位色彩顯示。 大部分的顯示器系統自移至真正的色彩，也就是24位色彩，或是紅色、綠色和藍色的每個色彩頻道都有8位。 在這裡，我們表示新一代的顯示器系統，可在每個個別色頻中使用超過8個位的方式運作。 也稱為深度色彩。

</dd> </dl>

### <a name="recommended-best-practices"></a>建議的最佳作法

### <a name="introduction"></a>簡介

除了符合技術需求，並在您的標題中採用一或多個展示，所有 Windows 遊戲都應遵循一些最佳作法。 雖然這些建議落在核心技術需求的範圍之外，但強烈建議您針對 Windows 標題的所有遊戲採用這些建議。

### <a name="additional-recommendations"></a>其他建議

-   使用最新的 Visual Studio 編譯器和執行時間。 較新版本的編譯器會針對所產生的程式碼品質和安全性問題，執行大幅的改進，並採用新式的處理器優化策略。 更新編譯器和使用最新的 C 執行時間是遷移至新式程式碼撰寫實務的簡單方法。
-   使用動態連結程式庫 (DLL) 版本的 C 執行時間，而不是靜態連結，並利用安全 CRT。  (例外狀況可以在特殊的預先安裝案例中進行，例如自動執行程式或安裝程式本身) 。
-   若為遊戲音訊，請使用 XAudio2、X3DAudio 及（或）交易，而不是 DirectSound。 針對執行所有混合和來源速率轉換的音訊引擎，以及只需要低延遲的音訊輸出解決方案，請使用 Windows XP (上的 DirectSound，只在 Windows Vista 和 Windows 7 上使用) 和 WASAPI。
-   避免使用舊版和已淘汰的 Api： DirectDraw、DirectSound、DirectPlay、DirectMusic 的效能層級、DirectPlay 語音和 Direct3D 保留模式。 請注意，Windows Vista 或 Windows 7 上都不提供 [DirectPlay 語音] 和 [Direct3D 保留] 模式。 X64 原生應用程式無法使用 DirectPlay 和 DirectMusic 的效能層級。
-   使用 SSE/SSE2 SIMD 指令集進行優化。 請參閱 Windows SDK 中的 [DirectXMath](/windows/desktop/dxmath/directxmath-portal) API，作為 SIMD 優化數學運算作業的跨平臺解決方案。
-   使用 Windows 安全性的新式最佳作法 (包括編譯器和連結器選項，例如 **/NXCOMPAT**、 **/gs**、 **/SAFESEH**、 **/DYNAMICBASE**、 **/SDL** 等) 。 如需詳細資訊，請參閱 [遊戲開發的最佳安全性作法](/windows/desktop/DxTechArts/best-security-practices-in-game-development)。
-   使用最新的 Windows SDK 元件和程式庫。 移除舊版 DirectSetup 的相依性，例如 D3DX9、D3DX10 和 D3DX11。 請考慮使用 [DirectXTex](https://github.com/Microsoft/DirectXTex) 或 [DirectXTK](https://github.com/Microsoft/DirectXTK) 或兩者。
-   請避免使用較舊的 HLSL 編譯器，而改為使用新式 HLSL 編譯器。 如果您的應用程式需要圖元著色器1.x 的支援，請使用著色器元件而非 HLSL，或將較舊的編譯器限制為只使用這些案例。

## <a name="resources"></a>資源



| 詞彙                                                                                                                                                                                                                         | 描述                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Games_for_Windows__Test_Cases__"></span><span id="games_for_windows__test_cases__"></span><span id="GAMES_FOR_WINDOWS__TEST_CASES__"></span>適用于 Windows 的遊戲：測試案例 <br/>                              | Windows XP、Windows Vista 和 Windows 7 遊戲的最佳作法<br/>                                                                               |
| <span id="Windows_SDK__"></span><span id="windows_sdk__"></span><span id="WINDOWS_SDK__"></span>Windows SDK <br/>                                                                                                      | [Windows Sdk](https://msdn.microsoft.com/bb980924.aspx)<br/>                                                                                      |
| <span id="User_Account_Control_Guidelines__"></span><span id="user_account_control_guidelines__"></span><span id="USER_ACCOUNT_CONTROL_GUIDELINES__"></span>使用者帳戶控制指導方針 <br/>                      | [使用者帳戶控制相容性的 Windows Vista 應用程式開發需求](/previous-versions/dotnet/articles/bb530410(v=msdn.10))<br/> |
| <span id="WinQual_Developer_Portal__"></span><span id="winqual_developer_portal__"></span><span id="WINQUAL_DEVELOPER_PORTAL__"></span>WinQual 開發人員入口網站 <br/>                                                  | [Windows Quality Online Services (Winqual) ](/windows-hardware/drivers/dashboard/winqual-submission-tool--winqualexe-)<br/>                                                                         |
| <span id="DirectX_Developer_Portal__"></span><span id="directx_developer_portal__"></span><span id="DIRECTX_DEVELOPER_PORTAL__"></span>DirectX 開發人員入口網站 <br/>                                                  | [Directx 開發人員中心](/previous-versions/windows/apps/hh452744(v=win.10))<br/>                                                                               |
| <span id="Games_for_Windows_and_DirectX_SDK_Blog"></span><span id="games_for_windows_and_directx_sdk_blog"></span><span id="GAMES_FOR_WINDOWS_AND_DIRECTX_SDK_BLOG"></span>Windows 和 DirectX SDK Blog 的遊戲<br/> | [適用於 Windows 與 DirectX SDK 的遊戲](https://walbourn.github.io/)<br/>                                                                           |
| <span id="Additional_DirectX_Articles"></span><span id="additional_directx_articles"></span><span id="ADDITIONAL_DIRECTX_ARTICLES"></span>其他 DirectX 文章<br/>                                             | [DirectX 技術文章](/windows/desktop/DxTechArts/dx9-technical-articles)<br/>                                                                                    |



 

 


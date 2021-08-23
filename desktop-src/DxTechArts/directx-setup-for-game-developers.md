---
title: 適用于遊戲開發人員的 DirectX 安裝
description: 本文旨在解決一些有關 DirectX 執行時間的常見問題，並使用 DirectSetup 安裝 DirectX。
ms.assetid: 2ab439be-8d99-bcf8-89af-d4274e044c88
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcd694243adad852d68e5db5fc342f9259ace7ebbc71923bf56a60bbc1b511b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070538"
---
# <a name="directx-installation-for-game-developers"></a>適用于遊戲開發人員的 DirectX 安裝

本文旨在解決一些有關 DirectX 執行時間的常見問題，並使用 DirectSetup 安裝 DirectX。

-   [DirectX 執行時間](#directx-runtime)
-   [DirectX 版本號碼](#directx-version-number)
-   [DirectX 程式庫](#directx-libraries)
-   [由遊戲安裝程式安裝 DirectX](#installation-of-directx-by-the-games-installer)
-   [小型安裝套件](#small-installation-packages)
-   [進行內部部署的 Debug DirectX Runtime](#internal-deployment-of-the-debug-directx-runtime)

> [!IMPORTANT]
> 舊版 DirectX SDK 于生命週期結束，但仍可供使用，以支援舊的遊戲、教學課程和專案。 新的專案不應使用它。 使用舊版 DirectX SDK 需要針對 D3DX9、D3DX10、D3DX11、XAudio 2.7、XInput 1.3 和交易等元件使用已被取代的 DirectSetup。 如需有關 DirectX SDK 目前狀態的詳細資訊，請參閱 [什麼是 DIRECTX sdk？](../directx-sdk--august-2009-.md)和 Blog 文章 [不會直接設定](https://walbourn.github.io/not-so-direct-setup/)。

## <a name="directx-runtime"></a>DirectX 執行時間

DirectX 執行時間是由核心元件和選擇性元件所組成。

系統會將核心元件（例如 Direct3D 和 DirectInput）視為作業系統的一部分。 directx 9.0 c 的核心元件自 directx SDK 夏天2004更新後尚未變更，且符合 Microsoft Windows XP SP2、Windows XP Pro x64 Edition 和 Windows Server 2003 SP1 所發行的內容。 WindowsVista 包含 DirectX 10，它支援 Windows 顯示驅動程式模型 (WDDM) 和 Direct3D 2.x。 Windows 7 和 Windows Vista (請參閱[KB971644](https://support.microsoft.com/kb/971644)) 支援 DirectX 11，支援 Direct3D 11、Direct2D、DirectWrite、WARP10 軟體轉譯裝置和10level9 功能等級。 如需詳細資訊，請參閱[Windows 中的圖形 api](/windows/desktop/direct3darticles/graphics-apis-in-windows-vista) 。

選用元件是在 DirectX SDK 的更新中發行，其中包含 D3DX、交易、XAudio2、XINPUT、Managed DirectX 和其他這類元件。 許多選擇性元件會定期更新，以整合客戶的意見反應並公開新的功能。

## <a name="directx-version-number"></a>DirectX 版本號碼

DirectX 版本號碼（例如 9.0 c）只會參考核心元件的版本，例如 Direct3D、DirectInput 或 DirectSound。 此數目並未涵蓋 DirectX SDK 中所發行之各種選用元件的版本，例如 D3DX、交易、XINPUT 等等。

一般來說，除了快速參考核心執行時間位之外，DirectX 版本號碼沒有任何意義。 此數位不應該用來檢查是否已安裝正確的 DirectX 執行時間，因為它不會考慮選用的 DirectX 元件。

## <a name="directx-libraries"></a>DirectX 程式庫

在過去，DirectX SDK 的選用元件（包括 D3DX）是以靜態程式庫的形式發行。 不過，這些現在是以類似動態的程式庫的形式發行 (DLL) ，因為這樣會增加更好的安全性作法需求。 Dll 允許服務先前發行的程式碼。 如果這些元件部署為靜態程式庫，則 Microsoft 將無法解決發行後發現的安全性問題。

當將功能新增或變更為選用元件時，對應 Dll 的名稱也會變更，以確保不會對使用已發行元件的現有遊戲造成回歸。 每個元件的 Dll 會並存，而遊戲開發人員可以藉由連結至對應的匯入程式庫，精確地選擇遊戲所使用的 DLL 版本。

雖然確保 Dll 安裝在系統上並不像單純地連結到靜態程式庫一樣簡單，但對 DirectX SDK 進行了一些變更，以解決 DLL 模型的痛苦：

-   您可以將 DirectX 可轉散發套件設定為僅包含應用程式所需的元件，以將散發和媒體大小降至最低。
-   可轉散發資料夾 [Program Files DirectX SDK 可轉散發套件] \\ \\ \\ 現在包含每個可能選用元件的封包 (.cab) 檔案，因此您不需要深入探索舊版 SDK 即可找到它們。
-   安裝 SDK 本身會安裝每個可能的選擇性元件。
-   包含所有選用元件的 DirectX 可轉散發套件是以 Web 為基礎的安裝程式和可下載的套件形式提供。如需詳細資訊，請參閱 DirectX 開發人員中心 ([directx](/previous-versions/windows/apps/hh452744(v=win.10))) 。

## <a name="installation-of-directx-by-the-games-installer"></a>由遊戲安裝程式安裝 DirectX

> [!Note]  
> 請參閱 [適用于遊戲開發人員的 Direct3D 11 部署](/windows/desktop/direct3darticles/direct3d11-deployment)。

 

以下是將 DirectX 安裝新增至遊戲安裝程式的最佳作法：



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>詞彙</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="Install_the_redistributable_components_every_time.__"></span><span id="install_the_redistributable_components_every_time.__"></span><span id="INSTALL_THE_REDISTRIBUTABLE_COMPONENTS_EVERY_TIME.__"></span>每次都安裝可轉散發元件。 <br/></td>
<td>遊戲的安裝程式應在每次單一安裝期間安裝 DirectX 可轉散發元件，而不允許使用者退出宣告。 如果您允許退出宣告，某些使用者將會猜不到它，如果他們真的這麼做，就不會執行遊戲。 <br/></td>
</tr>
<tr class="even">
<td><span id="Let_the_DirectX_installer_check_for_optional_components.__"></span><span id="let_the_directx_installer_check_for_optional_components.__"></span><span id="LET_THE_DIRECTX_INSTALLER_CHECK_FOR_OPTIONAL_COMPONENTS.__"></span>讓 DirectX 安裝程式檢查是否有選用的元件。 <br/></td>
<td>請勿假設系統上已安裝最新的選用元件，因為 Windows Update 和 Service pack 未提供任何 DirectX 的選擇性元件。 您必須直接執行 dxsetup.exe 或呼叫 DirectSetup，以安裝 DirectX 執行時間。 <br/></td>
</tr>
<tr class="odd">
<td><span id="Set_up_silently.__"></span><span id="set_up_silently.__"></span><span id="SET_UP_SILENTLY.__"></span>以無訊息方式設定。 <br/></td>
<td>以無訊息模式啟動安裝程式，讓使用者不會意外略過更新 DirectX 執行時間。 若要這麼做，您可以使用下列命令來啟動 dxsetup.exe： <br/>
<pre class="syntax" data-space="preserve"><code>   path-to-redistributable\dxsetup.exe /silent</code></pre>
或藉由呼叫 DirectSetup，而不顯示任何 UI。 <br/></td>
</tr>
<tr class="even">
<td><span id="Combine_EULA_acceptances.__"></span><span id="combine_eula_acceptances.__"></span><span id="COMBINE_EULA_ACCEPTANCES.__"></span>結合 EULA 接受。 <br/></td>
<td>如果您提示使用者接受授權合約，請在以無訊息模式安裝時，將其與提示接受 DirectX EULA 的提示結合，如此一來，就只會出現一次 Eula 的提示。 在您安裝任何動作之前，應該先進行提示，如此一來，如果使用者不接受，則最後不會出現失敗的部分安裝。 <br/></td>
</tr>
<tr class="odd">
<td><span id="Just_run_dxsetup_or_call_DirectSetup.__"></span><span id="just_run_dxsetup_or_call_directsetup.__"></span><span id="JUST_RUN_DXSETUP_OR_CALL_DIRECTSETUP.__"></span>只需執行 dxsetup 或呼叫 DirectSetup。 <br/></td>
<td>因為 DirectX 版本號碼未參考核心 DirectX 元件，所以在執行 dxsetup.exe 或呼叫 DirectSetup 之前，請勿檢查已安裝的版本。 此外，請勿檢查檔案是否存在，以測試是否已安裝選用元件，因為這通常不會正確判斷元件存在但需要更新的時間。 不過，DirectX 安裝套件將會快速地判斷這一點，並執行正確的動作。 <br/></td>
</tr>
</tbody>
</table>



 

## <a name="small-installation-packages"></a>小型安裝套件

您可以為 DirectX 建立較小的安裝套件，方法是將 DirectX 可轉散發資料夾的內容減少到讓安裝程式運作所需的最少檔案集，並保留您的遊戲所使用的任何其他元件。

根據您的最低規格，您可能甚至不需要在安裝媒體的可轉散發資料夾中包含核心 DirectX 9.0 c 封包檔。 大部分的 Windows XP 安裝都有 Service Pack 2，包括核心 directx 9.0 c 元件，因此 directx 安裝程式作業將會非常快速，且不需要重新開機。 可以建立的最小封裝約為 3 MB，而且可壓縮成大約一半的大小。 像這樣的封裝包含一個版本的 D3DX DLL，它需要 DirectX 9.0 c 已經存在。

建立可轉散發套件所需的最少量檔案是下列檔案，這些檔案位於 DirectX SDK 可轉散發套件資料夾中， (Program Files directx SDK 可轉散發套件 \\ \\ \) ：

-   dxsetup.exe
-   dsetup32.dll
-   dsetup.dll
-   dxupdate.cab

針對您要安裝的元件，將這些封包檔新增至這些檔案。 如果您需要應用程式的使用者已經有 DirectX 9.0 c，則不需要包含 DirectX.cab 或 dxnt.cab，這會造成大部分的空間需求。 只有 Windows 98 和 Windows DirectX.cab 才需要;只有 Windows 2000、Windows XP 和 Windows XP SP1 才需要 dxnt.cab;\_只有 Windows 2000、Windows xp RTM、Windows XP SP1 和 Windows Server 2003 RTM 才需要 dxdllregx86.cab。 此外，如果您未使用 DirectShow，或假設已經安裝，您可以省略 BDA.cab、BDANT.cab 和 BDAXP.cab。

> [!Note]  
> 您可以假設應用程式的使用者已經有 DirectX 9.0 c （如果您的應用程式是由繼承應用程式所安裝），您可以強制使用者透過 Web 安裝程式進行手動更新，或是假設他們有 Windows XP SP2 或更新版本。

 

繼續進行此範例，如果您只在4月2006使用32位版本的 D3DX，您可以新增 Apr2006 \_ d3dx9 \_ 30 \_x86.cab。 如果您使用32年8月 2006 32 位版本的 XINPUT，請新增 Aug2006 \_ XINPUT \_x86.cab。

如果您有原生的64位應用程式，則必須新增 \_ x64 版本。 但是，如果您在64位作業系統上執行了32位的應用程式，則32位版本的 Dll 將會運作。

然後，您可以散發此檔案封裝並以無訊息模式啟動 DirectSetup，或在命令介面中以無訊息模式執行 dxsetup.exe。 請記得不要透過任何版本檢查檔案來保護此套件，並確定您的使用者無法選擇不執行 DirectX 安裝程式。 其中一個事件會建立 fallible 安裝程式。

## <a name="internal-deployment-of-the-debug-directx-runtime"></a>進行內部部署的 Debug DirectX Runtime

DirectX 元件的偵錯工具執行時間是在安裝 DirectX SDK 時安裝的，但在每部測試電腦上安裝 SDK 可能很麻煩。 您必須設計您的安裝程式，以將偵錯工具檔中的偵錯工具執行時間 dll 複製到 \\ \\ \\ \\ Windows \\ system32 \\ 或遊戲的資料夾中。

不過，我們強烈建議您不要只複製已發行的執行時間 Dll，因為它很容易忘記移除最後一個產品。 相反地，請將 DirectX 安裝程式檔案放在共用資料夾中，然後從共用資料夾以無訊息模式執行安裝程式。

## <a name="desktop-bridge-applications"></a>傳統型橋接器應用程式 

傳統型橋接器使用 D3DX9、D3DX10、D3DX11、XAudio 2.7、XInput 1.3 或交易的應用程式，必須下載[的舊版](https://download.microsoft.com/download/c/c/2/cc291a37-2ebd-4ac2-ba5f-4c9124733bf1/UAPSignedBinary_Microsoft.DirectX.x86.appx) [directx SDK](https://download.microsoft.com/download/c/c/2/cc291a37-2ebd-4ac2-ba5f-4c9124733bf1/UAPSignedBinary_Microsoft.DirectX.x64.appx) ，才能部署這些舊版的 directx SDK 並存元件。 或者，您可以移除所有這類相依性 &mdash; (參閱[XAudio 2.9 的可轉散發版本開發人員指南](../xaudio2/xaudio2-redistributable.md)，以及[不含 D3DX](https://walbourn.github.io/living-without-d3dx/)和[XINPUT 和 Windows 8](https://walbourn.github.io/xinput-and-windows-8/)) 的 blog 文章。
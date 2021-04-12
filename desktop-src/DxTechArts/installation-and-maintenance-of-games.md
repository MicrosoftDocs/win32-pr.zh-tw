---
title: 遊戲的安裝與維護
description: 本文說明一組最佳作法，可協助降低使用者對安裝遊戲所需時間的挫折、防止不必要的支援電話，並讓使用者能夠快速且輕鬆地開始玩遊戲。
ms.assetid: c953165d-2318-ca06-a895-abedcbcb594c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de171fd76654eb3b6edb8818ec073c4ef5ba8ca4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316375"
---
# <a name="installation-and-maintenance-of-games"></a>遊戲的安裝與維護

本文說明一組最佳作法，可協助降低使用者對安裝遊戲所需時間的挫折、防止不必要的支援電話，並讓使用者能夠快速且輕鬆地開始玩遊戲。

-   [初始安裝](#initial-installation)
    -   [簡化安裝 UI](#streamlining-the-installation-ui)
    -   [縮短安裝所需的時間](#reducing-the-time-required-for-installation)
    -   [基本安裝](#minimal-installation)
    -   [隨選安裝](#install-on-demand)
-   [安裝後遊戲-Play](#post-installation-game-play)
    -   [自動](#autorun)
    -   [將安裝隨選安裝轉換成完整安裝](#converting-an-install-on-demand-installation-to-a-full-installation)
    -   [遊戲軟體和內容的維護](#maintenance-of-game-software-and-content)
    -   [自動檢查更新](#checking-for-updates-automatically)
    -   [自動下載修補程式](#downloading-patches-automatically)
-   [其他資源](#other-resources)
-   [相關主題](#related-topics)

## <a name="initial-installation"></a>初始安裝

使用者購買遊戲是因為他們喜歡玩遊戲，而不是因為他們喜歡安裝遊戲。 安裝遊戲應該是快速、直接的，且盡可能讓終端使用者更輕鬆。 在理想的情況下，終端使用者甚至不應該看到安裝 UI;他們應該只要把遊戲光碟放入紙匣，就可以開始播放了。

### <a name="streamlining-the-installation-ui"></a>簡化安裝 UI

現有遊戲安裝 Ui 的常見層面會干擾所需的終端使用者體驗：

-   詢問使用者不必要的問題。

    例如，許多遊戲會詢問使用者是否要安裝 DirectX。 如果遊戲需要執行 Microsoft DirectX，且尚未安裝正確版本的 DirectX，則遊戲應該只安裝 DirectX。

-   詢問使用者問題，大部分的使用者都會以相同的方式回答這些問題。

    若是一般使用者，安裝路徑、[開始] 功能表位置等的預設設定全都沒問題。 為想要變更這些設定的使用者提供先進的選項。

安裝 UI 的設計目的，是要讓一般使用者能夠儘快開始玩遊戲。 如果使用者電腦上已啟用自動啟動功能（預設值），安裝程式應該假設使用者想要儘快播放遊戲，略過任何不必要的問題。 安裝 progra[隨選安裝](#install-on-demand)m 應該會開始將遊戲安裝到預設安裝路徑，最好是使用如中所述的安裝程式。 讓使用者有機會在自動開始安裝之前變更安裝設定。 不過，若要完成此動作，請提示使用者按下按鍵以取得 advanced 安裝選項，如果使用者未在五到十秒內達到該索引鍵，則會以預設選項自動繼續。

如果使用者的電腦上未啟用自動執行功能，安裝程式應該假設使用者不希望安裝程式自動開始安裝遊戲。 如果安裝程式是以非自動執行時間以外的方式啟動，它應該會啟動 advanced 安裝程式 UI。

### <a name="reducing-the-time-required-for-installation"></a>縮短安裝所需的時間

現今大部分的 Microsoft Windows 遊戲都需要五分鐘到半小時的時間，才能完成安裝程式。 相較之下，大部分的主控台遊戲在使用者將遊戲 CD 插入遊戲時，不會花費30秒以上的時間。 這項差異是因為大部分的 Windows 遊戲都是設計成從電腦的硬碟執行大部分的內容（如果不是全部），如果主控台缺少可永久儲存大量內容的位置，則需要從來源媒體執行內容。 從本機硬碟載入內容時，可加快遊戲的載入時間，缺點是所有內容都必須在某個時間點從源媒體複製到硬碟。 大部分的 Windows 遊戲都選擇在安裝過程中，一次將所有內容複寫到硬碟上。 這會使由使用者的遊戲初始體驗，讓使用者在玩遊戲之前，先觀賞幾分鐘的進度列。

有兩種方法可用來將最初安裝遊戲所花費的時間降到最低： [最少安裝](#minimal-installation) 並 [隨選安裝](#install-on-demand)。

### <a name="minimal-installation"></a>基本安裝

在最小的安裝案例中，遊戲只會在硬碟上安裝最小的一組內容。 這通常只包含遊戲可執行檔和 Dll。 內容的其餘部分則是直接從來源媒體存取。 這可大幅縮短安裝所需的時間，因為遊戲的可執行檔很少會超過 10-20 MB。 缺點是遊戲需要較長的時間才能在遊戲中載入內容，因為它必須從較慢的來源媒體載入。

若要在以 Windows Installer 為基礎的安裝程式中建立基本安裝設定：

-   將安裝至硬碟的所有元件組成標示為在本機安裝的功能。

    這項功能將稱為「啟動程式」功能。

-   將從來源媒體執行的所有元件，組成標示為「從來源執行」的功能。
-   開啟可能位於來源媒體的檔案時，請使用 [**MsiGetComponentPath**](/windows/desktop/api/msi/nf-msi-msigetcomponentpatha) 函式來判斷檔案的路徑，而不是硬式編碼路徑。

    這樣做可確保即使使用者的 CD/DVD 磁片磁碟機的磁碟機號有所變更，也可以找到該檔案。

-   壓縮保留在 CD/DVD 上的內容。

    用來解壓縮內容的 CPU 時間量通常會因 CD/DVD 磁片磁碟機的資料傳送速率緩慢而隱藏。

-   將內容分組成大型、連續的檔案，並依序存取。

    CD/DVD 光碟機的搜尋時間與硬碟的 abysmal 相比，大部分的 CD/DVD 磁片磁碟機都不會達到尖峰傳輸速率，除非它們正在讀取大型的連續檔案。

-   依照可能存取的順序，在 CD/DVD 上配置內容。

    以與磁片上配置相同的順序存取檔案時，搜尋時間會大幅降低。

### <a name="install-on-demand"></a>隨選安裝

在隨選安裝的案例中，只是為了進行最基本的安裝，遊戲一開始只會在硬碟上安裝啟動遊戲所需的檔案。 不過，在每次需要時，它不會從來源媒體存取剩餘的內容，而是在每次需要時，將每個內容都安裝在硬碟上，然後在每次後續使用時從本機硬碟存取該內容。 初始安裝所需的時間與最小的安裝所需的時間一樣小，但在第一次存取每個內容之後，載入時間也會改善。

若要在以 Windows Installer 為基礎的安裝程式中建立隨選安裝：

-   將一開始安裝至硬碟的所有元件，組成標示為在本機安裝的功能。

    請注意，這與最基本安裝的啟動程式功能完全相同。

-   根據可能一起使用的元件，將其餘內容分組為多個功能。

    例如，在以層級為基礎的遊戲中，將指定層級上所使用的所有內容群組為一個功能。 請注意，Windows Installer 可讓多個功能共用元件，因此，如果您有用於多個層級的內容，您可以將該內容新增至所有必要層級的功能，而不需複寫內容。 所有這些功能都應標示為「已公告」，這表示它們一開始不會安裝，但可以在稍後視需要安裝。

-   需要檔案時，請先使用函式 [**MsiQueryFeatureState**](/windows/desktop/api/msi/nf-msi-msiqueryfeaturestatea)來檢查是否已安裝檔案。

    如果尚未安裝 (也就是它的狀態是 INSTALLSTATE \_ 通告) ，請呼叫函式 [**MsiConfigureFeature**](/windows/desktop/api/msi/nf-msi-msiconfigurefeaturea) ，以在本機安裝此功能。 在檔案安裝之後開啟檔案時，請呼叫 [**MsiGetComponentPath**](/windows/desktop/api/msi/nf-msi-msigetcomponentpatha) 來判斷檔案的路徑。 雖然這種情況並不是絕對必要 (因為內容一律會先安裝到硬碟上，才能) ，因此除了安裝隨選安裝之外，還可讓您更輕鬆地支援最少量的安裝。

-   可能的話，請預期很快就會需要什麼內容，並在閒置時間于背景安裝。

    當遊戲的時間點不需要電腦的每個上一盎司效能時，最適合使用背景安裝;例如，顯示簡介影片、剪下場景、功能表等等。

-   在遊戲的 [選項] 功能表中建立選項，以強制安裝所有剩餘的內容。

    若要執行這項操作，請建立一個功能，此功能是所有隨選安裝功能的父系，然後呼叫 [**MsiConfigureFeature**](/windows/desktop/api/msi/nf-msi-msiconfigurefeaturea) 在本機安裝此主要功能。 這會導致子功能也會安裝在本機。

-   內容版面配置應該類似于最基本的安裝，不同之處在于內容應該只與可能同時需要的其他內容一起叢集 (例如，一個層級的所有內容都應該一起) 。

## <a name="post-installation-game-play"></a>後續安裝 Game-Play

### <a name="autorun"></a>自動

若要播放已安裝的遊戲，使用者只需要在磁片磁碟機紙匣中放置安裝光碟。 光碟上自動執行可執行檔的第一件事，就是檢查遊戲是否已安裝，如果是，請啟動遊戲。 假設遊戲是使用以 Windows Installer 為基礎的安裝程式來安裝，則會透過單一呼叫函式 [**MsiQueryProductState**](/windows/desktop/api/msi/nf-msi-msiqueryproductstatea)來判斷是否已安裝遊戲。

### <a name="converting-an-install-on-demand-installation-to-a-full-installation"></a>將安裝隨選安裝轉換成完整安裝

當安裝隨選安裝讓使用者可以比完整安裝更快地開始播放遊戲時，使用者可能會想要將其餘的遊戲內容明確地安裝到本機硬碟上。 使用者可能想要能夠在不需要來源媒體的情況下播放遊戲，或可能只是想要避免因隨選內容安裝所導致的遊戲時間較長的載入時間。 如果遊戲的設定使用 Windows Installer，遊戲可在遊戲中選項 UI 提供選項，以完成安裝其餘內容。 當使用者選取此選項時，遊戲可以呼叫 [**MsiConfigureFeature**](/windows/desktop/api/msi/nf-msi-msiconfigurefeaturea) 來強制在本機安裝其餘的功能;不需要產生個別的安裝應用程式來這麼做。

### <a name="maintenance-of-game-software-and-content"></a>遊戲軟體和內容的維護

Windows 遊戲的主控台遊戲有一項優點，就是發行者可以在初始發行之後，將更新發行至遊戲的相對便利性。 無論這些更新是否會導入新的內容，或只是修正錯誤，請務必盡可能讓終端使用者的更新程式更簡單。 對於線上遊戲來說，更新程式更重要，因為這通常需要所有使用者執行最新版本的遊戲才能連接。

### <a name="checking-for-updates-automatically"></a>自動檢查更新

使用者不一定要記得尋找修補程式。 如果遊戲有可用的更新，使用者應該至少收到通知，而且在理想的情況下，應該已經下載修補程式。

檢查更新的一個簡單方式，就是使用特定的 URL 連接到發行者所裝載的 Web 服務器，並下載一個文字檔來指定最新可用版本的遊戲版本號碼，以及下載封裝以將遊戲更新至最新版本的 URL。

每次使用者玩遊戲時檢查更新，都足以確保使用者執行的是最新版本。 但是，如果在使用者嘗試播放遊戲之前立即探索到新的更新，使用者可能會被迫延遲播放遊戲，直到更新下載完成為止。 針對大型更新或慢速連線，此延遲可能是以小時為單位。 為了避免在播放遊戲之前強制使用者等待，遊戲可以使用工作排程器來排程定期檢查是否有新的更新。 如果偵測到更新，則遊戲可以立即開始下載更新，如此一來，當使用者下一次玩遊戲時，可能會完全下載並準備安裝。

### <a name="downloading-patches-automatically"></a>自動下載修補程式

一旦遊戲偵測到有新的更新可供使用，就應該立即開始下載更新。 因為檢查更新的工作通常會在背景以無訊息模式執行，所以下載必須盡可能不顯眼。 背景智慧型傳送服務 (位) 是一種作業系統功能，可讓應用程式即使在應用程式本身未執行的情況下，也可以從網際網路下載檔案。 BITS 下載作業只會在使用者登入時執行，而且只有在電腦已連線到網路時才會執行。 BITS 不會嘗試強制電腦自行連接到網路。 如果使用者從網路中斷連線或登出，BITS 工作會暫停，並會在使用者下次登入並聯機到網路時繼續下載。 應用程式可將其 BITS 作業設定為僅使用其他會保持未使用的網路頻寬，以防止工作影響可能使用 (網路的任何其他應用程式的效能，例如，線上遊戲) 。 BITS 可在 Windows XP 與 Windows 2000 Service Pack 3 上取得。

## <a name="other-resources"></a>其他資源

如需本文所參考技術的詳細資訊，請參閱 MSDN Library 的相關章節：

-   [Windows Installer](/windows/desktop/Msi/windows-installer-portal)
-   [工作排程器](/windows/desktop/TaskSchd/task-scheduler-start-page)
-   [背景智慧型傳送服務](/windows/desktop/Bits/background-intelligent-transfer-service-portal) (位) 

如需使用遊戲 Windows Installer 的詳細資訊，請收聽下個月的《駕駛 DirectX 》專欄：「遊戲開發人員的 Windows Installer 簡介」。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**MsiConfigureFeature**](/windows/desktop/api/msi/nf-msi-msiconfigurefeaturea)
</dt> <dt>

[**MsiQueryProductState**](/windows/desktop/api/msi/nf-msi-msiqueryproductstatea)
</dt> <dt>

[**MsiQueryFeatureState**](/windows/desktop/api/msi/nf-msi-msiqueryfeaturestatea)
</dt> <dt>

[**MsiGetComponentPath**](/windows/desktop/api/msi/nf-msi-msigetcomponentpatha)
</dt> </dl>

 

 
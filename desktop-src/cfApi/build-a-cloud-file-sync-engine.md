---
description: 瞭解如何使用雲端檔案 API 來建立使用預留位置檔案的雲端檔案同步處理引擎。
title: 建立支援預留位置檔案的雲端同步處理引擎
ms.topic: article
ms.date: 11/12/2020
ms.openlocfilehash: d7d1efae4a56e6f52473002953730fb9f1f9459f1ed8dc82e0ba75ddebf05dc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118551567"
---
# <a name="build-a-cloud-sync-engine-that-supports-placeholder-files"></a>建立支援預留位置檔案的雲端同步處理引擎

同步處理引擎是同步檔案的服務，通常是在遠端主機和本機用戶端之間。 Windows 上的同步處理引擎通常會透過 Windows 檔案系統和檔案總管，將這些檔案呈現給使用者。 在 1709 Windows 10 之前，Windows 中的同步處理引擎支援僅限於情節中立的臨機動作表面，例如檔案總管的流覽窗格、Windows 系統匣，以及 (檔案系統篩選器驅動程式的更多技術應用程式。

Windows 10 版本 1709 (也稱為「秋季建立者」更新) 引進「雲端檔案」 *API*。 此 API 是新的平臺，可正規化對同步引擎的支援。 雲端檔案 API 以提供許多新優勢給開發人員和使用者的方式，支援同步處理引擎。

雲端檔案 API 包含下列原生 Win32 api 和 Windows 執行階段 (WinRT) api：

* [雲端篩選 api](cloud-filter-reference.md)：這個原生 WIN32 API 會在使用者模式與檔案系統之間的界限提供功能。 此 API 會處理預留位置檔案和目錄的建立和管理。
* [Windows。儲存體。提供者命名空間](/uwp/api/windows.storage.provider)：此 WINRT API 可讓應用程式設定雲端存放裝置提供者，並向作業系統註冊同步根。

> [!NOTE]
> 雲端檔案 API 目前不支援在 UWP 應用程式中執行雲端同步引擎。 雲端同步引擎必須在桌面應用程式中執行。

## <a name="supported-features"></a>支援的功能

雲端檔案 API 提供下列功能來建立雲端同步引擎。

### <a name="placeholder-files"></a>預留位置檔案

* 同步處理引擎可以建立只針對 filesystem 標頭使用 1 KB 儲存空間的預留位置檔案，而且會在正常使用方式下自動以提供至完整檔案。 預留位置檔案會以一般檔案的形式呈現給應用程式，並在 Windows Shell 中呈現給終端使用者。
* 預留位置檔案會從 Windows 核心垂直整合至 Windows Shell，而與預留位置檔案的應用程式相容性通常是不成問題的問題。 無論您是使用檔案系統 Api、命令提示字元或桌面或 UWP 應用程式來存取預留位置檔案，檔案都不需要額外的程式碼變更即可以提供，而且該應用程式可以正常使用該檔案。
* 檔案可以有三種狀態：
  * **預留位置** 檔案：檔案的空白標記法，而且只有在同步處理服務可用時才可使用。
  * **完整** 檔案：已隱含水合檔案，而且如果需要空間，系統可能會凍結該檔案。
  * 已釘選的 **完整** 檔案：使用者透過檔案總管明確水合了檔案，而且保證可以離線使用。

下圖示范如何在檔案總管中顯示預留位置、完整和固定的完整檔案狀態。

  ![檔案總管中的三個檔狀態範例](images/cloud-file-states-file-explorer.png)

### <a name="standardized-sync-root-registration"></a>標準化的同步根目錄註冊

* 註冊同步根很簡單且標準化。 這包括在檔案總管的導覽窗格中建立品牌化節點，如下列螢幕擷取畫面所示。 您可以將根建立為個別的最上層專案，或做為父群組的子系。

  ![檔案總管中的同步根專案範例](images/register-sync-root-file-explorer.png)

### <a name="shell-integration"></a>Shell 整合

* 狀態圖示：
  * 雲端檔案 API 提供檔案總管和 Windows 桌面上所顯示的標準化、自動序列化狀態圖示。
  * 除了用於序列化狀態的標準 Windows 狀態圖示之外，您還可以提供其他服務特定屬性的自訂狀態圖示。
  * 取代舊版圖示重迭 Shell 擴充功能。
* 進度指示：
  * 開啟花費超過幾秒鐘以提供的預留位置檔案將會顯示序列化進度。 進度會顯示在幾個位置，視內容而定：
    * 在 [複製引擎] 對話方塊視窗中。
    * 內嵌進度會顯示在檔案總管的檔案旁邊。
    * 如果檔案未在使用者的特定指示中開啟，則會顯示快顯通知來通知使用者，並提供方法來控制非預期的序列化活動。
* 縮圖和中繼資料：
  * 預留位置檔案可擁有豐富的服務提供縮圖和擴充的檔案中繼資料，以提供使用者順暢的檔案總管體驗。
* 檔案總管流覽窗格：
  * 向雲端檔案 API 註冊同步根目錄會導致同步根 (與圖示和自訂名稱) 出現在檔案總管的流覽窗格中。
* 檔案總管內容功能表：
  * 使用雲端檔案 API 註冊同步根目錄會自動提供數個動詞 (功能表項目，) 在檔案總管的內容功能表中，讓使用者控制其檔案的序列化狀態。
  * 您可以使用傳統型橋接器相容的 api，將其他動詞新增至內容功能表的這個區段。
* File 序列化的使用者控制：
  * 使用者一律可以控制檔案序列化，即使使用者未明確水合檔案也是一樣。 會顯示互動式快顯通知，讓背景序列化警示使用者並提供選項。 下圖示范 hydrating 檔案的快顯通知。
    ![針對背景檔案序列化顯示的互動式快顯範例](images/file-hydration-interactive-toast.png)
  * 如果使用者透過互動式快顯從 hydrating 檔案封鎖應用程式，他們可以在 **設定** 的 [自動檔案 **下載**] 頁面中解除封鎖應用程式。
    ![自動下載檔案設定的螢幕擷取畫面](images/allow-automatic-file-downloads-setting.png)
* Windows 10 Insider preview 組建19624和更新版本中支援的 (連結複製引擎作業) ：
  * 雲端儲存體提供者可以註冊 shell 複製攔截器，以便監視其同步根內的檔案作業。
  * 提供者會將其同步根登錄機碼底下的 **CopyHook** 登錄值設定為其 COM 本機伺服器物件的 CLSID，以註冊其複製攔截。 這個本機伺服器物件會執行 [IStorageProviderCopyHook](../shell/nn-shobjidl-istorageprovidercopyhook.md) 介面。

### <a name="desktop-bridge"></a>傳統型橋接器

* 使用雲端檔案 api 的同步處理引擎是設計來使用[傳統型橋接器](/windows/uwp/porting/desktop-to-uwp-root)作為實作為需求。

## <a name="cloud-mirror-sample"></a>雲端鏡像範例

[雲端鏡像範例](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/CloudMirror)說明如何建立使用雲端檔案 API 的解決方案。 它不是用來做為實際執行程式碼。 它缺乏健全的錯誤處理，並且會盡可能容易理解。 因為它只會鏡像本機磁片上的本機資料夾，所以稱為「雲端鏡像」。 您可以指定要用來代表您的雲端檔案伺服器的伺服器資料夾，以及用來指定同步根路徑的用戶端資料夾。 最上層節點會出現在檔案總管的流覽窗格中，稱為 **TestStorageProviderDisplayName**，而此節點會對應至指定的用戶端資料夾。

進行同步處理時，這些是完全開發的雲端檔案同步處理提供者必須實行的專案：

* 當同步處理根檔案只是預留位置時，服務會負責複製檔案的內容以進行序列化。 這會在範例中執行。
* 當同步處理根檔案是完整檔案，且雲端服務中的檔案內容變更時，服務會負責通知本機同步用戶端變更，而本機同步處理用戶端必須根據自己的規格來處理合併。 此範例不會執行這項工作。
* 當同步處理根檔案是完整檔案，且同步根路徑中的檔案內容 (本機用戶端) 變更時，本機同步處理用戶端必須通知雲端服務，並根據自己的規格來處理合併。 本機檔案變更通知會在範例中執行，但不會執行任何動作。

### <a name="use-the-sample"></a>使用範例

1. 在您的本機硬碟上建立兩個資料夾。 其中一個將作為伺服器，另一個作為用戶端。
2. 將一些檔案加入到伺服器資料夾。 請確定用戶端資料夾是空的。
3. 在 Visual Studio 中開啟雲端鏡像範例。 將 **CloudMirrorPackage** 專案設定為啟始專案，然後建立並執行範例。 當此範例出現提示時，請輸入您的伺服器和用戶端資料夾的兩個路徑。 之後，您會看到含有診斷資訊的主控台視窗。
4. 開啟檔案總管並確認您看到 **TestStorageProviderDisplayName** 節點，以及您複製到伺服器資料夾中所有檔案的預留位置。 若要模擬嘗試在不使用選擇器的情況下開啟檔案的應用程式，請將數個影像複製到伺服器資料夾。 按兩下同步根資料夾中的其中一個，並確認它產生。 然後，開啟相片應用程式。 應用程式會在背景預先載入連續的檔案，讓使用者更有可能不會在查看其他圖片時遇到延遲。 您可以透過快顯通知或在檔案總管觀察背景凍結的發生情形。
5. 在檔案總管中的檔案上按一下滑鼠右鍵以顯示操作功能表，並確認您看到 [ **TestCommand** ] 功能表項目。 按一下這個功能表項目會顯示訊息方塊。
6. 若要停止此範例，請將焦點設定至主控台輸出，然後按下 **ctrl-c**。 這會清除同步根目錄註冊，以便將提供者卸載。 如果範例損毀，同步根可能仍會保持註冊。 這會導致每次您按下任何程式時都重新開機檔案總管，然後系統會提示您輸入假的用戶端和伺服器位置。 如果發生這種情況，請從您的電腦卸載 **CloudMirrorPackage** 範例應用程式。

### <a name="sample-architecture"></a>範例架構

此範例刻意簡單明瞭。 它會使用靜態類別，使其不需要傳遞實例指標。 以下是範例中的主要類別：

* **FakeCloudProvider**：這個最上層類別會控制下列背景工作類別：
  * **CloudProviderRegistrar**：使用 Windows Shell 來註冊同步的根資訊。
  * **預留位置**：在同步根路徑中產生預留位置檔案。
  * **ShellServices**：為內容功能表、縮圖和其他服務，構造 Windows Shell 提供者。
  * **CloudProviderSyncRootWatcher**：具現化 DirectoryWatcher，以監視同步處理根路徑的變更，並對變更採取動作。
  * **FileCopierWithProgress**：從伺服器資料夾將檔案複製到用戶端資料夾的速度緩慢，以模擬從真實的雲端伺服器下載這些檔案。 提供進度指示，讓快顯通知和檔案總管 UI 向使用者顯示有用的資訊。

除了上述類別之外，此範例也提供數個協助程式類別，以提示使用者提供資料夾和某些公用程式。 **TestExplorerCommandHandler**、 **CustomStateProvider**、 **ThumbnailProvider** 和 **UriSource** 都是 Shell 服務提供者的範例。

## <a name="cloud-files-api-architecture"></a>雲端檔案 API 架構

雲端檔案 API 中儲存體堆疊的核心是稱為 cldflt.sys 的檔案系統微篩選器驅動程式。 此驅動程式可做為使用者應用程式與同步處理引擎之間的 proxy。 您的同步處理引擎知道如何視需要下載及上傳資料，但 cldflt.sys 使用 Shell 來呈現檔案，就像雲端資料在本機可用一樣。

Cldflt.sys 目前僅支援 NTFS 磁片區，因為它相依于 NTFS 特有的某些功能。

系統中有許多檔案系統微篩選器驅動程式，且可同時在指定的磁片區上啟用。 雲端檔案 API 最感興趣的驅動程式是防毒程式檔案系統篩選器。

檔案系統微架構驅動程式是由稱為「篩選管理員」的特殊核心模式元件所管理和支援。 在許多其他的職責中，篩選管理員會透過稱為篩選訊息埠的結構，協助篩選和使用者模式元件之間的未篩選通訊。

## <a name="hydration-policies"></a>序列化原則

Windows 支援各種[主要序列化原則](/windows/desktop/api/cfapi/ne-cfapi-cf_hydration_policy_primary)和[次要序列化原則](/windows/desktop/api/cfapi/ne-cfapi-cf_hydration_policy_modifier)修飾詞。 主要序列化原則的順序如下：

  **Always full > Full > 漸進 > 部分**

應用程式和同步處理引擎都可以定義其慣用的主要序列化原則。 如果未指定，則應用程式和同步引擎的預設序列化原則為漸進式。

雲端檔案的序列化原則是在檔案開啟時，透過下列公式來決定：

  ```File hydration policy = max(app hydration policy, provider hydration policy)```

例如，假設使用者嘗試使用 Contoso PDF 檢視器開啟儲存在 Fabrikam 雲端磁片磁碟機上的 PDF 檔案，但該檔案未指定慣用的序列化原則。 因此，應用程式序列化原則是漸進式序列化，在此案例中為預設值。 不過，因為 Fabrikam 雲端磁片磁碟機是完整的序列化同步處理引擎，所以檔案上的最後一個序列化原則會變成完整的序列化，這會導致檔案在第一次存取時完全水合。 當同步處理引擎支援漸進式序列化，但應用程式的喜好設定為完整序列化時，就會發生相同的結果。

請注意，檔案序列化原則無法在檔案開啟後變更。

## <a name="compatibility-with-applications-that-use-reparse-points"></a>與使用重新分析點的應用程式相容

雲端檔案 API 會使用重新 [分析點](/windows/desktop/FileIO/reparse-points)來實行預留位置系統。 重新剖析點的常見誤解是它們與符號連結相同。 這種誤解有時候會反映在應用程式的執行中，因此，許多現有的應用程式會在遇到任何重新分析點時遇到錯誤。

為了減輕這種相容性問題，雲端檔案 API 一律會隱藏所有應用程式的重新分析點，除了同步引擎和主映射位於 **% systemroot%** 底下的進程。 瞭解重新分析點的應用程式，可以強制平臺使用 [RtlSetProcessPlaceholderCompatibilityMode](/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-rtlsetprocessplaceholdercompatibilitymode) 或 [RtlSetThreadProcessPlaceholderCompatibilityMode](/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-rtlsetthreadplaceholdercompatibilitymode)來公開雲端檔案 API 重新分析點。
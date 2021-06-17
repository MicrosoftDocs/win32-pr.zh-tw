---
description: XAudio 2.9 的可轉散發版本開發人員指南
ms.assetid: ''
title: XAudio 2.9 的可轉散發版本開發人員指南
ms.topic: article
ms.date: 10/17/2019
ms.openlocfilehash: a73ebd01d599446dc96e1e6735d8af572203a23b
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262590"
---
# <a name="developer-guide-for-redistributable-version-of-xaudio-29"></a>XAudio 2.9 的可轉散發版本開發人員指南

XAudio 2.9 的版本是以 [NuGet 套件](/nuget/what-is-nuget)的形式提供。 開發人員可以將此版本的 XAudio 2.9 與其應用程式一起轉散發。 這可讓應用程式在較舊版本的 Windows 上使用 XAudio 2.9，這些版本不包含 XAudio 2.9 作為作業系統映射的一部分。 因為 XAudio 2.7 自2010起尚未更新，所以最好使用此可轉散發套件，因為從 DirectX SDK 轉散發 XAudio 2.7。

請務必流覽 [Directx 登陸頁面](https://devblogs.microsoft.com/directx/landing-page/) ，以取得更多適用于 directx 開發人員的資源。

## <a name="supported-platforms"></a>支援的平台

XAudio 2.9 NuGet 套件 (*Microsoft. XAudio2 可轉散發套件。 \*nupkg*) 包含32位和64位版本的 DLL，可執行 XAudio 2.9 API。 DLL 稱為 XAUDIO2 \_9REDIST.DLL。 此 DLL 可在 Windows 7 SP1、Windows 8、Windows 8.1 和 Windows 10 上運作。

當 DLL 在 Windows 10 系統上使用時，它會檢查屬於作業系統的 XAUDIO29.DLL 的版本號碼 \_ ，如果作業系統較新，它就會將所有 API 呼叫委派給 \_ 作業系統中的 XAUDIO29.DLL。 這可確保應用程式一律使用目前平臺上可用的最新 XAudio 2.9 版本。

DLL 不適合 Xbox One。 如果用於 Xbox One，則 DLL 一律會將所有 API 呼叫委派給 \_ Xbox One 作業系統中的 XAUDIO29.DLL。

DLL 並非適用于 UWP 應用程式。 UWP 應用程式應該使用屬於 \_ 作業系統一部分的 XAUDIO29.DLL。

## <a name="installing-the-nuget-package"></a>安裝 NuGet 封裝

安裝 NuGet 套件最簡單的方式，就是在 Microsoft Visual Studio 中使用 [nuget 封裝管理員](/nuget/consume-packages/install-use-packages-visual-studio) 。 如果您這樣做，您的 Visual Studio 專案檔將會自動更新，以包含 *XAudio2*。 *.Targets* 檔案會將包含 XAudio2 標頭檔的 include 資料夾，新增至專案包含路徑的集合。 *.Targets* 檔案也會讓您的 .DLL 或 .EXE 連結 XAUDIO2REDIST。LIB 和 XAPOBASEREDIST。自由。

程式庫 XAPOBASEREDIST。只有當您想要 impement 自訂 XAudio 處理物件 (XAPO) ，而且如果未使用，也可以將它從 *XAudio2* 的可轉散發套件中移除時，才需要 LIB。

您也可以使用其他工具來解壓縮 NuGet 套件的內容，甚至重新命名副檔名以 .zip，並使用任何 ZIP 解壓縮工具工具解壓縮檔案。

> 另外還有一個 ``xaudio2redist`` 可供 [VC + + 封裝管理員](https://github.com/microsoft/vcpkg)使用的埠。

## <a name="compiling-your-app"></a>編譯您的應用程式

### <a name="choosing-which-headers-to-include"></a>選擇要包含的標頭

XAudio 2.9 NuGet 套件包含 Windows 10 SDK 中所含的相同 XAudio2 標頭檔。 不過，標頭檔已對它們進行一些調整，以確保您可以使用它們，同時明確地以所有 [支援的平臺](#supported-platforms)為目標，包括舊版的 Windows。

如果您在 Microsoft Visual Studio 中使用 NuGet 封裝管理員 [安裝 nuget 套件](#installing-the-nuget-package) ，則標頭檔的路徑會放置在 Windows SDK 標頭檔的路徑前面。 這表示，如果專案中的程式碼包含 XAUDIO2。H 標頭，它會從 NuGet 套件中挑選跨平臺的標頭。 這通常是所需的行為。

如果您手動將 include 標頭的路徑新增至專案，請務必小心，因為以錯誤順序指定這些標頭可能會導致作業系統版本的特定 [XAUDIO2。](/windows/win32/api/xaudio2/) 要包含在 Windows SDK 中的 H，而不是 XAUDIO2 的跨平臺版本。

為了使標頭包含較不容易出錯的標頭，NuGet 套件包含每個標頭的版本，並附加「可轉散發套件」。 例如，除了 XAUDIO2 之外。H，NuGet 套件也包含 XAUDIO2REDIST。 如果您想要的話，您的程式碼可以直接包含 XAUDIO2REDIST。H 以消除所使用的標頭檔的任何混淆。 包含-可轉散發套件。H 版本的標頭檔，包含檔案目錄在專案檔中所列的順序並不重要。

請注意，如果您的應用程式也是針對 Xbox One 進行編譯，您應該繼續包含 XAUDIO2。H 針對 Xbox One 進行編譯時，會從 XAUDIO2REDIST 中排除某些特定 Xbox One 的 Api。 此 NuGet 套件不適合 Xbox One。

### <a name="loading-the-dll"></a>載入 DLL

建議您將應用程式與 XAUDIO2REDIST 連結。LIB，並 \_ 將 XAUDIO29REDIST.DLL 安裝在與您應用程式可執行檔相同的資料夾中。 這會導致 \_ 在您的可執行檔啟動時，立即載入 XAUDIO29REDIST.DLL。 但是，如果您想要的話，也可以使用 [**LoadLibraryEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexw) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 來 \_ 視需要載入 XAUDIO29REDIST.DLL。 如果您的應用程式不一定需要使用 XAudio2 Api，這是很好的解決方案。 但是如果您這樣做，您應該在 \_ 應用程式結束之前讓 XAUDIO29REDIST.DLL 載入，因為嘗試卸載 dll 可能會在背景執行緒仍在 DLL 中執行程式碼時造成當機。

不同于較舊的 XAudio 2.7，無法使用 CoCreateInstance 載入 DLL。

### <a name="verifying-the-dll-signature"></a>確認 DLL 簽章

XAUDIO2 \_9REDIST.DLL 二進位檔是由 Microsoft 使用 sha-1 簽章簽署。 嘗試驗證簽章的任何程式碼（例如遊戲的防鋸齒模組）都必須支援 SHA-1。 請注意，Windows 7 SP1 原本並不支援 SHA-2，需要更新才能新增該功能。 更新會以 [KB4474419](https://support.microsoft.com/help/4474419/sha-2-code-signing-support-update)的形式提供。

## <a name="testing"></a>測試

### <a name="spatial-sound-in-newer-versions-of-windows-10"></a>較新版本的 Windows 10 中的空間音效

從 Windows 10 1903 更新開始，如果滿足特定條件，XAudio 2.9 會自動使用 [虛擬環繞音效](#spatial-sound-and-virtual-surround)。 我們建議在 Windows 10 1903 (或較新的) 上產生多聲道音效的測試遊戲，以驗證遊戲是否如預期般運作。

#### <a name="enabling-spatial-sound"></a>啟用空間音效

使用者可以在 Windows 系統匣中，以滑鼠右鍵按一下喇叭圖示來啟用空間音效格式。 

如果使用 XAudio2 API 的進程被 Windows Game Bar 辨識為遊戲，XAudio 2.9 將只會使用使用者所選取的空間音效格式。 在開發期間，Game Bar 可能尚未將進程辨識為遊戲。 若要變更此設定，請使用 Win + G 鍵盤短暫剪下，以在遊戲執行時帶出 Game Bar。 然後按一下 [設定] 圖示，並選取 [記住這是遊戲] 核取方塊。

#### <a name="opting-out-from-spatial-sound"></a>退出空間音效

有一種方法可以在 [**IXAudio2：： CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice)中指定 [**AUDIO_STREAM_CATEGORY**](/windows/win32/api/audiosessiontypes/ne-audiosessiontypes-audio_stream_category)參數的特定值，以選擇不要讓 XAudio2 使用空間音效編碼器。 

這些類別的空間音效已啟用：

* AudioCategory_ForegroundOnlyMedia
* AudioCategory_GameEffects
* AudioCategory_GameMedia
* AudioCategory_Movie
* AudioCategory_Media

如果指定了下列任何類別，則不會啟用空間音效：

* AudioCategory_Other
* AudioCategory_Communications
* AudioCategory_Alerts
* AudioCategory_SoundEffects
* AudioCategory_GameChat
* AudioCategory_Speech

### <a name="error-handling"></a>錯誤處理

請務必測試您的遊戲是否可以處理音訊裝置的變更，例如，當耳機插上或拔下時。 這應該使用只支援 44.1 kHz 取樣率的耳機進行測試。 許多低終端 USB 耳機和藍牙耳機僅支援 44.1 kHz。 48 kHz 取樣率和 44.1 kHz 取樣率之間的轉換可能會造成錯誤，即使使用 [虛擬音訊端點](#virtual-audio-endpoint) 功能也是一樣。 如果耳機也支援 48 kHz，就不會發生此錯誤。 請注意，Windows 7 SP1 上無法使用虛擬音訊端點功能。

XAudio 2.9 在無法從音訊端點的變更中自動復原時傳回的錯誤碼是 [XAUDIO2 \_ E \_ 裝置 \_ 失效](xaudio2-error-codes.md)。 不過，我們建議應用程式不要對錯誤碼具有特定值的相依性進行硬式編碼。

若要收到錯誤的通知，應用程式應該執行 [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) 介面，並叫用 [**IXAudio2：： RegisterForCallbacks**](xaudio2-callbacks.md) 方法，以提供該介面的指標。 如果播放期間發生錯誤，XAudio2 API 將會叫用應用程式的 [**IXAudio2EngineCallback：： OnCriticalError**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-oncriticalerror) 的執行。

請注意，如果音訊管線已暫停，則不一定會叫用 [**IXAudio2EngineCallback：： OnCriticalError**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-oncriticalerror) 。 例如，如果使用者將應用程式最小化，或因為任何原因而暫停應用程式，則可能會暫停播放音訊。 如果音訊裝置在這段時間內發生變更，則只有當應用程式叫用 [**IXAudio2：： StartEngine**](/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-startengine) 和/或叫用 [**IXAudio2SourceVoice：： Start**](/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start)時，才會傳回此錯誤。 如果您的應用程式可以暫停播放，則應該在播放暫停時測試變更音訊裝置，以確認應用程式仍然可以從這種情況復原。

## <a name="xaudio-29-api-differences-compared-to-xaudio-27"></a>相較于 XAudio 2.7，XAudio 2.9 API 差異

本節提供 XAudio 2.7 與可轉散發版本的 XAudio 2.9 之間的一些 API 差異摘要。

### <a name="supported-formats"></a>支援的格式

XAudio 2.9 在電腦上支援下列輸入格式：

* 線性16位 PCM
* 線性 32-位浮點數 PCM
* 16位 ADPCM
* xWMA

只有 Xbox One 才支援 XMA 格式。

### <a name="preferred-cpu-core"></a>慣用 CPU 核心

您可以指定哪個 CPU 核心 XAudio 2.9 應該用於其音訊處理執行緒。 不過，通常偏好讓 XAudio 2.9 自行選擇此值。 這是藉由將 [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create)呼叫中的 **XAudio2Processor** 參數設定為 XAUDIO2 \_ 使用 \_ 預設 \_ 處理器來完成。 

XAudio 2.9 會在 Xbox One 上選擇與電腦上不同的 CPU 核心。 IXAudio2Extension：： GetProcessor 方法可以用來判斷已選擇的 CPU 核心 XAudio2。

### <a name="virtual-audio-endpoint"></a>虛擬音訊端點

XAudio 2.9 在 Windows 8 或更新版本上執行時，預設會使用虛擬音訊端點。 這表示，如果使用 XAudio 2.9 時的預設音訊端點變更，它會嘗試自動切換至新的音訊端點。 當預設音訊端點是透過 USB 連接的一對耳機，然後使用者拔除耳機時，會發生這種情況的範例。 這會導致喇叭成為新的預設音訊端點。

如果應用程式在叫用 [**IXAudio2：： CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice)時指定特定的音訊格式，XAudio 2.9 可能無法執行此參數。 例如，如果應用程式指定使用 48 kHz 取樣率，而新的音訊裝置只支援 44.1 kHz，則自動切換將會失敗，而 XAudio 2.9 會回報 [XAUDIO2 \_ E \_ 裝置 \_ 失效](xaudio2-error-codes.md) 錯誤。

藉由將 [**XAUDIO2 \_ NO \_ 虛擬 \_ 音訊 \_ 用戶端**](xaudio2-boundary-values-and-flags.md) 旗標傳入 [**IXAudio2：： CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice)，應用程式可以選擇不使用虛擬音訊端點。

在 Windows 7 SP1 上無法使用虛擬音訊端點。 **XAUDIO2 \_ no \_ VIRTUAL \_ AUDIO \_ CLIENT** 旗標不會影響 Windows 7 SP1。

### <a name="audio-categories"></a>音訊分類

應用程式應指定其音訊串流的類別。 這是藉由在叫用 [**IXAudio2：： CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice) 方法時，提供來自 AudioCategory 列舉的值來完成。 例如，AudioCategory_GameEffects。 音訊類別會影響 Windows 處理音效的方式，或在音量控制台中代表音訊串流的方式。 如果自動啟用 [虛擬環繞音效](#spatial-sound-and-virtual-surround) ，音訊類別也會受到影響。

### <a name="duration-of-audio-processing-quantum"></a>音訊處理量子的持續時間

在大部分的電腦上，XAudio 2.9 會以10毫秒的區塊處理音訊。 這稱為處理量子。 不過，在某些硬體上，此量子的持續時間可能會不同于10毫秒。 需要知道確切量子的應用程式可以叫用 IXAudio2Extension：： GetProcessingQuantum 方法來取得值。

### <a name="spatial-sound-and-virtual-surround"></a>空間音效和虛擬環繞

從 Windows 10 1903 更新開始，如果滿足特定條件，XAudio 2.9 會自動使用虛擬環繞音效。 我們建議在 Windows 10 1903 (或較新的) 上產生多聲道音效的測試遊戲，以驗證遊戲是否如預期般運作。 如需如何測試這項功能的討論，請參閱「 [測試空間音效](#spatial-sound-in-newer-versions-of-windows-10) 」一節。

一般來說，XAudio 2.9 會折迭任何多頻道音訊，以符合音訊端點所支援的「實體」音訊聲道數目。 例如，如果遊戲提供7.1 聲道音訊來源，但音效是在耳機上播放，則 XAudio 2.9 會使用業界標準的折迭矩陣，將7.1 頻道音訊折迭為身歷聲。 如果電腦連線到 HDMI 音訊端點，則7.1 通道音訊將會透過 HDMI 連線以現狀傳輸。

Windows 10 使用集中式編碼器將音訊編碼為使用者選取的 [空間音效](../coreaudio/spatial-sound.md) 格式，以新增空間音訊的支援。 Windows 10 隨附于名為 Windows Sonic 的空間音效格式。 您可以從 Microsoft Store 下載其他格式，例如 Dolby Atmos for Headphones。 某些空間音效格式（例如 Windows Sonic 和 Dolby Atmos for Headphones）是設計用於身歷聲音訊端點。 這些格式會使用可達成「虛擬」環繞音效效果的專屬演算法，將「環繞音效」折迭到身歷聲。 換句話說，接聽程式可以觀察3D 空間中不同位置的音效，即使只是戴耳機，或是聆聽一對身歷聲喇叭也一樣。

您可以使用 XAudio 2.9 隨附的 [X3DAudio](x3daudio.md) api 來達成類似效果。 主要差異在於 X3DAudio 需要應用程式開發人員明確地為3D 音訊進行程式設計，而虛擬環繞音效則會自動套用到任何以 tradional 通道為基礎的音效來源。

在 Windows 10 1903 和更新版本的遊戲中，使用 XAudio 2.9 的遊戲將會使用使用者已在音訊端點上啟用的全系統空間音效格式（如果有的話）。 這表示，XAudio 2.9 不會將環繞音效的一般折迭執行至身歷聲。 相反地，環繞音效將會傳遞給空間音效編碼器 (例如，Windows Sonic) ，以達到虛擬環繞音效的效果。

### <a name="createhrtfapo"></a>CreateHrtfApo

[**CreateHrtfApo**](/windows/desktop/api/HrtfApoApi/nf-hrtfapoapi-createhrtfapo)函數僅適用于 Windows 10。 它不會在 XAudio 2.9 可轉散發套件中執行。

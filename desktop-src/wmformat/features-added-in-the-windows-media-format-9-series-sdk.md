---
title: Windows 媒體格式9系列 SDK 中新增的功能
description: Windows 媒體格式9系列 SDK 中新增的功能
ms.assetid: 73c4da27-a456-4845-a35b-edb75aa3f953
keywords:
- Windows媒體格式 SDK，功能
- Windows媒體格式 SDK，新功能
- Windows媒體格式 SDK，同步讀取器
- Windows媒體格式 SDK，以框架為基礎的索引
- Windows媒體格式 SDK，SMPTE 時間碼
- Windows媒體格式 SDK，DirectShow 篩選
- Windows媒體格式 SDK，DRM 寫入功能
- Windows媒體格式 SDK，檔案接收
- 'Windows媒體格式 SDK、DirectX 影片加速 (DXVA) '
- Windows媒體格式 SDK，多頻道音訊
- Windows媒體格式 SDK，浮水印
- Windows媒體格式 SDK，多重語言支援
- Windows媒體格式 SDK，裝置一致性範本
- Windows媒體格式 SDK，編解碼器列舉
- Windows媒體格式 SDK，相互排除
- Windows媒體格式 SDK， (MBR) 多位元率
- Windows媒體格式 SDK，使用智慧型 recompression 進行轉碼
- Windows媒體格式 SDK，智慧型 recompression
- Windows媒體格式 SDK，recompression
- Windows媒體格式 SDK，中繼資料
- Windows媒體格式 SDK，動態圖元外觀比例
- Windows媒體格式 SDK，交錯式影片串流
- Windows媒體格式 SDK，雙通路編碼
- Windows媒體格式 SDK，WMStub .lib
- 同步讀取器，關於
- 以框架為基礎的索引
- SMPTE 時間代碼，關於
- DirectShow 篩選
- 檔案接收，增強功能
- 多頻道音訊，關於
- 浮水印，關於
- 編解碼器，列舉
- 相互排除，關於
- 數位版權管理 (DRM) ，寫入功能
- DRM (數位版權管理) ，書寫功能
- DirectX Video 加速 (DXVA) ，關於
- DXVA (DirectX Video 加速) ，關於
- Advanced Systems Format (ASF) 、多重語言支援
- ASF (Advanced Systems Format) 、多重語言支援
- " (MBR) 的多重位元速率，關於"
- MBR (多位元率) ，關於
- 使用智慧型 recompression 進行轉碼
- 智慧型 recompression
- recompression
- 中繼資料，Windows 媒體格式 SDK
- 動態圖元外觀比例
- 交錯式影片串流
- 雙通路編碼，關於
- 2-通過編碼，關於
- WMStub .lib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76dc0f4a8c0b23ba33409039ae7f1d46ada1b3299790ef82fb98b8714f616117
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119547448"
---
# <a name="features-added-in-the-windows-media-format-9-series-sdk"></a>Windows 媒體格式9系列 SDK 中新增的功能

Windows 媒體格式9系列 SDK 引進了許多改進和功能。 本節概述從舊版 SDK 進行遷移的使用者所具備的優點。

## <a name="synchronous-reading"></a>同步讀取

您可以使用同步呼叫來讀取 ASF 檔案。 以同步方式讀取檔案時，您可以在讀取時變更讀取器的設定。 SDK 的同步讀取作業不支援透過網際網路讀取檔案，但您可以使用標準 COM 介面 **IStream**，從自訂來源讀取。

## <a name="frame-based-indexing"></a>以框架為基礎的索引

您可以根據影片畫面來編制 ASF 檔案的索引。 讀取器和同步讀取器都可以搜尋影片資料流程的框架，並將其他資料流程同步處理至該框架。

## <a name="indexing-and-seeking-with-smpte-time-code"></a>使用 SMPTE 時間碼來編制索引和搜尋

Windows 媒體格式 SDK 可讓您將 SMPTE 時間代碼儲存在 ASF 檔案中。 檔案可以透過 SMPTE 時間程式碼來編制索引，而非同步讀取器和同步讀取器可以搜尋 SMPTE 時間的程式碼索引項目。

## <a name="directshow-filters"></a>DirectShow過濾 器

Windows 媒體格式 SDK 包含兩個 Microsoft DirectShow®篩選器，可讓 DirectShow 型應用程式讀取和寫入 ASF 檔案。 DirectShow 也可讓應用程式從音訊影片裝置捕獲資料，並從各種不同的格式解壓縮資料，然後再將其編碼為 Windows 媒體型內容。

## <a name="enhanced-profiles"></a>增強型設定檔

設定檔可以包含頻寬共用資訊，以及串流優先順序資訊。 頻寬共用可讓您指定兩個或多個資料流程（不論其個別的位元速率為何）永遠不會使用超過指定的頻寬量。 設定檔中共用資料的頻寬純粹僅供參考;SDK 中的任何邏輯都不會強制執行。 資料流程優先順序可讓您針對設定檔中的資料流程指定優先權順序。 如果在播放時沒有足夠的頻寬可正常串流檔案，則可以忽略最低優先順序的資料流程，以改善效能。

## <a name="drm-writing-capability"></a>DRM 寫入功能

除了現有的 DRM 讀取支援，Windows 媒體格式9系列 SDK 還新增了使用 DRM 第1版或 drm 版本7保護來撰寫 ASF 檔案的支援。 這項新功能可提供「即時 DRM」案例，例如即時體育活動或演唱會的每一視圖網路廣播。

## <a name="enhanced-file-sink"></a>增強的檔案接收

9系列版本的 SDK 新增了數個新的檔案接收功能。 您可以設定檔案接收，以停用自動編制新建立之 ASF 檔案的索引。 您也可以選擇將它設定為未緩衝的輸入和輸出。

## <a name="directx-video-acceleration"></a>DirectX 影片加速

DirectX Video 加速 (DXVA) 是一種技術，可讓您以具有 DXVA 功能的圖形配接器，在功能較少的電腦上播放高位速率的影片 (DVD 品質或更好的) 。 您可以使用此 SDK 的 reader 物件，在播放 ASF 檔案時啟用 DirectX Video 加速（如果硬體支援的話）。

## <a name="multichannel-audio"></a>多頻道音訊

您可以編碼和播放多頻道音訊。 Windows Media 音訊 9 Professional 編解碼器支援具有6個通道和8個通道以及高定義身歷聲的格式。

## <a name="watermarking"></a>浮水印

您可以使用數位浮水印來編碼 ASF 檔案，以獲得安全性。 所有浮水印系統在其方法中都不同，但所有內嵌識別碼都是編碼的內容。 浮水印是使用特殊的協力廠商 DirectX®媒體物件 (DMOs) 來執行。

## <a name="support-for-multiple-languages-in-asf-files"></a>在 ASF 檔案中支援多種語言

您可以在多個 ASF 檔案中支援多種語言，包括資料流程和中繼資料。 例如，您可以使用數種語言建立包含音訊串流的影片檔案。 在播放時，使用者可以選取要使用的語言，或您的應用程式可以查詢播放電腦上的系統資訊，並自動選取語言。 中繼資料屬性也可以多次輸入，並以不同語言的值。

## <a name="device-conformance-templates"></a>裝置一致性範本

為了協助將內容設定為特定用戶端裝置，Windows 媒體編解碼器現在支援裝置一致性範本。 每個範本都包含一組已定義的設定和編解碼器功能，這些功能應用於適用于特定平臺類別的媒體。 Windows 媒體編解碼器的最新版本不再支援系統設定檔。 所有設定檔都必須自訂，以符合您的需求。 您可以使用「裝置一致性範本」來協助您設計您的設定檔。

## <a name="expanded-codec-enumeration"></a>擴充的編解碼器列舉

配置檔案管理員物件可以查詢 Windows Media 音訊和影片編解碼器，以取得支援的格式。 您可以設定所抓取格式的參數。 例如，您可以取出 Windows Media 音訊9編解碼器所支援的所有品質型變數位速率格式。

## <a name="improved-mutual-exclusion"></a>改進互斥

您可以建立包含相互排除物件內多個資料流程的命名記錄。 您也可以命名相互排除物件，使其更容易識別。 這可讓您建立相互排除的層級。 例如，檔案可以包含依位元速率和語言相互排斥的資料流程。 以語言為基礎的相互排除牽涉到資料流程群組，每個群組都是由相同語言的資料流程所組成，但位元速率互斥。

## <a name="expanded-multiple-bit-rate-support"></a>擴充的多位元率支援

相互排除支援包含在多個位速率內 (MBR) 音訊，以及串流不同映射大小的影片。

## <a name="attributes-for-streams"></a>資料流程的屬性

您可以將屬性指派給 ASF 檔案中的個別資料流程。 您仍然必須針對 MP3 檔案使用檔案層級的屬性。 這項功能不會將任何方法新增至 SDK，但現有的方法現在會接受零以外的資料流程號碼。

## <a name="transcoding-with-smart-recompression"></a>使用智慧型 Recompression 進行轉碼

Smart recompression 可讓您從高位元速率轉碼 Windows 媒體音訊檔案，其品質比以往更高。

## <a name="expanded-metadata-support"></a>擴充的中繼資料支援

Windows 媒體格式 SDK 提供下列新的中繼資料功能：

-   以索引為基礎的元資料標記，啟用多個具有相同名稱的標記。
-   能夠讀取不含 WMStubDRM .lib 檔案的 DRM 標頭屬性。
-   具有超過 64 kb 相關聯資料的屬性。
-   多種語言的屬性。
-   數十個新的預先定義屬性。

## <a name="dynamic-pixel-aspect-ratio"></a>動態圖元外觀比例

您可以藉由識別資料流程中不同樣本的圖元外觀比例，來容納包含各種內容類型的影片串流。 這可讓播放應用程式提供更好的內容播放。

## <a name="interlaced-video-streams"></a>交錯式影片串流

舊版 Windows 媒體格式 SDK 已提供將 [*交錯*](wmformat-glossary.md)式內容編碼成漸進式掃描影片串流的功能。 從 Windows 媒體格式9系列 SDK 開始，您可以編碼交錯式影片，同時保留其交錯格式。 這可能會導致播放改善，特別是在交錯裝置上，例如電視組。

## <a name="two-pass-encoding"></a>Two-Pass 編碼

新的 Windows 媒體編解碼器可啟用兩個傳遞的編碼。 在兩個階段中編碼的內容可以達到更高品質的輸出。

## <a name="new-speech-codec"></a>新的語音編解碼器

此 SDK 包含新的 Windows Media 音訊9語音編解碼器，最適合用來在使用低位速率的情況下編碼人類聲音。 此編解碼器也可為混合音樂-語音內容提供絕佳的效能。

## <a name="accessible-video-frame-duration"></a>可存取的影片畫面持續時間

您可以讓此 SDK 的寫入器物件將影片畫面的持續時間提供給讀者。

## <a name="streaming-html"></a>串流 HTML

在舊版的 SDK 中，您可以使用指令碼命令來指示您的應用程式開啟網頁。 從 Windows 媒體格式9系列 SDK 開始，您可以將網頁的元件儲存在您的 ASF 檔案中，以確保簡報中沒有任何延隔時間。

## <a name="wmstublib-no-longer-required-for-build-environment"></a>組建環境不再需要 WMStub .lib

Windows 媒體格式 SDK 的組建環境設定從 Windows 媒體格式9系列 sdk 開始變更。 您不再需要為使用此 SDK 的應用程式包含 WMStub。 不過，啟用 DRM 的應用程式仍然必須取得並簽署個別的授權合約，並從 Microsoft 取得唯一的靜態程式庫。 wmla@microsoft.com如需 DRM 程式庫和授權合約的詳細資訊，請洽詢。 如需使用此 SDK 建立專案的詳細資訊，請參閱連結[庫檔案和編譯器設定](library-files-and-compiler-settings.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**關於 Windows 媒體格式 SDK**](about-the-windows-media-format-sdk.md)
</dt> </dl>

 

 





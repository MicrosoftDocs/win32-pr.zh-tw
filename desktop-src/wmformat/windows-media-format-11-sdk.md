---
title: Windows Media Format 11 SDK
description: Windows Media Format 11 SDK
ms.assetid: 875e8914-b861-46f1-9391-8724ff77d26b
keywords:
- Windows Media Format SDK，關於
- Windows Media SDK
- 'Windows Media Format SDK、Advanced Systems Format (ASF) '
- Advanced Systems Format (ASF) 、about
- ASF (Advanced Systems Format) 、about
- Windows Media Format SDK，功能
- Windows Media Format SDK，主要功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 363c268194b476b6d3326a9c57fe1e709d17e2fe
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/09/2020
ms.locfileid: "104463861"
---
# <a name="windows-media-format-11-sdk"></a>Windows Media Format 11 SDK

本檔說明 Microsoft Windows Media Format 軟體發展工具組 (SDK) 並適用于32位和 x64 版本的 SDK。

Windows Media Format SDK 是 Microsoft Windows Media 軟體發展工具組的元件， (SDK) 。 其他元件包含 Windows Media Services SDK、Windows Media 編碼器 SDK、Windows Media Rights Manager SDK、Windows Media 裝置管理員 SDK 和 Windows Media Player SDK。

Windows Media Format SDK 可讓應用程式開發人員存取 Windows Media 格式的元件。 這些元件包括 Advanced Systems 格式 (ASF) 檔案容器、Windows Media 音訊和影片編解碼器、基本網路串流功能，以及數位版權管理。 Windows Media Format SDK 的物件會以較低的層級來操作 Windows Media 的元件;Windows Media SDK 的其他元件包含在較高層級上運作的物件。

Windows Media Format SDK 的主要目的是讓開發人員建立應用程式，以播放、寫入、編輯、加密和傳遞 Advanced Systems 格式 (ASF) 檔和網路串流。 這些檔案和資料流程通常包含使用 Windows Media 音訊和影片編解碼器編碼的音訊和影片內容。 不過，ASF 可以包含任何類型的資料。 如需 Advanced Systems Format 容器結構的詳細資訊，請參閱 [ASF 格式的總覽](overview-of-the-asf-format.md)。

Windows Media Format SDK 的主要功能如下：

-   支援領先業界的編解碼器。 Windows Media Format 11 SDK 包含 Microsoft Windows Media 視訊9編解碼器和 Microsoft Windows Media 音訊9.1 編解碼器。 這兩種編解碼器都提供數位媒體內容的例外編碼。 此版本的新功能是 Windows Media 視訊 9 Advanced Profile 編解碼器，提供廣播影片的優化。 此 SDK 也包含 Microsoft Windows Media 視訊9畫面編解碼器，可在使用者應用程式會話期間壓縮電腦螢幕活動，以及 Windows Media 音訊9.1 語音編解碼器，它會編碼低複雜性的音訊（例如語音），並以智慧方式適應更複雜的音訊（例如音樂），以提供更佳的組合語音音樂案例。
-   支援寫入 ASF 檔。 檔案是根據可自訂的設定檔所建立，可讓您輕鬆地設定和標準化檔案。 您可以使用此 SDK 來寫入超過 2 gb 的檔案，以啟用更長、更高品質的連續檔案。
-   支援讀取 ASF 檔。 此 SDK 提供讀取本機 ASF 檔案，以及讀取透過網路串流處理之 ASF 資料的支援。 此外，也提供許多先進閱讀功能的支援，例如 (MBR) 檔案的原生支援，其中包含多個串流具有以不同位元速率編碼的相同內容。 讀取器會根據播放時的可用頻寬，自動選取要使用的 MBR 串流。
-   透過網路傳遞 ASF 資料流程的支援。 此 SDK 支援透過 HTTP 將 ASF 資料傳遞到網路上的遠端電腦，也支援將資料直接傳遞至遠端 Windows Media 伺服器。
-   支援在 ASF 檔案中編輯中繼資料。 您可以使用此 SDK 輕鬆地操作檔案及其內容的相關資訊。 開發人員可以使用 SDK 中所包含之中繼資料屬性的健全系統，或建立自訂屬性以符合其需求。
-   支援內容編輯應用程式。 此 SDK 可讓應用程式依簡報時間和影片畫面來搜尋檔案中的點。 此外，使用 Windows Media 格式 SDK 所建立的檔案，可以使用電影和電視生產環境中所使用的格式來維護時間戳記。
-   支援在 MP3 檔中讀取和編輯中繼資料。 此 SDK 提供使用讀取 ASF 檔案的相同方法來讀取 MP3 檔案的整合式支援。 以 Windows Media Format SDK 建立的應用程式也可以使用內容建立者所使用最常見的 ID3 標記內建的支援，編輯 MP3 檔案中的中繼資料屬性。
-   支援數位 Rights Management 保護。 此 SDK 提供的方法可用來讀取和寫入由數位 Rights Management 保護的 ASF 檔案和網路串流，以防止未經授權播放或複製內容。

若要下載 Windows Media Format SDK，請參閱 Microsoft 網站上的 [Windows Media 下載](https://msdn.microsoft.com/windows/desktop/aa904949) 頁面。

本檔說明如何使用 Windows Media Format SDK 來開發數位媒體應用程式。 它分成下列各節。

> [!Note]  
> 雖然本檔包含最新版本的 Windows Media Format SDK 的相關資訊，但其所描述的大部分功能都是由舊版 SDK 支援。 Windows Media Format SDK 的方法、函式、結構和列舉參考頁面包含版本需求。

 



| 區段                                                                                                          | 描述                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [關於 Windows Media Format SDK](about-the-windows-media-format-sdk.md)                                     | 提供您在嘗試建立應用程式之前應該熟悉的總覽和背景資訊。                                                                                  |
| [程式設計指南](programming-guide.md)                                                                       | 提供執行各種工作的詳細指示，例如讀取、寫入和編制檔案索引、使用數位 Rights Management 保護檔案、透過網路串流 ASF 資料等等。 |
| [程式設計參考](programming-reference.md)                                                               | 提供與 Windows Media 格式相關之介面、方法、函式、結構、列舉類型和常數的參考資訊。                                                     |
| [Windows Media 音訊和影片編解碼器介面](windows-media-audio-and-video-codec-interfaces--deprecated.md) | 提供使用 Windows Media 音訊和影片編解碼器數位媒體物件 (直接) DMOs 的指示。                                                                                           |
| [*詞彙*](wmformat-glossary.md)                                                                              | 定義 Windows Media Format SDK 檔中使用的詞彙。                                                                                                                                    |



 

 

 





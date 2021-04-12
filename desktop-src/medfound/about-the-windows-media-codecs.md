---
description: 關於 Windows Media 編解碼器
ms.assetid: C0B0265C-AD20-433B-A554-112AEB0208B9
title: 關於 Windows Media 編解碼器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2240176de22682451814609abc94f33a52300563
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104195736"
---
# <a name="about-the-windows-media-codecs"></a>關於 Windows Media 編解碼器

-   [Windows Media 音訊編解碼器](#windows-media-audio-codecs)
    -   [Windows Media 音訊9](#windows-media-audio-9)
    -   [Windows Media 音訊10專業版](#windows-media-audio-10-professional)
    -   [Windows Media 音訊9無損](#windows-media-audio-9-lossless)
    -   [Windows Media 音訊9語音](#windows-media-audio-9-voice)
    -   [相容性](#compatibility)
-   [Windows Media 視訊9系列編解碼器](#windows-media-video-9-series-codecs)
    -   [Windows Media 視訊9](#windows-media-video-9-series-codecs)
    -   [Windows Media 視訊9螢幕](#windows-media-video-9-screen)
    -   [Windows Media 視訊9映射第2版](#windows-media-video-9-image-version-2)
    -   [Windows Media 視訊 9 BC-VCM-LVM-HYPERV](#windows-media-video-9-vcm)
    -   [相容性](#compatibility)
-   [相關主題](#related-topics)

## <a name="windows-media-audio-codecs"></a>Windows Media 音訊編解碼器

### <a name="windows-media-audio-9"></a>Windows Media 音訊9

此編解碼器會在44.1 或48千赫茲 (kHz) 使用16位，類似于目前的 CD 標準，以資料速率提供 CD 品質，從64到每秒 192 kb (Kbps) 。 產生的音效品質比以對等資料速率 Windows Media 音訊8取樣的音訊更快20%。

Windows Media 音訊9編解碼器 (WMA 9) 支援的位速率編碼 (VBR) ，這會根據音訊資料的複雜度，自動改變編碼位元速率，以較小的檔案大小啟用更高品質的音訊。 使用 VBR 時，編碼位元速率會增加，以捕獲複雜的資料區段，然後減少以最大化較不復雜區段的壓縮，進而產生精簡、高品質的壓縮。

WMA 9 與先前的 Windows Media 音訊相容的解碼器回溯相容，這表示您可以使用舊版的 Windows Media Player 或支援 Windows Media 的舊版消費性電子裝置來播放 WMA 9 內容。 如同所有 Windows Media 9 系列編解碼器，它支援 Windows Media 數位版權管理平臺，可用來安全地封裝和散佈禁止複製的數位媒體。

### <a name="windows-media-audio-10-professional"></a>Windows Media 音訊10專業版

Windows Media 音訊 10 Professional (WMA 10 Pro) 是最有彈性的 Windows Media 音訊編解碼器可用–支援的設定檔包括從全解析度24位/96 kHz 音訊（身歷聲、5.1 聲道或甚至 7.1 channel 環繞音效）到高效率的行動功能，24 Kbps 到 96 Kbps 的身歷聲，以及 128 Kbps 到 256 Kbps 的5.1 通道音效。 WMA 10 Pro 為使用高精確度硬體和5.1 通道環繞音效的電腦，以及在行動裝置上播放音訊內容的取用者提供絕佳的品質。 WMA 10 Pro 支援串流、漸進式下載，或從128到 768 Kbps 的下載並播放傳遞。

當您使用5.1 以 384 Kbps 壓縮的 WMA 10 Pro 壓縮的音效音訊時，大部分的接聽程式都無法辨別壓縮的音樂與原始脈衝程式碼調製 (PCM) 檔之間的任何差異。 WMA Pro 也提供動態的範圍控制，使用編碼程式期間所計算的最大和平均音訊 amplitudes。 使用 Windows Media Player 9 和更新版本中的「無訊息模式」功能，使用者可以聽到全動態範圍、最多12分貝的中等差異範圍 (dB) 高於平均，或在平均之上最多6個資料庫的差異範圍。

如果使用者嘗試播放使用5.1 通道編碼的檔案，24位、96 kHz 取樣功能，但沒有支援多聲道或高解析度音效的系統或音效卡，多個通道會合並成身歷聲音訊 (例如16位、雙聲道音訊) ，確保使用者獲得系統可提供的最佳播放體驗。

下表比較 WMA Pro 與競爭壓縮技術。



| 音訊資料              | 產業壓縮\*        | Windows Media\*            | 節省壓縮 |
|-------------------------|-------------------------------|----------------------------|---------------------|
| 2 ch x 48 kHz x 16 位 | 220 Kbps 的杜比數位2。0 | 128 Kbps 的 WMA 10 專業版     | 1.7：1               |
| 6 ch x 48 kHz x 20 位 | 384 Kbps 的杜比數位5。1 | WMA 10 Pro （192）-256 Kbps | 1.5-2：1             |
| 6 ch x 48 kHz x 24 位 | 1536 Kbps 的 DTS 5。1         | 768 Kbps 的 WMA 10 專業版     | 2:1                 |



 

\* 相依內容

### <a name="windows-media-audio-9-lossless"></a>Windows Media 音訊9無損

使用此編解碼器壓縮的音訊品質是所有 Windows Media 音訊編解碼器的最佳選擇。 它會建立原始音訊檔案的 bit （bit）複製，因此不會遺失任何資料，因此很適合用來封存內容主機。

根據原始的複雜度而定，內容將會以2:1 或3:1 的比率壓縮。 雖然這比其他 Windows Media 音訊9系列編解碼器達成的比率低，但它提供了相同的壓縮優點，同時讓資料保持不變。

如同 Windows Media 音訊 9 Professional，Windows Media 音訊9無失真編解碼器也使用編碼程式期間所計算的最大和平均音訊 amplitudes，提供動態的範圍控制。 使用 Windows Media Player 9 和更新版本中的「無訊息模式」功能時，使用者可以聽到全動態範圍、最多12個 dB 以上的平均範圍，或在平均值高於6個資料庫的差異範圍內。

### <a name="windows-media-audio-9-voice"></a>Windows Media 音訊9語音

這個低位速率編解碼器主要是針對語音內容，但可透過混合模式內容（包括語音和音樂）來執行。 在語音模式中，編解碼器會利用人類心聲的相對較不復雜且較窄的頻率範圍，來將壓縮最大化。 在 [音樂] 模式中，編解碼器的運作方式就像標準 Windows Media 音訊9編解碼器。 編碼的內容可以設定為自動在語音和音樂模式之間切換。

Windows Media 音訊9語音編解碼器提供低位速率串流案例的高品質， (少於 20 Kbps) ，例如廣播廣播、廣告、電子書、播客和 voiceovers。 語音編解碼器也可將內容壓縮為最低 4 Kbps 的 8 kHz。

### <a name="compatibility"></a>相容性

下表概述當您的使用者在 Windows XP 或舊版 Windows Media Player 的舊版 Microsoft Windows 作業系統上播放 Windows Media 音訊9系列內容時，會發生什麼事。 此表格也會列出 Apple Mac OS X 和 Windows CE 架構平臺的相容性。



| 轉碼器                              | 功能                                       | 播放機回溯相容性                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------|-----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Media 音訊9              | 常數位速率 (CBR) 編碼              | <dl> <dt>Windows Media Player 6.4 或更新版本的非可攜式裝置上 (使用轉碼（如有需要）) </dt> <dt>Windows Media Player 9 （</dt>適用<dt>于 Mac OS X Windows Media Player 9 系列 \* ，以及 Windows Media Player 9.1 適用于 Pocket PC</dt> <dt>Windows Media Player 9 系列和 Windows Media Player 9.1 for \* Smartphone</dt> </dl> |
|                                    | 變數位速率 (VBR) 編碼              | 在支援播放程式的所有裝置上 Windows Media Player 7 或更新版本， (視需要使用轉碼)                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Windows Media 音訊9專業版 | 一般                                       | <dl> Mac OS X <dt>Windows Media Player 7 或更新版本</dt> <dt>Windows Media Player 9</dt> </dl>                                                                                                                                                                                                                                                                                                                          |
|                                    | 離散通道播放 (例如 5.1)  | 需要 Windows Media Player 9 系列 (或 SDK) 或更新版本、Windows XP 及多頻道音訊卡。                                                                                                                                                                                                                                                                                                                                                                                                                         |
|                                    | 高解析度音訊 (24 位、96 kHz)         | 需要 Windows Media Player 9 系列 (或 SDK) 或更新版本、Windows XP 和高解析度的音訊卡。                                                                                                                                                                                                                                                                                                                                                                                                                      |
|                                    | 動態範圍控制項                         | 需要 Windows Media Player 9 系列 (或 SDK) 或更新版本和 Windows XP。                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Windows Media 音訊9無損     | 一般                                       | <dl> Mac OS X <dt>Windows Media Player 7 或更新版本</dt> <dt>Windows Media Player 9</dt> </dl>                                                                                                                                                                                                                                                                                                                          |
|                                    | 離散通道播放 (例如 5.1)  | 需要 Windows Media Player 9 系列 (或 SDK) 或更新版本、Windows XP 及多頻道音訊卡。                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Windows Media 音訊9語音        | 一般                                       | <dl> <dt>Windows Media Player 6.4 或更新版本</dt>的<dt>Windows Media Player 9 適用于 Mac OS X</dt> <dt>Windows Media Player 9 系列，以及適用 \* 于 Pocket PC 的 Windows Media Player 9.1</dt> Windows Media Player <dt>9 \* 系列，以及適用于 Smartphone 的 Windows Media Player 9.1</dt> </dl>                                                       |



 

> [!Note]  
> \* Pocket PC 和 Smartphone 的所有 Windows Media Player 版本都隨附于 Microsoft Windows Mobile 作業系統中。 適用于 Pocket PC 的 Windows Media Player 以及 Smartphone 的 Windows Media Player 不能從 Microsoft 下載。

 

## <a name="windows-media-video-9-series-codecs"></a>Windows Media 視訊9系列編解碼器

在2006中，運動圖片和電視工程師 (的) 正式發行了 SMPTE 421M 的最終規格，也稱為 VC-1。 VC-1 的正式標準化代表超過75的公司高潮多年來的技術審查，使編解碼器具有妥善記錄、極穩定、容易授權，並可由產業接受。 VC-1 支援三個設定檔：簡單、主要和先進。 簡單和主要的設定檔已完成數年，而現有的程式（例如 WMV 9）已長期支援使用這些設定檔來建立和播放內容，以及預先執行的 Advanced profile。 完成先進的設定檔，並將 VC-1 中所有設定檔的後續標準化，代表完整規格中的最後一個步驟，可在任何媒體或任何可用的裝置上提供高定義內容（交錯或漸進式）。

### <a name="windows-media-video-9"></a>Windows Media 視訊9

Windows Media 視訊9是 VC-1 SMPTE 標準的 Microsoft 實作為。 它支援簡單、主要和先進的設定檔。

### <a name="simple-and-main-profiles"></a>簡單和主要設定檔

Windows Media 視訊9簡單和主要設定檔完全符合 SMPTE VC-1 標準，並提供高品質的串流和下載影片。 這些設定檔支援廣泛的位元速率，從一半到一到一秒的高定義內容，到一秒的雙速率，以及透過撥號數據機提供的低位網際網路影片。 此編解碼器也支援具有雙通路和變數位元速率的專業品質可下載影片 (VBR) 編碼。 許多不同的播放程式和裝置都已支援 Windows Media 視訊9。

### <a name="advanced-profile"></a>Advanced Profile

Windows Media 視訊 9 Advanced profile 完全符合 SMPTE VC-1 標準、支援交錯式內容，而且與傳輸無關。 內容建立者可以使用此設定檔，以最低一三分之一的 MPEG-2 編解碼器（與 MPEG-2 相同的品質）來提供漸進式或交錯式內容。

在過去，交錯式影片內容在使用 Windows Media 視訊編解碼器進行編碼之前，一律會先取消交錯。 現在，編碼的應用程式（例如 Windows Media 9 系列）和協力廠商編碼解決方案可以支援壓縮交錯內容，而不需要先將它轉換成漸進式內容。 如果內容是在交錯顯示（例如電視）上轉譯，則維護編碼檔案中的交錯是很重要的。

傳輸獨立性也可讓您在不是以 Windows Media 為基礎的系統上傳遞 Windows Media 視訊 9 Advanced Profile，例如以標準為基礎的廣播基礎結構 (透過原生 MPEG-2 傳輸串流) 、無線基礎結構 (使用即時傳輸通訊協定 \[ RTP \]) 或甚至是 dvd。

下表比較 Windows Media 視訊 9 Advanced Profile 與競爭壓縮技術。



| 影片資料                                                  | 產業壓縮\* | Windows Media\*                                      | 節省壓縮 |
|-------------------------------------------------------------|------------------------|------------------------------------------------------|---------------------|
| 480/24p 720x480 圖元/框架 x 每個頻道8個位 x 24 fps  | MPEG-2，4– 6 Mbps     | Windows Media 視訊 9 Advanced Profile （1.3-2 Mbps） | 3:1                 |
| 480/30i 720x480 圖元/框架 x 每個頻道8個位元組 x 30 fps  | MPEG-2 為6– 8 Mbps     | Windows Media 視訊9的 Advanced Profile 2 – 4 Mbps   | 2-3：1               |
| 720/24p 1280x720 圖元/frame x 每個頻道8個位 x 24 fps | MPEG-2 （19 Mbps）      | 5– 8 Mbps 的 Windows Media 視訊 9 Advanced Profile   | 2.4 –3.8：1           |



 

\*相依內容

### <a name="windows-media-video-9-screen"></a>Windows Media 視訊9螢幕

Windows Media 視訊9螢幕編解碼器已針對壓縮從電腦顯示所捕獲的連續螢幕擷取畫面和高度靜態影片進行優化，使其非常適合提供示範或示範用來訓練的電腦。 編解碼器會利用一般的影像簡化和相對缺乏的動作來達到非常高的壓縮比率。

在編碼過程中，編解碼器會根據影片資料的複雜度，自動切換失真和無失真編碼模式。 針對複雜的資料，不失真模式會保留資料的完整複本。 針對較不復雜的資料，遺失模式會捨棄一些資料，以達到較高的壓縮比率。 藉由在這兩種模式之間自動切換，編解碼器會在最大化壓縮時維持影片品質。

整體來說，Windows Media 視訊9螢幕編解碼器可提供更佳的點陣圖影像和螢幕動作處理，即使是相對較低的 Cpu 也是一樣。 這也比常用的執行長度編碼更高出100倍。

### <a name="windows-media-video-9-image-version-2"></a>Windows Media 視訊9映射第2版

Windows Media 視訊9映射第2版編解碼器與其他視頻編解碼器不同。 它不會處理未壓縮的影片，而是使用剪輯之間的平移、縮放和交叉淡化轉換，將影像轉換成影片，以建立不限數目的效果。

然後，您可以將資料速率以最低每秒20千 (Kbps) 的資料速率傳遞結果。 這些檔案會使用固定的位元速率來壓縮 (CBR) 或以一次傳遞變數位元速率 (VBR) 模式。

> [!Note]  
> Windows Media 視訊9映射版本2的編解碼器與 Windows Media 視訊9映射編解碼器不相容。

 

### <a name="windows-media-video-9-vcm"></a>Windows Media 視訊 9 BC-VCM-LVM-HYPERV

影片壓縮管理員 (BC-VCM-LVM-HYPERV) 版本的 Windows Media 視訊9系列編解碼器，可讓舊版編碼和編輯應用程式支援檔案容器中的 Windows Media 視訊9系列編解碼器，例如音訊影片交錯 (AVI) 。 此編解碼器套件也可讓您根據 Windows Media Format 9 系列，在 ASF 和 AVI 檔案容器的 Windows Media Player 6.4 中播放 Windows Media 視訊 (WMV) 檔。

### <a name="compatibility"></a>相容性

下表概述當您在舊版 Microsoft Windows 作業系統或舊版 Windows Media Player 上播放 Windows Media 視訊9系列內容時，觀眾將會遇到的情況。 此表格也會列出 Apple Mac OS X 和 Windows CE 架構平臺的相容性。



| 轉碼器                                  | 功能             | 播放機回溯相容性                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Media 視訊9                  | 一般             | <dl> <dt>Windows Media Player 6.4 或更新版本</dt>的<dt>Windows Media Player 9 適用于 Mac OS X</dt> <dt>Windows Media Player 9 系列，以及適用 \* 于 Pocket PC 的 Windows Media Player 9.1</dt> Windows Media Player <dt>9 \* 系列，以及適用于 Smartphone 的 Windows Media Player 9.1</dt> </dl> |
|                                        | 框架插補 | 需要 Windows Media Player 9 系列 (或軟體發展工具組) 或更新版本和 Windows XP。                                                                                                                                                                                                                                                                                                                                                                           |
| Windows Media 視訊 9 Advanced Profile | 一般             | Windows Media Player 7 或更新版本                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Windows Media 視訊9螢幕           | 一般             | Windows Media Player 7 或更新版本                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Windows Media 視訊9映射第2版  | 一般             | Windows Media Player 7 或更新版本                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

> [!Note]  
> \*Pocket PC 和 Smartphone 的所有 Windows Media Player 版本都隨附于 Microsoft Windows Mobile 作業系統中。 適用于 Pocket PC 的 Windows Media Player 以及 Smartphone 的 Windows Media Player 不能從 Microsoft 下載。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows Media 轉碼器](windows-media-codecs.md)
</dt> </dl>

 

 




---
title: Windows Media 9.5 SDK 中新增的功能
description: Windows Media 9.5 SDK 中新增的功能
ms.assetid: 1525132c-8aa1-42bb-9552-41531fb83055
keywords:
- Windows Media Format SDK，功能
- Windows Media Format SDK，新功能
- Windows Media Format SDK，適用于應用程式特定處理的介面
- 'Windows Media Format SDK、DirectX Video 加速 (DXVA) '
- Windows Media Format SDK，IWMPlayerHook 介面
- IWMPlayerHook
- Windows Media Format SDK、x64 版本的 Windows
- Windows Media 格式 SDK，Windows Media 視訊映射編解碼器
- Windows Media Format SDK、音訊編解碼器
- 適用于網路裝置的 Windows Media Format SDK、DRM 10
- Windows Media Format SDK，DRM 授權
- Windows Media Format SDK，Advanced Profile 編解碼器
- 'Windows Media Format SDK、索尼/Philips 數位互連格式 (S/PDIF) '
- Windows Media Format SDK，低延遲格式
- Windows Media Format SDK，近似搜尋模式
- Windows Media Format SDK，播放清單燒錄
- Windows Media Format SDK，多重語言支援
- Windows Media Format SDK、Windows Media 裝置管理員 SDK
- Windows Media Format SDK，編解碼器介面
- 編解碼器，Windows Media 視訊映射
- 數位版權管理 (DRM) ，網路裝置安全傳輸通訊協定
- DRM (數位版權管理) ，網路裝置安全傳輸通訊協定
- 數位版權管理 (DRM) 、授權
- DRM (數位版權管理) 、授權
- 編解碼器，Advanced Profile 編解碼器
- 索尼/Philips 數位互連格式 (S/PDIF) 、使用傳送或傳輸
- S/PDIF (索尼/Philips 數位互連格式) 、使用傳送或傳輸
- 近似搜尋模式
- 中繼資料、多重語言支援
- Windows Media 裝置管理員 SDK
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e58c9816ef80325422ee365b952842727b5004e
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/20/2020
ms.locfileid: "104092562"
---
# <a name="features-added-in-the-windows-media-95-sdk"></a>Windows Media 9.5 SDK 中新增的功能

Windows Media Format 9.5 SDK 引進了新功能，可提供增強的內容安全性和彈性。 從9系列版本開始，已對 SDK 進行下列變更。

## <a name="new-interface-for-application-specific-processing-during-directx-video-acceleration"></a>DirectX 影片加速期間應用程式特定處理的新介面

支援 DirectX Video 加速的播放程式應用程式現在可以執行 [**IWMPlayerHook**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmplayerhook) 介面，以在 DirectX VA 解碼期間執行應用程式特定的處理。 讀取器會先呼叫 [**IWMPLayerHook：:P redecode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmplayerhook-predecode) 回呼方法，再將壓縮的影片範例傳遞至視頻處理器進行解碼。

> [!Note]  
> 若要使用 **IWMPlayerHook** 介面和相關聯的 [**IWMReaderAdvanced5**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced5) 介面，您必須在 Windows Media Format SDK 中安裝更新編號888656。 您可以從 [Microsoft 網站](https://support.microsoft.com/?id=888656)下載更新。

 

## <a name="windows-media-format-sdk-version-for-x64-based-versions-of-windows"></a>X64 版本 Windows 的 windows Media Format SDK 版本

有 x64 型版本的 Windows Media Format SDK 可用。 這份檔適用于32位版本和 x64 版本的 SDK。 不過，x64 架構的 Windows Media 格式 SDK 不支援數位版權管理 (DRM) 。

## <a name="new-version-of-the-windows-media-video-image-codec"></a>新版本的 Windows Media 視訊映射編解碼器

Windows Media 視訊9映射 v2 編解碼器可簡化移動和縮放的範例幾何計算。 新的編解碼器也支援在影像之間進行數個複雜的轉換。

## <a name="new-version-of-the-windows-media-audio-codecs"></a>新版本的 Windows Media 音訊編解碼器

Windows Media Format 9.5 SDK 包含下列更新的音訊編解碼器：

-   Windows Media 音訊9。1
-   Windows Media 音訊9.1 專業版
-   Windows Media 音訊9.1 無損

## <a name="windows-media-drm-10-for-network-devices-protocol-support"></a>適用于網路裝置的 Windows Media DRM 10 通訊協定支援

Windows Media Format 9.5 SDK 支援網路裝置安全傳輸通訊協定的新 Windows Media DRM 10。 此通訊協定可用來透過區域網路將加密的內容串流至播放裝置，例如機頂尖的影片接收者。

大部分用來為網路裝置執行 Windows Media DRM 10 支援的程式必須由應用程式執行。 不過，您可以使用 Windows Media Format SDK 的方法來提供下列功能：

-   維護裝置的資料庫，包括針對網路裝置啟用 Windows Media DRM 10 的裝置。
-   驗證裝置，確保它們「接近」足夠的網路上的用戶端以進行安全串流。
-   將受 DRM 保護的檔案轉換為網路裝置串流的 Windows Media DRM 10。
-   使用先前加密的資料來寫入檔案。

## <a name="support-for-new-drm-licenses"></a>支援新的 DRM 授權

使用 Windows Media Rights Manager SDK 建立的新授權會使用輸出保護層級 (OPLs) 來指定播放和複製內容的許可權和限制。 Windows Media Format SDK 提供從授權讀取 OPLs 的支援。

## <a name="new-video-codec"></a>新的影片編解碼器

Windows Media 視訊 9 Advanced Profile 編解碼器建基於 Windows Media 視訊9編解碼器的高品質，同時新增對交錯編碼的支援。

## <a name="spdif-output"></a>S/PDIF 輸出

使用 Windows Media 音訊 Professional 編解碼器編碼的內容，現在可以使用索尼/Philips 數位互連格式 (S/PDIF) 來傳送或傳輸。

## <a name="low-delay-audio"></a>Low-Delay 音訊

Windows Media 音訊9.1 和 Windows Media 音訊 9.1 Professional 編解碼器現在都支援數個低延遲格式。 這些格式會產生可更快速啟動的音訊串流，以減少串流切換案例中的延遲。 使用低延遲格式也可以改善即時廣播的整體延遲。

## <a name="approximate-seeking-mode"></a>近似搜尋模式

您現在可以使用讀取器在 ASF 檔案中搜尋大約的時間。 這種模式可改善執行不精確搜尋時的效能，例如當使用者按一下 Windows Media Player 中的搜尋列時。 近似搜尋會傳回先前 cleanpoint 的媒體範例，而不是針對搜尋的精確時間來重建範例。

## <a name="playlist-burning"></a>播放清單燒錄

Windows Media DRM 10 支援將音訊檔案複製到 Red Book CD 作為播放清單一部分的許可權。 Windows Media Format SDK 提供方法來確認是否允許複製播放清單中的檔案。

## <a name="improved-multiple-language-support-for-metadata"></a>改進了中繼資料的 Multiple-Language 支援

在 Windows Media Format 9 系列 SDK 中，所有新增至檔案的中繼資料都已指派給以預設語言的語言識別項指定的語言清單。 這會導致當不同地區設定中的內容散發者新增一些中繼資料時發生問題，因為散發者的地區設定中的使用者只會看到為其語言新增的幾個屬性。 Windows Media Format 9.5 SDK 會解決此問題，方法是在檔案中有兩種語言的屬性之前，不會建立語言清單。 屆時，所有的中繼資料都會與第二個語言的地區設定相關聯，而這會成為預設值。 如此一來，內容散發者可以保留檔案的所有原始中繼資料（例如標題和作者），而不會在新增與其地區設定相關的某些屬性時保持不變。

## <a name="windows-media-device-manager-sdk-included-in-installation"></a>安裝中包含 Windows Media 裝置管理員 SDK

Windows Media Format 9.5 SDK 的安裝套件會安裝 Windows Media 裝置管理員 SDK。 您可以在 C： WMSDK WMFSDK95 WMDM 檔資料夾中找到 Windows Media 裝置管理員 SDK 的檔 \\ \\ \\ \\ (如果沒有在預設資料夾中安裝 windows media Format SDK，您的資料夾將會有所不同。 ) 

## <a name="codec-interface-documentation"></a>編解碼器介面檔

本檔包含在 Windows Media 格式 SDK 之外使用 Windows Media 音訊和影片編解碼器的相關資訊。 這份檔最初是在從 Microsoft 開發人員網路下載時發行的一部分。 示範直接使用編解碼器 DMOs 的範例應用程式包含在 Windows Media 格式 SDK 安裝中，以及標頭。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**關於 Windows Media Format SDK**](about-the-windows-media-format-sdk.md)
</dt> </dl>

 

 





---
title: Windows Media Player 11的新功能
description: 本主題列出 Windows Media Player 11 和 Windows Media Player 11 SDK 的新功能。
ms.assetid: d2a6b6ce-a924-4b55-9dc7-68cc57e5651f
keywords:
- Windows Media Player，新功能
- Windows Media Player，新功能
- 軟體發展工具組 (SDK) 、Windows Media Player 11
- SDK (軟體發展工具組) 、Windows Media Player 11
- 檔，Windows Media Player 11 SDK
- 新功能，Windows Media Player 11
- 新功能，Windows Media Player 11
- 介面，Windows Media Player 11 中的新功能
- Windows Media Player 11 中的屬性、新功能
- Windows Media Player 的 ActiveX 控制項，第11版中的新功能
- ActiveX 控制項，第11版中的新功能
- Windows Media Player 11 中的外觀、新功能
- Windows Media Player 的外觀，第11版中的新功能
- 外掛程式，Windows Media Player 11 中的新功能
- Windows Media Player 外掛程式，第11版中的新功能
- 線上商店，Windows Media Player 11 的新功能
- Windows Media Player 線上商店，第11版的新功能
- 範例，Windows Media Player 11 中的新功能
- 版本的 Windows Media Player，第11版中的新功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12aa728aa1552ac0e65f5825cad62d8e9e0c7300
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "104023169"
---
# <a name="what-was-new-in-windows-media-player-11"></a>Windows Media Player 11的新功能

本主題列出 Windows Media Player 11 和 Windows Media Player 11 SDK 的新功能。

## <a name="windows-media-player-control"></a>Windows Media Player 控制項

下列介面是 Windows Media Player 11 ActiveX 控制項中的新介面。

-   [**IWMPLibrary 介面**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary)
-   [**IWMPLibraryServices 介面**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibraryservices)
-   [**IWMPLibrarySharingServices 介面**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrarysharingservices)
-   [**IWMPMediaCollection2 介面**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection2)
-   [**IWMPQuery 介面**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpquery)
-   [**IWMPStringCollection2 介面**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpstringcollection2)
-   [**MediaCollection 物件**](mediacollection-object.md)
-   [**Query 物件**](query-object.md)
-   [**StringCollection 物件**](stringcollection-object.md)
-   [**IWMPCdromRip 介面**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip)
-   [**IWMPCdromBurn 介面**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn)
-   [**IWMPFolderMonitorServices 介面**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices)
-   [**IWMPSyncDevice2 介面**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice2)
-   [**IWMPVideoRenderConfig 介面**](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmpvideorenderconfig)
-   [**IWMPUserEventSink**](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpusereventsink)
-   [**IWMPEvents3 介面**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents3)

## <a name="windows-media-player-skins"></a>Windows Media Player 的外觀

以下是 Windows Media Player 11 的新功能。

-   用來定位控制項的新屬性。 請參閱 [**AmbientAttributes right**](ambientattributes-right.md)和 [**AmbientAttributes。**](ambientattributes-bottom.md)
-   移動和調整大小控制項的新屬性。 請參閱 [**AmbientAttributes. moveSizeTo**](ambientattributes-movesizeto.md) 和 [**AmbientAttributes. slideTo**](ambientattributes-slideto.md)。
-   用來指定影像調整大小行為的新屬性。 請參閱 [**AmbientAttributes. resizeImages**](ambientattributes-resizeimages.md)。
-   新的屬性，用於指定面板元素的非統一縮放比例。 請參閱 [**AmbientAttributes. nineGridMargins**](ambientattributes-ninegridmargins.md)。

## <a name="windows-media-player-plug-ins"></a>Windows Media Player 外掛程式

Windows Media Player 11 SDK 引進了一種新類型的外掛程式，可轉換數位媒體檔案格式。 請參閱 [Windows Media Player 轉換外掛程式](windows-media-player-conversion-plug-ins.md)。

在 Windows Media Player 11 SDK 發行之前建立的 DSP 外掛程式必須更新，才能使用 Windows Media Player 11。 請參閱 [更新現有的 DSP 外掛程式](updating-existing-dsp-plug-ins.md)。

Windows Media Player 外掛程式嚮導已更新，可建立可在 Windows Media Player 11 中運作的 DSP 外掛程式。 如需詳細資訊，請參閱 [Windows Media Player 11 的 DSP 外掛程式的更新](updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11.md)。

## <a name="windows-media-player-online-stores"></a>Windows Media Player 線上商店

Windows Media Player 11 引進了新的模型，可將線上商店目錄整合到 Windows Media Player 程式庫功能中。 請參閱 [類型1線上商店](type-1-online-stores.md)。

## <a name="windows-media-player"></a>Windows Media Player

以下是 Windows Media Player 11 的新功能。

-   [用於報告取得內容的裝置擴充功能](device-extensions-for-reporting-acquired-content.md)
-   [播放清單物件喜好設定的裝置擴充功能](device-extensions-for-playlist-object-preferences.md)

## <a name="windows-media-player-sdk-samples"></a>Windows Media Player SDK 範例

名為 SchemaReader 的 c # 範例是 Windows Media Player 11 SDK 的新功能。 此範例所建立的工具，會使用 Windows Media Player 物件模型，來取得和顯示 Windows Media Player 程式庫或數位媒體檔案中中繼資料的相關資訊。 此工具可以將結果儲存至文字檔。 此工具會針對每個支援的架構，列舉程式庫中儲存的中繼資料屬性名稱 (音訊、影片、播放清單、相片和其他) 。 此工具也可以針對播放清單集合中的播放清單、CD 曲目、CD 目錄、DVD 標題、DVD 章節、DVD 目錄和個別媒體檔案提供可用屬性的相關資訊。

Windows Media Player 11 SDK 中已更新名為 WMPML 的 c + + 範例，以示範下列功能：

-   使用新的 [**IWMPStringCollection2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpstringcollection2) 介面建立類似 Windows Media Player 程式庫功能的使用者介面。
-   使用 [**IWMPQuery**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpquery) 和 [**IWMPMediaCollection2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection2) 介面來建立複合查詢並顯示結果。

 

 





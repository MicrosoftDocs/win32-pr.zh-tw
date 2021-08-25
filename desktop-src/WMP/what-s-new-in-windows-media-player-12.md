---
title: Windows Media Player 12的新功能
description: 本主題列出 Windows Media Player 12 中的新功能。
ms.assetid: 17f76963-c96d-46c9-82c0-3ed2d8a4e892
keywords:
- Windows Media Player，新功能
- Windows Media Player，新功能
- 軟體發展工具組 (SDK) ，Windows Media Player 12
- SDK (軟體發展工具組) ，Windows Media Player 12
- 檔，Windows Media Player 12 SDK
- 新功能，Windows Media Player 12
- 新功能，Windows Media Player 12
- 介面，Windows Media Player 12 中的新功能
- Windows Media Player 12 中的屬性、新功能
- 中繼資料，Windows Media Player 12 中的新功能
- 列舉，Windows Media Player 12 中的新功能
- Windows Media Player 12 中的旗標、新功能
- 介面，Windows Media Player 12 中已淘汰
- 方法，在 Windows Media Player 11 中已被取代，不是12
- 版本的 Windows Media Player，第12版中的新功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 976c9b0995188f9d6c6db6e7394ec0019047ff18b51940ada202c8c7ea713f39
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119862278"
---
# <a name="whats-new-in-windows-media-player-12"></a>Windows Media Player 12的新功能

本主題列出 Windows Media Player 12 中的新功能。

## <a name="new-interfaces"></a>新介面

-   [**IWMPAudioRenderConfig**](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmpaudiorenderconfig)
-   [**IWMPEvents4**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents4)
-   [**IWMPLibrary2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary2)
-   [**IWMPSyncDevice3**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice3)

## <a name="new-attributes"></a>新屬性

下列媒體專案的新屬性可透過 [**IWMPMedia**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia) 和 [**IWMPMedia3**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia3) 介面取得。

-   [**AlbumCoverURL**](wm-albumcoverurl-attribute.md)
-   [**AlternateSourceURL**](alternatesourceurl-attribute.md)
-   [**DLNASourceURI**](dlnasourceuri-attribute.md)
-   [**DLNAServerUDN**](dlnaserverudn-attribute.md)
-   [**DTCPIPHost**](dtcpiphost-attribute.md)
-   [**DTCPIPPort**](dtcpipport-attribute.md)
-   [**LibraryID**](libraryid-attribute.md)
-   [**LibraryName**](libraryname-attribute.md)

## <a name="new-device-metadata"></a>新的裝置中繼資料

您可以藉由呼叫 [**IWMPSyncDevice：： getItemInfo**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-getiteminfo)來取出下列新的裝置中繼資料專案。

-   **BackgroundSyncState**
-   **SkippedFiles**
-   **SyncFilter**

您可以藉由呼叫 [**IWMPSyncDevice2：： setItemInfo**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice2-setiteminfo)來設定下列新的裝置中繼資料專案。

-   **AutoSyncDefaultRules**
-   **BackgroundSyncState**
-   **IncludeSkippedFiles**
-   **SyncFilter**
-   **SyncOnConnect**

## <a name="new-enumeration-member"></a>新的列舉成員

[**WMPSyncState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpsyncstate)列舉具有下列的新成員。

-   **wmpssEstimating**

## <a name="new-flag"></a>新增旗標

[**IWMPGraphCreation：： GetGraphCreationFlags**](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpgraphcreation-getgraphcreationflags)方法支援下列新旗標。

-   **WMPGC \_ 旗標 \_ 使用 \_ 自訂 \_ 圖形**

## <a name="deprecated-interface"></a>已淘汰的介面

下列介面已被取代。

-   [**IWMPFolderMonitorServices**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices)

## <a name="methods-that-are-no-longer-deprecated"></a>不再被取代的方法

下列方法已在 Windows Media Player 11 SDK 中淘汰，但不再被取代。

-   [**IWMPGraphCreation::GraphCreationPreRender**](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpgraphcreation-graphcreationprerender)
-   [**IWMPGraphCreation::GraphCreationPostRender**](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpgraphcreation-graphcreationpostrender)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於 Windows Media Player SDK](about-the-windows-media-player-sdk.md)
</dt> </dl>

 

 





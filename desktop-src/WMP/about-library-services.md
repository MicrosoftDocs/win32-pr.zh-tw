---
title: 關於程式庫服務
description: 關於程式庫服務
ms.assetid: 2334aa4a-7988-481d-9b21-9f7b432fbd05
keywords:
- Windows Media Player，程式庫
- Windows Media Player 物件模型，程式庫
- 物件模型，程式庫
- Windows Media Player ActiveX 控制項，物件模型的程式庫
- ActiveX 控制項，物件模型的程式庫
- Windows Media Player 的行動 ActiveX 控制項、物件模型的程式庫
- Windows Media Player 行動裝置、物件模型的程式庫
- Windows Media Player 程式庫，關於
- Windows Media Player 程式庫，服務
- 程式庫，服務
- 程式庫，關於
- Windows Media Player、程式庫服務的版本
- 列舉，程式庫服務
- 事件，程式庫服務
- 範例，程式庫服務
- 介面，程式庫服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 743efc8ae5cb464aa38655314c52112bc9541de6
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/21/2020
ms.locfileid: "106967249"
---
# <a name="about-library-services"></a>關於程式庫服務

在舊版 Windows Media Player 中，軟體會為每個使用者使用單一程式庫資料庫。 此資料庫儲存在使用者的電腦上，並且在概念上與使用者和特定的播放程式實例相關聯。

Windows Media Player 11 引進了多個和遠端程式庫的概念。 現在除了預設值或 *本機* 程式庫之外，Windows Media Player 可以顯示從其他電腦連接到網路的程式庫抓取的內容，其中可能包括其他登入同一部電腦的使用者。 播放機也可以顯示來自其他來源的程式庫視圖，例如已啟用 MTP 的裝置或資料 Cd。 從使用者的觀點來看，這表示位於許多不同地點的數位媒體內容可以使用相同、熟悉的 Windows Media Player 使用者介面，從多個位置進行管理。 從開發人員的觀點來看，這表示您可以使用 Windows Media Player SDK COM 介面來列舉可用的程式庫，然後使用它們，就像您已在舊版中使用本機程式庫一樣。

若要列舉可用的程式庫，請使用 **IWMPLibraryServices** 介面。 此介面會公開 [IWMPLibraryServices：： getCountByType](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibraryservices-getcountbytype) 方法，以抓取指定類型的程式庫計數。 程式庫類型是由 [WMPLibraryType](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmplibrarytype) 列舉所定義。 此列舉包含本機程式庫的值 wmpltLocal。 這是因為程式庫服務功能一律可讓您使用 **IWMPLibraryServices** 和相關的介面來處理本機程式庫。

> [!Note]  
> **WMPLibraryType** 列舉包含值 wmpltRemote，代表網路共用的媒體程式庫。 若要存取這些共用程式庫，Player 控制項必須在遠端模式中執行。 如需在遠端模式中執行播放程式控制項的相關資訊，請參閱 [遠端處理 Windows Media Player 控制項](remoting-the-windows-media-player-control.md)。

 

在您抓取程式庫計數之後，您可以在迴圈中重複呼叫 [IWMPLibraryServices：： getLibraryByType](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibraryservices-getlibrarybytype) 來逐一查看可用的程式庫集合，並傳遞新的索引值給每個反復專案。 這個方法會抓取 [IWMPLibrary](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary) 介面的指標，代表個別的程式庫。

在您抓取 **IWMPLibrary** 的指標之後，您可以呼叫 [IWMPLibrary：： get \_ mediaCollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_mediacollection) 來取得 **IWMPMediaCollection** 介面的指標。 您可以使用這個介面指標來使用個別的程式庫，就像使用本機程式庫一樣。 您也可以藉由呼叫 [IWMPLibrary：： get \_ name](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_name)來取出包含程式庫名稱的字串，如果您需要對使用者顯示程式庫名稱，這會很有用。 您可以呼叫 [IWMPLibrary：： get \_ 類型](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type) 來取得特定程式庫的 **WMPLibraryType** 。

您可以處理 [IWMPEvents3：： LibraryConnect](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-libraryconnect) 事件，以瞭解程式庫何時可供使用，以及 [IWMPEvents3：： LibraryDisconnect](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-librarydisconnect) 事件以瞭解程式庫何時中斷連線。 每個事件都提供 **IWMPLibrary** 指標，表示連接或中斷連接的程式庫。 您可以呼叫 [IWMPLibrary：： isIdentical](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-isidentical) 來判斷連接或中斷連線的程式庫是否為您目前使用的程式庫。

相較于使用 [IWMPCore：： get \_ mediaCollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_mediacollection)所抓取的程式庫，使用透過 **IWMPLibraryServices** 介面抓取的程式庫時，有一些重要的差異。 適用下列差異：

-   從透過 **IWMPLibraryServices** 抓取的程式庫，您通常可以更快地取出查詢結果。  (這會假設其他因素，例如網路和硬碟存取時間相等。 ) 
-   從透過 **IWMPLibraryServices** 抓取的程式庫中可用的媒體專案中繼資料屬性清單，通常是透過 [IWMPCore](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcore)抓取之本機程式庫中可用的媒體專案中繼資料屬性的子集。
-   如果您透過 **IWMPLibraryServices** 抓取本機程式庫，則可以使用所有相同的屬性，因為當您透過 **IWMPCore** 抓取本機程式庫時可使用這些屬性。 不過，您可以更快速地為最常使用的屬性取得查詢結果。
-   當您使用透過 **IWMPLibraryServices** 抓取的程式庫時，您應該使用字串集合來建立使用者介面元素。 例如， [IWMPMediaCollection2：： getStringCollectionByQuery](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmediacollection2-getstringcollectionbyquery) 可讓您使用由 **IWMPQuery** 介面表示的自訂查詢 (，) 抓取字串集合。
-   透過 **IWMPLibraryServices** 介面抓取的遠端程式庫，可能不一定會連接到目前的播放機實例。 這表示，處理 **LibraryConnect** 和 **LibraryDisconnect** 事件，以瞭解程式庫可用性何時變更，以及處理 [IWMPEvents3：： StringCollectionChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-stringcollectionchange) 事件，以瞭解在您用來顯示使用者介面元素的字串集合中加入或移除字串時。 基於類似的原因，您也應該處理本機程式庫的 **StringCollectionChange** 事件。

請務必瞭解，特定程式庫的字串集合隨時都可變更。 當您第一次取出時，字串集合可能是空的，就像是最近連接的程式庫，但播放程式尚未列舉其內容。 相反地，字串集合可能已經包含您需要的所有資訊。 在這種情況下，您可能永遠不會收到 **StringCollectionChange** 事件，因為在您建立查詢之前已完全列舉程式庫的內容，而且沒有任何其他變更。

因此，若要讓使用者介面保持在最新的，您必須在抓取 **IWMPStringCollection** 介面時列舉字串集合內容，並在發生更新時處理 **StringCollectionChange** 事件以瞭解更新。

## <a name="sample"></a>範例

名為 WMPML 的範例示範如何使用程式庫服務。 如需 Windows Media Player SDK 範例的詳細資訊，請參閱 [範例](samples.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**關於程式庫**](about-the-library.md)
</dt> <dt>

[**關於 Query 物件**](about-the-query-object.md)
</dt> <dt>

[**IWMPEvents3 介面**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents3)
</dt> <dt>

[**IWMPLibrary 介面**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary)
</dt> <dt>

[**IWMPLibrary 介面 (VB 和 c # )**](iwmplibrary--vb-and-c.md)
</dt> <dt>

[**IWMPLibraryServices 介面**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibraryservices)
</dt> <dt>

[**IWMPLibraryServices 介面 (VB 和 c # )**](iwmplibraryservices--vb-and-c.md)
</dt> <dt>

[**IWMPMediaCollection 介面**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection)
</dt> <dt>

[**IWMPMediaCollection 介面 (VB 和 c # )**](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[**IWMPStringCollection 介面**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpstringcollection)
</dt> <dt>

[**IWMPStringCollection 介面 (VB 和 c # )**](iwmpstringcollection--vb-and-c.md)
</dt> <dt>

[**IWMPQuery 介面**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpquery)
</dt> <dt>

[**IWMPQuery 介面 (VB 和 c # )**](iwmpquery--vb-and-c.md)
</dt> <dt>

[**使用程式庫**](working-with-the-library.md)
</dt> </dl>

 

 





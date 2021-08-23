---
title: 探索頁面
description: 探索頁面
ms.assetid: deb0cbf9-b7e1-4ce6-8241-b9199129515a
keywords:
- Windows Media Player 線上商店，探索頁面
- 線上商店，探索頁面
- 輸入1個線上商店，探索頁面
- Windows Media Player 程式庫，探索頁面
- 程式庫，探索頁面
- 探索頁面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe29ed5d3948bbdcd6f36239938e3a4e552362318b6ec48658e85895cb58d163
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997338"
---
# <a name="discovery-pages"></a>探索頁面

如果有效的線上商店是類型1存放區，Windows Media Player 會在其使用者介面中顯示商店的內容。 程式庫樹狀檢視控制項具有線上商店的節點。 當使用者按一下該節點或其任何子節點時，Windows Media Player 會在詳細資料窗格中顯示線上商店的內容。

當使用者與樹狀檢視控制項或詳細資料窗格中的線上商店內容互動時，Windows Media Player 會顯示線上商店所提供的網頁，稱為 [*探索] 頁面*。 當使用者流覽線上商店的目錄時，探索頁面會提供音樂的其他相關資訊。 探索頁面會透過[外部物件](external-object-for-type-1-online-stores.md)的屬性、方法和事件與 Windows Media Player 進行通訊。

每當 Windows Media Player 變更線上商店內容的查看時，它會呼叫由線上商店的外掛程式所執行的[IWMPContentPartner：： GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate)，以取得要與新視圖一起顯示之探索頁面的 URL。

在 Windows Media Player 中，線上商店內容的顯示方式有五項資訊：工作、位置類型、位置識別碼、選取的專案類型，以及選取的專案識別碼。 Windows Media Player *將這* 五個專案提供給工作、*位置*、 *pCoNtext*、 *clickLocation* 和 *pClickCoNtext* 參數中的 **GetTemplate** 方法。 Windows Media Player 會將這五個專案提供給 **外部** 物件的 *task*、 *libraryLocationType*、 *libraryLocationID*、 *selectedItemType* 和 *selectedItemID* 屬性中的探索頁面使用。 如需 Windows Media Player 如何指定其線上商店內容之觀點的詳細資訊，請參閱[位置和選取的專案](location-and-selected-item.md)。

除了讓探索頁面與 Windows Media Player 通訊之外，**外部** 物件也可讓探索頁面與線上商店的外掛程式進行通訊。 發生這種情況時，Windows Media Player 會作為探索頁面與外掛程式之間的橋樑。 例如，[探索] 頁面可以呼叫 [sendMessage](external-sendmessage.md) ，以將自訂訊息傳送至外掛程式。 Windows Media Player 接收此方法呼叫，然後再呼叫[IWMPContentPartner：： SendMessage](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage) ，將訊息傳遞至外掛程式。 外掛程式完成訊息的處理之後，就會呼叫 [IWMPContentPartnerCallback：： SendMessageComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete)。 Windows Media Player 接著會引發[OnSendMessageComplete](external-onsendmessagecomplete-event.md)事件，以通知探索頁面。

**外部** 物件也提供可讓探索頁面與另一個探索頁面通訊的方式。 當探索頁面上的腳本呼叫 [changeView](external-changeview.md)時，腳本可以在 *ViewParams* 參數中提供字串。 Windows Media Player 不會解讀 *ViewParams* 字串，但它會將字串提供給 [viewParameters](external-viewparameters.md)屬性中的下一個 [探索] 頁面。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**關於類型1線上商店**](about-type-1-online-stores.md)
</dt> <dt>

[**位置和選取的專案**](location-and-selected-item.md)
</dt> </dl>

 

 





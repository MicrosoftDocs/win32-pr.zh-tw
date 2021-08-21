---
title: 視圖快取
description: 視圖快取
ms.assetid: d19c111c-1367-43a2-97a9-35dc0ff5dcc8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b155c0a9d3229db85a52b0589c4854bdee9a2e8e4171e231480036c512af737
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047676"
---
# <a name="view-caching"></a>視圖快取

容器應用程式必須能夠取得物件的呈現方式，以便在檔開啟時顯示或列印該物件，但是物件的伺服器應用程式不在執行中，或未安裝在使用者的電腦上。 不過，假設檔中的所有物件的伺服器都安裝在每個使用者的電腦上，而且隨時都可以視需要執行。 可以隨時使用的預設物件處理常式，會藉由在檔的儲存體中快取物件簡報並在任何平臺上操作這些簡報，來解決這個難題，而不管任何特定的容器安裝上可用性的物件服務器為何。

容器可以維護一或多個特定目標裝置的繪圖簡報，以及維護螢幕上物件所需的繪圖。 此外，如果您將物件從某個平臺移植到另一個平臺，OLE 會自動將物件的資料格式轉換為新平臺所支援的格式。 例如，如果您將物件從 Windows 移至 Macintosh，則 OLE 會將其中繼檔簡報轉換成 PICT 格式。

為了將内嵌物件的精確表示呈現給使用者，物件的容器應用程式會使用物件處理常式起始對話方塊，要求資料和繪製指示。 若要能夠滿足容器的要求，處理常式必須執行 [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject)、 [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2)和 [**IOleCache**](/windows/desktop/api/OleIdl/nn-oleidl-iolecache) 介面。

[**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) 可讓 OLE 容器應用程式取得資料，並將資料傳送至其內嵌或連結的物件。 當物件中的資料變更時，此介面會提供方法讓物件將其新資料提供給其容器，並提供容器更新其物件複本中資料的方式。  (如需資料傳輸的一般討論，請參閱第4章：資料傳輸 ) 。

[**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2)介面與 [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject)介面非常類似，不同之處在于它會要求物件在裝置內容（例如螢幕、印表機或中繼檔）上自行繪製，而不是將其資料移動或複製到記憶體或某些其他傳輸媒體。 介面的目的是要讓 OLE 容器取得其内嵌物件的替代圖解標記法，其資料已經有，藉此避免必須直接傳送相同資料物件之新實例的額外負荷，才能取得新的繪圖指令。 相反地， **IViewObject2** 介面可讓容器藉由在容器所指定的裝置內容中繪製，來要求物件提供其本身的圖形標記法。

當您呼叫 [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2) 介面時，容器應用程式也可以指定物件在目標裝置上繪製本身，而不是實際呈現該物件的目標裝置。 這會視需要啟用容器，以產生單一物件的不同轉譯。 例如，呼叫者可能會要求物件為印表機撰寫，即使產生的繪圖將會在螢幕上呈現也一樣。 當然，結果就是物件的預覽列印。

[**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2)介面也提供可讓容器註冊 view 變更通知的方法。 如同資料和 OLE 諮詢一樣，view 諮詢連接可讓容器以自己的便利性更新其物件的轉譯，而不是回應物件的呼叫。 例如，如果新版本的物件服務器應用程式提供相同資料的其他視圖，則物件的預設處理常式會呼叫每個容器的 [**IAdviseSink：： OnViewChange**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onviewchange) 實值，讓他們知道新的簡報可供使用。 只有在需要時，容器才會從建議接收取得此資訊。

因為 Windows 裝置內容只有在單一進程內有意義，所以您無法跨進程界限傳遞 [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2)指標。 如此一來，OLE 本機和遠端伺服器就不需要執行介面，即使有的話也不會正常運作。 只有物件處理常式和同進程伺服器會執行 **IViewObject2** 介面。 OLE 提供預設的實作為，只要藉由匯總 OLE 預設處理常式，您就可以在自己的 OLE 同進程伺服器和物件處理常式中使用。 或者，您也可以撰寫自己的 **IViewObject2** 執行。

物件會實 [**IOleCache**](/windows/desktop/api/OleIdl/nn-oleidl-iolecache) 介面，以便讓處理常式知道它應該快取的功能。 物件處理常式也擁有快取，並確保它會保持最新狀態。 當内嵌物件進入「執行中」狀態時，處理常式會在伺服器物件上設定適當的諮詢連接，其本身可作為接收。 [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject)和 [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2)介面的執行作業會在用戶端上快取的資料上運作。 處理常式的 **IViewObject2** 會負責決定要快取的資料格式，以便滿足用戶端繪製要求。 處理常式的 **IDataObject** 會負責取得不同格式的資料，以及在記憶體和内嵌物件的基礎 [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) 實例之間取得資料。 自訂處理常式可以藉由匯總預設處理常式來使用這些實值。

> [!Note]  
> [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2)介面是 [**IViewObject**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject)的簡單功能延伸模組，而且應該執行，而非後者現在已淘汰的介面。 除了提供 **IViewObject** 方法之外， **IViewObject2** 介面還提供一個額外的 [**GetExtent**](/windows/desktop/api/OleIdl/nf-oleidl-iviewobject2-getextent)成員，可讓容器應用程式從快取中取得物件展示的大小，而不需要先透過呼叫 [**IOleObject：： GetExtent**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getextent)，將物件移到執行中狀態。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[複合檔案](compound-documents.md)
</dt> </dl>

 

 
---
title: 在沒有介面時正常降級
description: 由於控制項可能不支援 IUnknown 以外的任何介面，因此當容器遇到任何特定的介面時，就必須正常地降級。
ms.assetid: 1b833900-2357-4b39-b88d-5ee6321f488e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fef1b329faa2d4da333cf2e201fc887764af96bc5ea2573060f41774b57c0d56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119501270"
---
# <a name="degrading-gracefully-in-the-absence-of-an-interface"></a>在沒有介面時正常降級

由於控制項可能不支援 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)以外的任何介面，因此當容器遇到任何特定的介面時，就必須正常地降級。

其中一個問題可能就是控制項的實用性，不只是 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)。 但是，請考慮控制項從容器的視覺化程式設計環境接收的優點 (例如 VB) 當容器將物件辨識為控制項時：

-   物件的按鈕會出現在 [工具箱] 中。
-   您可以將物件從 [工具箱] 拖曳到表單上，以建立物件。
-   您可以為物件提供一個可在視覺化程式設計環境中辨識的名稱。
-   上述 (3) 中的相同名稱可以立即用於撰寫相同表單上控制項的任何其他程式碼， (或甚至不同的表單) 。
-   容器可以自動提供該物件所提供之任何事件的程式碼進入點。
-   容器會為任何可用的屬性提供自己的屬性流覽 UI。

當物件無法辨識為控制項時，它可能會失去這些功能強大且有用的整合功能。 例如，在 Visual Basic 4.0 中，很難真正地整合某個不是完整意義之控制項的隨機物件，但可能仍有屬性和事件。 因為 Visual Basic 4 對控制項的概念非常嚴格，所以物件不會得到上述任何整合功能。 但即使是具有 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)的控制項（控制項的單純存留期決定了某些資源的存在），也應該能夠獲得上述的整合功能。

由於目前的工具需要大量的控制介面才能獲得任何優點，因此控制項通常會導致過度實行，使其包含的程式碼比真正需要的還要多。 可能會7K 的控制項可能會被25K，這是網際網路等區域中的重大效能問題。 這也表示，因為執行所有介面的複雜度，所以只能使用 CDK 之類的工具來執行控制項，而這對於這類控制項需要大型 DLL （例如 OC30.DLL）的影響，因而增加了工作集。 如果並非所有介面都是必要的，則會開啟許多開發人員，以使用直接的 OLE 或其他工具來撰寫非常小的控制項，並將每個控制項的額外負荷降到最低。

這就是為什麼此附錄會將控制項辨識為具有 CLSID 和 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) 介面的任何物件。 即使沒有 IUnknown，具有程式設計環境的容器應該至少能提供功能 \# 3 和 ) 登錄專案，它會取得 \# 1 和 \# 2。 如果物件提供 [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) (，而 [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) 通常是某些事件集的) ，則會取得 \# 5，如果它支援屬性和方法的 **IDispatch** ，則會獲得 \# 6，以及容器中更好的程式碼整合。

簡單地說，物件應該可以實作為 **IDispatch** ，以及透過 [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) 公開的一個事件集，以獲得上述所有的視覺功能。

請記住，下表說明容器在沒有任何可能的介面時，可能會執行的動作。 請注意，只會列出這些介面，容器將直接透過 [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q))取得這些介面。 其他介面（例如 [**IOleInPlaceActiveObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplaceactiveobject)）則是透過其他方式取得。



| 介面                                                                                                             | 介面缺少的意義                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2)<br/>                                                                       | 控制項沒有視覺效果，因此它本身不會有任何視覺效果，因此沒有可提供的明確範圍。 在執行時間中，容器不會在此介面不存在時嘗試繪製任何程式。 在設計階段中，容器必須至少繪製某種類型的預設矩形，以用於這類控制項，因此視覺化程式設計環境中的使用者可以選取物件，並簽出其屬性、方法和現有的事件。 處理不 [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2) 的問題，對於良好的視覺化程式設計支援非常重要。<br/> |
| [**IOleObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleobject)<br/>                                                                           | 控制項不需要網站，也不會參與任何內嵌的物件版面配置協商。 任何 (如控制範圍的資訊，都應該使用容器提供的預設值來填入容器可能預期來自此介面的) 。<br/>                                                                                                                                                                                                                                                                                                       |
| [**IOleInPlaceObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplaceobject)<br/>                                                             | 控制項不會就地使用 (例如標籤) ，因此永遠不會嘗試以這種方式啟動。 它的唯一啟用可能是其屬性頁。<br/>                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol)<br/>                                                                         | 控制項沒有助憶鍵，且不會使用環境屬性，也不會在意容器是否會忽略事件。 如果沒有這個介面，容器就不會呼叫其方法。<br/>                                                                                                                                                                                                                                                                                                                                                                         |
| [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject)<br/>                                                                         | 此控制項不提供任何可以快取的屬性集，也不會提供任何視覺轉譯，因此容器會選擇在缺少此介面的情況下快取一些預設呈現 (CF METAFILEPICT 的支援 \_ ，特別是) 並停用任何屬性集相關功能。<br/>                                                                                                                                                                                                                                                                            |
| **IDispatch**<br/>                                                                                              | 控制項沒有任何自訂屬性或方法。 在此情況下，容器不需要嘗試顯示任何控制項屬性，而且應該不允許容器無法辨識為屬於自己擴充控制項的任何自訂方法呼叫， (可支援) 的方法和屬性。 由於延伸控制項通常會將某些 **IDispatch** 呼叫委派給控制項，因此擴充的控制項不應預期控制項完全具有 **IDispatch** 。<br/>                                                                                          |
| [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer)<br/>                                             | 控制項沒有事件，因此容器不需要考慮處理任何事件。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo)<br/> [**Iprovideclassinfo2.getguid**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2)<br/> | 控制項可能沒有類型資訊或事件，或容器必須透過控制項的登錄專案進入控制項的類型資訊。 這個介面的存在是優化的。<br/>                                                                                                                                                                                                                                                                                                                                            |
| [**ISpecifyPropertyPages**](/windows/desktop/api/OCIdl/nn-ocidl-ispecifypropertypages)<br/>                                                     | 控制項沒有屬性頁，因此如果容器具有任何可叫用它們的 UI，容器應該停用該 UI。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**IPerPropertyBrowsing**](/windows/desktop/api/OCIdl/nn-ocidl-iperpropertybrowsing)<br/>                                                       | 控制項沒有顯示名稱本身、沒有預先決定的字串和值，也沒有頁面對應的屬性。 這個介面幾乎一律用來產生容器使用者介面，因此在沒有此介面的情況下，將會停用這類 UI 元素。<br/>                                                                                                                                                                                                                                                                                                 |
| IPersist\*<br/>                                                                                                 | 控制項沒有任何持續性的狀態，因此容器不需要擔心儲存任何控制項特定資料。 當然，容器也會將控制項的相關資訊儲存在本身的表單或檔中，但是控制項本身並沒有任何專案可參與該資訊。<br/>                                                                                                                                                                                                                                                        |
| [**IOleCache**](/windows/desktop/api/OleIdl/nn-oleidl-iolecache)<br/> [**IOleCache2**](/windows/desktop/api/OleIdl/nn-oleidl-iolecache2)<br/>                                 | 物件不支援快取。 容器仍可支援快取，只要使用 [**CreateDataCache**](/windows/desktop/api/ObjBase/nf-objbase-createdatacache)建立資料快取本身即可。<br/>                                                                                                                                                                                                                                                                                                                                                                                                    |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[容器](containers.md)
</dt> </dl>

 

 






---
title: 透過 IPropertyNotifySink 的資料系結
description: 透過 IPropertyNotifySink 的資料系結
ms.assetid: 275a84b3-65d8-43de-bfba-72e3e5ee59fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 337233455872928f824d8cbb903aba247b1ef496d02c0af04223361731fe3663
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854648"
---
# <a name="data-binding-through-ipropertynotifysink"></a>透過 IPropertyNotifySink 的資料系結

支援屬性的物件（例如透過 OLE Automation 和 **IDispatch** 介面）可能會想要允許在某些屬性變更值時通知用戶端。 這類屬性稱為可系結屬性，因為通知可讓用戶端同步處理它自己的物件目前屬性值的顯示。 此外，相同的物件可能會想要允許用戶端控制何時允許變更特定屬性。 這類屬性稱為「要求編輯屬性」。

[**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink)是一種標準的通知介面，可支援可系結和要求編輯的屬性。 從具有屬性（property）輸出介面的物件，支援 **IPropertyNotifySink** 。 也就是說，介面本身是由用戶端的接收物件所執行，而且用戶端會透過稍早所述的連接點機制，將接收器連接至支援的物件。 **IPropertyNotifySink** 的定義如下：

``` syntax
interface IPropertyNotifySink : IUnknown 
  { 
    HRESULT OnChanged([in] DISPID dispID); 
    HRESULT OnRequestEdit([in] DISPID dispID); 
  } 
 
```

當物件希望通知其連接的接收時，以指定的 DISPID 識別的可系結屬性已變更時，它會呼叫 [**OnChanged**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onchanged)。 如果物件一次變更多個屬性，則會將 DISPID \_ 未知傳遞給 **OnChanged** ，在此情況下，用戶端會重新整理其所有相關屬性值的快取。

當要求編輯屬性即將變更時，物件會要求用戶端是否允許發生變更。 物件會呼叫 [**OnRequestEdit**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onrequestedit) ，並將有問題的 dispid 屬性 (或 dispid \_ 未知，以找出) 的所有屬性。 用戶端的接收會傳回「 \_ 確定」，表示允許變更或 \_ (的錯誤，或) 指出不允許變更。 當物件呼叫 **OnRequestEdit** 時，必須遵循「確定」和「FALSE」傳回值的確切語義來遵守用戶端的願望 \_ \_ 。

請注意， [**OnRequestEdit**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onrequestedit) 無法用於資料驗證，因為在呼叫時，屬性的新值還無法使用。 通知只能用來控制屬性的唯讀狀態。

物件可控制哪些屬性是可系結的，並且要求編輯並在物件的型別資訊中標記這類屬性。 在類型資訊中，屬性可系結將屬性標示為支援 [**OnChanged**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onchanged)。 屬性 requestedit 會將屬性標示為支援 [**OnRequestEdit**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onrequestedit)。

其中一個屬性可支援這兩種行為，在這種情況下，會先呼叫 [**OnRequestEdit**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onrequestedit) ，而且只有在允許變更時才會呼叫 [**OnChanged**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onchanged) 。

這類屬性行為的唯一例外狀況是，由於物件的初始化或載入程式，不會傳送任何通知。 在這種情況下，會假設所有屬性都有變更，而且必須允許全部變更。 因此，只有在完全初始化/已載入物件的內容中，此介面的通知才有意義。

您可以將其他兩個屬性套用至物件類型資訊中的屬性。 Defaultbind 屬性會將可系結屬性標示為最能表示整體物件狀態的屬性。 Displaybind 屬性會將可系結的屬性標示為適合在用戶端自己的使用者介面中顯示。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[屬性頁和屬性工作表](property-pages-and-property-sheets.md)
</dt> </dl>

 

 





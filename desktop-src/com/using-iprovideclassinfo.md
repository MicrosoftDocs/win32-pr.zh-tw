---
title: 使用 IProvideClassInfo
description: 使用 IProvideClassInfo
ms.assetid: 16541aab-474f-4ae5-a6b6-fb2fea6d38ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32a3abd61bb330a2a7d681b6d53648c5fbde8c53
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104024165"
---
# <a name="using-iprovideclassinfo"></a>使用 IProvideClassInfo

可連線物件可提供 [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) 和 [**iprovideclassinfo2.getguid**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2) 介面，讓其用戶端可以輕鬆地檢查其類型資訊。 這項功能在處理輸出介面時很重要，因為定義是由物件定義，但由用戶端在其本身的接收物件上執行。 在某些情況下，在編譯時期，可連接的物件和接收物件都知道輸出介面;這就是 [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink)的情況。

不過，在其他情況下，只有可連接的物件會在編譯時期知道它的輸出介面定義。 在這些情況下，用戶端必須取得輸出介面的型別資訊，讓它能夠動態提供支援正確進入點的接收，如下所示：

1.  用戶端會列舉連接點，然後取得可連線物件所支援之輸出介面的 Iid，針對每個連接點呼叫 [**IConnectionPoint：： GetConnectionInterface**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-getconnectioninterface) 。
2.  用戶端會查詢其中一個 [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) 介面的可連線物件。
3.  用戶端會呼叫 [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) 介面中的方法，以取得輸出介面的型別資訊。
4.  用戶端會建立支援輸出介面的接收物件。
5.  此程式會繼續，且用戶端會呼叫 [**IConnectionPoint：： Advise**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-advise) 將其接收連接到連接點。

在類型資訊中，屬性 [**來源**](/windows/desktop/Midl/source)會將 [**coclass**](/windows/desktop/Midl/coclass)底下所 [**列的**](/windows/desktop/Midl/dispinterface)[**介面**](/windows/desktop/Midl/interface)或介面介面標示為連出介面。 如果未列出此屬性，則會將其視為傳入介面。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[可連線物件介面](connectable-object-interfaces.md)
</dt> <dt>

[提供類別資訊](providing-class-information.md)
</dt> </dl>

 

 
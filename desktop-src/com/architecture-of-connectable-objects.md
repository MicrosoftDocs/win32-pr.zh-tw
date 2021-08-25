---
title: 可連線物件的架構
description: 可連線物件的架構
ms.assetid: 69949a3b-3ab8-4054-84d8-9256fbf39c7b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1215b013c3db751e90b07ed21d5f897ef0332000ce2cd2b3b167cbe86798927
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993951"
---
# <a name="architecture-of-connectable-objects"></a>可連線物件的架構

可連線物件是可連線物件之整體架構的其中一個部分。 這項技術包含下列元素：

-   **可連線物件。** 會實 [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) 介面;至少建立一個連接點物件;定義用戶端的輸出介面。
-   **客戶。** 查詢物件以進行 [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) ，以判斷物件是否可連接;建立接收物件，以執行可連線物件所定義的連出介面。
-   **接收物件。** 會實作為輸出介面;用來建立連線物件的連接。
-   **連接點物件。** 會執行 [**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) 介面並管理與用戶端接收的連接。

下圖說明用戶端、可連線物件、連接點和接收器之間的關聯性：

![此圖表顯示用戶端與可連線物件之間的連接點。](images/1cd44fec-5d2c-4427-846b-ccab7ec0b08a.png)

在連接點物件于上圖中的步驟3中呼叫接收器介面內的方法之前，它必須是所需的特定介面的 [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) ，即使指標已在「 [**建議**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-advise) 」方法的步驟2呼叫中傳遞。

這兩個列舉值物件也會包含在此架構中，但不會顯示于圖例中。 其中一個是由 [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) 中的方法所建立，用來列舉可連線物件內的連接點。 另一個是透過 [**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) 中的方法來建立，以列舉目前為該連接點建立的連接。 一個連接點可以支援多個連接的接收介面，而且每次在該介面上進行方法呼叫時，都應該逐一查看連接清單。 此進程稱為多播。

使用可連線物件時，請務必瞭解可連接的物件、每個連接點、每個接收和所有列舉值都是個別的物件，具有個別的 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) 實值、個別的參考計數和個別的存留期。 使用這些物件的用戶端一律負責釋放它擁有的所有參考計數。

> [!Note]  
> 可連線物件可支援一個以上的用戶端，而且可以支援用戶端內的多個接收器。 同樣地，接收也可以連接到多個可連接的物件。

 

在用戶端與可連線物件之間建立連接的步驟如下：

1.  用戶端會查詢物件上的 [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) ，以判斷物件是否為可連接的。 如果成功呼叫，用戶端會在可連線物件上保存 **IConnectionPointContainer** 介面的指標，且可連接的物件參考計數器已遞增。 否則，物件是無法連接的，且不支援輸出介面。
2.  如果物件是可連接的，則用戶端接著會嘗試取得可連線物件內連接點上 [**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) 介面的指標。 在 [**IConnectionPointContainer：： FindConnectionPoint**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpointcontainer-findconnectionpoint) 和 [**IConnectionPointContainer：： EnumConnectionPoints**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpointcontainer-enumconnectionpoints)中，有兩種方法可以取得此指標。 如果使用 **EnumConnectionPoints** ，則需要一些額外的步驟。  (如需詳細資訊，請參閱 [使用 IConnectionPointContainer](using-iconnectionpointcontainer.md) 。 ) 如果成功，可連接的物件和用戶端都支援相同的輸出介面。 可連線物件會定義它並呼叫它，而用戶端會執行它。 然後，用戶端可以透過可連線物件內的連接點進行通訊。
3.  然後，用戶端會呼叫連接點上的 [**建議**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-advise) ，以建立其接收介面與物件連接點之間的連接。 在這個呼叫之後，物件的連接點會保存接收器上連出介面的指標。
4.  「 [**建議**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-advise) 」內的程式碼會在傳入的介面指標上呼叫 [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) ，要求它所連接的特定介面識別碼。
5.  物件會視需要呼叫接收器介面上的方法，並使用其連接點所持有的指標。
6.  用戶端會呼叫 [**Unadvise**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-unadvise) 來終止連接。 然後，用戶端會呼叫 **IConnectionPoint：： Release** 以釋放其在連接點上的保留，因此也可以連接到主要的可連線物件。 用戶端也必須呼叫 **IConnectionPointContainer：： Release** ，才能在主要可連線物件上釋放其保存。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[可連線物件介面](connectable-object-interfaces.md)
</dt> </dl>

 

 





---
title: COM 和可連線物件中的事件
description: 當程式偵測到發生的情況時，就會通知其用戶端。
ms.assetid: f6ffbd1d-4bc1-4dc2-b3ed-ee12359e3d75
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa5115cfd08d57658eec879d44b4361e88965b3c
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "104022962"
---
# <a name="events-in-com-and-connectable-objects"></a>COM 和可連線物件中的事件

當程式偵測到發生的情況時，就會通知其用戶端。 例如，如果股票報價方案偵測到股票價格的變化，它可以通知所有用戶端的變更。 此通知處理常式稱為 *引發事件*。

使用 COM 時，伺服器物件可以使用 COM 事件來引發事件，而不需要通知物件的任何相關資訊。 物件也可以使用可連接的 *物件* 來維護已要求通知之用戶端的詳細資訊。

COM 可連線物件除了連入介面外，還提供外寄介面給其用戶端。 因此，物件及其用戶端可以進行雙向通訊。 傳入介面會在物件上執行，並接收來自物件外部用戶端的呼叫，而傳出介面則是在用戶端的接收上執行，並接收來自物件的呼叫。 物件會定義它想要使用的介面，且用戶端會執行它。

物件會定義其傳入介面，並提供這些介面的實作為。 連入介面可透過物件的 [**IUnknown：： QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) 方法提供給用戶端。 用戶端會呼叫物件上的傳入介面方法，而物件會代表用戶端執行想要的動作。

輸出介面也會由物件定義，但用戶端會在用戶端所建立的接收物件上提供傳出介面的實作為。 然後，此物件會呼叫接收物件上之輸出介面的方法，以通知用戶端物件中的變更、在用戶端中觸發事件、從用戶端要求某個內容，或者，對於物件建立者所提出的任何目的。

輸出介面的其中一個範例是 IButtonSink 介面，這個介面是由推播按鈕控制項所定義，用來通知其事件的用戶端。 例如，當使用者按一下螢幕上的按鈕時，按鈕物件會在用戶端的接收物件上呼叫 IButtonSink：： OnClick。 按鈕控制項會定義輸出介面。 若要讓按鈕的用戶端處理事件，用戶端必須在接收物件上執行該輸出介面，然後將該接收連接到按鈕控制項。 然後，當事件發生在按鈕時，按鈕就會呼叫接收，此時用戶端可以執行任何想要指派給該按鈕的動作。

可連線物件提供物件對用戶端通訊的一般機制。 任何想要公開任何類型之事件或通知的物件，都可以使用這項技術。 除了一般可連線物件技術之外，COM 也提供許多特殊用途的接收和網站介面，可供物件用來通知用戶端感興趣的特定事件。 例如，物件可使用 [**IAdviseSink**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink) 來通知用戶端資料，並查看物件中的變更。

如需詳細資訊，請參閱下列主題：

-   [可連線物件的架構](architecture-of-connectable-objects.md)
-   [可連線物件介面](connectable-object-interfaces.md)

 

 





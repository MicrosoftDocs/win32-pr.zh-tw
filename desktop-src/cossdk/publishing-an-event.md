---
description: 發行事件
ms.assetid: b40d10aa-43bc-4c53-9e89-94c585d34238
title: 發行事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 724dc94ddf9cc25ec3b11cc31376805241e9d6d67250f8a494f8b417b9d201a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119990498"
---
# <a name="publishing-an-event"></a>發行事件

若要發佈事件，只要呼叫 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)或使用 EventClassID 或 EventClassName 作為引數的 Microsoft Visual Basic **CreateObject** 方法，即可將事件物件具現化。 發行者會呼叫事件物件上的 [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 來取得事件類別物件所支援的介面，並透過介面，在事件物件上叫用方法來發佈事件。 然後，事件系統會在 \_ 具有介面識別碼 IID IEventObjectChange 的事件類別 CLSID EventObjectChange 上發佈事件 \_ 。

為了支援將事件傳遞給多個訂閱者，事件類別方法應該只包含在參數中。

藉由使用 [事件類別](the-com--event-class-object.md) 物件的 FireInParallel 屬性，發行者可以要求事件系統使用多個執行緒，將事件傳遞給多個訂閱者。 選取平行傳遞機制並不保證將事件同時傳遞給多個訂閱者，但它會指示 COM + 事件服務允許發生此情況。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[在 COM + 中發行和傳遞事件](publishing-and-delivering-events-in-com-.md)
</dt> </dl>

 

 

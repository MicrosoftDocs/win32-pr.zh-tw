---
description: 若要發佈事件，只要將事件類別物件具現化，並叫用所需的方法;如需如何在程式碼中進行這項作業的詳細指示，請參閱發佈事件。
ms.assetid: 835c3753-fdcc-4afe-94c3-c954aaf1c832
title: 在 COM + 中發行和傳遞事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7de1625d1e18340d71b3ad3a53c06d2db79b9fd1f913e7a49274644bc3a715c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118812859"
---
# <a name="publishing-and-delivering-events-in-com"></a>在 COM + 中發行和傳遞事件

若要發佈事件，只要將 [事件類別](the-com--event-class-object.md) 物件具現化，並叫用所需的方法;如需如何在程式碼中進行這項作業的詳細指示，請參閱 [發佈事件](publishing-an-event.md)。

當發行者引發事件時，COM + 事件服務會搜尋訂閱資料庫，以尋找已向具現化事件類別註冊訂用帳戶的所有訂閱者。 它會連接到這些訂閱者 (由直接建立、標記或佇列元件) ，然後呼叫方法。 若要支援一個事件的多個訂閱者通知，方法只可包含在參數中，而且必須只傳回成功或失敗的 **HRESULT** 值。

> [!Note]  
> 此版本的 COM + 事件不支援分散式事件存放區。 訂閱者必須在每一部要接收通知的電腦上訂閱事件。 或者，您可以在中央電腦上註冊事件類別物件和訂用帳戶，並從您發佈事件的遠端電腦，將此事件類別物件具現化。 事件的傳遞是由 DCOM 或由 COM + 佇列元件服務提供。 如需使用 COM + 佇列元件服務的詳細資訊，請參閱使用 com + [事件與 COM + 佇列元件](using-com--events-with-com--queued-components.md)。

 

根據預設，COM + 事件服務會以未決定或可重複的順序，一次引發一個事件。 需要控制訂閱者接收事件之順序的發行者，可以執行發行者篩選。  (需詳細資訊，請參閱 [在 COM + 中篩選事件](filtering-events-in-com-.md)) 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[在 COM + 中篩選事件](filtering-events-in-com-.md)
</dt> <dt>

[訂用帳戶](subscriptions.md)
</dt> <dt>

[COM + 事件類別物件](the-com--event-class-object.md)
</dt> <dt>

[使用 com + 事件與 COM + 佇列元件](using-com--events-with-com--queued-components.md)
</dt> </dl>

 

 




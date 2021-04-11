---
description: 建立邏輯事件取用者和事件篩選器之後，您必須連結它們，以註冊邏輯取用者接收篩選所指定之事件的通知。
ms.assetid: 2fc3d781-2b93-4e9e-90a1-1b975ab40a01
ms.tgt_platform: multiple
title: 使用邏輯取用者來系結事件篩選器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e99f44c4b64b98877231b73543d8753c765c3219
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851672"
---
# <a name="binding-an-event-filter-with-a-logical-consumer"></a>使用邏輯取用者來系結事件篩選器

建立邏輯事件取用者和事件篩選器之後，您必須連結它們，以註冊邏輯取用者接收篩選所指定之事件的通知。

下列程式說明如何將事件篩選器與邏輯取用者系結。

**系結事件篩選器與邏輯取用者**

1.  在 WMI 存放庫中建立 [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md)系統類別的實例。

    [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md)類別是一個關聯類別，可透過 **篩選** 和取用 **者** 參考屬性，將事件篩選準則實例和邏輯取用者實例連結在一起。 如需詳細資訊，請參閱宣告 [關聯類別](declaring-an-association-class.md)。

2.  將 [ **篩選** ] 屬性設定為篩選準則的實例。
3.  將取用 **者** 屬性設定為邏輯取用者的實例。
4.  設定 **DeliverSynchronously** 屬性，以判斷您想要的傳遞類型。

    **DeliverSynchronously** 屬性可決定 WMI 何時以同步或非同步方式傳遞事件通知。 將這個屬性設定為 **TRUE** 會要求同步傳遞。 只有在永久取用者可以在大約100毫秒內處理事件時，才使用同步傳遞。

    > [!Note]  
    > 由於接收端的回呼可能不會與用戶端所需的驗證層級傳回，因此建議您使用 [半同步] 而非 [非同步通訊]。 如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。

     

5.  當您取消註冊邏輯事件取用者時，請務必刪除 [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md)實例。

    每個 [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md)實例都代表特定事件通知的註冊。 當您刪除系結時，WMI 會停用註冊。 您可能必須刪除邏輯取用者和事件篩選準則實例，才能根據執行來停用註冊。

下列程式碼範例會顯示 [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md)實例，此實例會將 [**ActiveScriptEventConsumer**](activescripteventconsumer.md)類別的實例與特定事件篩選器產生關聯 (在建立 [邏輯取用者](creating-a-logical-consumer.md)主題中建立事件取用者的實例，並在 [[建立事件篩選器](creating-an-event-filter.md)] 主題中建立事件篩選器) 。

``` syntax
instance of __FilterToConsumerBinding
{
    Filter = $FILTER;
    Consumer = $CONSUMER;
    DeliverSynchronously=FALSE;

    // this is the Administrators SID in array of bytes format
    CreatorSID = {1,2,0,0,0,0,0,5,32,0,0,0,32,2,0,0}; 
};
```

除非取用者是本機系統管理員群組的成員，否則兩個取用者（ [**ActiveScriptEventConsumer**](activescripteventconsumer.md) 和 [**CommandLineEventConsumer**](commandlineeventconsumer.md)）將無法運作。

**:** 當系統管理員建立訂用帳戶時，它的 SID 不會用在 **CreatorSID** 屬性中，而是改用本機 Administrators 群組的 sid。 因此，實例可以由不同的系統管理員建立，且訂用帳戶仍可運作。 如需詳細資訊，請參閱 [安全地接收事件](receiving-events-securely.md)。

當篩選準則系結至邏輯取用者時，Windows (ETW) 的 [事件追蹤](/windows/desktop/ETW/event-tracing-portal) 會記錄事件。 如需詳細資訊，請參閱 [追蹤 WMI 活動](tracing-wmi-activity.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[隨時接收事件](receiving-events-at-all-times.md)
</dt> </dl>

 

 

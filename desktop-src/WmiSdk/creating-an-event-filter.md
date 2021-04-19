---
description: 事件篩選器是一種 WMI 類別，描述 WMI 傳遞給實體取用者的事件。
ms.assetid: c0ce26a4-5ff2-44b4-8550-c7d8ad0ba0f0
ms.tgt_platform: multiple
title: 建立事件篩選器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 693e4ef2eee5de14550b8efbf25a9b6720d6a8b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980081"
---
# <a name="creating-an-event-filter"></a>建立事件篩選器

事件篩選器是一種 WMI 類別，描述 WMI 傳遞給實體取用者的事件。 例如，事件篩選器可以指示 WMI 傳遞給取用者所有的電源管理事件，或所有系統重新開機事件。 事件篩選器也會說明 WMI 傳遞事件的條件。 事件篩選器可以指定內建或外來事件;而且篩選可以參考源自命名空間的事件，也就是篩選的命名空間以外的事件。 永久取用者在取用者、篩選和系結實例中必須具有相同的 [**CreatorSID**](--eventconsumer.md) 。 如需詳細資訊，請參閱 [安全地接收事件](receiving-events-securely.md)。

下列程式說明如何建立事件篩選準則。

**若要建立事件篩選器**

1.  建立 WMI [**\_ \_ >eventfilter**](--eventfilter.md)系統類別的實例。
2.  以下列兩種方式之一，使用 [ **名稱** ] 屬性建立篩選器的唯一識別碼：

    -   使用私用配置。

        只要您不與其他篩選命名配置發生衝突，就可以任意命名事件篩選器的運作方式。 您必須避免命名衝突，因為加入具有重複 **名稱** 值的實例會覆寫舊的實例。

    -   使用全域唯一識別碼 (GUID) 。

        如果您將 [ **名稱** ] 保留空白，WMI 就會填滿 GUID 的 **名稱** 。

3.  描述您想要使用 **查詢** 屬性篩選的事件種類。

    **查詢** 屬性包含 WMI 查詢語言 (WQL) 查詢，可描述您想要篩選的事件種類。 您可以使用各種不同的運算子和 WQL 延伸來進行精確的篩選。

    當來自永久性事件取用者的查詢失敗時，就會產生 NT 記錄事件。 事件的來源為 WinMgmt，事件識別碼為10，而事件種類為「錯誤」。

    WMI 比廣泛查詢更有效率地處理限制的特定查詢。 藉由建立特定查詢，您可以避免不必要的處理序間通訊和網路流量。 在提供者所產生的事件案例中，WMI 會對提供者執行篩選，這可確保只有符合篩選準則的事件會產生進程間的通訊成本。 如需詳細資訊，請參閱 [查詢 WMI](querying-wmi.md)。

4.  將 **QueryLanguage** 屬性設定為您在 **查詢** 屬性中使用的查詢語言類型。

    您幾乎一律會將 **QueryLanguage** 設定為「WQL」。

下列程式碼範例描述事件篩選器，每次 WMI 在根 cimv2 命名空間中建立 [**\_ \_ TimerEvent**](--timerevent.md)類別的實例時，就會對事件發出信號 \\ 。

``` syntax
instance of __EventFilter as $FILTER
{
    Name = "MyFilterName";
    Query = "select * from __TimerEvent where TimerID=\"MyTimer\"";
    QueryLanguage = "WQL";
    EventNamespace = "\root\cimv2";

    // this is the Administrators SID in array of bytes format
    CreatorSID = {1,2,0,0,0,0,0,5,32,0,0,0,32,2,0,0}; 
};
```

**EventNamespace** 屬性會指定事件來源的命名空間。 您不需要在事件來源的命名空間中建立篩選準則的實例。 如果您沒有指定命名空間，則 WMI 會在預設命名空間中建立篩選。 內建事件類別（例如 [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md) ）可在每個命名空間中使用。

若要為您的邏輯取用者註冊事件通知，您必須將事件篩選器系結至邏輯取用者。 如需詳細資訊，請參閱系結 [事件篩選與邏輯取用者](binding-an-event-filter-with-a-logical-consumer.md)。

 

 




---
description: 您可能會想要撰寫可隨時回應事件的應用程式。
ms.assetid: 475dca47-b1e5-4362-ab00-9ab9383e92f9
ms.tgt_platform: multiple
title: 隨時接收事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e049b7816e53439ede5edbc67c3bcdbaf6ed6e71accb8b3f994544cdd0efbd31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118817444"
---
# <a name="receiving-events-at-all-times"></a>隨時接收事件

您可能會想要撰寫可隨時回應事件的應用程式。 例如，系統管理員可能會想要在網路伺服器上的特定效能措施拒絕時收到電子郵件訊息。 在此情況下，您的應用程式應該隨時執行。 不過，持續執行應用程式並不會有效率地使用系統資源。 相反地，WMI 可讓您建立永久事件取用者。 永久事件取用者必須符合特殊的安全性需求。 如需詳細資訊，請參閱 [保護 WMI 事件](securing-wmi-events.md)。

永久事件取用者會收到事件，直到明確取消其註冊為止。

永久事件取用者是位於您系統上的下列 WMI 類別、篩選和 COM 物件的組合：

-   稱為實體取用者的 COM 物件。 WMI 提供數個標準的永久取用者。 例如，動態指令碼事件取用者 [會在事件發生時執行腳本](running-a-script-based-on-an-event.md)。
-   新的永久取用者類別。
-   永久取用者類別的實例，稱為邏輯取用者。
-   包含事件查詢的篩選準則。
-   取用者與篩選之間的連結。

邏輯事件取用者的屬性會指定在事件收到通知時要執行的動作，但不會定義與其相關聯的事件查詢。 當收到信號時，WMI 會自動將代表永久事件取用者的 COM 物件載入至使用中記憶體。 一般來說，這會在啟動期間或為了回應觸發的事件時發生。 在啟用之後，永久事件取用者會以一般事件取用者的形式運作，但會一直保留到作業系統特別卸載為止。

您可以撰寫自己的永久事件取用者，或使用 WMI 預先安裝的 [標準取用者類別](standard-consumer-classes.md)，例如 [**ActiveScriptEventConsumer**](activescripteventconsumer.md)。 如需詳細資訊，請參閱 [標準取用者類別](standard-consumer-classes.md)、 [使用標準取用者監視和回應事件](monitoring-and-responding-to-events-with-standard-consumers.md)，以及 [監視事件](monitoring-events.md)。

下列程式說明如何建立您自己的永久事件取用者。

**建立您自己的永久事件取用者**

1.  決定您想要接收的事件種類。

    WMI 支援內部和外來事件。 內建事件是 WMI 預先定義的事件，而外建事件則是由協力廠商提供者所定義的事件。 如需詳細資訊，請參閱 [決定要接收的事件種類](determining-the-type-of-event-to-receive.md)。

2.  [實行實體取用者](implementing-a-physical-consumer.md)。

    管理應用程式與 [*實體取用者*](gloss-p.md) 之間的主要差異在於，使用者會載入和卸載管理應用程式，而 WMI 會載入和卸載實體取用者。 大部分的程式碼撰寫都應該在實體取用者中。

    > [!Note]  
    > 此步驟會先在程式中提供簡單的說明。 就程式碼而言，您應該先實際建立實體取用者。 如此一來，您就可以在開始冗長的程式碼之前，為您的永久事件提供者配置參數和邏輯。 但是，不會先撰寫實體取用者的限制。

     

3.  [建立新的取用者類別來描述實體取用者](creating-a-new-permanent-event-consumer-class.md)。

    就像任何類別一樣，取用者類別會描述永久事件取用者對 WMI 的一般參數。

4.  [建立取用者類別的實例](creating-a-logical-consumer.md)。

    如同其他任何 WMI 類別，如果您想要執行類別，則必須建立取用者類別的實例。 取用者類別的實例也稱為 [*邏輯取用者*](gloss-l.md)。 邏輯取用者代表 WMI 的實體取用者。

5.  [建立事件篩選準則](creating-an-event-filter.md)。

    啟用永久事件取用者的事件查詢稱為「 [*事件篩選準則*](gloss-e.md)」。 單一事件篩選器可以與多個邏輯事件取用者相關聯。 此外，多個事件篩選器可以與單一邏輯事件取用者相關聯。 篩選是 [**\_ \_ >eventfilter**](--eventfilter.md)的實例。

    當永久性事件取用者的查詢失敗時，就會產生 NT 記錄事件。 事件的來源為 WinMgmt，事件識別碼為10，而事件種類為「錯誤」。

6.  將[事件篩選器連結至邏輯取用者](binding-an-event-filter-with-a-logical-consumer.md)。

    藉由將事件篩選器連結至邏輯取用者，您可以指示 WMI 哪些事件篩選器屬於哪個邏輯取用者。 邏輯事件取用者和事件篩選器會透過 [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md)的關聯類別實例來連結。 當收到的事件符合事件篩選器中所述的事件查詢時，WMI 會藉由查看關聯類別實例來尋找相關聯的邏輯事件取用者。 在邏輯事件取用者實例找到之後，WMI 會使用 [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md)類別的實例來尋找並執行與此實例相關聯的實體事件取用者。

7.  [撰寫事件取用者提供者](writing-an-event-consumer-provider.md)。

    事件取用者提供者是 COM 物件，可尋找 WMI 的實體取用者。

 

 




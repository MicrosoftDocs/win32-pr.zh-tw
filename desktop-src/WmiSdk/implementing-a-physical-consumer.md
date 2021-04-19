---
description: 實體取用者是可實 IWbemUnboundObjectSink 介面的 COM 物件。
ms.assetid: 497457dc-61ca-4527-89fd-2af0383de5e9
ms.tgt_platform: multiple
title: 執行實體取用者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af0a9530ed7a98ce19b3b39f2f5a1fe52f3b0631
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107000300"
---
# <a name="implementing-a-physical-consumer"></a>執行實體取用者

實體取用者是可實 [**IWbemUnboundObjectSink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemunboundobjectsink) 介面的 COM 物件。 WMI 會載入您的實體取用者，並透過 **IWbemUnboundObjectSink** 傳遞事件，以回應一或多個事件（如相關聯的邏輯取用者所定義）。 永久取用者具有特殊的安全性需求。 如需詳細資訊，請參閱 [保護 WMI 事件](securing-wmi-events.md)。

下列程式說明如何為永久事件取用者執行實體取用者。

**若要為永久事件取用者執行實體取用者**

1.  建立 COM 物件。

    您必須使用 COM 通訊協定，將實體取用者實作為本機或遠端伺服器。

2.  判斷您是否要支援同步或非同步事件通知。

    使用非同步事件通知時，傳送執行緒與接收執行緒無關。 因此，當 WMI 將通知傳遞給任何已註冊要接收事件的取用者時，WMI 和事件提供者都不會遭到封鎖。 非同步傳遞的缺點是，在提供者產生事件和取用者收到事件之間的時間之間，會發生內容切換。 如需以非同步方式工作的詳細資訊，請參閱 Microsoft Windows 軟體開發套件 (SDK) 的 COM 章節中的 [Com 基本](../com/guide.md) 概念主題。 如需內容切換的詳細資訊，請參閱 Windows SDK 之 Dll、進程和執行緒一節中的 [內容切換](../procthread/context-switches.md) 主題。

    > [!Note]  
    > 由於接收端的回呼可能不會與用戶端所需的驗證層級傳回，因此建議您使用 [半同步] 而非 [非同步通訊]。 如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。

     

    透過同步通知，WMI 會在事件提供者用來將事件傳遞至 WMI 的相同執行緒上傳遞通知。 在此情況下，當事件提供者傳送通知時，WMI 會封鎖事件提供者，直到 WMI 傳遞通知為止。 只有當您的取用者非常快速，而且可以在100微秒內處理事件，您應該考慮支援同步通知。 花費太長時間處理事件的同步取用者可能會嚴重降低將事件傳遞給所有其他取用者的速度。 此外，它們可能會不慎封鎖提供者。 如需詳細資訊，請參閱系結 [事件篩選與邏輯取用者](binding-an-event-filter-with-a-logical-consumer.md)。

3.  執行 [**IWbemUnboundObjectSink：： IndicateToConsumer**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemunboundobjectsink-indicatetoconsumer) 函數。

    WMI 使用 [**IndicateToConsumer**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemunboundobjectsink-indicatetoconsumer) 函式，將必要的指標和事件傳遞給您的實體取用者，以進行同步和非同步通訊。 您的 **IndicateToConsumer** 執行應該包含所有必要的程式碼來回應事件。

    與暫時性事件取用者不同的是，您不需要呼叫 [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator) 介面來聯繫 WMI。 相反地，WMI 會透過事件取用者提供者來尋找您的取用者指標。 如需詳細資訊，請參閱 [撰寫事件取用者提供者](writing-an-event-consumer-provider.md)。

    但是，如果您想要回呼 WMI，請使用 [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator) 和 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) 介面。 連接到 WMI 的傳統方法是在 COM 物件的初始化程式期間。 如需詳細資訊，請參閱 [建立 WMI 應用程式或腳本](creating-a-wmi-application-or-script.md)。

    如果您將實體取用者實作為同進程 COM 伺服器，並與初始化程式分開連接至 WMI，則必須使用 **CLSID \_ WbemAdministrativeLocator** 類別識別碼來存取 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)呼叫中的 [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator)介面。

    下列範例顯示如何使用 **CLSID \_ WbemAdministrativeLocator** 類別識別碼來存取 [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator) 介面。

    ```C++
    IWbemLocator *pLoc = 0;

    DWORD dwRes = CoCreateInstance(CLSID_WbemAdministrativeLocator, 0, 
        CLSCTX_INPROC_SERVER, IID_IWbemLocator, (LPVOID *) &pLoc);
    ```

    

    [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator)介面會取得特定主機電腦上 WMI 的初始命名空間指標。 無法在 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)呼叫中使用 **CLSID \_ WbemAdministrativeLocator** 識別碼會導致「拒絕存取」錯誤。

    在一般情況下，WMI 會將非同步事件一次傳遞給用戶端。 但是，如果用戶端無法在事件抵達時儘快收到非同步事件通知，WMI 就會開始自動將事件批次處理成單一呼叫。 如果反復存取時間是問題的，則自動批次處理會有所説明，這在高輸送量案例中通常是如此。 但是，如果用戶端或網路頻寬是錯誤的，批次處理就不會改善系統效能。

 

 

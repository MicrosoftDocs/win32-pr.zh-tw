---
description: 事件提供者是一種 COM 物件，其提供內建和外來事件通知的 WMI。
ms.assetid: 075bdc65-4ea3-4f91-9823-1d2d0dc13423
ms.tgt_platform: multiple
title: 撰寫事件提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb118d89f214e9fc651c1c9d93abfcfe43f49fc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981514"
---
# <a name="writing-an-event-provider"></a>撰寫事件提供者

事件提供者是一種 COM 物件，其提供內建和外來事件通知的 WMI。 內建事件會報告內部資料變更至 WMI，而外建事件則會報告未由內建事件描述的使用者定義事件。 例如，回應變更、建立或刪除 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) 類別的事件會分類為內部事件。 基於修改、建立或刪除現有 WMI 物件以外的其他專案所產生的事件，是外來事件。 不論支援的類別為何，您都可以用相同的方式來執行所有事件提供者。

下列程式描述如何執行事件提供者。

**若要執行事件提供者**

1.  使用 WMI 設計和註冊您的類別提供者。

    類別提供者會藉由建立 [**\_ \_ Win32Provider**](--win32provider.md)實例和 [**\_ \_ EventProviderRegistration**](--eventproviderregistration.md)類別，向 WMI 註冊。 如需詳細資訊，請參閱 [註冊事件提供者](registering-an-event-provider.md)。

2.  為您的提供者執行 [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) 介面。

    [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit)介面是 WMI 用來載入和初始化所有提供者的通用介面。 如需詳細資訊，請參閱 [初始化提供者](initializing-a-provider.md)。

3.  將 [**IWbemEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovider) 實作為提供者的主要介面。

    [**IWbemEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovider)介面會使用 **ProviderEvents** 方法將事件提供給 WMI。 如需詳細資訊，請參閱 [執行事件提供者的主要介面](implementing-the-primary-interface-for-an-event-provider.md)。

    > [!Note]  
    > 事件提供者必須使用多執行緒模型「兩者」。

     

4.  （選擇性）您也可以執行 [**IWbemEventProviderQuerySink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventproviderquerysink) 介面，以增加事件提供者的效能。

    [**IWbemEventProviderQuerySink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventproviderquerysink)介面允許提供者在將回應傳送至 WMI 之前將查詢優化，而且對於提供多個類型之事件以及需要盡可能執行最多內部優化的提供者而言，最有用。 如需詳細資訊，請參閱 [優化事件提供者](optimizing-an-event-provider.md)。

5.  執行 [**IWbemEventProviderSecurity**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovidersecurity) 介面，將取用者限制為 (sid) 或執行 [**IWbemEventSink：： SetSinkSecurity**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity) 以保護接收器本身的特定安全識別碼。 提供者也可以設定事件類別中的 **安全 \_ 描述項** 屬性，以保護 MOF 程式碼中的個別事件。 如需詳細資訊，請參閱 [保護 WMI 事件](securing-wmi-events.md)。
6.  加入提供者所需的任何其他程式碼。

    設計提供者時，您很可能需要呼叫 WMI 介面。 如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。

    取得用戶端的資訊時，您可能需要存取該用戶端的安全性層級。 如需詳細資訊，請參閱模擬 [用戶端](impersonating-a-client.md)。

7.  以您的新程式碼取代預先存在的提供者。

    如果您沒有預先存在的提供者可進行複製，則不需要執行此步驟。 如需詳細資訊，請參閱 [更新提供者](updating-a-provider.md)。

用戶端應用程式可以透過將 WMI 註冊為事件取用者的方式來要求事件。 如需詳細資訊，請參閱 [接收 WMI 事件](receiving-a-wmi-event.md)。

 

 

---
description: 事件取用者提供者是永久取用者架構的元件，可判斷哪個永久性事件取用者會處理指定的事件。
ms.assetid: c5a0d0ec-99af-4815-9ad2-e59db70e04ce
ms.tgt_platform: multiple
title: 撰寫事件取用者提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 312e0c2ecbf02d8bb0a8f491339d191aadde41a66cd3e3228c3187d5dcf689e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118553095"
---
# <a name="writing-an-event-consumer-provider"></a>撰寫事件取用者提供者

事件取用者提供者是永久取用者架構的元件，可判斷哪個永久性事件取用者會處理指定的事件。 您應建立事件取用者提供者以及永久事件取用者，以正確地從 WMI 路由事件。

事件取用者提供者會連結事件提供者與取用者類別清單。 然後，這些取用者類別的實例會接收來自該提供者的事件。 WMI 會根據 [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md)實例來識別傳遞事件的取用者提供者，這會將取用者提供者 [**\_ \_ Win32Provider**](--win32provider.md)實例與邏輯取用者類別產生關聯。 使用者會在永久訂用帳戶中建立取用者類別的實例。 如果事件發生時，事件提供者未執行，則 WMI 會在需要傳遞事件時啟動提供者。

下列程式描述如何執行事件取用者提供者。

**若要執行事件取用者提供者**

1.  在受控物件格式 (MOF) 中設計取用者類別，並向 WMI 註冊它們。 如需詳細資訊，請參閱 [設計受控物件格式 (MOF) 類別](designing-managed-object-format--mof--classes.md)。

    類別提供者會藉由建立 [**\_ \_ Win32Provider**](--win32provider.md)實例和 [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md)類別，向 WMI 註冊。 如需詳細資訊，請參閱 [註冊事件取用者提供者](registering-an-event-consumer-provider.md)。

2.  為您的提供者執行 [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) 介面。

    WMI 使用 [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) 來載入和初始化提供者。 如需詳細資訊，請參閱 [初始化提供者](initializing-a-provider.md)。

    > [!Note]  
    > 強烈建議您使用多執行緒模型「兩者」的事件取用者。

     

3.  為您的提供者執行 [**IWbemEventConsumerProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventconsumerprovider) 介面。

    [**IWbemEventConsumerProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventconsumerprovider)介面是事件取用者提供者的主要介面。

4.  提供一或多個實體取用者，以接收來自 WMI 的事件訊息。

    實體取用者是代表永久事件取用者的 COM 物件。 所有實體取用者都必須執行 [**IWbemUnboundObjectSink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemunboundobjectsink) 介面。 如需詳細資訊，請參閱實 [作為實體取用者](implementing-a-physical-consumer.md)。

 

 




---
description: 事件提供者必須執行 IWbemEventProvider 介面，才能產生事件通知。
ms.assetid: ae33c9f5-61f7-4488-a281-01d7f9c62c46
ms.tgt_platform: multiple
title: 執行事件提供者的主要介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5621a2c6d0901a7925828149dd5c1480c2b11456
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944715"
---
# <a name="implementing-the-primary-interface-for-an-event-provider"></a>執行事件提供者的主要介面

事件提供者必須執行 [**IWbemEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovider) 介面，才能產生事件通知。 WMI 會呼叫提供者的 [**IWbemEventProvider：:P rovideevents**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventprovider-provideevents) 方法，並將指標傳入接收物件，該物件是 [**IWbemObjectSink**](iwbemobjectsink.md) 介面的執行。 當事件提供者準備好產生通知時，提供者會呼叫 [**IWbemObjectSink：：指示**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) 方法。

事件提供者應該將透過 [**IWbemEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovider) 產生的通知放在事件物件中。 您應該將事件物件實作為 [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject)介面陣列中的專案，該介面是由 [**指示**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate)方法的 *ppObjArray* 參數所代表。 由於 **IWbemClassObjects** 是 COM 物件，因此提供者必須藉由呼叫 [**IWbemObjectSink：： AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) 方法來遞增接收的參考計數。 必須提供許多通知的事件提供者 (例如，400事件) 應該藉由產生新的實例或複製現有的實例，為每個通知建立唯一的事件物件。 WMI 永遠不會在完成 **指出** 呼叫之後保留在事件物件上，而且對於上述和超越 COM 標準的 **AddRef** 沒有特殊需求。

執行事件提供者時，請考慮下列指導方針：

-   請勿在服務用戶端呼叫時進行任何類別變更。
-   請勿發出任何事件相關的呼叫，例如修改事件篩選器的呼叫。
-   處理 Windows 管理服務發出的任何要求（例如 [**CancelQuery**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventproviderquerysink-cancelquery)），然後再 refiring 事件。

    如果您沒有處理要求，則 refiring 事件可能會封鎖事件的接受。

-   絕對不要從提供者中呼叫 [**IWbemObjectSink：： SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) 。

 

 

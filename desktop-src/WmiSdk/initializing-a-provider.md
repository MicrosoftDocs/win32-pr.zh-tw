---
description: 您必須為提供者撰寫程式碼的第一項工作就是初始化程式，其中涵蓋了提供者必須執行的任何工作，讓它能夠從 WMI 傳送和接收資訊、控制受管理物件，以及執行其他工作。
ms.assetid: 3dc145b8-1ce4-4caa-b2ac-31a3681e76f1
ms.tgt_platform: multiple
title: 初始化提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e373cf72d4715919a9d7fc59064d156e80a1f2371c585d698a7c6edff4f22fa5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097278"
---
# <a name="initializing-a-provider"></a>初始化提供者

您必須為提供者撰寫程式碼的第一項工作就是初始化程式，其中涵蓋了提供者必須執行的任何工作，讓它能夠從 WMI 傳送和接收資訊、控制受管理物件，以及執行其他工作。 每一種類型的提供者都有一組不同的工作必須執行，而且有一組隨附的唯一介面。

不過，所有提供者都會透過 [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) 介面初始化，並透過 [**IWBEMPROVIDERINITSINK**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinitsink) 介面通知 WMI 其初始化狀態。

下列程式描述如何初始化提供者。

**初始化提供者**

1.  為您的提供者執行 [**IWbemProviderInit：： Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) 。

    當 WMI 判斷用戶端需要提供者的服務時，WMI 會藉由呼叫 [**IWbemProviderInit：： Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) 方法來載入提供者。

2.  針對您的提供者類型，執行任何獨特的介面。
3.  藉由呼叫 [**IWbemProviderInitSink：： SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus)，告知 WMI 您的提供者已完成初始化。

    [**IWbemProviderInit：： Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize)的所有執行都必須呼叫 [**IWbemProviderInitSink：： SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) ，才能向 WMI 報告初始化狀態。 **SetStatus** 方法可讓 WMI 判斷提供者是否已準備好接收要求，以及提供者已準備好接收的要求類型。

下列程式說明如何報告初始化成功。

**若要報告初始化成功**

-   將 [**SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus)的 *IStatus* 參數設定為 **已 \_ \_ 初始化的 WBEM S**。

    藉由傳回已 **\_ \_ 初始化的 WBEM**，提供者表示已準備好處理來自應用程式、WMI 和其他提供者的要求。 在接收 WBEM \_ \_ 初始化之後，WMI 會對提供者呼叫 [**IWbemProviderInit：： QueryInterface**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) 方法。 此查詢會捕獲提供者主要介面的指標。

下列程式描述如何在初始化期間報告錯誤。

**若要在初始化期間報告錯誤**

-   將 [**SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus)的 *IStatus* 參數設定為 **WBEM \_ E \_ 失敗**。 傳回 WBEM E 的 WMI 視圖提供者 **\_ \_ 無法** 正常運作。

    Wmi 在取得提供者的主要介面指標或初始化失敗之後，就會釋放 [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) 指標。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[開發 WMI 提供者](developing-a-wmi-provider.md)
</dt> <dt>

[設定命名空間安全描述項](setting-namespace-security-descriptors.md)
</dt> <dt>

[保護您的提供者](securing-your-provider.md)
</dt> </dl>

 

 




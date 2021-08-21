---
description: 事件提供者可能會花費大量時間來建立事件。
ms.assetid: 5cf414f0-b3a8-4623-9aaa-08e2a28b40c0
ms.tgt_platform: multiple
title: 優化事件提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 613fa6b054f979d0f7d1a33a87f927df9ef129a280cf7cd1675cbe0cf9818473
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117923405"
---
# <a name="optimizing-an-event-provider"></a>優化事件提供者

事件提供者可能會花費大量時間來建立事件。 如果沒有任何用戶端應用程式使用已建立的事件，則提供者會浪費系統資源。 此外，WMI 會將大量的資源剖析和傳送複雜的查詢傳送給適當的提供者。 若要避免系統資源浪費，並提升事件提供者的效能，您可以執行 [**IWbemEventProviderQuerySink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventproviderquerysink) 介面。 **IWbemEventProviderQuerySink** 會使用 [**NewQuery**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventproviderquerysink-newquery) 和 [**CancelQuery**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventproviderquerysink-cancelquery) 方法，監視用戶端應用程式向 WMI 註冊的查詢。 藉由監視已註冊的用戶端查詢，您的提供者可以判斷是否有任何訊息必須傳送至 WMI。

當用戶端取用者註冊的事件篩選器查詢包含該事件提供者所支援之事件的參考時，WMI 會呼叫事件提供者上的 [**NewQuery**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventproviderquerysink-newquery) 。 因此，負責 **EmailClass** 類別之實例修改事件的事件提供者可以設定為只針對 **寄件者** 產生通知。 當提供者收到要求 **主體** 屬性變更通知的查詢時，提供者可以開始產生這些通知。 在此案例中，您不需要 WMI 來捨棄報告 **收件** 者變更的通知。

同樣地，當用戶端取用者取消註冊的事件篩選器查詢包含事件提供者所支援事件的參考時，WMI 也會在事件提供者上呼叫 [**CancelQuery**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventproviderquerysink-cancelquery) 。 **CancelQuery** 的目的是要讓事件提供者更新應該送出哪些事件的清單。

> [!Note]  
> 如果您的提供者同時支援 [**IWbemEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovider) 和 [**IWbemEventProviderQuerySink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventproviderquerysink)，請確定您的 **IUnknown：： QueryInterface** 方法的實會傳回兩個介面的指標。

 

 

 




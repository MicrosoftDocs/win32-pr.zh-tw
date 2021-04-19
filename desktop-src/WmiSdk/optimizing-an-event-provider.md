---
description: 事件提供者可能會花費大量時間來建立事件。
ms.assetid: 5cf414f0-b3a8-4623-9aaa-08e2a28b40c0
ms.tgt_platform: multiple
title: 優化事件提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70eaabfbbd462b831059b10590d7959bdef05cbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987791"
---
# <a name="optimizing-an-event-provider"></a><span data-ttu-id="3a674-103">優化事件提供者</span><span class="sxs-lookup"><span data-stu-id="3a674-103">Optimizing an Event Provider</span></span>

<span data-ttu-id="3a674-104">事件提供者可能會花費大量時間來建立事件。</span><span class="sxs-lookup"><span data-stu-id="3a674-104">An event provider may devote a great deal of time to creating events.</span></span> <span data-ttu-id="3a674-105">如果沒有任何用戶端應用程式使用已建立的事件，則提供者會浪費系統資源。</span><span class="sxs-lookup"><span data-stu-id="3a674-105">If no client applications use the created events, then the provider is wasting system resources.</span></span> <span data-ttu-id="3a674-106">此外，WMI 會將大量的資源剖析和傳送複雜的查詢傳送給適當的提供者。</span><span class="sxs-lookup"><span data-stu-id="3a674-106">Further, WMI spends a considerable amount of resources parsing and sending complex queries to the appropriate provider.</span></span> <span data-ttu-id="3a674-107">若要避免系統資源浪費，並提升事件提供者的效能，您可以執行 [**IWbemEventProviderQuerySink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventproviderquerysink) 介面。</span><span class="sxs-lookup"><span data-stu-id="3a674-107">To avoid the waste of system resources and to improve the performance of your event provider, you can implement the [**IWbemEventProviderQuerySink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventproviderquerysink) interface.</span></span> <span data-ttu-id="3a674-108">**IWbemEventProviderQuerySink** 會使用 [**NewQuery**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventproviderquerysink-newquery) 和 [**CancelQuery**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventproviderquerysink-cancelquery) 方法，監視用戶端應用程式向 WMI 註冊的查詢。</span><span class="sxs-lookup"><span data-stu-id="3a674-108">**IWbemEventProviderQuerySink** monitors the queries that client applications register with WMI by using the [**NewQuery**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventproviderquerysink-newquery) and [**CancelQuery**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventproviderquerysink-cancelquery) methods.</span></span> <span data-ttu-id="3a674-109">藉由監視已註冊的用戶端查詢，您的提供者可以判斷是否有任何訊息必須傳送至 WMI。</span><span class="sxs-lookup"><span data-stu-id="3a674-109">By monitoring the registered client queries, your provider can determine what if any messages must be sent to WMI.</span></span>

<span data-ttu-id="3a674-110">當用戶端取用者註冊的事件篩選器查詢包含該事件提供者所支援之事件的參考時，WMI 會呼叫事件提供者上的 [**NewQuery**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventproviderquerysink-newquery) 。</span><span class="sxs-lookup"><span data-stu-id="3a674-110">WMI calls [**NewQuery**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventproviderquerysink-newquery) on an event provider when a client consumer registers an event filter query that contains references to events supported by that event provider.</span></span> <span data-ttu-id="3a674-111">因此，負責 **EmailClass** 類別之實例修改事件的事件提供者可以設定為只針對 **寄件者** 產生通知。</span><span class="sxs-lookup"><span data-stu-id="3a674-111">So the event provider responsible for instance modification events for the **EmailClass** class can be set up to generate notifications only for **sender**.</span></span> <span data-ttu-id="3a674-112">當提供者收到要求 **主體** 屬性變更通知的查詢時，提供者可以開始產生這些通知。</span><span class="sxs-lookup"><span data-stu-id="3a674-112">When the provider receives a query requesting notification of changes to the **subject** property, the provider can start generating those notifications.</span></span> <span data-ttu-id="3a674-113">在此案例中，您不需要 WMI 來捨棄報告 **收件** 者變更的通知。</span><span class="sxs-lookup"><span data-stu-id="3a674-113">In this scenario, WMI is not required to discard the notifications that report **recipient** changes only.</span></span>

<span data-ttu-id="3a674-114">同樣地，當用戶端取用者取消註冊的事件篩選器查詢包含事件提供者所支援事件的參考時，WMI 也會在事件提供者上呼叫 [**CancelQuery**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventproviderquerysink-cancelquery) 。</span><span class="sxs-lookup"><span data-stu-id="3a674-114">Similarly, WMI calls [**CancelQuery**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventproviderquerysink-cancelquery) on an event provider when a client consumer deregisters an event filter query that contains references to events supported by the event provider.</span></span> <span data-ttu-id="3a674-115">**CancelQuery** 的目的是要讓事件提供者更新應該送出哪些事件的清單。</span><span class="sxs-lookup"><span data-stu-id="3a674-115">The purpose of **CancelQuery** is for the event provider to update the list of what events should be sent out.</span></span>

> [!Note]  
> <span data-ttu-id="3a674-116">如果您的提供者同時支援 [**IWbemEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovider) 和 [**IWbemEventProviderQuerySink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventproviderquerysink)，請確定您的 **IUnknown：： QueryInterface** 方法的實會傳回兩個介面的指標。</span><span class="sxs-lookup"><span data-stu-id="3a674-116">If your provider supports both [**IWbemEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovider) and [**IWbemEventProviderQuerySink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventproviderquerysink), ensure that your implementation of the **IUnknown::QueryInterface** method returns pointers to both interfaces.</span></span>

 

 

 




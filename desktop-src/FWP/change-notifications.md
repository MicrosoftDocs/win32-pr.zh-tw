---
title: 變更通知
description: 基礎篩選引擎 (BFE) 變更通知遵循發佈/訂閱模式。
ms.assetid: 443f1767-5694-4584-ba0f-229275900774
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c7a3a2069525cc44823ed975fade3b5f100efd8
ms.sourcegitcommit: 60ad94096619da5476f9bbcd4cc231b40b6f5358
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/20/2020
ms.locfileid: "103932951"
---
# <a name="change-notifications"></a><span data-ttu-id="99657-103">變更通知</span><span class="sxs-lookup"><span data-stu-id="99657-103">Change Notifications</span></span>

<span data-ttu-id="99657-104">基礎篩選引擎 (BFE) 變更通知遵循發佈/訂閱模式：為了接收其中一個已發佈的變更通知，應用程式必須訂閱它。</span><span class="sxs-lookup"><span data-stu-id="99657-104">The Base Filtering Engine (BFE) change notifications follow the publish/subscribe pattern: in order to receive one of the published change notifications, an application has to subscribe to it.</span></span>

<span data-ttu-id="99657-105">針對 [**標注**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_callout_subscription0)、 [**篩選**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter_subscription0)、 [**提供**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_subscription0)者、 [**提供者**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_context_subscription0)內容和 [**子層**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_sublayer_subscription0)，已發佈的 BFE 變更通知是新增和移除。</span><span class="sxs-lookup"><span data-stu-id="99657-105">The published BFE change notifications are Add and Remove for [**callouts**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_callout_subscription0), [**filters**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter_subscription0), [**providers**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_subscription0), [**provider contexts**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_context_subscription0), and [**sub-layers**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_sublayer_subscription0).</span></span>

<span data-ttu-id="99657-106">若要訂閱上述其中一個通知，應用程式會呼叫對應的 [**Fwpm \* SubscribeChanges0**](fwp-mgmt-functions.md) 管理函式 (例如 [**FwpmCalloutSubscribeChanges0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutsubscribechanges0)) 。</span><span class="sxs-lookup"><span data-stu-id="99657-106">To subscribe to one of the above notifications, an application calls the corresponding [**Fwpm\*SubscribeChanges0**](fwp-mgmt-functions.md) management function (for example, [**FwpmCalloutSubscribeChanges0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutsubscribechanges0)).</span></span> <span data-ttu-id="99657-107">以引數形式傳遞給 **Fwpm \* SubscribeChanges0** 的回呼函式，會在其所訂閱的變更發生時由 BFE 叫用。</span><span class="sxs-lookup"><span data-stu-id="99657-107">The callback function passed as an argument to **Fwpm\*SubscribeChanges0** is invoked by BFE when the change to which it subscribed occurs.</span></span>

<span data-ttu-id="99657-108">若要取消訂閱上述其中一個通知，應用程式會呼叫對應的 **Fwpm \* UnsubscribeChanges0** 管理功能 (例如 [**FwpmCalloutUnsubscribeChanges0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutunsubscribechanges0)) 。</span><span class="sxs-lookup"><span data-stu-id="99657-108">To unsubscribe to one of the above notifications, an application calls the corresponding **Fwpm\*UnsubscribeChanges0** management function (for example, [**FwpmCalloutUnsubscribeChanges0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutunsubscribechanges0)).</span></span>

<span data-ttu-id="99657-109">為了查看上述其中一個通知的目前訂用帳戶，應用程式會呼叫對應的 [**Fwpm \* SubscriptionsGet0**](fwp-mgmt-functions.md) 管理功能 (例如 [**FwpmCalloutSubscriptionsGet0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutsubscriptionsget0)) 。</span><span class="sxs-lookup"><span data-stu-id="99657-109">To see the current subscriptions for one of the above notifications, an application calls the corresponding [**Fwpm\*SubscriptionsGet0**](fwp-mgmt-functions.md) management function (for example [**FwpmCalloutSubscriptionsGet0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutsubscriptionsget0)).</span></span>

<span data-ttu-id="99657-110">BFE 提供的變更通知如下：</span><span class="sxs-lookup"><span data-stu-id="99657-110">The change notifications offered by the BFE are:</span></span>

-   <span data-ttu-id="99657-111">非同步：觸發通知的函式呼叫可能會在通知分派給所有訂閱者之前傳回。</span><span class="sxs-lookup"><span data-stu-id="99657-111">Asynchronous — The function call that triggered a notification may return before the notification has been dispatched to all subscribers.</span></span>
-   <span data-ttu-id="99657-112">不可靠—不保證會成功傳遞通知。</span><span class="sxs-lookup"><span data-stu-id="99657-112">Unreliable — No guarantee is made that notifications will be successfully delivered.</span></span>

<span data-ttu-id="99657-113">訂閱者不會收到用來訂閱的會話控制碼所做之變更的通知。</span><span class="sxs-lookup"><span data-stu-id="99657-113">Subscribers do not receive notifications for changes made with the session handle they used to subscribe.</span></span> <span data-ttu-id="99657-114">一般來說，「訂閱者」只需要通知其他人所做的變更;他們已經知道自己所做的變更。</span><span class="sxs-lookup"><span data-stu-id="99657-114">Generally, subscribers only need to be informed of the changes made by others; they already know which changes were made by themselves.</span></span>

 

 





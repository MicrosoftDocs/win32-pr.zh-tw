---
title: 變更通知
description: 基礎篩選引擎 (BFE) 變更通知遵循發佈/訂閱模式。
ms.assetid: 443f1767-5694-4584-ba0f-229275900774
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0038dc851cb15414dbc0180f205104725bf069b599632a93ae6e257fe7a1f84
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078498"
---
# <a name="change-notifications"></a>變更通知

基礎篩選引擎 (BFE) 變更通知遵循發佈/訂閱模式：為了接收其中一個已發佈的變更通知，應用程式必須訂閱它。

針對 [**標注**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_callout_subscription0)、 [**篩選**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter_subscription0)、 [**提供**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_subscription0)者、 [**提供者**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_context_subscription0)內容和 [**子層**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_sublayer_subscription0)，已發佈的 BFE 變更通知是新增和移除。

若要訂閱上述其中一個通知，應用程式會呼叫對應的 [**Fwpm \* SubscribeChanges0**](fwp-mgmt-functions.md) 管理函式 (例如 [**FwpmCalloutSubscribeChanges0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutsubscribechanges0)) 。 以引數形式傳遞給 **Fwpm \* SubscribeChanges0** 的回呼函式，會在其所訂閱的變更發生時由 BFE 叫用。

若要取消訂閱上述其中一個通知，應用程式會呼叫對應的 **Fwpm \* UnsubscribeChanges0** 管理功能 (例如 [**FwpmCalloutUnsubscribeChanges0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutunsubscribechanges0)) 。

為了查看上述其中一個通知的目前訂用帳戶，應用程式會呼叫對應的 [**Fwpm \* SubscriptionsGet0**](fwp-mgmt-functions.md) 管理功能 (例如 [**FwpmCalloutSubscriptionsGet0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutsubscriptionsget0)) 。

BFE 提供的變更通知如下：

-   非同步：觸發通知的函式呼叫可能會在通知分派給所有訂閱者之前傳回。
-   不可靠—不保證會成功傳遞通知。

訂閱者不會收到用來訂閱的會話控制碼所做之變更的通知。 一般來說，「訂閱者」只需要通知其他人所做的變更;他們已經知道自己所做的變更。

 

 





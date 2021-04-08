---
title: WinRM 最佳作法
description: 本主題說明使用 WinRM API 各項功能的一些最佳作法。
ms.assetid: FC2CD030-199F-43C2-804E-9827EA2A46D5
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3452f2b8e61fb72b1fd5f99a073b48afb26dafb0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933291"
---
# <a name="winrm-best-practices"></a><span data-ttu-id="94b48-103">WinRM 最佳作法</span><span class="sxs-lookup"><span data-stu-id="94b48-103">WinRM Best Practices</span></span>

<span data-ttu-id="94b48-104">本主題說明使用 WinRM API 各項功能的一些最佳作法。</span><span class="sxs-lookup"><span data-stu-id="94b48-104">This topic explains some of the best practices for using the various features of the WinRM API.</span></span>

## <a name="quotas"></a><span data-ttu-id="94b48-105">配額</span><span class="sxs-lookup"><span data-stu-id="94b48-105">Quotas</span></span>

<span data-ttu-id="94b48-106">當達到配額時，WinRM 服務會將錯誤傳回給用戶端。</span><span class="sxs-lookup"><span data-stu-id="94b48-106">When a quota is hit, the WinRM service returns an error to the client.</span></span> <span data-ttu-id="94b48-107">因此，用戶端邏輯必須根據傳回的錯誤明確地重試作業。</span><span class="sxs-lookup"><span data-stu-id="94b48-107">As a result, the client logic must explicitly retry the operation based on the returned error.</span></span>

## <a name="event-subscriptions"></a><span data-ttu-id="94b48-108">事件訂閱</span><span class="sxs-lookup"><span data-stu-id="94b48-108">Event subscriptions</span></span>

<span data-ttu-id="94b48-109">使用收集器起始的訂用帳戶時，請將遠端電腦的數目限制為500，並將 [Windows 事件收集器](/windows/desktop/WEC/windows-event-collector) 服務 (wecsvc) 隔離在個別的主機進程中。</span><span class="sxs-lookup"><span data-stu-id="94b48-109">When using Collector-initiated subscriptions, limit the number of remote computers to 500 and isolate the [Windows Event Collector](/windows/desktop/WEC/windows-event-collector) service (wecsvc) in a separate host process.</span></span>

<span data-ttu-id="94b48-110">連接錯誤會保留執行緒，直到超時為止。大量的同時連線錯誤可能會導致執行緒集區耗盡，而導致伺服器沒有回應。</span><span class="sxs-lookup"><span data-stu-id="94b48-110">A connection error will hold a thread until it times out. A large number of simultaneous connection errors can cause thread pool exhaustion and render the server unresponsive.</span></span>

 

 
---
title: 2.0 版要求佇列的要求開始
description: .
ms.assetid: 84a744b7-1b0e-4fa7-8015-4840251aa856
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78d618ea3fa38a856eba743d2bf60bfbfec9a633
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933251"
---
# <a name="demand-start-on-version-20-request-queues"></a>2.0 版要求佇列的要求開始

HTTP 伺服器版本 2.0 API 要求佇列的需求啟動功能，可讓控制器應用程式延遲工作者進程具現化，直到第一個要求抵達要求佇列為止。 因此，應用程式可以避免耗用資源，直到需要它們為止。 如需控制器應用程式的詳細資訊，請參閱「 [命名要求佇列](named-request-queue.md) 」主題。

## <a name="asynchronous-demand-start"></a>非同步需求開始

控制器應用程式會使用要求佇列的控制碼來呼叫 [**HttpWaitForDemandStart**](/windows/desktop/api/Http/nf-http-httpwaitfordemandstart) ，以起始需求開始通知。 在非同步完成的情況下，應用程式會在 *pOverlapped* 參數中提供重迭的結構。 以非同步方式呼叫 **HttpWaitForDemandStart** 時，會在第一個要求抵達要求佇列時通知控制器應用程式。 當需求開始通知完成之後，控制器應用程式可以在要求佇列上註冊另一個需求開始通知。

HTTP 伺服器 API 不允許要求佇列有一個以上的同時需求開始通知。 不過，當未完成的要求開始通知完成時，應用程式會再次呼叫 [**HttpWaitForDemandStart**](/windows/desktop/api/Http/nf-http-httpwaitfordemandstart) ，以在要求佇列上啟動多個背景工作進程。 HTTP 不會強制執行要求佇列上操作的要求開始通知數目或背景工作進程數目的限制。 但是，控制器應用程式可以強制執行要求佇列上允許的工作者進程數目。

HTTP 伺服器 API 支援取消非同步 [**HttpWaitForDemandStart**](/windows/desktop/api/Http/nf-http-httpwaitfordemandstart) 呼叫。 應用程式可以使用 [**CancelIoEx**](/windows/desktop/FileIO/cancelioex-func) 搭配 *pOverlapped* 中提供的重迭結構，以取消未完成的 **HttpWaitForDemandStart** 呼叫。

## <a name="synchronous-demand-start"></a>同步需求開始

不建議啟動同步需求，因為應用程式會封鎖，直到要求抵達要求佇列為止。

 

 
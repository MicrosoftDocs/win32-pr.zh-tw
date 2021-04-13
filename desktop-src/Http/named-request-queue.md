---
title: 命名的要求佇列
description: 命名的要求佇列
ms.assetid: d0686a9b-fc3d-4b69-b083-d04b35ce5b50
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4aca045f84fe9f9e4b57365ba8831456f2dc1ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311096"
---
# <a name="named-request-queue"></a>命名的要求佇列

名為「要求佇列」功能的 HTTP Server 2.0 版 API 可讓多個應用程式在不同的進程和使用者帳戶下運作，以存取要求佇列。 要求佇列是依名稱開啟，並使用存取控制清單 (Acl) 來確保應用程式無法存取其他資料。 單一進程會建立要求佇列，並將許可權授與其他進程，以使用要求佇列。 因此，電腦上的其他進程會使用服務要求所需的最低許可權來存取要求佇列。 當應用程式在最低許可權下執行時，HTTP 服務可能會損毀，因為協力廠商程式碼中的弱點會降至最低。

已命名的要求佇列是使用 [**HttpCreateRequestQueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) 函式所建立。 建立要求佇列時，應用程式會在 *pSecurityAttribute* 參數中指定 ACL。 只有在建立要求佇列時才能設定 ACL，可讓工作者進程開啟要求佇列、接收要求和傳送回應。 依預設，除非已在 ACL 中授與許可權，否則不允許處理常式開啟要求佇列。 應用程式不需要系統管理許可權，就能建立要求佇列。

您必須使用 [**HttpCreateRequestQueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue)的 *pName* 參數中所指定的名稱來建立要求佇列，以供其他進程開啟要求佇列。 如果 *pName* 為 **Null**，則會建立未命名的要求佇列，而且沒有其他進程可以開啟它。

## <a name="creator-and-controller-processes"></a>建立者與控制器進程

建立要求佇列時，應用程式可以將它開啟為控制器進程或建立者進程。 控制器和建立者程式都是做為要求佇列的系統管理員，但控制器不會在其上執行 i/o 作業。 應用程式會在建立要求佇列時，藉由在 [**HttpCreateRequestQueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue)的 *Flags* 參數中指定 **HTTP \_ CREATE \_ request \_ queue \_ 旗標 \_ 控制器** 來指出它是控制器進程。 如果未設定 **HTTP \_ CREATE \_ REQUEST \_ QUEUE 旗標 \_ \_ 控制器** 旗標，則應用程式是建立者進程。

下列清單包含控制器進程和建立者進程所執行的工作：

-   建立要求佇列並指定名稱。
-   使用 [**HttpSetRequestQueueProperty**](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty) 函數設定要求佇列。
-   使用 [**HttpQueryRequestQueueProperty**](/windows/desktop/api/Http/nf-http-httpqueryrequestqueueproperty) 函數來查詢要求佇列設定參數。
-   建立 URL 群組，並將它們與要求佇列產生關聯。
-   設定 ACL，以指定允許在要求佇列上接收 i/o 的工作者進程。
-   呼叫 [**HttpWaitForDemandStart**](/windows/desktop/api/Http/nf-http-httpwaitfordemandstart) 來延遲工作者進程的具現化，直到第一個要求抵達要求佇列為止。

除了這些工作以外，建立者進程也可以在要求佇列上執行 i/o 作業。

## <a name="worker-processes"></a>工作者處理序

只有在背景工作進程已被授與 ACL 的存取權時，才能開啟現有的要求佇列。 以最低許可權運作的工作者進程可以開啟要求佇列，並在其上執行 i/o。 應用程式會藉由呼叫 [**HttpCreateRequestQueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue)和在 *旗標* 參數中 **\_ \_ \_ \_ \_ 開啟 \_ 現有的 HTTP CREATE request queue 旗** 標，以及 *pName* 參數中的要求佇列名稱，來開啟現有的要求佇列。

背景工作進程會執行下列功能：

-   在要求佇列上接收要求並傳送回應。
-   依名稱開啟現有的要求佇列。 傳回給背景工作進程之要求佇列的控制碼，無法用來設定要求佇列。
-   查詢要求佇列設定參數。

下圖顯示要求佇列的背景工作進程模型。 要求佇列可以有數個處理 i/o 的工作者進程，以及一個可設定要求佇列的建立者程式。

![要求佇列的背景工作進程模型](images/namedrequestqueue.png)

 

 





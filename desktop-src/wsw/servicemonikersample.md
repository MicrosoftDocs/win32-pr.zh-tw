---
title: ServiceMonikerSample
description: 這個範例會顯示可搭配 TCP 透過 ws-metadataexchange 範例使用的用戶端。 它會利用 WCF 服務的標記。
ms.assetid: cfcff5ee-c0e1-4694-831e-fed0bd0e9855
keywords:
- ServiceMonikerSample Windows Web 服務 API
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3188b41df830f55e77e151c5be9413a986a5dcf5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300776"
---
# <a name="servicemonikersample"></a><span data-ttu-id="a3e14-107">ServiceMonikerSample</span><span class="sxs-lookup"><span data-stu-id="a3e14-107">ServiceMonikerSample</span></span>

<span data-ttu-id="a3e14-108">這個範例會顯示可搭配 TCP 透過 ws-metadataexchange 範例使用的用戶端。</span><span class="sxs-lookup"><span data-stu-id="a3e14-108">This sample shows a client which can be used with the TCP MetadataExchange sample.</span></span> <span data-ttu-id="a3e14-109">它會利用 WCF 服務的標記。</span><span class="sxs-lookup"><span data-stu-id="a3e14-109">It utilizes WCF service moniker.</span></span>

-   [<span data-ttu-id="a3e14-110">PurchaseOrderClient.vbs</span><span class="sxs-lookup"><span data-stu-id="a3e14-110">PurchaseOrderClient.vbs</span></span>](#purchaseorderclientvbs)

## <a name="purchaseorderclientvbs"></a><span data-ttu-id="a3e14-111">PurchaseOrderClient.vbs</span><span class="sxs-lookup"><span data-stu-id="a3e14-111">PurchaseOrderClient.vbs</span></span>


```VB
set obj = GetObject("service:mexAddress='net.tcp://localhost/example/mex', address='net.tcp://localhost/example', contract='IPurchaseOrder', contractNamespace='http://example.org', binding=PurchaseOrderBinding, bindingNamespace='http://example.org'")
for i = 1 to 100
 orderId = obj.Order(i,"Pencil", date)
 Wscript.Echo orderId, date
Next 


```



 

 





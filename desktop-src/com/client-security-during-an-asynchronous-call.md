---
title: 非同步呼叫期間的用戶端安全性
description: 非同步呼叫期間的用戶端安全性
ms.assetid: 26d1f2c2-cb08-49f1-8beb-b99b029f0d8c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bea2f83bf6341704dd0265a37ec2f64b79e9b2a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674824"
---
# <a name="client-security-during-an-asynchronous-call"></a><span data-ttu-id="6f651-103">非同步呼叫期間的用戶端安全性</span><span class="sxs-lookup"><span data-stu-id="6f651-103">Client Security During an Asynchronous Call</span></span>

<span data-ttu-id="6f651-104">MIDL 針對使用標準封送處理的物件所建立的 proxy 管理員會執行 [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) 介面。</span><span class="sxs-lookup"><span data-stu-id="6f651-104">The proxy manager created by MIDL for objects that use standard marshaling implements the [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) interface.</span></span> <span data-ttu-id="6f651-105">用戶端可以藉由在呼叫物件上查詢 **IClientSecurity** ，以及取得或變更安全性設定，來管理封送呼叫的安全性。</span><span class="sxs-lookup"><span data-stu-id="6f651-105">Clients can manage the security of marshaled calls by querying for **IClientSecurity** on the call object and obtaining or changing security settings.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6f651-106">相關主題</span><span class="sxs-lookup"><span data-stu-id="6f651-106">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6f651-107">進行非同步呼叫</span><span class="sxs-lookup"><span data-stu-id="6f651-107">Making an Asynchronous Call</span></span>](making-an-asynchronous-call.md)
</dt> </dl>

 

 





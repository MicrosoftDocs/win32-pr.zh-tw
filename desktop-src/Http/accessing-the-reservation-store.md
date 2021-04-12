---
title: 存取保留存放區
description: HTTP 伺服器 API 會維護電腦上所有使用者的命名空間保留清單。
ms.assetid: 4b1291fc-cc62-4d4f-9150-18cbb1f6e5c0
keywords:
- 存取保留存放區 HTTP
- 保留存放區 HTTP，存取
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a138a0a2385e6338877e5e8623527a64a6eca796
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372202"
---
# <a name="accessing-the-reservation-store"></a><span data-ttu-id="e3e11-105">存取保留存放區</span><span class="sxs-lookup"><span data-stu-id="e3e11-105">Accessing the Reservation Store</span></span>

<span data-ttu-id="e3e11-106">HTTP 伺服器 API 會維護電腦上所有使用者的命名空間保留清單。</span><span class="sxs-lookup"><span data-stu-id="e3e11-106">The HTTP Server API maintains the namespace reservation list for all users on the computer.</span></span> <span data-ttu-id="e3e11-107">保留專案是由 [UrlPrefix](urlprefix-strings.md) 和對應的 ACL 所組成。</span><span class="sxs-lookup"><span data-stu-id="e3e11-107">A reservation entry consists of a [UrlPrefix](urlprefix-strings.md) and corresponding ACL.</span></span> <span data-ttu-id="e3e11-108">存放區中的每個 UrlPrefix 都有一個 ACL，其中會列出所有允許註冊的使用者，以接收命名空間的要求。</span><span class="sxs-lookup"><span data-stu-id="e3e11-108">Each UrlPrefix in the store has an ACL that lists all the users that are permitted to register to receive requests for the namespace.</span></span> <span data-ttu-id="e3e11-109">具有委派許可權的使用者可以將其所擁有之命名空間的子樹委派給其他使用者，或使用設定 Api 來刪除現有的保留。</span><span class="sxs-lookup"><span data-stu-id="e3e11-109">Users with delegation privileges can delegate subtrees of the namespace that they own to other users or delete existing reservations using the configuration APIs.</span></span>

<span data-ttu-id="e3e11-110">為了將保留新增至持續性保留存放區，應用程式會呼叫 [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) 函數，並將設定識別碼參數設定為 **HttpServiceConfigUrlAclInfo** 值。</span><span class="sxs-lookup"><span data-stu-id="e3e11-110">To add a reservation to the persistent reservation store, the application calls the [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) function with the configuration ID parameter set to the **HttpServiceConfigUrlAclInfo** value.</span></span> <span data-ttu-id="e3e11-111">HTTP 伺服器 API 會先驗證命名空間和使用者識別碼的擁有權，再將保留新增至存放區。</span><span class="sxs-lookup"><span data-stu-id="e3e11-111">The HTTP Server API verifies the ownership of the namespace and the user ID before adding a reservation to the store.</span></span>

<span data-ttu-id="e3e11-112">HTTP 伺服器 API 也會提供函數來查詢及刪除 URL 命名空間的服務設定。</span><span class="sxs-lookup"><span data-stu-id="e3e11-112">The HTTP Server API also supplies functions to query and delete the Service configurations for URL namespaces.</span></span> <span data-ttu-id="e3e11-113">呼叫 [**HttpQueryServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpqueryserviceconfiguration) 函式時，會將設定識別碼參數設定為 **HttpServiceConfigUrlAclInfo** 值查詢，並在 URL 命名空間存放區上刪除 [**HttpDeleteServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpdeleteserviceconfiguration) 函數。</span><span class="sxs-lookup"><span data-stu-id="e3e11-113">The [**HttpQueryServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpqueryserviceconfiguration) function called with the configuration ID parameter set to the **HttpServiceConfigUrlAclInfo** value queries, and the [**HttpDeleteServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpdeleteserviceconfiguration) function deletes on the URL namespace store.</span></span>

 

 





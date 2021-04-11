---
description: IUpdateServiceManager2 介面會定義下列方法。
ms.assetid: 50a99e84-0f7c-4cd9-86d1-2247ac0d33dd
title: IUpdateServiceManager2 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f93954ef7fae4e4cc2e6891dbcf3d759500d0059
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112161"
---
# <a name="iupdateservicemanager2-methods"></a><span data-ttu-id="69dc5-103">IUpdateServiceManager2 方法</span><span class="sxs-lookup"><span data-stu-id="69dc5-103">IUpdateServiceManager2 Methods</span></span>

<span data-ttu-id="69dc5-104">[**IUpdateServiceManager2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicemanager2)介面會定義下列方法。</span><span class="sxs-lookup"><span data-stu-id="69dc5-104">The [**IUpdateServiceManager2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicemanager2) interface defines the following methods.</span></span>



| <span data-ttu-id="69dc5-105">方法</span><span class="sxs-lookup"><span data-stu-id="69dc5-105">Method</span></span>                                                                                      | <span data-ttu-id="69dc5-106">描述</span><span class="sxs-lookup"><span data-stu-id="69dc5-106">Description</span></span>                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="69dc5-107">**AddService2**</span><span class="sxs-lookup"><span data-stu-id="69dc5-107">**AddService2**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager2-addservice2)                           | <span data-ttu-id="69dc5-108">使用 WUA 註冊服務，而不需要 ( .cab) 的授權封包檔，並傳回 [**IUpdateServiceRegistration**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicecollection) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="69dc5-108">Registers a service with WUA without requiring an authorization cabinet file (.cab), and returns a pointer to an [**IUpdateServiceRegistration**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicecollection) interface.</span></span> |
| [<span data-ttu-id="69dc5-109">**QueryServiceRegistration**</span><span class="sxs-lookup"><span data-stu-id="69dc5-109">**QueryServiceRegistration**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager2-queryserviceregistration) | <span data-ttu-id="69dc5-110">傳回 [**IUpdateServiceRegistration**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateserviceregistration) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="69dc5-110">Returns a pointer to an [**IUpdateServiceRegistration**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateserviceregistration) interface.</span></span>                                                                                        |



 

<span data-ttu-id="69dc5-111">如需此介面所繼承之成員的相關資訊，請參閱下列介面。</span><span class="sxs-lookup"><span data-stu-id="69dc5-111">For information about the members inherited by this interface, see the following interface.</span></span>

-   [<span data-ttu-id="69dc5-112">**IUpdateServiceManager**</span><span class="sxs-lookup"><span data-stu-id="69dc5-112">**IUpdateServiceManager**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicemanager)

 

 




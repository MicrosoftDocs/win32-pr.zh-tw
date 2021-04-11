---
description: IUpdateSession3 介面會定義下列方法。
ms.assetid: 8015443a-e232-44ab-b53a-e8cc4acd4dd3
title: IUpdateSession3 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bd4126d8bae9e1ba768e574fd9520bdb6cf3d45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112160"
---
# <a name="iupdatesession3-methods"></a><span data-ttu-id="cb5ed-103">IUpdateSession3 方法</span><span class="sxs-lookup"><span data-stu-id="cb5ed-103">IUpdateSession3 Methods</span></span>

<span data-ttu-id="cb5ed-104">[**IUpdateSession3**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession3)介面會定義下列方法。</span><span class="sxs-lookup"><span data-stu-id="cb5ed-104">The [**IUpdateSession3**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession3) interface defines the following methods.</span></span>



| <span data-ttu-id="cb5ed-105">方法</span><span class="sxs-lookup"><span data-stu-id="cb5ed-105">Method</span></span>                                                                           | <span data-ttu-id="cb5ed-106">描述</span><span class="sxs-lookup"><span data-stu-id="cb5ed-106">Description</span></span>                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cb5ed-107">**CreateUpdateServiceManager**</span><span class="sxs-lookup"><span data-stu-id="cb5ed-107">**CreateUpdateServiceManager**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession3-createupdateservicemanager) | <span data-ttu-id="cb5ed-108">傳回會話的 [**IUpdateServiceManager2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicemanager2) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="cb5ed-108">Returns a pointer to an [**IUpdateServiceManager2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicemanager2) interface for the session.</span></span>                                                                                                                                                                                                                |
| [<span data-ttu-id="cb5ed-109">**QueryHistory**</span><span class="sxs-lookup"><span data-stu-id="cb5ed-109">**QueryHistory**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession3-queryhistory)                             | <span data-ttu-id="cb5ed-110">傳回 [**IUpdateHistoryEntryCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentrycollection) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="cb5ed-110">Returns a pointer to an [**IUpdateHistoryEntryCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentrycollection) interface.</span></span> <span data-ttu-id="cb5ed-111">介面包含電腦上相符的事件記錄。</span><span class="sxs-lookup"><span data-stu-id="cb5ed-111">The interface contains matching event records on the computer.</span></span> <span data-ttu-id="cb5ed-112">這會導致 [**QueryHistory**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession3-queryhistory) 方法同步查詢電腦，以取得更新事件的歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="cb5ed-112">This causes the [**QueryHistory**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession3-queryhistory) method to synchronously query the computer for the history of update events.</span></span> |



 

<span data-ttu-id="cb5ed-113">如需此介面所繼承之成員的相關資訊，請參閱下列介面：</span><span class="sxs-lookup"><span data-stu-id="cb5ed-113">For information about the members inherited by this interface, see the following interfaces:</span></span>

-   [<span data-ttu-id="cb5ed-114">**IUpdateSession2**</span><span class="sxs-lookup"><span data-stu-id="cb5ed-114">**IUpdateSession2**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession2)
-   [<span data-ttu-id="cb5ed-115">**IUpdateSession**</span><span class="sxs-lookup"><span data-stu-id="cb5ed-115">**IUpdateSession**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession)

 

 




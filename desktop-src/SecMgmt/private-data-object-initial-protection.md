---
description: 建立私用資料物件時，它會被指派標準保護。
ms.assetid: 7aed8c42-ffa8-43ea-b36e-d894c2ed6bf9
title: 私用資料物件初始保護
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4324a0e147eaa36d2bf42b90b2597a91852183f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106998448"
---
# <a name="private-data-object-initial-protection"></a><span data-ttu-id="e36a9-103">私用資料物件初始保護</span><span class="sxs-lookup"><span data-stu-id="e36a9-103">Private Data Object Initial Protection</span></span>

<span data-ttu-id="e36a9-104">建立私用資料物件時，它會被指派標準保護，如下所示：</span><span class="sxs-lookup"><span data-stu-id="e36a9-104">When a Private Data object is created, it is assigned a standard protection as follows:</span></span>

-   <span data-ttu-id="e36a9-105">全球本機群組會被授與一般的 \_ 執行存取權。</span><span class="sxs-lookup"><span data-stu-id="e36a9-105">The WORLD local group is granted GENERIC\_EXECUTE access.</span></span>
-   <span data-ttu-id="e36a9-106">本機 \_ 系統管理員本機群組被授與 DELETE、generic \_ READ、generic \_ WRITE 和一般 \_ 執行存取權。</span><span class="sxs-lookup"><span data-stu-id="e36a9-106">The LOCAL\_ADMIN local group is granted DELETE, GENERIC\_READ, GENERIC\_WRITE, and GENERIC\_EXECUTE access.</span></span>
-   <span data-ttu-id="e36a9-107">本機 \_ 系統管理員本機群組會被指派為物件的擁有者和主要群組。</span><span class="sxs-lookup"><span data-stu-id="e36a9-107">The LOCAL\_ADMIN local group is assigned as owner and primary group of the object.</span></span>

 

 




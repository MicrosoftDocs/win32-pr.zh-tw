---
description: 建立 TrustedDomain 物件時，它會被指派標準保護。
ms.assetid: cc554630-7be7-4657-90f2-ce5fa81731b2
title: TrustedDomain 物件保護
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acd27a01c1bcfde12fd062f2e8ae7c92a979991a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107001664"
---
# <a name="trusteddomain-object-protection"></a><span data-ttu-id="e144d-103">TrustedDomain 物件保護</span><span class="sxs-lookup"><span data-stu-id="e144d-103">TrustedDomain Object Protection</span></span>

<span data-ttu-id="e144d-104">建立 [**TrustedDomain**](trusteddomain-object.md) 物件時，它會被指派標準保護，如下所示：</span><span class="sxs-lookup"><span data-stu-id="e144d-104">When a [**TrustedDomain**](trusteddomain-object.md) object is created, it is assigned a standard protection as follows:</span></span>

-   <span data-ttu-id="e144d-105">全球本機群組會被授與一般的 \_ 執行存取權。</span><span class="sxs-lookup"><span data-stu-id="e144d-105">The WORLD local group is granted GENERIC\_EXECUTE access.</span></span>
-   <span data-ttu-id="e144d-106">本機 \_ 系統管理員本機群組被授與 DELETE、generic \_ READ、generic \_ WRITE 和一般 \_ 執行存取權。</span><span class="sxs-lookup"><span data-stu-id="e144d-106">The LOCAL\_ADMIN local group is granted DELETE, GENERIC\_READ, GENERIC\_WRITE, and GENERIC\_EXECUTE access.</span></span>
-   <span data-ttu-id="e144d-107">本機 \_ 系統管理員本機群組會被指派為物件的擁有者和主要群組。</span><span class="sxs-lookup"><span data-stu-id="e144d-107">The LOCAL\_ADMIN local group is assigned as owner and primary group of the object.</span></span>

 

 




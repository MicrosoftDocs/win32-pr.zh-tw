---
description: 描述原則物件預設如何受到保護。
ms.assetid: e2d65ebf-5fbd-4e25-9862-a8188abb5492
title: 原則物件保護
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 802fea6ce37a070c8230c3c9993df78a45f439bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690123"
---
# <a name="policy-object-protection"></a><span data-ttu-id="90837-103">原則物件保護</span><span class="sxs-lookup"><span data-stu-id="90837-103">Policy Object Protection</span></span>

<span data-ttu-id="90837-104">[**原則**](policy-object.md)物件預設會使用下列設定來保護：</span><span class="sxs-lookup"><span data-stu-id="90837-104">The [**Policy**](policy-object.md) object is protected by default with the following settings:</span></span>

-   <span data-ttu-id="90837-105">本機群組世界具有一般 \_ 執行存取權。</span><span class="sxs-lookup"><span data-stu-id="90837-105">The local group WORLD has GENERIC\_EXECUTE access.</span></span>
-   <span data-ttu-id="90837-106">已知的識別碼系統會授與原則 \_ 所有 \_ 存取權。</span><span class="sxs-lookup"><span data-stu-id="90837-106">The well-known ID System is granted POLICY\_ALL\_ACCESS.</span></span>
-   <span data-ttu-id="90837-107">本機群組本機系統 \_ 管理員具有一般 \_ 讀取、一般 \_ 寫入和一般 \_ 執行存取權。</span><span class="sxs-lookup"><span data-stu-id="90837-107">The local group LOCAL\_ADMIN has GENERIC\_READ, GENERIC\_WRITE, and GENERIC\_EXECUTE access.</span></span>
-   <span data-ttu-id="90837-108">群組本機 \_ 系統管理員會被指派為此物件的擁有者和主要群組。</span><span class="sxs-lookup"><span data-stu-id="90837-108">The group LOCAL\_ADMIN is assigned as owner and primary group of this object.</span></span>

<span data-ttu-id="90837-109">無法建立或終結 [**原則**](policy-object.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="90837-109">The [**Policy**](policy-object.md) object cannot be created or destroyed.</span></span>

 

 




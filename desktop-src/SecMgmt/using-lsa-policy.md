---
description: 描述如何使用 LSA 原則函數。
ms.assetid: 7f4b963d-3442-4c04-b3d4-f7c8eb1ed15b
title: 使用 LSA 原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 240a59c9009b91d03c1e0904861f815773c95af2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194732"
---
# <a name="using-lsa-policy"></a><span data-ttu-id="b3801-103">使用 LSA 原則</span><span class="sxs-lookup"><span data-stu-id="b3801-103">Using LSA Policy</span></span>

<span data-ttu-id="b3801-104">下列主題描述如何使用 LSA 原則函數。</span><span class="sxs-lookup"><span data-stu-id="b3801-104">The following topics describe how to use the LSA Policy functions.</span></span>

-   <span data-ttu-id="b3801-105">[使用 LSA Unicode 字串](using-lsa-unicode-strings.md) 說明如何將字串轉換為某些 LSA 原則函式所使用的結構格式。</span><span class="sxs-lookup"><span data-stu-id="b3801-105">[Using LSA Unicode Strings](using-lsa-unicode-strings.md) explains how to convert strings into the structure format used by some LSA Policy functions.</span></span>
-   <span data-ttu-id="b3801-106">[開啟原則物件控制碼](opening-a-policy-object-handle.md) 描述如何開啟本機 [**原則**](policy-object.md) 物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="b3801-106">[Opening a Policy Object Handle](opening-a-policy-object-handle.md) describes how to open a handle to the local [**Policy**](policy-object.md) object.</span></span> <span data-ttu-id="b3801-107">許多 LSA 原則函式都需要這個控制碼做為輸入參數。</span><span class="sxs-lookup"><span data-stu-id="b3801-107">This handle is required by many of the LSA Policy functions as an input parameter.</span></span>
-   <span data-ttu-id="b3801-108">[管理原則資訊](managing-policy-information.md) 詳細資料如何設定及查詢本機系統和網域的全域原則資訊。</span><span class="sxs-lookup"><span data-stu-id="b3801-108">[Managing Policy Information](managing-policy-information.md) details how to set and query global policy information for the local system and the domain.</span></span>
-   <span data-ttu-id="b3801-109">[接收原則變更事件](receiving-policy-change-events.md) 描述如何建立和註冊事件，以在原則資訊變更時接收通知。</span><span class="sxs-lookup"><span data-stu-id="b3801-109">[Receiving Policy Change Events](receiving-policy-change-events.md) describes how to create and register an event to receive notifications when policy information changes.</span></span>
-   <span data-ttu-id="b3801-110">[管理帳戶許可權](managing-account-permissions.md) 說明如何建立、刪除和列舉帳戶，以及如何新增和移除這些帳戶的許可權。</span><span class="sxs-lookup"><span data-stu-id="b3801-110">[Managing Account Permissions](managing-account-permissions.md) explains how to create, delete, and enumerate accounts and how to add and remove privileges for those accounts.</span></span>
-   <span data-ttu-id="b3801-111">[管理受信任的網域資訊](managing-trusted-domain-information.md) 說明如何建立、列舉及刪除信任的網域，以及如何設定和取得受信任的網域資訊。</span><span class="sxs-lookup"><span data-stu-id="b3801-111">[Managing Trusted Domain Information](managing-trusted-domain-information.md) describes how to create, enumerate, and delete trusted domains, and how to set and retrieve trusted domain information.</span></span>
-   <span data-ttu-id="b3801-112">[在名稱和 Sid 之間](translating-between-names-and-sids.md) 轉譯會說明如何將 sid 對應到帳戶名稱，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="b3801-112">[Translating Between Names and SIDs](translating-between-names-and-sids.md) explains how to map SIDs to account names and vice versa.</span></span>
-   <span data-ttu-id="b3801-113">[對應 Posix 識別碼](mapping-posix-identifiers.md) 說明如何將 sid 對應至32位 Posix 識別碼。</span><span class="sxs-lookup"><span data-stu-id="b3801-113">[Mapping Posix Identifiers](mapping-posix-identifiers.md) describes how to map SIDs to 32-bit Posix identifiers.</span></span>
-   <span data-ttu-id="b3801-114">[儲存私用資料](storing-private-data.md) 會說明如何儲存和取出私用資料字串。</span><span class="sxs-lookup"><span data-stu-id="b3801-114">[Storing Private Data](storing-private-data.md) explains how to store and retrieve private data strings.</span></span>

<span data-ttu-id="b3801-115">如需如何使用 LSA 登入和驗證使用者的詳細資訊，請參閱 [LSA 驗證](/windows/desktop/SecAuthN/lsa-authentication)。</span><span class="sxs-lookup"><span data-stu-id="b3801-115">For information about how to use the LSA to logon and authenticate users, see [LSA Authentication](/windows/desktop/SecAuthN/lsa-authentication).</span></span>

 

 

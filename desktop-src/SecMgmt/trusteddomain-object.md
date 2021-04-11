---
description: TrustedDomain 物件會儲存與網域之信任關係的相關資訊。
ms.assetid: fab69367-2143-49ef-a1b9-9c1d846fd4e1
title: TrustedDomain 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 837d8a9e56273a87b22b9697ef4e5917d73bcc81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847880"
---
# <a name="trusteddomain-object"></a><span data-ttu-id="2a3de-103">TrustedDomain 物件</span><span class="sxs-lookup"><span data-stu-id="2a3de-103">TrustedDomain Object</span></span>

<span data-ttu-id="2a3de-104">**TrustedDomain** 物件會儲存與網域之信任關係的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2a3de-104">The **TrustedDomain** object stores information about a trust relationship with a domain.</span></span> <span data-ttu-id="2a3de-105">在信任的系統上建立 **TrustedDomain** 物件，以識別受信任網域中可用來提交驗證要求和執行其他作業的帳戶，例如 (SID) 轉譯的名稱和 [*安全性識別*](/windows/desktop/SecGloss/s-gly) 元。</span><span class="sxs-lookup"><span data-stu-id="2a3de-105">A **TrustedDomain** object is created on the trusting system to identify an account within the trusted domain that can be used to submit authentication requests and to perform other operations, such as name and [*security identifier*](/windows/desktop/SecGloss/s-gly) (SID) translations.</span></span>

<span data-ttu-id="2a3de-106">儲存在 **TrustedDomain** 物件中的資訊包括：</span><span class="sxs-lookup"><span data-stu-id="2a3de-106">The information stored in a **TrustedDomain** object includes:</span></span>

-   <span data-ttu-id="2a3de-107">受信任網域的 SID。</span><span class="sxs-lookup"><span data-stu-id="2a3de-107">The SID of the trusted domain.</span></span> <span data-ttu-id="2a3de-108">這項資訊不可修改，而且在所有 **TrustedDomain** 物件中都必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="2a3de-108">This information is not modifiable and must be unique among all **TrustedDomain** objects.</span></span>
-   <span data-ttu-id="2a3de-109">受信任網域的名稱。</span><span class="sxs-lookup"><span data-stu-id="2a3de-109">The name of the trusted domain.</span></span> <span data-ttu-id="2a3de-110">這項資訊不可修改，而且在所有 **TrustedDomain** 物件中都必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="2a3de-110">This information is not modifiable and must be unique among all **TrustedDomain** objects.</span></span>
-   <span data-ttu-id="2a3de-111">信任網域中用來提交驗證要求以及執行名稱和 SID 轉譯的帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="2a3de-111">The name of the account in the trusted domain used to submit authentication requests and to perform name and SID translations.</span></span> <span data-ttu-id="2a3de-112">無法修改這個名稱。</span><span class="sxs-lookup"><span data-stu-id="2a3de-112">This name is not modifiable.</span></span>
-   <span data-ttu-id="2a3de-113">用來提交驗證要求以及執行名稱和 SID 翻譯的密碼。</span><span class="sxs-lookup"><span data-stu-id="2a3de-113">The password used to submit authentication requests and perform name and SID translations.</span></span>

<span data-ttu-id="2a3de-114">如需詳細資訊，請參閱 [TrustedDomain 物件類型](the-trusteddomain-object-type.md)。</span><span class="sxs-lookup"><span data-stu-id="2a3de-114">For more information, see [The TrustedDomain Object Type](the-trusteddomain-object-type.md).</span></span>

 

 

---
title: 無伺服器系結和 RootDSE
description: 可能的話，請勿將伺服器名稱硬式編碼。
ms.assetid: 24cfd8ce-18e6-42f1-8bc5-2c6dee82d133
ms.tgt_platform: multiple
keywords:
- 無伺服器系結和 RootDSE AD
- 無伺服器系結廣告
- RootDSE AD
- Active Directory、Using、Binding、無伺服器系結
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 492a1ed115c4b0d9160305eb54b08c24db86abb8
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104462828"
---
# <a name="serverless-binding-and-rootdse"></a><span data-ttu-id="bde6c-107">無伺服器系結和 RootDSE</span><span class="sxs-lookup"><span data-stu-id="bde6c-107">Serverless Binding and RootDSE</span></span>

<span data-ttu-id="bde6c-108">可能的話，請勿將伺服器名稱硬式編碼。</span><span class="sxs-lookup"><span data-stu-id="bde6c-108">If possible, do not hard-code a server name.</span></span> <span data-ttu-id="bde6c-109">此外，在大部分情況下，系結不應與單一伺服器不必要地系結。</span><span class="sxs-lookup"><span data-stu-id="bde6c-109">Furthermore, under most circumstances, binding should not be unnecessarily tied to a single server.</span></span> <span data-ttu-id="bde6c-110">Active Directory Domain Services 支援無伺服器系結，這表示 Active Directory 可以在預設網域上系結，而不需要指定網域控制站的名稱。</span><span class="sxs-lookup"><span data-stu-id="bde6c-110">Active Directory Domain Services support serverless binding, which means that Active Directory can be bound to on the default domain without specifying the name of a domain controller.</span></span> <span data-ttu-id="bde6c-111">若為一般應用程式，這通常是已登入使用者的網域。</span><span class="sxs-lookup"><span data-stu-id="bde6c-111">For ordinary applications, this is typically the domain of the logged-on user.</span></span> <span data-ttu-id="bde6c-112">針對服務應用程式，這是服務登入帳戶的網域，或是服務所模擬之用戶端的網域。</span><span class="sxs-lookup"><span data-stu-id="bde6c-112">For service applications, this is either the domain of the service logon account or that of the client that the service impersonates.</span></span>

<span data-ttu-id="bde6c-113">在 LDAP 3.0 中，會將 rootDSE 定義為目錄伺服器上目錄資料樹狀結構的根目錄。</span><span class="sxs-lookup"><span data-stu-id="bde6c-113">In LDAP 3.0, rootDSE is defined as the root of the directory data tree on a directory server.</span></span> <span data-ttu-id="bde6c-114">RootDSE 不是任何命名空間的一部分。</span><span class="sxs-lookup"><span data-stu-id="bde6c-114">The rootDSE is not part of any namespace.</span></span> <span data-ttu-id="bde6c-115">RootDSE 的目的是要提供目錄伺服器的相關資料。</span><span class="sxs-lookup"><span data-stu-id="bde6c-115">The purpose of the rootDSE is to provide data about the directory server.</span></span> <span data-ttu-id="bde6c-116">以下是用來系結至 rootDSE 的系結字串。</span><span class="sxs-lookup"><span data-stu-id="bde6c-116">The following is the binding string that is used to bind to rootDSE.</span></span>


```C++
LDAP://<servername>/rootDSE
```



<span data-ttu-id="bde6c-117"><servername>是伺服器的 DNS 名稱。</span><span class="sxs-lookup"><span data-stu-id="bde6c-117">The <servername> is the DNS name of a server.</span></span> <span data-ttu-id="bde6c-118"><servername>是選擇性的，如下列格式所示。</span><span class="sxs-lookup"><span data-stu-id="bde6c-118">The <servername> is optional, as shown in the following format.</span></span>


```C++
LDAP://rootDSE
```



<span data-ttu-id="bde6c-119">在此情況下，將會使用來自網域的預設網域控制站，而呼叫執行緒的安全性內容將會使用。</span><span class="sxs-lookup"><span data-stu-id="bde6c-119">In this case, a default domain controller from the domain that the security context of the calling thread is in will be used.</span></span> <span data-ttu-id="bde6c-120">如果無法在網站記憶體取網域控制站，則會使用可找到的第一個網域控制站。</span><span class="sxs-lookup"><span data-stu-id="bde6c-120">If a domain controller cannot be accessed within the site, the first domain controller that can be found will be used.</span></span>

<span data-ttu-id="bde6c-121">RootDSE 是每個目錄伺服器上已知且可靠的位置，可取得網域、架構和設定容器的辨別名稱，以及伺服器的其他相關資料以及其目錄資料樹狀結構的內容。</span><span class="sxs-lookup"><span data-stu-id="bde6c-121">The rootDSE is a well-known and reliable location on every directory server to get distinguished names of the domain, schema, and configuration containers, and other data about the server and the contents of its directory data tree.</span></span> <span data-ttu-id="bde6c-122">這些屬性在特定伺服器上很少變更。</span><span class="sxs-lookup"><span data-stu-id="bde6c-122">These properties rarely change on a particular server.</span></span> <span data-ttu-id="bde6c-123">應用程式可以在啟動時讀取這些屬性，並在整個會話中使用它們。</span><span class="sxs-lookup"><span data-stu-id="bde6c-123">An application can read these properties at startup and use them throughout the session.</span></span>

<span data-ttu-id="bde6c-124">總而言之，應用程式應該使用無伺服器系結來系結至目前網域上的目錄、使用 rootDSE 取得命名空間的辨別名稱，以及使用該辨別名稱系結至命名空間中的物件。</span><span class="sxs-lookup"><span data-stu-id="bde6c-124">In summary, an application should use serverless binding to bind to the directory on the current domain, use rootDSE to get the distinguished name for a namespace, and use that distinguished name to bind to objects in the namespace.</span></span>

<span data-ttu-id="bde6c-125">如需 rootDSE 所支援之屬性的詳細資訊，請參閱 Active Directory 架構檔中的 [rootdse](/windows/desktop/ADSchema/rootdse) 。</span><span class="sxs-lookup"><span data-stu-id="bde6c-125">For more information about attributes supported by rootDSE, see [RootDSE](/windows/desktop/ADSchema/rootdse) in the Active Directory Schema documentation.</span></span>

<span data-ttu-id="bde6c-126">如需詳細資訊和示範如何使用無伺服器系結和 rootDSE 的程式碼範例，請參閱 [取得網域辨別名稱的範例程式碼](example-code-for-getting-the-distinguished-name-of-the-domain.md)。</span><span class="sxs-lookup"><span data-stu-id="bde6c-126">For more information and a code example that shows how to use serverless binding and rootDSE, see [Example Code for Getting the Distinguished Name of the Domain](example-code-for-getting-the-distinguished-name-of-the-domain.md).</span></span>

 

 
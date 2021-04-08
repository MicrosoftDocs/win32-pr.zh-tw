---
description: 就像系統使用安全描述項來控制安全物件的存取一樣，伺服器也可以使用安全描述項來控制其私用物件的存取權。 如需 Windows 安全性模型的詳細資訊，請參閱存取控制模型。
ms.assetid: d6219438-711a-4eda-a893-9095bce3a07d
title: 以 ACL 為基礎的存取控制
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b477f998b7866c66860b94c3ff1266392f49373
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692768"
---
# <a name="acl-based-access-control"></a><span data-ttu-id="2c9e8-104">以 ACL 為基礎的存取控制</span><span class="sxs-lookup"><span data-stu-id="2c9e8-104">ACL-based Access Control</span></span>

<span data-ttu-id="2c9e8-105">就像系統使用 [安全描述項](security-descriptors.md) 來控制安全物件的存取一樣，伺服器也可以使用安全描述項來控制其私用物件的存取權。</span><span class="sxs-lookup"><span data-stu-id="2c9e8-105">Just as the system uses [security descriptors](security-descriptors.md) to control access to securable objects, a server can use security descriptors to control access to its private objects.</span></span> <span data-ttu-id="2c9e8-106">如需 Windows 安全性模型的詳細資訊，請參閱 [存取控制模型](access-control-model.md)。</span><span class="sxs-lookup"><span data-stu-id="2c9e8-106">For more information about the Windows security model, see [Access Control Model](access-control-model.md).</span></span>

<span data-ttu-id="2c9e8-107">受保護的伺服器可以使用 DACL [建立安全描述項](security-descriptors-for-private-objects.md) ，以 [指定各種受](trustees.md)信任者允許的存取類型。</span><span class="sxs-lookup"><span data-stu-id="2c9e8-107">A protected server can [create a security descriptor](security-descriptors-for-private-objects.md) with a DACL that specifies the types of access allowed for various [trustees](trustees.md).</span></span> <span data-ttu-id="2c9e8-108">在簡單的情況下，伺服器可以建立單一安全描述項來 [控制所有伺服器資料和功能的存取](checking-access-to-private-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="2c9e8-108">In a simple case, the server could create a single security descriptor to [control access to all of the server's data and functionality](checking-access-to-private-objects.md).</span></span> <span data-ttu-id="2c9e8-109">為了提供更精細的保護，伺服器可以為每個私用物件或不同類型的功能建立安全描述項。</span><span class="sxs-lookup"><span data-stu-id="2c9e8-109">For a finer granularity of protection, the server could create security descriptors for each of its private objects, or for different types of functionality.</span></span>

<span data-ttu-id="2c9e8-110">例如，當用戶端要求伺服器在資料庫中建立新的物件時，伺服器可以為新的私用物件建立安全描述項。</span><span class="sxs-lookup"><span data-stu-id="2c9e8-110">For example, when a client asks the server to create a new object in a database, the server could create a security descriptor for the new private object.</span></span> <span data-ttu-id="2c9e8-111">然後，伺服器可以將安全描述項與私用物件儲存在資料庫中。</span><span class="sxs-lookup"><span data-stu-id="2c9e8-111">The server could then store the security descriptor with the private object in the database.</span></span> <span data-ttu-id="2c9e8-112">當用戶端嘗試存取物件時，伺服器會抓取安全描述項來檢查用戶端的存取權限。</span><span class="sxs-lookup"><span data-stu-id="2c9e8-112">When a client tries to access the object, the server retrieves the security descriptor to check the client's access rights.</span></span> <span data-ttu-id="2c9e8-113">請務必注意，安全描述項中沒有任何相關聯的安全性描述項會將它與所保護的物件或功能產生關聯。</span><span class="sxs-lookup"><span data-stu-id="2c9e8-113">It is important to note that there is nothing in a security descriptor that associates it with the object or functionality it is protecting.</span></span> <span data-ttu-id="2c9e8-114">相反地，它是由受保護的伺服器負責維護關聯。</span><span class="sxs-lookup"><span data-stu-id="2c9e8-114">Instead, it is up to the protected server to maintain the association.</span></span>

<span data-ttu-id="2c9e8-115">也可以審核私用物件的存取權。</span><span class="sxs-lookup"><span data-stu-id="2c9e8-115">Access to the private object can also be audited.</span></span> <span data-ttu-id="2c9e8-116">Refer to [Auditing Access to Private Objects](auditing-access-to-private-objects.md) for a description of this.</span><span class="sxs-lookup"><span data-stu-id="2c9e8-116">Refer to [Auditing Access to Private Objects](auditing-access-to-private-objects.md) for a description of this.</span></span>

 

 




---
title: 服務發行的安全性問題
description: 系統會限制建立、修改或刪除連接點物件的能力。 當您發行服務時，請留意這些限制，並加以處理。
ms.assetid: 38e20a47-738d-4951-ad74-249039afeb52
ms.tgt_platform: multiple
keywords:
- 服務發行 AD 的安全性問題
- Active Directory，使用，安全性，服務發行集安全性問題
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fee5be89c490fa938cdc9c7cf3d7d72434a3dffa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671235"
---
# <a name="security-issues-for-service-publication"></a><span data-ttu-id="0570b-106">服務發行的安全性問題</span><span class="sxs-lookup"><span data-stu-id="0570b-106">Security Issues for Service Publication</span></span>

<span data-ttu-id="0570b-107">系統會限制建立、修改或刪除連接點物件的能力。</span><span class="sxs-lookup"><span data-stu-id="0570b-107">The system restricts the ability to create, modify, or delete connection point objects.</span></span> <span data-ttu-id="0570b-108">當您發行服務時，請留意這些限制，並加以處理。</span><span class="sxs-lookup"><span data-stu-id="0570b-108">Be aware of, and handle, these restrictions when you publish a service.</span></span>

<span data-ttu-id="0570b-109">用戶端必須能夠信任在目錄的連接點物件中發行的資料。</span><span class="sxs-lookup"><span data-stu-id="0570b-109">Clients must be able to trust the data published in a connection point object in the directory.</span></span> <span data-ttu-id="0570b-110">基於這個理由，建立連接點物件的許可權通常僅限於具有特殊許可權的使用者，例如網域系統管理員。</span><span class="sxs-lookup"><span data-stu-id="0570b-110">For this reason, permission to create a connection point object is typically restricted to privileged users, such as domain administrators.</span></span> <span data-ttu-id="0570b-111">這可防止未經授權的使用者以偏概全用戶端，方法是為已知的服務建立不正確連接點。</span><span class="sxs-lookup"><span data-stu-id="0570b-111">This prevents unauthorized users from deceiving clients by creating invalid connection points for well-known services.</span></span>

<span data-ttu-id="0570b-112">服務不得以網域系統管理員許可權執行。</span><span class="sxs-lookup"><span data-stu-id="0570b-112">Services must not run with domain administrator privileges.</span></span> <span data-ttu-id="0570b-113">這表示服務通常無法建立自己的連接點。</span><span class="sxs-lookup"><span data-stu-id="0570b-113">This means that a service typically cannot create its own connection point.</span></span> <span data-ttu-id="0570b-114">相反地，您會提供可建立連接點的服務安裝或設定應用程式。</span><span class="sxs-lookup"><span data-stu-id="0570b-114">Instead, you provide a service installation or configuration application that creates the connection point.</span></span> <span data-ttu-id="0570b-115">此安裝程式必須由具有必要許可權的使用者執行。</span><span class="sxs-lookup"><span data-stu-id="0570b-115">This installer must be run by a user with the necessary privileges.</span></span>

<span data-ttu-id="0570b-116">雖然服務通常無法建立其連接點，但是它必須能夠在執行時間更新連接點屬性。</span><span class="sxs-lookup"><span data-stu-id="0570b-116">Although a service cannot typically create its connection point, it must be able to update the connection point properties at run time.</span></span> <span data-ttu-id="0570b-117">連接點屬性包含用戶端用來連接到服務的系結資料。</span><span class="sxs-lookup"><span data-stu-id="0570b-117">The connection point properties contain the binding data used by clients to connect to the service.</span></span> <span data-ttu-id="0570b-118">如果系結資料變更，則服務必須更新連接點;否則，用戶端無法使用服務。</span><span class="sxs-lookup"><span data-stu-id="0570b-118">If the binding data changes, the service must update the connection point; otherwise, clients cannot use the service.</span></span> <span data-ttu-id="0570b-119">這表示安裝程式也必須修改連接點物件上的安全描述項，讓服務在執行時間讀取和寫入適當的屬性。</span><span class="sxs-lookup"><span data-stu-id="0570b-119">This means that the installer must also modify the security descriptor on the connection point object to enable the service to read and write the appropriate properties at run time.</span></span> <span data-ttu-id="0570b-120">如需詳細資訊和程式碼範例，請參閱 [啟用服務帳戶以存取 SCP 屬性](enabling-service-account-to-access-scp-properties.md)。</span><span class="sxs-lookup"><span data-stu-id="0570b-120">For more information and a code example, see [Enabling Service Account to Access SCP Properties](enabling-service-account-to-access-scp-properties.md).</span></span>

<span data-ttu-id="0570b-121">在 LocalSystem 帳戶下執行的服務，可以在目錄中的專屬電腦物件下建立連接點做為子物件。</span><span class="sxs-lookup"><span data-stu-id="0570b-121">A service running under the LocalSystem account can create a connection point as a child object under its own computer object in the directory.</span></span> <span data-ttu-id="0570b-122">這類服務是服務規則的例外狀況，而不是建立自己的連接點。</span><span class="sxs-lookup"><span data-stu-id="0570b-122">Such a service is an exception to the rule of services not creating their own connection points.</span></span> <span data-ttu-id="0570b-123">LocalSystem 服務也有許可權可在其自己的電腦物件下修改連接點物件的內容。</span><span class="sxs-lookup"><span data-stu-id="0570b-123">A LocalSystem service also has permission to modify the properties of connection point objects under its own computer object.</span></span> <span data-ttu-id="0570b-124">請注意，只有在絕對必要時，服務才會在 LocalSystem 帳戶下執行。</span><span class="sxs-lookup"><span data-stu-id="0570b-124">Be aware that a service should run under the LocalSystem account only if absolutely necessary.</span></span> <span data-ttu-id="0570b-125">如需詳細資訊，請參閱 [選取服務登入帳戶的指導方針](guidelines-for-selecting-a-service-logon-account.md)。</span><span class="sxs-lookup"><span data-stu-id="0570b-125">For more information, see [Guidelines for Selecting a Service Logon Account](guidelines-for-selecting-a-service-logon-account.md).</span></span>

<span data-ttu-id="0570b-126">建立連接點物件或任何物件的應用程式，必須具有要在建立物件的容器中建立之物件類別的 create 子許可權。</span><span class="sxs-lookup"><span data-stu-id="0570b-126">The application that creates a connection point object, or any object, must have create child permissions for the object class to be created in the container where the object will be created.</span></span> <span data-ttu-id="0570b-127">若要移除物件，執行作業的處理常式必須具有 [刪除子系] 許可權，才能在持有物件的容器上刪除物件類別，或擁有物件本身的 [刪除] 許可權。</span><span class="sxs-lookup"><span data-stu-id="0570b-127">To remove an object, the process performing the operation must have delete child permissions for the object class to be deleted on the container holding the object, or have delete permissions on the object itself.</span></span> <span data-ttu-id="0570b-128">若要更新連接點，執行作業的進程必須具有要在物件上更新之屬性的寫入權限。</span><span class="sxs-lookup"><span data-stu-id="0570b-128">To update a connection point the process performing the operation must have write-access to the properties to be updated on the object.</span></span>

 

 





---
description: Windows 安全性模型可讓核心交易管理員的呼叫端 (KTM) 控制交易、交易管理員、資源管理員和登錄物件的存取權。
ms.assetid: c9d51d4d-9f07-44d6-a2e1-4a47367cc4ae
title: KTM 安全性與存取權限
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed4e42c9aaf8498ff16ebd1d32f539fef5b54b17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975874"
---
# <a name="ktm-security-and-access-rights"></a><span data-ttu-id="b323a-103">KTM 安全性與存取權限</span><span class="sxs-lookup"><span data-stu-id="b323a-103">KTM Security and Access Rights</span></span>

<span data-ttu-id="b323a-104">Windows 安全性模型可讓核心交易管理員的呼叫端 (KTM) 控制交易、交易管理員、資源管理員和登錄物件的存取權。</span><span class="sxs-lookup"><span data-stu-id="b323a-104">The Windows security model enables callers of Kernel Transaction Manager (KTM) to control access to transaction, transaction manager, resource manager, and enlistment objects.</span></span> <span data-ttu-id="b323a-105">如需詳細資訊，請參閱 [存取控制模型](/windows/desktop/SecAuthZ/access-control-model)。</span><span class="sxs-lookup"><span data-stu-id="b323a-105">For more information, see [Access-Control Model](/windows/desktop/SecAuthZ/access-control-model).</span></span> <span data-ttu-id="b323a-106">對於不在意安全性的應用程式，可以使用寬鬆的存取控制清單來建立交易 (Acl) ，讓任何資源管理員都能在交易上登記。</span><span class="sxs-lookup"><span data-stu-id="b323a-106">For applications that are not concerned about security, transactions can be created with permissive access control lists (ACLs) that allow any resource manager to enlist on a transaction.</span></span>

## <a name="transactions"></a><span data-ttu-id="b323a-107">交易</span><span class="sxs-lookup"><span data-stu-id="b323a-107">Transactions</span></span>

<span data-ttu-id="b323a-108">當用戶端使用 [**OpenTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransaction) 函式時，系統會針對交易對象的安全描述項，檢查要求的存取權限。</span><span class="sxs-lookup"><span data-stu-id="b323a-108">When a client uses the [**OpenTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransaction) function, the system checks the requested access rights against the security descriptor for the transaction object.</span></span>

<span data-ttu-id="b323a-109">交易對象的有效存取權限包括查詢和設定資訊、登錄和各種交易作業，以及 [標準存取權限](/windows/desktop/SecAuthZ/standard-access-rights)的能力。</span><span class="sxs-lookup"><span data-stu-id="b323a-109">The valid access rights for transaction objects include the ability to query and set information, enlist, and various transaction operations, as well as [standard access rights](/windows/desktop/SecAuthZ/standard-access-rights).</span></span> <span data-ttu-id="b323a-110">[**交易存取遮罩**](transaction-access-masks.md) 會列出交易的特定存取權限。</span><span class="sxs-lookup"><span data-stu-id="b323a-110">[**Transaction Access Masks**](transaction-access-masks.md) list the specific access rights for a transaction.</span></span>

<span data-ttu-id="b323a-111">因為交易具有持久狀態，所以與 KTM 互動的 RMs 和 Tm 必須符合其復原的義務。</span><span class="sxs-lookup"><span data-stu-id="b323a-111">Because transactions have a durable state, it is critical that RMs and TMs that interact with the KTM fulfill their obligations with regard to recovery.</span></span> <span data-ttu-id="b323a-112">若無法履行這些義務，可能會導致資源流失（即使系統重新開機也不會清除）。</span><span class="sxs-lookup"><span data-stu-id="b323a-112">Failure to fulfill these obligations can result in resource leaks that are not cleaned up, even by a system reboot.</span></span> <span data-ttu-id="b323a-113">請考慮造成 KTM 取用核心資源的持續性洩漏或惡意程式碼的影響，直到導致系統失敗為止;在產生的重新開機之後，KTM 會讀取其記錄並重新建立所有的持續性物件，可能會導致相同的系統失敗重複發生。</span><span class="sxs-lookup"><span data-stu-id="b323a-113">Consider the effect of a persistent leak or malicious code that caused the KTM to consume kernel resources until it resulted in a system failure; after the resulting reboot, the KTM would read its log and re-create all the persistent objects, potentially causing the same system failure to recur.</span></span> <span data-ttu-id="b323a-114">以配額為基礎的節流將可防止來自 rogue 或行為不良的 RM 的持續性資源。</span><span class="sxs-lookup"><span data-stu-id="b323a-114">Quota-based throttling will prevent persistent resource starvation from a rogue or ill-behaving RM.</span></span> <span data-ttu-id="b323a-115">最後，您必須建立系統管理機制，才能偵測和更正這類持續性流失。</span><span class="sxs-lookup"><span data-stu-id="b323a-115">Finally, administrative mechanisms must be created that allow for the detection and correction of such persistent leaks.</span></span>

## <a name="transaction-managers"></a><span data-ttu-id="b323a-116">交易管理員</span><span class="sxs-lookup"><span data-stu-id="b323a-116">Transaction Managers</span></span>

<span data-ttu-id="b323a-117">當用戶端使用 [**OpenTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransactionmanager) 函式時，系統會根據資源管理員物件的安全描述項來檢查要求的存取權限。</span><span class="sxs-lookup"><span data-stu-id="b323a-117">When a client uses the [**OpenTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransactionmanager) function, the system checks the requested access rights against the security descriptor for the resource manager object.</span></span>

<span data-ttu-id="b323a-118">交易管理員物件的有效存取權限包括查詢和設定資訊、建立 RMs、復原和重新命名作業以及 [標準存取權限](/windows/desktop/SecAuthZ/standard-access-rights)的能力。</span><span class="sxs-lookup"><span data-stu-id="b323a-118">The valid access rights for transaction manager objects include the ability to query and set information, create RMs, and recover and rename operations, as well as [standard access rights](/windows/desktop/SecAuthZ/standard-access-rights).</span></span> <span data-ttu-id="b323a-119">[**交易管理員存取遮罩**](transaction-manager-access-masks.md) 會列出交易管理員的特定存取權限。</span><span class="sxs-lookup"><span data-stu-id="b323a-119">[**Transaction Manager Access Masks**](transaction-manager-access-masks.md) lists the specific access rights for a transaction manager.</span></span>

<span data-ttu-id="b323a-120">資源管理員可以使用嚴格的 Acl 來建立自己的交易管理員物件，以限制哪些資源管理員可以參與使用該交易管理員記錄的交易。</span><span class="sxs-lookup"><span data-stu-id="b323a-120">A resource manager can create its own transaction manager objects with restrictive ACLs to limit which resource managers can participate in transactions that use that transaction manager's log.</span></span>

## <a name="resource-managers"></a><span data-ttu-id="b323a-121">資源管理員</span><span class="sxs-lookup"><span data-stu-id="b323a-121">Resource Managers</span></span>

<span data-ttu-id="b323a-122">當用戶端使用 [**OpenResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-openresourcemanager) 函式時，系統會根據資源管理員物件的安全描述項來檢查要求的存取權限。</span><span class="sxs-lookup"><span data-stu-id="b323a-122">When a client uses the [**OpenResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-openresourcemanager) function, the system checks the requested access rights against the security descriptor for the resource manager object.</span></span>

<span data-ttu-id="b323a-123">資源管理員物件的有效存取權限包括查詢和設定資訊、復原、登錄、註冊作業、傳播和復原作業，以及 [標準存取權限](/windows/desktop/SecAuthZ/standard-access-rights)的能力。</span><span class="sxs-lookup"><span data-stu-id="b323a-123">The valid access rights for resource manager objects include the ability to query and set information, recover, enlist, registration operations, and propagation and recover operations, as well as [standard access rights](/windows/desktop/SecAuthZ/standard-access-rights).</span></span> <span data-ttu-id="b323a-124">[**Resource Manager 存取遮罩**](resource-manager-access-masks.md) 會列出資源管理員的特定存取權限。</span><span class="sxs-lookup"><span data-stu-id="b323a-124">[**Resource Manager Access Masks**](resource-manager-access-masks.md) lists the specific access rights for a resource manager.</span></span>

<span data-ttu-id="b323a-125">如果您想要防止惡意程式碼攔截通知或強制執行特定交易結果，則資源管理員可以建立具有嚴格 Acl 的資源管理員物件。</span><span class="sxs-lookup"><span data-stu-id="b323a-125">A resource manager can create its own resource manager objects with restrictive ACLs if it wishes to prevent malicious code from intercepting notifications or forcing particular transactional outcomes.</span></span>

## <a name="enlistments"></a><span data-ttu-id="b323a-126">登記</span><span class="sxs-lookup"><span data-stu-id="b323a-126">Enlistments</span></span>

<span data-ttu-id="b323a-127">當用戶端使用 [**OpenEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-openenlistment) 函式時，系統會針對登錄物件的安全描述項，檢查要求的存取權限。</span><span class="sxs-lookup"><span data-stu-id="b323a-127">When a client uses the [**OpenEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-openenlistment) function, the system checks the requested access rights against the security descriptor for the enlistment object.</span></span>

<span data-ttu-id="b323a-128">登錄物件的有效存取權限包括查詢和設定資訊、復原作業以及 [標準存取權限](/windows/desktop/SecAuthZ/standard-access-rights)的能力。</span><span class="sxs-lookup"><span data-stu-id="b323a-128">The valid access rights for enlistment objects include the ability to query and set information, recover operations, as well as [standard access rights](/windows/desktop/SecAuthZ/standard-access-rights).</span></span> <span data-ttu-id="b323a-129">[**登記存取遮罩**](enlistment-access-masks.md) 會列出登記的特定存取權限。</span><span class="sxs-lookup"><span data-stu-id="b323a-129">[**Enlistment Access Masks**](enlistment-access-masks.md) lists the specific access rights for an enlistment.</span></span>

 

 

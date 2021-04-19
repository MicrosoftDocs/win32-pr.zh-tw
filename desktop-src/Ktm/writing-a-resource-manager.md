---
description: 如果您要撰寫服務或元件，且需要使用交易式服務，或者，如果您需要監視核心交易的狀態，您需要建立資源管理員 (RM) 。
ms.assetid: 9b62ef58-9897-4573-bda4-8c3ec952b6d2
title: 撰寫 Resource Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2c47f9a0704f6edaea02d752fe39f01fce61c0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106980814"
---
# <a name="writing-a-resource-manager"></a><span data-ttu-id="19afd-103">撰寫 Resource Manager</span><span class="sxs-lookup"><span data-stu-id="19afd-103">Writing a Resource Manager</span></span>

<span data-ttu-id="19afd-104">如果您要撰寫服務或元件，且需要使用交易式服務，或者，如果您需要監視核心交易的狀態，您需要建立資源管理員 (RM) 。</span><span class="sxs-lookup"><span data-stu-id="19afd-104">If you are writing a service or component and need to use transactional services or if you need to monitor the state of a kernel transaction, you need to create a resource manager (RM).</span></span>

<span data-ttu-id="19afd-105">若要撰寫 resource manager，您必須建立多個核心物件。</span><span class="sxs-lookup"><span data-stu-id="19afd-105">To write a resource manager, you must create multiple kernel objects.</span></span> <span data-ttu-id="19afd-106">RM 使用的物件為：</span><span class="sxs-lookup"><span data-stu-id="19afd-106">The objects that an RM uses are:</span></span>

-   <span data-ttu-id="19afd-107">交易管理員 (TM) 物件</span><span class="sxs-lookup"><span data-stu-id="19afd-107">Transaction Manager (TM) objects</span></span>
-   <span data-ttu-id="19afd-108">Resource Manager 物件</span><span class="sxs-lookup"><span data-stu-id="19afd-108">Resource Manager objects</span></span>
-   <span data-ttu-id="19afd-109">登錄物件</span><span class="sxs-lookup"><span data-stu-id="19afd-109">Enlistment objects</span></span>

<span data-ttu-id="19afd-110">首先，建立 TM 物件。</span><span class="sxs-lookup"><span data-stu-id="19afd-110">First, create a TM object.</span></span> <span data-ttu-id="19afd-111">有兩種類型的 Tm：</span><span class="sxs-lookup"><span data-stu-id="19afd-111">There are two types of TMs:</span></span>

-   <span data-ttu-id="19afd-112">Volatile-這些 Tm 沒有記錄檔，無法復原其狀態</span><span class="sxs-lookup"><span data-stu-id="19afd-112">Volatile – these TMs do not have a log and cannot recover their state</span></span>
-   <span data-ttu-id="19afd-113">耐用–這些 Tm 有記錄檔</span><span class="sxs-lookup"><span data-stu-id="19afd-113">Durable – these TMs have a log</span></span>

<span data-ttu-id="19afd-114">若要建立耐用 TM，您必須建立 CLFS 記錄檔並呼叫 [**CreateTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createtransactionmanager) ，或讓 KTM 為您建立。</span><span class="sxs-lookup"><span data-stu-id="19afd-114">To create a durable TM, you must either create a CLFS log and call [**CreateTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createtransactionmanager) or have KTM create it for you.</span></span> <span data-ttu-id="19afd-115">建立耐用 TM 之後，您必須先呼叫 [**RecoverTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-recovertransactionmanager)來復原 tm。</span><span class="sxs-lookup"><span data-stu-id="19afd-115">After a durable TM is created, you must first recover the TM by calling [**RecoverTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-recovertransactionmanager).</span></span> <span data-ttu-id="19afd-116">在 TM 復原之後，就可以使用它。</span><span class="sxs-lookup"><span data-stu-id="19afd-116">After the TM is recovered, it is available for use.</span></span>

<span data-ttu-id="19afd-117">如果您已復原現有的 TM，所有與此 TM 相關聯的 RMs 都會開始接收修復訊息。</span><span class="sxs-lookup"><span data-stu-id="19afd-117">If you recovered an existing TM, all RMs associated with this TM will start receiving recovery messages.</span></span> <span data-ttu-id="19afd-118">如需詳細資訊，請參閱復原 [處理](recovery-processing.md)。</span><span class="sxs-lookup"><span data-stu-id="19afd-118">For more information, see [Recovery Processing](recovery-processing.md).</span></span>

<span data-ttu-id="19afd-119">接下來，您會使用 TM 控制碼呼叫 [**CreateResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createresourcemanager) 來建立資源管理員。</span><span class="sxs-lookup"><span data-stu-id="19afd-119">Next, you create a resource manager by calling [**CreateResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createresourcemanager) with the TM handle.</span></span> <span data-ttu-id="19afd-120">RM 可以是暫時性或耐用的。</span><span class="sxs-lookup"><span data-stu-id="19afd-120">The RM can be volatile or durable.</span></span> <span data-ttu-id="19afd-121">只有持久的 Tm 可以搭配永久性的 RMs 使用。</span><span class="sxs-lookup"><span data-stu-id="19afd-121">Only durable TMs can be used with durable RMs.</span></span>

<span data-ttu-id="19afd-122">以交易方式工作時，您可以藉由呼叫 [**CreateEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment)並指定要接收的通知，在交易中登記。</span><span class="sxs-lookup"><span data-stu-id="19afd-122">When working transactionally, you enlist in the transaction by calling [**CreateEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment)and specifying which notifications to receive.</span></span>

<span data-ttu-id="19afd-123">**注意**  您可以在呼叫 [**CreateEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment) 完成之前，開始接收通知。</span><span class="sxs-lookup"><span data-stu-id="19afd-123">**Note**  You can start receiving notifications before the call to [**CreateEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment) is completed.</span></span>

<span data-ttu-id="19afd-124">當您收到通知時，請 \* 在與處理通知相關聯的任何工作完成時，呼叫適當的「完成」功能。</span><span class="sxs-lookup"><span data-stu-id="19afd-124">When you receive a notification, call the appropriate "Complete\*" function when any work associated with processing the notification is completed.</span></span> <span data-ttu-id="19afd-125">完整的功能包括：</span><span class="sxs-lookup"><span data-stu-id="19afd-125">The complete functions are:</span></span>

-   [<span data-ttu-id="19afd-126">**CommitComplete**</span><span class="sxs-lookup"><span data-stu-id="19afd-126">**CommitComplete**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete)
-   [<span data-ttu-id="19afd-127">**PrepareComplete**</span><span class="sxs-lookup"><span data-stu-id="19afd-127">**PrepareComplete**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete)
-   [<span data-ttu-id="19afd-128">**PreprepareComplete**</span><span class="sxs-lookup"><span data-stu-id="19afd-128">**PreprepareComplete**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-prepreparecomplete)

<span data-ttu-id="19afd-129">如果資源管理員在任何時候無法完成交易的工作，或如果繼續，則會導致應用程式無法復原在交易內完成的工作，您必須呼叫 [**RollbackEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackenlistment)來回複交易。</span><span class="sxs-lookup"><span data-stu-id="19afd-129">If at any time a resource manager is unable to complete the work of the transaction, or if continuing would render your application unable to undo the work done within the transaction, you must roll back the transaction by calling [**RollbackEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackenlistment).</span></span>

 

 




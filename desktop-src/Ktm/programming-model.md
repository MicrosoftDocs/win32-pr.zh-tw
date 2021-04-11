---
description: 應用程式寫入器可以使用核心交易管理員 (KTM) ，來進行次要的原始程式碼變更，以新增交易檔案和登錄作業。
ms.assetid: 356c66dc-5ddd-472f-835c-2e2cb019bcfd
title: 使用交易
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 255e40fb38ca4bfb24acdce717f133dbcf0c76f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849656"
---
# <a name="working-with-transactions"></a><span data-ttu-id="eb7d2-103">使用交易</span><span class="sxs-lookup"><span data-stu-id="eb7d2-103">Working With Transactions</span></span>

<span data-ttu-id="eb7d2-104">應用程式寫入器可以使用核心交易管理員 (KTM) ，來進行次要的原始程式碼變更，以新增交易檔案和登錄作業。</span><span class="sxs-lookup"><span data-stu-id="eb7d2-104">Application writers can make minor source code changes to add transacted file and registry operations using the Kernel Transaction Manager (KTM).</span></span> <span data-ttu-id="eb7d2-105">一般而言，這會牽涉到建立交易，並將控制碼傳遞給交易式資源（例如 [交易式 NTFS](/windows/desktop/FileIO/transactional-ntfs-portal) 和交易登錄）所提供的其他函式。</span><span class="sxs-lookup"><span data-stu-id="eb7d2-105">Typically, this will involve creating a transaction and passing the handle to other functions provided by transactional resources such as [Transactional NTFS](/windows/desktop/FileIO/transactional-ntfs-portal) and the Transacted Registry.</span></span>

<span data-ttu-id="eb7d2-106">KTM 提供的機制可讓您的應用程式參與交易，以及撰寫您自己的交易式資源管理員。</span><span class="sxs-lookup"><span data-stu-id="eb7d2-106">KTM provides mechanisms for your application to participate in transactions as well as to write your own transactional resource manager.</span></span> <span data-ttu-id="eb7d2-107">有一些函數可讓您建立、管理和使用四個核心物件類別：交易、交易管理員、資源管理員和登記。</span><span class="sxs-lookup"><span data-stu-id="eb7d2-107">There are functions that allow you to create, manage, and work with four classes of kernel objects: transactions, transaction managers, resource managers, and enlistments.</span></span> <span data-ttu-id="eb7d2-108">如果您只是使用交易，您只需要使用交易對象，並使用這些函數：</span><span class="sxs-lookup"><span data-stu-id="eb7d2-108">If you are simply using transactions, you only need to work with transaction objects and use these functions:</span></span>

-   [<span data-ttu-id="eb7d2-109">**CreateTransaction**</span><span class="sxs-lookup"><span data-stu-id="eb7d2-109">**CreateTransaction**</span></span>](/windows/desktop/api/KtmW32/nf-ktmw32-createtransaction)
-   [<span data-ttu-id="eb7d2-110">**CommitTransaction**</span><span class="sxs-lookup"><span data-stu-id="eb7d2-110">**CommitTransaction**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction)
-   [<span data-ttu-id="eb7d2-111">**RollbackTransaction**</span><span class="sxs-lookup"><span data-stu-id="eb7d2-111">**RollbackTransaction**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbacktransaction)

<span data-ttu-id="eb7d2-112">絕對不要假設交易處於作用中狀態。</span><span class="sxs-lookup"><span data-stu-id="eb7d2-112">Never assume a transaction is active.</span></span> <span data-ttu-id="eb7d2-113">交易可基於許多原因和隨時復原。</span><span class="sxs-lookup"><span data-stu-id="eb7d2-113">Transactions can be rolled back for many reasons and at any time.</span></span>

<span data-ttu-id="eb7d2-114">Windows 會將以控制碼為基礎的介面公開給系統資源。</span><span class="sxs-lookup"><span data-stu-id="eb7d2-114">Windows exposes a handle-based interface to system resources.</span></span> <span data-ttu-id="eb7d2-115">若要使用作業系統物件，應用程式會先要求物件的控制碼，然後在後續的函式呼叫中使用這個控制碼來存取或修改物件。</span><span class="sxs-lookup"><span data-stu-id="eb7d2-115">To work with an operating system object, the application first requests a handle to the object, and then uses this handle in subsequent function calls to access or modify the object.</span></span> <span data-ttu-id="eb7d2-116">控制碼通常可以不同的模式開啟;指定的模式會影響後續函式呼叫的語法。</span><span class="sxs-lookup"><span data-stu-id="eb7d2-116">A handle can usually be opened in different modes; the mode specified affects the semantics of subsequent function calls.</span></span> <span data-ttu-id="eb7d2-117">例如，透過呼叫 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) 開啟的檔案控制代碼，並將 *dwDesiredAccess* 旗標設為 [ **泛型 \_ READ** ]，就不能在修改檔案的呼叫中使用。</span><span class="sxs-lookup"><span data-stu-id="eb7d2-117">For example, a file handle that is opened by a call to [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) with the *dwDesiredAccess* flag set to **GENERIC\_READ** cannot be used in calls that modify the file.</span></span>

<span data-ttu-id="eb7d2-118">您可以使用 [分散式交易協調器](/previous-versions/windows/desktop/ms684146(v=vs.85)) 的使用者模式資源（例如 SQL 或 MSMQ），以及使用 KTM 的核心模式資源來進行協調。</span><span class="sxs-lookup"><span data-stu-id="eb7d2-118">You can coordinate with [Distributed Transaction Coordinator](/previous-versions/windows/desktop/ms684146(v=vs.85)) user-mode resources such as SQL or MSMQ, and with kernel-mode resources that use the KTM.</span></span> <span data-ttu-id="eb7d2-119">首先，建立 DTC 交易或 [**system.object**](/dotnet/api/system.transactions?view=dotnet-plat-ext-3.1) 物件，然後呼叫 [**IKernelTransaction**](/previous-versions/windows/desktop/aa344210(v=vs.85)) 物件，您可以從中取得 KTM 控制碼。</span><span class="sxs-lookup"><span data-stu-id="eb7d2-119">First, create a DTC transaction, or a [**System.Transactions**](/dotnet/api/system.transactions?view=dotnet-plat-ext-3.1) object, then call the [**IKernelTransaction**](/previous-versions/windows/desktop/aa344210(v=vs.85)) object, from which you can obtain the KTM handle.</span></span> <span data-ttu-id="eb7d2-120">**IKernelTransaction** 物件會建立隸屬于 DTC 交易的 KTM 交易。</span><span class="sxs-lookup"><span data-stu-id="eb7d2-120">The **IKernelTransaction** object creates a KTM transaction that is subordinate to the DTC transaction.</span></span> <span data-ttu-id="eb7d2-121">使用這個控制碼，您可以建立交易對象，但使用 **DTC 或 system.string** 來表示交易結果。</span><span class="sxs-lookup"><span data-stu-id="eb7d2-121">With this handle, you can create your transacted objects, but signal the outcome of the transaction using DTC or **System.Transactions**.</span></span>

 

 

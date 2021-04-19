---
description: 管理交易式 NTFS 中的交易式檔案控制代碼。
ms.assetid: 29879a3f-14b4-462c-a001-46c3c3eb74d1
title: 如何使用交易式 NTFS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43681f0d5b27f0db03d8b6c44564b792fce4b467
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975282"
---
# <a name="how-to-use-transactional-ntfs"></a><span data-ttu-id="e3d34-103">如何使用交易式 NTFS</span><span class="sxs-lookup"><span data-stu-id="e3d34-103">How to Use Transactional NTFS</span></span>

## <a name="transacted-file-handles"></a><span data-ttu-id="e3d34-104">交易的檔案控制代碼</span><span class="sxs-lookup"><span data-stu-id="e3d34-104">Transacted File Handles</span></span>

<span data-ttu-id="e3d34-105">交易式 NTFS (TxF) 將檔案控制代碼系結至交易。</span><span class="sxs-lookup"><span data-stu-id="e3d34-105">Transactional NTFS (TxF) binds a file handle to a transaction.</span></span> <span data-ttu-id="e3d34-106">針對處理 (的作業，例如， [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) 和 [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) 函式) ，實際的 API 函式呼叫不會變更。</span><span class="sxs-lookup"><span data-stu-id="e3d34-106">For operations that work on a handle (for example, the [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) and [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) functions), the actual API function call does not change.</span></span> <span data-ttu-id="e3d34-107">針對採用名稱的檔案作業，這些作業有明確的交易函式。</span><span class="sxs-lookup"><span data-stu-id="e3d34-107">For file operations that take a name, there are explicit transacted functions for these operations.</span></span> <span data-ttu-id="e3d34-108">例如，不是呼叫 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)，而是呼叫 [**CreateFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda)。</span><span class="sxs-lookup"><span data-stu-id="e3d34-108">For example, instead of calling [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea), call [**CreateFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda).</span></span> <span data-ttu-id="e3d34-109">這會建立交易檔案控制代碼，然後用於所有需要控制碼的檔案作業。</span><span class="sxs-lookup"><span data-stu-id="e3d34-109">This creates a transacted file handle, which can then be used for all file operations requiring a handle.</span></span> <span data-ttu-id="e3d34-110">使用此控制碼的所有後續作業都是交易作業。</span><span class="sxs-lookup"><span data-stu-id="e3d34-110">All subsequent operations using this handle are transacted operations.</span></span>

## <a name="basic-txf-usage"></a><span data-ttu-id="e3d34-111">基本 TxF 使用方式</span><span class="sxs-lookup"><span data-stu-id="e3d34-111">Basic TxF Usage</span></span>

<span data-ttu-id="e3d34-112">下列一系列的步驟代表 TxF 的最基本使用方式。</span><span class="sxs-lookup"><span data-stu-id="e3d34-112">The following series of steps represents the most basic usage for TxF.</span></span> <span data-ttu-id="e3d34-113">此外，也支援更複雜的案例，也就是應用程式設計工具的判斷。</span><span class="sxs-lookup"><span data-stu-id="e3d34-113">More complex scenarios are also supported, at the discretion of the application designer.</span></span>

1.  <span data-ttu-id="e3d34-114">藉由呼叫 KTM 函數 [**CreateTransaction**](/windows/desktop/api/ktmw32/nf-ktmw32-createtransaction)或使用 [分散式交易協調器](/previous-versions/windows/desktop/mscs/distributed-transaction-coordinator) (DTC) 的 **IKernelTransaction** 介面，建立交易。</span><span class="sxs-lookup"><span data-stu-id="e3d34-114">Create a transaction by calling the KTM function [**CreateTransaction**](/windows/desktop/api/ktmw32/nf-ktmw32-createtransaction) or by using the **IKernelTransaction** interface of the [Distributed Transaction Coordinator](/previous-versions/windows/desktop/mscs/distributed-transaction-coordinator) (DTC).</span></span>
2.  <span data-ttu-id="e3d34-115">藉由呼叫 [**CreateFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda)取得交易檔案控制代碼 (s) 。</span><span class="sxs-lookup"><span data-stu-id="e3d34-115">Get transacted file handle(s) by calling [**CreateFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda).</span></span>
3.  <span data-ttu-id="e3d34-116">使用交易式檔案控制代碼 (s) ，視需要修改 (s) 的檔案。</span><span class="sxs-lookup"><span data-stu-id="e3d34-116">Modify the file(s) as necessary using the transacted file handle(s).</span></span>
4.  <span data-ttu-id="e3d34-117">關閉與步驟1中建立之交易相關聯的所有交易式檔案控制代碼。</span><span class="sxs-lookup"><span data-stu-id="e3d34-117">Close all transacted file handles associated with the transaction created in step 1.</span></span>
5.  <span data-ttu-id="e3d34-118">藉由呼叫對應的 KTM 或 DTC 函數來認可或中止交易。</span><span class="sxs-lookup"><span data-stu-id="e3d34-118">Commit or abort the transaction by calling the corresponding KTM or DTC function.</span></span>

## <a name="key-points-of-the-txf-programming-model"></a><span data-ttu-id="e3d34-119">TxF 程式設計模型的重點</span><span class="sxs-lookup"><span data-stu-id="e3d34-119">Key Points of the TxF Programming Model</span></span>

<span data-ttu-id="e3d34-120">當您開發 TxF 應用程式時，您可以考慮使用 TxF 程式設計模型的重點：</span><span class="sxs-lookup"><span data-stu-id="e3d34-120">The TxF programming model has the following key points for you to consider when you develop a TxF application:</span></span>

-   <span data-ttu-id="e3d34-121">強烈建議應用程式在認可或回復交易之前，先關閉所有交易的檔案控制代碼。</span><span class="sxs-lookup"><span data-stu-id="e3d34-121">It is highly recommended that an application close all transacted file handles before committing or rolling back a transaction.</span></span> <span data-ttu-id="e3d34-122">當交易結束時，系統會使所有交易控制碼失效。</span><span class="sxs-lookup"><span data-stu-id="e3d34-122">The system invalidates all transacted handles when a transaction ends.</span></span> <span data-ttu-id="e3d34-123">交易結束之後，在交易控制碼上執行的任何作業（除了 close 以外）都會傳回下列錯誤： **錯誤 \_ 控制碼 \_ 不再 \_ \_ 有效**。</span><span class="sxs-lookup"><span data-stu-id="e3d34-123">Any operation, except close, performed on a transacted handle after the transaction ends returns the following error: **ERROR\_HANDLE\_NO\_LONGER\_VALID**.</span></span>
-   <span data-ttu-id="e3d34-124">檔案會被視為儲存裝置。</span><span class="sxs-lookup"><span data-stu-id="e3d34-124">A file is viewed as a unit of storage.</span></span> <span data-ttu-id="e3d34-125">支援部分更新和完整檔案複寫。</span><span class="sxs-lookup"><span data-stu-id="e3d34-125">Partial updates and complete file overwrites are supported.</span></span> <span data-ttu-id="e3d34-126">多個交易無法同時修改同一個檔案。</span><span class="sxs-lookup"><span data-stu-id="e3d34-126">Multiple transactions cannot concurrently modify the same file.</span></span>
-   <span data-ttu-id="e3d34-127">記憶體對應 i/o 是透明的，而且與一般檔案 i/o 一致。</span><span class="sxs-lookup"><span data-stu-id="e3d34-127">Memory mapped I/O is transparent and consistent with the regular file I/O.</span></span> <span data-ttu-id="e3d34-128">應用程式必須在認可交易之前，先排清並關閉已開啟的區段。</span><span class="sxs-lookup"><span data-stu-id="e3d34-128">An application must flush and close an opened section before committing a transaction.</span></span> <span data-ttu-id="e3d34-129">若未這麼做，可能會導致交易內對應檔案的部分變更。</span><span class="sxs-lookup"><span data-stu-id="e3d34-129">Failure to do this can result in partial changes to the mapped file within the transaction.</span></span> <span data-ttu-id="e3d34-130">如果未完成，則復原會失敗。</span><span class="sxs-lookup"><span data-stu-id="e3d34-130">A rollback fails if this is not done.</span></span>

## <a name="common-programming-errors"></a><span data-ttu-id="e3d34-131">常見的程式設計錯誤</span><span class="sxs-lookup"><span data-stu-id="e3d34-131">Common Programming Errors</span></span>

<span data-ttu-id="e3d34-132">開發交易應用程式時，可能會發生下列常見錯誤：</span><span class="sxs-lookup"><span data-stu-id="e3d34-132">The following common errors can occur when developing transacted applications:</span></span>

-   <span data-ttu-id="e3d34-133">在交易完成之後使用檔案控制代碼。</span><span class="sxs-lookup"><span data-stu-id="e3d34-133">Using a file handle after a transaction is completed.</span></span>
-   <span data-ttu-id="e3d34-134">在認可交易之前，無法關閉已刪除之檔案和目錄的控制碼，這會導致無法進行刪除作業。</span><span class="sxs-lookup"><span data-stu-id="e3d34-134">Failing to close handles to deleted files and directories before committing a transaction, which will prevent the delete operations from occurring.</span></span> <span data-ttu-id="e3d34-135">執行認可之前，必須先發生這個事件，才能將刪除作業視為交易的一部分。</span><span class="sxs-lookup"><span data-stu-id="e3d34-135">This event must occur before performing the commit for the delete operation to be considered part of the transaction.</span></span> <span data-ttu-id="e3d34-136">這是因為系統不會實際刪除檔案，直到其最後一個控制碼關閉為止，即使作業不是交易式，也是 Windows 檔案 i/o 子系統的一部分。</span><span class="sxs-lookup"><span data-stu-id="e3d34-136">This is because the system does not actually delete a file until the last handle to it is closed, even when the operation is not transacted, as part of the Windows file I/O subsystem.</span></span>
-   <span data-ttu-id="e3d34-137">無法考慮系統起始的交易復原，可能會在任何時間發生;例如，如果系統資源已用盡，則會回復交易。</span><span class="sxs-lookup"><span data-stu-id="e3d34-137">Failing to account for system-initiated transaction rollbacks, which may happen at any time; for example, a transaction is rolled back if the system resources are exhausted.</span></span>

 

 

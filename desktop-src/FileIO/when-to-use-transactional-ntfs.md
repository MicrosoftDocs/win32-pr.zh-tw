---
description: 使用交易式 NTFS 來維護資料完整性。
ms.assetid: 886d6075-57e8-47db-aec5-77660d0a53f9
title: 使用交易式 NTFS 的時機
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28c0a134a8cb5824337022fedf14fe3db3c6f76c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106989472"
---
# <a name="when-to-use-transactional-ntfs"></a><span data-ttu-id="33c6a-103">使用交易式 NTFS 的時機</span><span class="sxs-lookup"><span data-stu-id="33c6a-103">When to Use Transactional NTFS</span></span>

<span data-ttu-id="33c6a-104">應用程式可以使用交易式 NTFS (TxF) 在非預期的錯誤情況期間，保留磁片上資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="33c6a-104">An application can use Transactional NTFS (TxF) to preserve the integrity of data on disk during unexpected error conditions.</span></span> <span data-ttu-id="33c6a-105">一般情況下，應用程式應該考慮使用 TxF （如果應用程式正在清除檔案，以及使用其他技術來維持資料完整性）。</span><span class="sxs-lookup"><span data-stu-id="33c6a-105">In general, an application should consider using TxF if the application is flushing files and using other techniques to maintain data integrity.</span></span> <span data-ttu-id="33c6a-106">TxF 可以更妥善地執行並簡化應用程式的錯誤處理常式代碼，同時改善錯誤的復原和可靠性。</span><span class="sxs-lookup"><span data-stu-id="33c6a-106">TxF can perform better and simplify the application's error handling code while improving error recovery and reliability.</span></span> <span data-ttu-id="33c6a-107">本主題中的下列各節提供使用 TxF 的案例範例。</span><span class="sxs-lookup"><span data-stu-id="33c6a-107">The following sections in this topic provide examples of scenarios for you to use TxF.</span></span>

## <a name="updating-a-file"></a><span data-ttu-id="33c6a-108">更新檔案</span><span class="sxs-lookup"><span data-stu-id="33c6a-108">Updating a File</span></span>

<span data-ttu-id="33c6a-109">檔案的更新是常見且一般簡單的操作。</span><span class="sxs-lookup"><span data-stu-id="33c6a-109">The updating of a file is a common and typically simple operation.</span></span> <span data-ttu-id="33c6a-110">但是，如果在應用程式更新磁片上的資訊時，系統或應用程式失敗，結果可能會造成嚴重的後果，因為使用者資料可能會因已部分完成的檔案更新作業而損毀。</span><span class="sxs-lookup"><span data-stu-id="33c6a-110">However, if the system or application fails while an application is updating information on a disk, the result can be catastrophic, because the user data can be corrupted by a file update operation that is partially completed.</span></span> <span data-ttu-id="33c6a-111">健全的應用程式通常會執行一系列的檔案複製和檔案重新命名，以確保在系統失敗時資料不會損毀。</span><span class="sxs-lookup"><span data-stu-id="33c6a-111">Robust applications often perform complex sequences of file copies and file renames to ensure that data is not corrupted if a system fails.</span></span>

<span data-ttu-id="33c6a-112">TxF 讓應用程式可以輕鬆地保護檔案更新作業，避免系統或應用程式失敗。</span><span class="sxs-lookup"><span data-stu-id="33c6a-112">TxF makes it simple for an application to protect file update operations from system or application failure.</span></span> <span data-ttu-id="33c6a-113">為了安全地更新檔案，應用程式會以交易模式開啟檔案、進行必要的更新，然後認可交易。</span><span class="sxs-lookup"><span data-stu-id="33c6a-113">To update a file safely, the application opens the file in transacted mode, makes the necessary updates, and then commits the transaction.</span></span> <span data-ttu-id="33c6a-114">如果在檔案更新期間，系統或應用程式失敗，則 TxF 會自動將檔案還原至檔案更新開始之前的狀態，這樣可避免檔案損毀。</span><span class="sxs-lookup"><span data-stu-id="33c6a-114">If the system or application fails during the file update, then TxF automatically restores the file to the state that it had before the file update began, which avoids file corruption.</span></span>

## <a name="multi-file-updates"></a><span data-ttu-id="33c6a-115">多檔案更新</span><span class="sxs-lookup"><span data-stu-id="33c6a-115">Multi-File Updates</span></span>

<span data-ttu-id="33c6a-116">當單一邏輯作業影響多個檔案時，TxF 更為重要。</span><span class="sxs-lookup"><span data-stu-id="33c6a-116">TxF is even more important when a single logical operation affects multiple files.</span></span> <span data-ttu-id="33c6a-117">例如，如果您想要使用工具來重新命名網站上的其中一個 HTML 或 ASP 頁面，設計完善的工具也會修正所有連結，以使用新的檔案名。</span><span class="sxs-lookup"><span data-stu-id="33c6a-117">For example, if you want to use a tool to rename one of the HTML or ASP pages on a website, a well-designed tool would also fix all links to use the new file name.</span></span> <span data-ttu-id="33c6a-118">不過，在此作業期間發生失敗時，網站會處於不一致的狀態，而某些連結仍會參考舊的檔案名。</span><span class="sxs-lookup"><span data-stu-id="33c6a-118">However, a failure during this operation leaves the website in an inconsistent state, with some of the links still referring to the old file name.</span></span> <span data-ttu-id="33c6a-119">藉由讓檔案重新命名作業和連結修正作業成為單一交易，TxF 可確保檔案重新命名和連結修正成功或失敗，以做為單一作業。</span><span class="sxs-lookup"><span data-stu-id="33c6a-119">By making the file rename operation and the link fixing operation a single transaction, TxF ensures that the file rename and link fix succeed or fail as a single operation.</span></span>

## <a name="consistent-concurrent-updates"></a><span data-ttu-id="33c6a-120">一致的並行更新</span><span class="sxs-lookup"><span data-stu-id="33c6a-120">Consistent Concurrent Updates</span></span>

<span data-ttu-id="33c6a-121">TxF 會隔離並行交易。</span><span class="sxs-lookup"><span data-stu-id="33c6a-121">TxF isolates concurrent transactions.</span></span> <span data-ttu-id="33c6a-122">如果應用程式在另一個應用程式開啟交易式更新的相同檔案時，開啟交易式讀取的檔案，則 TxF 會將這兩個交易的效果彼此隔離。</span><span class="sxs-lookup"><span data-stu-id="33c6a-122">If an application opens a file for a transactional read while another application has the same file open for a transactional update, TxF isolates the effects of the two transactions from one another.</span></span> <span data-ttu-id="33c6a-123">換句話說，交易式讀取器一律會查看單一的一致版本檔案，即使該檔案正在由另一個交易進行更新。</span><span class="sxs-lookup"><span data-stu-id="33c6a-123">In other words, the transactional reader always views a single, consistent version of the file, even while that file is in the process of being updated by another transaction.</span></span>

<span data-ttu-id="33c6a-124">應用程式可以使用這種功能，讓客戶在其他客戶進行更新時查看檔案。</span><span class="sxs-lookup"><span data-stu-id="33c6a-124">An application can use this functionality to allow customers to view files while other customers make updates.</span></span> <span data-ttu-id="33c6a-125">例如，交易式 web 伺服器可以提供單一且一致的檔案視圖，而另一個工具會同時更新這些檔案。</span><span class="sxs-lookup"><span data-stu-id="33c6a-125">For example, a transactional web server can provide a single, consistent view of files while another tool concurrently updates those files.</span></span>

> [!Note]  
> <span data-ttu-id="33c6a-126">在不同的交易中，TxF 不支援多個寫入器的並行更新。</span><span class="sxs-lookup"><span data-stu-id="33c6a-126">TxF does not support concurrent updates by multiple writers in different transactions.</span></span> <span data-ttu-id="33c6a-127">TxF 僅支援具有多個並行和一致讀取器的單一寫入器。</span><span class="sxs-lookup"><span data-stu-id="33c6a-127">TxF supports only a single writer with multiple concurrent and consistent readers.</span></span>

 

## <a name="coordinating-with-other-transacted-resource-managers"></a><span data-ttu-id="33c6a-128">與其他交易的資源管理員協調</span><span class="sxs-lookup"><span data-stu-id="33c6a-128">Coordinating With Other Transacted Resource Managers</span></span>

<span data-ttu-id="33c6a-129">交易式檔案系統所使用的交易也可以搭配交易登錄使用。</span><span class="sxs-lookup"><span data-stu-id="33c6a-129">Transactions used with transacted file systems may also be used with the transacted registry.</span></span> <span data-ttu-id="33c6a-130">檔案和登錄的更新會與單一交易協調。</span><span class="sxs-lookup"><span data-stu-id="33c6a-130">Updates to the file and the registry are coordinated with a single transaction.</span></span>

<span data-ttu-id="33c6a-131">藉由使用 [分散式交易協調器](/previous-versions/windows/desktop/mscs/distributed-transaction-coordinator) (DTC) 交易或系統交易，對 SQL、MSMQ 和其他交易式資源所做的更新，可以與交易檔案更新協調。</span><span class="sxs-lookup"><span data-stu-id="33c6a-131">By using [Distributed Transaction Coordinator](/previous-versions/windows/desktop/mscs/distributed-transaction-coordinator) (DTC) transactions or System.Transactions, updates made to SQL, MSMQ, and other transactional resources can be coordinated with transacted file updates.</span></span> <span data-ttu-id="33c6a-132">如需詳細資訊，請參閱 DTC 的 [IKernelTransaction](/previous-versions/windows/desktop/aa344210(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="33c6a-132">For more information, see DTC's [IKernelTransaction](/previous-versions/windows/desktop/aa344210(v=vs.85)).</span></span>

## <a name="unsupported-scenarios"></a><span data-ttu-id="33c6a-133">不支援的案例</span><span class="sxs-lookup"><span data-stu-id="33c6a-133">Unsupported Scenarios</span></span>

<span data-ttu-id="33c6a-134">TxF 不支援下列交易案例：</span><span class="sxs-lookup"><span data-stu-id="33c6a-134">TxF does not support the following transaction scenarios:</span></span>

-   <span data-ttu-id="33c6a-135">網路磁片區上的交易，例如檔案共用。</span><span class="sxs-lookup"><span data-stu-id="33c6a-135">Transactions on network volumes, for example on file shares.</span></span> <span data-ttu-id="33c6a-136">CIFS/SMB 通訊協定不支援 TxF。</span><span class="sxs-lookup"><span data-stu-id="33c6a-136">TxF is not supported by the CIFS/SMB protocols.</span></span>
-   <span data-ttu-id="33c6a-137">NTFS 以外的任何檔案系統上的交易。</span><span class="sxs-lookup"><span data-stu-id="33c6a-137">Transactions on any file system other than NTFS.</span></span>
-   <span data-ttu-id="33c6a-138">針對由用戶端快取快取的檔案進行的交易作業。</span><span class="sxs-lookup"><span data-stu-id="33c6a-138">Transacted operations against files cached by client-side caching.</span></span>
-   <span data-ttu-id="33c6a-139">使用物件識別碼存取檔案。</span><span class="sxs-lookup"><span data-stu-id="33c6a-139">File access using object IDs.</span></span>
-   <span data-ttu-id="33c6a-140">任何共用的寫入器案例。</span><span class="sxs-lookup"><span data-stu-id="33c6a-140">Any shared writer scenario.</span></span>
-   <span data-ttu-id="33c6a-141">任何情況下，檔案會在一段時間內開啟一段很長的時間)  (天或數周。</span><span class="sxs-lookup"><span data-stu-id="33c6a-141">Any situation where a file is opened for an extended period of time (days or weeks).</span></span>

 

 

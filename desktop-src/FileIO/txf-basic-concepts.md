---
description: 描述交易式 NTFS 中的讀取認可一致性、讀取認可隔離和交易鎖定概念。
ms.assetid: 18579c4a-a832-4c89-8fb1-cd2542e4375e
title: 基本 TxF 概念
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7f2f5d0885795f20a8dfb5e0963468ff04bb8e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320104"
---
# <a name="basic-txf-concepts"></a><span data-ttu-id="0924a-103">基本 TxF 概念</span><span class="sxs-lookup"><span data-stu-id="0924a-103">Basic TxF Concepts</span></span>

## <a name="read-isolation"></a><span data-ttu-id="0924a-104">讀取隔離</span><span class="sxs-lookup"><span data-stu-id="0924a-104">Read Isolation</span></span>

<span data-ttu-id="0924a-105">交易式 NTFS (TxF) 提供讀取認可的一致性。</span><span class="sxs-lookup"><span data-stu-id="0924a-105">Transactional NTFS (TxF) provides read-committed consistency.</span></span>

<span data-ttu-id="0924a-106">[*交易寫入器*](glossary.md)指的是使用不屬於泛型讀取權限的任何許可權開啟的交易檔案控制代碼，但屬於一般寫入存取權的一部分。</span><span class="sxs-lookup"><span data-stu-id="0924a-106">A [*transacted writer*](glossary.md) refers to a transacted file handle opened with any permission that is not part of generic read access but is part of generic write access.</span></span> <span data-ttu-id="0924a-107">交易 *寫入器* 會查看檔案的最新版本，其中包含相同交易的所有變更。</span><span class="sxs-lookup"><span data-stu-id="0924a-107">A *transacted writer* views the most recent version of a file that includes all of the changes by the same transaction.</span></span> <span data-ttu-id="0924a-108">每個檔案只能有一個交易寫入器。</span><span class="sxs-lookup"><span data-stu-id="0924a-108">There can be only one transacted writer per file.</span></span> <span data-ttu-id="0924a-109">交易寫入器一律會封鎖非交易寫入器，即使以共用寫入權限開啟檔案也是一樣。</span><span class="sxs-lookup"><span data-stu-id="0924a-109">Non-transacted writers are always blocked by a transacted writer, even if the file is opened with shared-write permissions.</span></span>

<span data-ttu-id="0924a-110">[*交易式讀取器*](glossary.md)指的是交易式檔案控制代碼，該控制碼是以泛型讀取權限的一部分開啟，但不屬於一般寫入存取權。</span><span class="sxs-lookup"><span data-stu-id="0924a-110">A [*transacted reader*](glossary.md) refers to a transacted file handle opened with any permission that is a part of generic read access but is not part of generic write access.</span></span> <span data-ttu-id="0924a-111">*交易式讀取器* 會查看檔案控制代碼開啟時所存在之檔案的認可版本。</span><span class="sxs-lookup"><span data-stu-id="0924a-111">A *transacted reader* views a committed version of the file that existed at the time the file handle was opened.</span></span> <span data-ttu-id="0924a-112">交易讀取器會與交易寫入器的效果隔離。</span><span class="sxs-lookup"><span data-stu-id="0924a-112">The transacted reader is isolated from the effects of transacted writers.</span></span> <span data-ttu-id="0924a-113">這只會在檔案控制代碼的存留期內提供檔案的一致觀點，並封鎖非交易寫入器。</span><span class="sxs-lookup"><span data-stu-id="0924a-113">This provides a consistent view of the file only for the life of the file handle and blocks non-transacted writers.</span></span>

> [!Note]  
> <span data-ttu-id="0924a-114">使用 [**CreateFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda) 函式開啟控制碼以進行修改時，所有後續開啟該交易中的檔案（不論是唯讀或未將它轉換為交易寫入器），以供隔離和其他交易式語義之用。</span><span class="sxs-lookup"><span data-stu-id="0924a-114">When a handle has been opened for modification with the [**CreateFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda) function, all subsequent opens of the file within that transaction whether read-only or not are converted by the system to be a transacted writer for the purposes of isolation and other transactional semantics.</span></span> <span data-ttu-id="0924a-115">這表示，在開啟控制碼以進行唯讀存取時，控制碼不會在交易開始之前收到檔案的視圖;它會接收檔案的使用中交易視圖。</span><span class="sxs-lookup"><span data-stu-id="0924a-115">This means that subsequently, when a handle is opened for read-only access, the handle does not receive a view of the file prior to the start of the transaction; it receives the active transaction view of the file.</span></span>

 

<span data-ttu-id="0924a-116">非交易式檔案控制代碼在交易認可之前，不會看到在交易內進行的任何變更。</span><span class="sxs-lookup"><span data-stu-id="0924a-116">A non-transacted file handle does not see any changes made within a transaction until the transaction is committed.</span></span> <span data-ttu-id="0924a-117">非交易式檔案控制代碼會收到類似于交易讀取器的隔離式查看，但不同于交易讀取器，它會在交易寫入器認可交易時，接收檔案更新。</span><span class="sxs-lookup"><span data-stu-id="0924a-117">The non-transacted file handle receives an isolated view that is similar to a transacted reader, but unlike a transacted reader, it receives the file update when a transacted writer commits the transaction.</span></span>

## <a name="isolation-levels"></a><span data-ttu-id="0924a-118">隔離等級</span><span class="sxs-lookup"><span data-stu-id="0924a-118">Isolation Levels</span></span>

<span data-ttu-id="0924a-119">TxF 提供讀取認可隔離。</span><span class="sxs-lookup"><span data-stu-id="0924a-119">TxF provides read-committed isolation.</span></span> <span data-ttu-id="0924a-120">這表示在交易外部看不到檔案更新。</span><span class="sxs-lookup"><span data-stu-id="0924a-120">This means that file updates are not seen outside the transaction.</span></span> <span data-ttu-id="0924a-121">此外，如果在讀取交易內的檔案時多次開啟檔案，您可能會在每次後續開啟時看到不同的結果。</span><span class="sxs-lookup"><span data-stu-id="0924a-121">In addition, if a file is opened more than once while reading files within the transaction, you may see different results with each subsequent opening.</span></span> <span data-ttu-id="0924a-122">當您第一次存取這些檔案時，可能無法 (使用這些檔案，因為它們已) 刪除，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="0924a-122">Files that were available the first time you accessed them may not be available (because they were deleted), or vice versa.</span></span>

## <a name="transactional-locking"></a><span data-ttu-id="0924a-123">交易式鎖定</span><span class="sxs-lookup"><span data-stu-id="0924a-123">Transactional Locking</span></span>

<span data-ttu-id="0924a-124">在檔案上建立交易寫入器會以交易方式 *鎖定* 檔案。</span><span class="sxs-lookup"><span data-stu-id="0924a-124">Creating a transacted writer on a file *transactionally locks* the file.</span></span> <span data-ttu-id="0924a-125">當交易鎖定檔案之後，嘗試修改交易鎖定檔案之鎖定交易以外的其他檔案系統作業，將會因為 **錯誤 \_ 共用 \_ 違規** 或 **錯誤 \_ 交易 \_ 衝突** 而失敗。</span><span class="sxs-lookup"><span data-stu-id="0924a-125">After a file is locked by a transaction, other file system operations external to the locking transaction that try to modify the transactionally locked file will fail with either **ERROR\_SHARING\_VIOLATION** or **ERROR\_TRANSACTIONAL\_CONFLICT**.</span></span>

<span data-ttu-id="0924a-126">下表摘要說明交易鎖定。</span><span class="sxs-lookup"><span data-stu-id="0924a-126">The following table summarizes transactional locking.</span></span>



<span data-ttu-id="0924a-127">目前開啟的檔案</span><span class="sxs-lookup"><span data-stu-id="0924a-127">File currently opened by</span></span>

<span data-ttu-id="0924a-128">嘗試開啟的檔案</span><span class="sxs-lookup"><span data-stu-id="0924a-128">File open attempted by</span></span>

<span data-ttu-id="0924a-129">交易</span><span class="sxs-lookup"><span data-stu-id="0924a-129">Transacted</span></span>

<span data-ttu-id="0924a-130">非交易</span><span class="sxs-lookup"><span data-stu-id="0924a-130">Non-Transacted</span></span>

<span data-ttu-id="0924a-131">讀者</span><span class="sxs-lookup"><span data-stu-id="0924a-131">Reader</span></span>

<span data-ttu-id="0924a-132">讀取器/寫入器</span><span class="sxs-lookup"><span data-stu-id="0924a-132">Reader/Writer</span></span>

<span data-ttu-id="0924a-133">讀者</span><span class="sxs-lookup"><span data-stu-id="0924a-133">Reader</span></span>

<span data-ttu-id="0924a-134">讀取器/寫入器</span><span class="sxs-lookup"><span data-stu-id="0924a-134">Reader/Writer</span></span>

<span data-ttu-id="0924a-135">交易讀取器</span><span class="sxs-lookup"><span data-stu-id="0924a-135">Transacted Reader</span></span>

<span data-ttu-id="0924a-136">是</span><span class="sxs-lookup"><span data-stu-id="0924a-136">Yes</span></span>

<span data-ttu-id="0924a-137">是</span><span class="sxs-lookup"><span data-stu-id="0924a-137">Yes</span></span>

<span data-ttu-id="0924a-138">是</span><span class="sxs-lookup"><span data-stu-id="0924a-138">Yes</span></span>

<span data-ttu-id="0924a-139">否2</span><span class="sxs-lookup"><span data-stu-id="0924a-139">No2</span></span>

<span data-ttu-id="0924a-140">交易讀取器/寫入器</span><span class="sxs-lookup"><span data-stu-id="0924a-140">Transacted Reader/Writer</span></span>

<span data-ttu-id="0924a-141">Yes</span><span class="sxs-lookup"><span data-stu-id="0924a-141">Yes</span></span>

<span data-ttu-id="0924a-142">否2</span><span class="sxs-lookup"><span data-stu-id="0924a-142">No2</span></span>

<span data-ttu-id="0924a-143">Yes</span><span class="sxs-lookup"><span data-stu-id="0924a-143">Yes</span></span>

<span data-ttu-id="0924a-144">否2</span><span class="sxs-lookup"><span data-stu-id="0924a-144">No2</span></span>

<span data-ttu-id="0924a-145">非交易讀取者</span><span class="sxs-lookup"><span data-stu-id="0924a-145">Non-Transacted Reader</span></span>

<span data-ttu-id="0924a-146">是</span><span class="sxs-lookup"><span data-stu-id="0924a-146">Yes</span></span>

<span data-ttu-id="0924a-147">是</span><span class="sxs-lookup"><span data-stu-id="0924a-147">Yes</span></span>

<span data-ttu-id="0924a-148">是</span><span class="sxs-lookup"><span data-stu-id="0924a-148">Yes</span></span>

<span data-ttu-id="0924a-149">是</span><span class="sxs-lookup"><span data-stu-id="0924a-149">Yes</span></span>

<span data-ttu-id="0924a-150">非交易讀取器/寫入器</span><span class="sxs-lookup"><span data-stu-id="0924a-150">Non-Transacted Reader/Writer</span></span>

<span data-ttu-id="0924a-151">否</span><span class="sxs-lookup"><span data-stu-id="0924a-151">No1</span></span>

<span data-ttu-id="0924a-152">否</span><span class="sxs-lookup"><span data-stu-id="0924a-152">No1</span></span>

<span data-ttu-id="0924a-153">是</span><span class="sxs-lookup"><span data-stu-id="0924a-153">Yes</span></span>

<span data-ttu-id="0924a-154">是</span><span class="sxs-lookup"><span data-stu-id="0924a-154">Yes</span></span>

1. <span data-ttu-id="0924a-155">因 **\_ 交易 \_ 衝突錯誤** 而失敗</span><span class="sxs-lookup"><span data-stu-id="0924a-155">Fails with **ERROR\_TRANSACTIONAL\_CONFLICT**</span></span><br/> <span data-ttu-id="0924a-156">2. 失敗併發生 **錯誤 \_ 共用 \_ 違規**</span><span class="sxs-lookup"><span data-stu-id="0924a-156">2. Fails with **ERROR\_SHARING\_VIOLATION**</span></span><br/>



 

<span data-ttu-id="0924a-157">如果您針對使用交易的修改來開啟命名資料流程，則必須鎖定整個檔案。</span><span class="sxs-lookup"><span data-stu-id="0924a-157">If you open a named stream for a modification that is using a transaction, the entire file is required to be locked.</span></span>

<span data-ttu-id="0924a-158">除了交易式鎖定之外，也適用一般的 NTFS 檔案共用規則。</span><span class="sxs-lookup"><span data-stu-id="0924a-158">In addition to transactional locking, typical NTFS file-sharing rules apply.</span></span>

<span data-ttu-id="0924a-159">您必須將下列兩個檔案共用模式平行考慮：</span><span class="sxs-lookup"><span data-stu-id="0924a-159">You need to consider the following two file sharing modes in parallel:</span></span>

-   <span data-ttu-id="0924a-160">交易式鎖定模式。</span><span class="sxs-lookup"><span data-stu-id="0924a-160">The transactional locking mode.</span></span>
-   <span data-ttu-id="0924a-161">一般檔案共用模式。</span><span class="sxs-lookup"><span data-stu-id="0924a-161">Normal file-sharing modes.</span></span>

<span data-ttu-id="0924a-162">無論何種模式較嚴格，都是套用的。</span><span class="sxs-lookup"><span data-stu-id="0924a-162">Whichever mode is more restrictive is the one that applies.</span></span>

 

 





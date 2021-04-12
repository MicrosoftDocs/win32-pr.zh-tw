---
description: 深入瞭解： EsentStateException 類別
title: EsentStateException 類別
TOCTitle: EsentStateException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentStateException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentstateexception(v=EXCHG.10)
ms:contentKeyID: 55102986
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentStateException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentStateException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d5815c3b308874f69eab9dcc7b3803ee24f6831b
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "104195681"
---
# <a name="esentstateexception-class"></a><span data-ttu-id="fa957-103">EsentStateException 類別</span><span class="sxs-lookup"><span data-stu-id="fa957-103">EsentStateException class</span></span>

<span data-ttu-id="fa957-104">狀態例外狀況的基類。</span><span class="sxs-lookup"><span data-stu-id="fa957-104">Base class for State exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="fa957-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="fa957-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="fa957-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="fa957-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="fa957-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="fa957-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="fa957-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="fa957-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="fa957-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="fa957-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="fa957-110">EsentApiException （.）</span><span class="sxs-lookup"><span data-stu-id="fa957-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          <span data-ttu-id="fa957-111">EsentStateException （.）</span><span class="sxs-lookup"><span data-stu-id="fa957-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>  
            

<span data-ttu-id="fa957-112">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="fa957-112">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="fa957-113">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="fa957-113">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="fa957-114">Syntax</span><span class="sxs-lookup"><span data-stu-id="fa957-114">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentStateException _
    Inherits EsentApiException
'Usage
Dim instance As EsentStateException
```

``` csharp
[SerializableAttribute]
public abstract class EsentStateException : EsentApiException
```

## <a name="thread-safety"></a><span data-ttu-id="fa957-115">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="fa957-115">Thread safety</span></span>

<span data-ttu-id="fa957-116">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="fa957-116">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="fa957-117">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="fa957-117">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="fa957-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fa957-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="fa957-119">參考</span><span class="sxs-lookup"><span data-stu-id="fa957-119">Reference</span></span>

[<span data-ttu-id="fa957-120">EsentStateException 成員</span><span class="sxs-lookup"><span data-stu-id="fa957-120">EsentStateException members</span></span>](./esentstateexception-members.md)

[<span data-ttu-id="fa957-121">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="fa957-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a><span data-ttu-id="fa957-122">衍生類型</span><span class="sxs-lookup"><span data-stu-id="fa957-122">Derived types</span></span>

[<span data-ttu-id="fa957-123">System.Object</span><span class="sxs-lookup"><span data-stu-id="fa957-123">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="fa957-124">System.Exception</span><span class="sxs-lookup"><span data-stu-id="fa957-124">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="fa957-125">EsentException。</span><span class="sxs-lookup"><span data-stu-id="fa957-125">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="fa957-126">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="fa957-126">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="fa957-127">EsentApiException （.）</span><span class="sxs-lookup"><span data-stu-id="fa957-127">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          <span data-ttu-id="fa957-128">EsentStateException （.）</span><span class="sxs-lookup"><span data-stu-id="fa957-128">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>  
            [<span data-ttu-id="fa957-129">EsentBackupInProgressException （.）</span><span class="sxs-lookup"><span data-stu-id="fa957-129">Microsoft.Isam.Esent.Interop.EsentBackupInProgressException</span></span>](./esentbackupinprogressexception-class.md)  
            [<span data-ttu-id="fa957-130">EsentBackupNotAllowedYetException （.）</span><span class="sxs-lookup"><span data-stu-id="fa957-130">Microsoft.Isam.Esent.Interop.EsentBackupNotAllowedYetException</span></span>](./esentbackupnotallowedyetexception-class.md)  
            [<span data-ttu-id="fa957-131">EsentBadItagSequenceException （.）</span><span class="sxs-lookup"><span data-stu-id="fa957-131">Microsoft.Isam.Esent.Interop.EsentBadItagSequenceException</span></span>](./esentbaditagsequenceexception-class.md)  
            [<span data-ttu-id="fa957-132">EsentBufferTooSmallException （.）</span><span class="sxs-lookup"><span data-stu-id="fa957-132">Microsoft.Isam.Esent.Interop.EsentBufferTooSmallException</span></span>](./esentbuffertoosmallexception-class.md)  
            [<span data-ttu-id="fa957-133">EsentCallbackFailedException （.）</span><span class="sxs-lookup"><span data-stu-id="fa957-133">Microsoft.Isam.Esent.Interop.EsentCallbackFailedException</span></span>](./esentcallbackfailedexception-class.md)  
            [<span data-ttu-id="fa957-134">EsentDatabaseAlreadyUpgradedException （.）</span><span class="sxs-lookup"><span data-stu-id="fa957-134">Microsoft.Isam.Esent.Interop.EsentDatabaseAlreadyUpgradedException</span></span>](./esentdatabasealreadyupgradedexception-class.md)  
            [<span data-ttu-id="fa957-135">EsentDatabaseFailedIncrementalReseedException （.）</span><span class="sxs-lookup"><span data-stu-id="fa957-135">Microsoft.Isam.Esent.Interop.EsentDatabaseFailedIncrementalReseedException</span></span>](./esentdatabasefailedincrementalreseedexception-class.md)  
            [<span data-ttu-id="fa957-136">EsentDatabaseIncompleteUpgradeException （.）</span><span class="sxs-lookup"><span data-stu-id="fa957-136">Microsoft.Isam.Esent.Interop.EsentDatabaseIncompleteUpgradeException</span></span>](./esentdatabaseincompleteupgradeexception-class.md)  
            [<span data-ttu-id="fa957-137">EsentDatabaseLeakInSpaceException （.）</span><span class="sxs-lookup"><span data-stu-id="fa957-137">Microsoft.Isam.Esent.Interop.EsentDatabaseLeakInSpaceException</span></span>](./esentdatabaseleakinspaceexception-class.md)  
            [<span data-ttu-id="fa957-138">EsentDirtyShutdownException （.）</span><span class="sxs-lookup"><span data-stu-id="fa957-138">Microsoft.Isam.Esent.Interop.EsentDirtyShutdownException</span></span>](./esentdirtyshutdownexception-class.md)  
            [<span data-ttu-id="fa957-139">EsentFileNotFoundException （.）</span><span class="sxs-lookup"><span data-stu-id="fa957-139">Microsoft.Isam.Esent.Interop.EsentFileNotFoundException</span></span>](./esentfilenotfoundexception-class.md)  
            [<span data-ttu-id="fa957-140">EsentIndexInUseException （.）</span><span class="sxs-lookup"><span data-stu-id="fa957-140">Microsoft.Isam.Esent.Interop.EsentIndexInUseException</span></span>](./esentindexinuseexception-class.md)  
            [<span data-ttu-id="fa957-141">EsentIndexNotFoundException （.）</span><span class="sxs-lookup"><span data-stu-id="fa957-141">Microsoft.Isam.Esent.Interop.EsentIndexNotFoundException</span></span>](./esentindexnotfoundexception-class.md)  
            [<span data-ttu-id="fa957-142">EsentInvalidBufferSizeException （.）</span><span class="sxs-lookup"><span data-stu-id="fa957-142">Microsoft.Isam.Esent.Interop.EsentInvalidBufferSizeException</span></span>](./esentinvalidbuffersizeexception-class.md)  
            [<span data-ttu-id="fa957-143">EsentInvalidLogDataSequenceException （.）</span><span class="sxs-lookup"><span data-stu-id="fa957-143">Microsoft.Isam.Esent.Interop.EsentInvalidLogDataSequenceException</span></span>](./esentinvalidlogdatasequenceexception-class.md)  
            [<span data-ttu-id="fa957-144">EsentKeyDuplicateException （.）</span><span class="sxs-lookup"><span data-stu-id="fa957-144">Microsoft.Isam.Esent.Interop.EsentKeyDuplicateException</span></span>](./esentkeyduplicateexception-class.md)  
            [<span data-ttu-id="fa957-145">EsentKeyTruncatedException （.）</span><span class="sxs-lookup"><span data-stu-id="fa957-145">Microsoft.Isam.Esent.Interop.EsentKeyTruncatedException</span></span>](./esentkeytruncatedexception-class.md)  
            [<span data-ttu-id="fa957-146">EsentLogFileSizeMismatchDatabasesConsistentException （.）</span><span class="sxs-lookup"><span data-stu-id="fa957-146">Microsoft.Isam.Esent.Interop.EsentLogFileSizeMismatchDatabasesConsistentException</span></span>](./esentlogfilesizemismatchdatabasesconsistentexception-class.md)  
            [<span data-ttu-id="fa957-147">EsentLogSectorSizeMismatchDatabasesConsistentException （.）</span><span class="sxs-lookup"><span data-stu-id="fa957-147">Microsoft.Isam.Esent.Interop.EsentLogSectorSizeMismatchDatabasesConsistentException</span></span>](./esentlogsectorsizemismatchdatabasesconsistentexception-class.md)  
            [<span data-ttu-id="fa957-148">EsentLSNotSetException （.）</span><span class="sxs-lookup"><span data-stu-id="fa957-148">Microsoft.Isam.Esent.Interop.EsentLSNotSetException</span></span>](./esentlsnotsetexception-class.md)  
            [<span data-ttu-id="fa957-149">EsentMissingFullBackupException （.）</span><span class="sxs-lookup"><span data-stu-id="fa957-149">Microsoft.Isam.Esent.Interop.EsentMissingFullBackupException</span></span>](./esentmissingfullbackupexception-class.md)  
            [<span data-ttu-id="fa957-150">EsentMultiValuedDuplicateAfterTruncationException （.）</span><span class="sxs-lookup"><span data-stu-id="fa957-150">Microsoft.Isam.Esent.Interop.EsentMultiValuedDuplicateAfterTruncationException</span></span>](./esentmultivaluedduplicateaftertruncationexception-class.md)  
            [<span data-ttu-id="fa957-151">EsentMultiValuedDuplicateException （.）</span><span class="sxs-lookup"><span data-stu-id="fa957-151">Microsoft.Isam.Esent.Interop.EsentMultiValuedDuplicateException</span></span>](./esentmultivaluedduplicateexception-class.md)  
            [<span data-ttu-id="fa957-152">EsentNoAttachmentsFailedIncrementalReseedException （.）</span><span class="sxs-lookup"><span data-stu-id="fa957-152">Microsoft.Isam.Esent.Interop.EsentNoAttachmentsFailedIncrementalReseedException</span></span>](./esentnoattachmentsfailedincrementalreseedexception-class.md)  
            [<span data-ttu-id="fa957-153">EsentNoBackupException （.）</span><span class="sxs-lookup"><span data-stu-id="fa957-153">Microsoft.Isam.Esent.Interop.EsentNoBackupException</span></span>](./esentnobackupexception-class.md)  
            [<span data-ttu-id="fa957-154">EsentNoCurrentRecordException （.）</span><span class="sxs-lookup"><span data-stu-id="fa957-154">Microsoft.Isam.Esent.Interop.EsentNoCurrentRecordException</span></span>](./esentnocurrentrecordexception-class.md)  
            [<span data-ttu-id="fa957-155">EsentObjectNotFoundException （.）</span><span class="sxs-lookup"><span data-stu-id="fa957-155">Microsoft.Isam.Esent.Interop.EsentObjectNotFoundException</span></span>](./esentobjectnotfoundexception-class.md)  
            [<span data-ttu-id="fa957-156">EsentOSSnapshotNotAllowedException （.）</span><span class="sxs-lookup"><span data-stu-id="fa957-156">Microsoft.Isam.Esent.Interop.EsentOSSnapshotNotAllowedException</span></span>](./esentossnapshotnotallowedexception-class.md)  
            [<span data-ttu-id="fa957-157">EsentRecordDeletedException （.）</span><span class="sxs-lookup"><span data-stu-id="fa957-157">Microsoft.Isam.Esent.Interop.EsentRecordDeletedException</span></span>](./esentrecorddeletedexception-class.md)  
            [<span data-ttu-id="fa957-158">EsentRecordNotFoundException （.）</span><span class="sxs-lookup"><span data-stu-id="fa957-158">Microsoft.Isam.Esent.Interop.EsentRecordNotFoundException</span></span>](./esentrecordnotfoundexception-class.md)  
            [<span data-ttu-id="fa957-159">EsentRecordTooBigException （.）</span><span class="sxs-lookup"><span data-stu-id="fa957-159">Microsoft.Isam.Esent.Interop.EsentRecordTooBigException</span></span>](./esentrecordtoobigexception-class.md)  
            [<span data-ttu-id="fa957-160">EsentRecordTooBigForBackwardCompatibilityException （.）</span><span class="sxs-lookup"><span data-stu-id="fa957-160">Microsoft.Isam.Esent.Interop.EsentRecordTooBigForBackwardCompatibilityException</span></span>](./esentrecordtoobigforbackwardcompatibilityexception-class.md)  
            [<span data-ttu-id="fa957-161">EsentRecoveredWithErrorsException （.）</span><span class="sxs-lookup"><span data-stu-id="fa957-161">Microsoft.Isam.Esent.Interop.EsentRecoveredWithErrorsException</span></span>](./esentrecoveredwitherrorsexception-class.md)  
            [<span data-ttu-id="fa957-162">EsentRecoveredWithoutUndoDatabasesConsistentException （.）</span><span class="sxs-lookup"><span data-stu-id="fa957-162">Microsoft.Isam.Esent.Interop.EsentRecoveredWithoutUndoDatabasesConsistentException</span></span>](./esentrecoveredwithoutundodatabasesconsistentexception-class.md)  
            [<span data-ttu-id="fa957-163">EsentRecoveredWithoutUndoException （.）</span><span class="sxs-lookup"><span data-stu-id="fa957-163">Microsoft.Isam.Esent.Interop.EsentRecoveredWithoutUndoException</span></span>](./esentrecoveredwithoutundoexception-class.md)  
            [<span data-ttu-id="fa957-164">EsentRestoreInProgressException （.）</span><span class="sxs-lookup"><span data-stu-id="fa957-164">Microsoft.Isam.Esent.Interop.EsentRestoreInProgressException</span></span>](./esentrestoreinprogressexception-class.md)  
            [<span data-ttu-id="fa957-165">EsentSeparatedLongValueException （.）</span><span class="sxs-lookup"><span data-stu-id="fa957-165">Microsoft.Isam.Esent.Interop.EsentSeparatedLongValueException</span></span>](./esentseparatedlongvalueexception-class.md)  
            [<span data-ttu-id="fa957-166">EsentSurrogateBackupInProgressException （.）</span><span class="sxs-lookup"><span data-stu-id="fa957-166">Microsoft.Isam.Esent.Interop.EsentSurrogateBackupInProgressException</span></span>](./esentsurrogatebackupinprogressexception-class.md)  
            [<span data-ttu-id="fa957-167">EsentTableDuplicateException （.）</span><span class="sxs-lookup"><span data-stu-id="fa957-167">Microsoft.Isam.Esent.Interop.EsentTableDuplicateException</span></span>](./esenttableduplicateexception-class.md)  
            [<span data-ttu-id="fa957-168">EsentTableInUseException （.）</span><span class="sxs-lookup"><span data-stu-id="fa957-168">Microsoft.Isam.Esent.Interop.EsentTableInUseException</span></span>](./esenttableinuseexception-class.md)  
            [<span data-ttu-id="fa957-169">EsentTestInjectionNotSupportedException （.）</span><span class="sxs-lookup"><span data-stu-id="fa957-169">Microsoft.Isam.Esent.Interop.EsentTestInjectionNotSupportedException</span></span>](./esenttestinjectionnotsupportedexception-class.md)  
            [<span data-ttu-id="fa957-170">EsentWriteConflictException （.）</span><span class="sxs-lookup"><span data-stu-id="fa957-170">Microsoft.Isam.Esent.Interop.EsentWriteConflictException</span></span>](./esentwriteconflictexception-class.md)  
            [<span data-ttu-id="fa957-171">EsentWriteConflictPrimaryIndexException （.）</span><span class="sxs-lookup"><span data-stu-id="fa957-171">Microsoft.Isam.Esent.Interop.EsentWriteConflictPrimaryIndexException</span></span>](./esentwriteconflictprimaryindexexception-class.md)
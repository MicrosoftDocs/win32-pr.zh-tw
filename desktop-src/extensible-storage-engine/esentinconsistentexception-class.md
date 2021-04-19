---
description: 深入瞭解： EsentInconsistentException 類別
title: EsentInconsistentException 類別
TOCTitle: EsentInconsistentException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentInconsistentException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinconsistentexception(v=EXCHG.10)
ms:contentKeyID: 55101798
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentInconsistentException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentInconsistentException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e62b963e5b0d3f400a860f7742bb76a183b67bd7
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "106992114"
---
# <a name="esentinconsistentexception-class"></a><span data-ttu-id="9a80a-103">EsentInconsistentException 類別</span><span class="sxs-lookup"><span data-stu-id="9a80a-103">EsentInconsistentException class</span></span>

<span data-ttu-id="9a80a-104">不一致例外狀況的基類。</span><span class="sxs-lookup"><span data-stu-id="9a80a-104">Base class for Inconsistent exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="9a80a-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="9a80a-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="9a80a-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="9a80a-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="9a80a-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="9a80a-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="9a80a-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="9a80a-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="9a80a-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="9a80a-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="9a80a-110">EsentDataException （.）</span><span class="sxs-lookup"><span data-stu-id="9a80a-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          <span data-ttu-id="9a80a-111">EsentInconsistentException （.）</span><span class="sxs-lookup"><span data-stu-id="9a80a-111">Microsoft.Isam.Esent.Interop.EsentInconsistentException</span></span>  
            

<span data-ttu-id="9a80a-112">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9a80a-112">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="9a80a-113">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="9a80a-113">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9a80a-114">Syntax</span><span class="sxs-lookup"><span data-stu-id="9a80a-114">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentInconsistentException _
    Inherits EsentDataException
'Usage
Dim instance As EsentInconsistentException
```

``` csharp
[SerializableAttribute]
public abstract class EsentInconsistentException : EsentDataException
```

## <a name="thread-safety"></a><span data-ttu-id="9a80a-115">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="9a80a-115">Thread safety</span></span>

<span data-ttu-id="9a80a-116">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="9a80a-116">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="9a80a-117">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="9a80a-117">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="9a80a-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9a80a-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9a80a-119">參考</span><span class="sxs-lookup"><span data-stu-id="9a80a-119">Reference</span></span>

[<span data-ttu-id="9a80a-120">EsentInconsistentException 成員</span><span class="sxs-lookup"><span data-stu-id="9a80a-120">EsentInconsistentException members</span></span>](./esentinconsistentexception-members.md)

[<span data-ttu-id="9a80a-121">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="9a80a-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a><span data-ttu-id="9a80a-122">衍生類型</span><span class="sxs-lookup"><span data-stu-id="9a80a-122">Derived types</span></span>

[<span data-ttu-id="9a80a-123">System.Object</span><span class="sxs-lookup"><span data-stu-id="9a80a-123">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="9a80a-124">System.Exception</span><span class="sxs-lookup"><span data-stu-id="9a80a-124">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="9a80a-125">EsentException。</span><span class="sxs-lookup"><span data-stu-id="9a80a-125">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="9a80a-126">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="9a80a-126">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="9a80a-127">EsentDataException （.）</span><span class="sxs-lookup"><span data-stu-id="9a80a-127">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          <span data-ttu-id="9a80a-128">EsentInconsistentException （.）</span><span class="sxs-lookup"><span data-stu-id="9a80a-128">Microsoft.Isam.Esent.Interop.EsentInconsistentException</span></span>  
            [<span data-ttu-id="9a80a-129">EsentAttachedDatabaseMismatchException （.）</span><span class="sxs-lookup"><span data-stu-id="9a80a-129">Microsoft.Isam.Esent.Interop.EsentAttachedDatabaseMismatchException</span></span>](./esentattacheddatabasemismatchexception-class.md)  
            [<span data-ttu-id="9a80a-130">EsentBadCheckpointSignatureException （.）</span><span class="sxs-lookup"><span data-stu-id="9a80a-130">Microsoft.Isam.Esent.Interop.EsentBadCheckpointSignatureException</span></span>](./esentbadcheckpointsignatureexception-class.md)  
            [<span data-ttu-id="9a80a-131">EsentBadLogSignatureException （.）</span><span class="sxs-lookup"><span data-stu-id="9a80a-131">Microsoft.Isam.Esent.Interop.EsentBadLogSignatureException</span></span>](./esentbadlogsignatureexception-class.md)  
            [<span data-ttu-id="9a80a-132">EsentBadLogVersionException （.）</span><span class="sxs-lookup"><span data-stu-id="9a80a-132">Microsoft.Isam.Esent.Interop.EsentBadLogVersionException</span></span>](./esentbadlogversionexception-class.md)  
            [<span data-ttu-id="9a80a-133">EsentCheckpointFileNotFoundException （.）</span><span class="sxs-lookup"><span data-stu-id="9a80a-133">Microsoft.Isam.Esent.Interop.EsentCheckpointFileNotFoundException</span></span>](./esentcheckpointfilenotfoundexception-class.md)  
            [<span data-ttu-id="9a80a-134">EsentConsistentTimeMismatchException （.）</span><span class="sxs-lookup"><span data-stu-id="9a80a-134">Microsoft.Isam.Esent.Interop.EsentConsistentTimeMismatchException</span></span>](./esentconsistenttimemismatchexception-class.md)  
            [<span data-ttu-id="9a80a-135">EsentDatabaseDirtyShutdownException （.）</span><span class="sxs-lookup"><span data-stu-id="9a80a-135">Microsoft.Isam.Esent.Interop.EsentDatabaseDirtyShutdownException</span></span>](./esentdatabasedirtyshutdownexception-class.md)  
            [<span data-ttu-id="9a80a-136">EsentDatabaseIncompleteIncrementalReseedException （.）</span><span class="sxs-lookup"><span data-stu-id="9a80a-136">Microsoft.Isam.Esent.Interop.EsentDatabaseIncompleteIncrementalReseedException</span></span>](./esentdatabaseincompleteincrementalreseedexception-class.md)  
            [<span data-ttu-id="9a80a-137">EsentDatabaseLogSetMismatchException （.）</span><span class="sxs-lookup"><span data-stu-id="9a80a-137">Microsoft.Isam.Esent.Interop.EsentDatabaseLogSetMismatchException</span></span>](./esentdatabaselogsetmismatchexception-class.md)  
            [<span data-ttu-id="9a80a-138">EsentDbTimeTooNewException （.）</span><span class="sxs-lookup"><span data-stu-id="9a80a-138">Microsoft.Isam.Esent.Interop.EsentDbTimeTooNewException</span></span>](./esentdbtimetoonewexception-class.md)  
            [<span data-ttu-id="9a80a-139">EsentDbTimeTooOldException （.）</span><span class="sxs-lookup"><span data-stu-id="9a80a-139">Microsoft.Isam.Esent.Interop.EsentDbTimeTooOldException</span></span>](./esentdbtimetoooldexception-class.md)  
            [<span data-ttu-id="9a80a-140">EsentEndingRestoreLogTooLowException （.）</span><span class="sxs-lookup"><span data-stu-id="9a80a-140">Microsoft.Isam.Esent.Interop.EsentEndingRestoreLogTooLowException</span></span>](./esentendingrestorelogtoolowexception-class.md)  
            [<span data-ttu-id="9a80a-141">EsentExistingLogFileHasBadSignatureException （.）</span><span class="sxs-lookup"><span data-stu-id="9a80a-141">Microsoft.Isam.Esent.Interop.EsentExistingLogFileHasBadSignatureException</span></span>](./esentexistinglogfilehasbadsignatureexception-class.md)  
            [<span data-ttu-id="9a80a-142">EsentExistingLogFileIsNotContiguousException （.）</span><span class="sxs-lookup"><span data-stu-id="9a80a-142">Microsoft.Isam.Esent.Interop.EsentExistingLogFileIsNotContiguousException</span></span>](./esentexistinglogfileisnotcontiguousexception-class.md)  
            [<span data-ttu-id="9a80a-143">EsentFileInvalidTypeException （.）</span><span class="sxs-lookup"><span data-stu-id="9a80a-143">Microsoft.Isam.Esent.Interop.EsentFileInvalidTypeException</span></span>](./esentfileinvalidtypeexception-class.md)  
            [<span data-ttu-id="9a80a-144">EsentGivenLogFileHasBadSignatureException （.）</span><span class="sxs-lookup"><span data-stu-id="9a80a-144">Microsoft.Isam.Esent.Interop.EsentGivenLogFileHasBadSignatureException</span></span>](./esentgivenlogfilehasbadsignatureexception-class.md)  
            [<span data-ttu-id="9a80a-145">EsentGivenLogFileIsNotContiguousException （.）</span><span class="sxs-lookup"><span data-stu-id="9a80a-145">Microsoft.Isam.Esent.Interop.EsentGivenLogFileIsNotContiguousException</span></span>](./esentgivenlogfileisnotcontiguousexception-class.md)  
            [<span data-ttu-id="9a80a-146">EsentInvalidCreateDbVersionException （.）</span><span class="sxs-lookup"><span data-stu-id="9a80a-146">Microsoft.Isam.Esent.Interop.EsentInvalidCreateDbVersionException</span></span>](./esentinvalidcreatedbversionexception-class.md)  
            [<span data-ttu-id="9a80a-147">EsentInvalidDatabaseVersionException （.）</span><span class="sxs-lookup"><span data-stu-id="9a80a-147">Microsoft.Isam.Esent.Interop.EsentInvalidDatabaseVersionException</span></span>](./esentinvaliddatabaseversionexception-class.md)  
            [<span data-ttu-id="9a80a-148">EsentLogGenerationMismatchException （.）</span><span class="sxs-lookup"><span data-stu-id="9a80a-148">Microsoft.Isam.Esent.Interop.EsentLogGenerationMismatchException</span></span>](./esentloggenerationmismatchexception-class.md)  
            [<span data-ttu-id="9a80a-149">EsentMissingCurrentLogFilesException （.）</span><span class="sxs-lookup"><span data-stu-id="9a80a-149">Microsoft.Isam.Esent.Interop.EsentMissingCurrentLogFilesException</span></span>](./esentmissingcurrentlogfilesexception-class.md)  
            [<span data-ttu-id="9a80a-150">EsentMissingFileToBackupException （.）</span><span class="sxs-lookup"><span data-stu-id="9a80a-150">Microsoft.Isam.Esent.Interop.EsentMissingFileToBackupException</span></span>](./esentmissingfiletobackupexception-class.md)  
            [<span data-ttu-id="9a80a-151">EsentMissingRestoreLogFilesException （.）</span><span class="sxs-lookup"><span data-stu-id="9a80a-151">Microsoft.Isam.Esent.Interop.EsentMissingRestoreLogFilesException</span></span>](./esentmissingrestorelogfilesexception-class.md)  
            [<span data-ttu-id="9a80a-152">EsentPageSizeMismatchException （.）</span><span class="sxs-lookup"><span data-stu-id="9a80a-152">Microsoft.Isam.Esent.Interop.EsentPageSizeMismatchException</span></span>](./esentpagesizemismatchexception-class.md)  
            [<span data-ttu-id="9a80a-153">EsentRequiredLogFilesMissingException （.）</span><span class="sxs-lookup"><span data-stu-id="9a80a-153">Microsoft.Isam.Esent.Interop.EsentRequiredLogFilesMissingException</span></span>](./esentrequiredlogfilesmissingexception-class.md)  
            [<span data-ttu-id="9a80a-154">EsentStartingRestoreLogTooHighException （.）</span><span class="sxs-lookup"><span data-stu-id="9a80a-154">Microsoft.Isam.Esent.Interop.EsentStartingRestoreLogTooHighException</span></span>](./esentstartingrestorelogtoohighexception-class.md)
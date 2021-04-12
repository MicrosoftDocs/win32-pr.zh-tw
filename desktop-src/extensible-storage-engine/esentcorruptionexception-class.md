---
description: 深入瞭解： EsentCorruptionException 類別
title: EsentCorruptionException 類別
TOCTitle: EsentCorruptionException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentCorruptionException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentcorruptionexception(v=EXCHG.10)
ms:contentKeyID: 55101411
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentCorruptionException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentCorruptionException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a6914c2bf133a1050e3e3800e5c113c6cac1a11f
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "104195683"
---
# <a name="esentcorruptionexception-class"></a><span data-ttu-id="2a4c2-103">EsentCorruptionException 類別</span><span class="sxs-lookup"><span data-stu-id="2a4c2-103">EsentCorruptionException class</span></span>

<span data-ttu-id="2a4c2-104">損毀例外狀況的基類。</span><span class="sxs-lookup"><span data-stu-id="2a4c2-104">Base class for Corruption exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="2a4c2-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="2a4c2-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="2a4c2-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="2a4c2-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="2a4c2-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="2a4c2-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="2a4c2-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="2a4c2-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="2a4c2-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="2a4c2-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="2a4c2-110">EsentDataException （.）</span><span class="sxs-lookup"><span data-stu-id="2a4c2-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          <span data-ttu-id="2a4c2-111">EsentCorruptionException （.）</span><span class="sxs-lookup"><span data-stu-id="2a4c2-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>  
            

<span data-ttu-id="2a4c2-112">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2a4c2-112">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="2a4c2-113">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="2a4c2-113">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2a4c2-114">Syntax</span><span class="sxs-lookup"><span data-stu-id="2a4c2-114">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentCorruptionException _
    Inherits EsentDataException
'Usage
Dim instance As EsentCorruptionException
```

``` csharp
[SerializableAttribute]
public abstract class EsentCorruptionException : EsentDataException
```

## <a name="thread-safety"></a><span data-ttu-id="2a4c2-115">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="2a4c2-115">Thread safety</span></span>

<span data-ttu-id="2a4c2-116">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="2a4c2-116">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="2a4c2-117">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="2a4c2-117">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="2a4c2-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2a4c2-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2a4c2-119">參考</span><span class="sxs-lookup"><span data-stu-id="2a4c2-119">Reference</span></span>

[<span data-ttu-id="2a4c2-120">EsentCorruptionException 成員</span><span class="sxs-lookup"><span data-stu-id="2a4c2-120">EsentCorruptionException members</span></span>](./esentcorruptionexception-members.md)

[<span data-ttu-id="2a4c2-121">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="2a4c2-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a><span data-ttu-id="2a4c2-122">衍生類型</span><span class="sxs-lookup"><span data-stu-id="2a4c2-122">Derived types</span></span>

[<span data-ttu-id="2a4c2-123">System.Object</span><span class="sxs-lookup"><span data-stu-id="2a4c2-123">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="2a4c2-124">System.Exception</span><span class="sxs-lookup"><span data-stu-id="2a4c2-124">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="2a4c2-125">EsentException。</span><span class="sxs-lookup"><span data-stu-id="2a4c2-125">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="2a4c2-126">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="2a4c2-126">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="2a4c2-127">EsentDataException （.）</span><span class="sxs-lookup"><span data-stu-id="2a4c2-127">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          <span data-ttu-id="2a4c2-128">EsentCorruptionException （.）</span><span class="sxs-lookup"><span data-stu-id="2a4c2-128">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>  
            [<span data-ttu-id="2a4c2-129">EsentBadEmptyPageException （.）</span><span class="sxs-lookup"><span data-stu-id="2a4c2-129">Microsoft.Isam.Esent.Interop.EsentBadEmptyPageException</span></span>](./esentbademptypageexception-class.md)  
            [<span data-ttu-id="2a4c2-130">EsentBadPageLinkException （.）</span><span class="sxs-lookup"><span data-stu-id="2a4c2-130">Microsoft.Isam.Esent.Interop.EsentBadPageLinkException</span></span>](./esentbadpagelinkexception-class.md)  
            [<span data-ttu-id="2a4c2-131">EsentBadParentPageLinkException （.）</span><span class="sxs-lookup"><span data-stu-id="2a4c2-131">Microsoft.Isam.Esent.Interop.EsentBadParentPageLinkException</span></span>](./esentbadparentpagelinkexception-class.md)  
            [<span data-ttu-id="2a4c2-132">EsentCatalogCorruptedException （.）</span><span class="sxs-lookup"><span data-stu-id="2a4c2-132">Microsoft.Isam.Esent.Interop.EsentCatalogCorruptedException</span></span>](./esentcatalogcorruptedexception-class.md)  
            [<span data-ttu-id="2a4c2-133">EsentCheckpointCorruptException （.）</span><span class="sxs-lookup"><span data-stu-id="2a4c2-133">Microsoft.Isam.Esent.Interop.EsentCheckpointCorruptException</span></span>](./esentcheckpointcorruptexception-class.md)  
            [<span data-ttu-id="2a4c2-134">EsentCommittedLogFileCorruptException （.）</span><span class="sxs-lookup"><span data-stu-id="2a4c2-134">Microsoft.Isam.Esent.Interop.EsentCommittedLogFileCorruptException</span></span>](./esentcommittedlogfilecorruptexception-class.md)  
            [<span data-ttu-id="2a4c2-135">EsentCommittedLogFilesMissingException （.）</span><span class="sxs-lookup"><span data-stu-id="2a4c2-135">Microsoft.Isam.Esent.Interop.EsentCommittedLogFilesMissingException</span></span>](./esentcommittedlogfilesmissingexception-class.md)  
            [<span data-ttu-id="2a4c2-136">EsentDatabaseBufferDependenciesCorruptedException （.）</span><span class="sxs-lookup"><span data-stu-id="2a4c2-136">Microsoft.Isam.Esent.Interop.EsentDatabaseBufferDependenciesCorruptedException</span></span>](./esentdatabasebufferdependenciescorruptedexception-class.md)  
            [<span data-ttu-id="2a4c2-137">EsentDatabaseCorruptedException （.）</span><span class="sxs-lookup"><span data-stu-id="2a4c2-137">Microsoft.Isam.Esent.Interop.EsentDatabaseCorruptedException</span></span>](./esentdatabasecorruptedexception-class.md)  
            [<span data-ttu-id="2a4c2-138">EsentDbTimeCorruptedException （.）</span><span class="sxs-lookup"><span data-stu-id="2a4c2-138">Microsoft.Isam.Esent.Interop.EsentDbTimeCorruptedException</span></span>](./esentdbtimecorruptedexception-class.md)  
            [<span data-ttu-id="2a4c2-139">EsentDecompressionFailedException （.）</span><span class="sxs-lookup"><span data-stu-id="2a4c2-139">Microsoft.Isam.Esent.Interop.EsentDecompressionFailedException</span></span>](./esentdecompressionfailedexception-class.md)  
            [<span data-ttu-id="2a4c2-140">EsentDerivedColumnCorruptionException （.）</span><span class="sxs-lookup"><span data-stu-id="2a4c2-140">Microsoft.Isam.Esent.Interop.EsentDerivedColumnCorruptionException</span></span>](./esentderivedcolumncorruptionexception-class.md)  
            [<span data-ttu-id="2a4c2-141">EsentDiskReadVerificationFailureException （.）</span><span class="sxs-lookup"><span data-stu-id="2a4c2-141">Microsoft.Isam.Esent.Interop.EsentDiskReadVerificationFailureException</span></span>](./esentdiskreadverificationfailureexception-class.md)  
            [<span data-ttu-id="2a4c2-142">EsentFileIOBeyondEOFException （.）</span><span class="sxs-lookup"><span data-stu-id="2a4c2-142">Microsoft.Isam.Esent.Interop.EsentFileIOBeyondEOFException</span></span>](./esentfileiobeyondeofexception-class.md)  
            [<span data-ttu-id="2a4c2-143">EsentFileSystemCorruptionException （.）</span><span class="sxs-lookup"><span data-stu-id="2a4c2-143">Microsoft.Isam.Esent.Interop.EsentFileSystemCorruptionException</span></span>](./esentfilesystemcorruptionexception-class.md)  
            [<span data-ttu-id="2a4c2-144">EsentIndexBuildCorruptedException （.）</span><span class="sxs-lookup"><span data-stu-id="2a4c2-144">Microsoft.Isam.Esent.Interop.EsentIndexBuildCorruptedException</span></span>](./esentindexbuildcorruptedexception-class.md)  
            [<span data-ttu-id="2a4c2-145">EsentInvalidLogSequenceException （.）</span><span class="sxs-lookup"><span data-stu-id="2a4c2-145">Microsoft.Isam.Esent.Interop.EsentInvalidLogSequenceException</span></span>](./esentinvalidlogsequenceexception-class.md)  
            [<span data-ttu-id="2a4c2-146">EsentLogCorruptDuringHardRecoveryException （.）</span><span class="sxs-lookup"><span data-stu-id="2a4c2-146">Microsoft.Isam.Esent.Interop.EsentLogCorruptDuringHardRecoveryException</span></span>](./esentlogcorruptduringhardrecoveryexception-class.md)  
            [<span data-ttu-id="2a4c2-147">EsentLogCorruptDuringHardRestoreException （.）</span><span class="sxs-lookup"><span data-stu-id="2a4c2-147">Microsoft.Isam.Esent.Interop.EsentLogCorruptDuringHardRestoreException</span></span>](./esentlogcorruptduringhardrestoreexception-class.md)  
            [<span data-ttu-id="2a4c2-148">EsentLogCorruptedException （.）</span><span class="sxs-lookup"><span data-stu-id="2a4c2-148">Microsoft.Isam.Esent.Interop.EsentLogCorruptedException</span></span>](./esentlogcorruptedexception-class.md)  
            [<span data-ttu-id="2a4c2-149">EsentLogFileCorruptException （.）</span><span class="sxs-lookup"><span data-stu-id="2a4c2-149">Microsoft.Isam.Esent.Interop.EsentLogFileCorruptException</span></span>](./esentlogfilecorruptexception-class.md)  
            [<span data-ttu-id="2a4c2-150">EsentLogReadVerifyFailureException （.）</span><span class="sxs-lookup"><span data-stu-id="2a4c2-150">Microsoft.Isam.Esent.Interop.EsentLogReadVerifyFailureException</span></span>](./esentlogreadverifyfailureexception-class.md)  
            [<span data-ttu-id="2a4c2-151">EsentLogTornWriteDuringHardRecoveryException （.）</span><span class="sxs-lookup"><span data-stu-id="2a4c2-151">Microsoft.Isam.Esent.Interop.EsentLogTornWriteDuringHardRecoveryException</span></span>](./esentlogtornwriteduringhardrecoveryexception-class.md)  
            [<span data-ttu-id="2a4c2-152">EsentLogTornWriteDuringHardRestoreException （.）</span><span class="sxs-lookup"><span data-stu-id="2a4c2-152">Microsoft.Isam.Esent.Interop.EsentLogTornWriteDuringHardRestoreException</span></span>](./esentlogtornwriteduringhardrestoreexception-class.md)  
            [<span data-ttu-id="2a4c2-153">EsentLVCorruptedException （.）</span><span class="sxs-lookup"><span data-stu-id="2a4c2-153">Microsoft.Isam.Esent.Interop.EsentLVCorruptedException</span></span>](./esentlvcorruptedexception-class.md)  
            [<span data-ttu-id="2a4c2-154">EsentMissingLogFileException （.）</span><span class="sxs-lookup"><span data-stu-id="2a4c2-154">Microsoft.Isam.Esent.Interop.EsentMissingLogFileException</span></span>](./esentmissinglogfileexception-class.md)  
            [<span data-ttu-id="2a4c2-155">EsentMissingPreviousLogFileException （.）</span><span class="sxs-lookup"><span data-stu-id="2a4c2-155">Microsoft.Isam.Esent.Interop.EsentMissingPreviousLogFileException</span></span>](./esentmissingpreviouslogfileexception-class.md)  
            [<span data-ttu-id="2a4c2-156">EsentPageNotInitializedException （.）</span><span class="sxs-lookup"><span data-stu-id="2a4c2-156">Microsoft.Isam.Esent.Interop.EsentPageNotInitializedException</span></span>](./esentpagenotinitializedexception-class.md)  
            [<span data-ttu-id="2a4c2-157">EsentPrimaryIndexCorruptedException （.）</span><span class="sxs-lookup"><span data-stu-id="2a4c2-157">Microsoft.Isam.Esent.Interop.EsentPrimaryIndexCorruptedException</span></span>](./esentprimaryindexcorruptedexception-class.md)  
            [<span data-ttu-id="2a4c2-158">EsentReadLostFlushVerifyFailureException （.）</span><span class="sxs-lookup"><span data-stu-id="2a4c2-158">Microsoft.Isam.Esent.Interop.EsentReadLostFlushVerifyFailureException</span></span>](./esentreadlostflushverifyfailureexception-class.md)  
            [<span data-ttu-id="2a4c2-159">EsentReadPgnoVerifyFailureException （.）</span><span class="sxs-lookup"><span data-stu-id="2a4c2-159">Microsoft.Isam.Esent.Interop.EsentReadPgnoVerifyFailureException</span></span>](./esentreadpgnoverifyfailureexception-class.md)  
            [<span data-ttu-id="2a4c2-160">EsentReadVerifyFailureException （.）</span><span class="sxs-lookup"><span data-stu-id="2a4c2-160">Microsoft.Isam.Esent.Interop.EsentReadVerifyFailureException</span></span>](./esentreadverifyfailureexception-class.md)  
            [<span data-ttu-id="2a4c2-161">EsentRecordFormatConversionFailedException （.）</span><span class="sxs-lookup"><span data-stu-id="2a4c2-161">Microsoft.Isam.Esent.Interop.EsentRecordFormatConversionFailedException</span></span>](./esentrecordformatconversionfailedexception-class.md)  
            [<span data-ttu-id="2a4c2-162">EsentRecoveryVerifyFailureException （.）</span><span class="sxs-lookup"><span data-stu-id="2a4c2-162">Microsoft.Isam.Esent.Interop.EsentRecoveryVerifyFailureException</span></span>](./esentrecoveryverifyfailureexception-class.md)  
            [<span data-ttu-id="2a4c2-163">EsentRedoAbruptEndedException （.）</span><span class="sxs-lookup"><span data-stu-id="2a4c2-163">Microsoft.Isam.Esent.Interop.EsentRedoAbruptEndedException</span></span>](./esentredoabruptendedexception-class.md)  
            [<span data-ttu-id="2a4c2-164">EsentSecondaryIndexCorruptedException （.）</span><span class="sxs-lookup"><span data-stu-id="2a4c2-164">Microsoft.Isam.Esent.Interop.EsentSecondaryIndexCorruptedException</span></span>](./esentsecondaryindexcorruptedexception-class.md)  
            [<span data-ttu-id="2a4c2-165">EsentSPAvailExtCorruptedException （.）</span><span class="sxs-lookup"><span data-stu-id="2a4c2-165">Microsoft.Isam.Esent.Interop.EsentSPAvailExtCorruptedException</span></span>](./esentspavailextcorruptedexception-class.md)  
            [<span data-ttu-id="2a4c2-166">EsentSPOwnExtCorruptedException （.）</span><span class="sxs-lookup"><span data-stu-id="2a4c2-166">Microsoft.Isam.Esent.Interop.EsentSPOwnExtCorruptedException</span></span>](./esentspownextcorruptedexception-class.md)
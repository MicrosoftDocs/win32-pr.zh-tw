---
description: 深入瞭解： EsentUsageException 類別
title: EsentUsageException 類別
TOCTitle: EsentUsageException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentUsageException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentusageexception(v=EXCHG.10)
ms:contentKeyID: 55103173
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentUsageException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentUsageException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0319ae3d6185e3075931fb601ec789aba70dfd82
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "103853247"
---
# <a name="esentusageexception-class"></a><span data-ttu-id="20521-103">EsentUsageException 類別</span><span class="sxs-lookup"><span data-stu-id="20521-103">EsentUsageException class</span></span>

<span data-ttu-id="20521-104">使用例外狀況的基類。</span><span class="sxs-lookup"><span data-stu-id="20521-104">Base class for Usage exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="20521-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="20521-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="20521-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="20521-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="20521-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="20521-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="20521-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="20521-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="20521-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="20521-110">EsentApiException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          <span data-ttu-id="20521-111">EsentUsageException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>  
            

<span data-ttu-id="20521-112">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="20521-112">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="20521-113">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="20521-113">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="20521-114">Syntax</span><span class="sxs-lookup"><span data-stu-id="20521-114">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentUsageException _
    Inherits EsentApiException
'Usage
Dim instance As EsentUsageException
```

``` csharp
[SerializableAttribute]
public abstract class EsentUsageException : EsentApiException
```

## <a name="thread-safety"></a><span data-ttu-id="20521-115">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="20521-115">Thread safety</span></span>

<span data-ttu-id="20521-116">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="20521-116">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="20521-117">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="20521-117">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="20521-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="20521-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="20521-119">參考</span><span class="sxs-lookup"><span data-stu-id="20521-119">Reference</span></span>

[<span data-ttu-id="20521-120">EsentUsageException 成員</span><span class="sxs-lookup"><span data-stu-id="20521-120">EsentUsageException members</span></span>](./esentusageexception-members.md)

[<span data-ttu-id="20521-121">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="20521-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a><span data-ttu-id="20521-122">衍生類型</span><span class="sxs-lookup"><span data-stu-id="20521-122">Derived types</span></span>

[<span data-ttu-id="20521-123">System.Object</span><span class="sxs-lookup"><span data-stu-id="20521-123">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="20521-124">System.Exception</span><span class="sxs-lookup"><span data-stu-id="20521-124">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="20521-125">EsentException。</span><span class="sxs-lookup"><span data-stu-id="20521-125">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="20521-126">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-126">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="20521-127">EsentApiException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-127">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          <span data-ttu-id="20521-128">EsentUsageException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-128">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>  
            [<span data-ttu-id="20521-129">EsentAfterInitializationException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-129">Microsoft.Isam.Esent.Interop.EsentAfterInitializationException</span></span>](./esentafterinitializationexception-class.md)  
            [<span data-ttu-id="20521-130">EsentAlreadyInitializedException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-130">Microsoft.Isam.Esent.Interop.EsentAlreadyInitializedException</span></span>](./esentalreadyinitializedexception-class.md)  
            [<span data-ttu-id="20521-131">EsentAlreadyPreparedException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-131">Microsoft.Isam.Esent.Interop.EsentAlreadyPreparedException</span></span>](./esentalreadypreparedexception-class.md)  
            [<span data-ttu-id="20521-132">EsentBackupDirectoryNotEmptyException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-132">Microsoft.Isam.Esent.Interop.EsentBackupDirectoryNotEmptyException</span></span>](./esentbackupdirectorynotemptyexception-class.md)  
            [<span data-ttu-id="20521-133">EsentBadColumnIdException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-133">Microsoft.Isam.Esent.Interop.EsentBadColumnIdException</span></span>](./esentbadcolumnidexception-class.md)  
            [<span data-ttu-id="20521-134">EsentBadRestoreTargetInstanceException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-134">Microsoft.Isam.Esent.Interop.EsentBadRestoreTargetInstanceException</span></span>](./esentbadrestoretargetinstanceexception-class.md)  
            [<span data-ttu-id="20521-135">EsentCallbackNotResolvedException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-135">Microsoft.Isam.Esent.Interop.EsentCallbackNotResolvedException</span></span>](./esentcallbacknotresolvedexception-class.md)  
            [<span data-ttu-id="20521-136">EsentCannotBeTaggedException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-136">Microsoft.Isam.Esent.Interop.EsentCannotBeTaggedException</span></span>](./esentcannotbetaggedexception-class.md)  
            [<span data-ttu-id="20521-137">EsentCannotDeleteSystemTableException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-137">Microsoft.Isam.Esent.Interop.EsentCannotDeleteSystemTableException</span></span>](./esentcannotdeletesystemtableexception-class.md)  
            [<span data-ttu-id="20521-138">EsentCannotDeleteTemplateTableException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-138">Microsoft.Isam.Esent.Interop.EsentCannotDeleteTemplateTableException</span></span>](./esentcannotdeletetemplatetableexception-class.md)  
            [<span data-ttu-id="20521-139">EsentCannotDeleteTempTableException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-139">Microsoft.Isam.Esent.Interop.EsentCannotDeleteTempTableException</span></span>](./esentcannotdeletetemptableexception-class.md)  
            [<span data-ttu-id="20521-140">EsentCannotDisableVersioningException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-140">Microsoft.Isam.Esent.Interop.EsentCannotDisableVersioningException</span></span>](./esentcannotdisableversioningexception-class.md)  
            [<span data-ttu-id="20521-141">EsentCannotIndexException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-141">Microsoft.Isam.Esent.Interop.EsentCannotIndexException</span></span>](./esentcannotindexexception-class.md)  
            [<span data-ttu-id="20521-142">EsentCannotMaterializeForwardOnlySortException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-142">Microsoft.Isam.Esent.Interop.EsentCannotMaterializeForwardOnlySortException</span></span>](./esentcannotmaterializeforwardonlysortexception-class.md)  
            [<span data-ttu-id="20521-143">EsentCannotNestDDLException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-143">Microsoft.Isam.Esent.Interop.EsentCannotNestDDLException</span></span>](./esentcannotnestddlexception-class.md)  
            [<span data-ttu-id="20521-144">EsentCannotSeparateIntrinsicLVException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-144">Microsoft.Isam.Esent.Interop.EsentCannotSeparateIntrinsicLVException</span></span>](./esentcannotseparateintrinsiclvexception-class.md)  
            [<span data-ttu-id="20521-145">EsentColumnCannotBeCompressedException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-145">Microsoft.Isam.Esent.Interop.EsentColumnCannotBeCompressedException</span></span>](./esentcolumncannotbecompressedexception-class.md)  
            [<span data-ttu-id="20521-146">EsentColumnDoesNotFitException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-146">Microsoft.Isam.Esent.Interop.EsentColumnDoesNotFitException</span></span>](./esentcolumndoesnotfitexception-class.md)  
            [<span data-ttu-id="20521-147">EsentColumnDuplicateException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-147">Microsoft.Isam.Esent.Interop.EsentColumnDuplicateException</span></span>](./esentcolumnduplicateexception-class.md)  
            [<span data-ttu-id="20521-148">EsentColumnInUseException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-148">Microsoft.Isam.Esent.Interop.EsentColumnInUseException</span></span>](./esentcolumninuseexception-class.md)  
            [<span data-ttu-id="20521-149">EsentColumnNoChunkException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-149">Microsoft.Isam.Esent.Interop.EsentColumnNoChunkException</span></span>](./esentcolumnnochunkexception-class.md)  
            [<span data-ttu-id="20521-150">EsentColumnNotFoundException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-150">Microsoft.Isam.Esent.Interop.EsentColumnNotFoundException</span></span>](./esentcolumnnotfoundexception-class.md)  
            [<span data-ttu-id="20521-151">EsentColumnNotUpdatableException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-151">Microsoft.Isam.Esent.Interop.EsentColumnNotUpdatableException</span></span>](./esentcolumnnotupdatableexception-class.md)  
            [<span data-ttu-id="20521-152">EsentColumnRedundantException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-152">Microsoft.Isam.Esent.Interop.EsentColumnRedundantException</span></span>](./esentcolumnredundantexception-class.md)  
            [<span data-ttu-id="20521-153">EsentColumnTooBigException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-153">Microsoft.Isam.Esent.Interop.EsentColumnTooBigException</span></span>](./esentcolumntoobigexception-class.md)  
            [<span data-ttu-id="20521-154">EsentDatabaseAlreadyRunningMaintenanceException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-154">Microsoft.Isam.Esent.Interop.EsentDatabaseAlreadyRunningMaintenanceException</span></span>](./esentdatabasealreadyrunningmaintenanceexception-class.md)  
            [<span data-ttu-id="20521-155">EsentDatabaseCorruptedNoRepairException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-155">Microsoft.Isam.Esent.Interop.EsentDatabaseCorruptedNoRepairException</span></span>](./esentdatabasecorruptednorepairexception-class.md)  
            [<span data-ttu-id="20521-156">EsentDatabaseDuplicateException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-156">Microsoft.Isam.Esent.Interop.EsentDatabaseDuplicateException</span></span>](./esentdatabaseduplicateexception-class.md)  
            [<span data-ttu-id="20521-157">EsentDatabaseFileReadOnlyException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-157">Microsoft.Isam.Esent.Interop.EsentDatabaseFileReadOnlyException</span></span>](./esentdatabasefilereadonlyexception-class.md)  
            [<span data-ttu-id="20521-158">EsentDatabaseInUseException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-158">Microsoft.Isam.Esent.Interop.EsentDatabaseInUseException</span></span>](./esentdatabaseinuseexception-class.md)  
            [<span data-ttu-id="20521-159">EsentDatabaseInvalidIncrementalReseedException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-159">Microsoft.Isam.Esent.Interop.EsentDatabaseInvalidIncrementalReseedException</span></span>](./esentdatabaseinvalidincrementalreseedexception-class.md)  
            [<span data-ttu-id="20521-160">EsentDatabaseInvalidNameException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-160">Microsoft.Isam.Esent.Interop.EsentDatabaseInvalidNameException</span></span>](./esentdatabaseinvalidnameexception-class.md)  
            [<span data-ttu-id="20521-161">EsentDatabaseInvalidPagesException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-161">Microsoft.Isam.Esent.Interop.EsentDatabaseInvalidPagesException</span></span>](./esentdatabaseinvalidpagesexception-class.md)  
            [<span data-ttu-id="20521-162">EsentDatabaseInvalidPathException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-162">Microsoft.Isam.Esent.Interop.EsentDatabaseInvalidPathException</span></span>](./esentdatabaseinvalidpathexception-class.md)  
            [<span data-ttu-id="20521-163">EsentDatabaseLockedException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-163">Microsoft.Isam.Esent.Interop.EsentDatabaseLockedException</span></span>](./esentdatabaselockedexception-class.md)  
            [<span data-ttu-id="20521-164">EsentDatabaseNotFoundException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-164">Microsoft.Isam.Esent.Interop.EsentDatabaseNotFoundException</span></span>](./esentdatabasenotfoundexception-class.md)  
            [<span data-ttu-id="20521-165">EsentDatabaseSharingViolationException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-165">Microsoft.Isam.Esent.Interop.EsentDatabaseSharingViolationException</span></span>](./esentdatabasesharingviolationexception-class.md)  
            [<span data-ttu-id="20521-166">EsentDatabaseSignInUseException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-166">Microsoft.Isam.Esent.Interop.EsentDatabaseSignInUseException</span></span>](./esentdatabasesigninuseexception-class.md)  
            [<span data-ttu-id="20521-167">EsentDDLNotInheritableException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-167">Microsoft.Isam.Esent.Interop.EsentDDLNotInheritableException</span></span>](./esentddlnotinheritableexception-class.md)  
            [<span data-ttu-id="20521-168">EsentDefaultValueTooBigException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-168">Microsoft.Isam.Esent.Interop.EsentDefaultValueTooBigException</span></span>](./esentdefaultvaluetoobigexception-class.md)  
            [<span data-ttu-id="20521-169">EsentDensityInvalidException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-169">Microsoft.Isam.Esent.Interop.EsentDensityInvalidException</span></span>](./esentdensityinvalidexception-class.md)  
            [<span data-ttu-id="20521-170">EsentDisabledFunctionalityException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-170">Microsoft.Isam.Esent.Interop.EsentDisabledFunctionalityException</span></span>](./esentdisabledfunctionalityexception-class.md)  
            [<span data-ttu-id="20521-171">EsentEntryPointNotFoundException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-171">Microsoft.Isam.Esent.Interop.EsentEntryPointNotFoundException</span></span>](./esententrypointnotfoundexception-class.md)  
            [<span data-ttu-id="20521-172">EsentExclusiveTableLockRequiredException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-172">Microsoft.Isam.Esent.Interop.EsentExclusiveTableLockRequiredException</span></span>](./esentexclusivetablelockrequiredexception-class.md)  
            [<span data-ttu-id="20521-173">EsentFeatureNotAvailableException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-173">Microsoft.Isam.Esent.Interop.EsentFeatureNotAvailableException</span></span>](./esentfeaturenotavailableexception-class.md)  
            [<span data-ttu-id="20521-174">EsentFileCompressedException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-174">Microsoft.Isam.Esent.Interop.EsentFileCompressedException</span></span>](./esentfilecompressedexception-class.md)  
            [<span data-ttu-id="20521-175">EsentFilteredMoveNotSupportedException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-175">Microsoft.Isam.Esent.Interop.EsentFilteredMoveNotSupportedException</span></span>](./esentfilteredmovenotsupportedexception-class.md)  
            [<span data-ttu-id="20521-176">EsentFixedDDLException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-176">Microsoft.Isam.Esent.Interop.EsentFixedDDLException</span></span>](./esentfixedddlexception-class.md)  
            [<span data-ttu-id="20521-177">EsentFixedInheritedDDLException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-177">Microsoft.Isam.Esent.Interop.EsentFixedInheritedDDLException</span></span>](./esentfixedinheritedddlexception-class.md)  
            [<span data-ttu-id="20521-178">EsentForceDetachNotAllowedException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-178">Microsoft.Isam.Esent.Interop.EsentForceDetachNotAllowedException</span></span>](./esentforcedetachnotallowedexception-class.md)  
            [<span data-ttu-id="20521-179">EsentIllegalOperationException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-179">Microsoft.Isam.Esent.Interop.EsentIllegalOperationException</span></span>](./esentillegaloperationexception-class.md)  
            [<span data-ttu-id="20521-180">EsentIndexDuplicateException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-180">Microsoft.Isam.Esent.Interop.EsentIndexDuplicateException</span></span>](./esentindexduplicateexception-class.md)  
            [<span data-ttu-id="20521-181">EsentIndexHasPrimaryException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-181">Microsoft.Isam.Esent.Interop.EsentIndexHasPrimaryException</span></span>](./esentindexhasprimaryexception-class.md)  
            [<span data-ttu-id="20521-182">EsentIndexInvalidDefException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-182">Microsoft.Isam.Esent.Interop.EsentIndexInvalidDefException</span></span>](./esentindexinvaliddefexception-class.md)  
            [<span data-ttu-id="20521-183">EsentIndexMustStayException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-183">Microsoft.Isam.Esent.Interop.EsentIndexMustStayException</span></span>](./esentindexmuststayexception-class.md)  
            [<span data-ttu-id="20521-184">EsentIndexTuplesCannotRetrieveFromIndexException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-184">Microsoft.Isam.Esent.Interop.EsentIndexTuplesCannotRetrieveFromIndexException</span></span>](./esentindextuplescannotretrievefromindexexception-class.md)  
            [<span data-ttu-id="20521-185">EsentIndexTuplesInvalidLimitsException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-185">Microsoft.Isam.Esent.Interop.EsentIndexTuplesInvalidLimitsException</span></span>](./esentindextuplesinvalidlimitsexception-class.md)  
            [<span data-ttu-id="20521-186">EsentIndexTuplesKeyTooSmallException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-186">Microsoft.Isam.Esent.Interop.EsentIndexTuplesKeyTooSmallException</span></span>](./esentindextupleskeytoosmallexception-class.md)  
            [<span data-ttu-id="20521-187">EsentIndexTuplesNonUniqueOnlyException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-187">Microsoft.Isam.Esent.Interop.EsentIndexTuplesNonUniqueOnlyException</span></span>](./esentindextuplesnonuniqueonlyexception-class.md)  
            [<span data-ttu-id="20521-188">EsentIndexTuplesSecondaryIndexOnlyException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-188">Microsoft.Isam.Esent.Interop.EsentIndexTuplesSecondaryIndexOnlyException</span></span>](./esentindextuplessecondaryindexonlyexception-class.md)  
            [<span data-ttu-id="20521-189">EsentIndexTuplesTextBinaryColumnsOnlyException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-189">Microsoft.Isam.Esent.Interop.EsentIndexTuplesTextBinaryColumnsOnlyException</span></span>](./esentindextuplestextbinarycolumnsonlyexception-class.md)  
            [<span data-ttu-id="20521-190">EsentIndexTuplesVarSegMacNotAllowedException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-190">Microsoft.Isam.Esent.Interop.EsentIndexTuplesVarSegMacNotAllowedException</span></span>](./esentindextuplesvarsegmacnotallowedexception-class.md)  
            [<span data-ttu-id="20521-191">EsentInstanceNameInUseException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-191">Microsoft.Isam.Esent.Interop.EsentInstanceNameInUseException</span></span>](./esentinstancenameinuseexception-class.md)  
            [<span data-ttu-id="20521-192">EsentInTransactionException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-192">Microsoft.Isam.Esent.Interop.EsentInTransactionException</span></span>](./esentintransactionexception-class.md)  
            [<span data-ttu-id="20521-193">EsentInvalidBackupException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-193">Microsoft.Isam.Esent.Interop.EsentInvalidBackupException</span></span>](./esentinvalidbackupexception-class.md)  
            [<span data-ttu-id="20521-194">EsentInvalidBackupSequenceException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-194">Microsoft.Isam.Esent.Interop.EsentInvalidBackupSequenceException</span></span>](./esentinvalidbackupsequenceexception-class.md)  
            [<span data-ttu-id="20521-195">EsentInvalidBookmarkException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-195">Microsoft.Isam.Esent.Interop.EsentInvalidBookmarkException</span></span>](./esentinvalidbookmarkexception-class.md)  
            [<span data-ttu-id="20521-196">EsentInvalidCodePageException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-196">Microsoft.Isam.Esent.Interop.EsentInvalidCodePageException</span></span>](./esentinvalidcodepageexception-class.md)  
            [<span data-ttu-id="20521-197">EsentInvalidColumnTypeException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-197">Microsoft.Isam.Esent.Interop.EsentInvalidColumnTypeException</span></span>](./esentinvalidcolumntypeexception-class.md)  
            [<span data-ttu-id="20521-198">EsentInvalidCreateIndexException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-198">Microsoft.Isam.Esent.Interop.EsentInvalidCreateIndexException</span></span>](./esentinvalidcreateindexexception-class.md)  
            [<span data-ttu-id="20521-199">EsentInvalidDatabaseException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-199">Microsoft.Isam.Esent.Interop.EsentInvalidDatabaseException</span></span>](./esentinvaliddatabaseexception-class.md)  
            [<span data-ttu-id="20521-200">EsentInvalidDatabaseIdException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-200">Microsoft.Isam.Esent.Interop.EsentInvalidDatabaseIdException</span></span>](./esentinvaliddatabaseidexception-class.md)  
            [<span data-ttu-id="20521-201">EsentInvalidGrbitException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-201">Microsoft.Isam.Esent.Interop.EsentInvalidGrbitException</span></span>](./esentinvalidgrbitexception-class.md)  
            [<span data-ttu-id="20521-202">EsentInvalidIndexIdException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-202">Microsoft.Isam.Esent.Interop.EsentInvalidIndexIdException</span></span>](./esentinvalidindexidexception-class.md)  
            [<span data-ttu-id="20521-203">EsentInvalidInstanceException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-203">Microsoft.Isam.Esent.Interop.EsentInvalidInstanceException</span></span>](./esentinvalidinstanceexception-class.md)  
            [<span data-ttu-id="20521-204">EsentInvalidLanguageIdException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-204">Microsoft.Isam.Esent.Interop.EsentInvalidLanguageIdException</span></span>](./esentinvalidlanguageidexception-class.md)  
            [<span data-ttu-id="20521-205">EsentInvalidLCMapStringFlagsException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-205">Microsoft.Isam.Esent.Interop.EsentInvalidLCMapStringFlagsException</span></span>](./esentinvalidlcmapstringflagsexception-class.md)  
            [<span data-ttu-id="20521-206">EsentInvalidNameException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-206">Microsoft.Isam.Esent.Interop.EsentInvalidNameException</span></span>](./esentinvalidnameexception-class.md)  
            [<span data-ttu-id="20521-207">EsentInvalidOperationException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-207">Microsoft.Isam.Esent.Interop.EsentInvalidOperationException</span></span>](./esentinvalidoperationexception-class.md)  
            [<span data-ttu-id="20521-208">EsentInvalidParameterException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-208">Microsoft.Isam.Esent.Interop.EsentInvalidParameterException</span></span>](./esentinvalidparameterexception-class.md)  
            [<span data-ttu-id="20521-209">EsentInvalidPathException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-209">Microsoft.Isam.Esent.Interop.EsentInvalidPathException</span></span>](./esentinvalidpathexception-class.md)  
            [<span data-ttu-id="20521-210">EsentInvalidPlaceholderColumnException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-210">Microsoft.Isam.Esent.Interop.EsentInvalidPlaceholderColumnException</span></span>](./esentinvalidplaceholdercolumnexception-class.md)  
            [<span data-ttu-id="20521-211">EsentInvalidPrereadException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-211">Microsoft.Isam.Esent.Interop.EsentInvalidPrereadException</span></span>](./esentinvalidprereadexception-class.md)  
            [<span data-ttu-id="20521-212">EsentInvalidSesidException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-212">Microsoft.Isam.Esent.Interop.EsentInvalidSesidException</span></span>](./esentinvalidsesidexception-class.md)  
            [<span data-ttu-id="20521-213">EsentInvalidSettingsException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-213">Microsoft.Isam.Esent.Interop.EsentInvalidSettingsException</span></span>](./esentinvalidsettingsexception-class.md)  
            [<span data-ttu-id="20521-214">EsentInvalidTableIdException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-214">Microsoft.Isam.Esent.Interop.EsentInvalidTableIdException</span></span>](./esentinvalidtableidexception-class.md)  
            [<span data-ttu-id="20521-215">EsentKeyIsMadeException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-215">Microsoft.Isam.Esent.Interop.EsentKeyIsMadeException</span></span>](./esentkeyismadeexception-class.md)  
            [<span data-ttu-id="20521-216">EsentKeyNotMadeException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-216">Microsoft.Isam.Esent.Interop.EsentKeyNotMadeException</span></span>](./esentkeynotmadeexception-class.md)  
            [<span data-ttu-id="20521-217">EsentLogFileNotCopiedException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-217">Microsoft.Isam.Esent.Interop.EsentLogFileNotCopiedException</span></span>](./esentlogfilenotcopiedexception-class.md)  
            [<span data-ttu-id="20521-218">EsentLogFilePathInUseException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-218">Microsoft.Isam.Esent.Interop.EsentLogFilePathInUseException</span></span>](./esentlogfilepathinuseexception-class.md)  
            [<span data-ttu-id="20521-219">EsentLogFileSizeMismatchException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-219">Microsoft.Isam.Esent.Interop.EsentLogFileSizeMismatchException</span></span>](./esentlogfilesizemismatchexception-class.md)  
            [<span data-ttu-id="20521-220">EsentLoggingDisabledException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-220">Microsoft.Isam.Esent.Interop.EsentLoggingDisabledException</span></span>](./esentloggingdisabledexception-class.md)  
            [<span data-ttu-id="20521-221">EsentLSAlreadySetException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-221">Microsoft.Isam.Esent.Interop.EsentLSAlreadySetException</span></span>](./esentlsalreadysetexception-class.md)  
            [<span data-ttu-id="20521-222">EsentLSCallbackNotSpecifiedException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-222">Microsoft.Isam.Esent.Interop.EsentLSCallbackNotSpecifiedException</span></span>](./esentlscallbacknotspecifiedexception-class.md)  
            [<span data-ttu-id="20521-223">EsentMultiValuedColumnMustBeTaggedException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-223">Microsoft.Isam.Esent.Interop.EsentMultiValuedColumnMustBeTaggedException</span></span>](./esentmultivaluedcolumnmustbetaggedexception-class.md)  
            [<span data-ttu-id="20521-224">EsentMultiValuedIndexViolationException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-224">Microsoft.Isam.Esent.Interop.EsentMultiValuedIndexViolationException</span></span>](./esentmultivaluedindexviolationexception-class.md)  
            [<span data-ttu-id="20521-225">EsentMustBeSeparateLongValueException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-225">Microsoft.Isam.Esent.Interop.EsentMustBeSeparateLongValueException</span></span>](./esentmustbeseparatelongvalueexception-class.md)  
            [<span data-ttu-id="20521-226">EsentMustRollbackException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-226">Microsoft.Isam.Esent.Interop.EsentMustRollbackException</span></span>](./esentmustrollbackexception-class.md)  
            [<span data-ttu-id="20521-227">EsentNoBackupDirectoryException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-227">Microsoft.Isam.Esent.Interop.EsentNoBackupDirectoryException</span></span>](./esentnobackupdirectoryexception-class.md)  
            [<span data-ttu-id="20521-228">EsentNoCurrentIndexException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-228">Microsoft.Isam.Esent.Interop.EsentNoCurrentIndexException</span></span>](./esentnocurrentindexexception-class.md)  
            [<span data-ttu-id="20521-229">EsentNotInitializedException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-229">Microsoft.Isam.Esent.Interop.EsentNotInitializedException</span></span>](./esentnotinitializedexception-class.md)  
            [<span data-ttu-id="20521-230">EsentNotInTransactionException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-230">Microsoft.Isam.Esent.Interop.EsentNotInTransactionException</span></span>](./esentnotintransactionexception-class.md)  
            [<span data-ttu-id="20521-231">EsentNullInvalidException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-231">Microsoft.Isam.Esent.Interop.EsentNullInvalidException</span></span>](./esentnullinvalidexception-class.md)  
            [<span data-ttu-id="20521-232">EsentNullKeyDisallowedException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-232">Microsoft.Isam.Esent.Interop.EsentNullKeyDisallowedException</span></span>](./esentnullkeydisallowedexception-class.md)  
            [<span data-ttu-id="20521-233">EsentOneDatabasePerSessionException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-233">Microsoft.Isam.Esent.Interop.EsentOneDatabasePerSessionException</span></span>](./esentonedatabasepersessionexception-class.md)  
            [<span data-ttu-id="20521-234">EsentOSSnapshotInvalidSequenceException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-234">Microsoft.Isam.Esent.Interop.EsentOSSnapshotInvalidSequenceException</span></span>](./esentossnapshotinvalidsequenceexception-class.md)  
            [<span data-ttu-id="20521-235">EsentOSSnapshotInvalidSnapIdException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-235">Microsoft.Isam.Esent.Interop.EsentOSSnapshotInvalidSnapIdException</span></span>](./esentossnapshotinvalidsnapidexception-class.md)  
            [<span data-ttu-id="20521-236">EsentPartiallyAttachedDBException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-236">Microsoft.Isam.Esent.Interop.EsentPartiallyAttachedDBException</span></span>](./esentpartiallyattacheddbexception-class.md)  
            [<span data-ttu-id="20521-237">EsentPermissionDeniedException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-237">Microsoft.Isam.Esent.Interop.EsentPermissionDeniedException</span></span>](./esentpermissiondeniedexception-class.md)  
            [<span data-ttu-id="20521-238">EsentQueryNotSupportedException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-238">Microsoft.Isam.Esent.Interop.EsentQueryNotSupportedException</span></span>](./esentquerynotsupportedexception-class.md)  
            [<span data-ttu-id="20521-239">EsentRecordNoCopyException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-239">Microsoft.Isam.Esent.Interop.EsentRecordNoCopyException</span></span>](./esentrecordnocopyexception-class.md)  
            [<span data-ttu-id="20521-240">EsentRecordPrimaryChangedException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-240">Microsoft.Isam.Esent.Interop.EsentRecordPrimaryChangedException</span></span>](./esentrecordprimarychangedexception-class.md)  
            [<span data-ttu-id="20521-241">EsentRestoreOfNonBackupDatabaseException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-241">Microsoft.Isam.Esent.Interop.EsentRestoreOfNonBackupDatabaseException</span></span>](./esentrestoreofnonbackupdatabaseexception-class.md)  
            [<span data-ttu-id="20521-242">EsentRunningInMultiInstanceModeException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-242">Microsoft.Isam.Esent.Interop.EsentRunningInMultiInstanceModeException</span></span>](./esentrunninginmultiinstancemodeexception-class.md)  
            [<span data-ttu-id="20521-243">EsentRunningInOneInstanceModeException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-243">Microsoft.Isam.Esent.Interop.EsentRunningInOneInstanceModeException</span></span>](./esentrunninginoneinstancemodeexception-class.md)  
            [<span data-ttu-id="20521-244">EsentSesidTableIdMismatchException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-244">Microsoft.Isam.Esent.Interop.EsentSesidTableIdMismatchException</span></span>](./esentsesidtableidmismatchexception-class.md)  
            [<span data-ttu-id="20521-245">EsentSessionCoNtextAlreadySetException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-245">Microsoft.Isam.Esent.Interop.EsentSessionContextAlreadySetException</span></span>](./esentsessioncontextalreadysetexception-class.md)  
            [<span data-ttu-id="20521-246">EsentSessionCoNtextNotSetByThisThreadException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-246">Microsoft.Isam.Esent.Interop.EsentSessionContextNotSetByThisThreadException</span></span>](./esentsessioncontextnotsetbythisthreadexception-class.md)  
            [<span data-ttu-id="20521-247">EsentSessionInUseException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-247">Microsoft.Isam.Esent.Interop.EsentSessionInUseException</span></span>](./esentsessioninuseexception-class.md)  
            [<span data-ttu-id="20521-248">EsentSessionSharingViolationException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-248">Microsoft.Isam.Esent.Interop.EsentSessionSharingViolationException</span></span>](./esentsessionsharingviolationexception-class.md)  
            [<span data-ttu-id="20521-249">EsentSessionWriteConflictException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-249">Microsoft.Isam.Esent.Interop.EsentSessionWriteConflictException</span></span>](./esentsessionwriteconflictexception-class.md)  
            [<span data-ttu-id="20521-250">EsentSoftRecoveryOnBackupDatabaseException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-250">Microsoft.Isam.Esent.Interop.EsentSoftRecoveryOnBackupDatabaseException</span></span>](./esentsoftrecoveryonbackupdatabaseexception-class.md)  
            [<span data-ttu-id="20521-251">EsentSpaceHintsInvalidException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-251">Microsoft.Isam.Esent.Interop.EsentSpaceHintsInvalidException</span></span>](./esentspacehintsinvalidexception-class.md)  
            [<span data-ttu-id="20521-252">EsentSystemParamsAlreadySetException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-252">Microsoft.Isam.Esent.Interop.EsentSystemParamsAlreadySetException</span></span>](./esentsystemparamsalreadysetexception-class.md)  
            [<span data-ttu-id="20521-253">EsentSystemPathInUseException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-253">Microsoft.Isam.Esent.Interop.EsentSystemPathInUseException</span></span>](./esentsystempathinuseexception-class.md)  
            [<span data-ttu-id="20521-254">EsentTableLockedException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-254">Microsoft.Isam.Esent.Interop.EsentTableLockedException</span></span>](./esenttablelockedexception-class.md)  
            [<span data-ttu-id="20521-255">EsentTableNotEmptyException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-255">Microsoft.Isam.Esent.Interop.EsentTableNotEmptyException</span></span>](./esenttablenotemptyexception-class.md)  
            [<span data-ttu-id="20521-256">EsentTempPathInUseException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-256">Microsoft.Isam.Esent.Interop.EsentTempPathInUseException</span></span>](./esenttemppathinuseexception-class.md)  
            [<span data-ttu-id="20521-257">EsentTooManyActiveUsersException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-257">Microsoft.Isam.Esent.Interop.EsentTooManyActiveUsersException</span></span>](./esenttoomanyactiveusersexception-class.md)  
            [<span data-ttu-id="20521-258">EsentTooManyAttachedDatabasesException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-258">Microsoft.Isam.Esent.Interop.EsentTooManyAttachedDatabasesException</span></span>](./esenttoomanyattacheddatabasesexception-class.md)  
            [<span data-ttu-id="20521-259">EsentTooManyColumnsException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-259">Microsoft.Isam.Esent.Interop.EsentTooManyColumnsException</span></span>](./esenttoomanycolumnsexception-class.md)  
            [<span data-ttu-id="20521-260">EsentTooManyIndexesException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-260">Microsoft.Isam.Esent.Interop.EsentTooManyIndexesException</span></span>](./esenttoomanyindexesexception-class.md)  
            [<span data-ttu-id="20521-261">EsentTooManyKeysException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-261">Microsoft.Isam.Esent.Interop.EsentTooManyKeysException</span></span>](./esenttoomanykeysexception-class.md)  
            [<span data-ttu-id="20521-262">EsentTooManyOpenTablesAndCleanupTimedOutException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-262">Microsoft.Isam.Esent.Interop.EsentTooManyOpenTablesAndCleanupTimedOutException</span></span>](./esenttoomanyopentablesandcleanuptimedoutexception-class.md)  
            [<span data-ttu-id="20521-263">EsentTooManyTestInjectionsException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-263">Microsoft.Isam.Esent.Interop.EsentTooManyTestInjectionsException</span></span>](./esenttoomanytestinjectionsexception-class.md)  
            [<span data-ttu-id="20521-264">EsentTransReadOnlyException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-264">Microsoft.Isam.Esent.Interop.EsentTransReadOnlyException</span></span>](./esenttransreadonlyexception-class.md)  
            [<span data-ttu-id="20521-265">EsentTransTooDeepException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-265">Microsoft.Isam.Esent.Interop.EsentTransTooDeepException</span></span>](./esenttranstoodeepexception-class.md)  
            [<span data-ttu-id="20521-266">EsentUnicodeNormalizationNotSupportedException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-266">Microsoft.Isam.Esent.Interop.EsentUnicodeNormalizationNotSupportedException</span></span>](./esentunicodenormalizationnotsupportedexception-class.md)  
            [<span data-ttu-id="20521-267">EsentUpdateMustVersionException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-267">Microsoft.Isam.Esent.Interop.EsentUpdateMustVersionException</span></span>](./esentupdatemustversionexception-class.md)  
            [<span data-ttu-id="20521-268">EsentUpdateNotPreparedException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-268">Microsoft.Isam.Esent.Interop.EsentUpdateNotPreparedException</span></span>](./esentupdatenotpreparedexception-class.md)  
            [<span data-ttu-id="20521-269">EsentVersionStoreOutOfMemoryAndCleanupTimedOutException （.）</span><span class="sxs-lookup"><span data-stu-id="20521-269">Microsoft.Isam.Esent.Interop.EsentVersionStoreOutOfMemoryAndCleanupTimedOutException</span></span>](./esentversionstoreoutofmemoryandcleanuptimedoutexception-class.md)
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
# <a name="esentusageexception-class"></a><span data-ttu-id="5c5ba-103">EsentUsageException 類別</span><span class="sxs-lookup"><span data-stu-id="5c5ba-103">EsentUsageException class</span></span>

<span data-ttu-id="5c5ba-104">使用例外狀況的基類。</span><span class="sxs-lookup"><span data-stu-id="5c5ba-104">Base class for Usage exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="5c5ba-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="5c5ba-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="5c5ba-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="5c5ba-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="5c5ba-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="5c5ba-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="5c5ba-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="5c5ba-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="5c5ba-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="5c5ba-110">EsentApiException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          <span data-ttu-id="5c5ba-111">EsentUsageException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>  
            

<span data-ttu-id="5c5ba-112">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5c5ba-112">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5c5ba-113">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="5c5ba-113">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5c5ba-114">Syntax</span><span class="sxs-lookup"><span data-stu-id="5c5ba-114">Syntax</span></span>

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

## <a name="thread-safety"></a><span data-ttu-id="5c5ba-115">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="5c5ba-115">Thread safety</span></span>

<span data-ttu-id="5c5ba-116">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="5c5ba-116">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="5c5ba-117">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="5c5ba-117">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="5c5ba-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5c5ba-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5c5ba-119">參考</span><span class="sxs-lookup"><span data-stu-id="5c5ba-119">Reference</span></span>

[<span data-ttu-id="5c5ba-120">EsentUsageException 成員</span><span class="sxs-lookup"><span data-stu-id="5c5ba-120">EsentUsageException members</span></span>](./esentusageexception-members.md)

[<span data-ttu-id="5c5ba-121">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="5c5ba-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a><span data-ttu-id="5c5ba-122">衍生類型</span><span class="sxs-lookup"><span data-stu-id="5c5ba-122">Derived types</span></span>

[<span data-ttu-id="5c5ba-123">System.Object</span><span class="sxs-lookup"><span data-stu-id="5c5ba-123">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="5c5ba-124">System.Exception</span><span class="sxs-lookup"><span data-stu-id="5c5ba-124">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="5c5ba-125">EsentException。</span><span class="sxs-lookup"><span data-stu-id="5c5ba-125">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="5c5ba-126">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-126">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="5c5ba-127">EsentApiException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-127">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          <span data-ttu-id="5c5ba-128">EsentUsageException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-128">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>  
            [<span data-ttu-id="5c5ba-129">EsentAfterInitializationException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-129">Microsoft.Isam.Esent.Interop.EsentAfterInitializationException</span></span>](./esentafterinitializationexception-class.md)  
            [<span data-ttu-id="5c5ba-130">EsentAlreadyInitializedException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-130">Microsoft.Isam.Esent.Interop.EsentAlreadyInitializedException</span></span>](./esentalreadyinitializedexception-class.md)  
            [<span data-ttu-id="5c5ba-131">EsentAlreadyPreparedException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-131">Microsoft.Isam.Esent.Interop.EsentAlreadyPreparedException</span></span>](./esentalreadypreparedexception-class.md)  
            [<span data-ttu-id="5c5ba-132">EsentBackupDirectoryNotEmptyException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-132">Microsoft.Isam.Esent.Interop.EsentBackupDirectoryNotEmptyException</span></span>](./esentbackupdirectorynotemptyexception-class.md)  
            [<span data-ttu-id="5c5ba-133">EsentBadColumnIdException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-133">Microsoft.Isam.Esent.Interop.EsentBadColumnIdException</span></span>](./esentbadcolumnidexception-class.md)  
            [<span data-ttu-id="5c5ba-134">EsentBadRestoreTargetInstanceException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-134">Microsoft.Isam.Esent.Interop.EsentBadRestoreTargetInstanceException</span></span>](./esentbadrestoretargetinstanceexception-class.md)  
            [<span data-ttu-id="5c5ba-135">EsentCallbackNotResolvedException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-135">Microsoft.Isam.Esent.Interop.EsentCallbackNotResolvedException</span></span>](./esentcallbacknotresolvedexception-class.md)  
            [<span data-ttu-id="5c5ba-136">EsentCannotBeTaggedException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-136">Microsoft.Isam.Esent.Interop.EsentCannotBeTaggedException</span></span>](./esentcannotbetaggedexception-class.md)  
            [<span data-ttu-id="5c5ba-137">EsentCannotDeleteSystemTableException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-137">Microsoft.Isam.Esent.Interop.EsentCannotDeleteSystemTableException</span></span>](./esentcannotdeletesystemtableexception-class.md)  
            [<span data-ttu-id="5c5ba-138">EsentCannotDeleteTemplateTableException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-138">Microsoft.Isam.Esent.Interop.EsentCannotDeleteTemplateTableException</span></span>](./esentcannotdeletetemplatetableexception-class.md)  
            [<span data-ttu-id="5c5ba-139">EsentCannotDeleteTempTableException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-139">Microsoft.Isam.Esent.Interop.EsentCannotDeleteTempTableException</span></span>](./esentcannotdeletetemptableexception-class.md)  
            [<span data-ttu-id="5c5ba-140">EsentCannotDisableVersioningException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-140">Microsoft.Isam.Esent.Interop.EsentCannotDisableVersioningException</span></span>](./esentcannotdisableversioningexception-class.md)  
            [<span data-ttu-id="5c5ba-141">EsentCannotIndexException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-141">Microsoft.Isam.Esent.Interop.EsentCannotIndexException</span></span>](./esentcannotindexexception-class.md)  
            [<span data-ttu-id="5c5ba-142">EsentCannotMaterializeForwardOnlySortException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-142">Microsoft.Isam.Esent.Interop.EsentCannotMaterializeForwardOnlySortException</span></span>](./esentcannotmaterializeforwardonlysortexception-class.md)  
            [<span data-ttu-id="5c5ba-143">EsentCannotNestDDLException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-143">Microsoft.Isam.Esent.Interop.EsentCannotNestDDLException</span></span>](./esentcannotnestddlexception-class.md)  
            [<span data-ttu-id="5c5ba-144">EsentCannotSeparateIntrinsicLVException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-144">Microsoft.Isam.Esent.Interop.EsentCannotSeparateIntrinsicLVException</span></span>](./esentcannotseparateintrinsiclvexception-class.md)  
            [<span data-ttu-id="5c5ba-145">EsentColumnCannotBeCompressedException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-145">Microsoft.Isam.Esent.Interop.EsentColumnCannotBeCompressedException</span></span>](./esentcolumncannotbecompressedexception-class.md)  
            [<span data-ttu-id="5c5ba-146">EsentColumnDoesNotFitException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-146">Microsoft.Isam.Esent.Interop.EsentColumnDoesNotFitException</span></span>](./esentcolumndoesnotfitexception-class.md)  
            [<span data-ttu-id="5c5ba-147">EsentColumnDuplicateException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-147">Microsoft.Isam.Esent.Interop.EsentColumnDuplicateException</span></span>](./esentcolumnduplicateexception-class.md)  
            [<span data-ttu-id="5c5ba-148">EsentColumnInUseException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-148">Microsoft.Isam.Esent.Interop.EsentColumnInUseException</span></span>](./esentcolumninuseexception-class.md)  
            [<span data-ttu-id="5c5ba-149">EsentColumnNoChunkException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-149">Microsoft.Isam.Esent.Interop.EsentColumnNoChunkException</span></span>](./esentcolumnnochunkexception-class.md)  
            [<span data-ttu-id="5c5ba-150">EsentColumnNotFoundException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-150">Microsoft.Isam.Esent.Interop.EsentColumnNotFoundException</span></span>](./esentcolumnnotfoundexception-class.md)  
            [<span data-ttu-id="5c5ba-151">EsentColumnNotUpdatableException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-151">Microsoft.Isam.Esent.Interop.EsentColumnNotUpdatableException</span></span>](./esentcolumnnotupdatableexception-class.md)  
            [<span data-ttu-id="5c5ba-152">EsentColumnRedundantException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-152">Microsoft.Isam.Esent.Interop.EsentColumnRedundantException</span></span>](./esentcolumnredundantexception-class.md)  
            [<span data-ttu-id="5c5ba-153">EsentColumnTooBigException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-153">Microsoft.Isam.Esent.Interop.EsentColumnTooBigException</span></span>](./esentcolumntoobigexception-class.md)  
            [<span data-ttu-id="5c5ba-154">EsentDatabaseAlreadyRunningMaintenanceException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-154">Microsoft.Isam.Esent.Interop.EsentDatabaseAlreadyRunningMaintenanceException</span></span>](./esentdatabasealreadyrunningmaintenanceexception-class.md)  
            [<span data-ttu-id="5c5ba-155">EsentDatabaseCorruptedNoRepairException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-155">Microsoft.Isam.Esent.Interop.EsentDatabaseCorruptedNoRepairException</span></span>](./esentdatabasecorruptednorepairexception-class.md)  
            [<span data-ttu-id="5c5ba-156">EsentDatabaseDuplicateException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-156">Microsoft.Isam.Esent.Interop.EsentDatabaseDuplicateException</span></span>](./esentdatabaseduplicateexception-class.md)  
            [<span data-ttu-id="5c5ba-157">EsentDatabaseFileReadOnlyException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-157">Microsoft.Isam.Esent.Interop.EsentDatabaseFileReadOnlyException</span></span>](./esentdatabasefilereadonlyexception-class.md)  
            [<span data-ttu-id="5c5ba-158">EsentDatabaseInUseException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-158">Microsoft.Isam.Esent.Interop.EsentDatabaseInUseException</span></span>](./esentdatabaseinuseexception-class.md)  
            [<span data-ttu-id="5c5ba-159">EsentDatabaseInvalidIncrementalReseedException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-159">Microsoft.Isam.Esent.Interop.EsentDatabaseInvalidIncrementalReseedException</span></span>](./esentdatabaseinvalidincrementalreseedexception-class.md)  
            [<span data-ttu-id="5c5ba-160">EsentDatabaseInvalidNameException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-160">Microsoft.Isam.Esent.Interop.EsentDatabaseInvalidNameException</span></span>](./esentdatabaseinvalidnameexception-class.md)  
            [<span data-ttu-id="5c5ba-161">EsentDatabaseInvalidPagesException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-161">Microsoft.Isam.Esent.Interop.EsentDatabaseInvalidPagesException</span></span>](./esentdatabaseinvalidpagesexception-class.md)  
            [<span data-ttu-id="5c5ba-162">EsentDatabaseInvalidPathException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-162">Microsoft.Isam.Esent.Interop.EsentDatabaseInvalidPathException</span></span>](./esentdatabaseinvalidpathexception-class.md)  
            [<span data-ttu-id="5c5ba-163">EsentDatabaseLockedException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-163">Microsoft.Isam.Esent.Interop.EsentDatabaseLockedException</span></span>](./esentdatabaselockedexception-class.md)  
            [<span data-ttu-id="5c5ba-164">EsentDatabaseNotFoundException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-164">Microsoft.Isam.Esent.Interop.EsentDatabaseNotFoundException</span></span>](./esentdatabasenotfoundexception-class.md)  
            [<span data-ttu-id="5c5ba-165">EsentDatabaseSharingViolationException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-165">Microsoft.Isam.Esent.Interop.EsentDatabaseSharingViolationException</span></span>](./esentdatabasesharingviolationexception-class.md)  
            [<span data-ttu-id="5c5ba-166">EsentDatabaseSignInUseException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-166">Microsoft.Isam.Esent.Interop.EsentDatabaseSignInUseException</span></span>](./esentdatabasesigninuseexception-class.md)  
            [<span data-ttu-id="5c5ba-167">EsentDDLNotInheritableException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-167">Microsoft.Isam.Esent.Interop.EsentDDLNotInheritableException</span></span>](./esentddlnotinheritableexception-class.md)  
            [<span data-ttu-id="5c5ba-168">EsentDefaultValueTooBigException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-168">Microsoft.Isam.Esent.Interop.EsentDefaultValueTooBigException</span></span>](./esentdefaultvaluetoobigexception-class.md)  
            [<span data-ttu-id="5c5ba-169">EsentDensityInvalidException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-169">Microsoft.Isam.Esent.Interop.EsentDensityInvalidException</span></span>](./esentdensityinvalidexception-class.md)  
            [<span data-ttu-id="5c5ba-170">EsentDisabledFunctionalityException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-170">Microsoft.Isam.Esent.Interop.EsentDisabledFunctionalityException</span></span>](./esentdisabledfunctionalityexception-class.md)  
            [<span data-ttu-id="5c5ba-171">EsentEntryPointNotFoundException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-171">Microsoft.Isam.Esent.Interop.EsentEntryPointNotFoundException</span></span>](./esententrypointnotfoundexception-class.md)  
            [<span data-ttu-id="5c5ba-172">EsentExclusiveTableLockRequiredException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-172">Microsoft.Isam.Esent.Interop.EsentExclusiveTableLockRequiredException</span></span>](./esentexclusivetablelockrequiredexception-class.md)  
            [<span data-ttu-id="5c5ba-173">EsentFeatureNotAvailableException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-173">Microsoft.Isam.Esent.Interop.EsentFeatureNotAvailableException</span></span>](./esentfeaturenotavailableexception-class.md)  
            [<span data-ttu-id="5c5ba-174">EsentFileCompressedException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-174">Microsoft.Isam.Esent.Interop.EsentFileCompressedException</span></span>](./esentfilecompressedexception-class.md)  
            [<span data-ttu-id="5c5ba-175">EsentFilteredMoveNotSupportedException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-175">Microsoft.Isam.Esent.Interop.EsentFilteredMoveNotSupportedException</span></span>](./esentfilteredmovenotsupportedexception-class.md)  
            [<span data-ttu-id="5c5ba-176">EsentFixedDDLException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-176">Microsoft.Isam.Esent.Interop.EsentFixedDDLException</span></span>](./esentfixedddlexception-class.md)  
            [<span data-ttu-id="5c5ba-177">EsentFixedInheritedDDLException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-177">Microsoft.Isam.Esent.Interop.EsentFixedInheritedDDLException</span></span>](./esentfixedinheritedddlexception-class.md)  
            [<span data-ttu-id="5c5ba-178">EsentForceDetachNotAllowedException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-178">Microsoft.Isam.Esent.Interop.EsentForceDetachNotAllowedException</span></span>](./esentforcedetachnotallowedexception-class.md)  
            [<span data-ttu-id="5c5ba-179">EsentIllegalOperationException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-179">Microsoft.Isam.Esent.Interop.EsentIllegalOperationException</span></span>](./esentillegaloperationexception-class.md)  
            [<span data-ttu-id="5c5ba-180">EsentIndexDuplicateException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-180">Microsoft.Isam.Esent.Interop.EsentIndexDuplicateException</span></span>](./esentindexduplicateexception-class.md)  
            [<span data-ttu-id="5c5ba-181">EsentIndexHasPrimaryException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-181">Microsoft.Isam.Esent.Interop.EsentIndexHasPrimaryException</span></span>](./esentindexhasprimaryexception-class.md)  
            [<span data-ttu-id="5c5ba-182">EsentIndexInvalidDefException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-182">Microsoft.Isam.Esent.Interop.EsentIndexInvalidDefException</span></span>](./esentindexinvaliddefexception-class.md)  
            [<span data-ttu-id="5c5ba-183">EsentIndexMustStayException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-183">Microsoft.Isam.Esent.Interop.EsentIndexMustStayException</span></span>](./esentindexmuststayexception-class.md)  
            [<span data-ttu-id="5c5ba-184">EsentIndexTuplesCannotRetrieveFromIndexException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-184">Microsoft.Isam.Esent.Interop.EsentIndexTuplesCannotRetrieveFromIndexException</span></span>](./esentindextuplescannotretrievefromindexexception-class.md)  
            [<span data-ttu-id="5c5ba-185">EsentIndexTuplesInvalidLimitsException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-185">Microsoft.Isam.Esent.Interop.EsentIndexTuplesInvalidLimitsException</span></span>](./esentindextuplesinvalidlimitsexception-class.md)  
            [<span data-ttu-id="5c5ba-186">EsentIndexTuplesKeyTooSmallException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-186">Microsoft.Isam.Esent.Interop.EsentIndexTuplesKeyTooSmallException</span></span>](./esentindextupleskeytoosmallexception-class.md)  
            [<span data-ttu-id="5c5ba-187">EsentIndexTuplesNonUniqueOnlyException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-187">Microsoft.Isam.Esent.Interop.EsentIndexTuplesNonUniqueOnlyException</span></span>](./esentindextuplesnonuniqueonlyexception-class.md)  
            [<span data-ttu-id="5c5ba-188">EsentIndexTuplesSecondaryIndexOnlyException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-188">Microsoft.Isam.Esent.Interop.EsentIndexTuplesSecondaryIndexOnlyException</span></span>](./esentindextuplessecondaryindexonlyexception-class.md)  
            [<span data-ttu-id="5c5ba-189">EsentIndexTuplesTextBinaryColumnsOnlyException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-189">Microsoft.Isam.Esent.Interop.EsentIndexTuplesTextBinaryColumnsOnlyException</span></span>](./esentindextuplestextbinarycolumnsonlyexception-class.md)  
            [<span data-ttu-id="5c5ba-190">EsentIndexTuplesVarSegMacNotAllowedException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-190">Microsoft.Isam.Esent.Interop.EsentIndexTuplesVarSegMacNotAllowedException</span></span>](./esentindextuplesvarsegmacnotallowedexception-class.md)  
            [<span data-ttu-id="5c5ba-191">EsentInstanceNameInUseException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-191">Microsoft.Isam.Esent.Interop.EsentInstanceNameInUseException</span></span>](./esentinstancenameinuseexception-class.md)  
            [<span data-ttu-id="5c5ba-192">EsentInTransactionException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-192">Microsoft.Isam.Esent.Interop.EsentInTransactionException</span></span>](./esentintransactionexception-class.md)  
            [<span data-ttu-id="5c5ba-193">EsentInvalidBackupException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-193">Microsoft.Isam.Esent.Interop.EsentInvalidBackupException</span></span>](./esentinvalidbackupexception-class.md)  
            [<span data-ttu-id="5c5ba-194">EsentInvalidBackupSequenceException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-194">Microsoft.Isam.Esent.Interop.EsentInvalidBackupSequenceException</span></span>](./esentinvalidbackupsequenceexception-class.md)  
            [<span data-ttu-id="5c5ba-195">EsentInvalidBookmarkException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-195">Microsoft.Isam.Esent.Interop.EsentInvalidBookmarkException</span></span>](./esentinvalidbookmarkexception-class.md)  
            [<span data-ttu-id="5c5ba-196">EsentInvalidCodePageException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-196">Microsoft.Isam.Esent.Interop.EsentInvalidCodePageException</span></span>](./esentinvalidcodepageexception-class.md)  
            [<span data-ttu-id="5c5ba-197">EsentInvalidColumnTypeException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-197">Microsoft.Isam.Esent.Interop.EsentInvalidColumnTypeException</span></span>](./esentinvalidcolumntypeexception-class.md)  
            [<span data-ttu-id="5c5ba-198">EsentInvalidCreateIndexException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-198">Microsoft.Isam.Esent.Interop.EsentInvalidCreateIndexException</span></span>](./esentinvalidcreateindexexception-class.md)  
            [<span data-ttu-id="5c5ba-199">EsentInvalidDatabaseException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-199">Microsoft.Isam.Esent.Interop.EsentInvalidDatabaseException</span></span>](./esentinvaliddatabaseexception-class.md)  
            [<span data-ttu-id="5c5ba-200">EsentInvalidDatabaseIdException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-200">Microsoft.Isam.Esent.Interop.EsentInvalidDatabaseIdException</span></span>](./esentinvaliddatabaseidexception-class.md)  
            [<span data-ttu-id="5c5ba-201">EsentInvalidGrbitException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-201">Microsoft.Isam.Esent.Interop.EsentInvalidGrbitException</span></span>](./esentinvalidgrbitexception-class.md)  
            [<span data-ttu-id="5c5ba-202">EsentInvalidIndexIdException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-202">Microsoft.Isam.Esent.Interop.EsentInvalidIndexIdException</span></span>](./esentinvalidindexidexception-class.md)  
            [<span data-ttu-id="5c5ba-203">EsentInvalidInstanceException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-203">Microsoft.Isam.Esent.Interop.EsentInvalidInstanceException</span></span>](./esentinvalidinstanceexception-class.md)  
            [<span data-ttu-id="5c5ba-204">EsentInvalidLanguageIdException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-204">Microsoft.Isam.Esent.Interop.EsentInvalidLanguageIdException</span></span>](./esentinvalidlanguageidexception-class.md)  
            [<span data-ttu-id="5c5ba-205">EsentInvalidLCMapStringFlagsException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-205">Microsoft.Isam.Esent.Interop.EsentInvalidLCMapStringFlagsException</span></span>](./esentinvalidlcmapstringflagsexception-class.md)  
            [<span data-ttu-id="5c5ba-206">EsentInvalidNameException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-206">Microsoft.Isam.Esent.Interop.EsentInvalidNameException</span></span>](./esentinvalidnameexception-class.md)  
            [<span data-ttu-id="5c5ba-207">EsentInvalidOperationException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-207">Microsoft.Isam.Esent.Interop.EsentInvalidOperationException</span></span>](./esentinvalidoperationexception-class.md)  
            [<span data-ttu-id="5c5ba-208">EsentInvalidParameterException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-208">Microsoft.Isam.Esent.Interop.EsentInvalidParameterException</span></span>](./esentinvalidparameterexception-class.md)  
            [<span data-ttu-id="5c5ba-209">EsentInvalidPathException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-209">Microsoft.Isam.Esent.Interop.EsentInvalidPathException</span></span>](./esentinvalidpathexception-class.md)  
            [<span data-ttu-id="5c5ba-210">EsentInvalidPlaceholderColumnException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-210">Microsoft.Isam.Esent.Interop.EsentInvalidPlaceholderColumnException</span></span>](./esentinvalidplaceholdercolumnexception-class.md)  
            [<span data-ttu-id="5c5ba-211">EsentInvalidPrereadException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-211">Microsoft.Isam.Esent.Interop.EsentInvalidPrereadException</span></span>](./esentinvalidprereadexception-class.md)  
            [<span data-ttu-id="5c5ba-212">EsentInvalidSesidException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-212">Microsoft.Isam.Esent.Interop.EsentInvalidSesidException</span></span>](./esentinvalidsesidexception-class.md)  
            [<span data-ttu-id="5c5ba-213">EsentInvalidSettingsException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-213">Microsoft.Isam.Esent.Interop.EsentInvalidSettingsException</span></span>](./esentinvalidsettingsexception-class.md)  
            [<span data-ttu-id="5c5ba-214">EsentInvalidTableIdException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-214">Microsoft.Isam.Esent.Interop.EsentInvalidTableIdException</span></span>](./esentinvalidtableidexception-class.md)  
            [<span data-ttu-id="5c5ba-215">EsentKeyIsMadeException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-215">Microsoft.Isam.Esent.Interop.EsentKeyIsMadeException</span></span>](./esentkeyismadeexception-class.md)  
            [<span data-ttu-id="5c5ba-216">EsentKeyNotMadeException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-216">Microsoft.Isam.Esent.Interop.EsentKeyNotMadeException</span></span>](./esentkeynotmadeexception-class.md)  
            [<span data-ttu-id="5c5ba-217">EsentLogFileNotCopiedException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-217">Microsoft.Isam.Esent.Interop.EsentLogFileNotCopiedException</span></span>](./esentlogfilenotcopiedexception-class.md)  
            [<span data-ttu-id="5c5ba-218">EsentLogFilePathInUseException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-218">Microsoft.Isam.Esent.Interop.EsentLogFilePathInUseException</span></span>](./esentlogfilepathinuseexception-class.md)  
            [<span data-ttu-id="5c5ba-219">EsentLogFileSizeMismatchException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-219">Microsoft.Isam.Esent.Interop.EsentLogFileSizeMismatchException</span></span>](./esentlogfilesizemismatchexception-class.md)  
            [<span data-ttu-id="5c5ba-220">EsentLoggingDisabledException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-220">Microsoft.Isam.Esent.Interop.EsentLoggingDisabledException</span></span>](./esentloggingdisabledexception-class.md)  
            [<span data-ttu-id="5c5ba-221">EsentLSAlreadySetException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-221">Microsoft.Isam.Esent.Interop.EsentLSAlreadySetException</span></span>](./esentlsalreadysetexception-class.md)  
            [<span data-ttu-id="5c5ba-222">EsentLSCallbackNotSpecifiedException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-222">Microsoft.Isam.Esent.Interop.EsentLSCallbackNotSpecifiedException</span></span>](./esentlscallbacknotspecifiedexception-class.md)  
            [<span data-ttu-id="5c5ba-223">EsentMultiValuedColumnMustBeTaggedException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-223">Microsoft.Isam.Esent.Interop.EsentMultiValuedColumnMustBeTaggedException</span></span>](./esentmultivaluedcolumnmustbetaggedexception-class.md)  
            [<span data-ttu-id="5c5ba-224">EsentMultiValuedIndexViolationException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-224">Microsoft.Isam.Esent.Interop.EsentMultiValuedIndexViolationException</span></span>](./esentmultivaluedindexviolationexception-class.md)  
            [<span data-ttu-id="5c5ba-225">EsentMustBeSeparateLongValueException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-225">Microsoft.Isam.Esent.Interop.EsentMustBeSeparateLongValueException</span></span>](./esentmustbeseparatelongvalueexception-class.md)  
            [<span data-ttu-id="5c5ba-226">EsentMustRollbackException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-226">Microsoft.Isam.Esent.Interop.EsentMustRollbackException</span></span>](./esentmustrollbackexception-class.md)  
            [<span data-ttu-id="5c5ba-227">EsentNoBackupDirectoryException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-227">Microsoft.Isam.Esent.Interop.EsentNoBackupDirectoryException</span></span>](./esentnobackupdirectoryexception-class.md)  
            [<span data-ttu-id="5c5ba-228">EsentNoCurrentIndexException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-228">Microsoft.Isam.Esent.Interop.EsentNoCurrentIndexException</span></span>](./esentnocurrentindexexception-class.md)  
            [<span data-ttu-id="5c5ba-229">EsentNotInitializedException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-229">Microsoft.Isam.Esent.Interop.EsentNotInitializedException</span></span>](./esentnotinitializedexception-class.md)  
            [<span data-ttu-id="5c5ba-230">EsentNotInTransactionException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-230">Microsoft.Isam.Esent.Interop.EsentNotInTransactionException</span></span>](./esentnotintransactionexception-class.md)  
            [<span data-ttu-id="5c5ba-231">EsentNullInvalidException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-231">Microsoft.Isam.Esent.Interop.EsentNullInvalidException</span></span>](./esentnullinvalidexception-class.md)  
            [<span data-ttu-id="5c5ba-232">EsentNullKeyDisallowedException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-232">Microsoft.Isam.Esent.Interop.EsentNullKeyDisallowedException</span></span>](./esentnullkeydisallowedexception-class.md)  
            [<span data-ttu-id="5c5ba-233">EsentOneDatabasePerSessionException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-233">Microsoft.Isam.Esent.Interop.EsentOneDatabasePerSessionException</span></span>](./esentonedatabasepersessionexception-class.md)  
            [<span data-ttu-id="5c5ba-234">EsentOSSnapshotInvalidSequenceException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-234">Microsoft.Isam.Esent.Interop.EsentOSSnapshotInvalidSequenceException</span></span>](./esentossnapshotinvalidsequenceexception-class.md)  
            [<span data-ttu-id="5c5ba-235">EsentOSSnapshotInvalidSnapIdException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-235">Microsoft.Isam.Esent.Interop.EsentOSSnapshotInvalidSnapIdException</span></span>](./esentossnapshotinvalidsnapidexception-class.md)  
            [<span data-ttu-id="5c5ba-236">EsentPartiallyAttachedDBException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-236">Microsoft.Isam.Esent.Interop.EsentPartiallyAttachedDBException</span></span>](./esentpartiallyattacheddbexception-class.md)  
            [<span data-ttu-id="5c5ba-237">EsentPermissionDeniedException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-237">Microsoft.Isam.Esent.Interop.EsentPermissionDeniedException</span></span>](./esentpermissiondeniedexception-class.md)  
            [<span data-ttu-id="5c5ba-238">EsentQueryNotSupportedException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-238">Microsoft.Isam.Esent.Interop.EsentQueryNotSupportedException</span></span>](./esentquerynotsupportedexception-class.md)  
            [<span data-ttu-id="5c5ba-239">EsentRecordNoCopyException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-239">Microsoft.Isam.Esent.Interop.EsentRecordNoCopyException</span></span>](./esentrecordnocopyexception-class.md)  
            [<span data-ttu-id="5c5ba-240">EsentRecordPrimaryChangedException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-240">Microsoft.Isam.Esent.Interop.EsentRecordPrimaryChangedException</span></span>](./esentrecordprimarychangedexception-class.md)  
            [<span data-ttu-id="5c5ba-241">EsentRestoreOfNonBackupDatabaseException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-241">Microsoft.Isam.Esent.Interop.EsentRestoreOfNonBackupDatabaseException</span></span>](./esentrestoreofnonbackupdatabaseexception-class.md)  
            [<span data-ttu-id="5c5ba-242">EsentRunningInMultiInstanceModeException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-242">Microsoft.Isam.Esent.Interop.EsentRunningInMultiInstanceModeException</span></span>](./esentrunninginmultiinstancemodeexception-class.md)  
            [<span data-ttu-id="5c5ba-243">EsentRunningInOneInstanceModeException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-243">Microsoft.Isam.Esent.Interop.EsentRunningInOneInstanceModeException</span></span>](./esentrunninginoneinstancemodeexception-class.md)  
            [<span data-ttu-id="5c5ba-244">EsentSesidTableIdMismatchException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-244">Microsoft.Isam.Esent.Interop.EsentSesidTableIdMismatchException</span></span>](./esentsesidtableidmismatchexception-class.md)  
            [<span data-ttu-id="5c5ba-245">EsentSessionCoNtextAlreadySetException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-245">Microsoft.Isam.Esent.Interop.EsentSessionContextAlreadySetException</span></span>](./esentsessioncontextalreadysetexception-class.md)  
            [<span data-ttu-id="5c5ba-246">EsentSessionCoNtextNotSetByThisThreadException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-246">Microsoft.Isam.Esent.Interop.EsentSessionContextNotSetByThisThreadException</span></span>](./esentsessioncontextnotsetbythisthreadexception-class.md)  
            [<span data-ttu-id="5c5ba-247">EsentSessionInUseException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-247">Microsoft.Isam.Esent.Interop.EsentSessionInUseException</span></span>](./esentsessioninuseexception-class.md)  
            [<span data-ttu-id="5c5ba-248">EsentSessionSharingViolationException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-248">Microsoft.Isam.Esent.Interop.EsentSessionSharingViolationException</span></span>](./esentsessionsharingviolationexception-class.md)  
            [<span data-ttu-id="5c5ba-249">EsentSessionWriteConflictException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-249">Microsoft.Isam.Esent.Interop.EsentSessionWriteConflictException</span></span>](./esentsessionwriteconflictexception-class.md)  
            [<span data-ttu-id="5c5ba-250">EsentSoftRecoveryOnBackupDatabaseException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-250">Microsoft.Isam.Esent.Interop.EsentSoftRecoveryOnBackupDatabaseException</span></span>](./esentsoftrecoveryonbackupdatabaseexception-class.md)  
            [<span data-ttu-id="5c5ba-251">EsentSpaceHintsInvalidException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-251">Microsoft.Isam.Esent.Interop.EsentSpaceHintsInvalidException</span></span>](./esentspacehintsinvalidexception-class.md)  
            [<span data-ttu-id="5c5ba-252">EsentSystemParamsAlreadySetException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-252">Microsoft.Isam.Esent.Interop.EsentSystemParamsAlreadySetException</span></span>](./esentsystemparamsalreadysetexception-class.md)  
            [<span data-ttu-id="5c5ba-253">EsentSystemPathInUseException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-253">Microsoft.Isam.Esent.Interop.EsentSystemPathInUseException</span></span>](./esentsystempathinuseexception-class.md)  
            [<span data-ttu-id="5c5ba-254">EsentTableLockedException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-254">Microsoft.Isam.Esent.Interop.EsentTableLockedException</span></span>](./esenttablelockedexception-class.md)  
            [<span data-ttu-id="5c5ba-255">EsentTableNotEmptyException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-255">Microsoft.Isam.Esent.Interop.EsentTableNotEmptyException</span></span>](./esenttablenotemptyexception-class.md)  
            [<span data-ttu-id="5c5ba-256">EsentTempPathInUseException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-256">Microsoft.Isam.Esent.Interop.EsentTempPathInUseException</span></span>](./esenttemppathinuseexception-class.md)  
            [<span data-ttu-id="5c5ba-257">EsentTooManyActiveUsersException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-257">Microsoft.Isam.Esent.Interop.EsentTooManyActiveUsersException</span></span>](./esenttoomanyactiveusersexception-class.md)  
            [<span data-ttu-id="5c5ba-258">EsentTooManyAttachedDatabasesException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-258">Microsoft.Isam.Esent.Interop.EsentTooManyAttachedDatabasesException</span></span>](./esenttoomanyattacheddatabasesexception-class.md)  
            [<span data-ttu-id="5c5ba-259">EsentTooManyColumnsException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-259">Microsoft.Isam.Esent.Interop.EsentTooManyColumnsException</span></span>](./esenttoomanycolumnsexception-class.md)  
            [<span data-ttu-id="5c5ba-260">EsentTooManyIndexesException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-260">Microsoft.Isam.Esent.Interop.EsentTooManyIndexesException</span></span>](./esenttoomanyindexesexception-class.md)  
            [<span data-ttu-id="5c5ba-261">EsentTooManyKeysException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-261">Microsoft.Isam.Esent.Interop.EsentTooManyKeysException</span></span>](./esenttoomanykeysexception-class.md)  
            [<span data-ttu-id="5c5ba-262">EsentTooManyOpenTablesAndCleanupTimedOutException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-262">Microsoft.Isam.Esent.Interop.EsentTooManyOpenTablesAndCleanupTimedOutException</span></span>](./esenttoomanyopentablesandcleanuptimedoutexception-class.md)  
            [<span data-ttu-id="5c5ba-263">EsentTooManyTestInjectionsException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-263">Microsoft.Isam.Esent.Interop.EsentTooManyTestInjectionsException</span></span>](./esenttoomanytestinjectionsexception-class.md)  
            [<span data-ttu-id="5c5ba-264">EsentTransReadOnlyException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-264">Microsoft.Isam.Esent.Interop.EsentTransReadOnlyException</span></span>](./esenttransreadonlyexception-class.md)  
            [<span data-ttu-id="5c5ba-265">EsentTransTooDeepException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-265">Microsoft.Isam.Esent.Interop.EsentTransTooDeepException</span></span>](./esenttranstoodeepexception-class.md)  
            [<span data-ttu-id="5c5ba-266">EsentUnicodeNormalizationNotSupportedException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-266">Microsoft.Isam.Esent.Interop.EsentUnicodeNormalizationNotSupportedException</span></span>](./esentunicodenormalizationnotsupportedexception-class.md)  
            [<span data-ttu-id="5c5ba-267">EsentUpdateMustVersionException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-267">Microsoft.Isam.Esent.Interop.EsentUpdateMustVersionException</span></span>](./esentupdatemustversionexception-class.md)  
            [<span data-ttu-id="5c5ba-268">EsentUpdateNotPreparedException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-268">Microsoft.Isam.Esent.Interop.EsentUpdateNotPreparedException</span></span>](./esentupdatenotpreparedexception-class.md)  
            [<span data-ttu-id="5c5ba-269">EsentVersionStoreOutOfMemoryAndCleanupTimedOutException （.）</span><span class="sxs-lookup"><span data-stu-id="5c5ba-269">Microsoft.Isam.Esent.Interop.EsentVersionStoreOutOfMemoryAndCleanupTimedOutException</span></span>](./esentversionstoreoutofmemoryandcleanuptimedoutexception-class.md)
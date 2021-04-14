---
description: 深入瞭解： EsentObsoleteException 類別
title: EsentObsoleteException 類別
TOCTitle: EsentObsoleteException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentObsoleteException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentobsoleteexception(v=EXCHG.10)
ms:contentKeyID: 55102357
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentObsoleteException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentObsoleteException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c9d9597c3022d18ba0c6d476710f1c43430babc2
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "104514285"
---
# <a name="esentobsoleteexception-class"></a><span data-ttu-id="100a3-103">EsentObsoleteException 類別</span><span class="sxs-lookup"><span data-stu-id="100a3-103">EsentObsoleteException class</span></span>

<span data-ttu-id="100a3-104">已淘汰例外狀況的基類。</span><span class="sxs-lookup"><span data-stu-id="100a3-104">Base class for Obsolete exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="100a3-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="100a3-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="100a3-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="100a3-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="100a3-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="100a3-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="100a3-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="100a3-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="100a3-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="100a3-110">EsentApiException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          <span data-ttu-id="100a3-111">EsentObsoleteException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>  
            

<span data-ttu-id="100a3-112">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="100a3-112">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="100a3-113">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="100a3-113">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="100a3-114">Syntax</span><span class="sxs-lookup"><span data-stu-id="100a3-114">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentObsoleteException _
    Inherits EsentApiException
'Usage
Dim instance As EsentObsoleteException
```

``` csharp
[SerializableAttribute]
public abstract class EsentObsoleteException : EsentApiException
```

## <a name="thread-safety"></a><span data-ttu-id="100a3-115">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="100a3-115">Thread safety</span></span>

<span data-ttu-id="100a3-116">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="100a3-116">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="100a3-117">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="100a3-117">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="100a3-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="100a3-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="100a3-119">參考</span><span class="sxs-lookup"><span data-stu-id="100a3-119">Reference</span></span>

[<span data-ttu-id="100a3-120">EsentObsoleteException 成員</span><span class="sxs-lookup"><span data-stu-id="100a3-120">EsentObsoleteException members</span></span>](./esentobsoleteexception-members.md)

[<span data-ttu-id="100a3-121">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="100a3-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a><span data-ttu-id="100a3-122">衍生類型</span><span class="sxs-lookup"><span data-stu-id="100a3-122">Derived types</span></span>

[<span data-ttu-id="100a3-123">System.Object</span><span class="sxs-lookup"><span data-stu-id="100a3-123">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="100a3-124">System.Exception</span><span class="sxs-lookup"><span data-stu-id="100a3-124">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="100a3-125">EsentException。</span><span class="sxs-lookup"><span data-stu-id="100a3-125">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="100a3-126">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-126">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="100a3-127">EsentApiException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-127">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          <span data-ttu-id="100a3-128">EsentObsoleteException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-128">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>  
            [<span data-ttu-id="100a3-129">EsentAccessDeniedException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-129">Microsoft.Isam.Esent.Interop.EsentAccessDeniedException</span></span>](./esentaccessdeniedexception-class.md)  
            [<span data-ttu-id="100a3-130">EsentBadBackupDatabaseSizeException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-130">Microsoft.Isam.Esent.Interop.EsentBadBackupDatabaseSizeException</span></span>](./esentbadbackupdatabasesizeexception-class.md)  
            [<span data-ttu-id="100a3-131">EsentBadBookmarkException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-131">Microsoft.Isam.Esent.Interop.EsentBadBookmarkException</span></span>](./esentbadbookmarkexception-class.md)  
            [<span data-ttu-id="100a3-132">EsentBadDbSignatureException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-132">Microsoft.Isam.Esent.Interop.EsentBadDbSignatureException</span></span>](./esentbaddbsignatureexception-class.md)  
            [<span data-ttu-id="100a3-133">EsentBadPatchPageException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-133">Microsoft.Isam.Esent.Interop.EsentBadPatchPageException</span></span>](./esentbadpatchpageexception-class.md)  
            [<span data-ttu-id="100a3-134">EsentBadSLVSignatureException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-134">Microsoft.Isam.Esent.Interop.EsentBadSLVSignatureException</span></span>](./esentbadslvsignatureexception-class.md)  
            [<span data-ttu-id="100a3-135">EsentCannotAddFixedVarColumnToDerivedTableException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-135">Microsoft.Isam.Esent.Interop.EsentCannotAddFixedVarColumnToDerivedTableException</span></span>](./esentcannotaddfixedvarcolumntoderivedtableexception-class.md)  
            [<span data-ttu-id="100a3-136">EsentCannotNestDistributedTransactionsException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-136">Microsoft.Isam.Esent.Interop.EsentCannotNestDistributedTransactionsException</span></span>](./esentcannotnestdistributedtransactionsexception-class.md)  
            [<span data-ttu-id="100a3-137">EsentColumnIndexedException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-137">Microsoft.Isam.Esent.Interop.EsentColumnIndexedException</span></span>](./esentcolumnindexedexception-class.md)  
            [<span data-ttu-id="100a3-138">EsentColumnInRelationshipException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-138">Microsoft.Isam.Esent.Interop.EsentColumnInRelationshipException</span></span>](./esentcolumninrelationshipexception-class.md)  
            [<span data-ttu-id="100a3-139">EsentColumnLongException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-139">Microsoft.Isam.Esent.Interop.EsentColumnLongException</span></span>](./esentcolumnlongexception-class.md)  
            [<span data-ttu-id="100a3-140">EsentContainerNotEmptyException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-140">Microsoft.Isam.Esent.Interop.EsentContainerNotEmptyException</span></span>](./esentcontainernotemptyexception-class.md)  
            [<span data-ttu-id="100a3-141">EsentCurrencyStackOutOfMemoryException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-141">Microsoft.Isam.Esent.Interop.EsentCurrencyStackOutOfMemoryException</span></span>](./esentcurrencystackoutofmemoryexception-class.md)  
            [<span data-ttu-id="100a3-142">EsentDatabase200FormatException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-142">Microsoft.Isam.Esent.Interop.EsentDatabase200FormatException</span></span>](./esentdatabase200formatexception-class.md)  
            [<span data-ttu-id="100a3-143">EsentDatabase400FormatException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-143">Microsoft.Isam.Esent.Interop.EsentDatabase400FormatException</span></span>](./esentdatabase400formatexception-class.md)  
            [<span data-ttu-id="100a3-144">EsentDatabase500FormatException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-144">Microsoft.Isam.Esent.Interop.EsentDatabase500FormatException</span></span>](./esentdatabase500formatexception-class.md)  
            [<span data-ttu-id="100a3-145">EsentDatabaseIdInUseException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-145">Microsoft.Isam.Esent.Interop.EsentDatabaseIdInUseException</span></span>](./esentdatabaseidinuseexception-class.md)  
            [<span data-ttu-id="100a3-146">EsentDatabasePatchFileMismatchException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-146">Microsoft.Isam.Esent.Interop.EsentDatabasePatchFileMismatchException</span></span>](./esentdatabasepatchfilemismatchexception-class.md)  
            [<span data-ttu-id="100a3-147">EsentDatabasesNotFromSameSnapshotException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-147">Microsoft.Isam.Esent.Interop.EsentDatabasesNotFromSameSnapshotException</span></span>](./esentdatabasesnotfromsamesnapshotexception-class.md)  
            [<span data-ttu-id="100a3-148">EsentDatabaseStreamingFileMismatchException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-148">Microsoft.Isam.Esent.Interop.EsentDatabaseStreamingFileMismatchException</span></span>](./esentdatabasestreamingfilemismatchexception-class.md)  
            [<span data-ttu-id="100a3-149">EsentDatabaseUnavailableException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-149">Microsoft.Isam.Esent.Interop.EsentDatabaseUnavailableException</span></span>](./esentdatabaseunavailableexception-class.md)  
            [<span data-ttu-id="100a3-150">EsentDataHasChangedException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-150">Microsoft.Isam.Esent.Interop.EsentDataHasChangedException</span></span>](./esentdatahaschangedexception-class.md)  
            [<span data-ttu-id="100a3-151">EsentDistributedTransactionAlreadyPreparedToCommitException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-151">Microsoft.Isam.Esent.Interop.EsentDistributedTransactionAlreadyPreparedToCommitException</span></span>](./esentdistributedtransactionalreadypreparedtocommitexception-class.md)  
            [<span data-ttu-id="100a3-152">EsentDistributedTransactionNotYetPreparedToCommitException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-152">Microsoft.Isam.Esent.Interop.EsentDistributedTransactionNotYetPreparedToCommitException</span></span>](./esentdistributedtransactionnotyetpreparedtocommitexception-class.md)  
            [<span data-ttu-id="100a3-153">EsentDTCCallbackUnexpectedErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-153">Microsoft.Isam.Esent.Interop.EsentDTCCallbackUnexpectedErrorException</span></span>](./esentdtccallbackunexpectederrorexception-class.md)  
            [<span data-ttu-id="100a3-154">EsentDTCMissingCallbackException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-154">Microsoft.Isam.Esent.Interop.EsentDTCMissingCallbackException</span></span>](./esentdtcmissingcallbackexception-class.md)  
            [<span data-ttu-id="100a3-155">EsentDTCMissingCallbackOnRecoveryException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-155">Microsoft.Isam.Esent.Interop.EsentDTCMissingCallbackOnRecoveryException</span></span>](./esentdtcmissingcallbackonrecoveryexception-class.md)  
            [<span data-ttu-id="100a3-156">EsentFileCloseException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-156">Microsoft.Isam.Esent.Interop.EsentFileCloseException</span></span>](./esentfilecloseexception-class.md)  
            [<span data-ttu-id="100a3-157">EsentFileIOAbortException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-157">Microsoft.Isam.Esent.Interop.EsentFileIOAbortException</span></span>](./esentfileioabortexception-class.md)  
            [<span data-ttu-id="100a3-158">EsentFileIOFailException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-158">Microsoft.Isam.Esent.Interop.EsentFileIOFailException</span></span>](./esentfileiofailexception-class.md)  
            [<span data-ttu-id="100a3-159">EsentFileIORetryException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-159">Microsoft.Isam.Esent.Interop.EsentFileIORetryException</span></span>](./esentfileioretryexception-class.md)  
            [<span data-ttu-id="100a3-160">EsentFileIOSparseException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-160">Microsoft.Isam.Esent.Interop.EsentFileIOSparseException</span></span>](./esentfileiosparseexception-class.md)  
            [<span data-ttu-id="100a3-161">EsentIndexCantBuildException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-161">Microsoft.Isam.Esent.Interop.EsentIndexCantBuildException</span></span>](./esentindexcantbuildexception-class.md)  
            [<span data-ttu-id="100a3-162">EsentIndexTuplesTooManyColumnsException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-162">Microsoft.Isam.Esent.Interop.EsentIndexTuplesTooManyColumnsException</span></span>](./esentindextuplestoomanycolumnsexception-class.md)  
            [<span data-ttu-id="100a3-163">EsentInvalidCountryException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-163">Microsoft.Isam.Esent.Interop.EsentInvalidCountryException</span></span>](./esentinvalidcountryexception-class.md)  
            [<span data-ttu-id="100a3-164">EsentInvalidFilenameException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-164">Microsoft.Isam.Esent.Interop.EsentInvalidFilenameException</span></span>](./esentinvalidfilenameexception-class.md)  
            [<span data-ttu-id="100a3-165">EsentInvalidLogDirectoryException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-165">Microsoft.Isam.Esent.Interop.EsentInvalidLogDirectoryException</span></span>](./esentinvalidlogdirectoryexception-class.md)  
            [<span data-ttu-id="100a3-166">EsentInvalidLoggedOperationException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-166">Microsoft.Isam.Esent.Interop.EsentInvalidLoggedOperationException</span></span>](./esentinvalidloggedoperationexception-class.md)  
            [<span data-ttu-id="100a3-167">EsentInvalidObjectException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-167">Microsoft.Isam.Esent.Interop.EsentInvalidObjectException</span></span>](./esentinvalidobjectexception-class.md)  
            [<span data-ttu-id="100a3-168">EsentInvalidOnSortException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-168">Microsoft.Isam.Esent.Interop.EsentInvalidOnSortException</span></span>](./esentinvalidonsortexception-class.md)  
            [<span data-ttu-id="100a3-169">EsentInvalidSystemPathException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-169">Microsoft.Isam.Esent.Interop.EsentInvalidSystemPathException</span></span>](./esentinvalidsystempathexception-class.md)  
            [<span data-ttu-id="100a3-170">EsentKeyBoundaryException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-170">Microsoft.Isam.Esent.Interop.EsentKeyBoundaryException</span></span>](./esentkeyboundaryexception-class.md)  
            [<span data-ttu-id="100a3-171">EsentKeyTooBigException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-171">Microsoft.Isam.Esent.Interop.EsentKeyTooBigException</span></span>](./esentkeytoobigexception-class.md)  
            [<span data-ttu-id="100a3-172">EsentLanguageNotSupportedException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-172">Microsoft.Isam.Esent.Interop.EsentLanguageNotSupportedException</span></span>](./esentlanguagenotsupportedexception-class.md)  
            [<span data-ttu-id="100a3-173">EsentLinkNotSupportedException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-173">Microsoft.Isam.Esent.Interop.EsentLinkNotSupportedException</span></span>](./esentlinknotsupportedexception-class.md)  
            [<span data-ttu-id="100a3-174">EsentLogBufferTooSmallException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-174">Microsoft.Isam.Esent.Interop.EsentLogBufferTooSmallException</span></span>](./esentlogbuffertoosmallexception-class.md)  
            [<span data-ttu-id="100a3-175">EsentMissingPatchPageException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-175">Microsoft.Isam.Esent.Interop.EsentMissingPatchPageException</span></span>](./esentmissingpatchpageexception-class.md)  
            [<span data-ttu-id="100a3-176">EsentMustCommitDistributedTransactionToLevel0Exception （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-176">Microsoft.Isam.Esent.Interop.EsentMustCommitDistributedTransactionToLevel0Exception</span></span>](./esentmustcommitdistributedtransactiontolevel0exception-class.md)  
            [<span data-ttu-id="100a3-177">EsentMustDisableLoggingForDbUpgradeException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-177">Microsoft.Isam.Esent.Interop.EsentMustDisableLoggingForDbUpgradeException</span></span>](./esentmustdisableloggingfordbupgradeexception-class.md)  
            [<span data-ttu-id="100a3-178">EsentNotInDistributedTransactionException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-178">Microsoft.Isam.Esent.Interop.EsentNotInDistributedTransactionException</span></span>](./esentnotindistributedtransactionexception-class.md)  
            [<span data-ttu-id="100a3-179">EsentObjectDuplicateException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-179">Microsoft.Isam.Esent.Interop.EsentObjectDuplicateException</span></span>](./esentobjectduplicateexception-class.md)  
            [<span data-ttu-id="100a3-180">EsentPageBoundaryException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-180">Microsoft.Isam.Esent.Interop.EsentPageBoundaryException</span></span>](./esentpageboundaryexception-class.md)  
            [<span data-ttu-id="100a3-181">EsentPatchFileMissingException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-181">Microsoft.Isam.Esent.Interop.EsentPatchFileMissingException</span></span>](./esentpatchfilemissingexception-class.md)  
            [<span data-ttu-id="100a3-182">EsentRfsFailureException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-182">Microsoft.Isam.Esent.Interop.EsentRfsFailureException</span></span>](./esentrfsfailureexception-class.md)  
            [<span data-ttu-id="100a3-183">EsentRfsNotArmedException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-183">Microsoft.Isam.Esent.Interop.EsentRfsNotArmedException</span></span>](./esentrfsnotarmedexception-class.md)  
            [<span data-ttu-id="100a3-184">EsentRollbackRequiredException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-184">Microsoft.Isam.Esent.Interop.EsentRollbackRequiredException</span></span>](./esentrollbackrequiredexception-class.md)  
            [<span data-ttu-id="100a3-185">EsentSLVBufferTooSmallException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-185">Microsoft.Isam.Esent.Interop.EsentSLVBufferTooSmallException</span></span>](./esentslvbuffertoosmallexception-class.md)  
            [<span data-ttu-id="100a3-186">EsentSLVColumnCannotDeleteException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-186">Microsoft.Isam.Esent.Interop.EsentSLVColumnCannotDeleteException</span></span>](./esentslvcolumncannotdeleteexception-class.md)  
            [<span data-ttu-id="100a3-187">EsentSLVColumnDefaultValueNotAllowedException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-187">Microsoft.Isam.Esent.Interop.EsentSLVColumnDefaultValueNotAllowedException</span></span>](./esentslvcolumndefaultvaluenotallowedexception-class.md)  
            [<span data-ttu-id="100a3-188">EsentSLVCorruptedException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-188">Microsoft.Isam.Esent.Interop.EsentSLVCorruptedException</span></span>](./esentslvcorruptedexception-class.md)  
            [<span data-ttu-id="100a3-189">EsentSLVDatabaseMissingException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-189">Microsoft.Isam.Esent.Interop.EsentSLVDatabaseMissingException</span></span>](./esentslvdatabasemissingexception-class.md)  
            [<span data-ttu-id="100a3-190">EsentSLVEAListCorruptException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-190">Microsoft.Isam.Esent.Interop.EsentSLVEAListCorruptException</span></span>](./esentslvealistcorruptexception-class.md)  
            [<span data-ttu-id="100a3-191">EsentSLVEAListTooBigException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-191">Microsoft.Isam.Esent.Interop.EsentSLVEAListTooBigException</span></span>](./esentslvealisttoobigexception-class.md)  
            [<span data-ttu-id="100a3-192">EsentSLVEAListZeroAllocationException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-192">Microsoft.Isam.Esent.Interop.EsentSLVEAListZeroAllocationException</span></span>](./esentslvealistzeroallocationexception-class.md)  
            [<span data-ttu-id="100a3-193">EsentSLVFileAccessDeniedException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-193">Microsoft.Isam.Esent.Interop.EsentSLVFileAccessDeniedException</span></span>](./esentslvfileaccessdeniedexception-class.md)  
            [<span data-ttu-id="100a3-194">EsentSLVFileInUseException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-194">Microsoft.Isam.Esent.Interop.EsentSLVFileInUseException</span></span>](./esentslvfileinuseexception-class.md)  
            [<span data-ttu-id="100a3-195">EsentSLVFileInvalidPathException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-195">Microsoft.Isam.Esent.Interop.EsentSLVFileInvalidPathException</span></span>](./esentslvfileinvalidpathexception-class.md)  
            [<span data-ttu-id="100a3-196">EsentSLVFileIOException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-196">Microsoft.Isam.Esent.Interop.EsentSLVFileIOException</span></span>](./esentslvfileioexception-class.md)  
            [<span data-ttu-id="100a3-197">EsentSLVFileNotFoundException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-197">Microsoft.Isam.Esent.Interop.EsentSLVFileNotFoundException</span></span>](./esentslvfilenotfoundexception-class.md)  
            [<span data-ttu-id="100a3-198">EsentSLVFileStaleException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-198">Microsoft.Isam.Esent.Interop.EsentSLVFileStaleException</span></span>](./esentslvfilestaleexception-class.md)  
            [<span data-ttu-id="100a3-199">EsentSLVFileUnknownException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-199">Microsoft.Isam.Esent.Interop.EsentSLVFileUnknownException</span></span>](./esentslvfileunknownexception-class.md)  
            [<span data-ttu-id="100a3-200">EsentSLVHeaderBadChecksumException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-200">Microsoft.Isam.Esent.Interop.EsentSLVHeaderBadChecksumException</span></span>](./esentslvheaderbadchecksumexception-class.md)  
            [<span data-ttu-id="100a3-201">EsentSLVHeaderCorruptedException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-201">Microsoft.Isam.Esent.Interop.EsentSLVHeaderCorruptedException</span></span>](./esentslvheadercorruptedexception-class.md)  
            [<span data-ttu-id="100a3-202">EsentSLVInvalidPathException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-202">Microsoft.Isam.Esent.Interop.EsentSLVInvalidPathException</span></span>](./esentslvinvalidpathexception-class.md)  
            [<span data-ttu-id="100a3-203">EsentSLVOwnerMapAlreadyExistsException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-203">Microsoft.Isam.Esent.Interop.EsentSLVOwnerMapAlreadyExistsException</span></span>](./esentslvownermapalreadyexistsexception-class.md)  
            [<span data-ttu-id="100a3-204">EsentSLVOwnerMapCorruptedException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-204">Microsoft.Isam.Esent.Interop.EsentSLVOwnerMapCorruptedException</span></span>](./esentslvownermapcorruptedexception-class.md)  
            [<span data-ttu-id="100a3-205">EsentSLVOwnerMapPageNotFoundException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-205">Microsoft.Isam.Esent.Interop.EsentSLVOwnerMapPageNotFoundException</span></span>](./esentslvownermappagenotfoundexception-class.md)  
            [<span data-ttu-id="100a3-206">EsentSLVPagesNotCommittedException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-206">Microsoft.Isam.Esent.Interop.EsentSLVPagesNotCommittedException</span></span>](./esentslvpagesnotcommittedexception-class.md)  
            [<span data-ttu-id="100a3-207">EsentSLVPagesNotDeletedException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-207">Microsoft.Isam.Esent.Interop.EsentSLVPagesNotDeletedException</span></span>](./esentslvpagesnotdeletedexception-class.md)  
            [<span data-ttu-id="100a3-208">EsentSLVPagesNotFreeException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-208">Microsoft.Isam.Esent.Interop.EsentSLVPagesNotFreeException</span></span>](./esentslvpagesnotfreeexception-class.md)  
            [<span data-ttu-id="100a3-209">EsentSLVPagesNotReservedException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-209">Microsoft.Isam.Esent.Interop.EsentSLVPagesNotReservedException</span></span>](./esentslvpagesnotreservedexception-class.md)  
            [<span data-ttu-id="100a3-210">EsentSLVProviderNotLoadedException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-210">Microsoft.Isam.Esent.Interop.EsentSLVProviderNotLoadedException</span></span>](./esentslvprovidernotloadedexception-class.md)  
            [<span data-ttu-id="100a3-211">EsentSLVProviderVersionMismatchException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-211">Microsoft.Isam.Esent.Interop.EsentSLVProviderVersionMismatchException</span></span>](./esentslvproviderversionmismatchexception-class.md)  
            [<span data-ttu-id="100a3-212">EsentSLVReadVerifyFailureException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-212">Microsoft.Isam.Esent.Interop.EsentSLVReadVerifyFailureException</span></span>](./esentslvreadverifyfailureexception-class.md)  
            [<span data-ttu-id="100a3-213">EsentSLVRootNotSpecifiedException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-213">Microsoft.Isam.Esent.Interop.EsentSLVRootNotSpecifiedException</span></span>](./esentslvrootnotspecifiedexception-class.md)  
            [<span data-ttu-id="100a3-214">EsentSLVRootPathInvalidException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-214">Microsoft.Isam.Esent.Interop.EsentSLVRootPathInvalidException</span></span>](./esentslvrootpathinvalidexception-class.md)  
            [<span data-ttu-id="100a3-215">EsentSLVRootStillOpenException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-215">Microsoft.Isam.Esent.Interop.EsentSLVRootStillOpenException</span></span>](./esentslvrootstillopenexception-class.md)  
            [<span data-ttu-id="100a3-216">EsentSLVSpaceCorruptedException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-216">Microsoft.Isam.Esent.Interop.EsentSLVSpaceCorruptedException</span></span>](./esentslvspacecorruptedexception-class.md)  
            [<span data-ttu-id="100a3-217">EsentSLVSpaceWriteConflictException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-217">Microsoft.Isam.Esent.Interop.EsentSLVSpaceWriteConflictException</span></span>](./esentslvspacewriteconflictexception-class.md)  
            [<span data-ttu-id="100a3-218">EsentSLVStreamingFileAlreadyExistsException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-218">Microsoft.Isam.Esent.Interop.EsentSLVStreamingFileAlreadyExistsException</span></span>](./esentslvstreamingfilealreadyexistsexception-class.md)  
            [<span data-ttu-id="100a3-219">EsentSLVStreamingFileFullException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-219">Microsoft.Isam.Esent.Interop.EsentSLVStreamingFileFullException</span></span>](./esentslvstreamingfilefullexception-class.md)  
            [<span data-ttu-id="100a3-220">EsentSLVStreamingFileInUseException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-220">Microsoft.Isam.Esent.Interop.EsentSLVStreamingFileInUseException</span></span>](./esentslvstreamingfileinuseexception-class.md)  
            [<span data-ttu-id="100a3-221">EsentSLVStreamingFileMissingException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-221">Microsoft.Isam.Esent.Interop.EsentSLVStreamingFileMissingException</span></span>](./esentslvstreamingfilemissingexception-class.md)  
            [<span data-ttu-id="100a3-222">EsentSLVStreamingFileNotCreatedException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-222">Microsoft.Isam.Esent.Interop.EsentSLVStreamingFileNotCreatedException</span></span>](./esentslvstreamingfilenotcreatedexception-class.md)  
            [<span data-ttu-id="100a3-223">EsentSLVStreamingFileReadOnlyException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-223">Microsoft.Isam.Esent.Interop.EsentSLVStreamingFileReadOnlyException</span></span>](./esentslvstreamingfilereadonlyexception-class.md)  
            [<span data-ttu-id="100a3-224">EsentSoftRecoveryOnSnapshotException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-224">Microsoft.Isam.Esent.Interop.EsentSoftRecoveryOnSnapshotException</span></span>](./esentsoftrecoveryonsnapshotexception-class.md)  
            [<span data-ttu-id="100a3-225">EsentSPAvailExtCacheOutOfMemoryException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-225">Microsoft.Isam.Esent.Interop.EsentSPAvailExtCacheOutOfMemoryException</span></span>](./esentspavailextcacheoutofmemoryexception-class.md)  
            [<span data-ttu-id="100a3-226">EsentSPAvailExtCacheOutOfSyncException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-226">Microsoft.Isam.Esent.Interop.EsentSPAvailExtCacheOutOfSyncException</span></span>](./esentspavailextcacheoutofsyncexception-class.md)  
            [<span data-ttu-id="100a3-227">EsentSQLLinkNotSupportedException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-227">Microsoft.Isam.Esent.Interop.EsentSQLLinkNotSupportedException</span></span>](./esentsqllinknotsupportedexception-class.md)  
            [<span data-ttu-id="100a3-228">EsentStreamingDataNotLoggedException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-228">Microsoft.Isam.Esent.Interop.EsentStreamingDataNotLoggedException</span></span>](./esentstreamingdatanotloggedexception-class.md)  
            [<span data-ttu-id="100a3-229">EsentTaggedNotNullException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-229">Microsoft.Isam.Esent.Interop.EsentTaggedNotNULLException</span></span>](./esenttaggednotnullexception-class.md)  
            [<span data-ttu-id="100a3-230">EsentTempFileOpenErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-230">Microsoft.Isam.Esent.Interop.EsentTempFileOpenErrorException</span></span>](./esenttempfileopenerrorexception-class.md)  
            [<span data-ttu-id="100a3-231">EsentTooManyOpenDatabasesException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-231">Microsoft.Isam.Esent.Interop.EsentTooManyOpenDatabasesException</span></span>](./esenttoomanyopendatabasesexception-class.md)  
            [<span data-ttu-id="100a3-232">EsentTooManySplitsException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-232">Microsoft.Isam.Esent.Interop.EsentTooManySplitsException</span></span>](./esenttoomanysplitsexception-class.md)  
            [<span data-ttu-id="100a3-233">EsentUnicodeTranslationBufferTooSmallException （.）</span><span class="sxs-lookup"><span data-stu-id="100a3-233">Microsoft.Isam.Esent.Interop.EsentUnicodeTranslationBufferTooSmallException</span></span>](./esentunicodetranslationbuffertoosmallexception-class.md)
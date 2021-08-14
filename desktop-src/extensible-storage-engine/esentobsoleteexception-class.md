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
ms.openlocfilehash: db67425defce2b2247aa7ba94a9742c53a671c27287d76474223cbc050725f5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118494015"
---
# <a name="esentobsoleteexception-class"></a>EsentObsoleteException 類別

已淘汰例外狀況的基類。

## <a name="inheritance-hierarchy"></a>繼承階層

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [EsentException。](./esentexception-class.md)  
      [EsentErrorException （.）](./esenterrorexception-class.md)  
        [EsentApiException （.）](./esentapiexception-class.md)  
          EsentObsoleteException （.）  
            

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

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

## <a name="thread-safety"></a>執行緒安全

這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。 並非所有的執行個體成員都是安全執行緒。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[EsentObsoleteException 成員](./esentobsoleteexception-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a>衍生類型

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [EsentException。](./esentexception-class.md)  
      [EsentErrorException （.）](./esenterrorexception-class.md)  
        [EsentApiException （.）](./esentapiexception-class.md)  
          EsentObsoleteException （.）  
            [EsentAccessDeniedException （.）](./esentaccessdeniedexception-class.md)  
            [EsentBadBackupDatabaseSizeException （.）](./esentbadbackupdatabasesizeexception-class.md)  
            [EsentBadBookmarkException （.）](./esentbadbookmarkexception-class.md)  
            [EsentBadDbSignatureException （.）](./esentbaddbsignatureexception-class.md)  
            [EsentBadPatchPageException （.）](./esentbadpatchpageexception-class.md)  
            [EsentBadSLVSignatureException （.）](./esentbadslvsignatureexception-class.md)  
            [EsentCannotAddFixedVarColumnToDerivedTableException （.）](./esentcannotaddfixedvarcolumntoderivedtableexception-class.md)  
            [EsentCannotNestDistributedTransactionsException （.）](./esentcannotnestdistributedtransactionsexception-class.md)  
            [EsentColumnIndexedException （.）](./esentcolumnindexedexception-class.md)  
            [EsentColumnInRelationshipException （.）](./esentcolumninrelationshipexception-class.md)  
            [EsentColumnLongException （.）](./esentcolumnlongexception-class.md)  
            [EsentContainerNotEmptyException （.）](./esentcontainernotemptyexception-class.md)  
            [EsentCurrencyStackOutOfMemoryException （.）](./esentcurrencystackoutofmemoryexception-class.md)  
            [EsentDatabase200FormatException （.）](./esentdatabase200formatexception-class.md)  
            [EsentDatabase400FormatException （.）](./esentdatabase400formatexception-class.md)  
            [EsentDatabase500FormatException （.）](./esentdatabase500formatexception-class.md)  
            [EsentDatabaseIdInUseException （.）](./esentdatabaseidinuseexception-class.md)  
            [EsentDatabasePatchFileMismatchException （.）](./esentdatabasepatchfilemismatchexception-class.md)  
            [EsentDatabasesNotFromSameSnapshotException （.）](./esentdatabasesnotfromsamesnapshotexception-class.md)  
            [EsentDatabaseStreamingFileMismatchException （.）](./esentdatabasestreamingfilemismatchexception-class.md)  
            [EsentDatabaseUnavailableException （.）](./esentdatabaseunavailableexception-class.md)  
            [EsentDataHasChangedException （.）](./esentdatahaschangedexception-class.md)  
            [EsentDistributedTransactionAlreadyPreparedToCommitException （.）](./esentdistributedtransactionalreadypreparedtocommitexception-class.md)  
            [EsentDistributedTransactionNotYetPreparedToCommitException （.）](./esentdistributedtransactionnotyetpreparedtocommitexception-class.md)  
            [EsentDTCCallbackUnexpectedErrorException （.）](./esentdtccallbackunexpectederrorexception-class.md)  
            [EsentDTCMissingCallbackException （.）](./esentdtcmissingcallbackexception-class.md)  
            [EsentDTCMissingCallbackOnRecoveryException （.）](./esentdtcmissingcallbackonrecoveryexception-class.md)  
            [EsentFileCloseException （.）](./esentfilecloseexception-class.md)  
            [EsentFileIOAbortException （.）](./esentfileioabortexception-class.md)  
            [EsentFileIOFailException （.）](./esentfileiofailexception-class.md)  
            [EsentFileIORetryException （.）](./esentfileioretryexception-class.md)  
            [EsentFileIOSparseException （.）](./esentfileiosparseexception-class.md)  
            [EsentIndexCantBuildException （.）](./esentindexcantbuildexception-class.md)  
            [EsentIndexTuplesTooManyColumnsException （.）](./esentindextuplestoomanycolumnsexception-class.md)  
            [EsentInvalidCountryException （.）](./esentinvalidcountryexception-class.md)  
            [EsentInvalidFilenameException （.）](./esentinvalidfilenameexception-class.md)  
            [EsentInvalidLogDirectoryException （.）](./esentinvalidlogdirectoryexception-class.md)  
            [EsentInvalidLoggedOperationException （.）](./esentinvalidloggedoperationexception-class.md)  
            [EsentInvalidObjectException （.）](./esentinvalidobjectexception-class.md)  
            [EsentInvalidOnSortException （.）](./esentinvalidonsortexception-class.md)  
            [EsentInvalidSystemPathException （.）](./esentinvalidsystempathexception-class.md)  
            [EsentKeyBoundaryException （.）](./esentkeyboundaryexception-class.md)  
            [EsentKeyTooBigException （.）](./esentkeytoobigexception-class.md)  
            [EsentLanguageNotSupportedException （.）](./esentlanguagenotsupportedexception-class.md)  
            [EsentLinkNotSupportedException （.）](./esentlinknotsupportedexception-class.md)  
            [EsentLogBufferTooSmallException （.）](./esentlogbuffertoosmallexception-class.md)  
            [EsentMissingPatchPageException （.）](./esentmissingpatchpageexception-class.md)  
            [EsentMustCommitDistributedTransactionToLevel0Exception （.）](./esentmustcommitdistributedtransactiontolevel0exception-class.md)  
            [EsentMustDisableLoggingForDbUpgradeException （.）](./esentmustdisableloggingfordbupgradeexception-class.md)  
            [EsentNotInDistributedTransactionException （.）](./esentnotindistributedtransactionexception-class.md)  
            [EsentObjectDuplicateException （.）](./esentobjectduplicateexception-class.md)  
            [EsentPageBoundaryException （.）](./esentpageboundaryexception-class.md)  
            [EsentPatchFileMissingException （.）](./esentpatchfilemissingexception-class.md)  
            [EsentRfsFailureException （.）](./esentrfsfailureexception-class.md)  
            [EsentRfsNotArmedException （.）](./esentrfsnotarmedexception-class.md)  
            [EsentRollbackRequiredException （.）](./esentrollbackrequiredexception-class.md)  
            [EsentSLVBufferTooSmallException （.）](./esentslvbuffertoosmallexception-class.md)  
            [EsentSLVColumnCannotDeleteException （.）](./esentslvcolumncannotdeleteexception-class.md)  
            [EsentSLVColumnDefaultValueNotAllowedException （.）](./esentslvcolumndefaultvaluenotallowedexception-class.md)  
            [EsentSLVCorruptedException （.）](./esentslvcorruptedexception-class.md)  
            [EsentSLVDatabaseMissingException （.）](./esentslvdatabasemissingexception-class.md)  
            [EsentSLVEAListCorruptException （.）](./esentslvealistcorruptexception-class.md)  
            [EsentSLVEAListTooBigException （.）](./esentslvealisttoobigexception-class.md)  
            [EsentSLVEAListZeroAllocationException （.）](./esentslvealistzeroallocationexception-class.md)  
            [EsentSLVFileAccessDeniedException （.）](./esentslvfileaccessdeniedexception-class.md)  
            [EsentSLVFileInUseException （.）](./esentslvfileinuseexception-class.md)  
            [EsentSLVFileInvalidPathException （.）](./esentslvfileinvalidpathexception-class.md)  
            [EsentSLVFileIOException （.）](./esentslvfileioexception-class.md)  
            [EsentSLVFileNotFoundException （.）](./esentslvfilenotfoundexception-class.md)  
            [EsentSLVFileStaleException （.）](./esentslvfilestaleexception-class.md)  
            [EsentSLVFileUnknownException （.）](./esentslvfileunknownexception-class.md)  
            [EsentSLVHeaderBadChecksumException （.）](./esentslvheaderbadchecksumexception-class.md)  
            [EsentSLVHeaderCorruptedException （.）](./esentslvheadercorruptedexception-class.md)  
            [EsentSLVInvalidPathException （.）](./esentslvinvalidpathexception-class.md)  
            [EsentSLVOwnerMapAlreadyExistsException （.）](./esentslvownermapalreadyexistsexception-class.md)  
            [EsentSLVOwnerMapCorruptedException （.）](./esentslvownermapcorruptedexception-class.md)  
            [EsentSLVOwnerMapPageNotFoundException （.）](./esentslvownermappagenotfoundexception-class.md)  
            [EsentSLVPagesNotCommittedException （.）](./esentslvpagesnotcommittedexception-class.md)  
            [EsentSLVPagesNotDeletedException （.）](./esentslvpagesnotdeletedexception-class.md)  
            [EsentSLVPagesNotFreeException （.）](./esentslvpagesnotfreeexception-class.md)  
            [EsentSLVPagesNotReservedException （.）](./esentslvpagesnotreservedexception-class.md)  
            [EsentSLVProviderNotLoadedException （.）](./esentslvprovidernotloadedexception-class.md)  
            [EsentSLVProviderVersionMismatchException （.）](./esentslvproviderversionmismatchexception-class.md)  
            [EsentSLVReadVerifyFailureException （.）](./esentslvreadverifyfailureexception-class.md)  
            [EsentSLVRootNotSpecifiedException （.）](./esentslvrootnotspecifiedexception-class.md)  
            [EsentSLVRootPathInvalidException （.）](./esentslvrootpathinvalidexception-class.md)  
            [EsentSLVRootStillOpenException （.）](./esentslvrootstillopenexception-class.md)  
            [EsentSLVSpaceCorruptedException （.）](./esentslvspacecorruptedexception-class.md)  
            [EsentSLVSpaceWriteConflictException （.）](./esentslvspacewriteconflictexception-class.md)  
            [EsentSLVStreamingFileAlreadyExistsException （.）](./esentslvstreamingfilealreadyexistsexception-class.md)  
            [EsentSLVStreamingFileFullException （.）](./esentslvstreamingfilefullexception-class.md)  
            [EsentSLVStreamingFileInUseException （.）](./esentslvstreamingfileinuseexception-class.md)  
            [EsentSLVStreamingFileMissingException （.）](./esentslvstreamingfilemissingexception-class.md)  
            [EsentSLVStreamingFileNotCreatedException （.）](./esentslvstreamingfilenotcreatedexception-class.md)  
            [EsentSLVStreamingFileReadOnlyException （.）](./esentslvstreamingfilereadonlyexception-class.md)  
            [EsentSoftRecoveryOnSnapshotException （.）](./esentsoftrecoveryonsnapshotexception-class.md)  
            [EsentSPAvailExtCacheOutOfMemoryException （.）](./esentspavailextcacheoutofmemoryexception-class.md)  
            [EsentSPAvailExtCacheOutOfSyncException （.）](./esentspavailextcacheoutofsyncexception-class.md)  
            [EsentSQLLinkNotSupportedException （.）](./esentsqllinknotsupportedexception-class.md)  
            [EsentStreamingDataNotLoggedException （.）](./esentstreamingdatanotloggedexception-class.md)  
            [EsentTaggedNotNullException （.）](./esenttaggednotnullexception-class.md)  
            [EsentTempFileOpenErrorException （.）](./esenttempfileopenerrorexception-class.md)  
            [EsentTooManyOpenDatabasesException （.）](./esenttoomanyopendatabasesexception-class.md)  
            [EsentTooManySplitsException （.）](./esenttoomanysplitsexception-class.md)  
            [EsentUnicodeTranslationBufferTooSmallException （.）](./esentunicodetranslationbuffertoosmallexception-class.md)
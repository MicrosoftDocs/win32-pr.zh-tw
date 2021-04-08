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
# <a name="esentusageexception-class"></a>EsentUsageException 類別

使用例外狀況的基類。

## <a name="inheritance-hierarchy"></a>繼承階層

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [EsentException。](./esentexception-class.md)  
      [EsentErrorException （.）](./esenterrorexception-class.md)  
        [EsentApiException （.）](./esentapiexception-class.md)  
          EsentUsageException （.）  
            

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

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

## <a name="thread-safety"></a>執行緒安全

這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。 並非所有的執行個體成員都是安全執行緒。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[EsentUsageException 成員](./esentusageexception-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a>衍生類型

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [EsentException。](./esentexception-class.md)  
      [EsentErrorException （.）](./esenterrorexception-class.md)  
        [EsentApiException （.）](./esentapiexception-class.md)  
          EsentUsageException （.）  
            [EsentAfterInitializationException （.）](./esentafterinitializationexception-class.md)  
            [EsentAlreadyInitializedException （.）](./esentalreadyinitializedexception-class.md)  
            [EsentAlreadyPreparedException （.）](./esentalreadypreparedexception-class.md)  
            [EsentBackupDirectoryNotEmptyException （.）](./esentbackupdirectorynotemptyexception-class.md)  
            [EsentBadColumnIdException （.）](./esentbadcolumnidexception-class.md)  
            [EsentBadRestoreTargetInstanceException （.）](./esentbadrestoretargetinstanceexception-class.md)  
            [EsentCallbackNotResolvedException （.）](./esentcallbacknotresolvedexception-class.md)  
            [EsentCannotBeTaggedException （.）](./esentcannotbetaggedexception-class.md)  
            [EsentCannotDeleteSystemTableException （.）](./esentcannotdeletesystemtableexception-class.md)  
            [EsentCannotDeleteTemplateTableException （.）](./esentcannotdeletetemplatetableexception-class.md)  
            [EsentCannotDeleteTempTableException （.）](./esentcannotdeletetemptableexception-class.md)  
            [EsentCannotDisableVersioningException （.）](./esentcannotdisableversioningexception-class.md)  
            [EsentCannotIndexException （.）](./esentcannotindexexception-class.md)  
            [EsentCannotMaterializeForwardOnlySortException （.）](./esentcannotmaterializeforwardonlysortexception-class.md)  
            [EsentCannotNestDDLException （.）](./esentcannotnestddlexception-class.md)  
            [EsentCannotSeparateIntrinsicLVException （.）](./esentcannotseparateintrinsiclvexception-class.md)  
            [EsentColumnCannotBeCompressedException （.）](./esentcolumncannotbecompressedexception-class.md)  
            [EsentColumnDoesNotFitException （.）](./esentcolumndoesnotfitexception-class.md)  
            [EsentColumnDuplicateException （.）](./esentcolumnduplicateexception-class.md)  
            [EsentColumnInUseException （.）](./esentcolumninuseexception-class.md)  
            [EsentColumnNoChunkException （.）](./esentcolumnnochunkexception-class.md)  
            [EsentColumnNotFoundException （.）](./esentcolumnnotfoundexception-class.md)  
            [EsentColumnNotUpdatableException （.）](./esentcolumnnotupdatableexception-class.md)  
            [EsentColumnRedundantException （.）](./esentcolumnredundantexception-class.md)  
            [EsentColumnTooBigException （.）](./esentcolumntoobigexception-class.md)  
            [EsentDatabaseAlreadyRunningMaintenanceException （.）](./esentdatabasealreadyrunningmaintenanceexception-class.md)  
            [EsentDatabaseCorruptedNoRepairException （.）](./esentdatabasecorruptednorepairexception-class.md)  
            [EsentDatabaseDuplicateException （.）](./esentdatabaseduplicateexception-class.md)  
            [EsentDatabaseFileReadOnlyException （.）](./esentdatabasefilereadonlyexception-class.md)  
            [EsentDatabaseInUseException （.）](./esentdatabaseinuseexception-class.md)  
            [EsentDatabaseInvalidIncrementalReseedException （.）](./esentdatabaseinvalidincrementalreseedexception-class.md)  
            [EsentDatabaseInvalidNameException （.）](./esentdatabaseinvalidnameexception-class.md)  
            [EsentDatabaseInvalidPagesException （.）](./esentdatabaseinvalidpagesexception-class.md)  
            [EsentDatabaseInvalidPathException （.）](./esentdatabaseinvalidpathexception-class.md)  
            [EsentDatabaseLockedException （.）](./esentdatabaselockedexception-class.md)  
            [EsentDatabaseNotFoundException （.）](./esentdatabasenotfoundexception-class.md)  
            [EsentDatabaseSharingViolationException （.）](./esentdatabasesharingviolationexception-class.md)  
            [EsentDatabaseSignInUseException （.）](./esentdatabasesigninuseexception-class.md)  
            [EsentDDLNotInheritableException （.）](./esentddlnotinheritableexception-class.md)  
            [EsentDefaultValueTooBigException （.）](./esentdefaultvaluetoobigexception-class.md)  
            [EsentDensityInvalidException （.）](./esentdensityinvalidexception-class.md)  
            [EsentDisabledFunctionalityException （.）](./esentdisabledfunctionalityexception-class.md)  
            [EsentEntryPointNotFoundException （.）](./esententrypointnotfoundexception-class.md)  
            [EsentExclusiveTableLockRequiredException （.）](./esentexclusivetablelockrequiredexception-class.md)  
            [EsentFeatureNotAvailableException （.）](./esentfeaturenotavailableexception-class.md)  
            [EsentFileCompressedException （.）](./esentfilecompressedexception-class.md)  
            [EsentFilteredMoveNotSupportedException （.）](./esentfilteredmovenotsupportedexception-class.md)  
            [EsentFixedDDLException （.）](./esentfixedddlexception-class.md)  
            [EsentFixedInheritedDDLException （.）](./esentfixedinheritedddlexception-class.md)  
            [EsentForceDetachNotAllowedException （.）](./esentforcedetachnotallowedexception-class.md)  
            [EsentIllegalOperationException （.）](./esentillegaloperationexception-class.md)  
            [EsentIndexDuplicateException （.）](./esentindexduplicateexception-class.md)  
            [EsentIndexHasPrimaryException （.）](./esentindexhasprimaryexception-class.md)  
            [EsentIndexInvalidDefException （.）](./esentindexinvaliddefexception-class.md)  
            [EsentIndexMustStayException （.）](./esentindexmuststayexception-class.md)  
            [EsentIndexTuplesCannotRetrieveFromIndexException （.）](./esentindextuplescannotretrievefromindexexception-class.md)  
            [EsentIndexTuplesInvalidLimitsException （.）](./esentindextuplesinvalidlimitsexception-class.md)  
            [EsentIndexTuplesKeyTooSmallException （.）](./esentindextupleskeytoosmallexception-class.md)  
            [EsentIndexTuplesNonUniqueOnlyException （.）](./esentindextuplesnonuniqueonlyexception-class.md)  
            [EsentIndexTuplesSecondaryIndexOnlyException （.）](./esentindextuplessecondaryindexonlyexception-class.md)  
            [EsentIndexTuplesTextBinaryColumnsOnlyException （.）](./esentindextuplestextbinarycolumnsonlyexception-class.md)  
            [EsentIndexTuplesVarSegMacNotAllowedException （.）](./esentindextuplesvarsegmacnotallowedexception-class.md)  
            [EsentInstanceNameInUseException （.）](./esentinstancenameinuseexception-class.md)  
            [EsentInTransactionException （.）](./esentintransactionexception-class.md)  
            [EsentInvalidBackupException （.）](./esentinvalidbackupexception-class.md)  
            [EsentInvalidBackupSequenceException （.）](./esentinvalidbackupsequenceexception-class.md)  
            [EsentInvalidBookmarkException （.）](./esentinvalidbookmarkexception-class.md)  
            [EsentInvalidCodePageException （.）](./esentinvalidcodepageexception-class.md)  
            [EsentInvalidColumnTypeException （.）](./esentinvalidcolumntypeexception-class.md)  
            [EsentInvalidCreateIndexException （.）](./esentinvalidcreateindexexception-class.md)  
            [EsentInvalidDatabaseException （.）](./esentinvaliddatabaseexception-class.md)  
            [EsentInvalidDatabaseIdException （.）](./esentinvaliddatabaseidexception-class.md)  
            [EsentInvalidGrbitException （.）](./esentinvalidgrbitexception-class.md)  
            [EsentInvalidIndexIdException （.）](./esentinvalidindexidexception-class.md)  
            [EsentInvalidInstanceException （.）](./esentinvalidinstanceexception-class.md)  
            [EsentInvalidLanguageIdException （.）](./esentinvalidlanguageidexception-class.md)  
            [EsentInvalidLCMapStringFlagsException （.）](./esentinvalidlcmapstringflagsexception-class.md)  
            [EsentInvalidNameException （.）](./esentinvalidnameexception-class.md)  
            [EsentInvalidOperationException （.）](./esentinvalidoperationexception-class.md)  
            [EsentInvalidParameterException （.）](./esentinvalidparameterexception-class.md)  
            [EsentInvalidPathException （.）](./esentinvalidpathexception-class.md)  
            [EsentInvalidPlaceholderColumnException （.）](./esentinvalidplaceholdercolumnexception-class.md)  
            [EsentInvalidPrereadException （.）](./esentinvalidprereadexception-class.md)  
            [EsentInvalidSesidException （.）](./esentinvalidsesidexception-class.md)  
            [EsentInvalidSettingsException （.）](./esentinvalidsettingsexception-class.md)  
            [EsentInvalidTableIdException （.）](./esentinvalidtableidexception-class.md)  
            [EsentKeyIsMadeException （.）](./esentkeyismadeexception-class.md)  
            [EsentKeyNotMadeException （.）](./esentkeynotmadeexception-class.md)  
            [EsentLogFileNotCopiedException （.）](./esentlogfilenotcopiedexception-class.md)  
            [EsentLogFilePathInUseException （.）](./esentlogfilepathinuseexception-class.md)  
            [EsentLogFileSizeMismatchException （.）](./esentlogfilesizemismatchexception-class.md)  
            [EsentLoggingDisabledException （.）](./esentloggingdisabledexception-class.md)  
            [EsentLSAlreadySetException （.）](./esentlsalreadysetexception-class.md)  
            [EsentLSCallbackNotSpecifiedException （.）](./esentlscallbacknotspecifiedexception-class.md)  
            [EsentMultiValuedColumnMustBeTaggedException （.）](./esentmultivaluedcolumnmustbetaggedexception-class.md)  
            [EsentMultiValuedIndexViolationException （.）](./esentmultivaluedindexviolationexception-class.md)  
            [EsentMustBeSeparateLongValueException （.）](./esentmustbeseparatelongvalueexception-class.md)  
            [EsentMustRollbackException （.）](./esentmustrollbackexception-class.md)  
            [EsentNoBackupDirectoryException （.）](./esentnobackupdirectoryexception-class.md)  
            [EsentNoCurrentIndexException （.）](./esentnocurrentindexexception-class.md)  
            [EsentNotInitializedException （.）](./esentnotinitializedexception-class.md)  
            [EsentNotInTransactionException （.）](./esentnotintransactionexception-class.md)  
            [EsentNullInvalidException （.）](./esentnullinvalidexception-class.md)  
            [EsentNullKeyDisallowedException （.）](./esentnullkeydisallowedexception-class.md)  
            [EsentOneDatabasePerSessionException （.）](./esentonedatabasepersessionexception-class.md)  
            [EsentOSSnapshotInvalidSequenceException （.）](./esentossnapshotinvalidsequenceexception-class.md)  
            [EsentOSSnapshotInvalidSnapIdException （.）](./esentossnapshotinvalidsnapidexception-class.md)  
            [EsentPartiallyAttachedDBException （.）](./esentpartiallyattacheddbexception-class.md)  
            [EsentPermissionDeniedException （.）](./esentpermissiondeniedexception-class.md)  
            [EsentQueryNotSupportedException （.）](./esentquerynotsupportedexception-class.md)  
            [EsentRecordNoCopyException （.）](./esentrecordnocopyexception-class.md)  
            [EsentRecordPrimaryChangedException （.）](./esentrecordprimarychangedexception-class.md)  
            [EsentRestoreOfNonBackupDatabaseException （.）](./esentrestoreofnonbackupdatabaseexception-class.md)  
            [EsentRunningInMultiInstanceModeException （.）](./esentrunninginmultiinstancemodeexception-class.md)  
            [EsentRunningInOneInstanceModeException （.）](./esentrunninginoneinstancemodeexception-class.md)  
            [EsentSesidTableIdMismatchException （.）](./esentsesidtableidmismatchexception-class.md)  
            [EsentSessionCoNtextAlreadySetException （.）](./esentsessioncontextalreadysetexception-class.md)  
            [EsentSessionCoNtextNotSetByThisThreadException （.）](./esentsessioncontextnotsetbythisthreadexception-class.md)  
            [EsentSessionInUseException （.）](./esentsessioninuseexception-class.md)  
            [EsentSessionSharingViolationException （.）](./esentsessionsharingviolationexception-class.md)  
            [EsentSessionWriteConflictException （.）](./esentsessionwriteconflictexception-class.md)  
            [EsentSoftRecoveryOnBackupDatabaseException （.）](./esentsoftrecoveryonbackupdatabaseexception-class.md)  
            [EsentSpaceHintsInvalidException （.）](./esentspacehintsinvalidexception-class.md)  
            [EsentSystemParamsAlreadySetException （.）](./esentsystemparamsalreadysetexception-class.md)  
            [EsentSystemPathInUseException （.）](./esentsystempathinuseexception-class.md)  
            [EsentTableLockedException （.）](./esenttablelockedexception-class.md)  
            [EsentTableNotEmptyException （.）](./esenttablenotemptyexception-class.md)  
            [EsentTempPathInUseException （.）](./esenttemppathinuseexception-class.md)  
            [EsentTooManyActiveUsersException （.）](./esenttoomanyactiveusersexception-class.md)  
            [EsentTooManyAttachedDatabasesException （.）](./esenttoomanyattacheddatabasesexception-class.md)  
            [EsentTooManyColumnsException （.）](./esenttoomanycolumnsexception-class.md)  
            [EsentTooManyIndexesException （.）](./esenttoomanyindexesexception-class.md)  
            [EsentTooManyKeysException （.）](./esenttoomanykeysexception-class.md)  
            [EsentTooManyOpenTablesAndCleanupTimedOutException （.）](./esenttoomanyopentablesandcleanuptimedoutexception-class.md)  
            [EsentTooManyTestInjectionsException （.）](./esenttoomanytestinjectionsexception-class.md)  
            [EsentTransReadOnlyException （.）](./esenttransreadonlyexception-class.md)  
            [EsentTransTooDeepException （.）](./esenttranstoodeepexception-class.md)  
            [EsentUnicodeNormalizationNotSupportedException （.）](./esentunicodenormalizationnotsupportedexception-class.md)  
            [EsentUpdateMustVersionException （.）](./esentupdatemustversionexception-class.md)  
            [EsentUpdateNotPreparedException （.）](./esentupdatenotpreparedexception-class.md)  
            [EsentVersionStoreOutOfMemoryAndCleanupTimedOutException （.）](./esentversionstoreoutofmemoryandcleanuptimedoutexception-class.md)
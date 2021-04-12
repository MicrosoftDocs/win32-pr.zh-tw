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
# <a name="esentstateexception-class"></a>EsentStateException 類別

狀態例外狀況的基類。

## <a name="inheritance-hierarchy"></a>繼承階層

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [EsentException。](./esentexception-class.md)  
      [EsentErrorException （.）](./esenterrorexception-class.md)  
        [EsentApiException （.）](./esentapiexception-class.md)  
          EsentStateException （.）  
            

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

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

## <a name="thread-safety"></a>執行緒安全

這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。 並非所有的執行個體成員都是安全執行緒。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[EsentStateException 成員](./esentstateexception-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a>衍生類型

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [EsentException。](./esentexception-class.md)  
      [EsentErrorException （.）](./esenterrorexception-class.md)  
        [EsentApiException （.）](./esentapiexception-class.md)  
          EsentStateException （.）  
            [EsentBackupInProgressException （.）](./esentbackupinprogressexception-class.md)  
            [EsentBackupNotAllowedYetException （.）](./esentbackupnotallowedyetexception-class.md)  
            [EsentBadItagSequenceException （.）](./esentbaditagsequenceexception-class.md)  
            [EsentBufferTooSmallException （.）](./esentbuffertoosmallexception-class.md)  
            [EsentCallbackFailedException （.）](./esentcallbackfailedexception-class.md)  
            [EsentDatabaseAlreadyUpgradedException （.）](./esentdatabasealreadyupgradedexception-class.md)  
            [EsentDatabaseFailedIncrementalReseedException （.）](./esentdatabasefailedincrementalreseedexception-class.md)  
            [EsentDatabaseIncompleteUpgradeException （.）](./esentdatabaseincompleteupgradeexception-class.md)  
            [EsentDatabaseLeakInSpaceException （.）](./esentdatabaseleakinspaceexception-class.md)  
            [EsentDirtyShutdownException （.）](./esentdirtyshutdownexception-class.md)  
            [EsentFileNotFoundException （.）](./esentfilenotfoundexception-class.md)  
            [EsentIndexInUseException （.）](./esentindexinuseexception-class.md)  
            [EsentIndexNotFoundException （.）](./esentindexnotfoundexception-class.md)  
            [EsentInvalidBufferSizeException （.）](./esentinvalidbuffersizeexception-class.md)  
            [EsentInvalidLogDataSequenceException （.）](./esentinvalidlogdatasequenceexception-class.md)  
            [EsentKeyDuplicateException （.）](./esentkeyduplicateexception-class.md)  
            [EsentKeyTruncatedException （.）](./esentkeytruncatedexception-class.md)  
            [EsentLogFileSizeMismatchDatabasesConsistentException （.）](./esentlogfilesizemismatchdatabasesconsistentexception-class.md)  
            [EsentLogSectorSizeMismatchDatabasesConsistentException （.）](./esentlogsectorsizemismatchdatabasesconsistentexception-class.md)  
            [EsentLSNotSetException （.）](./esentlsnotsetexception-class.md)  
            [EsentMissingFullBackupException （.）](./esentmissingfullbackupexception-class.md)  
            [EsentMultiValuedDuplicateAfterTruncationException （.）](./esentmultivaluedduplicateaftertruncationexception-class.md)  
            [EsentMultiValuedDuplicateException （.）](./esentmultivaluedduplicateexception-class.md)  
            [EsentNoAttachmentsFailedIncrementalReseedException （.）](./esentnoattachmentsfailedincrementalreseedexception-class.md)  
            [EsentNoBackupException （.）](./esentnobackupexception-class.md)  
            [EsentNoCurrentRecordException （.）](./esentnocurrentrecordexception-class.md)  
            [EsentObjectNotFoundException （.）](./esentobjectnotfoundexception-class.md)  
            [EsentOSSnapshotNotAllowedException （.）](./esentossnapshotnotallowedexception-class.md)  
            [EsentRecordDeletedException （.）](./esentrecorddeletedexception-class.md)  
            [EsentRecordNotFoundException （.）](./esentrecordnotfoundexception-class.md)  
            [EsentRecordTooBigException （.）](./esentrecordtoobigexception-class.md)  
            [EsentRecordTooBigForBackwardCompatibilityException （.）](./esentrecordtoobigforbackwardcompatibilityexception-class.md)  
            [EsentRecoveredWithErrorsException （.）](./esentrecoveredwitherrorsexception-class.md)  
            [EsentRecoveredWithoutUndoDatabasesConsistentException （.）](./esentrecoveredwithoutundodatabasesconsistentexception-class.md)  
            [EsentRecoveredWithoutUndoException （.）](./esentrecoveredwithoutundoexception-class.md)  
            [EsentRestoreInProgressException （.）](./esentrestoreinprogressexception-class.md)  
            [EsentSeparatedLongValueException （.）](./esentseparatedlongvalueexception-class.md)  
            [EsentSurrogateBackupInProgressException （.）](./esentsurrogatebackupinprogressexception-class.md)  
            [EsentTableDuplicateException （.）](./esenttableduplicateexception-class.md)  
            [EsentTableInUseException （.）](./esenttableinuseexception-class.md)  
            [EsentTestInjectionNotSupportedException （.）](./esenttestinjectionnotsupportedexception-class.md)  
            [EsentWriteConflictException （.）](./esentwriteconflictexception-class.md)  
            [EsentWriteConflictPrimaryIndexException （.）](./esentwriteconflictprimaryindexexception-class.md)
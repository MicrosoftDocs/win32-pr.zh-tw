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
# <a name="esentinconsistentexception-class"></a>EsentInconsistentException 類別

不一致例外狀況的基類。

## <a name="inheritance-hierarchy"></a>繼承階層

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [EsentException。](./esentexception-class.md)  
      [EsentErrorException （.）](./esenterrorexception-class.md)  
        [EsentDataException （.）](./esentdataexception-class.md)  
          EsentInconsistentException （.）  
            

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

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

## <a name="thread-safety"></a>執行緒安全

這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。 並非所有的執行個體成員都是安全執行緒。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[EsentInconsistentException 成員](./esentinconsistentexception-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a>衍生類型

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [EsentException。](./esentexception-class.md)  
      [EsentErrorException （.）](./esenterrorexception-class.md)  
        [EsentDataException （.）](./esentdataexception-class.md)  
          EsentInconsistentException （.）  
            [EsentAttachedDatabaseMismatchException （.）](./esentattacheddatabasemismatchexception-class.md)  
            [EsentBadCheckpointSignatureException （.）](./esentbadcheckpointsignatureexception-class.md)  
            [EsentBadLogSignatureException （.）](./esentbadlogsignatureexception-class.md)  
            [EsentBadLogVersionException （.）](./esentbadlogversionexception-class.md)  
            [EsentCheckpointFileNotFoundException （.）](./esentcheckpointfilenotfoundexception-class.md)  
            [EsentConsistentTimeMismatchException （.）](./esentconsistenttimemismatchexception-class.md)  
            [EsentDatabaseDirtyShutdownException （.）](./esentdatabasedirtyshutdownexception-class.md)  
            [EsentDatabaseIncompleteIncrementalReseedException （.）](./esentdatabaseincompleteincrementalreseedexception-class.md)  
            [EsentDatabaseLogSetMismatchException （.）](./esentdatabaselogsetmismatchexception-class.md)  
            [EsentDbTimeTooNewException （.）](./esentdbtimetoonewexception-class.md)  
            [EsentDbTimeTooOldException （.）](./esentdbtimetoooldexception-class.md)  
            [EsentEndingRestoreLogTooLowException （.）](./esentendingrestorelogtoolowexception-class.md)  
            [EsentExistingLogFileHasBadSignatureException （.）](./esentexistinglogfilehasbadsignatureexception-class.md)  
            [EsentExistingLogFileIsNotContiguousException （.）](./esentexistinglogfileisnotcontiguousexception-class.md)  
            [EsentFileInvalidTypeException （.）](./esentfileinvalidtypeexception-class.md)  
            [EsentGivenLogFileHasBadSignatureException （.）](./esentgivenlogfilehasbadsignatureexception-class.md)  
            [EsentGivenLogFileIsNotContiguousException （.）](./esentgivenlogfileisnotcontiguousexception-class.md)  
            [EsentInvalidCreateDbVersionException （.）](./esentinvalidcreatedbversionexception-class.md)  
            [EsentInvalidDatabaseVersionException （.）](./esentinvaliddatabaseversionexception-class.md)  
            [EsentLogGenerationMismatchException （.）](./esentloggenerationmismatchexception-class.md)  
            [EsentMissingCurrentLogFilesException （.）](./esentmissingcurrentlogfilesexception-class.md)  
            [EsentMissingFileToBackupException （.）](./esentmissingfiletobackupexception-class.md)  
            [EsentMissingRestoreLogFilesException （.）](./esentmissingrestorelogfilesexception-class.md)  
            [EsentPageSizeMismatchException （.）](./esentpagesizemismatchexception-class.md)  
            [EsentRequiredLogFilesMissingException （.）](./esentrequiredlogfilesmissingexception-class.md)  
            [EsentStartingRestoreLogTooHighException （.）](./esentstartingrestorelogtoohighexception-class.md)
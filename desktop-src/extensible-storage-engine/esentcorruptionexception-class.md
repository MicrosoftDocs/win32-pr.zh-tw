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
# <a name="esentcorruptionexception-class"></a>EsentCorruptionException 類別

損毀例外狀況的基類。

## <a name="inheritance-hierarchy"></a>繼承階層

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [EsentException。](./esentexception-class.md)  
      [EsentErrorException （.）](./esenterrorexception-class.md)  
        [EsentDataException （.）](./esentdataexception-class.md)  
          EsentCorruptionException （.）  
            

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

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

## <a name="thread-safety"></a>執行緒安全

這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。 並非所有的執行個體成員都是安全執行緒。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[EsentCorruptionException 成員](./esentcorruptionexception-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a>衍生類型

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [EsentException。](./esentexception-class.md)  
      [EsentErrorException （.）](./esenterrorexception-class.md)  
        [EsentDataException （.）](./esentdataexception-class.md)  
          EsentCorruptionException （.）  
            [EsentBadEmptyPageException （.）](./esentbademptypageexception-class.md)  
            [EsentBadPageLinkException （.）](./esentbadpagelinkexception-class.md)  
            [EsentBadParentPageLinkException （.）](./esentbadparentpagelinkexception-class.md)  
            [EsentCatalogCorruptedException （.）](./esentcatalogcorruptedexception-class.md)  
            [EsentCheckpointCorruptException （.）](./esentcheckpointcorruptexception-class.md)  
            [EsentCommittedLogFileCorruptException （.）](./esentcommittedlogfilecorruptexception-class.md)  
            [EsentCommittedLogFilesMissingException （.）](./esentcommittedlogfilesmissingexception-class.md)  
            [EsentDatabaseBufferDependenciesCorruptedException （.）](./esentdatabasebufferdependenciescorruptedexception-class.md)  
            [EsentDatabaseCorruptedException （.）](./esentdatabasecorruptedexception-class.md)  
            [EsentDbTimeCorruptedException （.）](./esentdbtimecorruptedexception-class.md)  
            [EsentDecompressionFailedException （.）](./esentdecompressionfailedexception-class.md)  
            [EsentDerivedColumnCorruptionException （.）](./esentderivedcolumncorruptionexception-class.md)  
            [EsentDiskReadVerificationFailureException （.）](./esentdiskreadverificationfailureexception-class.md)  
            [EsentFileIOBeyondEOFException （.）](./esentfileiobeyondeofexception-class.md)  
            [EsentFileSystemCorruptionException （.）](./esentfilesystemcorruptionexception-class.md)  
            [EsentIndexBuildCorruptedException （.）](./esentindexbuildcorruptedexception-class.md)  
            [EsentInvalidLogSequenceException （.）](./esentinvalidlogsequenceexception-class.md)  
            [EsentLogCorruptDuringHardRecoveryException （.）](./esentlogcorruptduringhardrecoveryexception-class.md)  
            [EsentLogCorruptDuringHardRestoreException （.）](./esentlogcorruptduringhardrestoreexception-class.md)  
            [EsentLogCorruptedException （.）](./esentlogcorruptedexception-class.md)  
            [EsentLogFileCorruptException （.）](./esentlogfilecorruptexception-class.md)  
            [EsentLogReadVerifyFailureException （.）](./esentlogreadverifyfailureexception-class.md)  
            [EsentLogTornWriteDuringHardRecoveryException （.）](./esentlogtornwriteduringhardrecoveryexception-class.md)  
            [EsentLogTornWriteDuringHardRestoreException （.）](./esentlogtornwriteduringhardrestoreexception-class.md)  
            [EsentLVCorruptedException （.）](./esentlvcorruptedexception-class.md)  
            [EsentMissingLogFileException （.）](./esentmissinglogfileexception-class.md)  
            [EsentMissingPreviousLogFileException （.）](./esentmissingpreviouslogfileexception-class.md)  
            [EsentPageNotInitializedException （.）](./esentpagenotinitializedexception-class.md)  
            [EsentPrimaryIndexCorruptedException （.）](./esentprimaryindexcorruptedexception-class.md)  
            [EsentReadLostFlushVerifyFailureException （.）](./esentreadlostflushverifyfailureexception-class.md)  
            [EsentReadPgnoVerifyFailureException （.）](./esentreadpgnoverifyfailureexception-class.md)  
            [EsentReadVerifyFailureException （.）](./esentreadverifyfailureexception-class.md)  
            [EsentRecordFormatConversionFailedException （.）](./esentrecordformatconversionfailedexception-class.md)  
            [EsentRecoveryVerifyFailureException （.）](./esentrecoveryverifyfailureexception-class.md)  
            [EsentRedoAbruptEndedException （.）](./esentredoabruptendedexception-class.md)  
            [EsentSecondaryIndexCorruptedException （.）](./esentsecondaryindexcorruptedexception-class.md)  
            [EsentSPAvailExtCorruptedException （.）](./esentspavailextcorruptedexception-class.md)  
            [EsentSPOwnExtCorruptedException （.）](./esentspownextcorruptedexception-class.md)
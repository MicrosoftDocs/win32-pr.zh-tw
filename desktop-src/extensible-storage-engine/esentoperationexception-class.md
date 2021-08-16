---
description: 深入瞭解： EsentOperationException 類別
title: EsentOperationException 類別
TOCTitle: EsentOperationException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentOperationException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentoperationexception(v=EXCHG.10)
ms:contentKeyID: 55102414
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentOperationException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentOperationException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bfa501840c276941d39873dd402d0c0cc949c4ecd2d9bccf59c2d0500534861a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118493960"
---
# <a name="esentoperationexception-class"></a>EsentOperationException 類別

作業例外狀況的基類。

## <a name="inheritance-hierarchy"></a>繼承階層

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [EsentException。](./esentexception-class.md)  
      [EsentErrorException （.）](./esenterrorexception-class.md)  
        EsentOperationException （.）  
          

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentOperationException _
    Inherits EsentErrorException
'Usage
Dim instance As EsentOperationException
```

``` csharp
[SerializableAttribute]
public abstract class EsentOperationException : EsentErrorException
```

## <a name="thread-safety"></a>執行緒安全

這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。 並非所有的執行個體成員都是安全執行緒。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[EsentOperationException 成員](./esentoperationexception-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a>衍生類型

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [EsentException。](./esentexception-class.md)  
      [EsentErrorException （.）](./esenterrorexception-class.md)  
        EsentOperationException （.）  
          [EsentBackupAbortByServerException （.）](./esentbackupabortbyserverexception-class.md)  
          [EsentCheckpointDepthTooDeepException （.）](./esentcheckpointdepthtoodeepexception-class.md)  
          [EsentClientRequestToStopJetServiceException （.）](./esentclientrequesttostopjetserviceexception-class.md)  
          [EsentFatalException （.）](./esentfatalexception-class.md)  
          [EsentInitInProgressException （.）](./esentinitinprogressexception-class.md)  
          [EsentInternalErrorException （.）](./esentinternalerrorexception-class.md)  
          [EsentIOException （.）](./esentioexception-class.md)  
          [EsentNTSystemCallFailedException （.）](./esentntsystemcallfailedexception-class.md)  
          [EsentOSSnapshotTimeOutException （.）](./esentossnapshottimeoutexception-class.md)  
          [EsentRecordNotDeletedException （.）](./esentrecordnotdeletedexception-class.md)  
          [EsentResourceException （.）](./esentresourceexception-class.md)  
          [EsentTermInProgressException （.）](./esentterminprogressexception-class.md)  
          [EsentUnicodeLanguageValidationFailureException （.）](./esentunicodelanguagevalidationfailureexception-class.md)  
          [EsentUnicodeTranslationFailException （.）](./esentunicodetranslationfailexception-class.md)
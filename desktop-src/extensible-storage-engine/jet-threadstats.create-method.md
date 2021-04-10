---
description: 深入瞭解： JET_THREADSTATS。Create 方法
title: 'JET_THREADSTATS。建立方法 (的 < a0/&gt; < a1/&gt;) '
TOCTitle: 'Create method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Create(System.Int32,System.Int32,System.Int32,System.Int32,System.Int32,System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats.create(v=EXCHG.10)
ms:contentKeyID: 39509886
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Create
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Create
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: beaaee85fc0f6c331db1d813280d4b900e39fb54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103694303"
---
# <a name="jet_threadstatscreate-method"></a>JET_THREADSTATS。Create 方法

使用指定的值建立新的 [JET_THREADSTATS](./jet-threadstats-structure2.md) 結構。

**命名空間：**[Microsoft. Isam](./microsoft.isam.esent.interop.vista-namespace.md) 。    
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Shared Function Create ( _
    cPageReferenced As Integer, _
    cPageRead As Integer, _
    cPagePreread As Integer, _
    cPageDirtied As Integer, _
    cPageRedirtied As Integer, _
    cLogRecord As Integer, _
    cbLogRecord As Integer _
) As JET_THREADSTATS
'Usage
Dim cPageReferenced As Integer
Dim cPageRead As Integer
Dim cPagePreread As Integer
Dim cPageDirtied As Integer
Dim cPageRedirtied As Integer
Dim cLogRecord As Integer
Dim cbLogRecord As Integer
Dim returnValue As JET_THREADSTATS

returnValue = JET_THREADSTATS.Create(cPageReferenced, _
    cPageRead, cPagePreread, cPageDirtied, _
    cPageRedirtied, cLogRecord, cbLogRecord)
```

``` csharp
public static JET_THREADSTATS Create(
    int cPageReferenced,
    int cPageRead,
    int cPagePreread,
    int cPageDirtied,
    int cPageRedirtied,
    int cLogRecord,
    int cbLogRecord
)
```

#### <a name="parameters"></a>參數

  - cPageReferenced  
    類型： [system.object](/dotnet/api/system.int32)  
    
    造訪的頁面數目。

<!-- end list -->

  - cPageRead  
    類型： [system.object](/dotnet/api/system.int32)  
    
    讀取的頁面數目。

<!-- end list -->

  - cPagePreread  
    類型： [system.object](/dotnet/api/system.int32)  
    
    Preread 的頁面數目。

<!-- end list -->

  - cPageDirtied  
    類型： [system.object](/dotnet/api/system.int32)  
    
    TNumber 的頁面變動總數。

<!-- end list -->

  - cPageRedirtied  
    類型： [system.object](/dotnet/api/system.int32)  
    
    Redirtied 的頁面數目。

<!-- end list -->

  - cLogRecord  
    類型： [system.object](/dotnet/api/system.int32)  
    
    產生的記錄檔記錄數目。

<!-- end list -->

  - cbLogRecord  
    類型： [system.object](/dotnet/api/system.int32)  
    
    寫入的記錄檔記錄位元組數。

#### <a name="return-value"></a>傳回值

類型： [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)  
具有指定值的新 [JET_THREADSTATS](./jet-threadstats-structure2.md) 結構。  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_THREADSTATS 結構](./jet-threadstats-structure2.md)

[JET_THREADSTATS 成員](./jet-threadstats-members.md)

[Microsoft.Isam.Esent.Interop.Vista namespace](./microsoft.isam.esent.interop.vista-namespace.md)

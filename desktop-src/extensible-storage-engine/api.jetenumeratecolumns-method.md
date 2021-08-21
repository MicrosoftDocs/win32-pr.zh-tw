---
description: 深入瞭解： JetEnumerateColumns 方法
title: JetEnumerateColumns 方法
TOCTitle: 'JetEnumerateColumns method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetEnumerateColumns(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Int32,Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID[],System.Int32@,Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN[]@,Microsoft.Isam.Esent.Interop.JET_PFNREALLOC,System.IntPtr,System.Int32,Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetenumeratecolumns(v=EXCHG.10)
ms:contentKeyID: 55100695
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetEnumerateColumns
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetEnumerateColumns
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 713b02835aa063e888a2385df9bd8abdff9af1300a2e9885c06e995f2b814bbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119042706"
---
# <a name="apijetenumeratecolumns-method"></a>JetEnumerateColumns 方法

有效率地從資料指標的目前記錄或該資料指標的複製緩衝區，抓取一組資料行和其值。 您可以使用資料行識別碼、itagSequence 數位和其他特性的清單來限制抓取的資料行和值。 此資料行抓取 API 是唯一的，因為它會將資訊傳回給動態配置的記憶體，而這些記憶體是使用使用者提供的 realloc 相容回呼所取得。 這項新的彈性可讓您有效率地抓取具有特定特性 (的資料行資料，例如呼叫端未知) 大小和多重性。 如此一來，就不需要使用 JetRetrieveColumn 的探索模式來判斷這些特性，以便設定 JetRetrieveColumn 的最後一個呼叫，以成功取得所需的資料。

此 API 不符合 CLS 規範。 

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Function JetEnumerateColumns ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    numColumnids As Integer, _
    columnids As JET_ENUMCOLUMNID(), _
    <OutAttribute> ByRef numColumnValues As Integer, _
    <OutAttribute> ByRef columnValues As JET_ENUMCOLUMN(), _
    allocator As JET_PFNREALLOC, _
    allocatorContext As IntPtr, _
    maxDataSize As Integer, _
    grbit As EnumerateColumnsGrbit _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim numColumnids As Integer
Dim columnids As JET_ENUMCOLUMNID()
Dim numColumnValues As Integer
Dim columnValues As JET_ENUMCOLUMN()
Dim allocator As JET_PFNREALLOC
Dim allocatorContext As IntPtr
Dim maxDataSize As Integer
Dim grbit As EnumerateColumnsGrbit
Dim returnValue As JET_wrn

returnValue = Api.JetEnumerateColumns(sesid, _
    tableid, numColumnids, columnids, _
    numColumnValues, columnValues, allocator, _
    allocatorContext, maxDataSize, grbit)
```

``` csharp
[CLSCompliantAttribute(false)]
public static JET_wrn JetEnumerateColumns(
    JET_SESID sesid,
    JET_TABLEID tableid,
    int numColumnids,
    JET_ENUMCOLUMNID[] columnids,
    out int numColumnValues,
    out JET_ENUMCOLUMN[] columnValues,
    JET_PFNREALLOC allocator,
    IntPtr allocatorContext,
    int maxDataSize,
    EnumerateColumnsGrbit grbit
)
```

#### <a name="parameters"></a>參數

  - sesid  
    類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    要使用的會話。

<!-- end list -->

  - tableid  
    類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    要從中取出資料的資料指標。

<!-- end list -->

  - numColumnids  
    類型： [system.object](/dotnet/api/system.int32)  
    
    JET_ENUMCOLUMNIDS 的數目。

<!-- end list -->

  - columnids  
    類型： \[\]  
    
    一個選擇性的資料行識別碼陣列，每個都有一個選擇性的 itagSequence 數位陣列來列舉。

<!-- end list -->

  - numColumnValues  
    類型： [system.object](/dotnet/api/system.int32)  
    
    傳回抓取的資料行值數目。

<!-- end list -->

  - columnValues  
    類型： \[\]  
    
    傳回列舉的資料行值。

<!-- end list -->

  - allocator  
    類型： [Microsoft.Isam.Esent.Interop.JET_PFNREALLOC](./jet-pfnrealloc-delegate.md)  
    
    用來配置記憶體的回呼。

<!-- end list -->

  - allocatorCoNtext  
    類型： [system.object](/dotnet/api/system.intptr)  
    
    配置回呼的內容。

<!-- end list -->

  - maxDataSize  
    類型： [system.object](/dotnet/api/system.int32)  
    
    設定要從長文字或長二進位資料行傳回的資料量上限。 您可以使用這個參數來防止列舉非常大的資料行值。

<!-- end list -->

  - grbit  
    型別： [EnumerateColumnsGrbit](./enumeratecolumnsgrbit-enumeration.md) 。  
    
    取出選項。

#### <a name="return-value"></a>傳回值

類型： [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)  
警告或成功。  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Api 類別](./api-class.md)

[Api 成員](./api-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)

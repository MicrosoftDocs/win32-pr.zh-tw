---
description: 深入瞭解： JET_cbtyp 列舉
title: JET_cbtyp 列舉
TOCTitle: JET_cbtyp enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_cbtyp
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_cbtyp(v=EXCHG.10)
ms:contentKeyID: 39511758
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_cbtyp.BeforeDelete
- Microsoft.Isam.Esent.Interop.JET_cbtyp.Finalize
- Microsoft.Isam.Esent.Interop.JET_cbtyp.OnlineDefragCompleted
- Microsoft.Isam.Esent.Interop.JET_cbtyp.UserDefinedDefaultValue
- Microsoft.Isam.Esent.Interop.JET_cbtyp
- Microsoft.Isam.Esent.Interop.JET_cbtyp.AfterDelete
- Microsoft.Isam.Esent.Interop.JET_cbtyp.FreeCursorLS
- Microsoft.Isam.Esent.Interop.JET_cbtyp.AfterReplace
- Microsoft.Isam.Esent.Interop.JET_cbtyp.FreeTableLS
- Microsoft.Isam.Esent.Interop.JET_cbtyp.Null
- Microsoft.Isam.Esent.Interop.JET_cbtyp.BeforeReplace
- Microsoft.Isam.Esent.Interop.JET_cbtyp.BeforeInsert
- Microsoft.Isam.Esent.Interop.JET_cbtyp.AfterInsert
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_cbtyp.BeforeReplace
- Microsoft.Isam.Esent.Interop.JET_cbtyp.FreeCursorLS
- Microsoft.Isam.Esent.Interop.JET_cbtyp.FreeTableLS
- Microsoft.Isam.Esent.Interop.JET_cbtyp.BeforeDelete
- Microsoft.Isam.Esent.Interop.JET_cbtyp.Null
- Microsoft.Isam.Esent.Interop.JET_cbtyp.AfterReplace
- Microsoft.Isam.Esent.Interop.JET_cbtyp
- Microsoft.Isam.Esent.Interop.JET_cbtyp.AfterDelete
- Microsoft.Isam.Esent.Interop.JET_cbtyp.OnlineDefragCompleted
- Microsoft.Isam.Esent.Interop.JET_cbtyp.AfterInsert
- Microsoft.Isam.Esent.Interop.JET_cbtyp.BeforeInsert
- Microsoft.Isam.Esent.Interop.JET_cbtyp.Finalize
- Microsoft.Isam.Esent.Interop.JET_cbtyp.UserDefinedDefaultValue
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3d2e545fea9c1942dc09df82eb93eafa1d3e4e89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106976770"
---
# <a name="jet_cbtyp-enumeration"></a>JET_cbtyp 列舉

要報告的進度類型。

此列舉有 [FlagsAttribute](/dotnet/api/system.flagsattribute) 屬性，因此其成員值可進行位元組合。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration JET_cbtyp
'Usage
Dim instance As JET_cbtyp
```

``` csharp
[FlagsAttribute]
public enum JET_cbtyp
```

## <a name="members"></a>成員

<table>
<thead>
<tr class="header">
<th></th>
<th>成員名稱</th>
<th>說明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td>Null</td>
<td>這是保留的回呼，而且一律視為無效。</td>
</tr>
<tr class="even">
<td></td>
<td>定案</td>
<td>可結束的資料行已離開零。</td>
</tr>
<tr class="odd">
<td></td>
<td>BeforeInsert</td>
<td>這項回呼會在透過呼叫 JetUpdate 將新的記錄插入資料表之前進行。</td>
</tr>
<tr class="even">
<td></td>
<td>AfterInsert</td>
<td>只要呼叫 JetUpdate，但在 JetUpdate 傳回之前，會將新的記錄插入資料表中，就會發生此回呼。</td>
</tr>
<tr class="odd">
<td></td>
<td>BeforeReplace</td>
<td>這項回呼會在 JetUpdate 的呼叫變更資料表中的現有記錄之前發生。</td>
</tr>
<tr class="even">
<td></td>
<td>AfterReplace</td>
<td>這項回呼將會在資料表中的現有記錄已由呼叫 JetUpdate，但在 JetUpdate 傳回之前變更。</td>
</tr>
<tr class="odd">
<td></td>
<td>BeforeDelete</td>
<td>這項回呼會在呼叫 JetDelete 來刪除資料表中的現有記錄之前發生。</td>
</tr>
<tr class="even">
<td></td>
<td>AfterDelete</td>
<td>這項回呼會在 JetDelete 的呼叫刪除資料表中的現有記錄之後發生。</td>
</tr>
<tr class="odd">
<td></td>
<td>UserDefinedDefaultValue</td>
<td>當引擎需要從應用程式取得使用者定義的資料行預設值時，就會發生此回呼。 此回呼基本上是由應用程式評估的 JetRetrieveColumn 有限實作為。 最多可以針對使用者定義的預設值傳回一個資料行值。</td>
</tr>
<tr class="even">
<td></td>
<td>OnlineDefragCompleted</td>
<td>當 JetDefragment 所起始的資料庫線上磁碟重組已停止，因為進程已完成或達到時間限制時，就會發生此回呼。</td>
</tr>
<tr class="odd">
<td></td>
<td>FreeCursorLS</td>
<td>當應用程式需要清除與資料庫引擎所釋放之資料指標相關聯之本機儲存體的內容控制碼時，就會發生此回呼。 如需詳細資訊，請參閱 JetSetLS。 此回呼原因的委派是透過 JET_paramRuntimeCallback 的 JetSetSystemParameter 來設定。</td>
</tr>
<tr class="even">
<td></td>
<td>FreeTableLS</td>
<td>這項回呼的原因是，應用程式必須清除與資料庫引擎所釋放之資料表相關聯之本機儲存體的內容控制碼。 如需詳細資訊，請參閱 JetSetLS。 此回呼原因的委派是透過 JET_paramRuntimeCallback 的 JetSetSystemParameter 來設定。</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)

---
description: 深入瞭解： SetCurrentIndexGrbit 列舉
title: SetCurrentIndexGrbit 列舉
TOCTitle: SetCurrentIndexGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.setcurrentindexgrbit(v=EXCHG.10)
ms:contentKeyID: 39515072
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit.MoveFirst
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit.NoMove
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit.None
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit.NoMove
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit.MoveFirst
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ee060e73208219408b278e325d2ecf21c36e50975fc5d72e7723fab344b9459b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119107262"
---
# <a name="setcurrentindexgrbit-enumeration"></a>SetCurrentIndexGrbit 列舉

[JetSetCurrentIndex2 (JET_SESID、JET_TABLEID、string、SetCurrentIndexGrbit) ](./api.jetsetcurrentindex2-method.md)和[JetSetCurrentIndex3 (JET_SESID、JET_TABLEID、string、SetCurrentIndexGrbit、Int32) ](./api.jetsetcurrentindex3-method.md)的選項。

此列舉有 [FlagsAttribute](/dotnet/api/system.flagsattribute) 屬性，因此其成員值可進行位元組合。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration SetCurrentIndexGrbit
'Usage
Dim instance As SetCurrentIndexGrbit
```

``` csharp
[FlagsAttribute]
public enum SetCurrentIndexGrbit
```

## <a name="members"></a>成員

<table>
<thead>
<tr class="header">
<th></th>
<th>成員名稱</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td>無</td>
<td>預設選項。 這與 MoveFirst 相同。</td>
</tr>
<tr class="even">
<td></td>
<td>MoveFirst</td>
<td>表示資料指標應放置在指定之索引的第一個專案。 如果選取目前的索引，則會忽略此選項。</td>
</tr>
<tr class="odd">
<td></td>
<td>NoMove</td>
<td>表示資料指標應放置在新索引的索引項目上，此索引會對應到舊索引上資料指標目前位置的索引項目相關記錄。</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)

---
description: 深入瞭解： JET_prep 列舉
title: JET_prep 列舉
TOCTitle: JET_prep enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_prep
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_prep(v=EXCHG.10)
ms:contentKeyID: 39510193
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_prep.Replace
- Microsoft.Isam.Esent.Interop.JET_prep.InsertCopy
- Microsoft.Isam.Esent.Interop.JET_prep.Cancel
- Microsoft.Isam.Esent.Interop.JET_prep.Insert
- Microsoft.Isam.Esent.Interop.JET_prep.InsertCopyDeleteOriginal
- Microsoft.Isam.Esent.Interop.JET_prep
- Microsoft.Isam.Esent.Interop.JET_prep.ReplaceNoLock
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_prep.InsertCopyDeleteOriginal
- Microsoft.Isam.Esent.Interop.JET_prep.ReplaceNoLock
- Microsoft.Isam.Esent.Interop.JET_prep
- Microsoft.Isam.Esent.Interop.JET_prep.Cancel
- Microsoft.Isam.Esent.Interop.JET_prep.InsertCopy
- Microsoft.Isam.Esent.Interop.JET_prep.Insert
- Microsoft.Isam.Esent.Interop.JET_prep.Replace
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: edeaef8144fe6e13674ec6d3dfcb8adf7522e148
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996901"
---
# <a name="jet_prep-enumeration"></a>JET_prep 列舉

更新 JetPrepareUpdate 的類型。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Enumeration JET_prep
'Usage
Dim instance As JET_prep
```

``` csharp
public enum JET_prep
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
<td>插入</td>
<td>此旗標會讓資料指標準備插入新的記錄。 所有資料都會初始化為記錄的預設狀態。 如果資料表具有自動遞增資料行，就會將新的值指派給此記錄，而不論更新最終成功、失敗或已取消。</td>
</tr>
<tr class="even">
<td></td>
<td>取代</td>
<td>此旗標會讓資料指標準備取代目前的記錄。 如果資料表有版本資料行，則 [版本] 欄會設定為其序列中的下一個值。 如果此更新未完成，則記錄中的版本值不會受到影響。 記錄上會執行更新鎖定，以防止其他會話在此會話完成之前更新此記錄。</td>
</tr>
<tr class="odd">
<td></td>
<td>取消</td>
<td>此旗標會使 JetPrepareUpdate 取消此資料指標的更新。</td>
</tr>
<tr class="even">
<td></td>
<td>ReplaceNoLock</td>
<td>此旗標類似于 JET_prepReplace，但不會採取任何鎖定來防止其他會話更新此記錄。 相反地，此會話可能會在呼叫 JetUpdate 來完成更新時收到 JET_errWriteConflict。</td>
</tr>
<tr class="odd">
<td></td>
<td>InsertCopy</td>
<td>此旗標會讓資料指標準備插入現有記錄的複本。 如果使用此選項，則必須要有目前的記錄。 新記錄的初始狀態會從目前記錄複製。 幾乎會複製儲存在登出的 Long 值。</td>
</tr>
<tr class="even">
<td></td>
<td>InsertCopyDeleteOriginal</td>
<td>此旗標會讓資料指標準備插入相同的記錄，以及刪除或原始記錄。 當主要金鑰已變更時，就會使用它。</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)

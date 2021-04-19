---
description: 深入瞭解： OpenTableGrbit 列舉
title: OpenTableGrbit 列舉
TOCTitle: OpenTableGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.OpenTableGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.opentablegrbit(v=EXCHG.10)
ms:contentKeyID: 39510721
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.NoCache
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.DenyWrite
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.DenyRead
- Microsoft.Isam.Esent.Interop.OpenTableGrbit
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.Updatable
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.Preread
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass9
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass15
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass6
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass14
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass3
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass8
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass7
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.Sequential
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass5
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass2
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.ReadOnly
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass4
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.None
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass10
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass13
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass12
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass1
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.PermitDDL
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass11
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass1
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass11
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass14
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.Sequential
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass2
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass5
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass8
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.DenyRead
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.DenyWrite
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.PermitDDL
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass10
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass12
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass3
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.NoCache
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass9
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.Updatable
- Microsoft.Isam.Esent.Interop.OpenTableGrbit
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.None
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass4
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass7
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.Preread
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.ReadOnly
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass13
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass15
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass6
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: dfb2d75fc17e37dc669acf1fd84f38c957d467f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985176"
---
# <a name="opentablegrbit-enumeration"></a>OpenTableGrbit 列舉

JetOpenTable 的選項。

此列舉有 [FlagsAttribute](/dotnet/api/system.flagsattribute) 屬性，因此其成員值可進行位元組合。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration OpenTableGrbit
'Usage
Dim instance As OpenTableGrbit
```

``` csharp
[FlagsAttribute]
public enum OpenTableGrbit
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
<td>預設選項。</td>
</tr>
<tr class="even">
<td></td>
<td>DenyWrite</td>
<td>無法開啟此資料表以供另一個會話進行寫入存取。</td>
</tr>
<tr class="odd">
<td></td>
<td>DenyRead</td>
<td>此資料表無法由另一個會話開啟以供讀取存取。</td>
</tr>
<tr class="even">
<td></td>
<td>ReadOnly</td>
<td>要求資料表的唯讀存取權。</td>
</tr>
<tr class="odd">
<td></td>
<td>可更新</td>
<td>要求資料表的寫入存取權。</td>
</tr>
<tr class="even">
<td></td>
<td>PermitDDL</td>
<td>允許對標示為 FixedDDL 的資料表進行 DDL 修改。 此選項必須與 DenyRead 搭配使用。</td>
</tr>
<tr class="odd">
<td></td>
<td>NoCache</td>
<td>不要快取此資料表的頁面。</td>
</tr>
<tr class="even">
<td></td>
<td>Preread</td>
<td>提供資料表可能不在緩衝區快取中的提示，而且預先讀取可能會對效能有所説明。</td>
</tr>
<tr class="odd">
<td></td>
<td>循序</td>
<td>假設順序存取模式和預先提取的資料庫頁面。</td>
</tr>
<tr class="even">
<td></td>
<td>TableClass1</td>
<td>資料表屬於 stats 類別1。</td>
</tr>
<tr class="odd">
<td></td>
<td>TableClass2</td>
<td>資料表屬於 stats 類別2。</td>
</tr>
<tr class="even">
<td></td>
<td>TableClass3</td>
<td>資料表屬於 stats 類別3。</td>
</tr>
<tr class="odd">
<td></td>
<td>TableClass4</td>
<td>資料表屬於 stats 類別4。</td>
</tr>
<tr class="even">
<td></td>
<td>TableClass5</td>
<td>資料表屬於 stats 類別5。</td>
</tr>
<tr class="odd">
<td></td>
<td>TableClass6</td>
<td>資料表屬於 stats 類別6。</td>
</tr>
<tr class="even">
<td></td>
<td>TableClass7</td>
<td>資料表屬於 stats 類別7。</td>
</tr>
<tr class="odd">
<td></td>
<td>TableClass8</td>
<td>資料表屬於 stats 類別8。</td>
</tr>
<tr class="even">
<td></td>
<td>TableClass9</td>
<td>資料表屬於 stats 類別9。</td>
</tr>
<tr class="odd">
<td></td>
<td>TableClass10</td>
<td>資料表屬於 stats 類別10。</td>
</tr>
<tr class="even">
<td></td>
<td>TableClass11</td>
<td>資料表屬於 stats 類別11。</td>
</tr>
<tr class="odd">
<td></td>
<td>TableClass12</td>
<td>資料表屬於 stats 類別12。</td>
</tr>
<tr class="even">
<td></td>
<td>TableClass13</td>
<td>資料表屬於 stats 類別13。</td>
</tr>
<tr class="odd">
<td></td>
<td>TableClass14</td>
<td>資料表屬於 stats 類別14。</td>
</tr>
<tr class="even">
<td></td>
<td>TableClass15</td>
<td>資料表屬於 stats 類別15。</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)

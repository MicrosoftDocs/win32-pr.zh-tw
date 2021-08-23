---
description: 深入瞭解： JET_ENUMCOLUMN 屬性
title: JET_ENUMCOLUMN 屬性
TOCTitle: JET_ENUMCOLUMN properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumn_properties(v=EXCHG.10)
ms:contentKeyID: 55103495
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: ee11c050d558fbefb15be4783a08b1808744718d043de038b297fdc5ebd9e3fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119667918"
---
# <a name="jet_enumcolumn-properties"></a>JET_ENUMCOLUMN 屬性

包含受保護的成員  
包含繼承的成員  

[JET_ENUMCOLUMN](./jet-enumcolumn-class.md)類型會公開下列成員。

## <a name="properties"></a>屬性

<table>
<thead>
<tr class="header">
<th> </th>
<th>名稱</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn335137(v=exchg.10).md">cbData</a></td>
<td>取得為數據行列舉之值的大小。 只有當 <a href="dn335086(v=exchg.10).md">err</a> 等於 <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>時，才會使用這個成員。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn335085(v=exchg.10).md">cEnumColumnValue</a></td>
<td>取得針對資料行列舉的資料行值數目。 只有在未<a href="hh557250(v=exchg.10).md">ColumnSingleValue</a> <a href="dn335086(v=exchg.10).md">err</a>時，才會使用這個成員。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn335135(v=exchg.10).md">columnid</a></td>
<td>取得已列舉的 columnid 識別碼。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn335086(v=exchg.10).md">犯 錯</a></td>
<td>取得列舉所產生的資料行狀態碼。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn335087(v=exchg.10).md">pvData</a></td>
<td>取得為數據行列舉的值。 只有當 <a href="dn335086(v=exchg.10).md">err</a> 等於 <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>時，才會使用這個成員。 這會指向傳遞給<a href="dn292148(v=exchg.10).md">JetEnumerateColumns (JET_SESID、JET_TABLEID、Int32、[]、int32、[]、JET_PFNREALLOC、IntPtr、int32、EnumerateColumnsGrbit) </a>的<a href="hh566077(v=exchg.10).md">JET_PFNREALLOC</a>配置器回呼所配置的記憶體。 請記得在完成時釋放記憶體。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn335089(v=exchg.10).md">rgEnumColumnValue</a></td>
<td>取得資料行的列舉資料行值。 只有在未<a href="hh557250(v=exchg.10).md">ColumnSingleValue</a> <a href="dn335086(v=exchg.10).md">err</a>時，才會使用這個成員。</td>
</tr>
</tbody>
</table>


頁首

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_ENUMCOLUMN 類別](./jet-enumcolumn-class.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)

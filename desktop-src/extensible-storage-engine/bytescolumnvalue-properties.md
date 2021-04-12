---
description: 深入瞭解： BytesColumnValue 屬性
title: BytesColumnValue 屬性
TOCTitle: BytesColumnValue properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.BytesColumnValue
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.bytescolumnvalue_properties(v=EXCHG.10)
ms:contentKeyID: 55100964
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: bafae34a3fa6dac29cc504ebe9a34c0abd7b870a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104321008"
---
# <a name="bytescolumnvalue-properties"></a>BytesColumnValue 屬性

包含受保護的成員  
包含繼承的成員  

[BytesColumnValue](./bytescolumnvalue-class.md)類型會公開下列成員。

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
<td><a href="dn334166(v=exchg.10).md">Columnid</a></td>
<td>取得或設定要設定或取出的 columnid。  (繼承自 <a href="dn334206(v=exchg.10).md">ColumnValue</a>。 ) </td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn334212(v=exchg.10).md">錯誤</a></td>
<td>取得藉由取得或設定此資料行所產生的警告。  (繼承自 <a href="dn334206(v=exchg.10).md">ColumnValue</a>。 ) </td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn334165(v=exchg.10).md">ItagSequence</a></td>
<td>取得或設定資料行 itag 序列。  (繼承自 <a href="dn334206(v=exchg.10).md">ColumnValue</a>。 ) </td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn334126(v=exchg.10).md">長度</a></td>
<td>取得資料行值的位元組長度，如果資料行是 null，則為零，否則會符合位元組陣列的實際長度。  (覆寫 <a href="dn334213(v=exchg.10).md">ColumnValue。</a>) </td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn334169(v=exchg.10).md">RetrieveGrbit</a></td>
<td>取得或設定資料行抓取選項。  (繼承自 <a href="dn334206(v=exchg.10).md">ColumnValue</a>。 ) </td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn334215(v=exchg.10).md">SetGrbit</a></td>
<td>取得或設定資料行更新選項。  (繼承自 <a href="dn334206(v=exchg.10).md">ColumnValue</a>。 ) </td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.protproperty(exchg.10).gif" title="受保護的屬性" alt="Protected property" /></td>
<td><a href="dn334176(v=exchg.10).md">大小</a></td>
<td>取得資料行中值的大小。 這會針對可變大小的資料行傳回0， (即二進位和字串) 。  (覆寫 <a href="dn334172(v=exchg.10).md">ColumnValue。大小</a>) </td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn334129(v=exchg.10).md">值</a></td>
<td>取得或設定資料行的值。 使用 <a href="dn334138(v=exchg.10).md">SetColumns (JET_SESID、JET_TABLEID、[] ) </a> 來更新具有資料行值的記錄。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn334177(v=exchg.10).md">ValueAsObject</a></td>
<td>取得資料行的最後一個設定或抓取值。 此值會以泛型物件的形式傳回。  (覆寫 <a href="dn334214(v=exchg.10).md">ColumnValue. ValueAsObject</a>) </td>
</tr>
</tbody>
</table>


頁首

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[BytesColumnValue 類別](./bytescolumnvalue-class.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)

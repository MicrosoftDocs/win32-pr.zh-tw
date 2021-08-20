---
description: 深入瞭解： BytesColumnValue 成員
title: BytesColumnValue 成員
TOCTitle: BytesColumnValue members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.BytesColumnValue
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.bytescolumnvalue_members(v=EXCHG.10)
ms:contentKeyID: 55100914
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: b5c82031298f5cf1bee82e424401bb8994a414353c1ccd04cb8aa0fbb75ac557
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118084147"
---
# <a name="bytescolumnvalue-members"></a>BytesColumnValue 成員

包含受保護的成員  
包含繼承的成員  

位元組陣列資料行值。

[BytesColumnValue](./bytescolumnvalue-class.md)類型會公開下列成員。

## <a name="constructors"></a>建構函式

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
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><a href="dn334168(v=exchg.10).md">BytesColumnValue</a></td>
<td></td>
</tr>
</tbody>
</table>


頁首

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

## <a name="methods"></a>方法

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
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">等於</a></td>
<td> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">完成</a></td>
<td> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></td>
<td> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></td>
<td> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><a href="dn334173(v=exchg.10).md">GetValueFromBytes</a></td>
<td>從 ESENT 取出資料，將資料解碼，並設定 ColumnValue 物件中的值。  (覆寫 <a href="dn334208(v=exchg.10).md">ColumnValue. GetValueFromBytes ( []，int32，int32，int32) </a>。 ) </td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></td>
<td> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><a href="dn334124(v=exchg.10).md">ToString</a></td>
<td>傳回表示目前<a href="dn334170(v=exchg.10).md">BytesColumnValue</a>的<a href="/dotnet/api/system.string">字串</a>。  (覆寫 <a href="dn334163(v=exchg.10).md">ColumnValue () </a>。 ) </td>
</tr>
</tbody>
</table>


頁首

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[BytesColumnValue 類別](./bytescolumnvalue-class.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)

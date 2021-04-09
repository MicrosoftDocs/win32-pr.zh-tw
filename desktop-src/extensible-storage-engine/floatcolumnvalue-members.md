---
description: 深入瞭解： FloatColumnValue 成員
title: FloatColumnValue 成員
TOCTitle: FloatColumnValue members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.FloatColumnValue
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.floatcolumnvalue_members(v=EXCHG.10)
ms:contentKeyID: 55103206
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 04d30d4dbbbbb5e9559b691020d0526e19a87909
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943744"
---
# <a name="floatcolumnvalue-members"></a>FloatColumnValue 成員

包含受保護的成員  
包含繼承的成員  

[單一](/dotnet/api/system.single)資料行值。

[FloatColumnValue](./floatcolumnvalue-class.md)類型會公開下列成員。

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
<td><a href="dn350899(v=exchg.10).md">FloatColumnValue</a></td>
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
<td><a href="dn334225(v=exchg.10).md">長度</a></td>
<td>取得資料行值的位元組長度，如果資料行是 null，則為零，否則會符合此固定大小資料行的大小。  (繼承自<a href="dn334171(v=exchg.10).md">ColumnValueOfStruct &lt; T &gt; </a>. ) </td>
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
<td><a href="dn350901(v=exchg.10).md">大小</a></td>
<td>取得資料行中值的大小。 這會針對可變大小的資料行傳回0， (即二進位和字串) 。  (覆寫 <a href="dn334172(v=exchg.10).md">ColumnValue。大小</a>) </td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn334180(v=exchg.10).md">值</a></td>
<td>取得或設定結構中的值。  (繼承自<a href="dn334171(v=exchg.10).md">ColumnValueOfStruct &lt; T &gt; </a>. ) </td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn334226(v=exchg.10).md">ValueAsObject</a></td>
<td>取得資料行的最後一個設定或抓取值。 此值會以泛型物件的形式傳回。  (繼承自<a href="dn334171(v=exchg.10).md">ColumnValueOfStruct &lt; T &gt; </a>. ) </td>
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
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><a href="dn334178(v=exchg.10).md">CheckDataCount</a></td>
<td>請確定已抓取的資料完全是結構所需的大小。 如果有不相符的，則會擲回例外狀況。  (繼承自<a href="dn334171(v=exchg.10).md">ColumnValueOfStruct &lt; T &gt; </a>. ) </td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">等於</a></td>
<td> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">完成</a></td>
<td> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></td>
<td> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></td>
<td> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><a href="dn350900(v=exchg.10).md">GetValueFromBytes</a></td>
<td>從 ESENT 取出資料，將資料解碼，並設定 ColumnValue 物件中的值。  (覆寫 <a href="dn334208(v=exchg.10).md">ColumnValue. GetValueFromBytes ( []，int32，int32，int32) </a>。 ) </td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></td>
<td> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><a href="dn334223(v=exchg.10).md">ToString</a></td>
<td>取得這個物件的字串表示。  (繼承自<a href="dn334171(v=exchg.10).md">ColumnValueOfStruct &lt; T &gt; </a>. ) </td>
</tr>
</tbody>
</table>


頁首

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[FloatColumnValue 類別](./floatcolumnvalue-class.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)

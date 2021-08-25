---
description: 深入瞭解： JET_ENUMCOLUMNID 成員
title: JET_ENUMCOLUMNID 成員
TOCTitle: JET_ENUMCOLUMNID members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumnid_members(v=EXCHG.10)
ms:contentKeyID: 55103504
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 6aa360dce8b406e217496ad848be54992a71eaae04d375b2546ca08b75b1e751
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119891308"
---
# <a name="jet_enumcolumnid-members"></a>JET_ENUMCOLUMNID 成員

包含受保護的成員  
包含繼承的成員  

當使用 JetEnumerateColumns 函式時，列舉一組特定的資料行，並選擇性地列舉這些資料行的一組特定的多重值。 JetEnumerateColumns 會選擇性地採用 JET_ENUMCOLUMNID 結構的陣列。

[JET_ENUMCOLUMNID](./jet-enumcolumnid-class.md)類型會公開下列成員。

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
<td><a href="dn335140(v=exchg.10).md">JET_ENUMCOLUMNID</a></td>
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
<td><a href="dn335141(v=exchg.10).md">columnid</a></td>
<td>取得或設定要列舉的 columnid 識別碼。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn335092(v=exchg.10).md">ctagSequence</a></td>
<td>取得或設定以一為基礎的索引) 所 (的資料行值計數，以列舉指定的資料行識別碼。 如果 ctagSequence 為 0 (零) 則會忽略 rgtagSequence，並且會列舉指定之資料行識別碼的所有資料行值。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn335093(v=exchg.10).md">rgtagSequence</a></td>
<td>取得或設定指定資料行的資料行值陣列中，以一個為基底的索引陣列。 單一元素是 JET_RETRIEVECOLUMN 中定義的 itagSequence。 ItagSequence 0 (零) 表示 &quot; skip &quot; 。 1的 itagSequence 表示會傳回資料行的第一個資料行值，2表示第二個數據行的值，依此類推。</td>
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
<td><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></td>
<td> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><a href="dn335091(v=exchg.10).md">ToString</a></td>
<td>傳回表示目前<a href="dn335139(v=exchg.10).md">JET_ENUMCOLUMNID</a>的<a href="/dotnet/api/system.string">字串</a>。  (會覆寫 <a href="/dotnet/api/system.object.tostring#System_Object_ToString">物件 ToString () </a>。 ) </td>
</tr>
</tbody>
</table>


頁首

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_ENUMCOLUMNID 類別](./jet-enumcolumnid-class.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)

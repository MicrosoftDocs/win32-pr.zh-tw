---
description: 深入瞭解： JET_RETINFO 成員
title: JET_RETINFO 成員
TOCTitle: JET_RETINFO members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_RETINFO
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_retinfo_members(v=EXCHG.10)
ms:contentKeyID: 55103864
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: ede4e140cd3b70d7bb6364896a766f506ebde44465f879c6adbffff6febcf571
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118979668"
---
# <a name="jet_retinfo-members"></a>JET_RETINFO 成員

包含受保護的成員  
包含繼承的成員  

包含 JetRetrieveColumn 的選擇性輸入和輸出參數。

[JET_RETINFO](./jet-retinfo-class.md)類型會公開下列成員。

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
<td><a href="dn351023(v=exchg.10).md">JET_RETINFO</a></td>
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
<td><a href="dn335221(v=exchg.10).md">columnidNextTagged</a></td>
<td>藉由將0傳遞為 JetRetrieveColumn 的 columnid，來取得所有標記的資料行時，取得已標記、多重值或稀疏資料行的 columnid。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn335220(v=exchg.10).md">ibLongValue</a></td>
<td>取得或設定要從 <a href="hh577895(v=exchg.10).md">LongBinary</a>或 <a href="hh577895(v=exchg.10).md">LongText</a>類型的資料行中抓取之第一個位元組的位移。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn351035(v=exchg.10).md">itagSequence</a></td>
<td>取得或設定多重值資料行中值的序號。 值的陣列是以一為基礎。 第一個值是 sequence 1，不是0。 如果 [記錄] 資料行只有一個值，則應該以 itagSequence 的形式傳遞1。</td>
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
<td><a href="dn351024(v=exchg.10).md">ContentEquals</a></td>
<td>傳回值，這個值表示這個實例是否等於另一個實例。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><a href="dn335238(v=exchg.10).md">DeepClone</a></td>
<td>傳回物件的深層複本。</td>
</tr>
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
<td><a href="dn351027(v=exchg.10).md">ToString</a></td>
<td>傳回表示目前<a href="dn335277(v=exchg.10).md">JET_RETINFO</a>的<a href="/dotnet/api/system.string">字串</a>。  (會覆寫 <a href="/dotnet/api/system.object.tostring#System_Object_ToString">物件 ToString () </a>。 ) </td>
</tr>
</tbody>
</table>


頁首

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_RETINFO 類別](./jet-retinfo-class.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)

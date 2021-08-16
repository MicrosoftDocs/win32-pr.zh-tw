---
description: 深入瞭解： JET_COLUMNDEF 成員
title: JET_COLUMNDEF 成員
TOCTitle: JET_COLUMNDEF members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_COLUMNDEF
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columndef_members(v=EXCHG.10)
ms:contentKeyID: 55103480
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: eef054e3cfa5a10fed058c087c2161357737c8a6902139fcba64af5a7f86b397
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119112457"
---
# <a name="jet_columndef-members"></a>JET_COLUMNDEF 成員

包含受保護的成員  
包含繼承的成員  

描述 ESENT 資料庫之資料表中的資料行。

[JET_COLUMNDEF](./jet-columndef-class.md)類型會公開下列成員。

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
<td><a href="dn335040(v=exchg.10).md">JET_COLUMNDEF</a></td>
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
<td><a href="dn335080(v=exchg.10).md">cbMax</a></td>
<td>取得或設定資料行的最大長度。 只有 <a href="hh577895(v=exchg.10).md">Text</a>、 <a href="hh577895(v=exchg.10).md">LongText</a>、 <a href="hh577895(v=exchg.10).md">Binary</a> 和 <a href="hh577895(v=exchg.10).md">LongBinary</a>類型的資料行才有意義。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn335041(v=exchg.10).md">coltyp</a></td>
<td>取得或設定資料行的類型。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn335079(v=exchg.10).md">columnid</a></td>
<td>取得資料行的 columnid。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn335044(v=exchg.10).md">cp</a></td>
<td>取得或設定資料行的字碼頁。 只有 <a href="hh577895(v=exchg.10).md">Text</a> 和 <a href="hh577895(v=exchg.10).md">LongText</a>類型的資料行才有意義。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn335043(v=exchg.10).md">grbit</a></td>
<td>取得或設定資料行選項。</td>
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
<td><a href="dn335074(v=exchg.10).md">ContentEquals</a></td>
<td>傳回值，這個值表示這個實例是否等於另一個實例。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><a href="dn335042(v=exchg.10).md">DeepClone</a></td>
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
<td><a href="dn335039(v=exchg.10).md">ToString</a></td>
<td>傳回表示目前<a href="dn335038(v=exchg.10).md">JET_COLUMNDEF</a>的<a href="/dotnet/api/system.string">字串</a>。  (會覆寫 <a href="/dotnet/api/system.object.tostring#System_Object_ToString">物件 ToString () </a>。 ) </td>
</tr>
</tbody>
</table>


頁首

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_COLUMNDEF 類別](./jet-columndef-class.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)

---
description: 深入瞭解： JET_INDEXLIST 成員
title: JET_INDEXLIST 成員
TOCTitle: JET_INDEXLIST members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_INDEXLIST
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexlist_members(v=EXCHG.10)
ms:contentKeyID: 55103660
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: d7800ef911366bad40b2d02ee60e23b5d138d30c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027304"
---
# <a name="jet_indexlist-members"></a>JET_INDEXLIST 成員

包含受保護的成員  
包含繼承的成員  

臨時表的相關資訊，其中包含指定資料表之所有索引的相關資訊。

[JET_INDEXLIST](./jet-indexlist-class.md)類型會公開下列成員。

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
<td><a href="dn335166(v=exchg.10).md">JET_INDEXLIST</a></td>
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
<td><a href="dn335125(v=exchg.10).md">columnidcColumn</a></td>
<td>取得臨時表中的資料行 columnid，此資料表會儲存索引鍵中的資料行數目。 資料行的類型為 <a href="hh577895(v=exchg.10).md">Long</a>。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn335126(v=exchg.10).md">columnidcEntry</a></td>
<td>取得臨時表中的資料行 columnid，此資料表會儲存索引中的專案數。 此值不是最新值，而且只會由 &quot; JetComputeStats 更新 &quot; 。 資料行的類型為 <a href="hh577895(v=exchg.10).md">Long</a>。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn335127(v=exchg.10).md">columnidcKey</a></td>
<td>取得臨時表中的資料行 columnid，此資料表會儲存索引中唯一索引鍵的數目。 此值不是最新值，而且只會由 &quot; JetComputeStats 更新 &quot; 。 資料行的類型為 <a href="hh577895(v=exchg.10).md">Long</a>。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn335129(v=exchg.10).md">columnidcoltyp</a></td>
<td>取得臨時表中資料行的 columnid，該資料表會儲存正在編制索引之資料行的資料行類型。 資料行的類型為 <a href="hh577895(v=exchg.10).md">Long</a>。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn335130(v=exchg.10).md">columnidcolumnid</a></td>
<td>取得臨時表中的資料行 columnid，此資料表會儲存正在編制索引之資料行的 columnid。 資料行的類型為 <a href="hh577895(v=exchg.10).md">Long</a>。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn335167(v=exchg.10).md">columnidcolumnname</a></td>
<td>取得臨時表中的資料行 columnid，此資料表會儲存套用至索引資料行的 grbit。 請參閱 <a href="hh579266(v=exchg.10).md">IndexKeyGrbit</a>。 資料行的類型為 <a href="hh577895(v=exchg.10).md">Text</a>。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn335168(v=exchg.10).md">columnidCp</a></td>
<td>取得臨時表中的資料行 columnid，此資料表會儲存已編制索引之資料行的字碼頁。 資料行的類型為 <a href="hh577895(v=exchg.10).md">Short</a>。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn335136(v=exchg.10).md">columnidcPage</a></td>
<td>取得臨時表中的資料行 columnid，此資料表會儲存索引中的頁面數目。 此值不是最新值，而且只會由 &quot; JetComputeStats 更新 &quot; 。 資料行的類型為 <a href="hh577895(v=exchg.10).md">Long</a>。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn335169(v=exchg.10).md">columnidgrbitColumn</a></td>
<td>取得臨時表中的資料行 columnid，此資料表會儲存套用至索引資料行的 grbit。 請參閱 <a href="hh579266(v=exchg.10).md">IndexKeyGrbit</a>。 資料行的類型為 <a href="hh577895(v=exchg.10).md">Long</a>。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn335134(v=exchg.10).md">columnidgrbitIndex</a></td>
<td>取得臨時表中的資料行 columnid，此資料表會儲存用於索引的 grbits。 請參閱 <a href="hh578433(v=exchg.10).md">CreateIndexGrbit</a>。 資料行的類型為 <a href="hh577895(v=exchg.10).md">Long</a>。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn335170(v=exchg.10).md">columnidiColumn</a></td>
<td>取得臨時表中的資料行 columnid，此資料表會將此資料行的索引儲存在索引鍵中。 資料行的類型為 <a href="hh577895(v=exchg.10).md">Long</a>。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn335138(v=exchg.10).md">columnidindexname</a></td>
<td>取得臨時表中儲存索引名稱之資料行的 columnid。 資料行的類型為 <a href="hh577895(v=exchg.10).md">Text</a>。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn335171(v=exchg.10).md">columnidLangid</a></td>
<td>取得臨時表中的資料行 columnid，此資料表會儲存索引的語言識別項 (LCID) 。 資料行的類型為 <a href="hh577895(v=exchg.10).md">Short</a>。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn335172(v=exchg.10).md">columnidLCMapFlags</a></td>
<td>取得臨時表中的資料行 columnid，此資料表會儲存索引的 unicode 正規化旗標。 資料行的類型為 <a href="hh577895(v=exchg.10).md">Long</a>。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn335173(v=exchg.10).md">cRecord</a></td>
<td>取得臨時表中的記錄數目。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn335174(v=exchg.10).md">tableid</a></td>
<td>取得臨時表的 tableid。 當不再需要資料表時，這應該會關閉。</td>
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
<td><a href="dn335165(v=exchg.10).md">ToString</a></td>
<td>傳回表示目前<a href="dn335123(v=exchg.10).md">JET_INDEXLIST</a>的<a href="/dotnet/api/system.string">字串</a>。  (會覆寫 <a href="/dotnet/api/system.object.tostring#System_Object_ToString">物件 ToString () </a>。 ) </td>
</tr>
</tbody>
</table>


頁首

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_INDEXLIST 類別](./jet-indexlist-class.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)

---
description: 深入瞭解： JET_RETRIEVECOLUMN 成員
title: JET_RETRIEVECOLUMN 成員
TOCTitle: JET_RETRIEVECOLUMN members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_retrievecolumn_members(v=EXCHG.10)
ms:contentKeyID: 55103877
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 9a5eda1d671cfe6225a8419314b2f53558294754
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104553942"
---
# <a name="jet_retrievecolumn-members"></a>JET_RETRIEVECOLUMN 成員

包含受保護的成員  
包含繼承的成員  

包含[JetRetrieveColumns (JET_SESID、JET_TABLEID、 \[ \] 、Int32) ](./api.jetretrievecolumns-method.md)的輸入和輸出參數。 結構中的欄位描述要取出的資料行值、如何取出它，以及要儲存結果的位置。

[JET_RETRIEVECOLUMN](./jet-retrievecolumn-class.md)類型會公開下列成員。

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
<td><a href="dn351036(v=exchg.10).md">JET_RETRIEVECOLUMN</a></td>
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
<td><a href="dn335226(v=exchg.10).md">cbActual</a></td>
<td>取得抓取資料行作業抓取之資料的大小（以位元組為單位）。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn335228(v=exchg.10).md">cbData</a></td>
<td>取得或設定 <a href="dn351040(v=exchg.10).md">pvData</a> 緩衝區的大小（以位元組為單位）。 抓取資料行作業將不會在 pvData 中儲存比 cbData 更多的資料。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn335230(v=exchg.10).md">columnid</a></td>
<td>取得或設定要取得之資料行的資料行識別碼。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn335229(v=exchg.10).md">columnidNextTagged</a></td>
<td>藉由將0傳遞為 columnid，取得已標記、多重值或稀疏資料行的 columnid。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn335231(v=exchg.10).md">犯 錯</a></td>
<td>取得從資料行抓取傳回的警告。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn335232(v=exchg.10).md">grbit</a></td>
<td>取得或設定資料行抓取的選項。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn335233(v=exchg.10).md">ibData</a></td>
<td>取得或設定資料將儲存在緩衝區中的位移。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn335234(v=exchg.10).md">ibLongValue</a></td>
<td>取得或設定要從 <a href="hh577895(v=exchg.10).md">LongBinary</a> 或 <a href="hh577895(v=exchg.10).md">LongText</a>類型的資料行中抓取之第一個位元組的位移。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn351039(v=exchg.10).md">itagSequence</a></td>
<td>取得或設定包含在多值資料行中之值的序號。 如果 itagSequence 為0，則會傳回多重值資料行的實例數目，而不是任何資料行資料。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn351040(v=exchg.10).md">pvData</a></td>
<td>取得或設定將儲存從資料行取出之資料的緩衝區。</td>
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
<td><a href="dn335224(v=exchg.10).md">ToString</a></td>
<td>傳回表示目前<a href="dn351033(v=exchg.10).md">JET_RETRIEVECOLUMN</a>的<a href="/dotnet/api/system.string">字串</a>。  (會覆寫 <a href="/dotnet/api/system.object.tostring#System_Object_ToString">物件 ToString () </a>。 ) </td>
</tr>
</tbody>
</table>


頁首

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_RETRIEVECOLUMN 類別](./jet-retrievecolumn-class.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)

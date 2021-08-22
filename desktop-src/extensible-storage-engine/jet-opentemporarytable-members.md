---
description: 深入瞭解： JET_OPENTEMPORARYTABLE 成員
title: 'JET_OPENTEMPORARYTABLE 成員 (的) '
TOCTitle: JET_OPENTEMPORARYTABLE members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_opentemporarytable_members(v=EXCHG.10)
ms:contentKeyID: 55104223
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 934ea18663e2fd2de786bb44d32482f42fd45d38b9e6ec23e73caf815560b264
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119560038"
---
# <a name="jet_opentemporarytable-members"></a>JET_OPENTEMPORARYTABLE 成員

包含受保護的成員  
包含繼承的成員  

JetOpenTemporaryTable 方法的參數集合。

[JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md)類型會公開下列成員。

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
<td><a href="dn351224(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a></td>
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
<td><a href="dn335290(v=exchg.10).md">cbKeyMost</a></td>
<td>取得或設定表示指定資料列之索引鍵的大小上限。 您可以設定最大索引鍵大小來控制如何截斷金鑰。 金鑰截斷很重要，因為它可能會影響資料列視為相異的時間。 如果此參數設定為0或255，則最大的索引鍵大小及其語義將維持與 Windows Server 2003 所支援的最大金鑰大小相同。 此參數也可以設定為較大的值，做為實例 <a href="hh596135(v=exchg.10).md">DatabasePageSize</a>之資料庫頁面大小的功能。 如需詳細資訊，請參閱 <a href="dn335292(v=exchg.10).md">KeyMost</a> 。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn351219(v=exchg.10).md">cbVarSegMac</a></td>
<td>取得或設定將從任何變數 lengthcolumn 使用的最大資料量，以針對指定的資料列來建立索引鍵。 此參數可用來控制任何指定的索引鍵資料行所耗用的金鑰空間量。 這項限制是以位元組為單位。 如果此參數為零或與 <a href="dn335290(v=exchg.10).md">cbKeyMost</a> 屬性相同，則沒有作用中的限制。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn335287(v=exchg.10).md">ccolumn</a></td>
<td>取得或設定 <a href="dn351228(v=exchg.10).md">prgcolumndef</a>中的資料行數目。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn351232(v=exchg.10).md">grbit</a></td>
<td>取得或設定臨時表的選項。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn335288(v=exchg.10).md">pidxunicode</a></td>
<td>取得或設定要用來比較臨時表中任何 Unicode 索引鍵資料行資料的地區設定識別碼和正規化旗標。 當此參數為 null 時，預設的 LCID 將用來比較臨時表中的任何 Unicode 索引鍵資料行。 預設的 LCID 是美國英文地區設定。 當此參數為 null 時，將會使用預設正規化旗標來比較臨時表中的任何 Unicode 索引鍵資料行資料。 預設正規化旗標為： NORM_IGNORECASE、NORM_IGNOREKANATYPE 和 NORM_IGNOREWIDTH。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn351228(v=exchg.10).md">prgcolumndef</a></td>
<td>取得或設定在臨時表中建立之資料行的資料行定義。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn351233(v=exchg.10).md">prgcolumnid</a></td>
<td>取得或設定輸出緩衝區，此緩衝區會接收建立臨時表時所產生之資料行識別碼的陣列。 此陣列中的資料行識別碼，將會完全對應至資料行定義的輸入陣列。 因此，這個緩衝區的大小必須對應到 <a href="dn351228(v=exchg.10).md">prgcolumndef</a>的大小。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn335293(v=exchg.10).md">tableid</a></td>
<td>取得在成功呼叫 JetOpenTemporaryTable 時所建立之臨時表的資料表控制碼。</td>
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
<td><a href="dn335286(v=exchg.10).md">ToString</a></td>
<td>傳回表示目前<a href="dn351217(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a>的<a href="/dotnet/api/system.string">字串</a>。  (會覆寫 <a href="/dotnet/api/system.object.tostring#System_Object_ToString">物件 ToString () </a>。 ) </td>
</tr>
</tbody>
</table>


頁首

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_OPENTEMPORARYTABLE 類別](./jet-opentemporarytable-class.md)

[Microsoft.Isam.Esent.Interop.Vista namespace](./microsoft.isam.esent.interop.vista-namespace.md)

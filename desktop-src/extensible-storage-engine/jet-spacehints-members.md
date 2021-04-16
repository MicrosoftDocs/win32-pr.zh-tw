---
description: 深入瞭解： JET_SPACEHINTS 成員
title: JET_SPACEHINTS 成員
TOCTitle: JET_SPACEHINTS members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_SPACEHINTS
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_spacehints_members(v=EXCHG.10)
ms:contentKeyID: 55103957
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: c286e385a49e7f83565f3a26729be6e7045a3460
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104562324"
---
# <a name="jet_spacehints-members"></a>JET_SPACEHINTS 成員

包含受保護的成員  
包含繼承的成員  

描述 ESENT 資料庫之資料表中的資料行。

[JET_SPACEHINTS](./jet-spacehints-class.md)類型會公開下列成員。

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
<td><a href="dn351065(v=exchg.10).md">JET_SPACEHINTS</a></td>
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
<td><a href="dn351103(v=exchg.10).md">cbInitial</a></td>
<td>取得或設定初始大小 (（以位元組為單位）) 。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn351105(v=exchg.10).md">cbMaxExtent</a></td>
<td>取得或設定值，這個值會設定 ulGrowth 的上限。 這個值是以位元組為單位。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn351104(v=exchg.10).md">cbMinExtent</a></td>
<td>取得或設定覆寫 ulGrowth （如果太小）的值。 這個值是以位元組為單位。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn351068(v=exchg.10).md">grbit</a></td>
<td>取得或設定空間提示選項。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn351069(v=exchg.10).md">ulGrowth</a></td>
<td>取得或設定上一次成長或初始大小 (可能四捨五入為最接近原生 JET 配置大小) 的成長百分比。 有效的值為0，而 [100，50000) 。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn351070(v=exchg.10).md">ulInitialDensity</a></td>
<td>取得或設定 (附加) 版面配置的密度。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn351071(v=exchg.10).md">ulMaintDensity</a></td>
<td>取得或設定要維護的密度。</td>
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
<td><a href="dn351097(v=exchg.10).md">ContentEquals</a></td>
<td>傳回值，這個值表示這個實例是否等於另一個實例。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><a href="dn351100(v=exchg.10).md">DeepClone</a></td>
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
<td><a href="dn351066(v=exchg.10).md">ToString</a></td>
<td>產生實例的字串表示。  (會覆寫 <a href="/dotnet/api/system.object.tostring#System_Object_ToString">物件 ToString () </a>。 ) </td>
</tr>
</tbody>
</table>


頁首

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_SPACEHINTS 類別](./jet-spacehints-class.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)

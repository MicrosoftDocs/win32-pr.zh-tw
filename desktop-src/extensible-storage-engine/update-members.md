---
description: 深入瞭解：更新成員
title: 更新成員
TOCTitle: Update members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Update
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.update_members(v=EXCHG.10)
ms:contentKeyID: 55104188
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 9c97398ca903445c2d883b471e0dd7978fe95656
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104562359"
---
# <a name="update-members"></a>更新成員

包含受保護的成員  
包含繼承的成員  

封裝 JET_TABLEID 上之更新的類別。

[更新](./update-class.md)類型會公開下列成員。

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
<td><a href="dn351261(v=exchg.10).md">更新</a></td>
<td>初始化 Update 類別的新實例。 這會自動開始更新。 如果未明確儲存，將會取消更新。</td>
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
<td><img src="../images/dn292128.protproperty(exchg.10).gif" title="受保護的屬性" alt="Protected property" /></td>
<td><a href="dn350578(v=exchg.10).md">HasResource</a></td>
<td>取得值，指出目前是否已配置基礎資源。  (繼承自 <a href="dn319890(v=exchg.10).md">EsentResource</a>。 ) </td>
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
<td><a href="dn351266(v=exchg.10).md">取消</a></td>
<td>取消更新。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><a href="dn350541(v=exchg.10).md">CheckObjectIsNotDisposed</a></td>
<td>如果已處置這個物件，則擲回例外狀況。  (繼承自 <a href="dn319890(v=exchg.10).md">EsentResource</a>。 ) </td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><a href="dn350553(v=exchg.10).md">Dispose () </a></td>
<td>處置這個物件，釋放基礎 Esent 資源。  (繼承自 <a href="dn319890(v=exchg.10).md">EsentResource</a>。 ) </td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><a href="dn350543(v=exchg.10).md">Dispose (布林值) </a></td>
<td>由 Dispose 和完成項呼叫。  (繼承自 <a href="dn319890(v=exchg.10).md">EsentResource</a>。 ) </td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">等於</a></td>
<td> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><a href="dn350552(v=exchg.10).md">完成</a></td>
<td>完成 EsentResource 類別的實例。  (繼承自 <a href="dn319890(v=exchg.10).md">EsentResource</a>。 ) </td>
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
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><a href="dn351268(v=exchg.10).md">ReleaseResource</a></td>
<td>當交易在作用中處置時呼叫。 這應該會復原交易。  (覆寫 <a href="dn350545(v=exchg.10).md">EsentResource. ReleaseResource () </a>。 ) </td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><a href="dn350576(v=exchg.10).md">ResourceWasAllocated</a></td>
<td>當配置資源時由子類別呼叫。  (繼承自 <a href="dn319890(v=exchg.10).md">EsentResource</a>。 ) </td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><a href="dn350577(v=exchg.10).md">ResourceWasReleased</a></td>
<td>釋放資源時由子類別呼叫。  (繼承自 <a href="dn319890(v=exchg.10).md">EsentResource</a>。 ) </td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><a href="dn351270(v=exchg.10).md">儲存 () </a></td>
<td>更新 tableid。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><a href="dn351199(v=exchg.10).md">Save ( []，Int32，Int32) </a></td>
<td>更新 tableid。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><a href="dn351272(v=exchg.10).md">SaveAndGotoBookmark</a></td>
<td>更新 tableid，並將 tableid 放在修改過的記錄上。 這在插入記錄時很有用，因為 tableid 預設會保留在舊的位置。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><a href="dn351192(v=exchg.10).md">ToString</a></td>
<td>傳回 <a href="/dotnet/api/system.string">字串</a> ，表示目前的 <a href="dn351191(v=exchg.10).md">更新</a>。  (會覆寫 <a href="/dotnet/api/system.object.tostring#System_Object_ToString">物件 ToString () </a>。 ) </td>
</tr>
</tbody>
</table>


頁首

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Update 類別](./update-class.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)

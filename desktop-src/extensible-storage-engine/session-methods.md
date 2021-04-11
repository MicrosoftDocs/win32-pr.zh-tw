---
description: 深入瞭解：會話方法
title: 工作階段方法
TOCTitle: Session methods
ms:assetid: Methods.T:Microsoft.Isam.Esent.Interop.Session
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.session_methods(v=EXCHG.10)
ms:contentKeyID: 55104007
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 11f8b31d8c74e3074788b60f62677e9e81135ae5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691279"
---
# <a name="session-methods"></a>工作階段方法

包含受保護的成員  
包含繼承的成員  

此 [會話](./session-class.md) 類型會公開下列成員。

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
<td><a href="dn350541(v=exchg.10).md">CheckObjectIsNotDisposed</a></td>
<td>如果已處置這個物件，則擲回例外狀況。  (繼承自 <a href="dn319890(v=exchg.10).md">EsentResource</a>。 ) </td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><a href="dn350553(v=exchg.10).md">Dispose () </a></td>
<td>處置這個物件，釋放基礎 Esent 資源。  (繼承自 <a href="dn319890(v=exchg.10).md">EsentResource</a>。 ) </td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><a href="dn350543(v=exchg.10).md">Dispose (布林值) </a></td>
<td>由 Dispose 和完成項呼叫。  (繼承自 <a href="dn319890(v=exchg.10).md">EsentResource</a>。 ) </td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><a href="dn351128(v=exchg.10).md">結束</a></td>
<td>終止會話。</td>
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
<td><a href="dn351165(v=exchg.10).md">ReleaseResource</a></td>
<td>釋放基礎 JET_SESID。  (覆寫 <a href="dn350545(v=exchg.10).md">EsentResource. ReleaseResource () </a>。 ) </td>
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
<td><a href="dn351129(v=exchg.10).md">ToString</a></td>
<td>傳回表示目前<a href="dn351164(v=exchg.10).md">會話</a>的<a href="/dotnet/api/system.string">字串</a>。  (會覆寫 <a href="/dotnet/api/system.object.tostring#System_Object_ToString">物件 ToString () </a>。 ) </td>
</tr>
</tbody>
</table>


頁首

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[工作階段類別](./session-class.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)

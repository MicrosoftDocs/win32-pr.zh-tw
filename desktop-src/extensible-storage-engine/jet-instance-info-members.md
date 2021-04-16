---
description: 深入瞭解： JET_INSTANCE_INFO 成員
title: JET_INSTANCE_INFO 成員
TOCTitle: JET_INSTANCE_INFO members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_instance_info_members(v=EXCHG.10)
ms:contentKeyID: 55103693
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 42d9bcd2c078766875fc8230eaf83dc07fdb4b8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104565940"
---
# <a name="jet_instance_info-members"></a>JET_INSTANCE_INFO 成員

包含受保護的成員  
包含繼承的成員  

當搭配 JetGetInstanceInfo 和 JetOSSnapshotFreeze 函數使用時，接收有關執行中資料庫實例的資訊。

[JET_INSTANCE_INFO](./jet-instance-info-class.md)類型會公開下列成員。

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
<td><a href="dn335189(v=exchg.10).md">cDatabases</a></td>
<td>取得附加至資料庫實例的資料庫數目。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn335190(v=exchg.10).md">hInstanceId</a></td>
<td>取得指定實例的 JET_INSTANCE。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn335193(v=exchg.10).md">szDatabaseFileName</a></td>
<td>取得字串的集合，每個字串都包含附加至資料庫實例的資料庫檔案名。 陣列具有 cDatabases 元素。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn335194(v=exchg.10).md">szInstanceName</a></td>
<td>取得資料庫實例的名稱。 如果實例沒有名稱，這個值可以是 null。</td>
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
<td><a href="dn335184(v=exchg.10).md">等於 (物件) </a></td>
<td>傳回值，這個值表示這個實例是否等於另一個實例。  (覆寫 <a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_"> (物件) 的 Equals </a>。 ) </td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><a href="dn335187(v=exchg.10).md">等於 (JET_INSTANCE_INFO) </a></td>
<td>傳回值，這個值表示這個實例是否等於另一個實例。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">完成</a></td>
<td> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><a href="dn335191(v=exchg.10).md">GetHashCode</a></td>
<td>傳回這個執行個體的雜湊碼。  (覆寫 <a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode () </a>。 ) </td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></td>
<td> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></td>
<td> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><a href="dn335192(v=exchg.10).md">ToString</a></td>
<td>產生實例的字串表示。  (會覆寫 <a href="/dotnet/api/system.object.tostring#System_Object_ToString">物件 ToString () </a>。 ) </td>
</tr>
</tbody>
</table>


頁首

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_INSTANCE_INFO 類別](./jet-instance-info-class.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)

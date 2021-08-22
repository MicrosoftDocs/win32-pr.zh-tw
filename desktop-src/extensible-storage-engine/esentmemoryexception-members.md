---
description: 深入瞭解： EsentMemoryException 成員
title: EsentMemoryException 成員
TOCTitle: EsentMemoryException members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.EsentMemoryException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentmemoryexception_members(v=EXCHG.10)
ms:contentKeyID: 55102254
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 107c0b7d6bb117e6526929da060000b40c46b6e7f811771b488b5d3d024c8559
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119115628"
---
# <a name="esentmemoryexception-members"></a>EsentMemoryException 成員

包含受保護的成員  
包含繼承的成員  

記憶體例外狀況的基類。

[EsentMemoryException](./esentmemoryexception-class.md)類型會公開下列成員。

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
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><a href="dn334560(v=exchg.10).md">EsentMemoryException (SerializationInfo、StreamingCoNtext) </a></td>
<td>初始化 EsentMemoryException 類別的新實例。 這個函式是用來將序列化的例外狀況還原序列化。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><a href="dn334638(v=exchg.10).md">EsentMemoryException (字串 JET_err) </a></td>
<td>初始化 EsentMemoryException 類別的新實例。</td>
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
<td><a href="/dotnet/api/system.exception.data#System_Exception_Data">資料</a></td>
<td> (繼承自 <a href="/dotnet/api/system.exception">例外</a>狀況。 ) </td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn274313(v=exchg.10).md">錯誤</a></td>
<td>取得這個例外狀況的基礎 Esent 錯誤。  (繼承自 <a href="dn274314(v=exchg.10).md">EsentErrorException</a>。 ) </td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="/dotnet/api/system.exception.helplink#System_Exception_HelpLink">HelpLink</a></td>
<td> (繼承自 <a href="/dotnet/api/system.exception">例外</a>狀況。 ) </td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.protproperty(exchg.10).gif" title="受保護的屬性" alt="Protected property" /></td>
<td><a href="/dotnet/api/system.exception.hresult#System_Exception_HResult">HResult</a></td>
<td> (繼承自 <a href="/dotnet/api/system.exception">例外</a>狀況。 ) </td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="/dotnet/api/system.exception.innerexception#System_Exception_InnerException">InnerException</a></td>
<td> (繼承自 <a href="/dotnet/api/system.exception">例外</a>狀況。 ) </td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="/dotnet/api/system.exception.message#System_Exception_Message">訊息</a></td>
<td> (繼承自 <a href="/dotnet/api/system.exception">例外</a>狀況。 ) </td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="/dotnet/api/system.exception.source#System_Exception_Source">來源</a></td>
<td> (繼承自 <a href="/dotnet/api/system.exception">例外</a>狀況。 ) </td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="/dotnet/api/system.exception.stacktrace#System_Exception_StackTrace">StackTrace</a></td>
<td> (繼承自 <a href="/dotnet/api/system.exception">例外</a>狀況。 ) </td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="/dotnet/api/system.exception.targetsite#System_Exception_TargetSite">TargetSite</a></td>
<td> (繼承自 <a href="/dotnet/api/system.exception">例外</a>狀況。 ) </td>
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
<td><a href="/dotnet/api/system.exception.getbaseexception#System_Exception_GetBaseException">GetBaseException</a></td>
<td> (繼承自 <a href="/dotnet/api/system.exception">例外</a>狀況。 ) </td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></td>
<td> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><a href="dn334369(v=exchg.10).md">GetObjectData</a></td>
<td>在衍生類別中覆寫時，使用例外狀況的相關資訊設定 <a href="/dotnet/api/system.runtime.serialization.serializationinfo">SerializationInfo</a> 。  (繼承自 <a href="dn274314(v=exchg.10).md">EsentErrorException</a>。 ) </td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><a href="/dotnet/api/system.exception.gettype#System_Exception_GetType">GetType</a></td>
<td> (繼承自 <a href="/dotnet/api/system.exception">例外</a>狀況。 ) </td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></td>
<td> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><a href="/dotnet/api/system.exception.tostring#System_Exception_ToString">ToString</a></td>
<td> (繼承自 <a href="/dotnet/api/system.exception">例外</a>狀況。 ) </td>
</tr>
</tbody>
</table>


頁首

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[EsentMemoryException 類別](./esentmemoryexception-class.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)

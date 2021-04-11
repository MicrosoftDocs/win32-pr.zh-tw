---
description: 深入瞭解： EsentException 成員
title: 'EsentException 成員 (Microsoft 的 Isam) '
TOCTitle: EsentException members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.EsentException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.esentexception_members(v=EXCHG.10)
ms:contentKeyID: 55107214
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 8edc1bc32b4a4a1f3b4036fcd53dc09ab53a5a54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194008"
---
# <a name="esentexception-members"></a><span data-ttu-id="31eb7-103">EsentException 成員</span><span class="sxs-lookup"><span data-stu-id="31eb7-103">EsentException members</span></span>

<span data-ttu-id="31eb7-104">包含受保護的成員</span><span class="sxs-lookup"><span data-stu-id="31eb7-104">Include protected members</span></span>  
<span data-ttu-id="31eb7-105">包含繼承的成員</span><span class="sxs-lookup"><span data-stu-id="31eb7-105">Include inherited members</span></span>  

<span data-ttu-id="31eb7-106">ESENT 例外狀況的基類。</span><span class="sxs-lookup"><span data-stu-id="31eb7-106">Base class for ESENT exceptions.</span></span>

<span data-ttu-id="31eb7-107">[EsentException](./esentexception-class.md)類型會公開下列成員。</span><span class="sxs-lookup"><span data-stu-id="31eb7-107">The [EsentException](./esentexception-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="31eb7-108">建構函式</span><span class="sxs-lookup"><span data-stu-id="31eb7-108">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="31eb7-109">名稱</span><span class="sxs-lookup"><span data-stu-id="31eb7-109">Name</span></span></th>
<th><span data-ttu-id="31eb7-110">描述</span><span class="sxs-lookup"><span data-stu-id="31eb7-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="31eb7-112"><a href="dn292117(v=exchg.10).md">EsentException () </a></span><span class="sxs-lookup"><span data-stu-id="31eb7-112"><a href="dn292117(v=exchg.10).md">EsentException()</a></span></span></td>
<td><span data-ttu-id="31eb7-113">初始化 EsentException 類別的新實例。</span><span class="sxs-lookup"><span data-stu-id="31eb7-113">Initializes a new instance of the EsentException class.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="31eb7-115"><a href="dn292119(v=exchg.10).md">EsentException (字串) </a></span><span class="sxs-lookup"><span data-stu-id="31eb7-115"><a href="dn292119(v=exchg.10).md">EsentException(String)</a></span></span></td>
<td><span data-ttu-id="31eb7-116">使用指定的錯誤訊息，初始化 EsentException 類別的新實例。</span><span class="sxs-lookup"><span data-stu-id="31eb7-116">Initializes a new instance of the EsentException class with a specified error message.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="31eb7-118"><a href="dn292125(v=exchg.10).md">EsentException (SerializationInfo、StreamingCoNtext) </a></span><span class="sxs-lookup"><span data-stu-id="31eb7-118"><a href="dn292125(v=exchg.10).md">EsentException(SerializationInfo, StreamingContext)</a></span></span></td>
<td><span data-ttu-id="31eb7-119">初始化 EsentException 類別的新實例。</span><span class="sxs-lookup"><span data-stu-id="31eb7-119">Initializes a new instance of the EsentException class.</span></span> <span data-ttu-id="31eb7-120">這個函式是用來將序列化的例外狀況還原序列化。</span><span class="sxs-lookup"><span data-stu-id="31eb7-120">This constructor is used to deserialize a serialized exception.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="31eb7-121">頁首</span><span class="sxs-lookup"><span data-stu-id="31eb7-121">Top</span></span>

## <a name="properties"></a><span data-ttu-id="31eb7-122">屬性</span><span class="sxs-lookup"><span data-stu-id="31eb7-122">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="31eb7-123">名稱</span><span class="sxs-lookup"><span data-stu-id="31eb7-123">Name</span></span></th>
<th><span data-ttu-id="31eb7-124">描述</span><span class="sxs-lookup"><span data-stu-id="31eb7-124">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="31eb7-126"><a href="/dotnet/api/system.exception.data#System_Exception_Data">資料</a></span><span class="sxs-lookup"><span data-stu-id="31eb7-126"><a href="/dotnet/api/system.exception.data#System_Exception_Data">Data</a></span></span></td>
<td><span data-ttu-id="31eb7-127"> (繼承自 <a href="/dotnet/api/system.exception">例外</a>狀況。 ) </span><span class="sxs-lookup"><span data-stu-id="31eb7-127">(Inherited from <a href="/dotnet/api/system.exception">Exception</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="31eb7-129"><a href="/dotnet/api/system.exception.helplink#System_Exception_HelpLink">HelpLink</a></span><span class="sxs-lookup"><span data-stu-id="31eb7-129"><a href="/dotnet/api/system.exception.helplink#System_Exception_HelpLink">HelpLink</a></span></span></td>
<td><span data-ttu-id="31eb7-130"> (繼承自 <a href="/dotnet/api/system.exception">例外</a>狀況。 ) </span><span class="sxs-lookup"><span data-stu-id="31eb7-130">(Inherited from <a href="/dotnet/api/system.exception">Exception</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.protproperty(exchg.10).gif" title="受保護的屬性" alt="Protected property" /></td>
<td><span data-ttu-id="31eb7-132"><a href="/dotnet/api/system.exception.hresult#System_Exception_HResult">HResult</a></span><span class="sxs-lookup"><span data-stu-id="31eb7-132"><a href="/dotnet/api/system.exception.hresult#System_Exception_HResult">HResult</a></span></span></td>
<td><span data-ttu-id="31eb7-133"> (繼承自 <a href="/dotnet/api/system.exception">例外</a>狀況。 ) </span><span class="sxs-lookup"><span data-stu-id="31eb7-133">(Inherited from <a href="/dotnet/api/system.exception">Exception</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="31eb7-135"><a href="/dotnet/api/system.exception.innerexception#System_Exception_InnerException">InnerException</a></span><span class="sxs-lookup"><span data-stu-id="31eb7-135"><a href="/dotnet/api/system.exception.innerexception#System_Exception_InnerException">InnerException</a></span></span></td>
<td><span data-ttu-id="31eb7-136"> (繼承自 <a href="/dotnet/api/system.exception">例外</a>狀況。 ) </span><span class="sxs-lookup"><span data-stu-id="31eb7-136">(Inherited from <a href="/dotnet/api/system.exception">Exception</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="31eb7-138"><a href="/dotnet/api/system.exception.message#System_Exception_Message">訊息</a></span><span class="sxs-lookup"><span data-stu-id="31eb7-138"><a href="/dotnet/api/system.exception.message#System_Exception_Message">Message</a></span></span></td>
<td><span data-ttu-id="31eb7-139"> (繼承自 <a href="/dotnet/api/system.exception">例外</a>狀況。 ) </span><span class="sxs-lookup"><span data-stu-id="31eb7-139">(Inherited from <a href="/dotnet/api/system.exception">Exception</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="31eb7-141"><a href="/dotnet/api/system.exception.source#System_Exception_Source">來源</a></span><span class="sxs-lookup"><span data-stu-id="31eb7-141"><a href="/dotnet/api/system.exception.source#System_Exception_Source">Source</a></span></span></td>
<td><span data-ttu-id="31eb7-142"> (繼承自 <a href="/dotnet/api/system.exception">例外</a>狀況。 ) </span><span class="sxs-lookup"><span data-stu-id="31eb7-142">(Inherited from <a href="/dotnet/api/system.exception">Exception</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="31eb7-144"><a href="/dotnet/api/system.exception.stacktrace#System_Exception_StackTrace">StackTrace</a></span><span class="sxs-lookup"><span data-stu-id="31eb7-144"><a href="/dotnet/api/system.exception.stacktrace#System_Exception_StackTrace">StackTrace</a></span></span></td>
<td><span data-ttu-id="31eb7-145"> (繼承自 <a href="/dotnet/api/system.exception">例外</a>狀況。 ) </span><span class="sxs-lookup"><span data-stu-id="31eb7-145">(Inherited from <a href="/dotnet/api/system.exception">Exception</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="31eb7-147"><a href="/dotnet/api/system.exception.targetsite#System_Exception_TargetSite">TargetSite</a></span><span class="sxs-lookup"><span data-stu-id="31eb7-147"><a href="/dotnet/api/system.exception.targetsite#System_Exception_TargetSite">TargetSite</a></span></span></td>
<td><span data-ttu-id="31eb7-148"> (繼承自 <a href="/dotnet/api/system.exception">例外</a>狀況。 ) </span><span class="sxs-lookup"><span data-stu-id="31eb7-148">(Inherited from <a href="/dotnet/api/system.exception">Exception</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="31eb7-149">頁首</span><span class="sxs-lookup"><span data-stu-id="31eb7-149">Top</span></span>

## <a name="methods"></a><span data-ttu-id="31eb7-150">方法</span><span class="sxs-lookup"><span data-stu-id="31eb7-150">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="31eb7-151">名稱</span><span class="sxs-lookup"><span data-stu-id="31eb7-151">Name</span></span></th>
<th><span data-ttu-id="31eb7-152">描述</span><span class="sxs-lookup"><span data-stu-id="31eb7-152">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="31eb7-154"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">等於</a></span><span class="sxs-lookup"><span data-stu-id="31eb7-154"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="31eb7-155"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="31eb7-155">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="31eb7-157"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">完成</a></span><span class="sxs-lookup"><span data-stu-id="31eb7-157"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="31eb7-158"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="31eb7-158">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="31eb7-160"><a href="/dotnet/api/system.exception.getbaseexception#System_Exception_GetBaseException">GetBaseException</a></span><span class="sxs-lookup"><span data-stu-id="31eb7-160"><a href="/dotnet/api/system.exception.getbaseexception#System_Exception_GetBaseException">GetBaseException</a></span></span></td>
<td><span data-ttu-id="31eb7-161"> (繼承自 <a href="/dotnet/api/system.exception">例外</a>狀況。 ) </span><span class="sxs-lookup"><span data-stu-id="31eb7-161">(Inherited from <a href="/dotnet/api/system.exception">Exception</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="31eb7-163"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="31eb7-163"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="31eb7-164"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="31eb7-164">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="31eb7-166"><a href="/dotnet/api/system.exception.getobjectdata#System_Exception_GetObjectData_System_Runtime_Serialization_SerializationInfo_System_Runtime_Serialization_StreamingContext_">GetObjectData</a></span><span class="sxs-lookup"><span data-stu-id="31eb7-166"><a href="/dotnet/api/system.exception.getobjectdata#System_Exception_GetObjectData_System_Runtime_Serialization_SerializationInfo_System_Runtime_Serialization_StreamingContext_">GetObjectData</a></span></span></td>
<td><span data-ttu-id="31eb7-167"> (繼承自 <a href="/dotnet/api/system.exception">例外</a>狀況。 ) </span><span class="sxs-lookup"><span data-stu-id="31eb7-167">(Inherited from <a href="/dotnet/api/system.exception">Exception</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="31eb7-169"><a href="/dotnet/api/system.exception.gettype#System_Exception_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="31eb7-169"><a href="/dotnet/api/system.exception.gettype#System_Exception_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="31eb7-170"> (繼承自 <a href="/dotnet/api/system.exception">例外</a>狀況。 ) </span><span class="sxs-lookup"><span data-stu-id="31eb7-170">(Inherited from <a href="/dotnet/api/system.exception">Exception</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="31eb7-172"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="31eb7-172"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="31eb7-173"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="31eb7-173">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="31eb7-175"><a href="/dotnet/api/system.exception.tostring#System_Exception_ToString">ToString</a></span><span class="sxs-lookup"><span data-stu-id="31eb7-175"><a href="/dotnet/api/system.exception.tostring#System_Exception_ToString">ToString</a></span></span></td>
<td><span data-ttu-id="31eb7-176"> (繼承自 <a href="/dotnet/api/system.exception">例外</a>狀況。 ) </span><span class="sxs-lookup"><span data-stu-id="31eb7-176">(Inherited from <a href="/dotnet/api/system.exception">Exception</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="31eb7-177">頁首</span><span class="sxs-lookup"><span data-stu-id="31eb7-177">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="31eb7-178">另請參閱</span><span class="sxs-lookup"><span data-stu-id="31eb7-178">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="31eb7-179">參考</span><span class="sxs-lookup"><span data-stu-id="31eb7-179">Reference</span></span>

[<span data-ttu-id="31eb7-180">EsentException 類別</span><span class="sxs-lookup"><span data-stu-id="31eb7-180">EsentException class</span></span>](./esentexception-class.md)

[<span data-ttu-id="31eb7-181">Microsoft Isam 命名空間</span><span class="sxs-lookup"><span data-stu-id="31eb7-181">Microsoft.Isam.Esent namespace</span></span>](./microsoft.isam.esent-namespace.md)

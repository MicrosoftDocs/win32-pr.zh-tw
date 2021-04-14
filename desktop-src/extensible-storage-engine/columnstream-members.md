---
description: 深入瞭解： ColumnStream 成員
title: ColumnStream 成員
TOCTitle: ColumnStream members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.ColumnStream
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnstream_members(v=EXCHG.10)
ms:contentKeyID: 55101147
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 9f35c0e000329bc98e2f9fd5873cd724516271d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104565037"
---
# <a name="columnstream-members"></a><span data-ttu-id="2d887-103">ColumnStream 成員</span><span class="sxs-lookup"><span data-stu-id="2d887-103">ColumnStream members</span></span>

<span data-ttu-id="2d887-104">包含受保護的成員</span><span class="sxs-lookup"><span data-stu-id="2d887-104">Include protected members</span></span>  
<span data-ttu-id="2d887-105">包含繼承的成員</span><span class="sxs-lookup"><span data-stu-id="2d887-105">Include inherited members</span></span>  

<span data-ttu-id="2d887-106">這個類別會提供 long 值資料行的串流介面 (亦即 [LongBinary](./jet-coltyp-enumeration.md) 或) [LongText](./jet-coltyp-enumeration.md) 類型的資料行。</span><span class="sxs-lookup"><span data-stu-id="2d887-106">This class provides a streaming interface to a long-value column (i.e. a column of type [LongBinary](./jet-coltyp-enumeration.md) or [LongText](./jet-coltyp-enumeration.md)).</span></span>

<span data-ttu-id="2d887-107">[ColumnStream](./columnstream-class.md)類型會公開下列成員。</span><span class="sxs-lookup"><span data-stu-id="2d887-107">The [ColumnStream](./columnstream-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="2d887-108">建構函式</span><span class="sxs-lookup"><span data-stu-id="2d887-108">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="2d887-109">名稱</span><span class="sxs-lookup"><span data-stu-id="2d887-109">Name</span></span></th>
<th><span data-ttu-id="2d887-110">描述</span><span class="sxs-lookup"><span data-stu-id="2d887-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="2d887-112"><a href="dn334142(v=exchg.10).md">ColumnStream</a></span><span class="sxs-lookup"><span data-stu-id="2d887-112"><a href="dn334142(v=exchg.10).md">ColumnStream</a></span></span></td>
<td><span data-ttu-id="2d887-113">初始化 ColumnStream 類別的新實例。</span><span class="sxs-lookup"><span data-stu-id="2d887-113">Initializes a new instance of the ColumnStream class.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2d887-114">頁首</span><span class="sxs-lookup"><span data-stu-id="2d887-114">Top</span></span>

## <a name="properties"></a><span data-ttu-id="2d887-115">屬性</span><span class="sxs-lookup"><span data-stu-id="2d887-115">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="2d887-116">名稱</span><span class="sxs-lookup"><span data-stu-id="2d887-116">Name</span></span></th>
<th><span data-ttu-id="2d887-117">描述</span><span class="sxs-lookup"><span data-stu-id="2d887-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="2d887-119"><a href="dn334201(v=exchg.10).md">CanRead</a></span><span class="sxs-lookup"><span data-stu-id="2d887-119"><a href="dn334201(v=exchg.10).md">CanRead</a></span></span></td>
<td><span data-ttu-id="2d887-120">取得值，指出資料流程是否支援讀取。</span><span class="sxs-lookup"><span data-stu-id="2d887-120">Gets a value indicating whether the stream supports reading.</span></span> <span data-ttu-id="2d887-121"> (覆寫 <a href="/dotnet/api/system.io.stream.canread#System_IO_Stream_CanRead">CanRead</a>。 ) </span><span class="sxs-lookup"><span data-stu-id="2d887-121">(Overrides <a href="/dotnet/api/system.io.stream.canread#System_IO_Stream_CanRead">Stream.CanRead</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="2d887-123"><a href="dn334153(v=exchg.10).md">CanSeek</a></span><span class="sxs-lookup"><span data-stu-id="2d887-123"><a href="dn334153(v=exchg.10).md">CanSeek</a></span></span></td>
<td><span data-ttu-id="2d887-124">取得值，指出資料流是否支援搜尋。</span><span class="sxs-lookup"><span data-stu-id="2d887-124">Gets a value indicating whether the stream supports seeking.</span></span> <span data-ttu-id="2d887-125"> (覆寫 <a href="/dotnet/api/system.io.stream.canseek#System_IO_Stream_CanSeek">CanSeek</a>。 ) </span><span class="sxs-lookup"><span data-stu-id="2d887-125">(Overrides <a href="/dotnet/api/system.io.stream.canseek#System_IO_Stream_CanSeek">Stream.CanSeek</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="2d887-127"><a href="/dotnet/api/system.io.stream.cantimeout#System_IO_Stream_CanTimeout">CanTimeout</a></span><span class="sxs-lookup"><span data-stu-id="2d887-127"><a href="/dotnet/api/system.io.stream.cantimeout#System_IO_Stream_CanTimeout">CanTimeout</a></span></span></td>
<td><span data-ttu-id="2d887-128"> (繼承自 <a href="/dotnet/api/system.io.stream">Stream</a>。 ) </span><span class="sxs-lookup"><span data-stu-id="2d887-128">(Inherited from <a href="/dotnet/api/system.io.stream">Stream</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="2d887-130"><a href="dn334204(v=exchg.10).md">CanWrite</a></span><span class="sxs-lookup"><span data-stu-id="2d887-130"><a href="dn334204(v=exchg.10).md">CanWrite</a></span></span></td>
<td><span data-ttu-id="2d887-131">取得值，指出資料流是否支援寫入。</span><span class="sxs-lookup"><span data-stu-id="2d887-131">Gets a value indicating whether the stream supports writing.</span></span> <span data-ttu-id="2d887-132"> (覆寫 <a href="/dotnet/api/system.io.stream.canwrite#System_IO_Stream_CanWrite">CanWrite</a>。 ) </span><span class="sxs-lookup"><span data-stu-id="2d887-132">(Overrides <a href="/dotnet/api/system.io.stream.canwrite#System_IO_Stream_CanWrite">Stream.CanWrite</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="2d887-134"><a href="dn334159(v=exchg.10).md">Itag</a></span><span class="sxs-lookup"><span data-stu-id="2d887-134"><a href="dn334159(v=exchg.10).md">Itag</a></span></span></td>
<td><span data-ttu-id="2d887-135">取得或設定資料行的 itag。</span><span class="sxs-lookup"><span data-stu-id="2d887-135">Gets or sets the itag of the column.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="2d887-137"><a href="dn334205(v=exchg.10).md">長度</a></span><span class="sxs-lookup"><span data-stu-id="2d887-137"><a href="dn334205(v=exchg.10).md">Length</a></span></span></td>
<td><span data-ttu-id="2d887-138">取得目前的資料流程長度。</span><span class="sxs-lookup"><span data-stu-id="2d887-138">Gets the current length of the stream.</span></span> <span data-ttu-id="2d887-139"> (覆寫 <a href="/dotnet/api/system.io.stream.length#System_IO_Stream_Length">資料流程. Length</a>. ) </span><span class="sxs-lookup"><span data-stu-id="2d887-139">(Overrides <a href="/dotnet/api/system.io.stream.length#System_IO_Stream_Length">Stream.Length</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="2d887-141"><a href="dn334161(v=exchg.10).md">位置</a></span><span class="sxs-lookup"><span data-stu-id="2d887-141"><a href="dn334161(v=exchg.10).md">Position</a></span></span></td>
<td><span data-ttu-id="2d887-142">取得或設定資料流中目前的位置。</span><span class="sxs-lookup"><span data-stu-id="2d887-142">Gets or sets the current position in the stream.</span></span> <span data-ttu-id="2d887-143"> (覆寫 <a href="/dotnet/api/system.io.stream.position#System_IO_Stream_Position">資料流程。位置</a>) </span><span class="sxs-lookup"><span data-stu-id="2d887-143">(Overrides <a href="/dotnet/api/system.io.stream.position#System_IO_Stream_Position">Stream.Position</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="2d887-145"><a href="/dotnet/api/system.io.stream.readtimeout#System_IO_Stream_ReadTimeout">ReadTimeout</a></span><span class="sxs-lookup"><span data-stu-id="2d887-145"><a href="/dotnet/api/system.io.stream.readtimeout#System_IO_Stream_ReadTimeout">ReadTimeout</a></span></span></td>
<td><span data-ttu-id="2d887-146"> (繼承自 <a href="/dotnet/api/system.io.stream">Stream</a>。 ) </span><span class="sxs-lookup"><span data-stu-id="2d887-146">(Inherited from <a href="/dotnet/api/system.io.stream">Stream</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="2d887-148"><a href="/dotnet/api/system.io.stream.writetimeout#System_IO_Stream_WriteTimeout">WriteTimeout</a></span><span class="sxs-lookup"><span data-stu-id="2d887-148"><a href="/dotnet/api/system.io.stream.writetimeout#System_IO_Stream_WriteTimeout">WriteTimeout</a></span></span></td>
<td><span data-ttu-id="2d887-149"> (繼承自 <a href="/dotnet/api/system.io.stream">Stream</a>。 ) </span><span class="sxs-lookup"><span data-stu-id="2d887-149">(Inherited from <a href="/dotnet/api/system.io.stream">Stream</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2d887-150">頁首</span><span class="sxs-lookup"><span data-stu-id="2d887-150">Top</span></span>

## <a name="methods"></a><span data-ttu-id="2d887-151">方法</span><span class="sxs-lookup"><span data-stu-id="2d887-151">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="2d887-152">名稱</span><span class="sxs-lookup"><span data-stu-id="2d887-152">Name</span></span></th>
<th><span data-ttu-id="2d887-153">描述</span><span class="sxs-lookup"><span data-stu-id="2d887-153">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="2d887-155"><a href="/dotnet/api/system.io.stream.beginread#System_IO_Stream_BeginRead_System_Byte___System_Int32_System_Int32_System_AsyncCallback_System_Object_">BeginRead</a></span><span class="sxs-lookup"><span data-stu-id="2d887-155"><a href="/dotnet/api/system.io.stream.beginread#System_IO_Stream_BeginRead_System_Byte___System_Int32_System_Int32_System_AsyncCallback_System_Object_">BeginRead</a></span></span></td>
<td><span data-ttu-id="2d887-156"> (繼承自 <a href="/dotnet/api/system.io.stream">Stream</a>。 ) </span><span class="sxs-lookup"><span data-stu-id="2d887-156">(Inherited from <a href="/dotnet/api/system.io.stream">Stream</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="2d887-158"><a href="/dotnet/api/system.io.stream.beginwrite#System_IO_Stream_BeginWrite_System_Byte___System_Int32_System_Int32_System_AsyncCallback_System_Object_">BeginWrite</a></span><span class="sxs-lookup"><span data-stu-id="2d887-158"><a href="/dotnet/api/system.io.stream.beginwrite#System_IO_Stream_BeginWrite_System_Byte___System_Int32_System_Int32_System_AsyncCallback_System_Object_">BeginWrite</a></span></span></td>
<td><span data-ttu-id="2d887-159"> (繼承自 <a href="/dotnet/api/system.io.stream">Stream</a>。 ) </span><span class="sxs-lookup"><span data-stu-id="2d887-159">(Inherited from <a href="/dotnet/api/system.io.stream">Stream</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="2d887-161"><a href="/dotnet/api/system.io.stream.close#System_IO_Stream_Close">關閉</a></span><span class="sxs-lookup"><span data-stu-id="2d887-161"><a href="/dotnet/api/system.io.stream.close#System_IO_Stream_Close">Close</a></span></span></td>
<td><span data-ttu-id="2d887-162"> (繼承自 <a href="/dotnet/api/system.io.stream">Stream</a>。 ) </span><span class="sxs-lookup"><span data-stu-id="2d887-162">(Inherited from <a href="/dotnet/api/system.io.stream">Stream</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="2d887-164"><a href="/dotnet/api/system.marshalbyrefobject.createobjref#System_MarshalByRefObject_CreateObjRef_System_Type_">CreateObjRef</a></span><span class="sxs-lookup"><span data-stu-id="2d887-164"><a href="/dotnet/api/system.marshalbyrefobject.createobjref#System_MarshalByRefObject_CreateObjRef_System_Type_">CreateObjRef</a></span></span></td>
<td><span data-ttu-id="2d887-165"> (繼承自 <a href="/dotnet/api/system.marshalbyrefobject">MarshalByRefObject</a>。 ) </span><span class="sxs-lookup"><span data-stu-id="2d887-165">(Inherited from <a href="/dotnet/api/system.marshalbyrefobject">MarshalByRefObject</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="2d887-167"><a href="/dotnet/api/system.io.stream.createwaithandle#System_IO_Stream_CreateWaitHandle">CreateWaitHandle</a></span><span class="sxs-lookup"><span data-stu-id="2d887-167"><a href="/dotnet/api/system.io.stream.createwaithandle#System_IO_Stream_CreateWaitHandle">CreateWaitHandle</a></span></span></td>
<td><span data-ttu-id="2d887-168"><strong>已淘汰。</strong></span><span class="sxs-lookup"><span data-stu-id="2d887-168"><strong>Obsolete.</strong></span></span> <span data-ttu-id="2d887-169"> (繼承自 <a href="/dotnet/api/system.io.stream">Stream</a>。 ) </span><span class="sxs-lookup"><span data-stu-id="2d887-169">(Inherited from <a href="/dotnet/api/system.io.stream">Stream</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="2d887-171"><a href="/dotnet/api/system.io.stream.dispose#System_IO_Stream_Dispose">Dispose () </a></span><span class="sxs-lookup"><span data-stu-id="2d887-171"><a href="/dotnet/api/system.io.stream.dispose#System_IO_Stream_Dispose">Dispose()</a></span></span></td>
<td><span data-ttu-id="2d887-172"> (繼承自 <a href="/dotnet/api/system.io.stream">Stream</a>。 ) </span><span class="sxs-lookup"><span data-stu-id="2d887-172">(Inherited from <a href="/dotnet/api/system.io.stream">Stream</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="2d887-174"><a href="/dotnet/api/system.io.stream.dispose#System_IO_Stream_Dispose_System_Boolean_">Dispose (布林值) </a></span><span class="sxs-lookup"><span data-stu-id="2d887-174"><a href="/dotnet/api/system.io.stream.dispose#System_IO_Stream_Dispose_System_Boolean_">Dispose(Boolean)</a></span></span></td>
<td><span data-ttu-id="2d887-175"> (繼承自 <a href="/dotnet/api/system.io.stream">Stream</a>。 ) </span><span class="sxs-lookup"><span data-stu-id="2d887-175">(Inherited from <a href="/dotnet/api/system.io.stream">Stream</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="2d887-177"><a href="/dotnet/api/system.io.stream.endread#System_IO_Stream_EndRead_System_IAsyncResult_">EndRead</a></span><span class="sxs-lookup"><span data-stu-id="2d887-177"><a href="/dotnet/api/system.io.stream.endread#System_IO_Stream_EndRead_System_IAsyncResult_">EndRead</a></span></span></td>
<td><span data-ttu-id="2d887-178"> (繼承自 <a href="/dotnet/api/system.io.stream">Stream</a>。 ) </span><span class="sxs-lookup"><span data-stu-id="2d887-178">(Inherited from <a href="/dotnet/api/system.io.stream">Stream</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="2d887-180"><a href="/dotnet/api/system.io.stream.endwrite#System_IO_Stream_EndWrite_System_IAsyncResult_">EndWrite</a></span><span class="sxs-lookup"><span data-stu-id="2d887-180"><a href="/dotnet/api/system.io.stream.endwrite#System_IO_Stream_EndWrite_System_IAsyncResult_">EndWrite</a></span></span></td>
<td><span data-ttu-id="2d887-181"> (繼承自 <a href="/dotnet/api/system.io.stream">Stream</a>。 ) </span><span class="sxs-lookup"><span data-stu-id="2d887-181">(Inherited from <a href="/dotnet/api/system.io.stream">Stream</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="2d887-183"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">等於</a></span><span class="sxs-lookup"><span data-stu-id="2d887-183"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="2d887-184"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="2d887-184">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="2d887-186"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">完成</a></span><span class="sxs-lookup"><span data-stu-id="2d887-186"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="2d887-187"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="2d887-187">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="2d887-189"><a href="dn334193(v=exchg.10).md">清除</a></span><span class="sxs-lookup"><span data-stu-id="2d887-189"><a href="dn334193(v=exchg.10).md">Flush</a></span></span></td>
<td><span data-ttu-id="2d887-190">清除資料流程。</span><span class="sxs-lookup"><span data-stu-id="2d887-190">Flush the stream.</span></span> <span data-ttu-id="2d887-191"> (覆寫 <a href="/dotnet/api/system.io.stream.flush#System_IO_Stream_Flush">資料流程。 </a>排清 () 。 ) </span><span class="sxs-lookup"><span data-stu-id="2d887-191">(Overrides <a href="/dotnet/api/system.io.stream.flush#System_IO_Stream_Flush">Stream.Flush()</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="2d887-193"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="2d887-193"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="2d887-194"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="2d887-194">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="2d887-196"><a href="/dotnet/api/system.marshalbyrefobject.getlifetimeservice#System_MarshalByRefObject_GetLifetimeService">GetLifetimeService</a></span><span class="sxs-lookup"><span data-stu-id="2d887-196"><a href="/dotnet/api/system.marshalbyrefobject.getlifetimeservice#System_MarshalByRefObject_GetLifetimeService">GetLifetimeService</a></span></span></td>
<td><span data-ttu-id="2d887-197"> (繼承自 <a href="/dotnet/api/system.marshalbyrefobject">MarshalByRefObject</a>。 ) </span><span class="sxs-lookup"><span data-stu-id="2d887-197">(Inherited from <a href="/dotnet/api/system.marshalbyrefobject">MarshalByRefObject</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="2d887-199"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="2d887-199"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="2d887-200"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="2d887-200">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="2d887-202"><a href="/dotnet/api/system.marshalbyrefobject.initializelifetimeservice#System_MarshalByRefObject_InitializeLifetimeService">InitializeLifetimeService</a></span><span class="sxs-lookup"><span data-stu-id="2d887-202"><a href="/dotnet/api/system.marshalbyrefobject.initializelifetimeservice#System_MarshalByRefObject_InitializeLifetimeService">InitializeLifetimeService</a></span></span></td>
<td><span data-ttu-id="2d887-203"> (繼承自 <a href="/dotnet/api/system.marshalbyrefobject">MarshalByRefObject</a>。 ) </span><span class="sxs-lookup"><span data-stu-id="2d887-203">(Inherited from <a href="/dotnet/api/system.marshalbyrefobject">MarshalByRefObject</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="2d887-205"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone () </a></span><span class="sxs-lookup"><span data-stu-id="2d887-205"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone()</a></span></span></td>
<td><span data-ttu-id="2d887-206"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="2d887-206">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="2d887-208"><a href="/dotnet/api/system.marshalbyrefobject.memberwiseclone#System_MarshalByRefObject_MemberwiseClone_System_Boolean_">MemberwiseClone (布林值) </a></span><span class="sxs-lookup"><span data-stu-id="2d887-208"><a href="/dotnet/api/system.marshalbyrefobject.memberwiseclone#System_MarshalByRefObject_MemberwiseClone_System_Boolean_">MemberwiseClone(Boolean)</a></span></span></td>
<td><span data-ttu-id="2d887-209"> (繼承自 <a href="/dotnet/api/system.marshalbyrefobject">MarshalByRefObject</a>。 ) </span><span class="sxs-lookup"><span data-stu-id="2d887-209">(Inherited from <a href="/dotnet/api/system.marshalbyrefobject">MarshalByRefObject</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="2d887-211"><a href="dn334198(v=exchg.10).md">讀取</a></span><span class="sxs-lookup"><span data-stu-id="2d887-211"><a href="dn334198(v=exchg.10).md">Read</a></span></span></td>
<td><span data-ttu-id="2d887-212">從目前的資料流讀取位元組序列，並依讀取的位元組數將資料流中的位置往前移。</span><span class="sxs-lookup"><span data-stu-id="2d887-212">Reads a sequence of bytes from the current stream and advances the position within the stream by the number of bytes read.</span></span> <span data-ttu-id="2d887-213"> (覆寫 <a href="/dotnet/api/system.io.stream.read#System_IO_Stream_Read_System_Byte___System_Int32_System_Int32_">資料流程。讀取 ( []，int32，int32) </a>. ) </span><span class="sxs-lookup"><span data-stu-id="2d887-213">(Overrides <a href="/dotnet/api/system.io.stream.read#System_IO_Stream_Read_System_Byte___System_Int32_System_Int32_">Stream.Read([], Int32, Int32)</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="2d887-215"><a href="/dotnet/api/system.io.stream.readbyte#System_IO_Stream_ReadByte">ReadByte</a></span><span class="sxs-lookup"><span data-stu-id="2d887-215"><a href="/dotnet/api/system.io.stream.readbyte#System_IO_Stream_ReadByte">ReadByte</a></span></span></td>
<td><span data-ttu-id="2d887-216"> (繼承自 <a href="/dotnet/api/system.io.stream">Stream</a>。 ) </span><span class="sxs-lookup"><span data-stu-id="2d887-216">(Inherited from <a href="/dotnet/api/system.io.stream">Stream</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="2d887-218"><a href="dn334154(v=exchg.10).md">Seek</a></span><span class="sxs-lookup"><span data-stu-id="2d887-218"><a href="dn334154(v=exchg.10).md">Seek</a></span></span></td>
<td><span data-ttu-id="2d887-219">在目前資料流中設定位置。</span><span class="sxs-lookup"><span data-stu-id="2d887-219">Sets the position in the current stream.</span></span> <span data-ttu-id="2d887-220"> (覆寫 <a href="/dotnet/api/system.io.stream.seek#System_IO_Stream_Seek_System_Int64_System_IO_SeekOrigin_">資料流程。搜尋 (Int64，SeekOrigin) </a>。 ) </span><span class="sxs-lookup"><span data-stu-id="2d887-220">(Overrides <a href="/dotnet/api/system.io.stream.seek#System_IO_Stream_Seek_System_Int64_System_IO_SeekOrigin_">Stream.Seek(Int64, SeekOrigin)</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="2d887-222"><a href="dn334196(v=exchg.10).md">SetLength</a></span><span class="sxs-lookup"><span data-stu-id="2d887-222"><a href="dn334196(v=exchg.10).md">SetLength</a></span></span></td>
<td><span data-ttu-id="2d887-223">設定資料流的長度。</span><span class="sxs-lookup"><span data-stu-id="2d887-223">Sets the length of the stream.</span></span> <span data-ttu-id="2d887-224"> (覆寫 <a href="/dotnet/api/system.io.stream.setlength#System_IO_Stream_SetLength_System_Int64_">Stream. SetLength (Int64) </a>。 ) </span><span class="sxs-lookup"><span data-stu-id="2d887-224">(Overrides <a href="/dotnet/api/system.io.stream.setlength#System_IO_Stream_SetLength_System_Int64_">Stream.SetLength(Int64)</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="2d887-226"><a href="dn334149(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="2d887-226"><a href="dn334149(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="2d887-227">傳回表示目前<a href="dn334143(v=exchg.10).md">ColumnStream</a>的<a href="/dotnet/api/system.string">字串</a>。</span><span class="sxs-lookup"><span data-stu-id="2d887-227">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn334143(v=exchg.10).md">ColumnStream</a>.</span></span> <span data-ttu-id="2d887-228"> (會覆寫 <a href="/dotnet/api/system.object.tostring#System_Object_ToString">物件 ToString () </a>。 ) </span><span class="sxs-lookup"><span data-stu-id="2d887-228">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="2d887-230"><a href="dn334197(v=exchg.10).md">寫入</a></span><span class="sxs-lookup"><span data-stu-id="2d887-230"><a href="dn334197(v=exchg.10).md">Write</a></span></span></td>
<td><span data-ttu-id="2d887-231">將位元組序列寫入至目前的資料流，並依寫入的位元組數將資料流中目前的位置往前移。</span><span class="sxs-lookup"><span data-stu-id="2d887-231">Writes a sequence of bytes to the current stream and advances the current position within this stream by the number of bytes written.</span></span> <span data-ttu-id="2d887-232"> (覆寫 <a href="/dotnet/api/system.io.stream.write#System_IO_Stream_Write_System_Byte___System_Int32_System_Int32_">資料流程。寫入 ( []，int32，int32) </a>。 ) </span><span class="sxs-lookup"><span data-stu-id="2d887-232">(Overrides <a href="/dotnet/api/system.io.stream.write#System_IO_Stream_Write_System_Byte___System_Int32_System_Int32_">Stream.Write([], Int32, Int32)</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="2d887-234"><a href="/dotnet/api/system.io.stream.writebyte#System_IO_Stream_WriteByte_System_Byte_">WriteByte</a></span><span class="sxs-lookup"><span data-stu-id="2d887-234"><a href="/dotnet/api/system.io.stream.writebyte#System_IO_Stream_WriteByte_System_Byte_">WriteByte</a></span></span></td>
<td><span data-ttu-id="2d887-235"> (繼承自 <a href="/dotnet/api/system.io.stream">Stream</a>。 ) </span><span class="sxs-lookup"><span data-stu-id="2d887-235">(Inherited from <a href="/dotnet/api/system.io.stream">Stream</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2d887-236">頁首</span><span class="sxs-lookup"><span data-stu-id="2d887-236">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="2d887-237">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2d887-237">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2d887-238">參考</span><span class="sxs-lookup"><span data-stu-id="2d887-238">Reference</span></span>

[<span data-ttu-id="2d887-239">ColumnStream 類別</span><span class="sxs-lookup"><span data-stu-id="2d887-239">ColumnStream class</span></span>](./columnstream-class.md)

[<span data-ttu-id="2d887-240">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="2d887-240">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

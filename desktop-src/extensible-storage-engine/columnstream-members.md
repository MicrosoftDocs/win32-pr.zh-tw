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
# <a name="columnstream-members"></a>ColumnStream 成員

包含受保護的成員  
包含繼承的成員  

這個類別會提供 long 值資料行的串流介面 (亦即 [LongBinary](./jet-coltyp-enumeration.md) 或) [LongText](./jet-coltyp-enumeration.md) 類型的資料行。

[ColumnStream](./columnstream-class.md)類型會公開下列成員。

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
<td><a href="dn334142(v=exchg.10).md">ColumnStream</a></td>
<td>初始化 ColumnStream 類別的新實例。</td>
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
<td><a href="dn334201(v=exchg.10).md">CanRead</a></td>
<td>取得值，指出資料流程是否支援讀取。  (覆寫 <a href="/dotnet/api/system.io.stream.canread#System_IO_Stream_CanRead">CanRead</a>。 ) </td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn334153(v=exchg.10).md">CanSeek</a></td>
<td>取得值，指出資料流是否支援搜尋。  (覆寫 <a href="/dotnet/api/system.io.stream.canseek#System_IO_Stream_CanSeek">CanSeek</a>。 ) </td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="/dotnet/api/system.io.stream.cantimeout#System_IO_Stream_CanTimeout">CanTimeout</a></td>
<td> (繼承自 <a href="/dotnet/api/system.io.stream">Stream</a>。 ) </td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn334204(v=exchg.10).md">CanWrite</a></td>
<td>取得值，指出資料流是否支援寫入。  (覆寫 <a href="/dotnet/api/system.io.stream.canwrite#System_IO_Stream_CanWrite">CanWrite</a>。 ) </td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn334159(v=exchg.10).md">Itag</a></td>
<td>取得或設定資料行的 itag。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn334205(v=exchg.10).md">長度</a></td>
<td>取得目前的資料流程長度。  (覆寫 <a href="/dotnet/api/system.io.stream.length#System_IO_Stream_Length">資料流程. Length</a>. ) </td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn334161(v=exchg.10).md">位置</a></td>
<td>取得或設定資料流中目前的位置。  (覆寫 <a href="/dotnet/api/system.io.stream.position#System_IO_Stream_Position">資料流程。位置</a>) </td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="/dotnet/api/system.io.stream.readtimeout#System_IO_Stream_ReadTimeout">ReadTimeout</a></td>
<td> (繼承自 <a href="/dotnet/api/system.io.stream">Stream</a>。 ) </td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="/dotnet/api/system.io.stream.writetimeout#System_IO_Stream_WriteTimeout">WriteTimeout</a></td>
<td> (繼承自 <a href="/dotnet/api/system.io.stream">Stream</a>。 ) </td>
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
<td><a href="/dotnet/api/system.io.stream.beginread#System_IO_Stream_BeginRead_System_Byte___System_Int32_System_Int32_System_AsyncCallback_System_Object_">BeginRead</a></td>
<td> (繼承自 <a href="/dotnet/api/system.io.stream">Stream</a>。 ) </td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><a href="/dotnet/api/system.io.stream.beginwrite#System_IO_Stream_BeginWrite_System_Byte___System_Int32_System_Int32_System_AsyncCallback_System_Object_">BeginWrite</a></td>
<td> (繼承自 <a href="/dotnet/api/system.io.stream">Stream</a>。 ) </td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><a href="/dotnet/api/system.io.stream.close#System_IO_Stream_Close">關閉</a></td>
<td> (繼承自 <a href="/dotnet/api/system.io.stream">Stream</a>。 ) </td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><a href="/dotnet/api/system.marshalbyrefobject.createobjref#System_MarshalByRefObject_CreateObjRef_System_Type_">CreateObjRef</a></td>
<td> (繼承自 <a href="/dotnet/api/system.marshalbyrefobject">MarshalByRefObject</a>。 ) </td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.io.stream.createwaithandle#System_IO_Stream_CreateWaitHandle">CreateWaitHandle</a></td>
<td><strong>已淘汰。</strong>  (繼承自 <a href="/dotnet/api/system.io.stream">Stream</a>。 ) </td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><a href="/dotnet/api/system.io.stream.dispose#System_IO_Stream_Dispose">Dispose () </a></td>
<td> (繼承自 <a href="/dotnet/api/system.io.stream">Stream</a>。 ) </td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.io.stream.dispose#System_IO_Stream_Dispose_System_Boolean_">Dispose (布林值) </a></td>
<td> (繼承自 <a href="/dotnet/api/system.io.stream">Stream</a>。 ) </td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><a href="/dotnet/api/system.io.stream.endread#System_IO_Stream_EndRead_System_IAsyncResult_">EndRead</a></td>
<td> (繼承自 <a href="/dotnet/api/system.io.stream">Stream</a>。 ) </td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><a href="/dotnet/api/system.io.stream.endwrite#System_IO_Stream_EndWrite_System_IAsyncResult_">EndWrite</a></td>
<td> (繼承自 <a href="/dotnet/api/system.io.stream">Stream</a>。 ) </td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">等於</a></td>
<td> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">完成</a></td>
<td> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><a href="dn334193(v=exchg.10).md">清除</a></td>
<td>清除資料流程。  (覆寫 <a href="/dotnet/api/system.io.stream.flush#System_IO_Stream_Flush">資料流程。 </a>排清 () 。 ) </td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></td>
<td> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><a href="/dotnet/api/system.marshalbyrefobject.getlifetimeservice#System_MarshalByRefObject_GetLifetimeService">GetLifetimeService</a></td>
<td> (繼承自 <a href="/dotnet/api/system.marshalbyrefobject">MarshalByRefObject</a>。 ) </td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></td>
<td> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><a href="/dotnet/api/system.marshalbyrefobject.initializelifetimeservice#System_MarshalByRefObject_InitializeLifetimeService">InitializeLifetimeService</a></td>
<td> (繼承自 <a href="/dotnet/api/system.marshalbyrefobject">MarshalByRefObject</a>。 ) </td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone () </a></td>
<td> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.marshalbyrefobject.memberwiseclone#System_MarshalByRefObject_MemberwiseClone_System_Boolean_">MemberwiseClone (布林值) </a></td>
<td> (繼承自 <a href="/dotnet/api/system.marshalbyrefobject">MarshalByRefObject</a>。 ) </td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><a href="dn334198(v=exchg.10).md">讀取</a></td>
<td>從目前的資料流讀取位元組序列，並依讀取的位元組數將資料流中的位置往前移。  (覆寫 <a href="/dotnet/api/system.io.stream.read#System_IO_Stream_Read_System_Byte___System_Int32_System_Int32_">資料流程。讀取 ( []，int32，int32) </a>. ) </td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><a href="/dotnet/api/system.io.stream.readbyte#System_IO_Stream_ReadByte">ReadByte</a></td>
<td> (繼承自 <a href="/dotnet/api/system.io.stream">Stream</a>。 ) </td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><a href="dn334154(v=exchg.10).md">Seek</a></td>
<td>在目前資料流中設定位置。  (覆寫 <a href="/dotnet/api/system.io.stream.seek#System_IO_Stream_Seek_System_Int64_System_IO_SeekOrigin_">資料流程。搜尋 (Int64，SeekOrigin) </a>。 ) </td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><a href="dn334196(v=exchg.10).md">SetLength</a></td>
<td>設定資料流的長度。  (覆寫 <a href="/dotnet/api/system.io.stream.setlength#System_IO_Stream_SetLength_System_Int64_">Stream. SetLength (Int64) </a>。 ) </td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><a href="dn334149(v=exchg.10).md">ToString</a></td>
<td>傳回表示目前<a href="dn334143(v=exchg.10).md">ColumnStream</a>的<a href="/dotnet/api/system.string">字串</a>。  (會覆寫 <a href="/dotnet/api/system.object.tostring#System_Object_ToString">物件 ToString () </a>。 ) </td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><a href="dn334197(v=exchg.10).md">寫入</a></td>
<td>將位元組序列寫入至目前的資料流，並依寫入的位元組數將資料流中目前的位置往前移。  (覆寫 <a href="/dotnet/api/system.io.stream.write#System_IO_Stream_Write_System_Byte___System_Int32_System_Int32_">資料流程。寫入 ( []，int32，int32) </a>。 ) </td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><a href="/dotnet/api/system.io.stream.writebyte#System_IO_Stream_WriteByte_System_Byte_">WriteByte</a></td>
<td> (繼承自 <a href="/dotnet/api/system.io.stream">Stream</a>。 ) </td>
</tr>
</tbody>
</table>


頁首

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[ColumnStream 類別](./columnstream-class.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)

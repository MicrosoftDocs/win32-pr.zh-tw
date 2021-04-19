---
title: DataDefinitionType 複雜類型
description: 定義您想要包含在事件中的資料項目。 |DataDefinitionType 複雜類型
ms.assetid: f4234e54-a5a8-48e4-941f-05107dcd3f88
keywords:
- DataDefinitionType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- DataDefinitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 19584c28a7bdf7ae01b87d1f414b9464b7b4271d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106992525"
---
# <a name="datadefinitiontype-complex-type"></a>DataDefinitionType 複雜類型

定義您想要包含在事件中的資料項目。

``` syntax
<xs:complexType name="DataDefinitionType"
    mixed="true"
>
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="name"
                type="string"
                use="required"
             />
            <xs:attribute name="inType"
                type="QName"
                use="required"
             />
            <xs:attribute name="outType"
                type="QName"
                use="optional"
             />
            <xs:attribute name="map"
                type="string"
                use="optional"
             />
            <xs:attribute name="length"
                type="LengthType"
                use="optional"
             />
            <xs:attribute name="count"
                type="CountType"
                use="optional"
             />
            <xs:anyAttribute
                processContents="lax"
                namespace="##other"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a>屬性



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>名稱</th>
<th>類型</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>count</td>
<td><a href="eventmanifestschema-counttype-simpletype.md"><strong>CountType</strong></a></td>
<td>如果資料項目是陣列，則為數組中的元素數目。 您可以指定包含計數的其他資料項目的實際計數或名稱。 <br/></td>
</tr>
<tr class="even">
<td>inType</td>
<td><strong>QName</strong></td>
<td>這項資料項目的資料類型。 如需預先定義的輸入資料類型清單，請參閱 <a href="eventmanifestschema-inputtype-complextype.md"><strong>InputType</strong></a> 複雜型別。<br/></td>
</tr>
<tr class="odd">
<td>長度</td>
<td><a href="eventmanifestschema-lengthtype-simpletype.md"><strong>LengthType</strong></a></td>
<td>變數長度資料項目的長度，例如二進位 blob。 針對二進位資料，指定以位元組為單位的長度，並指定字串資料的長度（以字元為單位）。 您可以指定包含長度的其他資料項目的實際長度或名稱。<br/> 如果您使用 length 屬性來指定固定長度的字串，則必須將字串填補到其固定長度，以允許在結尾使用 null 結束字元字元 (例如，如果長度為5，則字串 &quot; abc &quot; 必須填補為 &quot; abc &quot; 。 字串長度必須包含 null 結束字元字元。<br/></td>
</tr>
<tr class="even">
<td>map</td>
<td>字串</td>
<td>用來將整數值對應至字串的名稱/值對應名稱。 資料項目的資料類型必須屬於下列其中一種類型：<br/>
<ul>
<li>win:UInt8</li>
<li>win:UInt16</li>
<li>win:UInt32</li>
</ul></td>
</tr>
<tr class="odd">
<td>NAME</td>
<td>字串</td>
<td>資料項目的名稱。 如果您在範本中指定 <a href="eventmanifestschema-userdata-templateitemtype-element.md"><strong>UserData</strong></a> 區段，您可以使用此名稱來參考 XML 片段中的這個資料項目。 如果這個資料項目包含長度或計數值，您也可以在另一個資料項目的長度或計數屬性中參考此名稱。<br/> <strong>Windows Vista：</strong> 這個屬性是選擇性的。<br/></td>
</tr>
<tr class="even">
<td>outType</td>
<td><strong>QName</strong></td>
<td>轉譯這個資料項目時要使用的資料型別。 如需預先定義之輸出資料類型的清單，請參閱 <a href="eventmanifestschema-outputtype-complextype.md"><strong>OutputType</strong></a> 複雜型別。<br/> <strong>Windows Vista：</strong> 輸出類型會被忽略，而服務會根據輸入類型來決定型別。<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>備註

對於可變長度的輸入類型（例如二進位 blob），您必須使用 length 屬性來明確指定資料的大小。 若為字串，只有當字串的長度固定時，才指定 length 屬性。

## <a name="examples"></a>範例

以下是一些資料項目定義的範例。


```XML
<!-- The data item is an 8-bit integer -->
<data name="binaryChar" inType="win:UInt8">
 
<!-- The data item is a single ANSI character -->
<data name="ansiChar" inType="win:UInt8" outtype="xs:string">
 
<!-- The data item is a single Unicode character -->
<data name="unicodeChar" inType="win:UInt16" outtype="xs:string">
 
<!-- The data item is an IP address that is rendered as a dot separated list of interger values -->
<data name="ipAddress" inType="win:UInt32" outtype="win:IPv4">
 
<!-- The data item is a Boolean value -->
<data name="success" inType="win:boolean">
 
<!-- The data item is a null-terminated ANSI string -->
<data name="string" inType="win:AnsiString"> 

<!-- The data item is a fixed length ANSI string -->
<data name="string" inType="win:AnsiString" length="42"> 
 
<!-- The data item is a fixed length array of null-terminated ANSI strings -->
<data name="strings" inType="win:AnsiString" count="20">
 
<!-- The data item is a fixed length array of fixed length ANSI strings -->
<data name="strings" inType="win:AnsiString" length="42" count="20">
 
<!-- The data item is a variable length array of same sized ANSI strings -->
<data name="stringLength" inType="win:UInt16">
<data name="arrayCount" inType="win:Uint16">
<data name="strings" inType="win:AnsiString" length="stringLength" count="arrayCount"> 
 
<!-- For binary data, you must specify the size.
<!-- The data item is a fixed length array of fixed length binary blobs -->
<data name="blobs" inType="win:Binary" length="42" count="20">

<!-- The data item is a fixed length binary blob -->
<data name="blob" inType="win:Binary" length="42">

<!-- The following are illegal binary data definitions -->
<!-- This definition is illegal because no length is specified -->
<data name="blob" inType="win:Binary"> 
 
<!-- This definition is illegal because you cannot determine the length of each binary blob -->
<data name="blob" inType="win:Binary" count="20"> 
 
<!-- The data item is a variable length array of structures. Each structure -->
<!-- contains an array of same sized ANSI strings --> 
<data name="arrayStructCount" inType="win:UInt16">
<struct name="countedStrings" count="arrayStructCount">
      <data name="stringLength" inType="win:UInt16">
      <data name="string" inType="win:AnsiString" length="stringLength">
</struct>
 
<!-- The data item is a time stamp that is rendered in 100ns units -->
<data name="timestamp" inType="win:UInt32" outType="win:ETWTIME">

<!-- The data item is a fixed length array of integers --> 
<data name="integers" inType="win:UInt32" count="20">

<!-- The data item is a variable length array of integers -->
<data name="arrayCount" inType="win:UInt16"> 
<data name="integers" inType="win:UInt32" count="arrayCount"> 

<!-- The following is illegal because you cannot assign a length value to a data type of a known size -->
<data name="integer" inType="win:UInt32" length="42">
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



 

 






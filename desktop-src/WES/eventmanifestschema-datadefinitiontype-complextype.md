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
# <a name="datadefinitiontype-complex-type"></a><span data-ttu-id="39d4c-105">DataDefinitionType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="39d4c-105">DataDefinitionType Complex Type</span></span>

<span data-ttu-id="39d4c-106">定義您想要包含在事件中的資料項目。</span><span class="sxs-lookup"><span data-stu-id="39d4c-106">Defines a data item that you want to include with the event.</span></span>

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

## <a name="attributes"></a><span data-ttu-id="39d4c-107">屬性</span><span class="sxs-lookup"><span data-stu-id="39d4c-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="39d4c-108">名稱</span><span class="sxs-lookup"><span data-stu-id="39d4c-108">Name</span></span></th>
<th><span data-ttu-id="39d4c-109">類型</span><span class="sxs-lookup"><span data-stu-id="39d4c-109">Type</span></span></th>
<th><span data-ttu-id="39d4c-110">描述</span><span class="sxs-lookup"><span data-stu-id="39d4c-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="39d4c-111">count</span><span class="sxs-lookup"><span data-stu-id="39d4c-111">count</span></span></td>
<td><span data-ttu-id="39d4c-112"><a href="eventmanifestschema-counttype-simpletype.md"><strong>CountType</strong></a></span><span class="sxs-lookup"><span data-stu-id="39d4c-112"><a href="eventmanifestschema-counttype-simpletype.md"><strong>CountType</strong></a></span></span></td>
<td><span data-ttu-id="39d4c-113">如果資料項目是陣列，則為數組中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="39d4c-113">The number of elements in the array if the data item is an array.</span></span> <span data-ttu-id="39d4c-114">您可以指定包含計數的其他資料項目的實際計數或名稱。</span><span class="sxs-lookup"><span data-stu-id="39d4c-114">You can specify the actual count or the name of another data item that contains the count.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="39d4c-115">inType</span><span class="sxs-lookup"><span data-stu-id="39d4c-115">inType</span></span></td>
<td><span data-ttu-id="39d4c-116"><strong>QName</strong></span><span class="sxs-lookup"><span data-stu-id="39d4c-116"><strong>QName</strong></span></span></td>
<td><span data-ttu-id="39d4c-117">這項資料項目的資料類型。</span><span class="sxs-lookup"><span data-stu-id="39d4c-117">The data type for this data item.</span></span> <span data-ttu-id="39d4c-118">如需預先定義的輸入資料類型清單，請參閱 <a href="eventmanifestschema-inputtype-complextype.md"><strong>InputType</strong></a> 複雜型別。</span><span class="sxs-lookup"><span data-stu-id="39d4c-118">For a list of predefined input data types, see the <a href="eventmanifestschema-inputtype-complextype.md"><strong>InputType</strong></a> complex type.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="39d4c-119">長度</span><span class="sxs-lookup"><span data-stu-id="39d4c-119">length</span></span></td>
<td><span data-ttu-id="39d4c-120"><a href="eventmanifestschema-lengthtype-simpletype.md"><strong>LengthType</strong></a></span><span class="sxs-lookup"><span data-stu-id="39d4c-120"><a href="eventmanifestschema-lengthtype-simpletype.md"><strong>LengthType</strong></a></span></span></td>
<td><span data-ttu-id="39d4c-121">變數長度資料項目的長度，例如二進位 blob。</span><span class="sxs-lookup"><span data-stu-id="39d4c-121">The length of a variable length data item, such as a binary blob.</span></span> <span data-ttu-id="39d4c-122">針對二進位資料，指定以位元組為單位的長度，並指定字串資料的長度（以字元為單位）。</span><span class="sxs-lookup"><span data-stu-id="39d4c-122">For binary data, specify the length in bytes and for string data, specify the length in characters.</span></span> <span data-ttu-id="39d4c-123">您可以指定包含長度的其他資料項目的實際長度或名稱。</span><span class="sxs-lookup"><span data-stu-id="39d4c-123">You can specify the actual length or the name of another data item that contains the length.</span></span><br/> <span data-ttu-id="39d4c-124">如果您使用 length 屬性來指定固定長度的字串，則必須將字串填補到其固定長度，以允許在結尾使用 null 結束字元字元 (例如，如果長度為5，則字串 &quot; abc &quot; 必須填補為 &quot; abc &quot; 。</span><span class="sxs-lookup"><span data-stu-id="39d4c-124">If you use the length attribute to specify a fixed length string, you must pad the string to its fixed length allowing for the null-terminator character at the end (for example, if the length is 5, the string &quot;abc&quot; must be padded as &quot;abc &quot;.</span></span> <span data-ttu-id="39d4c-125">字串長度必須包含 null 結束字元字元。</span><span class="sxs-lookup"><span data-stu-id="39d4c-125">The string length must include the null-terminator character.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="39d4c-126">map</span><span class="sxs-lookup"><span data-stu-id="39d4c-126">map</span></span></td>
<td><span data-ttu-id="39d4c-127">字串</span><span class="sxs-lookup"><span data-stu-id="39d4c-127">string</span></span></td>
<td><span data-ttu-id="39d4c-128">用來將整數值對應至字串的名稱/值對應名稱。</span><span class="sxs-lookup"><span data-stu-id="39d4c-128">The name of the name/value map to use to map integer values to strings.</span></span> <span data-ttu-id="39d4c-129">資料項目的資料類型必須屬於下列其中一種類型：</span><span class="sxs-lookup"><span data-stu-id="39d4c-129">The data type of the data item must be of one of the following types:</span></span><br/>
<ul>
<li><span data-ttu-id="39d4c-130">win:UInt8</span><span class="sxs-lookup"><span data-stu-id="39d4c-130">win:UInt8</span></span></li>
<li><span data-ttu-id="39d4c-131">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="39d4c-131">win:UInt16</span></span></li>
<li><span data-ttu-id="39d4c-132">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="39d4c-132">win:UInt32</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="39d4c-133">NAME</span><span class="sxs-lookup"><span data-stu-id="39d4c-133">name</span></span></td>
<td><span data-ttu-id="39d4c-134">字串</span><span class="sxs-lookup"><span data-stu-id="39d4c-134">string</span></span></td>
<td><span data-ttu-id="39d4c-135">資料項目的名稱。</span><span class="sxs-lookup"><span data-stu-id="39d4c-135">The name of the data item.</span></span> <span data-ttu-id="39d4c-136">如果您在範本中指定 <a href="eventmanifestschema-userdata-templateitemtype-element.md"><strong>UserData</strong></a> 區段，您可以使用此名稱來參考 XML 片段中的這個資料項目。</span><span class="sxs-lookup"><span data-stu-id="39d4c-136">You can use the name to reference this data item in your XML fragment if you specify a <a href="eventmanifestschema-userdata-templateitemtype-element.md"><strong>UserData</strong></a> section in your template.</span></span> <span data-ttu-id="39d4c-137">如果這個資料項目包含長度或計數值，您也可以在另一個資料項目的長度或計數屬性中參考此名稱。</span><span class="sxs-lookup"><span data-stu-id="39d4c-137">You can also reference this name in a length or count attribute of another data item if this data item contains its length or count value.</span></span><br/> <span data-ttu-id="39d4c-138"><strong>Windows Vista：</strong> 這個屬性是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="39d4c-138"><strong>Windows Vista:</strong> This attribute is optional.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="39d4c-139">outType</span><span class="sxs-lookup"><span data-stu-id="39d4c-139">outType</span></span></td>
<td><span data-ttu-id="39d4c-140"><strong>QName</strong></span><span class="sxs-lookup"><span data-stu-id="39d4c-140"><strong>QName</strong></span></span></td>
<td><span data-ttu-id="39d4c-141">轉譯這個資料項目時要使用的資料型別。</span><span class="sxs-lookup"><span data-stu-id="39d4c-141">The data type to use when rendering this data item.</span></span> <span data-ttu-id="39d4c-142">如需預先定義之輸出資料類型的清單，請參閱 <a href="eventmanifestschema-outputtype-complextype.md"><strong>OutputType</strong></a> 複雜型別。</span><span class="sxs-lookup"><span data-stu-id="39d4c-142">For a list of predefined output data types, see the <a href="eventmanifestschema-outputtype-complextype.md"><strong>OutputType</strong></a> complex type.</span></span><br/> <span data-ttu-id="39d4c-143"><strong>Windows Vista：</strong> 輸出類型會被忽略，而服務會根據輸入類型來決定型別。</span><span class="sxs-lookup"><span data-stu-id="39d4c-143"><strong>Windows Vista:</strong> The output type is ignored, and the service determines the type based on the input type.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="39d4c-144">備註</span><span class="sxs-lookup"><span data-stu-id="39d4c-144">Remarks</span></span>

<span data-ttu-id="39d4c-145">對於可變長度的輸入類型（例如二進位 blob），您必須使用 length 屬性來明確指定資料的大小。</span><span class="sxs-lookup"><span data-stu-id="39d4c-145">For variable length input types, such as binary blobs, you must use the length attribute to explicitly specify the size of the data.</span></span> <span data-ttu-id="39d4c-146">若為字串，只有當字串的長度固定時，才指定 length 屬性。</span><span class="sxs-lookup"><span data-stu-id="39d4c-146">For strings, specify the length attribute only if the strings are of a fixed length.</span></span>

## <a name="examples"></a><span data-ttu-id="39d4c-147">範例</span><span class="sxs-lookup"><span data-stu-id="39d4c-147">Examples</span></span>

<span data-ttu-id="39d4c-148">以下是一些資料項目定義的範例。</span><span class="sxs-lookup"><span data-stu-id="39d4c-148">The following are a few examples of the data item definitions.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="39d4c-149">規格需求</span><span class="sxs-lookup"><span data-stu-id="39d4c-149">Requirements</span></span>



| <span data-ttu-id="39d4c-150">需求</span><span class="sxs-lookup"><span data-stu-id="39d4c-150">Requirement</span></span> | <span data-ttu-id="39d4c-151">值</span><span class="sxs-lookup"><span data-stu-id="39d4c-151">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="39d4c-152">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="39d4c-152">Minimum supported client</span></span><br/> | <span data-ttu-id="39d4c-153">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="39d4c-153">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="39d4c-154">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="39d4c-154">Minimum supported server</span></span><br/> | <span data-ttu-id="39d4c-155">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="39d4c-155">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 






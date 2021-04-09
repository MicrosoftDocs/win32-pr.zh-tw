---
description: 定義提供者和它所提供的計數器。
ms.assetid: 85299b01-5679-40f8-8aec-5c2ff8d7cfc8
title: 提供者複雜類型
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6eec52139710d0ffafe06f22504a735e59312818
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849280"
---
# <a name="provider-complex-type"></a>提供者複雜類型

定義提供者和它所提供的計數器。

``` syntax
<xs:complexType name="provider">
    <xs:choice
        minOccurs="0"
        maxOccurs="unbounded"
    >
        <xs:element name="counterSet"
            type="man:counterSet"
        >
            <xs:key name="uniqueCounterID">
                <xs:selector
                    xpath="./man:counter"
                 />
                <xs:field
                    xpath="@id"
                 />
            </xs:key>
            <xs:unique name="uniqueCounterName">
                <xs:selector
                    xpath="./man:counter"
                 />
                <xs:field
                    xpath="@name"
                 />
            </xs:unique>
            <xs:keyref name="existBaseID">
                <xs:selector
                    xpath="./man:counter"
                 />
                <xs:field
                    xpath="@baseID"
                 />
            </xs:keyref>
            <xs:keyref name="existPerfTimeID">
                <xs:selector
                    xpath="./man:counter"
                 />
                <xs:field
                    xpath="@perfTimeID"
                 />
            </xs:keyref>
            <xs:keyref name="existPerfFreqID">
                <xs:selector
                    xpath="./man:counter"
                 />
                <xs:field
                    xpath="@perfFreqID"
                 />
            </xs:keyref>
            <xs:keyref name="existMultiCounterID">
                <xs:selector
                    xpath="./man:counter"
                 />
                <xs:field
                    xpath="@multiCounterID"
                 />
            </xs:keyref>
            <xs:key name="uniqueStructNames">
                <xs:selector
                    xpath="./man:structs/man:struct"
                 />
                <xs:field
                    xpath="@name"
                 />
            </xs:key>
            <xs:keyref name="existCounterName">
                <xs:selector
                    xpath="./man:counter"
                 />
                <xs:field
                    xpath="@struct"
                 />
            </xs:keyref>
        </xs:element>
    </xs:choice>
    <xs:attribute name="symbol"
        type="man:CSymbolType"
        use="optional"
     />
    <xs:attribute name="callback"
        use="optional"
        default="default"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:enumeration
                    value="custom"
                 />
                <xs:enumeration
                    value="default"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="providerGuid"
        type="man:GUIDType"
        use="required"
     />
    <xs:attribute name="applicationIdentity"
        type="xs:string"
        use="required"
     />
    <xs:attribute name="providerType"
        use="optional"
        default="userMode"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:enumeration
                    value="userMode"
                 />
                <xs:enumeration
                    value="kernelMode"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="providerName"
        type="xs:string"
        use="optional"
        default="Counters"
     />
    <xs:attribute name="resourceBase"
        type="man:UInt32Type"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a>子元素



| 元素        | 類型                                                                   | Description                                                                                 |
|----------------|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| **counterSet** | [**男人： counterSet**](performance-counters-counterset-complex-type.md) | 識別包含一或多個邏輯相關計數器的計數器集合。<br/> |



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
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>applicationIdentity</td>
<td><strong>xs:string</strong></td>
<td>包含當地語系化資源字串（.exe 或 .dll 檔案）的二進位檔案名稱 (不包含二進位) 的路徑。<br/> Lodctr.exe 公用程式會使用選擇性 [<em>path</em>] 參數的路徑來搜尋二進位檔案。 例如， <strong>lodctr</strong> [<strong>/m：</strong><em>manifest</em> [<em>path</em>]]。 如果您未包含 [<em>path</em>] 參數，Lodctr.exe 會搜尋包含資訊清單的資料夾。<br/></td>
</tr>
<tr class="even">
<td>回撥</td>

<td>這個屬性指出當取用者執行某些動作時，您想要收到通知。 <br/> 如果您包含這個屬性，CTRPP 工具會使用替代的 <a href="counterinitialize.md"><strong>CounterInitialize</strong></a> 函式簽章，您可以使用此簽章來傳遞函式的名稱，以執行 <a href="/windows/desktop/api/Perflib/nc-perflib-perflibrequest"><strong>ControlCallback</strong></a> 回呼函式。<br/> 除了指定此屬性之外，您還可以使用 <strong>-NotificationCallback</strong><a href="ctrpp.md">CTRPP</a> 引數。<br/> <strong>Windows Vista：</strong> 這個屬性唯一有效的值為 &quot; custom &quot; 。 <a href="ctrpp.md">CTRPP</a>公用程式會產生<a href="/windows/desktop/api/Perflib/nc-perflib-perflibrequest"><strong>ControlCallback</strong></a>回呼函數的範本。 範本會包含在 CTRPP 產生的 .c 檔案中。 <br/> <br/></td>
</tr>
<tr class="odd">
<td>providerGuid</td>
<td><a href="performance-counters-guidtype-simple-type.md"><strong>男人： GUIDType</strong></a></td>
<td>可在資訊清單中唯一識別提供者的字串 GUID。 GUID 在資訊清單中必須是唯一的。<br/> 只有 (當您支援) 的並存安裝時，您才需要提供新的 GUID。<br/></td>
</tr>
<tr class="even">
<td>providerName</td>
<td><strong>xs:string</strong></td>
<td>用來建立 WMI Win32_PerfRawData 類別名稱的名稱。 如果您未指定名稱，則 &quot; &quot; 會使用計數器作為類別的名稱。<br/></td>
</tr>
<tr class="odd">
<td>providerType</td>

<td>識別提供者是否為使用者模式提供者、核心模式提供者或驅動程式提供者。 可能的值如下。<br/> 
<table>
<thead>
<tr class="header">
<th>詞彙</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="userMode"></span><span id="usermode"></span><span id="USERMODE"></span>userMode<br/></td>
<td>為使用者模式元件指定此模式，例如應用程式、DLL 或使用者模式驅動程式。 使用者模式元件的一般擴充功能為 .exe 或 .dll。 此為預設值。<br/></td>
</tr>
<tr class="even">
<td><span id="kernel"></span><span id="KERNEL"></span>內核<br/></td>
<td>為核心模式元件指定此模式，例如 WDM 或 WDF 驅動程式。 核心模式元件的一般延伸模組是 sys。<br/> <strong>Windows Vista 和 Windows Server 2008：</strong> 在 Windows 7 和 Windows Server 2008 R2 之前，不支援這個值。<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>resourceBase</td>
<td><a href="performance-counters-uint32type-simple-type.md"><strong>男人： UInt32Type</strong></a></td>
<td><p>定義 <a href="ctrpp.md">CTRPP</a> 用來產生資源識別碼的起始資源索引值。</p></td>
</tr>
<tr class="odd">
<td>符號</td>
<td><a href="performance-counters-csymboltype-simple-type.md"><strong>男人： CSymbolType</strong></a></td>
<td><p>識別提供者的符號名稱。 <a href="ctrpp.md">CTRPP</a>工具會建立控制碼變數，您可以在呼叫需要提供 (者控制碼的函式時使用，例如<a href="/windows/desktop/api/Perflib/nf-perflib-perfsetulongcountervalue"><strong>PerfSetULongCounterValue</strong></a>) 。 符號名稱是變數的名稱。</p>
<p>如果您在呼叫<a href="ctrpp.md">CTRPP</a>時包含<strong>-prefix</strong>引數，則前置詞字串會加入符號名稱的開頭。</p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



 

 





---
title: EventDefinitionType 複雜類型
description: 定義您的提供者可以撰寫的事件。
ms.assetid: 09ea89c9-6618-4874-ac72-5ee19cde4040
keywords:
- EventDefinitionType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- EventDefinitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b7719abea1e97cae88edd47d176e5c578d73f0b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106991781"
---
# <a name="eventdefinitiontype-complex-type"></a>EventDefinitionType 複雜類型

定義您的提供者可以撰寫的事件。

``` syntax
<xs:complexType name="EventDefinitionType">
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="value"
                type="UInt32Type"
                use="required"
             />
            <xs:attribute name="level"
                type="QName"
                use="optional"
             />
            <xs:attribute name="template"
                type="token"
                use="optional"
             />
            <xs:attribute name="channel"
                type="token"
                use="optional"
             />
            <xs:attribute name="keywords"
                type="QNameList"
                use="optional"
             />
            <xs:attribute name="task"
                type="QName"
                use="optional"
             />
            <xs:attribute name="opcode"
                type="QName"
                use="optional"
             />
            <xs:attribute name="symbol"
                type="CSymbolType"
                use="optional"
             />
            <xs:attribute name="version"
                type="unsignedByte"
                use="optional"
             />
            <xs:attribute name="message"
                type="strTableRef"
                use="optional"
             />
            <xs:attribute name="notLogged"
                type="boolean"
                use="optional"
                default="false"
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
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>通道</td>
<td>token</td>
<td>識別寫入事件之通道的識別碼。 指定您所定義或匯入之其中一個通道的通道識別碼。 如果通道未指定通道識別碼，請使用通道的名稱。 如需定義或匯入通道的詳細資訊，請參閱 <a href="eventmanifestschema-channellisttype-complextype.md"><strong>ChannelListType</strong></a> 複雜類型。<br/> 如果您未指定通道，則不會將事件寫入通道。 一般而言，不指定通道的唯一原因是您只是要將事件寫入至 ETW 會話。 如需詳細資訊，請參閱建立 ETW 會話的詳細資訊，請參閱 <a href="/windows/desktop/ETW/controlling-event-tracing-sessions">控制事件追蹤會話</a>。<br/></td>
</tr>
<tr class="even">
<td>關鍵字</td>
<td><a href="eventmanifestschema-qnamelist-simpletype.md"><strong>QNameList</strong></a></td>
<td>關鍵字名稱的空格分隔清單，用來識別這個事件所屬的事件類別。 從您定義的關鍵字清單中指定關鍵字名稱。 如需定義關鍵字的詳細資訊，請參閱 <a href="eventmanifestschema-keywordtype-complextype.md"><strong>KeywordType</strong></a> 複雜類型。<br/> 如果您未指定關鍵字，則事件描述項會針對關鍵字包含零。<br/></td>
</tr>
<tr class="odd">
<td>等級</td>
<td><strong>QName</strong></td>
<td>寫入事件時要使用的詳細層級。 指定您在資訊清單中定義的層級名稱，或是包含在 Windows SDK 的 \Include\Winmeta.xml 檔中定義的其中一個層級的名稱。 如需定義層級的詳細資訊，請參閱 <a href="eventmanifestschema-leveltype-complextype.md"><strong>LevelType</strong></a> 複雜類型。<br/> 如果您未指定層級，事件描述項的層級就會包含零。<br/> 如果寫入事件的通道類型為 Admin，您必須指定層級。層級必須是 Winmeata.xml 中所定義的下列其中一個層級：
<ul>
<li>win:Critical</li>
<li>win:Error</li>
<li>win:Warning</li>
<li>win:Informational</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td>message</td>
<td><a href="eventmanifestschema-strtableref-simpletype.md"><strong>strTableRef</strong></a></td>
<td>事件的當地語系化訊息。 訊息字串會參考資訊清單之 <a href="eventmanifestschema-stringtable-resources-element.md"><strong>stringTable</strong></a> 區段中的當地語系化字串。<br/> 如果寫入事件的通道類型是 Admin，則必須指定訊息。<br/></td>
</tr>
<tr class="odd">
<td>notLogged</td>
<td>boolean</td>
<td>決定提供者是否要記錄此事件。 如果提供者記錄此事件，請指定 true;否則為 false。 使用這個屬性來表示提供者不再記錄此事件，而不是從資訊清單中移除事件。 在資訊清單中保留事件，可讓取用者將包含事件的舊版 etl 檔案解碼。<br/> <strong>Windows Server 2008 和 Windows Vista：</strong> 在 Windows SDK 的 Windows 7 版本之前隨附的訊息編譯器版本不支援這個屬性。<br/></td>
</tr>
<tr class="even">
<td>opcode</td>
<td><strong>QName</strong></td>
<td>在工作中識別作業的 opcode 名稱。 指定您在資訊清單中定義的 opcode 名稱，或 Winmeta.xml 中定義的其中一個操作碼。 如需定義 opcode 的詳細資訊，請參閱 <a href="eventmanifestschema-opcodetype-complextype.md"><strong>OpcodeType</strong></a> 複雜類型。<br/> 如果您參考的工作包含工作特定 (本機) 作業碼，則可以指定其中一個工作特定的作業碼，或在提供者層級定義的作業碼， (全域操作碼) 。 如果您指定全域操作碼，全域 opcode 的值不能與工作的其中一個本機作業碼相同。<br/> 如果您參考本機作業碼，則工作屬性必須參考本機作業碼所屬的工作。<br/> 如果您未指定作業碼，則事件描述項會針對 opcode 包含零。<br/></td>
</tr>
<tr class="odd">
<td>符號</td>
<td><a href="eventmanifestschema-csymboltype-simpletype.md"><strong>CSymbolType</strong></a></td>
<td>用來在應用程式中參考這個事件之事件描述項的符號。 <a href="message-compiler--mc-exe-.md"><strong>訊息編譯器 (MC.exe) </strong></a>會使用符號，在編譯器產生的標頭檔中建立事件描述項的常數。 如果您未指定符號，編譯器會為您產生一個符號。 當您呼叫 <a href="/windows/desktop/api/evntprov/nf-evntprov-eventwrite"><strong>EventWrite</strong></a> 函式來寫入事件時，會使用描述項。<br/></td>
</tr>
<tr class="even">
<td>工作 (task)</td>
<td><strong>QName</strong></td>
<td>識別產生此事件之元件或子元件的工作名稱。 指定您在資訊清單中定義的工作名稱。 如需定義工作的詳細資訊，請參閱 <a href="eventmanifestschema-tasktype-complextype.md"><strong>TaskType</strong></a> 複雜類型。<br/> 如果您未指定工作，則事件描述項會包含工作的零。<br/></td>
</tr>
<tr class="odd">
<td>template</td>
<td>token</td>
<td>範本的範本識別碼，定義此事件包含的資料項目。 指定您在資訊清單中定義的範本識別碼。 如需定義範本的詳細資訊，請參閱 <a href="eventmanifestschema-templateitemtype-complextype.md"><strong>TemplateItemType</strong></a> 複雜類型。<br/></td>
</tr>
<tr class="even">
<td>value</td>
<td><a href="eventmanifestschema-hexint32type-simpletype.md"><strong>UInt32Type</strong></a></td>
<td>事件識別項。 識別碼在您定義的事件清單中必須是唯一的。<br/></td>
</tr>
<tr class="odd">
<td>version</td>
<td>unsignedByte</td>
<td>事件定義的單位元組版本號碼。<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>備註

如果您使用 [**EvtFormatMessage**](/windows/desktop/api/WinEvt/nf-winevt-evtformatmessage) 來格式化事件 (的訊息字串，或使用事件檢視器來查看訊息字串) ，訊息字串可以包含插入字串和 Win32 **FormatMessage** 函數所支援的任何格式字串。 插入字串的限制為%*n* 或%*n*！ s！  (例如，%1) ，其中 *n* 是在事件範本中定義之資料項目的參考（以一為基礎）。 訊息字串也可以包含格式為%%*n* (的參數插入字串，例如% %4) 。 訊息可以包含的插入字串數目上限為100。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



 


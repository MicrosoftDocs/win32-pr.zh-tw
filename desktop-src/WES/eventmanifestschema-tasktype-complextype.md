---
title: TaskType 複雜類型
description: 定義應用程式的元件或子元件。 |TaskType 複雜類型
ms.assetid: d117636d-6363-43b6-ac5a-52234ac7c729
keywords:
- TaskType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- TaskType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ccad6813624d0a27a093ff4baa7fc8b9a6aa8b14
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106991430"
---
# <a name="tasktype-complex-type"></a>TaskType 複雜類型

定義應用程式的元件或子元件。

``` syntax
<xs:complexType name="TaskType"
    mixed="true"
>
    <xs:sequence>
        <xs:element name="opcodes"
            type="OpcodeListType"
            minOccurs="0"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="QName"
        use="required"
     />
    <xs:attribute name="symbol"
        type="CSymbolType"
        use="optional"
     />
    <xs:attribute name="value"
        type="UInt16Type"
        use="required"
     />
    <xs:attribute name="eventGUID"
        type="GUIDType"
        use="optional"
     />
    <xs:attribute name="message"
        type="strTableRef"
        use="optional"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>子元素



| 元素                                                         | 類型                                                                     | Description                                                                                                                            |
|-----------------------------------------------------------------|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**碼**](eventmanifestschema-opcodes-tasktype-element.md) | [**OpcodeListType**](eventmanifestschema-opcodelisttype-complextype.md) | 定義工作特定作業碼的清單。 您無法使用 Winmeta.xml 中為工作專屬的作業碼定義的 opcode 值。<br/> |



## <a name="attributes"></a>屬性



| 名稱      | 類型                                                              | Description                                                                                                                                                                                                                                                                                                      |
|-----------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| eventGUID | [**GUIDType**](eventmanifestschema-guidtype-simpletype.md)       | 識別工作的全域唯一識別碼（登錄格式）。 如果您使用-mof 訊息編譯器引數來產生下層支援的 MOF 類別，則需要這個屬性。<br/>                                                                                                   |
| message   | [**strTableRef**](eventmanifestschema-strtableref-simpletype.md) | 工作的當地語系化顯示名稱。 訊息字串會參考資訊清單之 [**stringTable**](eventmanifestschema-stringtable-resources-element.md) 區段中的當地語系化字串。 <br/>                                                                                                   |
| NAME      | **QName**                                                         | 工作的名稱。<br/>                                                                                                                                                                                                                                                                                 |
| 符號    | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | 用來參考應用程式中工作的符號。 [**訊息編譯器 (MC.exe)**](message-compiler--mc-exe-.md)會使用符號，在編譯器產生的標頭檔中建立工作的常數。 如果您未指定符號，編譯器會為您產生一個符號。<br/> |
| value     | [**UInt16Type**](eventmanifestschema-hexint16type-simpletype.md) | 在提供者所定義的工作清單中，可唯一識別這項工作的數位值。 值的範圍必須介於1到239之間。<br/>                                                                                                                                             |



## <a name="examples"></a>範例

下列範例顯示如何指定工作。


```XML
<tasks>
  <task name="printspool:Disconnect" 
         symbol="PRINTSPOOL_TASK_DISCONNECT"
         value="0" 
         message="$(string.disconnect)"/>
 
  <task name="printspool:Connect" 
         symbol="PRINTSPOOL_TASK_CONNECT"
         value="1" 
         message="$(string.connect)">
       <opcodes>
          <opcode name="ReadRegistry" 
                  symbol="MYOPCODE_READ_REGISTRY" value="11"
                  message="$(string.ReadRegistry)"/>
       </opcodes>
   </task>
</tasks>
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



 

 






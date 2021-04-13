---
title: ProviderType 複雜類型
description: 定義提供者及其用來定義其事件的中繼資料。 |ProviderType 複雜類型
ms.assetid: 70199cf5-a6d0-4780-9ff1-ed083a5b49ac
keywords:
- ProviderType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- ProviderType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c258b3ff48cdd2f00f632fdce770b58182a531c7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322324"
---
# <a name="providertype-complex-type"></a>ProviderType 複雜類型

定義提供者及其用來定義其事件的中繼資料。

``` syntax
<xs:complexType name="ProviderType">
    <xs:choice
        minOccurs="0"
        maxOccurs="unbounded"
    >
        <xs:element name="channels"
            type="ChannelListType"
         />
        <xs:element name="levels"
            type="LevelListType"
         />
        <xs:element name="tasks"
            type="TaskListType"
         />
        <xs:element name="opcodes"
            type="OpcodeListType"
         />
        <xs:element name="keywords"
            type="KeywordListType"
         />
        <xs:element name="maps"
            type="MapType"
         />
        <xs:element name="namedQueries"
            type="NamedQueryType"
         />
        <xs:element name="templates"
            type="TemplateListType"
         />
        <xs:element name="events"
            type="DefinitionType"
         />
        <xs:element name="filters"
            type="FilterListType"
         />
        <xs:any
            processContents="lax"
            namespace="##other"
         />
    </xs:choice>
    <xs:attribute name="name"
        type="anyURI"
        use="required"
     />
    <xs:attribute name="guid"
        type="GUIDType"
        use="required"
     />
    <xs:attribute name="resourceFileName"
        type="filePath"
        use="optional"
     />
    <xs:attribute name="messageFileName"
        type="filePath"
        use="optional"
     />
    <xs:attribute name="parameterFileName"
        type="filePath"
        use="optional"
     />
    <xs:attribute name="helpLink"
        type="anyURI"
        use="optional"
     />
    <xs:attribute name="symbol"
        type="CSymbolType"
        use="required"
     />
    <xs:attribute name="message"
        type="strTableRef"
        use="optional"
     />
    <xs:attribute name="source"
        use="optional"
        default="Xml"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:enumeration
                    value="Xml"
                 />
                <xs:enumeration
                    value="Wbem"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="warnOnApplicationCompatibilityError"
        type="xs:boolean"
        use="optional"
        default="false"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>子元素



| 元素                                                                       | 類型                                                                         | Description                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**管道**](eventmanifestschema-channels-providertype-element.md)         | [**ChannelListType**](eventmanifestschema-channellisttype-complextype.md)   | 定義提供者可以記錄事件的通道清單。<br/>                                                                                                                                                                                      |
| [**事件**](eventmanifestschema-events-providertype-element.md)             | [**DefinitionType**](eventmanifestschema-definitiontype-complextype.md)     | 定義提供者可以記錄之事件的事件定義清單。<br/>                                                                                                                                                                       |
| **過濾 器**                                                                   | [**FilterListType**](eventmanifestschema-filterlisttype-complextype.md)     | 定義提供者所支援的篩選器清單。 您可以使用篩選準則（如同您對層級和關鍵字）來判斷是否要撰寫事件。 <br/> **Windows Server 2008 和 Windows Vista：** 在 Windows 7 之前不受支援。<br/> |
| [**關鍵 字**](eventmanifestschema-keywords-providertype-element.md)         | [**KeywordListType**](eventmanifestschema-keywordlisttype-complextype.md)   | 定義分類事件的關鍵字清單。<br/>                                                                                                                                                                                                 |
| [**水準**](eventmanifestschema-levels-providertype-element.md)             | [**LevelListType**](eventmanifestschema-levellisttype-complextype.md)       | 定義指定事件嚴重性的層級清單。<br/>                                                                                                                                                                                    |
| [**地圖**](eventmanifestschema-maps-providertype-element.md)                 | [**MapType**](eventmanifestschema-maptype-complextype.md)                   | 定義名稱/值組的清單，您可以在資訊清單的範本區段中參考。<br/>                                                                                                                                                 |
| [**namedQueries**](eventmanifestschema-namedqueries-providertype-element.md) | [**NamedQueryType**](eventmanifestschema-namedquerytype-complextype.md)     | 未使用。 定義已命名查詢的清單，這些查詢會查詢事件訊息字串中的值，並執行指定的動作（如果找到的話）。<br/>                                                                                                                 |
| [**碼**](eventmanifestschema-opcodes-providertype-element.md)           | [**OpcodeListType**](eventmanifestschema-opcodelisttype-complextype.md)     | 定義可用於將工作中的事件群組在一起的作業碼清單。<br/>                                                                                                                                                                          |
| [**任務**](eventmanifestschema-tasks-providertype-element.md)               | [**TaskListType**](eventmanifestschema-tasklisttype-complextype.md)         | 定義提供者可用來群組事件的工作清單。 一般而言，您會使用工作將提供者的功能或元件的事件分組。<br/>                                                                                              |
| [**範本**](eventmanifestschema-templates-providertype-element.md)       | [**TemplateListType**](eventmanifestschema-templatelisttype-complextype.md) | 定義範本清單，以指定要包含在事件中的資料。<br/>                                                                                                                                                                      |



## <a name="attributes"></a>屬性



| 名稱                                | 類型                                                              | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| guid                                | [**GUIDType**](eventmanifestschema-guidtype-simpletype.md)       | 可唯一識別提供者的 GUID。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| helpLink                            | anyURI                                                            | 提供提供者所引發事件相關資訊的內容 URL 或 MS 說明連結。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                           |
| message                             | [**strTableRef**](eventmanifestschema-strtableref-simpletype.md) | 提供者的當地語系化顯示名稱。 訊息字串會參考資訊清單之 [**stringTable**](eventmanifestschema-stringtable-resources-element.md) 區段中的當地語系化字串。 <br/>                                                                                                                                                                                                                                                                                                                           |
| messageFileName                     | [**filePath**](eventmanifestschema-filepath-simpletype.md)       | 檔案的完整路徑，該檔案包含提供者的當地語系化訊息資源。 檔案可以是可執行檔或 DLL 檔案。<br/>                                                                                                                                                                                                                                                                                                                                                                                               |
| NAME                                | anyURI                                                            | 提供者的名稱。 名稱的格式應為 *Company* - *Product* - *Component*。<br/> 名稱不能超過255個字元，且不能包含下列字元： ' > '、' < '、' & '、' "'、' \| '、' \\ '、'： '、' '、'？ '、' \* '，或代碼小於31的字元。 此外，名稱必須遵循檔案和登錄機碼名稱的一般條件約束。 您可以在 [命名](/windows/desktop/FileIO/naming-a-file)檔案和登錄專案 [大小限制](/windows/desktop/SysInfo/registry-element-size-limits)中找到這些條件約束。<br/> |
| parameterFileName                   | [**filePath**](eventmanifestschema-filepath-simpletype.md)       | 檔案的完整路徑，該檔案包含提供者的參數字串資源。 檔案可以是可執行檔或 DLL 檔案。 您可以指定一個以上的參數檔案，並以分號分隔。 當事件的訊息字串包含參數字串時，會搜尋該檔案。 參數可讓您提供可當地語系化的插入字串。 如需詳細資訊，請參閱「備註」。<br/>                                                                                                                                                |
| resourceFileName                    | [**filePath**](eventmanifestschema-filepath-simpletype.md)       | 檔案的完整路徑，該檔案包含提供者的中繼資料資源。 檔案可以是可執行檔或 DLL 檔案。<br/>                                                                                                                                                                                                                                                                                                                                                                                                        |
| source                              |                                                                   | 僅供內部使用。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| 符號                              | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | 用來參考應用程式中提供者 GUID 的符號。 [**訊息編譯器 (MC.exe)**](message-compiler--mc-exe-.md)會使用符號，在編譯器產生的標頭檔中，為提供者的 GUID 建立常數。<br/>                                                                                                                                                                                                                                                                           |
| warnOnApplicationCompatibilityError | **xs:boolean**                                                    | 僅供內部使用。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



## <a name="remarks"></a>備註

Windows 事件檢視器 (Eventvwr.exe) 會使用當地語系化的訊息字串（如果有的話）：否則，它會使用 name 屬性中的字串。

ResourceFileName、messageFileName 和 parameterFileName 的路徑可以包含環境變數。 如果您定義要在路徑中使用的新環境變數，則必須重新開機電腦，事件記錄檔服務才能挑選新的變數;否則，服務將無法找到您的提供者資源。

事件的訊息字串可以包含插入字串和參數字串。 插入字串的格式為%*n*，其中 *n* 是以一為起始的索引，可從事件的資料範本識別您想要插入至訊息的資料項目。 參數字串 (查看 **parameterFileName** 屬性) 的格式為%%*n*，其中 n 是訊息資料表中訊息的識別碼。 如果事件的訊息字串包含 "%1% %11 = %2% %12" 和 %1 和 %2 的資料項目值分別為8和2，而且% %11 和% %12 的參數字串分別為 "夸脫" 和 "加侖"，則格式化的字串會是 "8 夸脫 = 2 加侖"。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



 


---
title: instrumentationManifest 元素
description: 資訊清單的根節點。
ms.assetid: cb7b5201-be11-48f9-bcca-4606904f0c1d
keywords:
- instrumentationManifest 元素 EventLog
topic_type:
- apiref
api_name:
- instrumentationManifest
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7dac9ab8c8aa2a6caeacf43023c4995be69f293affd5dd5a904d7fb96d710266
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118343714"
---
# <a name="instrumentationmanifest-element"></a>instrumentationManifest 元素

資訊清單的根節點。

``` syntax
<xs:element name="instrumentationManifest">
    <xs:complexType>
        <xs:complexContent>
            <xs:extension
                base="InstrumentationManifestType"
            >
                <xs:choice
                    maxOccurs="3"
                >
                    <xs:choice>
                        <xs:element name="metadata"
                            type="MetadataType"
                         />
                        <xs:element name="instrumentation"
                            type="InstrumentationType"
                         />
                    </xs:choice>
                    <xs:element name="localization"
                        type="LocalizationType"
                     />
                    <xs:any
                        processContents="lax"
                        minOccurs="0"
                        maxOccurs="unbounded"
                        namespace="##other"
                     />
                </xs:choice>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a>子元素



| 元素                                                                                        | 類型                                                                               | 描述                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**儀錶**](eventmanifestschema-instrumentation-instrumentationmanifest-element.md) | [**Instrumentationtype.event**](eventmanifestschema-instrumentationtype-complextype.md) | 此區段會定義一或多個事件提供者，以及它們所記錄的事件。<br/>                                                                                                                                                                                                                     |
| [**定位**](eventmanifestschema-localization-instrumentationmanifest-element.md)       | [**LocalizationType**](eventmanifestschema-localizationtype-complextype.md)       | 此區段會定義取用者用來顯示的當地語系化訊息字串。 例如，此區段會包含提供者名稱的當地語系化訊息字串、您所定義的事件，以及您定義的任何事件屬性，例如通道、工作和作業碼。<br/> |
| [**元**](eventmanifestschema-metadata-instrumentationmanifest-element.md)               | [**MetadataType**](eventmanifestschema-metadatatype-complextype.md)               | 此區段會定義其他資訊清單可以使用的元資料類型。 如需範例，請參閱 Windows SDK 的 Include 資料夾中包含的 Winmeta.xml 檔案 \\ 。<br/>                                                                                                                                    |



## <a name="remarks"></a>備註

**InstrumentationManifest** 元素必須包含下列命名空間：

<dl> xmlns = " https://schemas.microsoft.com/win/2004/08/events "  
xmlns： win = " https://manifests.microsoft.com/win/2004/08/windows/events "  
xmlns： xs = " https://www.w3.org/2001/XMLSchema "  
</dl>

資訊清單必須包含檢測區段和當地語系化區段。 檢測區段和中繼資料區段互斥 (您無法在相同的資訊清單) 中定義。 雖然您可以建立包含中繼資料區段的資訊清單，但服務將不會使用它。服務唯一可辨識的中繼資料是 Winmeta.xml 檔案中找到的中繼資料。

## <a name="examples"></a>範例

下列範例顯示完整定義之檢測資訊清單的基本架構。


```XML
<instrumentationManifest
    xmlns="http://schemas.microsoft.com/win/2004/08/events" 
    xmlns:win="https://manifests.microsoft.com/win/2004/08/windows/events"
    xmlns:xs="https://www.w3.org/2001/XMLSchema"    
    >

    <instrumentation>
        <events>
            <provider ...>
                <channels>
                    <importChanel .../>
                    <channel .../>
                </channels>
                <levels>
                <level .../>
                </levels>
                <tasks>
                    <task .../>
                </tasks>
                <opcodes>
                    <opcode .../>
                </opcodes>
                <keywords>
                    <keyword .../>
                </keywords>
                <filters>
                    <filter .../>
                </filters>
                <maps>
                    <valueMap ...>
                        <map .../>
                    </valueMap>
                    <bitMap ...>
                        <map .../>
                    </bitMap>
                </maps>
                <namedQueries>
                    <patternMap ...>
                        <map .../>
                    </patternMap>  
                </namedQueries>
                <templates>
                    <template ...>
                        <data .../>
                        <UserData>
                            <!-- valid XML fragment -->
                        </UserData>
                    </template>
                </templates>
                <events>
                    <event .../>
                </events>
            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources ...>
            <stringTable>
                <string .../>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



 

 






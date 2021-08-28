---
description: 包含無線區域網路原則。
ms.assetid: 16ffb682-f88b-4ca1-a902-d2db5e347975
title: WLANPolicy 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WLANPolicy
api_type:
- Schema
api_location: ''
ms.openlocfilehash: e9e56e25e51a3c6e798242b390f5d8b7341d7306455f1b15eb9e450830d3c9b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119064698"
---
# <a name="wlanpolicy-element"></a>WLANPolicy 元素

**WLANPolicy** 元素包含無線區域網路原則。 此元素是無線原則設定檔的唯一根項目。

**WLANPolicy** 元素的目標命名空間為 `https://www.microsoft.com/networking/WLAN/policy/v1` 。

``` syntax
<xs:element name="WLANPolicy">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="name"
                type="nameType"
             />
            <xs:element name="description"
                type="nameType"
                minOccurs="0"
             />
            <xs:element name="globalFlags">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="enableAutoConfig"
                            type="boolean"
                         />
                        <xs:element name="showDeniedNetwork"
                            type="boolean"
                         />
                        <xs:element name="allowEveryoneToCreateAllUserProfiles"
                            type="boolean"
                         />
                        <xs:any
                            processContents="lax"
                            minOccurs="0"
                            maxOccurs="unbounded"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:element name="networkFilter"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="allowList"
                            minOccurs="0"
                        >
                            <xs:complexType>
                                <xs:sequence>
                                    <xs:element name="network"
                                        type="networkItemType"
                                        maxOccurs="unbounded"
                                     />
                                    <xs:any
                                        processContents="lax"
                                        minOccurs="0"
                                        maxOccurs="unbounded"
                                        namespace="##other"
                                     />
                                </xs:sequence>
                            </xs:complexType>
                        </xs:element>
                        <xs:element name="blockList"
                            minOccurs="0"
                        >
                            <xs:complexType>
                                <xs:sequence>
                                    <xs:element name="network"
                                        type="networkItemType"
                                        maxOccurs="unbounded"
                                     />
                                    <xs:any
                                        processContents="lax"
                                        minOccurs="0"
                                        maxOccurs="unbounded"
                                        namespace="##other"
                                     />
                                </xs:sequence>
                            </xs:complexType>
                        </xs:element>
                        <xs:element name="denyAllIBSS"
                            type="boolean"
                            minOccurs="0"
                         />
                        <xs:element name="denyAllESS"
                            type="boolean"
                            minOccurs="0"
                         />
                        <xs:any
                            processContents="lax"
                            minOccurs="0"
                            maxOccurs="unbounded"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:element name="profileList"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:any
                            processContents="lax"
                            maxOccurs="unbounded"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a>子元素



| 元素                                                                                                                    | 類型                                                                     | Description                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [**allowEveryoneToCreateAllUserProfiles**](wlan-policyschema-alloweveryonetocreatealluserprofiles-globalflags-element.md) | boolean                                                                  | 指定任何使用者是否可以建立所有使用者設定檔。 <br/>                                                               |
| [**允許清單**](wlan-policyschema-allowlist-networkfilter-element.md)                                                     |                                                                          | 必須允許任何電腦連接的無線區域網路網路清單。 <br/>                                       |
| [**封鎖清單**](wlan-policyschema-blocklist-networkfilter-element.md)                                                     |                                                                          | 電腦不能連線的無線區域網路網路清單。<br/>                                                    |
| [**denyAllESS**](wlan-policyschema-denyalless-networkfilter-element.md)                                                   | boolean                                                                  | 指定是否封鎖對所有基礎結構網路的存取。 <br/>                                                           |
| [**denyAllIBSS**](wlan-policyschema-denyallibss-networkfilter-element.md)                                                 | boolean                                                                  | 指定是否封鎖對所有特定網路的存取。 <br/>                                                                   |
| [**description**](wlan-policyschema-description-wlanpolicy-element.md)                                                    | [**nameType**](wlan-policyschema-nametype-simpletype.md)                | 無線區域網路原則的描述。 <br/>                                                                                |
| [**enableAutoConfig**](wlan-policyschema-enableautoconfig-globalflags-element.md)                                         | boolean                                                                  | 指定電腦是否使用內建的自動設定 (自動設定) 服務來管理無線連線。 <br/> |
| [**globalFlags**](wlan-policyschema-globalflags-wlanpolicy-element.md)                                                    |                                                                          | 包含自動設定模組的全域設定 (配置) 。 <br/>                                                    |
| [**名字**](wlan-policyschema-name-wlanpolicy-element.md)                                                                  | [**nameType**](wlan-policyschema-nametype-simpletype.md)                | 無線區域網路原則的名稱。 <br/>                                                                                       |
| [**網路**](wlan-policyschema-network-allowlist-element.md)                                                             | [**networkItemType**](wlan-policyschema-networkitemtype-complextype.md) | 允許的網路。 <br/>                                                                                                      |
| [**網路**](wlan-policyschema-network-blocklist-element.md)                                                             | [**networkItemType**](wlan-policyschema-networkitemtype-complextype.md) | 封鎖的網路。 <br/>                                                                                                       |
| [**networkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md)                                                |                                                                          | 允許和拒絕的網路清單。<br/>                                                                                  |
| [**profileList**](wlan-policyschema-profilelist-wlanpolicy-element.md)                                                    |                                                                          | 包含要在網域或電腦層級套用的配置檔案清單。 <br/>                                                |
| [**showDeniedNetwork**](wlan-policyschema-showdeniednetwork-globalflags-element.md)                                       | boolean                                                                  | 指定在網路 wizard 的 **連線** 中是否會出現拒絕的網路。 <br/>                                         |



## <a name="remarks"></a>備註

若要查看類似樹狀結構中子專案的清單，請參閱 [WLAN \_ 原則架構元素](wlan-policyschema-elements.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



 

 





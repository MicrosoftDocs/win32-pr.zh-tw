---
description: 指定有線或無線局域網路設定檔的 802.1 X 設定資訊。
ms.assetid: 4528fcb5-ee8e-4824-a69e-8d67622c4b4d
title: OneX 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OneX
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 4b3e3d91087a394efb7909d36d6244bfbf6115e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106998497"
---
# <a name="onex-element"></a>OneX 元素

OneX 元素會指定有線或無線局域網路設定檔的 802.1 X 設定資訊。 這個元素是 802.1 X 設定檔的唯一根項目。

OneX 元素的目標命名空間為 `https://www.microsoft.com/networking/OneX/v1` 。 所有的 OneX 元素子項目都在 `OneX` 命名空間中。 有一個例外狀況： [**EAPConfig**](onexschema-eapconfig-onex-element.md) 元素位於 `https://www.microsoft.com/provisioning/EapHostConfig` 命名空間中。

Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 只支援 [**EAPConfig**](onexschema-eapconfig-onex-element.md)元素。 如果設定檔中有其他專案，則會忽略這些元素。

``` syntax
<xs:element name="OneX">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="cacheUserData"
                type="boolean"
                minOccurs="0"
             />
            <xs:element name="heldPeriod"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="integer"
                    >
                        <xs:enumeration
                            value="1"
                         />
                        <xs:enumeration
                            value="3600"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="authPeriod"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="integer"
                    >
                        <xs:enumeration
                            value="1"
                         />
                        <xs:enumeration
                            value="3600"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="startPeriod"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="integer"
                    >
                        <xs:enumeration
                            value="1"
                         />
                        <xs:enumeration
                            value="3600"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="maxStart"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="integer"
                    >
                        <xs:enumeration
                            value="1"
                         />
                        <xs:enumeration
                            value="100"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="maxAuthFailures"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="integer"
                    >
                        <xs:enumeration
                            value="1"
                         />
                        <xs:enumeration
                            value="100"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="supplicantMode"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="inhibitTransmission"
                         />
                        <xs:enumeration
                            value="includeLearning"
                         />
                        <xs:enumeration
                            value="compliant"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="authMode"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="machineOrUser"
                         />
                        <xs:enumeration
                            value="machine"
                         />
                        <xs:enumeration
                            value="user"
                         />
                        <xs:enumeration
                            value="guest"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="singleSignOn"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="type"
                            minOccurs="1"
                        >
                            <xs:simpleType>
                                <xs:restriction
                                    base="string"
                                >
                                    <xs:enumeration
                                        value="preLogon"
                                     />
                                    <xs:enumeration
                                        value="postLogon"
                                     />
                                </xs:restriction>
                            </xs:simpleType>
                        </xs:element>
                        <xs:element name="maxDelay"
                            minOccurs="0"
                        >
                            <xs:simpleType>
                                <xs:restriction
                                    base="integer"
                                >
                                    <xs:enumeration
                                        value="0"
                                     />
                                    <xs:enumeration
                                        value="120"
                                     />
                                </xs:restriction>
                            </xs:simpleType>
                        </xs:element>
                        <xs:element name="userBasedVirtualLan"
                            type="boolean"
                            minOccurs="0"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:element name="EAPConfig">
                <xs:complexType>
                    <xs:sequence>
                        <xs:any
                            processContents="lax"
                            minOccurs="1"
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



| 元素                                                                            | 類型    | Description                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**authMode**](onexschema-authmode-onex-element.md)                               |         | 指定用於驗證的認證類型。<br/>                                                                                                                                                        |
| [**authPeriod**](onexschema-authperiod-onex-element.md)                           |         | 指定用戶端等候驗證器回應的最大時間長度（以秒為單位）。<br/>                                                                                                  |
| [**cacheUserData**](onexschema-cacheuserdata-onex-element.md)                     | boolean | 指定是否快取使用者認證以進行後續連接。<br/>                                                                                                                                     |
| [**EAPConfig**](onexschema-eapconfig-onex-element.md)                             |         | 指定 EAPHost 設定。<br/>                                                                                                                                                                              |
| [**heldPeriod**](onexschema-heldperiod-onex-element.md)                           |         | 指定在驗證嘗試失敗之後，用戶端不會重新嘗試驗證的時間長度（以秒為單位）。<br/>                                                                             |
| [**maxAuthFailures**](onexschema-maxauthfailures-onex-element.md)                 |         | 指定一組認證允許的驗證失敗次數上限。<br/>                                                                                                                         |
| [**maxDelay**](onexschema-maxdelay-singlesignon-element.md)                       |         | 指定單一登入連線嘗試失敗之前的延遲上限（以秒為單位）。<br/>                                                                                                                      |
| [**maxStart**](onexschema-maxstart-onex-element.md)                               |         | 指定傳送 EAPOL-Start 訊息的數目上限。<br/>                                                                                                                                                        |
| [**singleSignOn**](onexschema-singlesignon-onex-element.md)                       |         | 指定單一登入網路設定資訊。<br/>                                                                                                                                                       |
| [**startPeriod**](onexschema-startperiod-onex-element.md)                         |         | 指定傳送 EAPOL-Start 之前等候的時間長度（以秒為單位）。<br/>                                                                                                                                  |
| [**supplicantMode**](onexschema-supplicantmode-onex-element.md)                   |         | 指定用於 EAPOL 封包的傳輸方法。<br/>                                                                                                                                                      |
| [**類型**](onexschema-type-singlesignon-element.md)                               |         | 指定何時執行單一登入。 當設定為時 `preLogon` ，會在使用者登入之前執行單一登入。 當設定為時 `postLogon` ，會在使用者登入後立即執行單一登入。<br/> |
| [**userBasedVirtualLan**](onexschema-userbasedvirtuallan-singlesignon-element.md) | boolean | 指定裝置所使用的虛擬 LAN (VLAN) 是否會根據使用者的認證而變更。<br/>                                                                                                                   |



## <a name="remarks"></a>備註

若要查看類似樹狀結構中子專案的清單，請參閱 [OneX 架構元素](onexschema-elements.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista、Windows XP （僅含 SP3） \[ 桌面應用程式\]<br/> |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                |
| 可轉散發套件<br/>          | 適用于 Windows XP SP2 的無線區域網路 API<br/>                 |



 

 





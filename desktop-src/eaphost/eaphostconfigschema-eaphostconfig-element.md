---
title: EapHostConfig 元素
description: 包含 EapMethod 元素和 Config 或 ConfigBlob 元素。 無法同時使用 Config 和 ConfigBlob 元素。
ms.assetid: 6c42d71e-0c61-48e4-a447-cfd1eae90297
keywords:
- EapHostConfig 元素 EAPHost
topic_type:
- apiref
api_name:
- EapHostConfig
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 125b5fa2cab8bf3f9da12bd842a1a102beee3fb0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024518"
---
# <a name="eaphostconfig-element"></a>EapHostConfig 元素

**EapHostConfig** 元素包含 [**EapMethod**](eaphostconfigschema-eapmethod-eaphostconfig-element.md)元素和 [**Config**](eaphostconfigschema-config-eaphostconfig-element.md)或 [**ConfigBlob**](eaphostconfigschema-configblob-eaphostconfig-element.md)元素。

無法同時使用 [**Config**](eaphostconfigschema-config-eaphostconfig-element.md) 和 [**ConfigBlob**](eaphostconfigschema-configblob-eaphostconfig-element.md) 元素。

``` syntax
<xs:element name="EapHostConfig">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="EapMethod"
                type="EapMethodType"
             />
            <xs:choice>
                <xs:element name="Config"
                    type="BaseEapMethodConfig"
                 />
                <xs:element name="ConfigBlob"
                    type="hexBinary"
                 />
            </xs:choice>
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



| 元素                                                                    | 類型                                                                                     | Description                                                                                          |
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**配置**](eaphostconfigschema-config-eaphostconfig-element.md)         | [**BaseEapMethodConfig**](baseeapmethodconfigschema-baseeapmethodconfig-complextype.md) | 當方法設定為 XML 文字格式，而非二進位 BLOB 時，會使用。<br/>       |
| [**ConfigBlob**](eaphostconfigschema-configblob-eaphostconfig-element.md) | hexBinary                                                                                | 當方法設定為二進位 BLOB 格式，而不是字串文字格式時，就會使用。<br/> |
| [**EapMethod**](eaphostconfigschema-eapmethod-eaphostconfig-element.md)   | [**EapMethodType**](eapcommonschema-eapmethodtype-complextype.md)                       | 識別所參考的方法。 <br/>                                                 |



## <a name="remarks"></a>備註

**ProcessContents** 元素可讓架構的未來增強功能。 **ProcessContents** 元素是選擇性的。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[EAPHost 和舊版架構](eaphost-schemas.md)
</dt> <dt>

[eaphostconfig 架構](eaphostconfigschema-schema.md)
</dt> </dl>

 

 






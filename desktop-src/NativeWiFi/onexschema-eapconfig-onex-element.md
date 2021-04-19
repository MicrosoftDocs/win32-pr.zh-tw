---
description: 指定 EAPHost 設定。
ms.assetid: 71ec3ed6-3670-46fc-a24b-580d15297437
title: EAPConfig (OneX) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EAPConfig
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 955b3647aca787097495b6051407b718dfa91f53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979132"
---
# <a name="eapconfig-onex-element"></a>EAPConfig (OneX) 元素

**EAPConfig** (OneX) 元素會指定 EAPHost 設定。

不同于 802.1 X 設定檔架構中的大部分元素，此專案位於 `https://www.microsoft.com/provisioning/EapHostConfig` 命名空間中。 其子項目是在 [eaphostconfig 架構](../eaphost/eaphostconfigschema-schema.md)中定義。 [**EapHostConfig**](../eaphost/eaphostconfigschema-eaphostconfig-element.md)元素是 **EAPConfig** 元素的子系。

``` syntax
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
```

**EAPConfig** 元素是由 [**OneX**](onexschema-onex-element.md)元素所定義。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista、Windows XP （僅含 SP3） \[ 桌面應用程式\]<br/> |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                |
| 可轉散發套件<br/>          | 適用于 Windows XP SP2 的無線區域網路 API<br/>                 |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**架構中的元素定義內容**
</dt> <dt>

[**OneX**](onexschema-onex-element.md)
</dt> <dt>

**架構實例中可能的直屬父元素**
</dt> <dt>

[**OneX**](onexschema-onex-element.md)
</dt> </dl>

 

 

---
description: 包含自動設定模組的全域設定 (配置) 。
ms.assetid: fb2b96d0-38cc-44fe-a82a-97e73b6a8f2a
title: globalFlags (WLANPolicy) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- globalFlags
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 2851ae779bf1693d44642f87d33a71c17000e9dc0b68eeb8daab83972b37457d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119800328"
---
# <a name="globalflags-wlanpolicy-element"></a>globalFlags (WLANPolicy) 元素

GlobalFlags (WLANPolicy) 元素包含自動設定模組的全域設定 (的 [配置]) 。 此為必要元素。

``` syntax
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
```

**GlobalFlags** 元素是由 [**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md)元素定義。

## <a name="child-elements"></a>子元素



| 元素                                                                                                                    | 類型    | 描述                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------|---------|--------------------------------------------------------------------------------------------------------------------------------------|
| [**allowEveryoneToCreateAllUserProfiles**](wlan-policyschema-alloweveryonetocreatealluserprofiles-globalflags-element.md) | boolean | 指定任何使用者是否可以建立所有使用者設定檔。 <br/>                                                               |
| [**enableAutoConfig**](wlan-policyschema-enableautoconfig-globalflags-element.md)                                         | boolean | 指定電腦是否使用內建的自動設定 (自動設定) 服務來管理無線連線。 <br/> |
| [**showDeniedNetwork**](wlan-policyschema-showdeniednetwork-globalflags-element.md)                                       | boolean | 指定在網路 wizard 的 **連線** 中是否會出現拒絕的網路。 <br/>                                         |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**架構中的元素定義內容**
</dt> <dt>

[**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md)
</dt> <dt>

**架構實例中可能的直屬父元素**
</dt> <dt>

[**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md)
</dt> </dl>

 

 





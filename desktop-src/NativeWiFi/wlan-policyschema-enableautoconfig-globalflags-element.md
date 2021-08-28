---
description: 指定電腦是否使用內建的自動設定 (自動設定) 服務來管理無線連線。
ms.assetid: c255e0a0-65ae-44a8-95cb-1a000394109d
title: '適用于 WLAN 的 enableAutoConfig (globalFlags) 元素 (LAN_policy) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- enableAutoConfig
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 77b09bf046cdbadb58c888a3084d14ed14794064bf9f11c110ccecaff105fceb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684408"
---
# <a name="enableautoconfig-globalflags-element-lan_policy-for-wlan"></a>適用于 WLAN 的 enableAutoConfig (globalFlags) 元素 (LAN_policy)  

**EnableAutoConfig** (globalFlags) 元素會指定電腦是否使用內建的自動設定 (自動設定) 服務來管理無線連線。 當 **enableAutoConfig** 的值為 FALSE 時，電腦不能使用自動設定來管理無線連線，而且自動設定服務只會回應啟用服務的要求。 當 **enableAutoConfig** 的值為 TRUE 時，電腦可能會使用自動設定服務。

此為必要元素。 當設定檔由自動設定服務建立時，此元素的預設值會是 TRUE。

``` syntax
<xs:element name="enableAutoConfig"
    type="boolean"
 />
```

**EnableAutoConfig** 元素是由 [**globalFlags**](wlan-policyschema-globalflags-wlanpolicy-element.md)元素定義。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**架構中的元素定義內容**
</dt> <dt>

[**globalFlags**](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> <dt>

**架構實例中可能的直屬父元素**
</dt> <dt>

[**globalFlags (WLANPolicy)**](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> </dl>

 

 





---
description: 指定電腦是否使用內建的自動設定服務來管理需要第2層驗證 (（例如 802.1 X) ）之有線網路的連接。
ms.assetid: c7a0f6bc-4d42-4d95-8483-2c480f4d8db9
title: 'enableAutoConfig (globalFlags) 元素 (LAN_policy) '
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
ms.openlocfilehash: 2842da69b07136df80d15ea84553aecdf2c62d417c73f7ec85d9c315b819a397
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119780198"
---
# <a name="enableautoconfig-globalflags-element-lan_policy"></a>enableAutoConfig (globalFlags) 元素 (LAN_policy) 

**EnableAutoConfig** (globalFlags) 元素會指定電腦是否使用內建的自動設定服務來管理需要第2層 (驗證的有線網路連線，例如 802.1 x) 。

當 **enableAutoConfig** 的值為 FALSE 時，電腦不能使用內建的自動設定服務來管理需要第2層驗證的連接。 相反地， [**profileList**](lan-policyschema-profilelist-lanpolicy-element.md) 元素中指定的網路是唯一可供連接的網路。 自動設定服務只會回應啟用服務的要求。

當 **enableAutoConfig** 的值為 TRUE 時，電腦可能會使用內建的自動設定服務來連線到需要第2層驗證的有線網路。

``` syntax
<xs:element name="enableAutoConfig"
    type="boolean"
 />
```

**EnableAutoConfig** 元素是由 [**globalFlags**](lan-policyschema-globalflags-lanpolicy-element.md)元素定義。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**架構中的元素定義內容**
</dt> <dt>

[**globalFlags**](lan-policyschema-globalflags-lanpolicy-element.md)
</dt> <dt>

**架構實例中可能的直屬父元素**
</dt> <dt>

[**globalFlags (LANPolicy)**](lan-policyschema-globalflags-lanpolicy-element.md)
</dt> </dl>

 

 





---
description: 指定已拒絕的網路是否出現在 [連接到網路] 嚮導中。
ms.assetid: d0a13a80-2532-4383-8946-2536cc1f5e12
title: showDeniedNetwork (globalFlags) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- showDeniedNetwork
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 33049dad00e5fda22e3f739d3dc200a282481a8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512528"
---
# <a name="showdeniednetwork-globalflags-element"></a>showDeniedNetwork (globalFlags) 元素

**ShowDeniedNetwork** (globalFlags) 元素會指定已拒絕的網路是否出現在 [**連接到網路**] 嚮導中。 群組原則或使用者設定可能會拒絕網路。 當 **showDeniedNetwork** 的值為 TRUE 時，拒絕的網路會出現在 [ **連接到網路** ] 嚮導中;否則，已拒絕的網路不會出現在嚮導中。

此為必要元素。 當設定檔是由自動設定服務建立時，此元素將採用預設值 FALSE。

``` syntax
<xs:element name="showDeniedNetwork"
    type="boolean"
 />
```

**ShowDeniedNetwork** 元素是由 [**globalFlags**](wlan-policyschema-globalflags-wlanpolicy-element.md)元素定義。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



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

 

 





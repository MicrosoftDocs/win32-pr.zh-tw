---
description: 指定行動寬頻裝置是否會自動連接到網路。
ms.assetid: a2673ac7-6d70-4005-9ac4-cf670eba26ae
title: AutoConnectOnInternet (MBNProfile) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AutoConnectOnInternet
api_type:
- Schema
ms.openlocfilehash: fd08e93572d7d0af8b490ac079e3057413c469ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191443"
---
# <a name="autoconnectoninternet-mbnprofile-element"></a>AutoConnectOnInternet (MBNProfile) 元素

**AutoConnectOnInternet (MBNProfile)** 元素會指定行動寬頻裝置是否會自動連接到網路。

如果設定為 **FALSE**，則如果系統有其他可用的網路連線，就不會使用行動寬頻服務的自動連接邏輯。 如果設定為 **TRUE**，行動寬頻服務會根據 [**ConnectionMode**](schema-connectionmode-mbnprofile-element.md) 元素中定義的自動連線設定，嘗試自動將裝置連線到網路。

**Windows 8 和更新版本：** 此元素已被取代。 請改用 [**WcmSetProperty**](/windows/desktop/api/wcmapi/nf-wcmapi-wcmsetproperty) 方法，將 *property* 參數設定為 [ **wcm \_ global Property 的 \_ \_ 最小化 \_ 原則** ]。

``` syntax
<xs:element name="AutoConnectOnInternet"
    type="boolean"
 />
```

**AutoConnectOnInternet** 元素是由 [**MBNProfile**](schema-mbnprofile-element.md)元素定義。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]<br/> |
| 最低支援的伺服器<br/> | 都不支援<br/>                         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**架構中的元素定義內容**
</dt> <dt>

[**MBNProfile**](schema-mbnprofile-element.md)
</dt> <dt>

**架構實例中可能的直屬父元素**
</dt> <dt>

[**MBNProfile**](schema-mbnprofile-element.md)
</dt> </dl>

 


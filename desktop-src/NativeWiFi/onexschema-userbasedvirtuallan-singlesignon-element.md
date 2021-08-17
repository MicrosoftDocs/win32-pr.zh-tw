---
description: 指定裝置所使用的虛擬 LAN (VLAN) 是否會根據使用者的認證而變更。
ms.assetid: 4ac92954-adb2-4b0c-9c4e-81f772ea03ed
title: userBasedVirtualLan (singleSignOn) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- userBasedVirtualLan
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 9272f61e7efeaf90ba68b1577af9b0062e507984372f7f09ebdbfc15e4ac6fbb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119064968"
---
# <a name="userbasedvirtuallan-singlesignon-element"></a>userBasedVirtualLan (singleSignOn) 元素

UserBasedVirtualLan (singleSignOn) 元素會指定裝置所使用的虛擬 LAN (VLAN) 是否會根據使用者的認證而變更。 有些網路存取伺服器 (NAS) 裝置會在使用者驗證之後變更 VLAN。 當 userBasedVirtualLan 為 TRUE 時，NAS 可能會在使用者驗證之後變更裝置的 VLAN。

這是選擇性的項目。 當設定檔中未指定 userBasedVirtualLan 時，會使用 FALSE 值。

**Windows xp 搭配 SP3 和適用于 Windows XP SP2 的無線區域網路 API：** 如果設定檔中有此元素，將會予以忽略。

``` syntax
<xs:element name="userBasedVirtualLan"
    type="boolean"
    minOccurs="0"
 />
```

**UserBasedVirtualLan** 元素是由 [**singleSignOn**](onexschema-singlesignon-onex-element.md)元素定義。

## <a name="remarks"></a>備註

您可以使用 **netsh wlan set profileparameter** 命令，在命令列設定這個參數。 如需詳細資訊，請參閱 [無線區域網路 (wlan) 的 Netsh 命令 ](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10))。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**架構中的元素定義內容**
</dt> <dt>

[**singleSignOn**](onexschema-singlesignon-onex-element.md)
</dt> <dt>

**架構實例中可能的直屬父元素**
</dt> <dt>

[**singleSignOn (OneX)**](onexschema-singlesignon-onex-element.md)
</dt> </dl>

 

 

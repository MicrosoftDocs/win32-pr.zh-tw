---
description: 指出是否使用 802.1 X 驗證。
ms.assetid: dbddaf5a-7574-4282-ab4d-f6f697ed94ab
title: useOneX (authEncryption) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- useOneX
api_type:
- Schema
api_location: ''
ms.openlocfilehash: cb327be4006e8da0074815a74e49d3ccdc5d3c84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106969418"
---
# <a name="useonex-authencryption-element"></a>useOneX (authEncryption) 元素

UseOneX (authEncryption) 元素指出是否使用 802.1 X 驗證。

``` syntax
<xs:element name="useOneX"
    type="boolean"
    minOccurs="0"
 />
```

元素是由 [**authEncryption**](wlan-profileschema-authencryption-security-element.md) 元素所定義。

## <a name="examples"></a>範例

若要查看使用 **useOneX** 元素的範例設定檔，請參閱 [無線設定檔範例](wireless-profile-samples.md)。

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

[**authEncryption**](wlan-profileschema-authencryption-security-element.md)
</dt> <dt>

**架構實例中可能的直屬父元素**
</dt> <dt>

[**authEncryption (安全性)**](wlan-profileschema-authencryption-security-element.md)
</dt> </dl>

 

 





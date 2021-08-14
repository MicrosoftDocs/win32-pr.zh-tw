---
description: 指定有線網路的自動設定服務是否需要使用 802.1 X 進行埠驗證。
ms.assetid: fb01be74-46ad-4d8c-be4c-50ae05a0c33b
title: OneXEnforced (安全性) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OneXEnforced
api_type:
- Schema
api_location: ''
ms.openlocfilehash: bcaa8604fb8b813417299725133e9c6e51f7d7510b540cf8495ff9009b9d1c46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117798438"
---
# <a name="onexenforced-security-element"></a>OneXEnforced (安全性) 元素

**OneXEnforced** (security) 元素會指定有線網路的自動設定服務是否需要使用 802.1 x 進行埠驗證。 當 **OneXEnforced** 為 TRUE 時，自動設定服務必須使用 802.1 x 進行埠驗證。 當 **OneXEnforced** 為 FALSE 時，自動設定服務會嘗試使用 802.1 x 進行埠驗證，但如果 802.1 x 驗證因任何原因而失敗，則此服務會回復為無驗證。

這是選擇性的項目。 預設值為 FALSE。

如果 [**OneXEnabled**](lan-profileschema-onexenabled-security-element.md) 為 TRUE，則這個元素只有一個有意義的值。 如果 **OneXEnabled** 為 FALSE，則會忽略此元素的值。

``` syntax
<xs:element name="OneXEnforced"
    type="boolean"
 />
```

**OneXEnforced** 元素是由 [**安全性**](lan-profileschema-security-msm-element.md)元素所定義。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**架構中的元素定義內容**
</dt> <dt>

[**安全**](lan-profileschema-security-msm-element.md)
</dt> <dt>

**架構實例中可能的直屬父元素**
</dt> <dt>

[**(MSM) 的安全性**](lan-profileschema-security-msm-element.md)
</dt> </dl>

 

 





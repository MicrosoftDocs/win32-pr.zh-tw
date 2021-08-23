---
description: 指定有線網路的自動設定服務是否會嘗試使用 802.1 X 進行埠驗證。
ms.assetid: ab6cfc59-9cfd-45d3-ad27-306ad4f6d4e1
title: OneXEnabled (安全性) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OneXEnabled
api_type:
- Schema
api_location: ''
ms.openlocfilehash: aaaf5344078e4c8da2e5ee2118eed84563ebeb4daa8aebd700a29630b2fe4301
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119801088"
---
# <a name="onexenabled-security-element"></a>OneXEnabled (安全性) 元素

**OneXEnabled** (security) 元素會指定有線網路的自動設定服務是否會嘗試使用 802.1 x 進行埠驗證。 當 **OneXEnabled** 為 FALSE 時，自動設定服務永遠不會使用 802.1 x 進行埠驗證。 當 **OneXEnabled** 為 TRUE 時，自動設定服務會使用 802.1 x 嘗試埠驗證。

這是選擇性的項目。 預設值為 TRUE。 當設定檔中未指定 **OneXEnabled** 時，802.1 x 可能會用於埠驗證。

``` syntax
<xs:element name="OneXEnabled"
    type="boolean"
 />
```

**OneXEnabled** 元素是由 [**安全性**](lan-profileschema-security-msm-element.md)元素所定義。

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

 

 





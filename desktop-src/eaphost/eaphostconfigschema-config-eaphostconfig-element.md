---
title: Config (EapHostConfig) 元素
description: 當方法設定為 XML 文字格式，而非二進位 BLOB 時，會使用。
ms.assetid: f47bec23-745f-47db-84db-2556beb6a9e9
keywords:
- Config 元素 EAPHost
topic_type:
- apiref
api_name:
- Config
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a81c90063a57a9d55d8ab6d9c18486315c187f0e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465609"
---
# <a name="config-eaphostconfig-element"></a>Config (EapHostConfig) 元素

當方法設定為 XML 文字格式，而非二進位 BLOB 時，會使用 **Config (EapHostConfig)** 元素。

``` syntax
<xs:element name="Config"
    type="BaseEapMethodConfig"
 />
```

**Config** 元素是由 [**EapHostConfig**](eaphostconfigschema-eaphostconfig-element.md)元素定義。

## <a name="remarks"></a>備註

無法同時使用 **Config** 和 [**ConfigBlob**](eaphostconfigschema-configblob-eaphostconfig-element.md) 元素。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**架構中的元素定義內容**
</dt> <dt>

[**EapHostConfig**](eaphostconfigschema-eaphostconfig-element.md)
</dt> <dt>

**架構實例中可能的直屬父元素**
</dt> <dt>

[**EapHostConfig**](eaphostconfigschema-eaphostconfig-element.md)
</dt> <dt>

[EAPHost 和舊版架構](eaphost-schemas.md)
</dt> <dt>

[eaphostconfig 架構](eaphostconfigschema-schema.md)
</dt> </dl>

 

 






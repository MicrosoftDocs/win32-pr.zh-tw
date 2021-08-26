---
title: ConfigBlob (EapHostConfig) 元素
description: 當方法設定為二進位 BLOB 格式，而不是文字字串格式時，就會使用。
ms.assetid: 2820e0b8-2cd1-40e8-ac0c-a62e73ac3847
keywords:
- ConfigBlob 元素 EAPHost
topic_type:
- apiref
api_name:
- ConfigBlob
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8f0d3b928ebc6cd24a6d7102ea37a8d0ae980c54499f568d25ca224b1121a20b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021638"
---
# <a name="configblob-eaphostconfig-element"></a>ConfigBlob (EapHostConfig) 元素

當方法設定為二進位 BLOB 格式，而不是文字字串格式時，就會使用 **ConfigBlob (EapHostConfig)** 元素。

``` syntax
<xs:element name="ConfigBlob"
    type="hexBinary"
 />
```

**ConfigBlob** 元素是由 [**EapHostConfig**](eaphostconfigschema-eaphostconfig-element.md)元素定義。

## <a name="remarks"></a>備註

無法同時使用 [**Config**](eaphostconfigschema-config-eaphostconfig-element.md) 和 **ConfigBlob** 元素。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



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

 

 






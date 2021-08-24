---
description: 指定是否快取使用者認證以進行後續連接。
ms.assetid: 65ed03f1-f61e-46f8-a666-91b393618de3
title: cacheUserData (OneX) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- cacheUserData
api_type:
- Schema
api_location: ''
ms.openlocfilehash: d7f4663153fa9aff176180387ebaf0321ab3d48ec2c382e9e84c0f524d6e0ee1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119800868"
---
# <a name="cacheuserdata-onex-element"></a>cacheUserData (OneX) 元素

CacheUserData (OneX) 元素會指定是否要快取使用者認證以進行後續連接。 當 cacheUserData 為 TRUE 時，會快取認證。 當 cacheUserData 為 FALSE 時，將不會快取認證，而且使用者可能會在後續連接嘗試時提示您輸入認證。

這是選擇性的項目。 當設定檔中未指定 cacheUserData 時，會快取使用者認證。

**Windows xp 搭配 SP3 和適用于 Windows XP SP2 的無線區域網路 API：** 如果設定檔中有此元素，將會予以忽略。

``` syntax
<xs:element name="cacheUserData"
    type="boolean"
 />
```

**CacheUserData** 元素是由 [**OneX**](onexschema-onex-element.md)元素所定義。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**架構中的元素定義內容**
</dt> <dt>

[**OneX**](onexschema-onex-element.md)
</dt> <dt>

**架構實例中可能的直屬父元素**
</dt> <dt>

[**OneX**](onexschema-onex-element.md)
</dt> </dl>

 

 





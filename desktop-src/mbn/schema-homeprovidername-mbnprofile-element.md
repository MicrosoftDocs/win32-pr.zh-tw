---
description: 識別指定之 SIM/裝置的家用提供者名稱。
ms.assetid: 05d65091-5a1d-427a-8f51-1e1b9d189571
title: HomeProviderName (MBNProfile) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HomeProviderName
api_type:
- Schema
ms.openlocfilehash: 3d0af51e4873915838f2d55f683d07e9098aad3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690323"
---
# <a name="homeprovidername-mbnprofile-element"></a>HomeProviderName (MBNProfile) 元素

**HomeProviderName (MBNProfile)** 元素會識別給定 SIM/裝置的家用提供者名稱。

這個元素是選擇性的，且由行動寬頻服務設定供內部使用。 應用程式在建立或更新設定檔時，不應設定此欄位。

``` syntax
<xs:element name="HomeProviderName"
    type="providerNameType"
 />
```

**HomeProviderName** 元素是由 [**MBNProfile**](schema-mbnprofile-element.md)元素定義。

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

 

 





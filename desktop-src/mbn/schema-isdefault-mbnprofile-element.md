---
description: 指定這是否為裝置的預設設定檔。
ms.assetid: 024ef936-ddf4-41f6-81c9-5c8a632690a0
title: IsDefault (MBNProfile) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsDefault
api_type:
- Schema
ms.openlocfilehash: a59001e385fa7007d188daf2c1348d1a00c3a074
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104469000"
---
# <a name="isdefault-mbnprofile-element"></a>IsDefault (MBNProfile) 元素

**IsDefault (MBNProfile)** 元素會指定這是否為裝置的預設設定檔。

這是選擇性專案，如果未指定，則不會將設定檔設定為預設設定檔。

行動寬頻服務會使用預設設定檔進行下列用途

-   行動寬頻服務在執行自動網路連線時，會使用預設設定檔中的連線設定。 這些設定包括存取點名稱、使用者名稱、密碼等等。
-   行動寬頻裝置的自動連線原則是取自其預設設定檔。
-   作業系統網路連線 UI 也會使用連接作業的預設設定檔中的連接資料。

行動電話服務提供者可以在設定檔中提供連線詳細資料，並將該設定檔設定為預設設定檔。 行動寬頻服務將會使用這些連接設定，而不會提示使用者提供詳細資料。

``` syntax
<xs:element name="IsDefault"
    type="boolean"
 />
```

**IsDefault** 元素是由 [**MBNProfile**](schema-mbnprofile-element.md)元素定義。

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

 

 





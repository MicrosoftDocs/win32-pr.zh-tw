---
description: 定義型別，這個型別是用來針對日誌 XML 檔案中特定專案的色彩指定有效值。
ms.assetid: 10a19f28-d0aa-4126-b3f5-fde35fc5fdb0
title: ColorType 簡單類型
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ColorType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 883c34f42f8d31f3581599445b398b93676d416b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106966661"
---
# <a name="colortype-simple-type"></a>ColorType 簡單類型

定義型別，這個型別是用來針對日誌 XML 檔案中特定專案的色彩指定有效值。

``` syntax
<xs:simpleType name="ColorType">
    <xs:restriction
        base="string"
     />
</xs:simpleType>
```

## <a name="remarks"></a>備註

色彩可以是 RRGGBB 格式的十六進位 RGB 值 \# 。 它必須符合下列正則運算式： \# \[ 0-9A-FA-F \] {6} 。 例如： " \# 4a79B5"。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/> |
| 最低支援的伺服器<br/> | 都不支援<br/>                                     |



 

 





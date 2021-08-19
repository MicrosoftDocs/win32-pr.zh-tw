---
description: 表示 tablet 裝置的類型，例如畫筆、滑鼠或觸控式的數位化數位板。
ms.assetid: 4cca1e09-99c0-4357-a6ef-159bc8d17d57
title: TABLET_DEVICE_KIND 列舉
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TABLET_DEVICE_KIND
api_type:
- NA
api_location: ''
ms.openlocfilehash: 784e2393f5470f8abd966ca6dbdce3ac9d9bff734f1245ebd0ef169180c62d79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119820178"
---
# <a name="tablet_device_kind-enumeration"></a>平板電腦 \_ 裝置 \_ 種類列舉

表示 tablet 裝置的類型，例如畫筆、滑鼠或觸控式的數位化數位板。

## <a name="syntax"></a>Syntax


```C++
typedef enum _TABLET_DEVICE_KIND { 
  TABLET_DEVICE_MOUSE  = 0,
  TABLET_DEVICE_PEN,
  TABLET_DEVICE_TOUCH
} TABLET_DEVICE_KIND;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="TABLET_DEVICE_MOUSE"></span><span id="tablet_device_mouse"></span>**TABLET \_ 裝置 \_ 滑鼠**
</dt> <dd>

Tablet 是老鼠。 這包括在許多膝上型電腦上找到的 touchpads。

</dd> <dt>

<span id="TABLET_DEVICE_PEN"></span><span id="tablet_device_pen"></span>**TABLET \_ 裝置 \_ 畫筆**
</dt> <dd>

Tablet 會利用電磁輻射和數位板。

</dd> <dt>

<span id="TABLET_DEVICE_TOUCH"></span><span id="tablet_device_touch"></span>**TABLET \_ 裝置 \_ 觸控**
</dt> <dd>

Tablet 會利用觸控式的數位化數位板。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows僅限 XP Tablet PC Edition \[ 桌面應用程式\]<br/> |
| 最低支援的伺服器<br/> | 都不支援<br/>                                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITablet2：： GetDeviceKind 方法**](itablet2-getdevicekind.md)
</dt> </dl>

 

 





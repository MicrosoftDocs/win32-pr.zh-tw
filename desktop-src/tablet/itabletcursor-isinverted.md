---
description: 指出手寫筆是否已反轉。
ms.assetid: 04b05287-000d-455f-88e5-821c7fdb8119
title: ITabletCursor：： IsInverted 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursor.IsInverted
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 81bbb5f4f93026e0d6910cb7f23d0a7d2ddeea5595e87f816faa016d22986d0e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119223065"
---
# <a name="itabletcursorisinverted-method"></a>ITabletCursor：： IsInverted 方法

指出手寫筆是否已反轉。

## <a name="syntax"></a>語法


```C++
HRESULT IsInverted();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼                                                                             | 描述                               |
|-----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>    | 手寫筆已反轉。<br/>        |
| <dl> <dt>**S \_ FALSE**</dt> </dl> | 手寫筆未反轉。<br/>    |
| <dl> <dt>**E \_ 失敗**</dt> </dl>  | 發生未指定的錯誤。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows僅限 XP Tablet PC Edition \[ 桌面應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                              |
| 程式庫<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITabletCursor**](itabletcursor.md)
</dt> <dt>

[**ITabletCursorButton 介面**](itabletcursorbutton.md)
</dt> </dl>

 

 





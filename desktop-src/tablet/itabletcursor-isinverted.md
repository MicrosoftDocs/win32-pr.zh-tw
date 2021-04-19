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
ms.openlocfilehash: 041b81c38f3370421c96a4c0d66201254a715e62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983775"
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



| 傳回碼                                                                             | Description                               |
|-----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>    | 手寫筆已反轉。<br/>        |
| <dl> <dt>**S \_ FALSE**</dt> </dl> | 手寫筆未反轉。<br/>    |
| <dl> <dt>**E \_ 失敗**</dt> </dl>  | 發生未指定的錯誤。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                              |
| 程式庫<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITabletCursor**](itabletcursor.md)
</dt> <dt>

[**ITabletCursorButton 介面**](itabletcursorbutton.md)
</dt> </dl>

 

 





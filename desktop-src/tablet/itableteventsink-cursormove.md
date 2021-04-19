---
description: 發生于游標移至 tablet 數位化板上時。
ms.assetid: cd2863af-59a9-4dd0-a679-84861a70ef53
title: ITabletEventSink：： CursorMove 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.CursorMove
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: f6950e0b30c1b8fc8ccf3e60a8aaa05b9eeb3215
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107000325"
---
# <a name="itableteventsinkcursormove-method"></a>ITabletEventSink：： CursorMove 方法

發生于游標移至 tablet 數位化板上時。

## <a name="syntax"></a>語法


```C++
HRESULT CursorMove(
   TABLET_CONTEXT_ID tcid,
   CURSOR_ID         cid,
   HWND              hWnd,
   LONG              xPos,
   LONG              yPos
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*tcid* 
</dt> <dd>

Tablet 數位板的唯一 dentifier。

</dd> <dt>

*Cid* 
</dt> <dd>

Tablet 手寫筆的唯一識別碼。

</dd> <dt>

*hWnd* 
</dt> <dd>

移動資料指標的視窗。

</dd> <dt>

*xPos* 
</dt> <dd>

手寫筆的 X 位置。

</dd> <dt>

*yPos* 
</dt> <dd>

手寫筆的 Y 位置。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼                                                                            | Description                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>   | 成功。<br/>                       |
| <dl> <dt>**E \_ 失敗**</dt> </dl> | 發生未指定的錯誤。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                              |
| 程式庫<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITabletEventSink 介面**](itableteventsink.md)
</dt> </dl>

 

 





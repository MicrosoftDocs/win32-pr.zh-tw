---
description: 抓取 tablet 手寫筆上的按鈕數目。
ms.assetid: ae4ce670-769a-4f00-b728-285020f09934
title: ITabletCursor：： GetButtonCount 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursor.GetButtonCount
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 82a0825d64bc93601b933a98b3a7e0e3f321954d2fb2d7aa285d8d08a315545c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119336018"
---
# <a name="itabletcursorgetbuttoncount-method"></a>ITabletCursor：： GetButtonCount 方法

抓取 tablet 手寫筆上的按鈕數目。

## <a name="syntax"></a>語法


```C++
HRESULT GetButtonCount(
  [out] ULONG *pcButtons
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pcButtons* \[擴展\]
</dt> <dd>

Tablet 手寫筆上的按鈕計數。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼                                                                            | 描述                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>   | 成功。<br/>                       |
| <dl> <dt>**E \_ 失敗**</dt> </dl> | 發生未指定的錯誤。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows僅限 XP Tablet PC Edition \[ 桌面應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                              |
| 程式庫<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITabletCursor 介面**](itabletcursor.md)
</dt> </dl>

 

 





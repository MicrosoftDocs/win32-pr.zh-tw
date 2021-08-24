---
description: 從 tablet 手寫筆取出指定的按鈕物件。
ms.assetid: 83a26703-4501-4f43-9e86-c5c753347012
title: ITabletCursor：： GetButton 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursor.GetButton
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 49306160a0c14badc23cb2f359400d0fb2947012078a9318315a6697050f48dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119938628"
---
# <a name="itabletcursorgetbutton-method"></a>ITabletCursor：： GetButton 方法

從 tablet 手寫筆取出指定的按鈕物件。

## <a name="syntax"></a>語法


```C++
HRESULT GetButton(
  [in]  ULONG               iButton,
  [out] ITabletCursorButton **ppButton
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*iButton* \[在\]
</dt> <dd>

要取出之按鈕的識別碼。

</dd> <dt>

*ppButton* \[擴展\]
</dt> <dd>

*IButton* 參數所指定的按鈕物件。

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

 

 





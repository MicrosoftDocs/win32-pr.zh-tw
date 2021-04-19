---
description: 傳回與平板電腦相關聯的資料指標物件數目。
ms.assetid: 7aa5802c-1255-41a4-b1fa-23e5f56c0b80
title: ITablet：： GetCursorCount 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.GetCursorCount
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 2309384e4aa36383277ba72cc407cabef7ab4b27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975440"
---
# <a name="itabletgetcursorcount-method"></a>ITablet：： GetCursorCount 方法

傳回與平板電腦相關聯的資料指標物件數目。

## <a name="syntax"></a>語法


```C++
HRESULT GetCursorCount(
  [out] ULONG *pcCurs
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pcCurs* \[擴展\]
</dt> <dd>

與平板電腦相關聯的資料指標物件數目。

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

[**ITablet 介面**](itablet.md)
</dt> </dl>

 

 





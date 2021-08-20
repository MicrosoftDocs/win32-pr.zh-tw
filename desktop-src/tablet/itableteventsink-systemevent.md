---
description: 發生于可用的系統事件時。
ms.assetid: 3d9e98f0-b11e-4a65-a544-9e1998a80d5f
title: ITabletEventSink：： SystemEvent 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.SystemEvent
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 6d2e636b5e0b70d13ae33850518e744fbc9425bd65c20002a89b6d38e56dbc50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118041740"
---
# <a name="itableteventsinksystemevent-method"></a>ITabletEventSink：： SystemEvent 方法

發生于可用的系統事件時。

## <a name="syntax"></a>語法


```C++
HRESULT SystemEvent(
  [in] TABLET_CONTEXT_ID tcid,
  [in] CURSOR_ID         cid,
  [in] SYSTEM_EVENT      event,
  [in] SYSTEM_EVENT_DATA eventdata
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*tcid* \[在\]
</dt> <dd>

Tablet 的識別碼。

</dd> <dt>

 \[ 中的 cid\]
</dt> <dd>

手寫筆的識別碼。

</dd> <dt>

*活動* \[在\]
</dt> <dd>

系統事件代碼。

</dd> <dt>

*eventdata* \[在\]
</dt> <dd>

系統事件資料。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼                                                                            | 描述                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>   | 成功。<br/>                       |
| <dl> <dt>**E \_ 失敗**</dt> </dl> | 發生未指定的錯誤。<br/> |



 

## <a name="remarks"></a>備註

下列清單包含事件參數的有效值。

-   SE \_水龍頭
-   SE \_按兩下 \_
-   SE \_以滑鼠右鍵 \_ 按一下
-   SE \_拖動
-   SE \_向右 \_ 拖曳
-   SE \_按住 \_ ENTER
-   SE \_保留 \_ 離開
-   SE \_停留 \_ 輸入
-   SE \_停留 \_ 離開
-   SE \_中間 \_ 按一下
-   SE \_關鍵
-   SE \_輔助 \_ 按鍵
-   SE \_手勢 \_ 模式
-   SE \_游標

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows僅限 XP Tablet PC Edition \[ 桌面應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                              |
| 程式庫<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITabletEventSink 介面**](itableteventsink.md)
</dt> </dl>

 

 





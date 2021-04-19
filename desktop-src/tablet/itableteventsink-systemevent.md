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
ms.openlocfilehash: 71b5882fd9e19df43581e00cce55c2af5faa432b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106992063"
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



| 傳回碼                                                                            | Description                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>   | 成功。<br/>                       |
| <dl> <dt>**E \_ 失敗**</dt> </dl> | 發生未指定的錯誤。<br/> |



 

## <a name="remarks"></a>備註

下列清單包含事件參數的有效值。

-   SE \_ 點一下
-   SE \_ 按兩下 \_
-   以 \_ 滑鼠右鍵 \_ 按一下
-   SE \_ 拖曳
-   SE \_ 向右 \_ 拖曳
-   SE \_ 按住 \_ ENTER
-   SE \_ 保留 \_
-   SE \_ 停留 \_ 輸入
-   SE \_ 停留 \_ 離開
-   SE \_ 中間 \_ 點按一下
-   SE \_ 金鑰
-   SE \_ 輔助 \_ 按鍵
-   SE \_ 手勢 \_ 模式
-   SE 資料 \_ 指標

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

 

 





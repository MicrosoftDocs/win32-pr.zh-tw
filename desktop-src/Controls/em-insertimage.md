---
title: 'EM_INSERTIMAGE 訊息 (Richedit .h) '
description: 以顯示影像的 blob 取代選取範圍。
ms.assetid: 147B298B-C4A9-455B-9736-A0B09D72902B
keywords:
- EM_INSERTIMAGE message Windows 控制項
topic_type:
- apiref
api_name:
- EM_INSERTIMAGE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc9ff1e0fd355cf5dd8d43d211c44fda6417c638
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464536"
---
# <a name="em_insertimage-message"></a>EM \_ INSERTIMAGE 訊息

以顯示影像的 blob 取代選取範圍。


```C++
#define EM_INSERTIMAGE       (WM_USER + 314)
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

未使用;必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

包含映射 blob 的 [**RICHEDIT \_ 影像 \_ 參數**](/windows/win32/api/richedit/ns-richedit-richedit_image_parameters) 結構指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

\_如果成功，則傳回 S OK，或下列其中一個錯誤碼。



| 傳回碼                                                                                    | Description                                                   |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <dt>**E \_失敗**</dt> </dl>        | 無法插入影像。 <br/>                          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>   | *LParam* 參數為 Null 或指向不正確影像。 |
| <dl> <dt>**E \_OUTOFMEMORY**</dt> </dl> | 可用的記憶體不足。<br/>                  |



 

## <a name="remarks"></a>備註

如果選取範圍是插入點，則會在插入點插入映射 blob。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**EM \_ INSERTTABLE**](em-inserttable.md)
</dt> </dl>

 

 






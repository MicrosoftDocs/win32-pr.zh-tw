---
title: WM_POINTERROUTEDAWAY 訊息
description: 當指標輸入路由傳送至另一個進程時，在接收輸入的進程上發生。AddContentWithCrossProcessChaining) 。
ms.assetid: 06F8152C-0DA0-4820-835E-07AD35B24310
keywords:
- WM_POINTERROUTEDAWAY 訊息輸入訊息和通知
topic_type:
- apiref
api_name:
- WM_POINTERROUTEDAWAY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 3c099c02338aa70817d75717064e0b99ac13c96b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025263"
---
# <a name="wm_pointerroutedaway-message"></a>WM_POINTERROUTEDAWAY 訊息

當指標輸入路由傳送至另一個進程時，在接收輸入的進程上發生。

當指標輸入在設定為跨進程連結 ([**AddContentWithCrossProcessChaining**](/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining)) 的內容之間轉換時，會傳送到另一個進程。

這則訊息會傳送至目前正在接收指標輸入的進程。


```C++
#define WM_POINTERROUTEDAWAY       0x0252
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

未使用的。

</dd> <dt>

*lParam* 
</dt> <dd>

未使用的。

</dd> </dl>

## <a name="return-value"></a>傳回值

NULL

## <a name="remarks"></a>備註

此訊息不會隨 [**WM_POINTERUP**](wm-pointerup.md) 訊息或 [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md) 訊息傳送。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 10 桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2016 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[訊息](messages.md)
</dt> <dt>

[**WM_POINTERROUTEDTO**](wm-pointerroutedto.md)
</dt> </dl>

 


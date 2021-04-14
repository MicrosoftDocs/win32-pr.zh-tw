---
title: WM_POINTERROUTEDTO 訊息
description: 在針對現有指標識別碼進行中的指標輸入時傳送，會在針對跨進程連結設定的內容之間，從一個進程轉換成另一個進程 (AddContentWithCrossProcessChaining) 。
ms.assetid: 163E2C31-4E29-4CBA-B079-1963D4762D7B
keywords:
- WM_POINTERROUTEDTO 訊息輸入訊息和通知
topic_type:
- apiref
api_name:
- WM_POINTERROUTEDTO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 7658aeef77a0f7e19f2449213e9332b4e60c9450
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384410"
---
# <a name="wm_pointerroutedto-message"></a>WM_POINTERROUTEDTO 訊息

在針對現有指標識別碼進行中的指標輸入時傳送，會在針對跨進程連結設定的內容之間，從一個進程轉換成另一個進程 ([**AddContentWithCrossProcessChaining**](/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining)) 。

這則訊息會傳送至目前未接收指標輸入的進程。


```C++
#define WM_POINTERROUTEDTO       0x0251
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

當針對不同進程的新指標識別碼張貼 [**WM_POINTERDOWN**](wm-pointerdown.md) 訊息時，不會傳送此訊息。

如果先張貼 **WM_POINTERROUTEDTO** 訊息，則不會傳送 [**WM_POINTERDOWN**](wm-pointerdown.md)訊息。

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

[**WM_POINTERROUTEDAWAY**](wm-pointerroutedaway.md)
</dt> </dl>

 


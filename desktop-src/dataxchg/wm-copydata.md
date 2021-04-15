---
title: 'WM_COPYDATA 訊息 (Winuser .h) '
description: 應用程式會傳送 WM \_ COPYDATA 訊息，以將資料傳遞給另一個應用程式。
ms.assetid: d937a260-9fd2-4450-a762-20120f589ab1
keywords:
- WM_COPYDATA 訊息資料交換
topic_type:
- apiref
api_name:
- WM_COPYDATA
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8160c88b11fa109e8bbfaa06f0f6c45c9b7daed0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465616"
---
# <a name="wm_copydata-message"></a>WM \_ COPYDATA 訊息

應用程式會傳送 **WM \_ COPYDATA** 訊息，以將資料傳遞給另一個應用程式。


```C++
#define WM_COPYDATA                     0x004A
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

傳遞資料的視窗控制碼。

</dd> <dt>

*lParam* 
</dt> <dd>

[**COPYDATASTRUCT**](/windows/win32/api/winuser/ns-winuser-copydatastruct)結構的指標，其中包含要傳遞的資料。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果接收的應用程式處理此訊息，它應該會傳回 **TRUE**;否則，它應該會傳回 **FALSE**。

## <a name="remarks"></a>備註

傳遞的資料不能包含指標或其他物件參考，無法存取接收資料的應用程式。

傳送此訊息時，所參考的資料不得由傳送進程的另一個執行緒變更。

接收應用程式應該將資料視為唯讀。 *LParam* 參數只在訊息處理期間有效。 接收的應用程式不應該釋放 *lParam* 所參考的記憶體。 如果接收應用程式必須在 [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) 傳回之後存取資料，則必須將資料複製到本機緩衝區。

## <a name="examples"></a>範例

如需範例，請參閱 [使用資料複製](using-data-copy.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[**COPYDATASTRUCT**](/windows/win32/api/winuser/ns-winuser-copydatastruct)
</dt> </dl>

 


---
title: 'WM_DDE_INITIATE 訊息 (的) '
description: 動態資料交換 (DDE) 用戶端應用程式傳送 WM \_ dde \_ 的初始訊息，以起始與伺服器應用程式的交談，回應指定的應用程式和主題名稱。
ms.assetid: d486f584-75a3-4ffd-ba5d-f95f2692cd6c
keywords:
- WM_DDE_INITIATE 訊息資料 Exchange
topic_type:
- apiref
api_name:
- WM_DDE_INITIATE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27d2d5cf46221e268cf27f7557349185b32aafff65bdd20b0ac20063fde151a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117915146"
---
# <a name="wm_dde_initiate-message"></a>WM \_ DDE \_ 起始訊息

動態資料交換 (DDE) 用戶端應用程式傳送 **WM \_ dde 的 \_ 初始** 訊息，以起始與伺服器應用程式的交談，回應指定的應用程式和主題名稱。 收到此訊息時，所有名稱符合指定之應用程式且支援指定主題的伺服器應用程式，都應該要知道它。  (需詳細資訊，請參閱 [**WM \_ DDE \_ ACK**](wm-dde-ack.md) 訊息。 ) 


```C++
#define WM_DDE_INITIATE        0x03E0
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

傳送訊息之用戶端視窗的控制碼。

</dd> <dt>

*lParam* 
</dt> <dd>

低序位字組包含 atom，用來識別要求交談的應用程式。 應用程式名稱不能包含斜線 (/) 或反斜線 (\\) 。 這些字元會保留給網路執行。 如果此參數為 **Null**，則會要求與所有應用程式的交談。

高序位單字包含的 atom 會識別要求交談的主題。 如果主題為 **Null**，則會要求所有可用主題的交談。

</dd> </dl>

## <a name="remarks"></a>備註

如果 *lParam* 的低序位字是 **Null**，任何伺服器應用程式都可以回應。 如果 *lParam* 的高序位字是 **Null**，則任何主題都有效。 在收到具有 *lParam* 參數高序位字組的 **wm \_ dde \_ 起始** 要求 **時，伺服器** 必須針對它所支援的每個主題傳送 [**wm \_ dde \_ ACK**](wm-dde-ack.md)訊息。

### <a name="sending"></a>傳送

用戶端會將 [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) 的第一個參數設定為 **HWND \_ 廣播**，以將訊息廣播到所有最上層視窗。

如果用戶端應用程式已經取得所需伺服器的視窗控制碼，它可以將伺服器的視窗控制碼傳遞為 [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)的第一個參數，以將該伺服器的視窗控制碼直接傳送到伺服器視窗。 **\_ \_**

用戶端應用程式會藉由呼叫 [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) 函數來配置原子。

當 [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) 傳回時，用戶端應用程式必須刪除原子。

### <a name="receiving"></a>接收

若要完成對話的起始，伺服器應用程式必須回應一或多個 [**WM \_ DDE \_**](wm-dde-ack.md) 通知訊息，其中每個訊息都是針對個別的主題。 傳送 **wm \_ dde \_** 通知訊息時，伺服器應該建立新的原子，不應重複使用與 **WM \_ DDE \_ 起始** 一起傳送的原子。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                 |
| 標頭<br/>                   | <dl> <dt>Dde. h (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)
</dt> <dt>

[**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[**WM \_ DDE \_ ACK**](wm-dde-ack.md)
</dt> <dt>

**概念**
</dt> <dt>

[關於動態資料交換](about-dynamic-data-exchange.md)
</dt> </dl>

 


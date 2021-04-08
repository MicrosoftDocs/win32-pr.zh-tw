---
title: 'WM_DDE_REQUEST 訊息 (的) '
description: 動態資料交換 (DDE) 用戶端應用程式會將 WM \_ DDE \_ 要求訊息張貼至 dde 伺服器應用程式，以要求資料項目的值。 若要張貼此訊息，請使用下列參數呼叫 PostMessage 函數。
ms.assetid: 922452d2-455c-43e1-a8a8-e3c52b0fab51
keywords:
- WM_DDE_REQUEST 訊息資料交換
topic_type:
- apiref
api_name:
- WM_DDE_REQUEST
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f7d5eab75d3b7298d78547b17fccfb164a47ae4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685804"
---
# <a name="wm_dde_request-message"></a>WM \_ DDE \_ 要求訊息

動態資料交換 (DDE) 用戶端應用程式會將 **WM \_ DDE \_ 要求** 訊息張貼至 dde 伺服器應用程式，以要求資料項目的值。

若要張貼此訊息，請使用下列參數呼叫 [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) 函數。


```C++
#define WM_DDE_REQUEST     0x03E6
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

傳送訊息之用戶端視窗的控制碼。

</dd> <dt>

*lParam* 
</dt> <dd>

低序位字組指定標準或已註冊的剪貼簿格式。

高序位單字包含一個 atom，用來識別從伺服器要求的資料項目。

</dd> </dl>

## <a name="remarks"></a>備註

### <a name="posting"></a>張貼

用戶端應用程式會藉由呼叫 [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) 函數來配置 atom。

### <a name="receiving"></a>接收

如果接收 (伺服器) 應用程式可以滿足要求，它就會以包含所要求資料的 [**WM \_ DDE \_ 資料**](wm-dde-data.md) 訊息進行回應。 否則，它會以負的 [**WM \_ DDE \_ 確認**](wm-dde-ack.md) 訊息來回應。

當回應 [**wm \_ dde \_ 資料**](wm-dde-data.md) 或 [**wm \_ dde \_**](wm-dde-ack.md) 通知訊息時，伺服器應用程式可以重複使用 atom，也可以刪除 atom 並建立一個新的 atom。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                 |
| 標頭<br/>                   | <dl> <dt> (包含 Windows. h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)
</dt> <dt>

[**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam)
</dt> <dt>

[**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam)
</dt> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[**UnpackDDElParam**](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[**WM \_ DDE \_ ACK**](wm-dde-ack.md)
</dt> <dt>

[**WM \_ DDE \_ 資料**](wm-dde-data.md)
</dt> <dt>

**概念**
</dt> <dt>

[關於動態資料交換](about-dynamic-data-exchange.md)
</dt> </dl>

 


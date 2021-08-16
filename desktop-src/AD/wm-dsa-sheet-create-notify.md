---
title: WM_DSA_SHEET_CREATE_NOTIFY 訊息
description: 張貼至 Active Directory MMC 嵌入式管理單元，以建立次要屬性工作表。
ms.assetid: 878878bf-fb78-4669-b282-1dd3349f35d5
ms.tgt_platform: multiple
keywords:
- WM_DSA_SHEET_CREATE_NOTIFY 訊息 Active Directory
topic_type:
- apiref
api_name:
- WM_DSA_SHEET_CREATE_NOTIFY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c51fc850504eb4455a41b881aed1109554d0482a8f889fafa2eaf7050488e450
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024186"
---
# <a name="wm_dsa_sheet_create_notify-message"></a>WM \_ DSA \_ 工作表 \_ 建立 \_ 通知訊息

「 **WM \_ DSA \_ 工作表 \_ 建立 \_ 通知** 」訊息會張貼至 Active Directory MMC 嵌入式管理單元，以建立次要屬性工作表。

> [!Note]  
> 這個訊息值未定義于已發行的標頭檔中。 若要使用這個訊息值，請以所示的確切格式來定義它。

 


```C++
#define WM_DSA_SHEET_CREATE_NOTIFY (WM_USER + 6)
LRESULT SendMessage(
    (HWND) hwnd, 
    WM_DSA_SHEET_CREATE_NOTIFY,
    (WPARAM) wParam, 
    (LPARAM) lParam);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hwnd* 
</dt> <dd>

將處理此訊息之嵌入式管理單元視窗的視窗控制碼。 這個控制碼是從 [**PROPSHEETCFG**](propsheetcfg.md)結構的 **hwndHidden** 成員取得的。

</dd> <dt>

*wParam* 
</dt> <dd>

包含 [**DSA \_ SEC \_ 頁面 \_ 資訊**](dsa-sec-page-info.md) 結構的指標，此結構會定義要建立的次要屬性工作表。 當不再需要時，訊息接收器必須使用 [**>localfree**](/windows/desktop/api/winbase/nf-winbase-localfree) 函式釋放此記憶體。

</dd> <dt>

*lParam* 
</dt> <dd>

未使用。

</dd> </dl>

## <a name="return-value"></a>傳回值

未使用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>       |
| 最低支援的伺服器<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**PROPSHEETCFG**](propsheetcfg.md)
</dt> <dt>

[**DSA \_ 秒 \_ 頁面 \_ 資訊**](dsa-sec-page-info.md)
</dt> <dt>

[**>localfree**](/windows/desktop/api/winbase/nf-winbase-localfree)
</dt> </dl>

 


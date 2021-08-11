---
title: WM_DSA_SHEET_CLOSE_NOTIFY 訊息
description: 當次要屬性工作表損毀時，張貼至 Active Directory MMC 嵌入式管理單元。
ms.assetid: 74271550-e1f7-4576-a04f-52d5b7c619cb
ms.tgt_platform: multiple
keywords:
- WM_DSA_SHEET_CLOSE_NOTIFY 訊息 Active Directory
topic_type:
- apiref
api_name:
- WM_DSA_SHEET_CLOSE_NOTIFY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f840790de51ce712b33fc9a9611934e8be9a76a35a0fc01a4ce0abe4ba040d2f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118181668"
---
# <a name="wm_dsa_sheet_close_notify-message"></a>WM \_ DSA \_ 工作表 \_ 關閉 \_ 通知訊息

當次要屬性工作表損毀時，會將 **WM \_ DSA \_ 工作表 \_ 關閉 \_ 通知** 訊息張貼至 Active Directory MMC 嵌入式管理單元。

> [!Note]  
> 這個訊息值未定義于已發行的標頭檔中。 若要使用這個訊息值，您必須以所示的確切格式來定義它。

 


```C++
#define WM_DSA_SHEET_CLOSE_NOTIFY (WM_USER + 5)
```




```C++
LRESULT SendMessage( (HWND)   hwnd, 
                     (UINT)   WM_DSA_SHEET_CLOSE_NOTIFY,
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

包含應用程式定義的32位值。 這是從 [**PROPSHEETCFG**](propsheetcfg.md)結構的 **wParamSheetClose** 成員取得的。

</dd> <dt>

*lParam* 
</dt> <dd>

未使用。

</dd> </dl>

## <a name="return-value"></a>傳回值

未使用此訊息的傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>       |
| 最低支援的伺服器<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**PROPSHEETCFG**](propsheetcfg.md)
</dt> </dl>

 

 






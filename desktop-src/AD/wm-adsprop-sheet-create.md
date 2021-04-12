---
title: WM_ADSPROP_SHEET_CREATE 訊息
description: 傳送至通知物件，以在 Active Directory MMC 嵌入式管理單元中建立次要屬性工作表。
ms.assetid: 3efa25f2-cd39-44f8-952e-203f1519ce2c
ms.tgt_platform: multiple
keywords:
- WM_ADSPROP_SHEET_CREATE 訊息 Active Directory
topic_type:
- apiref
api_name:
- WM_ADSPROP_SHEET_CREATE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b540ffd87d4350a323577ff5fa317e94f9271f2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508615"
---
# <a name="wm_adsprop_sheet_create-message"></a>WM \_ ADSPROP \_ 工作表 \_ 建立訊息

會將 **WM \_ ADSPROP \_ 工作表 \_ 建立** 訊息傳送至通知物件，以在 Active Directory MMC 嵌入式管理單元中建立次要屬性工作表。

> [!Note]  
> 這個訊息值未定義于已發行的標頭檔中。 若要使用這個訊息值，您必須以所示的確切格式來定義它。

 


```C++
#define WM_ADSPROP_SHEET_CREATE (WM_USER + 1108)
LRESULT SendMessage( (HWND)   hwnd, 
                     (UINT)   WM_ADSPROP_SHEET_CREATE,
                     (WPARAM) wParam, 
                     (LPARAM) lParam);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hwnd* 
</dt> <dd>

通知物件的控制碼。 若要取得此控制碼，請呼叫 [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)。

</dd> <dt>

*wParam* 
</dt> <dd>

包含 [**DSA \_ SEC \_ 頁面 \_ 資訊**](dsa-sec-page-info.md) 結構的指標，此結構會定義要建立的次要頁面。 只有一個次要屬性工作表可以使用 **WM \_ ADSPROP \_ 工作表 \_ 建立** 訊息來建立，因此 [**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) 結構只能包含一個 [**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) 結構。

</dd> <dt>

*lParam* 
</dt> <dd>

未使用。 必須是 **Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

此訊息的傳回值一律為零。

## <a name="remarks"></a>備註

呼叫端必須使用 [**LocalAlloc**](/windows/desktop/api/winbase/nf-winbase-localalloc)函式的單一呼叫來配置 [**DSA \_ SEC \_ 頁面 \_ 資訊**](dsa-sec-page-info.md)結構、title 字串和所有 [**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject)字串。 **WM \_ ADSPROP \_ SHEET \_ CREATE** message 是非同步訊息，因此它會在建立次要工作表之前傳回。 因此，在訊息傳回之後，記憶體必須保持不變。 接收器會在建立次要工作表之後，透過單一呼叫 [**>localfree**](/windows/desktop/api/winbase/nf-winbase-localfree) 函式來釋放此記憶體。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>       |
| 最低支援的伺服器<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CFSTR \_ DS \_ PARENTHWND**](cfstr-ds-parenthwnd.md)
</dt> <dt>

[**DSA \_ 秒 \_ 頁面 \_ 資訊**](dsa-sec-page-info.md)
</dt> <dt>

[**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames)
</dt> <dt>

[**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject)
</dt> <dt>

[**LocalAlloc**](/windows/desktop/api/winbase/nf-winbase-localalloc)
</dt> <dt>

[**>localfree**](/windows/desktop/api/winbase/nf-winbase-localfree)
</dt> </dl>

 


---
description: 應用程式會在對 \_ WIN.INI 檔案進行變更之後，將 WM WININICHANGE 訊息傳送至所有最上層視窗。 SystemParametersInfo 函式會在應用程式使用函式來變更 WIN.INI 中的設定之後傳送此訊息。
ms.assetid: 402f8d71-ad52-486d-be26-8b41a3f22045
title: 'WM_WININICHANGE 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81cfdfeff65c1580f0bd8373fdc5ef1eec409233a9624934ea67ba835ddf805e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810458"
---
# <a name="wm_wininichange-message"></a>WM \_ WININICHANGE 訊息

應用程式會在對 WIN.INI 檔案進行變更之後，將 **WM \_ WININICHANGE** 訊息傳送至所有最上層視窗。 [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)函式會在應用程式使用函式來變更 WIN.INI 中的設定之後傳送此訊息。

> [!Note]  
> 只有在與舊版系統相容時，才會提供 **WM \_ WININICHANGE** 訊息。 應用程式應該使用 [**WM \_ SETTINGCHANGE**](wm-settingchange.md) 訊息。

 

視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。


```C++
#define WM_WININICHANGE                 0x001A
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

不使用這個參數。

</dd> <dt>

*lParam* 
</dt> <dd>

字串的指標，其中包含已變更之系統參數的名稱。 例如，這個字串可以是登錄機碼的名稱或 Win.ini 檔中區段的名稱。 此參數在判斷哪些系統參數變更時特別有用。 例如，當字串是登錄名稱時，通常只會指出登錄中的分葉節點，而不是整個路徑。 此外，某些應用程式會傳送此訊息，並將 *lParam* 設定為 **Null**。 一般來說，當您收到此訊息時，您應該檢查並重載您的應用程式所使用的任何系統參數設定。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **LRESULT**

如果您處理此訊息，則傳回零。

## <a name="remarks"></a>備註

若要將 **WM \_ WININICHANGE** 訊息傳送至所有最上層視窗，請使用 [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) 函式並將 *hwnd* 參數設定為 **hwnd \_ 廣播**。

呼叫變更 WIN.INI 的函式，可能會改為對應至登錄。 當 WIN.INI，且變更的區段在登錄中的下列機碼下指定時，就會發生此對應：

**HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ IniFileMapping**

儲存位置的變更不會影響此訊息的行為。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
</dt> </dl>

 

 

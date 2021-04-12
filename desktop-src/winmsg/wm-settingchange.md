---
description: 當 SystemParametersInfo 函式變更整個系統的設定或原則設定變更時，傳送至所有最上層視窗的訊息。
ms.assetid: 77174e06-a25b-440a-9e9c-4fd5979c433c
title: 'WM_SETTINGCHANGE 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1c3d1360b5e4cc5de2dbd23b09b8f2ad034948f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194955"
---
# <a name="wm_settingchange-message"></a>WM \_ SETTINGCHANGE 訊息

當 [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) 函式變更整個系統的設定或原則設定變更時，傳送至所有最上層視窗的訊息。

應用程式應該會在對系統參數進行變更時，將 **WM \_ SETTINGCHANGE** 傳送至所有最上層視窗。  (無法直接將此訊息傳送至視窗。 ) 若要將 **WM \_ SETTINGCHANGE** 訊息傳送至所有最上層視窗，請使用 [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) 函式並將 *hwnd* 參數設定為 **hwnd \_ 廣播**。

視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。


```C++
#define WM_WININICHANGE                 0x001A
#define WM_SETTINGCHANGE                WM_WININICHANGE
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

當系統傳送此訊息作為 [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)呼叫的結果時， *wParam* 參數是傳遞給 **SystemParametersInfo** 函數的 *uiAction* 參數值。 如需值的清單，請參閱 **SystemParametersInfo**。

當系統由於原則設定變更而傳送此訊息時，此參數會指出已套用的原則類型。 如果套用了電腦原則，則此值為1，如果套用了使用者原則，則為零。

當系統因地區設定變更而傳送此訊息時，此參數為零。

當應用程式傳送此訊息時，此參數必須為 **Null**。

</dd> <dt>

*lParam* 
</dt> <dd>

當系統傳送此訊息作為 [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) 呼叫的結果時， *lParam* 是指向字串的指標，指出包含已變更之系統參數的區域。 此參數通常不會指出哪些特定的系統參數已變更。  (請注意，有些應用程式會傳送此訊息，並將 *lParam* 設定為 **Null**。 ) 一般而言，當您收到此訊息時，您應該檢查並重載您的應用程式所使用的任何系統參數設定。

這個字串可以是登錄機碼的名稱或 Win.ini 檔案中區段的名稱。 當字串是登錄名稱時，通常只會指出登錄中的分葉節點，而不是完整路徑。

當系統由於原則設定變更而傳送此訊息時，此參數會指向字串 "Policy"。

當系統因地區設定的變更而傳送此訊息時，此參數會指向字串 "國際"。

若要對系統或使用者的環境變數產生變更，請將 *lParam* 設定為字串 "環境" 的訊息廣播。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **LRESULT**

如果您處理此訊息，則傳回零。

## <a name="remarks"></a>備註

*LParam* 參數會指出已變更的系統計量，例如，如果已切換 ConvertibleSlateMode 指標，則為 "ConvertibleSlateMode"，如果停駐指標已切換，則為 "SystemDockMode"。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[原則事件](/previous-versions/windows/desktop/Policy/policy-events)
</dt> <dt>

[**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta)
</dt> <dt>

[**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
</dt> </dl>

 

 

---
description: 當系統要求視窗要接收的系統手勢時傳送。
ms.assetid: 5b747b3c-3b77-4913-932f-182114d1f674
title: 'WM_TABLET_QUERYSYSTEMGESTURESTATUS 訊息 (Tpcshrd .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 395196f963cae9b8d18697276e546f1eba05b245
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847974"
---
# <a name="wm_tablet_querysystemgesturestatus-message"></a>WM \_ 平板電腦 \_ QUERYSYSTEMGESTURESTATUS 訊息

當系統要求視窗要接收的系統手勢時傳送。


```C++
#define WM_TABLET_DEFBASE                    0x02C0
#define WM_TABLET_QUERYSYSTEMGESTURESTATUS   (WM_TABLET_DEFBASE + 12)       
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

未使用。

</dd> <dt>

*lParam* 
</dt> <dd>

代表螢幕座標的點值。

</dd> </dl>

## <a name="remarks"></a>備註

藉由處理此訊息，您可以動態停用視窗區域的筆觸。

> [!Note]  
> 您可以使用和宏，將 *lParam* 轉換為 x 座標和 y 座標 `GET_X_LPARAM` `GET_Y_LPARAM` 。

 

根據預設，您的視窗將會接收所有系統手勢事件。 您可以在 **WndProc** 中回應 **WM \_ TABLET \_ QUERYSYSTEMGESTURESTATUS** 訊息，以選擇您希望視窗接收的事件，以及您想要停用的事件。 **WM \_ TABLET \_ QUERYSYSTEMGESTURESTATUS** 訊息定義于 tpcshrd 中。 啟用及停用系統 tablet 系統手勢的值也會在 tpcshrd 中定義，如下所示：

``` syntax
#define TABLET_DISABLE_PRESSANDHOLD        0x00000001
#define TABLET_DISABLE_PENTAPFEEDBACK      0x00000008
#define TABLET_DISABLE_PENBARRELFEEDBACK   0x00000010
#define TABLET_DISABLE_TOUCHUIFORCEON      0x00000100
#define TABLET_DISABLE_TOUCHUIFORCEOFF     0x00000200
#define TABLET_DISABLE_TOUCHSWITCH         0x00008000
#define TABLET_DISABLE_FLICKS              0x00010000
#define TABLET_ENABLE_FLICKSONCONTEXT      0x00020000
#define TABLET_ENABLE_FLICKLEARNINGMODE    0x00040000
#define TABLET_DISABLE_SMOOTHSCROLLING     0x00080000
#define TABLET_DISABLE_FLICKFALLBACKKEYS   0x00100000
#define TABLET_ENABLE_MULTITOUCHDATA       0x01000000
```

> [!Note]
>
> 停用按住不放將會改善滑鼠點擊的回應速度，因為此功能會建立一個等候時間來區別這兩個作業。

 

處理 **WM \_ 平板電腦 \_ QUERYSYSTEMGESTURESTATUS** 訊息時，請特別小心。 **WM \_TABLET \_ QUERYSYSTEMGESTURESTATUS** 是使用 [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) 函式來傳遞。 如果您呼叫 COM 介面上的方法，該物件必須在相同的進程中。 如果不是，COM 會擲回例外狀況。

## <a name="examples"></a>範例

下列範例示範如何使用 WM TABLET QUERYSYSTEMGESTURESTATUS 來停用區域的 \_ 筆觸 \_ 。


```C++
#include <windowsx.h>        

(...)        
        
LRESULT CALLBACK WndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam){
    case WM_TABLET_QUERYSYSTEMGESTURESTATUS:
        int x = GET_X_LPARAM(lParam);
        int y = GET_Y_LPARAM(lParam);
        if (x < xThreashold && y < yThreshold){
            // no flicks in the region specified by the threashold
            return TABLET_DISABLE_FLICKS;
        }
        // flicks will happen otherwise
        return 0;
}        
        
```



下列範例顯示如何針對整個視窗停用各種筆觸功能。


```C++
const DWORD dwHwndTabletProperty = 
    TABLET_DISABLE_PRESSANDHOLD | // disables press and hold (right-click) gesture
    TABLET_DISABLE_PENTAPFEEDBACK | // disables UI feedback on pen up (waves)
    TABLET_DISABLE_PENBARRELFEEDBACK | // disables UI feedback on pen button down (circle)
    TABLET_DISABLE_FLICKS; // disables pen flicks (back, forward, drag down, drag up)
        
void SetTabletpenserviceProperties(HWND hWnd){
    ATOM atom = ::GlobalAddAtom(MICROSOFT_TABLETPENSERVICE_PROPERTY);    
    ::SetProp(hWnd, MICROSOFT_TABLETPENSERVICE_PROPERTY, reinterpret_cast<HANDLE>(dwHwndTabletProperty));
    ::GlobalDeleteAtom(atom);
}        
        
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Tpcshrd。h</dt> </dl> |



 

 

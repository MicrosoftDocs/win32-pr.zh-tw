---
title: 'WM_DWMSENDICONICLIVEPREVIEWBITMAP 訊息 (Dwmapi.dll .h) '
description: 指示視窗提供靜態點陣圖作為即時預覽 (也稱為該視窗的查看預覽) 。
ms.assetid: 24bf3b42-a850-4aa5-966a-29baab6b4d21
keywords:
- WM_DWMSENDICONICLIVEPREVIEWBITMAP 訊息桌面視窗管理員
topic_type:
- apiref
api_name:
- WM_DWMSENDICONICLIVEPREVIEWBITMAP
api_location:
- Dwmapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21f73076ab313da66171bc8265f7f4e7d068f93e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465497"
---
# <a name="wm_dwmsendiconiclivepreviewbitmap-message"></a>WM \_ DWMSENDICONICLIVEPREVIEWBITMAP 訊息

指示視窗提供靜態點陣圖作為 *即時預覽* (也稱為該視窗的 *查看預覽*) 。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

未使用。

</dd> <dt>

*lParam* 
</dt> <dd>

未使用。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式處理此訊息，它應該會傳回零。

## <a name="remarks"></a>備註

當使用者將滑鼠指標移至工作列中視窗的縮圖上，或在 ALT + TAB 視窗中提供縮圖焦點時，會出現一個 *即時預覽* (也稱為 [ *查看預覽* ]) 。 此視圖是視窗的完整大小預覽，可以是即時快照或 iconic 標記法。

當下列所有情況都成立時，桌面視窗管理員 (DWM) 會將此訊息傳送至視窗：

-   已在視窗上叫用即時預覽。
-   DWMWA 已在視窗上設定 [**\_ \_ ICONIC \_ BITMAP**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute) 屬性。
-   Iconic 標記法是此視窗唯一存在的標記法。

接收此訊息的視窗應該會產生完整縮放點陣圖以回應。 然後，此視窗會呼叫 [**DwmSetIconicLivePreviewBitmap**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap) 函式來設定即時預覽。 如果視窗未在指定的時間內設定點陣圖，DWM 會針對視窗使用自己的預設 iconic 標記法。

## <a name="examples"></a>範例

下列範例示範對 **WM \_ DWMSENDICONICLIVEPREVIEWBITMAP** 訊息的回應。 此範例會使用自訂、裝置獨立點陣圖的控制碼來呼叫 [**DwmSetIconicLivePreviewBitmap**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap) 函式，以作為視窗的標記法。


```C++
        case WM_DWMSENDICONICLIVEPREVIEWBITMAP:
        {
            // This window is being asked to provide a bitmap to show in Peek preview.
            // This indicates the thumbnail in the taskbar is being previewed.
            RECT rectWindow = {0, 0, 0, 0};
            if (GetClientRect(hwnd, &rectWindow))
            {
                nWidth = rectWindow.right - rectWindow.left;
                nHeight = rectWindow.bottom - rectWindow.top;
            }

            hbm = CreateDIB(nWidth, nHeight);
            if (hbm)
            {
                hr = DwmSetIconicLivePreviewBitmap(hwnd, hbm, NULL, DWM_SIT_DISPLAYFRAME);
                DeleteObject(hbm);
            }
        }
        break;
```



如需完整的程式碼，請參閱 [自訂 Iconic 縮圖和即時預覽點陣圖](dwm-sample-customizethumbnail.md) 範例。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Dwmapi.dll。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**WM \_ DWMSENDICONICTHUMBNAIL**](wm-dwmsendiconicthumbnail.md)
</dt> <dt>

[**DwmInvalidateIconicBitmaps**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwminvalidateiconicbitmaps)
</dt> </dl>

 

 






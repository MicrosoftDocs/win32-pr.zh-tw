---
title: 'WM_DWMSENDICONICTHUMBNAIL 訊息 (Dwmapi.dll .h) '
description: 指示視窗提供靜態點陣圖，以用來做為該視窗的縮圖標記法。
ms.assetid: 476c2542-f4d0-4777-93d3-bf50da26d94f
keywords:
- WM_DWMSENDICONICTHUMBNAIL 訊息桌面視窗管理員
topic_type:
- apiref
api_name:
- WM_DWMSENDICONICTHUMBNAIL
api_location:
- Dwmapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3263f34cd59ba68ee895e5d5c77e297144cbadd6c8d8bbaa49ca6272248c2024
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119842648"
---
# <a name="wm_dwmsendiconicthumbnail-message"></a>WM \_ DWMSENDICONICTHUMBNAIL 訊息

指示視窗提供靜態點陣圖，以用來做為該視窗的縮圖標記法。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

未使用。

</dd> <dt>

*lParam* 
</dt> <dd>

此值的 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) 是縮圖的最大 x 座標。 [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))是最大的 y 座標。 如果縮圖的維度超過其中一或兩個值，則 DWM 不接受縮圖。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式處理此訊息，它應該會傳回零。

## <a name="remarks"></a>備註

如果下列所有情況都成立，則 DWM 會將此訊息傳送至視窗：

-   DWM 會顯示視窗的 iconic 標記法。
-   DWMWA 已在視窗上設定 [**\_ \_ ICONIC \_ BITMAP**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute) 屬性。
-   視窗未設定快取點陣圖。
-   快取中有另一個點陣圖的空間。

接收此訊息的視窗應該會產生不超過訊息參數所要求大小的點陣圖，以回應。 然後，此視窗會呼叫 [**DwmSetIconicThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail) 函式來覆寫預設的縮圖。 如果視窗未在指定的時間內提供點陣圖，DWM 會針對視窗使用自己的預設 iconic 標記法。

視窗必須屬於呼叫進程。

## <a name="examples"></a>範例

下列程式碼範例顯示如何回應 **WM \_ DWMSENDICONICTHUMBNAIL** 訊息。 此範例會使用自訂、裝置獨立點陣圖的控制碼來呼叫 [**DwmSetIconicThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail)，以做為 windows 的表示。


```C++
        case WM_DWMSENDICONICTHUMBNAIL:
        {    
            // This window is being asked to provide its iconic bitmap. This indicates
            // a thumbnail is being drawn.
            hbm = CreateDIB(HIWORD(lParam), LOWORD(lParam)); 
            if (hbm)
            {
                hr = DwmSetIconicThumbnail(hwnd, hbm, 0);
                DeleteObject(hbm);
            }
        }
        break;
```



如需完整範例，請參閱 [自訂 Iconic 縮圖和即時預覽點陣圖](dwm-sample-customizethumbnail.md) 範例。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Dwmapi.dll。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DwmInvalidateIconicBitmaps**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwminvalidateiconicbitmaps)
</dt> <dt>

[**WM \_ DWMSENDICONICLIVEPREVIEWBITMAP**](wm-dwmsendiconiclivepreviewbitmap.md)
</dt> </dl>

 


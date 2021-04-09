---
title: 'WM_PSD_GREEKTEXTRECT 訊息 (Commdlg .h) '
description: 通知頁面設定對話方塊 PagePaintHook 的攔截程式，對話方塊即將在範例頁面的邊界矩形內繪製希臘文文字。
ms.assetid: ad0a200d-5626-4768-b3bd-73d4e3f0d548
keywords:
- WM_PSD_GREEKTEXTRECT 訊息對話方塊
topic_type:
- apiref
api_name:
- WM_PSD_GREEKTEXTRECT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd0853720bea8cadc8df40d8fa649f644fd00694
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025299"
---
# <a name="wm_psd_greektextrect-message"></a>WM \_ PSD \_ GREEKTEXTRECT 訊息

通知 **頁面設定** 對話方塊 [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)的攔截程式，對話方塊即將在範例頁面的邊界矩形內繪製希臘文文字。


```C++
#define WM_USER                  0x0400
#define WM_PSD_GREEKTEXTRECT    (WM_USER+4)
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

範例頁面的裝置內容控制碼。

</dd> <dt>

*lParam* 
</dt> <dd>

[**矩形**](/previous-versions//dd162897(v=vs.85))結構的指標，其中包含希臘文文字矩形的座標（以圖元為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果攔截程式傳回 **TRUE**，對話方塊就不會繪製範例頁面的希臘文文字部分。

如果攔截程式傳回 **FALSE**，對話方塊會繪製範例頁面的希臘文文字部分。

## <a name="remarks"></a>備註

[版面 **設定** ] 對話方塊包含範例頁面的影像，其中顯示使用者的選取專案如何影響列印輸出的外觀。 當您呼叫 [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) 函式時，您可以提供 [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) 攔截程式以自訂範例頁面的外觀。 每當對話方塊要繪製範例頁面的內容時，對話方塊會傳送一連串訊息給攔截程式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Commdlg (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)
</dt> <dt>

[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))
</dt> <dt>

[**WM \_ PSD \_ PAGESETUPDLG**](wm-psd-pagesetupdlg.md)
</dt> <dt>

**概念**
</dt> <dt>

[通用對話方塊程式庫](common-dialog-box-library.md)
</dt> </dl>

 


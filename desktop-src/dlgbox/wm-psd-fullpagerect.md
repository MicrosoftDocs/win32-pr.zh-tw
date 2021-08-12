---
title: 'WM_PSD_FULLPAGERECT 訊息 (Commdlg .h) '
description: 在 [版面設定] 對話方塊中，通知範例頁面矩形座標的 PagePaintHook 勾點程式。 當此對話方塊即將繪製範例頁面的內容時，就會傳送此訊息。
ms.assetid: 88ca1d60-3335-480a-b874-c6f248a3c23a
keywords:
- WM_PSD_FULLPAGERECT 訊息對話方塊
topic_type:
- apiref
api_name:
- WM_PSD_FULLPAGERECT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0b3d49ca34775657fbb626823fe68632ad963abc29a99ff5aa99dce69753e17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118280368"
---
# <a name="wm_psd_fullpagerect-message"></a>WM \_ PSD \_ FULLPAGERECT 訊息

在 [版面設定] 對話方塊中，通知範例頁面矩形座標的 [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) 勾點 **程式** 。 當此對話方塊即將繪製範例頁面的內容時，就會傳送此訊息。


```C++
#define WM_USER                  0x0400
#define WM_PSD_FULLPAGERECT     (WM_USER+1)
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

範例頁面的裝置內容控制碼。

</dd> <dt>

*lParam* 
</dt> <dd>

[**矩形**](/previous-versions//dd162897(v=vs.85))結構的指標，其中包含範例頁面的座標（以圖元為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果攔截程式傳回 **TRUE**，對話方塊將不再傳送任何訊息，而且在下一次系統需要重新繪製範例頁面之前，不會在範例頁面中繪製。

如果攔截程式傳回 **FALSE**，對話方塊會傳送繪圖順序的其餘訊息。

## <a name="remarks"></a>備註

[版面 **設定** ] 對話方塊包含範例頁面的影像，其中顯示使用者的選取專案如何影響列印輸出的外觀。 當您呼叫 [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) 函式時，您可以提供 [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) 攔截程式以自訂範例頁面的外觀。 每當對話方塊要繪製範例頁面的內容時，對話方塊會傳送一連串訊息給攔截程式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Commdlg (包含 Windows .h) </dt> </dl> |



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

 


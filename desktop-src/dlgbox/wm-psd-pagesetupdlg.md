---
title: 'WM_PSD_PAGESETUPDLG 訊息 (Commdlg .h) '
description: 通知 PagePaintHook 勾點程式，[版面設定] 對話方塊即將繪製範例頁面的內容。 攔截程式可以使用此訊息來執行與繪製範例頁面內容相關的初始化工作。
ms.assetid: 0d95240b-7d77-4819-8e5c-cc25cd1b30f2
keywords:
- WM_PSD_PAGESETUPDLG 訊息對話方塊
topic_type:
- apiref
api_name:
- WM_PSD_PAGESETUPDLG
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9706eff6d015dc31332d9f757c954081f0134b2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385210"
---
# <a name="wm_psd_pagesetupdlg-message"></a>WM \_ PSD \_ PAGESETUPDLG 訊息

通知 [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) 勾點程式，[版面 **設定** ] 對話方塊即將繪製範例頁面的內容。 攔截程式可以使用此訊息來執行與繪製範例頁面內容相關的初始化工作。


```C++
#define WM_USER                  0x0400
#define WM_PSD_PAGESETUPDLG     (WM_USER  )
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

低序位字組指定指出紙張大小的值。 這個值可以是結構描述中所列的其中一個 **DMPAPER \_** 值。 高序位單字指定紙張或信封的方向，以及印表機是否為點矩陣或 HPPCL (Hewlett Packard 印表機控制語言) 裝置。 此參數可以是下列其中一個值。



| 值                                                                             | 意義                                            |
|-----------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>0x0001</dt> </dl> | 橫向模式的紙張 (點矩陣) <br/>    |
| <dl> <dt>0x0003</dt> </dl> | 橫向模式的紙張 (HPPCL) <br/>         |
| <dl> <dt>0x0005</dt> </dl> | 直向模式的紙張 (點矩陣) <br/>     |
| <dl> <dt>0x0007</dt> </dl> | 直向模式的紙張 (HPPCL) <br/>          |
| <dl> <dt>0x000b</dt> </dl> | 橫向模式的信封 (HPPCL) <br/>      |
| <dl> <dt>0x000d</dt> </dl> | 直向模式的信封 (點矩陣) <br/>  |
| <dl> <dt>0x0019</dt> </dl> | 以橫向模式 (點矩陣) 的信封<br/> |
| <dl> <dt>0x001f</dt> </dl> | 直向模式的信封 (HPPCL) <br/>       |



 

</dd> <dt>

*lParam* 
</dt> <dd>

[**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga)結構的指標，其中包含用來初始化 [版面 **設定**] 對話方塊的資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果攔截程式傳回 **TRUE**，對話方塊將不再傳送任何訊息，而且在下一次系統需要重新繪製範例頁面之前，不會在範例頁面中繪製。

如果攔截程式傳回 **FALSE**，對話方塊會傳送繪圖順序的其餘訊息。

## <a name="remarks"></a>備註

[版面 **設定** ] 對話方塊包含範例頁面的影像，其中顯示使用者的選取專案如何影響列印輸出的外觀。 當您呼叫 [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) 函式時，您可以提供 [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) 攔截程式以自訂範例頁面的外觀。 每當對話方塊要繪製範例頁面的內容時，對話方塊會傳送一連串訊息給攔截程式。

繪圖順序的前三個訊息 (**wm \_ psd \_ PAGESETUPDLG**、 [**wm \_ psd \_ FULLPAGERECT**](wm-psd-fullpagerect.md)或 [**WM \_ psd \_ MINMARGINRECT**](wm-psd-minmarginrect.md)) 提供攔截程式可用來繪製範例頁面內容的資訊。 其餘訊息 ([**wm \_ psd \_ MARGINRECT**](wm-psd-marginrect.md)、 [**wm \_ psd \_ GREEKTEXTRECT**](wm-psd-greektextrect.md)、 [**wm \_ psd \_ ENVSTAMPRECT**](wm-psd-envstamprect.md)、 [**wm \_ psd \_ YAFULLPAGERECT**](wm-psd-yafullpagerect.md)) 通知攔截程式，指出對話方塊即將繪製範例頁面的特定部分。 這可讓攔截程式選擇性地繪製範例頁面的部分。

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

[**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga)
</dt> <dt>

[**WM \_ PSD \_ ENVSTAMPRECT**](wm-psd-envstamprect.md)
</dt> <dt>

[**WM \_ PSD \_ FULLPAGERECT**](wm-psd-fullpagerect.md)
</dt> <dt>

[**WM \_ PSD \_ GREEKTEXTRECT**](wm-psd-greektextrect.md)
</dt> <dt>

[**WM \_ PSD \_ MARGINRECT**](wm-psd-marginrect.md)
</dt> <dt>

[**WM \_ PSD \_ MINMARGINRECT**](wm-psd-minmarginrect.md)
</dt> <dt>

[**WM \_ PSD \_ YAFULLPAGERECT**](wm-psd-yafullpagerect.md)
</dt> <dt>

**概念**
</dt> <dt>

[通用對話方塊程式庫](common-dialog-box-library.md)
</dt> </dl>

 


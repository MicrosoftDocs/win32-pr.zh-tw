---
title: 'WM_CHANGEUISTATE 訊息 (Winuser .h) '
description: 應用程式會傳送 WM \_ CHANGEUISTATE 訊息，以指出應變更 UI 狀態。
ms.assetid: d8dfc2fe-c64f-4e7e-b021-127aa85d5dd6
keywords:
- WM_CHANGEUISTATE 訊息功能表和其他資源
topic_type:
- apiref
api_name:
- WM_CHANGEUISTATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cdfec2a26b3b3d160d3d207c338c8ebecd32bf2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686468"
---
# <a name="wm_changeuistate-message"></a>WM \_ CHANGEUISTATE 訊息

應用程式會傳送 **WM \_ CHANGEUISTATE** 訊息，以指出應變更 UI 狀態。


```C++
#define WM_CHANGEUISTATE                0x0127
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

低序位字組指定要採取的動作。 這個成員可以是下列其中一個值。



| 值                                                                                                                                                                                                                   | 意義                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="UIS_CLEAR"></span><span id="uis_clear"></span><dl> <dt>**Ui \_清除**</dt> <dt>2</dt> </dl>                | 高序位字組指定的 UI 狀態旗標應予以清除。<br/>                                                                  |
| <span id="UIS_INITIALIZE"></span><span id="uis_initialize"></span><dl> <dt>**Ui \_初始化**</dt> <dt>3</dt> </dl> | 高序位字組指定的 UI 狀態旗標應根據最後一個輸入事件來變更。 如需詳細資訊，請參閱＜備註＞。<br/> |
| <span id="UIS_SET"></span><span id="uis_set"></span><dl> <dt>**Ui \_設定**</dt> <dt>1</dt> </dl>                      | 應設定高序位字組所指定的 UI 狀態旗標。<br/>                                                                      |



 

高序位單字可指定受影響的 UI 狀態元素或控制項的樣式。 這個成員可以是下列一或多個值。



| 值                                                                                                                                                                                                                     | 意義                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="UISF_ACTIVE"></span><span id="uisf_active"></span><dl> <dt>**UISF \_現用**</dt> <dt>0x4</dt> </dl>          | 控制項應以用於作用中控制項的樣式來繪製。<br/> |
| <span id="UISF_HIDEACCEL"></span><span id="uisf_hideaccel"></span><dl> <dt>**UISF \_HIDEACCEL**</dt> <dt>0x2</dt> </dl> | 鍵盤快捷為隱藏。<br/>                                |
| <span id="UISF_HIDEFOCUS"></span><span id="uisf_hidefocus"></span><dl> <dt>**UISF \_HIDEFOCUS**</dt> <dt>0x1</dt> </dl> | 焦點指標是隱藏的。<br/>                                     |



 

</dd> <dt>

*lParam* 
</dt> <dd>

未使用此參數，且必須為0。

</dd> </dl>

## <a name="remarks"></a>備註

當視窗必須變更相同階層中所有視窗的 UI 狀態專案時，應該將此訊息傳送至本身或其父代。 視窗程式必須讓 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 處理此訊息，讓整個視窗樹狀結構具有一致的 UI 狀態。 當最上層視窗收到 **wm \_ CHANGEUISTATE** 訊息時，會將具有相同參數的 [**WM \_ UPDATEUISTATE**](wm-updateuistate.md) 訊息傳送至所有子視窗。 當系統處理 **WM \_ UPDATEUISTATE** 訊息時，它會在 UI 狀態下進行變更。

如果 *wParam* 的低序位文字是 ui \_ 初始化，系統會根據最後一個輸入事件，傳送具有 UI 狀態的 [**WM \_ UPDATEUISTATE**](wm-updateuistate.md) 訊息。 例如，如果最後一個輸入來自滑鼠，系統將會隱藏鍵盤提示。而且，如果最後輸入來自鍵盤，系統將會顯示鍵盤提示。如果處理 **WM \_ CHANGEUISTATE** 所產生的狀態與舊狀態相同， [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 就不會傳送此訊息。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**WM \_ QUERYUISTATE**](wm-queryuistate.md)
</dt> <dt>

**概念**
</dt> <dt>

[鍵盤加速器](keyboard-accelerators.md)
</dt> </dl>

 


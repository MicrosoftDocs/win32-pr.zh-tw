---
title: 'WM_UPDATEUISTATE 訊息 (Winuser .h) '
description: 應用程式會傳送 WM \_ UPDATEUISTATE 訊息，以變更指定之視窗及其所有子視窗的 UI 狀態。
ms.assetid: cbdeeddd-59b2-4a73-bfe9-17647d32bcf3
keywords:
- WM_UPDATEUISTATE 訊息功能表和其他資源
topic_type:
- apiref
api_name:
- WM_UPDATEUISTATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 351770019f18c52c4ff1588a09c803d07f0f58ce032b35af53501ff4e47b6aed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112858"
---
# <a name="wm_updateuistate-message"></a>WM \_ UPDATEUISTATE 訊息

應用程式會傳送 **WM \_ UPDATEUISTATE** 訊息，以變更指定之視窗及其所有子視窗的 UI 狀態。


```C++
#define WM_UPDATEUISTATE                0x0128
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

低序位字組指定要執行的動作。 此參數可以是下列其中一個值。



| 值                                                                                                                                                                                                                   | 意義                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="UIS_CLEAR"></span><span id="uis_clear"></span><dl> <dt>**Ui \_清除**</dt> <dt>2</dt> </dl>                | 高序位字組指定的 UI 狀態元素應該是隱藏的。<br/>                                                                   |
| <span id="UIS_INITIALIZE"></span><span id="uis_initialize"></span><dl> <dt>**Ui \_初始化**</dt> <dt>3</dt> </dl> | 高序位字組指定的 UI 狀態元素應根據最後一個輸入事件來變更。 如需詳細資訊，請參閱＜備註＞。<br/> |
| <span id="UIS_SET"></span><span id="uis_set"></span><dl> <dt>**Ui \_設定**</dt> <dt>1</dt> </dl>                      | 高序位字組所指定的 UI 狀態元素應該是可見的。<br/>                                                                  |



 

高序位單字可指定受影響的 UI 狀態元素或控制項的樣式。 這個參數可以是下列一或多個值。



| 值                                                                                                                                                                                                                     | 意義                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="UISF_ACTIVE"></span><span id="uisf_active"></span><dl> <dt>**UISF \_現用**</dt> <dt>0x4</dt> </dl>          | 控制項應以用於作用中控制項的樣式來繪製。<br/> |
| <span id="UISF_HIDEACCEL"></span><span id="uisf_hideaccel"></span><dl> <dt>**UISF \_HIDEACCEL**</dt> <dt>0x2</dt> </dl> | 鍵盤加速器。<br/>                                           |
| <span id="UISF_HIDEFOCUS"></span><span id="uisf_hidefocus"></span><dl> <dt>**UISF \_HIDEFOCUS**</dt> <dt>0x1</dt> </dl> | 焦點指標。<br/>                                                |



 

</dd> <dt>

*lParam* 
</dt> <dd>

不使用這個參數。

</dd> </dl>

## <a name="remarks"></a>備註

視窗應該會傳送此訊息來變更其所有子視窗的 UI 狀態。 相對於 [**wm \_ CHANGEUISTATE**](wm-changeuistate.md) 訊息（也就是通知），當 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 處理 **WM \_ UPDATEUISTATE** 訊息時，它會變更 UI 狀態，並將變更傳播到所有的子視窗。

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)函式會根據 *WPARAM* 值更新 UI 狀態。 如果 UI 狀態已修改，則函式會將訊息傳送至所有的直屬子視窗。 **DefWindowProc** 也會在收到 [**WM \_ CHANGEUISTATE**](wm-changeuistate.md) 訊息時傳送此訊息，通知系統子視窗要修改 UI 狀態。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**WM \_ CHANGEUISTATE**](wm-changeuistate.md)
</dt> <dt>

[**WM \_ QUERYUISTATE**](wm-queryuistate.md)
</dt> <dt>

**概念**
</dt> <dt>

[鍵盤加速器](keyboard-accelerators.md)
</dt> </dl>

 


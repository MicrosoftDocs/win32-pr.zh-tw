---
title: 'MCI_WINDOW 命令 (Mmsystem .h) '
description: MCI \_ 視窗命令可指定圖形裝置的視窗和視窗特性。 數位影片和影片重迭裝置會辨識此命令。
ms.assetid: 8b6c4d9a-ee72-4c64-aebe-6c8153167496
keywords:
- MCI_WINDOW 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_WINDOW
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3270dce8b2127cce783c7c3b8bf21102590cd3e82d74a3e990a3117c59772381
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119783688"
---
# <a name="mci_window-command"></a>MCI \_ 視窗命令

MCI \_ 視窗命令可指定圖形裝置的視窗和視窗特性。 數位影片和影片重迭裝置會辨識此命令。

若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_WINDOW, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpWindow
);
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*
</dt> <dd>

要接收命令訊息之 MCI 裝置的裝置識別碼。

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*
</dt> <dd>

\_ \_ 適用于數位視訊裝置、mci 測試的 mci 通知、mci 等待或 \_ 。 如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。

</dd> <dt>

<span id="lpWindow"></span><span id="lpwindow"></span><span id="LPWINDOW"></span>*lpWindow*
</dt> <dd>

[**MCI \_ 泛型 \_ PARMS**](mci-generic-parms.md)結構的指標。 具有擴充命令集的 (裝置，可能會以裝置特定結構取代此結構。 ) 

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回零，否則會傳回錯誤。

## <a name="remarks"></a>備註

圖形裝置應該在裝置開啟時建立預設視窗，但在收到 [MCI \_ PLAY](mci-play.md) 命令之前不應該顯示。 您可以 \_ 使用 [MCI 視窗] 命令，將應用程式建立的視窗提供給裝置，以及變更應用程式定義或預設顯示視窗的顯示特性。 如果應用程式提供顯示視窗，則應該準備好在視窗上更新不正確矩形。

下列其他旗標適用于 **digitalvideo** 裝置類型：

<dl> <dt>

<span id="MCI_DGV_WINDOW_HWND"></span><span id="mci_dgv_window_hwnd"></span>MCI \_ DGV \_ 視窗 \_ HWND
</dt> <dd>

使用做為目的地的視窗控制碼包含在 *lpWindow* 所識別之結構的 **hWnd** 成員中。

</dd> <dt>

<span id="MCI_DGV_WINDOW_STATE"></span><span id="mci_dgv_window_state"></span>MCI \_ DGV \_ 視窗 \_ 狀態
</dt> <dd>

*LpWindow* 所識別之結構的 **nCmdShow** 成員包含設定視窗狀態的參數。

</dd> <dt>

<span id="MCI_DGV_WINDOW_TEXT"></span><span id="mci_dgv_window_text"></span>MCI \_ DGV \_ 視窗 \_ 文字
</dt> <dd>

*LpWindow* 所識別之結構的 **lpstrText** 成員包含緩衝區的位址，其中包含視窗標題列中所使用的標題。

</dd> </dl>

針對數位影片裝置， *lpWindow* 參數會指向 [**MCI \_ DGV \_ 視窗 \_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_window_parmsa) 結構。

下列其他旗標會搭配覆迭 **裝置類型** 使用：

<dl> <dt>

<span id="MCI_OVLY_WINDOW_DISABLE_STRETCH"></span><span id="mci_ovly_window_disable_stretch"></span>MCI \_ OVLY \_ 視窗 \_ 停用 \_ STRETCH
</dt> <dd>

停用影像的延展。

</dd> <dt>

<span id="MCI_OVLY_WINDOW_ENABLE_STRETCH"></span><span id="mci_ovly_window_enable_stretch"></span>MCI \_ OVLY \_ 視窗 \_ 啟用 \_ 延展
</dt> <dd>

啟用延展影像。

</dd> <dt>

<span id="MCI_OVLY_WINDOW_HWND"></span><span id="mci_ovly_window_hwnd"></span>MCI \_ OVLY \_ 視窗 \_ HWND
</dt> <dd>

用於目的地的視窗控制碼會包含在 *lpWindow* 所識別之結構的 **hWnd** 成員中。 將此旗標設定為 MCI \_ OVLY \_ window \_ default，以返回預設視窗。

</dd> <dt>

<span id="MCI_OVLY_WINDOW_STATE"></span><span id="mci_ovly_window_state"></span>MCI \_ OVLY \_ 視窗 \_ 狀態
</dt> <dd>

*LpWindow* 結構的 **nCmdShow** 成員包含設定視窗狀態的參數。 此旗標相當於以 *state* 參數呼叫 [ShowWindow](/windows/win32/api/winuser/nf-winuser-showwindow) 。 這些常數與 WINDOWS 中定義的常數相同。H (例如 SW \_ HIDE、sw \_ 最小化或 sw \_ SHOWNORMAL) 。

</dd> <dt>

<span id="MCI_OVLY_WINDOW_TEXT"></span><span id="mci_ovly_window_text"></span>MCI \_ OVLY \_ 視窗 \_ 文字
</dt> <dd>

*LpWindow* 所識別之結構的 **lpstrText** 成員包含緩衝區的位址，其中包含用於視窗的標題。

</dd> </dl>

針對影片重迭裝置， *lpWindow* 參數會指向 [**MCI \_ OVLY \_ 視窗 \_ PARMS**](mci-ovly-window-parms.md) 結構。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Mmsystem (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[MCI 命令](mci-commands.md)
</dt> </dl>

 


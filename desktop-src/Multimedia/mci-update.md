---
title: 'MCI_UPDATE 命令 (Mmsystem .h) '
description: MCI \_ UPDATE 命令會更新顯示矩形。 數位影片裝置辨識此命令。
ms.assetid: 90a8c10f-61b9-49a1-bbcc-e0729aa8c454
keywords:
- MCI_UPDATE 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_UPDATE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 423186096c88a8f1ff74987ff57c6b49dc6c3131
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105911"
---
# <a name="mci_update-command"></a>MCI \_ 更新命令

MCI \_ UPDATE 命令會更新顯示矩形。 數位影片裝置辨識此命令。

若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_UPDATE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpDest
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

**MCI \_通知**、 **mci \_ 等候**，或適用于數位影片裝置、 **mci \_ 測試**。 如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。

</dd> <dt>

<span id="lpDest"></span><span id="lpdest"></span><span id="LPDEST"></span>*lpDest*
</dt> <dd>

[**MCI \_ 泛型 \_ PARMS**](mci-generic-parms.md)結構的指標。 具有擴充命令集的 (裝置，可能會以裝置特定結構取代此結構。 ) 

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回零，否則會傳回錯誤。

## <a name="remarks"></a>備註

下列其他旗標會搭配 "digitalvideo" 裝置類型使用：

<dl> <dt>

<span id="MCI_DGV_UPDATE_HDC"></span><span id="mci_dgv_update_hdc"></span>MCI \_ DGV \_ UPDATE \_ HDC
</dt> <dd>

*LpDest* 所識別之結構的 **hDC** 成員包含要繪製之 DC 的有效視窗。 此為必要旗標。

</dd> <dt>

<span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>MCI \_ DGV \_ RECT
</dt> <dd>

*LpUnfreeze* 所識別之結構的 **rc** 成員包含有效的顯示矩形。 矩形會指定相對於用戶端矩形的裁剪矩形。

</dd> <dt>

<span id="MCI_DGV_UPDATE_PAINT"></span><span id="mci_dgv_update_paint"></span>MCI \_ DGV \_ 更新 \_ 繪圖
</dt> <dd>

當應用程式收到適用于顯示 DC 的 [**WM \_ 油漆**](/windows/desktop/gdi/wm-paint) 訊息時，會使用此旗標。 框架緩衝區裝置通常會繪製按鍵色彩。 如果顯示裝置沒有框架緩衝區，則 \_ 使用 **mci \_ DGV \_ update \_ 油漆** 旗標時，可能會忽略 mci UPDATE 命令，因為播放作業期間會重新繪製顯示器。

</dd> </dl>

針對數位影片裝置， *lpDest* 參數會指向 [**MCI \_ DGV \_ 更新 \_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_update_parms) 結構。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Mmsystem (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Mci](mci.md)
</dt> <dt>

[MCI 命令](mci-commands.md)
</dt> </dl>

 


---
title: 'MCI_WHERE 命令 (Mmsystem .h) '
description: MCI \_ ，其中命令可取得影片裝置的剪切矩形。
ms.assetid: f64a7e49-4ee1-4836-ba9a-0bbdc47626b3
keywords:
- MCI_WHERE 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_WHERE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6619131319863d1159a3bdb8bb85d366243544a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934434"
---
# <a name="mci_where-command"></a>MCI \_ WHERE 命令

MCI \_ ，其中命令可取得影片裝置的剪切矩形。 數位影片和影片重迭裝置會辨識此命令。 [傳回之矩形的](/previous-versions//ms536136(v=vs.85))**左上角** 和 **左方** 成員包含裁剪矩形的原點，**右邊** 和 **底部** 的成員則包含裁剪矩形的寬度和高度。  (這不是 **右邊** 和 **底部** 成員的標準使用。 ) 

若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_WHERE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpQuery
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

<span id="lpQuery"></span><span id="lpquery"></span><span id="LPQUERY"></span>*lpQuery*
</dt> <dd>

[**MCI \_ 泛型 \_ PARMS**](mci-generic-parms.md)結構的指標。 具有擴充命令集的 (裝置，可能會以裝置特定結構取代此結構。 ) 

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回零，否則會傳回錯誤。

## <a name="remarks"></a>備註

下列其他旗標適用于 **digitalvideo** 裝置類型：

<dl> <dt>

<span id="MCI_DGV_WHERE_DESTINATION"></span><span id="mci_dgv_where_destination"></span>\_ \_ 目的地的 MCI \_ DGV
</dt> <dd>

取得用來在目前視窗的工作區中顯示影片和影像的矩形區域描述。

</dd> <dt>

<span id="MCI_DGV_WHERE_FRAME"></span><span id="mci_dgv_where_frame"></span>MCI \_ DGV \_ WHERE \_ FRAME
</dt> <dd>

取得畫面格緩衝區矩形區域的描述，以縮放影片矩形中的影像。 矩形座標會放置在 *lpQuery* 所識別之結構的 **rc** 成員中。

</dd> <dt>

<span id="MCI_DGV_WHERE_MAX"></span><span id="mci_dgv_where_max"></span>MCI \_ DGV \_ ，其中 \_ 最大值
</dt> <dd>

搭配 \_ \_ \_ 目的地或 mci DGV 來源的 mci DGV 使用時 \_ \_ \_ ，傳回的矩形表示指定區域的最大寬度和高度。 與 MCI \_ DGV \_ （其中 \_ 的視窗）搭配使用時，傳回的矩形表示整個顯示器的大小。

</dd> <dt>

<span id="MCI_DGV_WHERE_SOURCE"></span><span id="mci_dgv_where_source"></span>\_DGV \_ 來源的 \_ MCI
</dt> <dd>

取得矩形區域的描述， (裁剪自框架緩衝區) ，該緩衝區會延展以符合顯示器上的目的地矩形。

</dd> <dt>

<span id="MCI_DGV_WHERE_VIDEO"></span><span id="mci_dgv_where_video"></span>MCI \_ DGV \_ ，其中 \_ 影片
</dt> <dd>

取得裁剪自展示來源之矩形區域的描述，以填滿框架緩衝區中的框架矩形。 矩形座標會放置在 *lpQuery* 所識別之結構的 **rc** 成員中。

</dd> <dt>

<span id="MCI_DGV_WHERE_WINDOW"></span><span id="mci_dgv_where_window"></span>MCI \_ DGV \_ WHERE \_ WINDOW
</dt> <dd>

取得顯示視窗框架的描述。

</dd> <dt>


</dt> <dd></dd> </dl>

針對數位影片裝置， *lpQuery* 參數會指向 **PARMS 結構所在的 \_ MCI \_ DGV \_** 。 **Mci \_ DGV \_ ，其中 \_ PARMS** 結構等同于 [**mci \_ DGV \_ RECT \_ PARMS**](/windows/win32/api/digitalv/ns-digitalv-mci_dgv_rect_parms)結構。

下列其他旗標會搭配覆迭 **裝置類型** 使用：

<dl> <dt>

<span id="MCI_OVLY_WHERE_DESTINATION"></span><span id="mci_ovly_where_destination"></span>\_ \_ 目的地的 MCI \_ OVLY
</dt> <dd>

取得目的地顯示矩形。 矩形座標會放置在 *lpQuery* 所識別之結構的 **rc** 成員中。

</dd> <dt>

<span id="MCI_OVLY_WHERE_FRAME"></span><span id="mci_ovly_where_frame"></span>MCI \_ OVLY \_ WHERE \_ FRAME
</dt> <dd>

取得覆蓋框架矩形。 矩形座標會放置在 *lpQuery* 所識別之結構的 **rc** 成員中。

</dd> <dt>

<span id="MCI_OVLY_WHERE_SOURCE"></span><span id="mci_ovly_where_source"></span>\_OVLY \_ 來源的 \_ MCI
</dt> <dd>

取得來源矩形。 矩形座標會放置在 *lpQuery* 所識別之結構的 **rc** 成員中。

</dd> <dt>

<span id="MCI_OVLY_WHERE_VIDEO"></span><span id="mci_ovly_where_video"></span>MCI \_ OVLY \_ ，其中 \_ 影片
</dt> <dd>

取得影片矩形。 矩形座標會放置在 *lpQuery* 所識別之結構的 **rc** 成員中。

</dd> </dl>

針對影片重迭裝置， *lpQuery* 參數會指向 [**MCI \_ OVLY \_ RECT \_ PARMS**](mci-ovly-rect-parms.md) 結構。

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

 


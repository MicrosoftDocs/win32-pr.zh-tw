---
title: 'MCI_REALIZE 命令 (Mmsystem .h) '
description: MCI 的「 \_ 實現」命令會使圖形裝置將其選擇區實現到 (DC) 的裝置內容中。 數位影片裝置辨識此命令。
ms.assetid: cbc9e6ef-a372-4ddb-b7f3-ea99ac14ec95
keywords:
- MCI_REALIZE 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_REALIZE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e81204fe679d543438a0d0dcc7ec333462cb6a3d0c30212706969dc22a143df1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119689828"
---
# <a name="mci_realize-command"></a>MCI \_ 實現命令

MCI 的「 \_ 實現」命令會使圖形裝置將其選擇區實現到 (DC) 的裝置內容中。 數位影片裝置辨識此命令。

若要傳送此命令，請使用下列參數呼叫 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_REALIZE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpRealize
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

<span id="lpRealize"></span><span id="lprealize"></span><span id="LPREALIZE"></span>*lpRealize*
</dt> <dd>

[**MCI \_ 泛型 \_ PARMS**](mci-generic-parms.md)結構的指標。 具有擴充命令集的 (裝置，可能會以裝置特定結構取代此結構。 ) 

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回零，否則會傳回錯誤。

## <a name="remarks"></a>備註

當您的應用程式收到 [**WM \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) 訊息時，您應該使用此命令。

下列其他旗標會搭配 "digitalvideo" 裝置類型使用：

<dl> <dt>

<span id="MCI_DGV_REALIZE_BKGD"></span><span id="mci_dgv_realize_bkgd"></span>MCI \_ DGV \_ 實現 \_ BKGD
</dt> <dd>

將調色板視為背景調色板。

</dd> <dt>

<span id="MCI_DGV_REALIZE_NORM"></span><span id="mci_dgv_realize_norm"></span>MCI \_ DGV \_ 實現 \_ 標準
</dt> <dd>

正常地發現調色板。 此為預設值。

</dd> </dl>

針對數位影片裝置， *lpRealize* 參數會指向 **MCI \_ 實現 \_ PARMS** 結構。 如需詳細資訊，請參閱 [**MCI \_ 一般 \_ PARMS**](mci-generic-parms.md) 結構中的批註。

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

 


---
title: 'WM_CAP_GET_MCI_DEVICE 訊息 (Vfw .h) '
description: '[WM \_ cap \_ 取得 \_ mci \_ 裝置] 訊息會取出先前以 WM \_ CAP \_ SET \_ MCI \_ 裝置訊息設定的 MCI 裝置名稱。 您可以使用 capGetMCIDeviceName 宏明確地傳送此訊息。'
ms.assetid: c5d7d955-ab6a-4959-b79e-9ff35a282ba2
keywords:
- WM_CAP_GET_MCI_DEVICE message Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_GET_MCI_DEVICE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0960ff9aa1366802611f444383212c4bcc45bcb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464212"
---
# <a name="wm_cap_get_mci_device-message"></a>WM \_ CAP \_ 取得 \_ MCI \_ 裝置訊息

[ **Wm \_ cap \_ 取得 \_ mci \_ 裝置** ] 訊息會取出先前以 [**WM \_ CAP \_ set \_ MCI \_ 裝置**](wm-cap-set-mci-device.md) 訊息設定的 MCI 裝置名稱。 您可以使用 [**capGetMCIDeviceName**](/windows/desktop/api/Vfw/nf-vfw-capgetmcidevicename) 宏明確地傳送此訊息。


```C++
WM_CAP_GET_MCI_DEVICE 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*
</dt> <dd>

**>szname** 所參考的緩衝區長度（以位元組為單位）。

</dd> <dt>

<span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*>szname*
</dt> <dd>

包含 MCI 裝置名稱之以 null 結束的字串指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回 **TRUE** ，否則傳回 **FALSE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Vfw。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[影片捕獲](video-capture.md)
</dt> <dt>

[影片捕獲訊息](video-capture-messages.md)
</dt> </dl>

 

 






---
title: 'WM_CAP_GET_MCI_DEVICE 訊息 (Vfw .h) '
description: '[WM \_ cap \_ 取得 \_ mci \_ 裝置] 訊息會取出先前以 WM \_ CAP \_ SET \_ MCI \_ 裝置訊息設定的 MCI 裝置名稱。 您可以使用 capGetMCIDeviceName 宏明確地傳送此訊息。'
ms.assetid: c5d7d955-ab6a-4959-b79e-9ff35a282ba2
keywords:
- WM_CAP_GET_MCI_DEVICE 訊息 Windows 多媒體
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
ms.openlocfilehash: b9471177693bfbd5646d93e8487395cdf330b8281a1f43fa00d79dc690e6d718
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117800650"
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

**>Szname** 所參考的緩衝區長度（以位元組為單位）。

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

 

 






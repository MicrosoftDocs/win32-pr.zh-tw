---
title: 'WM_CAP_SET_MCI_DEVICE 訊息 (Vfw .h) '
description: '[WM \_ CAP \_ 設定 \_ MCI \_ 裝置訊息] 會指定要用來捕捉資料的 MCI video 裝置名稱。 您可以使用 capSetMCIDeviceName 宏明確地傳送此訊息。'
ms.assetid: 83fdf567-ceb2-45aa-8529-433a5c64ac0a
keywords:
- WM_CAP_SET_MCI_DEVICE message Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_SET_MCI_DEVICE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86187f3357bf72866e05b497332454c10bcd2fd3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685546"
---
# <a name="wm_cap_set_mci_device-message"></a>WM \_ CAP \_ 設定 \_ MCI \_ 裝置訊息

[ **WM \_ CAP \_ 設定 \_ MCI \_ 裝置** 訊息] 會指定要用來捕捉資料的 MCI video 裝置名稱。 您可以使用 [**capSetMCIDeviceName**](/windows/desktop/api/Vfw/nf-vfw-capsetmcidevicename) 宏明確地傳送此訊息。


```C++
WM_CAP_SET_MCI_DEVICE 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*>szname*
</dt> <dd>

以 null 結束的字串指標，其中包含裝置的名稱。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回 **TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

此訊息會將 MCI 裝置名稱儲存在內部結構中。 它不會開啟或存取裝置。 預設裝置名稱為 **Null**。

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

 

 






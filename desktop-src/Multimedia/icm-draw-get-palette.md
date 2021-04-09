---
title: 'ICM_DRAW_GET_PALETTE 訊息 (Vfw .h) '
description: ICM \_ 繪圖 \_ GET \_ 調色板訊息要求轉譯驅動程式傳回檔色板。
ms.assetid: 02a9df7d-e0b9-4bde-9cda-c36d2a10a23c
keywords:
- ICM_DRAW_GET_PALETTE message Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_DRAW_GET_PALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a03f3658d2a2653f940e18e9b82b7cc3d7690ad2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024711"
---
# <a name="icm_draw_get_palette-message"></a>ICM \_ 繪圖 \_ 取得 \_ 調色板訊息

**ICM \_ 繪圖 \_ GET \_ 調色板** 訊息要求轉譯驅動程式傳回檔色板。


```C++
ICM_DRAW_GET_PALETTE 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>傳回值

驅動程式應該會傳回下列其中一項：所使用之調色板的控制碼、 **Null** （如果沒有要傳回的控制碼）或 ICERR 不 \_ 支援調色板時不支援。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Vfw。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[影片壓縮管理員](video-compression-manager.md)
</dt> <dt>

[影片壓縮訊息](video-compression-messages.md)
</dt> </dl>

 

 






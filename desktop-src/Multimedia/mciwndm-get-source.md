---
title: 'MCIWNDM_GET_SOURCE 訊息 (Vfw .h) '
description: MCIWNDM \_ 取得 \_ 來源訊息會抓取來源矩形的座標，此來源矩形用於在播放期間裁剪 AVI 檔案的影像。 您可以使用 MCIWndGetSource 宏明確地傳送此訊息。
ms.assetid: d5f25926-5a3d-412e-8248-fbf307583757
keywords:
- MCIWNDM_GET_SOURCE message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_GET_SOURCE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85147182d06386efed73229fcdd6c75372244fd6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385025"
---
# <a name="mciwndm_get_source-message"></a>MCIWNDM \_ 取得 \_ 來源訊息

**MCIWNDM \_ 取得 \_ 來源** 訊息會抓取來源矩形的座標，此來源矩形用於在播放期間裁剪 AVI 檔案的影像。 您可以使用 [**MCIWndGetSource**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetsource) 宏明確地傳送此訊息。


```C++
MCIWNDM_GET_SOURCE 
wParam = 0; 
lParam = (LPARAM) (LPRECT) prc; 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="prc"></span><span id="PRC"></span>*中國*
</dt> <dd>

[**矩形**](/previous-versions//dd162897(v=vs.85))結構的指標，包含來源矩形的座標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回零，否則會傳回錯誤。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Vfw。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MCIWndGetSource**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetsource)
</dt> </dl>

 


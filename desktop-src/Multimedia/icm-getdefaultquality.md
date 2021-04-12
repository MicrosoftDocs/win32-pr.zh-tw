---
title: 'ICM_GETDEFAULTQUALITY 訊息 (Vfw .h) '
description: ICM \_ GETDEFAULTQUALITY 訊息會查詢視訊壓縮驅動程式，以提供其預設品質設定。 您可以使用 ICGetDefaultQuality 宏明確地傳送此訊息。
ms.assetid: bba7f451-52c2-4684-a7c9-e4b05cb946c5
keywords:
- ICM_GETDEFAULTQUALITY message Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_GETDEFAULTQUALITY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4350539851ca720e3538d297f955a56fedfc4a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464629"
---
# <a name="icm_getdefaultquality-message"></a>ICM \_ GETDEFAULTQUALITY 訊息

**ICM \_ GETDEFAULTQUALITY** 訊息會查詢視訊壓縮驅動程式，以提供其預設品質設定。 您可以使用 [**ICGetDefaultQuality**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultquality) 宏明確地傳送此訊息。


```C++
ICM_GETDEFAULTQUALITY 
wParam = (DWORD_PTR) (LPVOID) &dwICValue; 
lParam = 0; 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*dwICValue*
</dt> <dd>

包含預設品質值的位址。 品質值的範圍是從0到10000。

</dd> </dl>

## <a name="return-value"></a>傳回值

\_如果驅動程式支援此訊息或 ICERR 不支援，則會傳回 ICERR OK \_ 。

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

 

 






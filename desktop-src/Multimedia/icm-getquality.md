---
title: 'ICM_GETQUALITY 訊息 (Vfw .h) '
description: ICM 的 \_ GETQUALITY 訊息會查詢視訊壓縮驅動程式，以傳回其目前的品質設定。
ms.assetid: 8da99a26-7b2a-4118-89e1-7485915cbdc9
keywords:
- ICM_GETQUALITY 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_GETQUALITY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cef214fe36c713e63659fcbd4dde2021c8d410b36ea9f5525ed54c76c5c4b6a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119495858"
---
# <a name="icm_getquality-message"></a>ICM \_GETQUALITY 訊息

**ICM 的 \_ GETQUALITY** 訊息會查詢視訊壓縮驅動程式，以傳回其目前的品質設定。


```C++
ICM_GETQUALITY 
wParam = (DWORD) (LPVOID) &dwICValue; 
lParam = 0; 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*dwICValue*
</dt> <dd>

包含目前品質值的位址。 品質值的範圍是從0到10000。

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

 

 






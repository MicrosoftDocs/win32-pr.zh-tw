---
title: 'ICM_GETDEFAULTKEYFRAMERATE 訊息 (Vfw .h) '
description: ICM 的 \_ GETDEFAULTKEYFRAMERATE 訊息會查詢視訊壓縮驅動程式，以取得其預設 (或慣用) 的主要畫面格間距。 您可以使用 ICGetDefaulteyFrameRate 宏明確地傳送此訊息。
ms.assetid: 2ebe37cc-3ec2-4b52-bd8f-71c44b704647
keywords:
- ICM_GETDEFAULTKEYFRAMERATE 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_GETDEFAULTKEYFRAMERATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bff21682f08dfdcda120f5efb5f7f8629a9e93e21faaf27ff4ee9ee59da8c762
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038698"
---
# <a name="icm_getdefaultkeyframerate-message"></a>ICM \_GETDEFAULTKEYFRAMERATE 訊息

**ICM 的 \_ GETDEFAULTKEYFRAMERATE** 訊息會查詢視訊壓縮驅動程式，以取得其預設 (或慣用) 的主要畫面格間距。 您可以使用 [**ICGetDefaulteyFrameRate**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultkeyframerate) 宏明確地傳送此訊息。


```C++
ICM_GETDEFAULTKEYFRAMERATE 
wParam = (DWORD_PTR) (LPVOID) &dwICValue; 
lParam = 0; 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*dwICValue*
</dt> <dd>

要包含慣用主要畫面格間距的位址。

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

 

 






---
title: 'MCIWNDM_GETSTART 訊息 (Vfw .h) '
description: MCIWNDM \_ GETSTART 訊息會抓取 MCI 裝置或檔案的內容開頭位置。 您可以使用 MCIWndGetStart 宏明確地傳送此訊息。
ms.assetid: 2350616c-2aac-4ff6-b074-bb785a97cdfb
keywords:
- MCIWNDM_GETSTART 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_GETSTART
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0efb5689009fdd6928afd1d2f232bcb1bbeb2160aecf3d79ddb263ed6f315de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119429228"
---
# <a name="mciwndm_getstart-message"></a>MCIWNDM \_ GETSTART 訊息

**MCIWNDM \_ GETSTART** 訊息會抓取 MCI 裝置或檔案的內容開頭位置。 您可以使用 [**MCIWndGetStart**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart) 宏明確地傳送此訊息。


```C++
MCIWNDM_GETSTART 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>傳回值

傳回目前時間格式的位置。

## <a name="remarks"></a>備註

通常，傳回值為零。但有些裝置使用非零的起始位置。 搜尋此位置會將裝置設定為媒體的開頭。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Vfw。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MCIWndGetStart**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart)
</dt> </dl>

 

 






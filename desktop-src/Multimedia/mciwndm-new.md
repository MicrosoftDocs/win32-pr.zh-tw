---
title: 'MCIWNDM_NEW 訊息 (Vfw .h) '
description: MCIWNDM \_ NEW message 會為目前的 MCI 裝置建立新的檔案。 您可以使用 MCIWndNew 宏明確地傳送此訊息。
ms.assetid: 18b2340d-8303-415a-867f-bd346034db2a
keywords:
- MCIWNDM_NEW 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_NEW
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bca9c03aff08c07f3ab1d8337547de776aeab5c6623a34ddaa71bfada0bca4f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119783078"
---
# <a name="mciwndm_new-message"></a>MCIWNDM \_ 新訊息

**MCIWNDM \_ NEW** message 會為目前的 MCI 裝置建立新的檔案。 您可以使用 [**MCIWndNew**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew) 宏明確地傳送此訊息。


```C++
MCIWNDM_NEW 
wParam = 0; 
lParam = (LPARAM) (LPVOID) lp; 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="lp"></span><span id="LP"></span>*Lp*
</dt> <dd>

緩衝區的指標，其中包含將使用該檔案之 MCI 裝置的名稱。

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

[**MCIWndNew**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew)
</dt> </dl>

 

 






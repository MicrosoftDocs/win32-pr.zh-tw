---
title: 'MCIWNDM_OPENINTERFACE 訊息 (Vfw .h) '
description: MCIWNDM \_ OPENINTERFACE 訊息會將與指定介面相關聯的資料流程或檔案附加至 MCIWnd 視窗。 您可以使用 MCIWndOpenInterface 宏明確地傳送此訊息。
ms.assetid: 73cbd637-d315-4b39-a978-2b72aed1f303
keywords:
- MCIWNDM_OPENINTERFACE message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_OPENINTERFACE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c40453f4d587429508a5aae19bc432fc46088ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383849"
---
# <a name="mciwndm_openinterface-message"></a>MCIWNDM \_ OPENINTERFACE 訊息

**MCIWNDM \_ OPENINTERFACE** 訊息會將與指定介面相關聯的資料流程或檔案附加至 MCIWnd 視窗。 您可以使用 [**MCIWndOpenInterface**](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface) 宏明確地傳送此訊息。


```C++
MCIWNDM_OPENINTERFACE 
wParam = 0; 
lParam = (LPARAM) (LPUNKNOWN) pUnk; 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="pUnk"></span><span id="punk"></span><span id="PUNK"></span>*朋 克*
</dt> <dd>

指向檔案中的檔案或資料流程的 IAVI 介面指標。

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

[**MCIWndOpenInterface**](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface)
</dt> </dl>

 

 






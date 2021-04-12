---
title: 'MCIWNDM_GETLENGTH 訊息 (Vfw .h) '
description: MCIWNDM \_ GETLENGTH 訊息會抓取 MCI 裝置目前所使用的內容或檔案的長度。 您可以使用 MCIWndGetLength 宏明確地傳送此訊息。
ms.assetid: bee4d9fc-78eb-4577-98bb-d6c2d9acbb7f
keywords:
- MCIWNDM_GETLENGTH message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_GETLENGTH
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2347647fcff0beb87be12b7f6a05790b97f36d51
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464516"
---
# <a name="mciwndm_getlength-message"></a>MCIWNDM \_ GETLENGTH 訊息

**MCIWNDM \_ GETLENGTH** 訊息會抓取 MCI 裝置目前所使用的內容或檔案的長度。 您可以使用 [**MCIWndGetLength**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetlength) 宏明確地傳送此訊息。


```C++
MCIWNDM_GETLENGTH 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>傳回值

傳回長度。 長度的單位取決於目前的時間格式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Vfw。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MCIWndGetLength**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetlength)
</dt> </dl>

 

 






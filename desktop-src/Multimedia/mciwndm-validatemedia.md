---
title: 'MCIWNDM_VALIDATEMEDIA 訊息 (Vfw .h) '
description: MCIWNDM \_ VALIDATEMEDIA 訊息會根據目前時間格式，更新內容的開始和結束位置、內容中的目前位置，以及顯示的內容。
ms.assetid: 98ac6227-fc90-4276-8e26-2bd005e35dc6
keywords:
- MCIWNDM_VALIDATEMEDIA message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_VALIDATEMEDIA
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43cb6e6a4a7c320d4eb6472c3c72da2843d0814c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508331"
---
# <a name="mciwndm_validatemedia-message"></a>MCIWNDM \_ VALIDATEMEDIA 訊息

**MCIWNDM \_ VALIDATEMEDIA** 訊息會根據目前時間格式，更新內容的開始和結束位置、內容中的目前位置，以及顯示的內容。 您可以使用 [**MCIWndValidateMedia**](/windows/desktop/api/Vfw/nf-vfw-mciwndvalidatemedia) 宏明確地傳送此訊息。


```C++
MCIWNDM_VALIDATEMEDIA 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>傳回值

此訊息不會傳回值。

## <a name="remarks"></a>備註

一般來說，您應該不需要使用這個宏。但是，如果您的應用程式在不使用 MCIWnd 的情況下變更裝置的時間格式;內容的開始和結束位置以及這些內容會繼續使用舊格式。 您可以使用這個宏來更新這些值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Vfw。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MCIWndValidateMedia**](/windows/desktop/api/Vfw/nf-vfw-mciwndvalidatemedia)
</dt> </dl>

 

 






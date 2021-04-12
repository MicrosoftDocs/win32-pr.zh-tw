---
title: 'MCIWNDM_RETURNSTRING 訊息 (Vfw .h) '
description: MCIWNDM \_ RETURNSTRING 訊息會將回復傳給傳送至 MCI 裝置的最新 mci 字串命令。
ms.assetid: 36a5222c-a63c-4b8c-ad0c-a00477e95b96
keywords:
- MCIWNDM_RETURNSTRING message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_RETURNSTRING
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b99307bd7d61a70db594d0a696cceccd6d246a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025068"
---
# <a name="mciwndm_returnstring-message"></a>MCIWNDM \_ RETURNSTRING 訊息

**MCIWNDM \_ RETURNSTRING** 訊息會將回復傳給傳送至 MCI 裝置的最新 mci 字串命令。 回復中的資訊是以 null 終止字串的形式提供。 您可以使用 [**MCIWndReturnString**](/windows/desktop/api/Vfw/nf-vfw-mciwndreturnstring) 宏明確地傳送此訊息。


```C++
MCIWNDM_RETURNSTRING 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPVOID) lp; 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="len"></span><span id="LEN"></span>*萊恩*
</dt> <dd>

緩衝區的大小（以位元組為單位）。

</dd> <dt>

<span id="lp"></span><span id="LP"></span>*Lp*
</dt> <dd>

應用程式定義的緩衝區指標，包含以 null 終止的字串。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回對應至 MCI 字串的整數。

## <a name="remarks"></a>備註

如果以 null 終止的字串比緩衝區長，則會截斷字串。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Vfw。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MCIWndReturnString**](/windows/desktop/api/Vfw/nf-vfw-mciwndreturnstring)
</dt> </dl>

 

 






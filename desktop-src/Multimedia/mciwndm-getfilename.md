---
title: 'MCIWNDM_GETFILENAME 訊息 (Vfw .h) '
description: MCIWNDM \_ GETFILENAME 訊息會抓取 MCI 裝置目前所使用的檔案名。 您可以使用 MCIWndGetFileName 宏明確地傳送此訊息。
ms.assetid: d61b1b6d-0fae-4732-993c-41e08a4e05be
keywords:
- MCIWNDM_GETFILENAME 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_GETFILENAME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17969bd05e321594a618d0ab712ae3fdec86f079d4415689f0b8f27b1000abf9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117802912"
---
# <a name="mciwndm_getfilename-message"></a>MCIWNDM \_ GETFILENAME 訊息

**MCIWNDM \_ GETFILENAME** 訊息會抓取 MCI 裝置目前所使用的檔案名。 您可以使用 [**MCIWndGetFileName**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetfilename) 宏明確地傳送此訊息。


```C++
MCIWNDM_GETFILENAME 
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

應用程式定義之緩衝區的指標，以傳回檔案名。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回零; 否則傳回1。

## <a name="remarks"></a>備註

如果包含檔案名的以 null 終止的字串長度超過緩衝區，MCIWnd 會截斷檔案名。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Vfw。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MCIWndGetFileName**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetfilename)
</dt> </dl>

 

 






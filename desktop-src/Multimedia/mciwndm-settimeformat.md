---
title: 'MCIWNDM_SETTIMEFORMAT 訊息 (Vfw .h) '
description: MCIWNDM \_ SETTIMEFORMAT 訊息會設定 MCI 裝置的時間格式。 您可以使用 MCIWndSetTimeFormat 宏明確地傳送此訊息。
ms.assetid: 7de82094-6d35-44fd-88e7-ebd18a558cfd
keywords:
- MCIWNDM_SETTIMEFORMAT 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_SETTIMEFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79620aecba07b11ed63dfc43fd2d70b41728586b36649b4b13aace9d1364197c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117802892"
---
# <a name="mciwndm_settimeformat-message"></a>MCIWNDM \_ SETTIMEFORMAT 訊息

**MCIWNDM \_ SETTIMEFORMAT** 訊息會設定 MCI 裝置的時間格式。 您可以使用 [**MCIWndSetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimeformat) 宏明確地傳送此訊息。


```C++
MCIWNDM_SETTIMEFORMAT 
wParam = 0; 
lParam = (LPARAM) (LPSTR) lp; 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="lp"></span><span id="LP"></span>*Lp*
</dt> <dd>

緩衝區的指標，其中包含表示時間格式的以 null 結束的字串。 指定「框架」以將時間格式設定為框架，或指定 "ms" 以將時間格式設定為毫秒。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回零，否則會傳回錯誤。

## <a name="remarks"></a>備註

只要 MCI 裝置支援這些格式，應用程式就可以指定框架或毫秒以外的時間格式。 Noncontinuous 格式（例如追蹤和 SMPTE）可能會導致追蹤的行為不穩定。 針對這些時間格式，您可能會想要使用 [**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) 宏和指定 MCIWNDF NOPLAYBAR 視窗樣式來關閉工具列 \_ 。

如果您想要將時間格式設定為框架或毫秒，您也可以使用 [**MCIWndUseFrames**](/windows/desktop/api/Vfw/nf-vfw-mciwnduseframes) 或 [**MCIWndUseTime**](/windows/desktop/api/Vfw/nf-vfw-mciwndusetime) 宏。 如需時間格式的清單，請參閱 [**MCIWndGetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat) 宏。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Vfw。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles)
</dt> <dt>

[**MCIWndGetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat)
</dt> <dt>

[**MCIWndSetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimeformat)
</dt> <dt>

[**MCIWndUseFrames**](/windows/desktop/api/Vfw/nf-vfw-mciwnduseframes)
</dt> <dt>

[**MCIWndUseTime**](/windows/desktop/api/Vfw/nf-vfw-mciwndusetime)
</dt> </dl>

 

 






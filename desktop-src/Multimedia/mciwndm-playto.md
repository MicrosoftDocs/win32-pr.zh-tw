---
title: 'MCIWNDM_PLAYTO 訊息 (Vfw .h) '
description: MCIWNDM \_ PLAYTO 訊息會從目前位置將 MCI 裝置的內容播放到指定的結束位置，或直到另一個命令停止播放為止。
ms.assetid: ed940ee7-7b96-47da-99d3-6697f8a2e3d5
keywords:
- MCIWNDM_PLAYTO 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_PLAYTO
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61004706c8dfacb05ad47c6ddf261ac813d58f5076dfdd4e134896b3f8c646e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037938"
---
# <a name="mciwndm_playto-message"></a>MCIWNDM \_ PLAYTO 訊息

**MCIWNDM \_ PLAYTO** 訊息會從目前位置將 MCI 裝置的內容播放到指定的結束位置，或直到另一個命令停止播放為止。 如果指定的結束位置超出內容的結尾，則會在內容結尾停止播放。 您可以使用 [**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto) 宏明確地傳送此訊息。


```C++
MCIWNDM_PLAYTO 
wParam = 0; 
lParam = (LPARAM) (LONG) lEnd; 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="lEnd"></span><span id="lend"></span><span id="LEND"></span>*借給*
</dt> <dd>

結束位置。 結束位置的單位取決於目前的時間格式。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回零，否則會傳回錯誤。

## <a name="remarks"></a>備註

這個宏是使用 [**MCIWndSeek**](/windows/desktop/api/Vfw/nf-vfw-mciwndseek) 和 [**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto) 宏來定義，接著使用 [MCI \_ SEEK](mci-seek.md) 命令和 **MCIWNDM \_ PLAYTO** 訊息。

您也可以使用 [**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto) 宏來指定播放的開始和結束位置。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Vfw。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[MCI \_ 搜尋](mci-seek.md)
</dt> <dt>

[**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto)
</dt> <dt>

[**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto)
</dt> <dt>

[**MCIWndSeek**](/windows/desktop/api/Vfw/nf-vfw-mciwndseek)
</dt> </dl>

 

 






---
title: 'MCIWNDM_GETPOSITION 訊息 (Vfw .h) '
description: MCIWNDM \_ GETPOSITION 訊息會抓取 MCI 裝置內容中目前位置的數值。
ms.assetid: 6dc5d3bd-8515-4514-a2a5-c1bee07f7acf
keywords:
- MCIWNDM_GETPOSITION 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_GETPOSITION
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83cf16f5945bfccbfd2f745ba22fac750f0536696aa2c4c06c2872bd318b263e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119525428"
---
# <a name="mciwndm_getposition-message"></a>MCIWNDM \_ GETPOSITION 訊息

**MCIWNDM \_ GETPOSITION** 訊息會抓取 MCI 裝置內容中目前位置的數值。 這個宏也會在應用程式定義的緩衝區中，以字串形式提供目前的位置。 您可以明確地傳送此訊息，或使用 [**MCIWndGetPosition**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetposition) 或 [**MCIWndGetPositionString**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpositionstring) 宏來傳送。


```C++
MCIWNDM_GETPOSITION 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPTSTR) lp; 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="len"></span><span id="LEN"></span>*萊恩*
</dt> <dd>

緩衝區的大小（以位元組為單位）。 如果以 null 結尾的字串長度超過緩衝區，它就會被截斷。 使用零可禁止將位置抓取為字串。

</dd> <dt>

<span id="lp"></span><span id="LP"></span>*Lp*
</dt> <dd>

用來傳回位置的應用程式定義緩衝區指標。 使用零可禁止將位置抓取為字串。 如果裝置支援追蹤，則會以 TT： MM： SS： FF 格式傳回字串位置資訊，其中 TT 對應至曲目，MM 和 SS 對應到分鐘和秒，而 FF 對應至框架。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回對應至目前位置的整數。 Position 值的單位取決於目前的時間格式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Vfw。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MCIWndGetPosition**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetposition)
</dt> <dt>

[**MCIWndGetPositionString**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpositionstring)
</dt> </dl>

 

 






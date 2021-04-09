---
title: 'MCIWNDM_GETTIMEFORMAT 訊息 (Vfw .h) '
description: MCIWNDM \_ GETTIMEFORMAT 訊息會以兩種形式，以數值和字串形式抓取 MCI 裝置目前的時間格式。 您可以使用 MCIWndGetTimeFormat 宏明確地傳送此訊息。
ms.assetid: 01844872-5444-4f3b-92a3-64f80b94d3a0
keywords:
- MCIWNDM_GETTIMEFORMAT message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_GETTIMEFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a09f969c009ff23bc0951ed2efbc0dbf7aa95dda
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685592"
---
# <a name="mciwndm_gettimeformat-message"></a>MCIWNDM \_ GETTIMEFORMAT 訊息

**MCIWNDM \_ GETTIMEFORMAT** 訊息會以兩種形式抓取 MCI 裝置的目前時間格式：作為數值和字串。 您可以使用 [**MCIWndGetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat) 宏明確地傳送此訊息。


```C++
MCIWNDM_GETTIMEFORMAT 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPSTR) lp; 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="len"></span><span id="LEN"></span>*萊恩*
</dt> <dd>

緩衝區的大小（以位元組為單位）。

</dd> <dt>

<span id="lp"></span><span id="LP"></span>*Lp*
</dt> <dd>

緩衝區的指標，包含時間格式以 null 終止的字串格式。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回對應于定義時間格式之 MCI 常數的整數。

## <a name="remarks"></a>備註

如果時間格式字串的長度超過傳回緩衝區，MCIWnd 會截斷字串。

MCI 裝置可支援下列一或多個時間格式。



| 時間格式                      | MCI 常數               |
|----------------------------------|----------------------------|
| 位元組                            | MCI \_ 格式 \_ 位元組         |
| 框架                           | MCI \_ 格式 \_ 框架        |
| 小時、分鐘、秒          | MCI \_ 格式 \_ HMS           |
| 毫秒                     | MCI \_ 格式 \_ 毫秒  |
| 分鐘、秒、框架         | MCI \_ 格式 \_ MSF           |
| 範例                          | MCI \_ 格式 \_ 範例       |
| SMPTE 24                         | MCI \_ 格式的 \_ SMPTE \_ 24     |
| SMPTE 25                         | MCI \_ 格式的 \_ SMPTE \_ 25     |
| SMPTE 30 下降                    | MCI \_ 格式的 \_ SMPTE \_ 30DROP |
| SMPTE 30 (非捨棄)               | MCI \_ 格式 \_ SMPTE \_ 30     |
| 曲目、分、秒、畫面格 | MCI \_ 格式 \_ TMSF          |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Vfw。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MCIWndGetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat)
</dt> </dl>

 

 






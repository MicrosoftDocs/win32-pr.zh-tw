---
title: 'MCIWNDM_GETMODE 訊息 (Vfw .h) '
description: MCIWNDM \_ GETMODE 訊息會抓取 MCI 裝置目前的作業模式。 MCI 裝置有數個作業模式，由常數指定。 您可以使用 MCIWndGetMode 宏明確地傳送此訊息。
ms.assetid: cc327281-434e-4047-9e15-c04a10953f47
keywords:
- MCIWNDM_GETMODE message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_GETMODE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5daefea2c550a1d0cf807ae03840c38ae8b2567c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104093791"
---
# <a name="mciwndm_getmode-message"></a>MCIWNDM \_ GETMODE 訊息

**MCIWNDM \_ GETMODE** 訊息會抓取 MCI 裝置目前的作業模式。 MCI 裝置有數個作業模式，由常數指定。 您可以使用 [**MCIWndGetMode**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetmode) 宏明確地傳送此訊息。


```C++
MCIWNDM_GETMODE 
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

用來傳回模式的應用程式定義緩衝區指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回對應于定義模式之 MCI 常數的整數。

## <a name="remarks"></a>備註

如果描述模式的以 null 終止的字串比緩衝區長，則會被截斷。

並非所有裝置都可以在每種模式下運作。 例如，MCIAVI 裝置是播放裝置;它不支援錄製模式。 您可以使用 **MCIWNDM \_ GETMODE** 來取出下列模式。



| 作業模式 | MCI 常數          |
|----------------|-----------------------|
| 未就緒      | MCI \_ 模式 \_ 未 \_ 就緒 |
| 開啟           | \_開啟 MCI 模式 \_       |
| 暫停 (paused)         | MCI \_ 模式 \_ 暫停      |
| 正在播放 (playing)        | MCI \_ 模式 \_ 播放       |
| 記錄      | MCI \_ 模式 \_ 記錄     |
| 搜尋        | MCI \_ 模式 \_ 搜尋       |
| 停止        | MCI \_ 模式 \_ 停止       |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Vfw。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MCIWndGetMode**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetmode)
</dt> </dl>

 

 






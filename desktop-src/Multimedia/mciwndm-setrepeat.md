---
title: 'MCIWNDM_SETREPEAT 訊息 (Vfw .h) '
description: MCIWNDM \_ SETREPEAT 訊息會設定與連續播放相關聯的重複旗標。
ms.assetid: 9a8da201-9ce8-4b6c-8b76-cd9e1356c75d
keywords:
- MCIWNDM_SETREPEAT message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_SETREPEAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aeae2ac3cb57f8ddbb2343ee3f42d30fa8def370
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843912"
---
# <a name="mciwndm_setrepeat-message"></a>MCIWNDM \_ SETREPEAT 訊息

**MCIWNDM \_ SETREPEAT** 訊息會設定與連續播放相關聯的重複旗標。 **MCIWNDM \_ SETREPEAT** 訊息會與 [MCI \_ PLAY](mci-play.md)命令搭配運作，以提供持續播放的迴圈。 您可以使用 [**MCIWndSetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetrepeat) 宏明確地傳送此訊息。


```C++
MCIWNDM_SETREPEAT 
wParam = 0; 
lParam = (LPARAM) (BOOL) f; 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="f"></span><span id="F"></span>*F*
</dt> <dd>

重複旗標的新狀態。 指定 **TRUE** 以開啟連續播放。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回零。

## <a name="remarks"></a>備註

目前，MCIAVI 是唯一支援連續播放的裝置。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Vfw。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[MCI \_ 播放](mci-play.md)
</dt> <dt>

[**MCIWndSetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetrepeat)
</dt> </dl>

 

 






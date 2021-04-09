---
title: 'ICM_DECOMPRESS 訊息 (Vfw .h) '
description: ICM \_ 解壓縮訊息會通知影片解壓縮驅動程式將資料框架解壓縮至應用程式定義的緩衝區。
ms.assetid: 666f2ebf-80a5-4846-861d-c79c3001c5a0
keywords:
- ICM_DECOMPRESS message Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c890a8ca15202f57fdaa02922e364af75f7b952
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025366"
---
# <a name="icm_decompress-message"></a>ICM \_ 解壓縮訊息

**ICM \_ 解壓縮** 訊息會通知影片解壓縮驅動程式將資料框架解壓縮至應用程式定義的緩衝區。


```C++
ICM_DECOMPRESS 
wParam = (DWORD) (LPVOID) &icd; 
lParam = sizeof(ICDECOMPRESS); 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="icd"></span><span id="ICD"></span>*Icd*
</dt> <dd>

[**ICDECOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-icdecompress)結構的指標。

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

[**ICDECOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-icdecompress)的大小（以位元組為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則會傳回 ICERR \_ OK，否則會傳回錯誤。

## <a name="remarks"></a>備註

如果您希望驅動程式將資料直接解壓縮到畫面，請傳送 [**ICM \_ 繪製**](icm-draw.md) 訊息。

如果在 [**ICM \_ 解壓縮 \_ 開始**](icm-decompress-begin.md) 訊息之前收到此訊息，驅動程式會傳回錯誤。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Vfw。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[影片壓縮管理員](video-compression-manager.md)
</dt> <dt>

[影片壓縮訊息](video-compression-messages.md)
</dt> </dl>

 

 






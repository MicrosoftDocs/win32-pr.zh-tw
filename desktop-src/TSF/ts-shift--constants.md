---
title: 'TS_SHIFT_ 常數 (Textstor) '
description: '\_ \_ IAnchor 介面會使用 TS Shift \ 常數來操作隱藏文字和字元計數。'
ms.assetid: 93329238-f6e8-432e-9167-550a02b33b46
topic_type:
- apiref
api_name:
- TS_SHIFT_COUNT_HIDDEN
- TS_SHIFT_HALT_HIDDEN
- TS_SHIFT_HALT_VISIBLE
- TS_SHIFT_COUNT_ONLY
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98f3a11463aea1633079d771bf6a8b333475865e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384694"
---
# <a name="ts_shift_-constants"></a>TS \_ 移位 \_ \* 常數

\_ \_ \* **IANCHOR** 介面會使用 TS 移位常數來操作隱藏文字和字元計數。



| 常數/值                                                                                                                                                                                                                                       | Description                                                                                                                                                                                                                                     |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_SHIFT_COUNT_HIDDEN"></span><span id="ts_shift_count_hidden"></span><dl> <dt>**TS \_SHIFT \_ COUNT \_ HIDDEN**</dt> <dt> ( 0x1 )</dt> </dl> | 指定錨點將移至下一個區域界限，包括隱藏文字區域的界限。 如果未設定，則會將錨點移到任何連續的隱藏文字之前，直到找到可見文字的區域為止。<br/> |
| <span id="TS_SHIFT_HALT_HIDDEN"></span><span id="ts_shift_halt_hidden"></span><dl> <dt>**TS \_SHIFT \_ 終止 \_ 隱藏**</dt> <dt> ( 0x2 )</dt> </dl>    | 未使用。<br/>                                                                                                                                                                                                                            |
| <span id="TS_SHIFT_HALT_VISIBLE"></span><span id="ts_shift_halt_visible"></span><dl> <dt>**TS \_SHIFT \_ 終止 \_ 可見**</dt> <dt> ( 0x4 )</dt> </dl> | 未使用。<br/>                                                                                                                                                                                                                            |
| <span id="TS_SHIFT_COUNT_ONLY"></span><span id="ts_shift_count_only"></span><dl> <dt>**TS \_移位 \_ 計數 \_ 只**</dt> <dt> ( 0x8 )</dt> </dl>       | 錨點不會移動。<br/>                                                                                                                                                                                                           |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                              |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                    |
| 可轉散發套件<br/>          | Windows 2000 Professional 上的 TSF 1。0<br/>                                         |
| 標頭<br/>                   | <dl> <dt>Textstor。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Textstor .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[IAnchor::ShiftRegion](/windows/desktop/api/Textstor/nf-textstor-ianchor-shiftregion)
</dt> </dl>

 

 






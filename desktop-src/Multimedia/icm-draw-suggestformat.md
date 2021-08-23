---
title: 'ICM_DRAW_SUGGESTFORMAT 訊息 (Vfw .h) '
description: ICM \_ DRAW \_ SUGGESTFORMAT 訊息會查詢轉譯驅動程式，以建議可繪製的解壓縮格式。
ms.assetid: e3e97790-dbd1-4436-9830-5218ae1f949b
keywords:
- ICM_DRAW_SUGGESTFORMAT 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_DRAW_SUGGESTFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 843dd2d398f5be6476a148922f3244113e94ab3fe3c10bac9ee08caefb8c4828
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119495947"
---
# <a name="icm_draw_suggestformat-message"></a>ICM \_繪製 \_ SUGGESTFORMAT 訊息

**ICM \_ DRAW \_ SUGGESTFORMAT** 訊息會查詢轉譯驅動程式，以建議可繪製的解壓縮格式。


```C++
ICM_DRAW_SUGGESTFORMAT 
wParam = (DWORD_PTR) (LPVOID) &icdrwSuggest; 
lParam = sizeof(ICDRAWSUGGEST); 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="icdrwSuggest"></span><span id="icdrwsuggest"></span><span id="ICDRWSUGGEST"></span>*icdrwSuggest*
</dt> <dd>

[**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest)結構的指標。

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

[**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest)的大小（以位元組為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

\_如果成功，則會傳回 ICERR OK。 如果 [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest)結構的 **LpbiSuggest** 成員是 **Null**，則此訊息會傳回包含建議格式所需的記憶體數量。

## <a name="remarks"></a>備註

驅動程式應該檢查 [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest)結構的 **lpbiIn** 成員中指定的格式，並使用 **lpbiSuggest** 成員傳回可繪製的格式。 輸出格式應盡可能保留輸入格式的最多資料。

（選擇性）驅動程式可以使用在 [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest)的 **hicDecompressor** 成員中傳遞的可安裝的壓縮程式控制碼，以進行更複雜的選取。 例如，如果輸入格式是24位 JPEG 資料，轉譯器可以查詢解壓縮程式以找出是否可以解壓縮至 YUV 格式 (在選取要建議的格式之前，) 可能會更有效率地繪製。

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

 

 






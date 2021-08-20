---
title: 'ICM_DECOMPRESSEX_BEGIN 訊息 (Vfw .h) '
description: ICM \_ DECOMPRESSEX \_ 開始訊息會通知影片壓縮驅動程式，準備將資料解壓縮。
ms.assetid: 35298274-91b5-4df0-b4b0-4a71d6a49990
keywords:
- ICM_DECOMPRESSEX_BEGIN 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_DECOMPRESSEX_BEGIN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffc74d5573437a1606db89377e36442b51677aca016cebd9635a0ab4f64cc55e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117987810"
---
# <a name="icm_decompressex_begin-message"></a>ICM \_DECOMPRESSEX \_ 開始訊息

**ICM \_ DECOMPRESSEX \_ 開始** 訊息會通知影片壓縮驅動程式，準備將資料解壓縮。


```C++
ICM_DECOMPRESSEX_BEGIN 
wParam = (DWORD_PTR) (LPVOID) &icdex; 
lParam = sizeof(ICDECOMPRESSEX); 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="icdex"></span><span id="ICDEX"></span>*icdex*
</dt> <dd>

[**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex)結構的指標，其中包含輸入和輸出格式。

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

[**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex)的大小（以位元組為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

\_如果支援指定的解壓縮或 ICERR BADFORMAT，則會傳回 ICERR OK （否則為） \_ 。

## <a name="remarks"></a>備註

當驅動程式收到此訊息時，它應該配置緩衝區並進行耗時的作業，以便有效率地處理 [**ICM 的 \_ DECOMPRESSEX**](icm-decompressex.md)訊息。

如果您希望驅動程式將資料直接解壓縮到畫面，請傳送 [**ICM \_ DRAW \_ BEGIN**](icm-draw-begin.md) message。

**ICM 的 \_ DECOMPRESSEX \_ 開始** 和 [**ICM \_ DECOMPRESSEX \_ 結束**](icm-decompressex-end.md)訊息不會被嵌套。 如果您的驅動程式收到 **ICM \_ DECOMPRESSEX \_** 在使用 **ICM \_ DECOMPRESSEX \_ 結束** 解壓縮之前停止，則應該以新的參數重新開機解壓縮。

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

 

 






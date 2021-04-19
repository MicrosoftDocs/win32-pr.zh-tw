---
title: 'ICM_DECOMPRESS_SET_PALETTE 訊息 (Vfw .h) '
description: 如果要 \_ 將 \_ \_ 影片解壓縮驅動程式解壓縮至使用調色板的格式，請使用 ICM 解壓縮設定的選擇區訊息。 您可以使用 ICDecompressSetPalette 宏明確地傳送此訊息。
ms.assetid: 269d01f9-b7c8-40e4-abdb-24dd0c9cc18d
keywords:
- ICM_DECOMPRESS_SET_PALETTE message Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS_SET_PALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f2bbbf1b09b8c5954a2149edd16cb213a08fb3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967558"
---
# <a name="icm_decompress_set_palette-message"></a>ICM \_ 解壓縮 \_ 設定的 \_ 調色板訊息

如果要將影片解壓縮驅動程式解壓縮至使用調色板的格式，請使用 **ICM \_ 解壓縮 \_ 設定 \_** 的選擇區訊息。 您可以使用 [**ICDecompressSetPalette**](/windows/desktop/api/Vfw/nf-vfw-icdecompresssetpalette) 宏明確地傳送此訊息。


```C++
ICM_DECOMPRESS_SET_PALETTE 
wParam = (DWORD_PTR) (LPVOID) lpbiPalette; 
lParam = 0; 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="lpbiPalette"></span><span id="lpbipalette"></span><span id="LPBIPALETTE"></span>*lpbiPalette*
</dt> <dd>

[**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85))結構的指標，其色彩表包含應該盡可能使用的色彩。 您可以指定零來使用一組預設的輸出色彩。

</dd> </dl>

## <a name="return-value"></a>傳回值

\_如果解壓縮驅動程式可以精確地將影像解壓縮至建議的調色板，請使用在選擇區中排列的色彩集合，以進行 ICERR 確定。 否則會傳回 \_ 不支援的 ICERR。

## <a name="remarks"></a>備註

此訊息不會影響正在進行的解壓縮;相反地，應該傳回使用此訊息傳遞的色彩，以回應未來的 [**ICM \_ 解壓縮 \_ 取得 \_ 格式**](icm-decompress-get-format.md) 和 [**ICM \_ 解壓縮 \_ 取得 \_**](icm-decompress-get-palette.md) 選擇區訊息。 在未來的 [**ICM \_ 解壓縮 \_ 開始**](icm-decompress-begin.md) 訊息中，色彩會傳送回解壓縮驅動程式。

此訊息主要是在驅動程式將影像解壓縮至螢幕，而另一個使用調色板的應用程式在前景時使用，以強制解壓縮驅動程式適應一組外部的色彩。

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

 


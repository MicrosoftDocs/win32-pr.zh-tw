---
description: 預設介面 stride，適用于未壓縮的影片媒體類型。 Stride 是從一個圖元到下一個資料列所需的位元組數目。
ms.assetid: 71fda231-3497-49db-b82e-2fd79f6ade66
title: 'MF_MT_DEFAULT_STRIDE 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e130918f62d6ff986ced7dd6449dcc2d381a00fc0d7c0342eeb4afcc03833bef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035236"
---
# <a name="mf_mt_default_stride-attribute"></a>MF \_ MT \_ 預設 \_ STRIDE 屬性

預設介面 stride，適用于未壓縮的影片媒體類型。 Stride 是從一個圖元到下一個資料列所需的位元組數目。

## <a name="data-type"></a>資料類型

**UINT32**

視為 **INT32** 值。

## <a name="remarks"></a>備註

屬性值會儲存為 **UINT32**，但應轉換成32位帶正負號的整數值。 Stride 可以是負數。

由上而下的影像而言，Stride 是正面的，而最下層的影像則為負數。

這個屬性會為記憶體中的影像的 *連續* 表示提供跨距，也就是在每個資料列之後，不含額外填補位元組的標記法。 如果媒體緩衝區支援 [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) 介面，請使用 [**IMF2DBuffer：： Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) 方法來取得介面的實際跨距，其中可能包含額外的填補位元組。

如需 surface stride 的詳細資訊，請參閱 [影像 stride](image-stride.md)。

如需如何計算預設 stride 的範例，請參閱 [未壓縮的視訊緩衝區](uncompressed-video-buffers.md)。

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | WindowsVista \[ desktop apps \| UWP 應用程式\]<br/>                              |
| 最低支援的伺服器<br/> | WindowsServer 2008 \[ desktop app \| UWP 應用程式\]<br/>                        |
| 標頭<br/>                   | <dl> <dt>Mfapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[媒體類型屬性](media-type-attributes.md)
</dt> <dt>

[影像 Stride](image-stride.md)
</dt> </dl>

 

 





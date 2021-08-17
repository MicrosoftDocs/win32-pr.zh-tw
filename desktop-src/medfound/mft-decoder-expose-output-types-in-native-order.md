---
description: 指定解碼器是否公開 IYUV/I420 輸出類型 (適用于其他格式之前的轉碼) 。
ms.assetid: 8505CFA1-210A-4DA8-B92A-FCE62F0310E5
title: 'MFT_DECODER_EXPOSE_OUTPUT_TYPES_IN_NATIVE_ORDER 屬性 (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46b91492054215aee5a63dbcf0adf300d74933a0859a2d71256e7e4352deba9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117872337"
---
# <a name="mft_decoder_expose_output_types_in_native_order-attribute"></a>MFT \_ 解碼 \_ 會 \_ \_ \_ 以 \_ 原生 \_ 順序屬性公開輸出類型

指定解碼器是否公開 IYUV/I420 輸出類型 (適用于其他格式之前的轉碼) 。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="remarks"></a>備註

這個屬性（attribute）是一種提示，可讓您根據預期的使用方式（播放或轉碼），以特定順序排列其輸出類型清單。

針對大部分的編碼格式 (h.264、MPEG-2、WMV) 、Microsoft 媒體基礎中的影片編碼器支援數個常見的 YUV 輸出，包括 NV12、YV12、YUY2、IYUV 和 I420。 此解碼器會透過其 [**IMFTransform：： GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) 方法，提供輸出類型的排序清單。

針對播放，NV12 是最有效率且廣泛支援的格式。 因此，根據預設，解碼器通常會提供 NV12 做為清單中的第一個輸出類型。 這可將在建立播放拓撲時解析媒體類型所需的時間降至最低。 不過，針對轉碼，IYUV 或 I420 對於 CPU 來說更有效率，而且通常是由編碼器所偏好。

如果解碼器支援這個屬性，屬性就會有下列行為：

-   如果屬性具有非零值，則 IYUV 和 I420 會先出現在輸出媒體類型清單中。 這項設定最有效率的轉碼。
-   如果屬性為零，NV12 會先出現在輸出媒體類型清單中。 這項設定最適合用來播放，而且是預設值。

若要設定此屬性：

1.  在解碼器上呼叫 [**IMFTransform：： GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) 來取得 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 指標。
2.  呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) 以加入屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[桌面應用程式 \| UWP 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                |
| 標頭<br/>                   | <dl> <dt>Mftransform。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 





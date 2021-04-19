---
description: 針對 YUV 媒體類型，定義從 YCbCr 色彩空間到 RGB 色彩空間的轉換矩陣。
ms.assetid: b268d16d-b4cc-4026-9ba7-805cc5409b95
title: 'MF_MT_YUV_MATRIX 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0c6976e4652c69b3bddc910dcc536a3d07bf39a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980508"
---
# <a name="mf_mt_yuv_matrix-attribute"></a>MF \_ MT \_ YUV \_ 矩陣屬性

針對 YUV 媒體類型，定義從 Y'Cb'Cr 的色彩空間到 R'G'B 的色彩空間的轉換矩陣。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="remarks"></a>備註

這個屬性的值是 [**MFVideoTransferMatrix**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideotransfermatrix) 列舉的成員。

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]<br/>                              |
| 最低支援的伺服器<br/> | Windows Server 2008 \[ desktop app \| UWP 應用程式\]<br/>                        |
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

[擴充的色彩資訊](extended-color-information.md)
</dt> </dl>

 

 





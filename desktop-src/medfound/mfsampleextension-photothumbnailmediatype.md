---
description: 包含描述 MFSampleExtension PhotoThumbnail 屬性中所包含之影像格式類型的 IMFMediaType \_ 。
ms.assetid: BA727189-385D-4BA1-9F17-AC6ECDD20ABF
title: 'MFSampleExtension_PhotoThumbnailMediaType 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77496340d598c7caf1064df0d3fc7e1ae7f112309bf6fbba6a66f3d5516e3828
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713598"
---
# <a name="mfsampleextension_photothumbnailmediatype-attribute"></a>MFSampleExtension \_ PhotoThumbnailMediaType 屬性

包含描述 [MFSampleExtension \_ PhotoThumbnail](mfsampleextension-photothumbnail.md)屬性中所包含之影像格式類型的 [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) 。

## <a name="data-type"></a>資料類型

以 **IMFMediaType** 儲存的 **IUnknown**

## <a name="remarks"></a>備註

如果照片範例中有 [MFSampleExtension \_ PhotoThumbnail](mfsampleextension-photothumbnail.md) 屬性，則需要 MFSampleExtension PhotoThumbnailMediaType， \_ 而且必須包含最小的 [mf \_ mt \_ 主要 \_ 類型](mf-mt-major-type-attribute.md)、 [mf \_ mt \_ 子類型](mf-mt-subtype-attribute.md) 和 [mf \_ mt \_ 框架 \_ 大小](mf-mt-frame-size-attribute.md) ，以描述縮圖。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1 \[桌面應用程式 \| UWP 應用程式\]<br/>                                |
| 最低支援的伺服器<br/> | Windows Server 2012R2 \[ desktop apps \| UWP 應用程式\]<br/>                     |
| 標頭<br/>                   | <dl> <dt>Mfapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[MFSampleExtension \_ PhotoThumbnail](mfsampleextension-photothumbnail.md)
</dt> </dl>

 

 





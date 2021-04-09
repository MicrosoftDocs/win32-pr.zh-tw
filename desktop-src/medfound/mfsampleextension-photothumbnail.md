---
description: 包含 IMFSample 的相片縮圖。
ms.assetid: 510706A3-92FB-4188-97B9-6E8E0B4B175F
title: 'MFSampleExtension_PhotoThumbnail 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5cbdb6f79b1b1ee187677a7f1a7a7792acb10fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115000"
---
# <a name="mfsampleextension_photothumbnail-attribute"></a>MFSampleExtension \_ PhotoThumbnail 屬性

包含 [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)的相片縮圖。

## <a name="data-type"></a>資料類型

以 **IMFMediaBuffer** 儲存的 **IUnknown**

縮圖會使用 **KSPROPERTYSETID \_ ExtendedCameraControl** 來設定。

## <a name="remarks"></a>備註

這個屬性是在 MFT0 所提供的 [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)上設定的，而且是與相片縮圖相關聯之 [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer)的 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。

相片縮圖的格式可以是 JPEG (主要類型影像) 、NV12 或 ARGB32。

縮圖需要 [MFSampleExtension \_ PhotoThumbnailMediaType](mfsampleextension-photothumbnailmediatype.md) 來描述媒體類型。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                |
| 最低支援的伺服器<br/> | Windows Server 2012 R2 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                     |
| 標頭<br/>                   | <dl> <dt>Mfapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> </dl>

 

 

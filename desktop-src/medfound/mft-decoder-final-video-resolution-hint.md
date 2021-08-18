---
description: 指定在視頻處理之後，解碼影像的最終輸出解析度。
ms.assetid: 067867D8-155C-4406-BE07-720016B2AEBC
title: 'MFT_DECODER_FINAL_VIDEO_RESOLUTION_HINT 屬性 (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 847a2925f2249c741e9a45a1dcc4826a1cbe3d6bb12cda4d8017ee0fb5de0069
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973137"
---
# <a name="mft_decoder_final_video_resolution_hint-attribute"></a>MFT \_ 解碼器 \_ 最終 \_ 影片 \_ 解析 \_ 提示屬性

指定在視頻處理之後，解碼影像的最終輸出解析度。

## <a name="data-type"></a>資料類型

**UINT64**

## <a name="remarks"></a>備註

部分影片解碼器支援此屬性。 應用程式可以設定此屬性，以指出影片處理之後影像的寬度和高度。 您可以使用這項資訊來優化解碼程式，特別是如果最終的映射大小遠小於原生映射大小。 例如，此解碼器可能會略過迴圈式篩選。

上方的32位包含寬度，而較低的32位則包含高度。

若要設定此屬性：

1.  在解碼器上呼叫 [**IMFTransform：： GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) 來取得 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 指標。
2.  呼叫 [**MFSetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributesize) 以加入屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[桌面應用程式 \| UWP 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                |
| 標頭<br/>                   | <dl> <dt>Mftransform。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[轉換屬性](transform-attributes.md)
</dt> </dl>

 

 





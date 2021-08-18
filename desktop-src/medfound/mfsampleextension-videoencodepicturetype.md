---
description: 指定影片編碼器輸出的圖片類型。
ms.assetid: 18A47033-3EAC-46C3-94AB-6ED20732F63C
title: 'MFSampleExtension_VideoEncodePictureType 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3be87284be3b605e3af70d64df98e5d762aa7cc353bb83b5f61a110d1242ae1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973167"
---
# <a name="mfsampleextension_videoencodepicturetype-attribute"></a>MFSampleExtension \_ VideoEncodePictureType 屬性

指定影片編碼器輸出的圖片類型。

## <a name="data-type"></a>資料類型

**eAVEncH264PictureType \_B** 儲存為 **UINT32**

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。

## <a name="applies-to"></a>適用於

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>備註

H.264 [**Video 編碼器**](h-264-video-encoder.md) 會在其產生的輸出範例上設定此屬性。 屬性的值是 [**eAVEncH264PictureType**](/windows/desktop/api/codecapi/ne-codecapi-eavench264picturetype) 列舉的成員。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[桌面應用程式 \| UWP 應用程式\]<br/>                                  |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Mfapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**H.264 影片編碼器**](h-264-video-encoder.md)
</dt> <dt>

[範例屬性](sample-attributes.md)
</dt> <dt>

[媒體範例](media-samples.md)
</dt> </dl>

 

 





---
description: 指出是否已將影片穩定套用至影片畫面。
ms.assetid: 13F877A3-7600-400F-9071-FE1B83027355
title: 'MFSampleExtension_VideoDSPMode 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95776fd7b8e130b9538e98843ca72d69980978b6f954747fadca939b8d3c5922
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119554928"
---
# <a name="mfsampleextension_videodspmode-attribute"></a>MFSampleExtension \_ VideoDSPMode 屬性

指出是否已將影片穩定套用至影片畫面。

## <a name="data-type"></a>資料類型

**MFVideoDSPMode** 儲存為 **UINT32**

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。

## <a name="applies-to"></a>適用於

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>備註

[**影片防震 MFT**](video-stabilization-mft.md)會在其產生的輸出範例上設定此屬性。 屬性的值是 [**MFVideoDSPMode**](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-mfvideodspmode) 列舉值。 如果值是 **MFVideoDSPMode \_ 穩定**，則表示該 MFT 將映射穩定套用至框架。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                              |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Wmcodecdsp。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[範例屬性](sample-attributes.md)
</dt> <dt>

[媒體範例](media-samples.md)
</dt> <dt>

[**影片防震 MFT**](video-stabilization-mft.md)
</dt> </dl>

 

 





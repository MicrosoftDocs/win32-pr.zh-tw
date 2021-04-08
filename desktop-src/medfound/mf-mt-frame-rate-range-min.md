---
description: 影片捕獲裝置所支援的最小畫面播放速率（以每秒畫面格數為單位）。
ms.assetid: d3725796-f683-4ca1-a37f-22c40fff0b76
title: 'MF_MT_FRAME_RATE_RANGE_MIN 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9692927242eea7ec65b86572db455e610e30c711
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851431"
---
# <a name="mf_mt_frame_rate_range_min-attribute"></a>MF \_ MT \_ 幀 \_ 速率 \_ 範圍 \_ 最小值屬性

影片捕獲裝置所支援的最小畫面播放速率（以每秒畫面格數為單位）。

## <a name="data-type"></a>資料類型

**UINT64**

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**MFGetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio)。

若要設定這個屬性，請呼叫 [**MFSetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio)。

## <a name="remarks"></a>備註

畫面播放速率以比例表示。 屬性值的上方32位包含分子，而較低的32位則包含分母。 例如，如果畫面播放速率是每秒30個畫面格 (fps) ，則比率為30/1。

如果捕捉裝置報告的畫面播放速率下限，媒體來源會在媒體類型上設定此屬性。 [ [MF \_ MT \_ 幀 \_ 速率 \_ 範圍 \_ 最大值](mf-mt-frame-rate-range-max.md) ] 屬性提供最大畫面播放速率。 裝置不保證可支援此範圍內的每個增量。

若要設定裝置的畫面播放速率，請先在媒體類型上修改 [ [**MF \_ MT \_ 幀 \_ 速率**](mf-mt-frame-rate-attribute.md) ] 屬性的值。 然後設定媒體來源上的媒體類型。

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                  |
| 最低支援的伺服器<br/> | Windows Server 2008 R2 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                     |
| 標頭<br/>                   | <dl> <dt>Mfapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[如何設定影片捕獲畫面播放速率](how-to-set-the-video-capture-frame-rate.md)
</dt> <dt>

[媒體類型屬性](media-type-attributes.md)
</dt> <dt>

[影片捕獲](video-capture.md)
</dt> <dt>

[MF \_ MT \_ 幀 \_ 速率 \_ 範圍 \_ 最大值](mf-mt-frame-rate-range-max.md)
</dt> </dl>

 

 





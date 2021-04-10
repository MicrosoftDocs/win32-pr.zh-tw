---
description: 指定監視器的重新整理頻率。
ms.assetid: deeb780c-2dc2-4a9a-926a-23b9ae3bedd5
title: 'MF_TOPOLOGY_PLAYBACK_FRAMERATE 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 620d7ff7dbc893065ebb378557f0731cd8826582
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191881"
---
# <a name="mf_topology_playback_framerate-attribute"></a>MF \_ 拓撲 \_ 播放 \_ 畫面播放速率屬性

指定監視器的重新整理頻率。

## <a name="data-type"></a>資料類型

**UINT64**

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**MFGetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio)。

若要設定這個屬性，請呼叫 [**MFSetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio)。

## <a name="applies-to"></a>適用於

[**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a>備註

拓撲載入器會使用此屬性，在播放開始之前將管線優化。 如果設定此屬性，也請將 [ [MF \_ 拓撲 \_ 靜態 \_ 播放 \_ 優化](mf-topology-static-playback-optimizations.md) ] 屬性設定為 [ **TRUE**]。

畫面播放速率以比例表示。 屬性值的上方32位包含分子，而較低的32位則包含分母。

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/>                            |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[拓撲屬性](topology-attributes.md)
</dt> <dt>

[影片品質管制](video-quality-management.md)
</dt> </dl>

 

 





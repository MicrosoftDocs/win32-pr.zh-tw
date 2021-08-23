---
description: 指定影片播放的目的地視窗大小。
ms.assetid: 46af4c11-042c-4580-ba9d-3aee6172de56
title: 'MF_TOPOLOGY_PLAYBACK_MAX_DIMS 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e98575a32b1d68414cb4d94a547273aa4986e03dc707023d5c40f9860b77b5a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119604778"
---
# <a name="mf_topology_playback_max_dims-attribute"></a>MF \_ 拓撲 \_ 播放 \_ 最大 \_ 亮度屬性

指定影片播放的目的地視窗大小。

## <a name="data-type"></a>資料類型

**UINT64**

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**MFGetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributesize)。

若要設定這個屬性，請呼叫 [**MFSetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributesize)。

## <a name="applies-to"></a>適用於

[**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a>備註

拓撲載入器會使用此屬性，在播放開始之前將管線優化。 如果設定此屬性，也請將 [ [MF \_ 拓撲 \_ 靜態 \_ 播放 \_ 優化](mf-topology-static-playback-optimizations.md) ] 屬性設定為 [ **TRUE**]。

屬性值的上方32位包含寬度，而較低的32位則包含高度（以圖元為單位）。

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/>                            |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[拓撲屬性](topology-attributes.md)
</dt> <dt>

[影片品質管制](video-quality-management.md)
</dt> </dl>

 

 





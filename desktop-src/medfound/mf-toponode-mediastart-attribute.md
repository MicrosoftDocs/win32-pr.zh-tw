---
description: 指定簡報的開始時間。
ms.assetid: a2a64cac-0dc1-41b0-b59c-a477c7304ba1
title: 'MF_TOPONODE_MEDIASTART 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7efeed2bd34745ffda4e756c8b43894bd51fc287ded5cba0ecf0ffb323713754
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118244419"
---
# <a name="mf_toponode_mediastart-attribute"></a>MF \_ TOPONODE \_ MEDIASTART 屬性

指定簡報的開始時間。

## <a name="data-type"></a>資料類型

**UINT64**

視為 **LONGLONG** 值。

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)。

## <a name="applies-to"></a>適用於

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)

## <a name="remarks"></a>備註

這個屬性會指定來源中播放開始播放的位置，相對於啟動來源，則以 100-毫微秒單位表示。 如果未設定此屬性，播放會從零開始 () 檔案的開頭。 例如，若要在5秒的標記開始播放，請將此屬性設定為50000000。 在拓撲 (節點（類型等於 **MF \_ 拓撲 \_ SOURCESTREAM \_ 節點**) ）的來源節點上設定屬性。 呼叫 [**IMFMediaSession：： SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology)之前，請先設定屬性。

> [!Note]  
> 如果您以手動方式將解碼器插入拓撲，您也必須在 [解碼器] 節點上，將 [ [mf \_ TOPONODE \_ MARKIN \_ ](mf-toponode-markin-here-attribute.md) ] 和 [ [mf \_ TOPONODE \_ MARKOUT \_ ](mf-toponode-markout-here-attribute.md) ] 屬性設定為。

 

這個屬性是帶正負號的值，雖然它會儲存為 **UINT64**。 不過，負值並沒有意義。

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[順序呈現時間](sequence-presentation-times.md)
</dt> <dt>

[拓撲節點屬性](topology-node-attributes.md)
</dt> <dt>

[**MF \_ TOPONODE \_ MEDIASTOP**](mf-toponode-mediastop-attribute.md)
</dt> </dl>

 

 





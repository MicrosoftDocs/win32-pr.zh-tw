---
description: 會將時間 (以 100-毫微秒) 單位來儲存，表示必須開始的時間，相對於媒體來源的開頭。
ms.assetid: 7a3dddad-067b-46af-9ed9-4ccc65f9d772
title: 'MF_PD_PLAYBACK_BOUNDARY_TIME 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22abadb4e0148a2079a9a7387e43599f4f79b8bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027468"
---
# <a name="mf_pd_playback_boundary_time-attribute"></a>MF \_ PD \_ 播放 \_ 界限 \_ 時間屬性

會將時間 (以 100-毫微秒) 單位來儲存，表示必須開始的時間，相對於媒體來源的開頭。

## <a name="data-type"></a>資料類型

**UINT64**

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)。

## <a name="applies-to"></a>適用於

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)

## <a name="remarks"></a>備註

在 \_ \_ 播放清單中，媒體來源的 [MF PD 播放 \_ 界限時間] \_ 屬性是選擇性的。 此值表示簡報的實際開始時間。 假設有一個播放清單包含媒體來源 *Element1*、 *Element2* 和 *Element3* 的順序。 *Element1* 開始播放後的15秒，就會發生動態資料流變更。 新的資料流程必須在簡報中開始15秒的時間。 不過，最接近15秒呈現時間的主要畫面格為新資料流程的12秒。 若要在15秒內啟動新的簡報，需要 markin，以便將解碼的樣本從12秒降至15秒。

在轉換之前，媒體來源會引發 [MENewPresentation](menewpresentation.md) 事件。 這會傳回包含 *Element1* 的 [MF \_ PD 播放專案 \_ \_ \_ 識別碼](mf-pd-playback-element-id.md)屬性的簡報描述項。 此外，它還包含 [MF \_ PD \_ 播放 \_ 界限時間] \_ 屬性（設定為15秒），以表示發生轉換的時間。 媒體來源會在解碼後的15秒執行 markin，以防止畫面格顯示12秒到15秒。

此值只會影響 markin 時間，不會影響媒體會話調整時間戳記的方式。 除非媒體來源透過 [ [MF \_ PD \_ 播放專案 \_ \_ 識別碼](mf-pd-playback-element-id.md) ] 屬性工作表示此簡報與上一個播放元素相同，否則會忽略這個屬性。

[MF \_ PD \_ 播放 \_ 界限 \_ 時間] 屬性類似于 [拓撲] 節點上設定的 [ [mf \_ TOPONODE \_ MEDIASTART](mf-toponode-mediastart-attribute.md) ] 屬性。 針對在 Windows Vista 上執行的應用程式，執行 [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) 的媒體來源應該使用 **mf \_ TOPONODE \_ MEDIASTART** ，而不是使用 mf \_ PD \_ 播放 \_ 界限 \_ 時間。

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                  |
| 最低支援的伺服器<br/> | Windows Server 2008 R2 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                     |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[展示描述項屬性](presentation-descriptor-attributes.md)
</dt> </dl>

 

 





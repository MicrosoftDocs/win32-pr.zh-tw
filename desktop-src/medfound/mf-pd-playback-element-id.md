---
description: 包含簡報中播放清單元素的識別碼。
ms.assetid: 355818cf-1e00-46ad-9ce1-ab3a178164f9
title: 'MF_PD_PLAYBACK_ELEMENT_ID 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 744a1d164c71cbd7eb8bb47ef12be68d47b8351d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996975"
---
# <a name="mf_pd_playback_element_id-attribute"></a>MF \_ PD \_ 播放 \_ 元素 \_ 識別碼屬性

包含簡報中播放清單元素的識別碼。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。

## <a name="applies-to"></a>適用於

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)

## <a name="remarks"></a>備註

傳遞播放清單的媒體來源可以選擇性地在其展示描述項上設定此屬性。

當媒體來源傳遞播放清單時，它會在第一個播放清單元素之後傳送 [MENewPresentation](menewpresentation.md) 事件。 此事件包含新播放清單元素的表示描述項。 媒體來源可以將識別碼指派給元素，方法是 \_ \_ \_ \_ 在每個呈現描述項上設定 [MF PD 播放專案識別碼] 屬性，包括 [**IMFMediaSource：： CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor)所建立的描述項。

媒體來源可能也會傳送 [MENewPresentation](menewpresentation.md) 事件，因為動態資料流參數或資料流程數目有所變更。 在這種情況下， \_ 兩個簡報中的 MF PD \_ 播放專案識別碼值 \_ \_ 應該保持不變，表示兩個簡報都代表相同的播放清單元素。 如果兩個連續的簡報都有相同的屬性值，Microsoft 媒體基礎管線會預期時間戳記會在整個轉換期間保持連續。 因此，當媒體來源轉換至下一個簡報時，不能使用 [MF \_ 事件 \_ 來源 \_ 實際 \_ 開始](mf-event-source-actual-start-attribute.md) 屬性。

執行 [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) 的媒體來源應該使用 [mf \_ TOPONODE \_ SEQUENCE \_ ELEMENTID](mf-toponode-sequence-elementid-attribute.md) 屬性，而不是使用 mf \_ PD \_ 播放 \_ 元素 \_ 識別碼屬性。

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

 

 





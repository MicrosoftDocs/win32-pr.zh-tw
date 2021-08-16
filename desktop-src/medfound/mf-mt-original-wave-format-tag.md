---
description: 包含音訊資料流程的原始 WAVE 格式標記。
ms.assetid: 2b30a1c2-4a42-4b09-acb6-b76267cc7ed0
title: 'MF_MT_ORIGINAL_WAVE_FORMAT_TAG 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a89f05086858f54c619e3896f5978cf81005e9b1e80e858bc89c71e951ab48b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118741663"
---
# <a name="mf_mt_original_wave_format_tag-attribute"></a>MF \_ MT \_ 原始 \_ WAVE \_ 格式 \_ 標記屬性

包含音訊資料流程的原始 WAVE 格式標記。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。

## <a name="applies-to"></a>適用於

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>備註

根據來源檔案，AVI 媒體來源可能會在其所提供的媒體類型上設定此屬性。

AVI 檔案包含檔案中每個資料流程的資料流程標頭。 AVI 媒體來源會將資料流程標頭轉譯為媒體類型。 針對音訊串流，資料流程標頭包含可識別音訊格式的格式標記。  (格式標籤包含在 [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))結構的 **wFormatTag** 成員中 ) 。在大部分情況下，AVI 媒體來源會將格式標記直接轉換成子類型 Guid，如「[**音訊子類型 guid**](audio-subtype-guids.md)」主題所述。 不過，在某些情況下，它會將原始格式標記對應至另一個相等的格式標記。 如果是的話，媒體來源會使用 MF \_ MT \_ 原始 \_ WAVE \_ 格式 \_ 標記屬性，將原始格式標記儲存在媒體類型中。

格式對應會儲存在登錄中的下列機碼底下：

**HKEY \_類別 \_ 根目錄** \\ **MediaFoundation** \\ **MapAudioFormatTag**

每個專案都是 **DWORD** 值。 專案的名稱是格式標記的十進位標記法。 專案的值是相等的格式標記。

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/>                            |
| 標頭<br/>                   | <dl> <dt>Mfapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[媒體類型屬性](media-type-attributes.md)
</dt> </dl>

 

 

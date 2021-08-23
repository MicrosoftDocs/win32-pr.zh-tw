---
description: 針對拓撲載入器是否會載入以硬體為基礎的轉換，指定轉碼拓撲。
ms.assetid: 33db8621-114a-4531-908f-f30034441973
title: 'MF_TRANSCODE_TOPOLOGYMODE 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36e8715c135e074956af2280b8474172e94e69e1cca20cd01b020fc6dc79076c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663838"
---
# <a name="mf_transcode_topologymode-attribute"></a>MF \_ 轉碼 \_ TOPOLOGYMODE 屬性

針對拓撲載入器是否會載入以硬體為基礎的轉換，指定轉碼拓撲。

拓撲模式會指定硬體轉換 (例如硬體編解碼器) 是否可用於轉碼拓撲中。 應用程式可以藉由呼叫 [**IMFTranscodeProfile：： SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes)，將此屬性儲存在轉碼設定檔中。

## <a name="data-type"></a>資料類型

**[**MF \_以 UINT32 形式儲存的轉碼 \_ TOPOLOGYMODE \_ 旗標**](/windows/desktop/api/mfidl/ne-mfidl-mf_transcode_topologymode_flags)** 

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。

## <a name="remarks"></a>備註

此屬性是選擇性的。 它必須有下列其中一個值。



| 值                                              | 描述                                                                                                                                                                                                                                                                       |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **允許的 MF \_ 轉碼 \_ TOPOLOGYMODE \_ 硬體 \_** | 拓撲載入器會載入以硬體為基礎的 MFTs，例如硬體解碼器（如果有的話）。<br/> 如果找不到硬體解碼器，或硬體解碼器因為某些原因而無法連線，拓撲載入器會自動切換回軟體解碼。<br/> |
| **\_僅限 MF 轉碼 \_ TOPOLOGYMODE \_ 軟體 \_**    | 拓撲載入器只會載入軟體 MFTs，包括軟體解碼器。                                                                                                                                                                                                    |



 

預設值為 **\_ \_ \_ \_ 僅限 MF 轉碼 TOPOLOGYMODE SOFTWARE**。

如果拓撲載入器將硬體 MFT 插入拓撲中，它會在 [拓撲] 節點上設定 [ [mft \_ 列舉 \_ 硬體 \_ URL] \_ 屬性](mft-enum-hardware-url-attribute.md) 屬性。 若要檢查硬體 MFT 是否存在，請列舉已解析拓撲中的節點，並檢查此屬性是否存在。

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

[轉碼 API](transcode-api.md)
</dt> <dt>

[**IMFTranscodeProfile::GetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getcontainerattributes)
</dt> <dt>

[**IMFTranscodeProfile::SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes)
</dt> </dl>

 

 





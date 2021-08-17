---
description: 指定裝置的輸出格式。
ms.assetid: 33a1b546-ece2-44ef-a1c0-5579c32be0bc
title: 'MF_DEVSOURCE_ATTRIBUTE_MEDIA_TYPE 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb4685f419658ecf77782a4cef770fd205119bb6cfd95523edb7fbbe001fd700
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105034"
---
# <a name="mf_devsource_attribute_media_type-attribute"></a>MF \_ DEVSOURCE \_ 屬性 \_ 媒體 \_ 類型屬性

指定裝置的輸出格式。

## <a name="data-type"></a>資料類型

**[**MFT \_儲存 \_ \_**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info)** 為 **位元組 \[ 的 \]** 註冊類型資訊

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)。

## <a name="remarks"></a>備註

此屬性包含一對 Guid：主要類型和子類型。 這些 Guid 描述裝置的預設輸出格式。 裝置可能會支援其他輸出格式。

例如，如果影片捕獲裝置輸出 RGB-32 影片，則此屬性的值為 `{ MFMediaType_Video, MFVideoFormat_RGB32 }` 。

這個屬性是應用程式的提示。 若要取得確切的輸出格式，請建立裝置的媒體來源，並取得媒體來源的展示描述項。

這個屬性是在下列函式所傳回的啟用物件上設定：

-   [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

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

[音訊/視訊擷取](audio-video-capture.md)
</dt> <dt>

[捕獲裝置屬性](capture-device-attributes.md)
</dt> </dl>

 

 





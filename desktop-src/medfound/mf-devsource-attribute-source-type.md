---
description: 指定裝置類型，例如音訊捕獲或影片捕獲。
ms.assetid: c6c05267-1c93-48e2-b463-b5a1514f1b7b
title: 'MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3445c74b1a77472bad564f6988f9ae2f4696fef7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977021"
---
# <a name="mf_devsource_attribute_source_type-attribute"></a>MF \_ DEVSOURCE \_ 屬性 \_ 來源 \_ 類型屬性

指定裝置的類型，例如音訊捕獲或影片捕獲。

## <a name="data-type"></a>資料類型

**GUID**

這個屬性會定義下列值：



| 值                                                                                                                                                                                                                                                                 | 意義                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_GUID"></span><span id="mf_devsource_attribute_source_type_audcap_guid"></span><dl> <dt>**MF \_ DEVSOURCE \_ 屬性 \_ 來源 \_ 類型 \_ AUDCAP \_ GUID**</dt> </dl> | 音訊捕獲裝置。<br/> |
| <span id="MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_GUID"></span><span id="mf_devsource_attribute_source_type_vidcap_guid"></span><dl> <dt>**MF \_ DEVSOURCE \_ 屬性 \_ 來源 \_ 類型 \_ VIDCAP \_ GUID**</dt> </dl> | 影片捕獲裝置。<br/> |



 

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)。

## <a name="remarks"></a>備註

使用此屬性作為下列函式的輸入：

-   [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource)
-   [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

此外，這個屬性是在 [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) 函式所傳回的啟用物件上設定的。

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

[音訊/視訊擷取](audio-video-capture.md)
</dt> <dt>

[捕獲裝置屬性](capture-device-attributes.md)
</dt> </dl>

 

 





---
description: 指定音訊捕獲裝置的裝置角色。
ms.assetid: 4f2885b6-c771-4577-880d-5feea671432e
title: 'MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_ROLE 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 148ae6697151698eef58d3c0148de3ed81822a05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026448"
---
# <a name="mf_devsource_attribute_source_type_audcap_role-attribute"></a>MF \_ DEVSOURCE \_ 屬性 \_ 來源 \_ 類型 \_ AUDCAP \_ 角色屬性

指定音訊捕獲裝置的裝置角色。

## <a name="data-type"></a>資料類型

**ERole** 儲存為 **UINT32**

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。

## <a name="remarks"></a>備註

**ERole** 列舉型別記載于核心音訊 API 檔中。

屬性的值會指定裝置角色。 這個屬性與下列函數搭配使用。

這個屬性可用來作為 [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) 和 [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) 函數的輸入。 如果指定了屬性，則函式會建立媒體來源，以針對指定的裝置角色使用預設音訊捕獲裝置。

這個屬性也可以當做 [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) 函數的輸入使用。 如果指定了屬性，則列舉會限制為指定的裝置角色。 此外， **MFEnumDeviceSources** 函式所傳回的每個啟用物件都包含這個屬性。 然後，在建立媒體來源時，啟始物件會在內部使用此屬性。

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

 

 





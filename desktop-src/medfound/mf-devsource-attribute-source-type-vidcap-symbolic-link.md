---
description: 包含影片捕獲驅動程式的符號連結。
ms.assetid: 3d256dec-ec8c-4c62-883b-e2c292fd90eb
title: 'MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_SYMBOLIC_LINK 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1dd3b69899eb9df1973cb13611a822139ffda0e744c84137ff9d6094ed4a962d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104944"
---
# <a name="mf_devsource_attribute_source_type_vidcap_symbolic_link-attribute"></a>MF \_ DEVSOURCE \_ 屬性 \_ 來源 \_ 類型 \_ VIDCAP \_ 符號 \_ 連結屬性

包含影片捕獲驅動程式的符號連結。

## <a name="data-type"></a>資料類型

**WCHAR\***

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)。

## <a name="remarks"></a>備註

使用這個屬性做為 [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) 函數的輸入。

此外，此屬性是在下列函式所傳回的啟用物件上設定：

-   [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

符號連結應該視為不透明的字串。 適用于裝置的可讀取顯示名稱會包含在 [ [MF DEVSOURCE 屬性] 的 [ \_ \_ \_ 易記 \_ 名稱](mf-devsource-attribute-friendly-name.md) ] 屬性中。

您可以將 MF \_ DEVSOURCE \_ 屬性 \_ 來源 \_ 類型 \_ VIDCAP \_ 符號 \_ 連結屬性作為 [**SetupDiOpenDeviceInterface**](/windows/win32/api/setupapi/nf-setupapi-setupdiopendeviceinterfacea) 函數的 DevicePath 引數值傳入。

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

 

 

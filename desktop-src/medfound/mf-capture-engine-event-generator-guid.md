---
description: 識別產生 capture 事件的元件。
ms.assetid: DCCF3054-AF14-44C7-84C0-B03E35B5D90A
title: 'MF_CAPTURE_ENGINE_EVENT_GENERATOR_GUID 屬性 (Mfcaptureengine) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88efff7cea540c1fae2c14d44dd7676c4f523b562a66a4c4f4bc4dffea59d5e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118474466"
---
# <a name="mf_capture_engine_event_generator_guid-attribute"></a>MF \_ 捕獲 \_ 引擎 \_ 事件產生器 \_ \_ GUID 屬性

識別產生 capture 事件的元件。

## <a name="data-type"></a>資料類型

**GUID**

## <a name="remarks"></a>備註

這個屬性會出現在 capture 引擎的某些事件上。 若要取得這個屬性，請在事件物件上呼叫 [**IMFAttributes：： GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid) 。 事件物件會透過 [**IMFCaptureEngineOnEventCallback：： OnEvent**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengineoneventcallback-onevent) 方法傳遞給應用程式。

值是產生事件之元件的介面識別碼。 例如，值 **IID \_ IMFCapturePreviewSink** 表示預覽接收 ([**IMFCapturePreviewSink**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturepreviewsink)) 。 並非每個 capture 事件都包含這個屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                                   |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                         |
| 標頭<br/>                   | <dl> <dt>Mfcaptureengine. h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Capture 引擎屬性](capture-engine-attributes.md)
</dt> <dt>

[**IMFCaptureEngine：： Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 





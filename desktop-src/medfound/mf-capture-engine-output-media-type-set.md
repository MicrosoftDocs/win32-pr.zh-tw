---
description: 表示已在捕獲引擎上設定輸出類型，以回應 IMFCaptureSink2：： SetOutputType。
ms.assetid: A48CBC82-87C2-4AED-B7E0-B7C60FCCE4CC
title: 'MF_CAPTURE_ENGINE_OUTPUT_MEDIA_TYPE_SET 屬性 (Mfcaptureengine) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5819de6a07f3b6a339400d65ff9260c33b14c592
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104321635"
---
# <a name="mf_capture_engine_output_media_type_set-attribute"></a>MF \_ CAPTURE \_ ENGINE \_ 輸出 \_ 媒體 \_ 類型 \_ 設定屬性

表示已在捕獲引擎上設定輸出類型，以回應 [**IMFCaptureSink2：： SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)。

## <a name="data-type"></a>資料類型

**GUID**

## <a name="remarks"></a>備註

您可以呼叫 [**IMFMediaEvent：： GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstatus) ，找出作業是否成功。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8.1 桌面應用程式\]<br/>                                                   |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 R2 \[ desktop 應用程式\]<br/>                                        |
| 標頭<br/>                   | <dl> <dt>Mfcaptureengine. h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Mfcaptureengine .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFCaptureSink2::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)
</dt> </dl>

 

 





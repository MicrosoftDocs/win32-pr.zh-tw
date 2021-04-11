---
description: 在 capture 引擎上設定 DXGI 裝置管理員的指標。
ms.assetid: 1DFDE7AB-7DFF-4C39-9460-E42E37649AAC
title: 'MF_CAPTURE_ENGINE_D3D_MANAGER 屬性 (Mfcaptureengine) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3c5e87d4817f539f91ecd55aec10a2086afeaeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113684"
---
# <a name="mf_capture_engine_d3d_manager-attribute"></a>MF \_ CAPTURE \_ ENGINE \_ D3D \_ 管理員屬性

在 capture 引擎上設定 DXGI 裝置管理員的指標。

## <a name="data-type"></a>資料類型

**IUnknown \** _

## <a name="remarks"></a>備註

這個屬性的值是 [_ *IMFDXGIDeviceManager* *](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager)介面的指標。 此屬性可讓 capture engine 使用 DXGI 介面配置影片框架，並使用硬體加速進行解碼和影片處理。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                                   |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                         |
| 標頭<br/>                   | <dl> <dt>Mfcaptureengine. h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Capture 引擎屬性](capture-engine-attributes.md)
</dt> <dt>

[**IMFCaptureEngine：： Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 





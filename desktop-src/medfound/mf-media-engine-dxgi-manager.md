---
description: 設定媒體引擎上的 Microsoft DirectX Graphic Infrastructure (DXGI) 裝置管理員。
ms.assetid: CB952492-0ACF-4501-BD8B-133E26FCE8F7
title: 'MF_MEDIA_ENGINE_DXGI_MANAGER 屬性 (Mfmediaengine) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c454041f83a58cdb5b3c1e340d63908386546090eb52811e0c876e5d8bed0bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119723050"
---
# <a name="mf_media_engine_dxgi_manager-attribute"></a>MF \_ 媒體 \_ 引擎 \_ DXGI \_ 管理員屬性

設定媒體引擎上的 Microsoft DirectX Graphic Infrastructure (DXGI) 裝置管理員。

## <a name="data-type"></a>資料類型

**IMFDXGIDeviceManager \* *_ 儲存為 _* IUnknown\***

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)。

## <a name="remarks"></a>備註

這個屬性的值是 [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) 介面的指標。

在框架伺服器模式中，此屬性可讓媒體引擎使用硬體加速進行影片解碼和影片處理。 如果未設定此屬性，則媒體引擎會使用軟體解碼和處理。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[桌面應用程式 \| UWP 應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | Windows Server 2012 \[桌面應用程式 \| UWP 應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Mfmediaengine。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFMediaEngineClassFactory：： CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance)
</dt> </dl>

 

 





---
description: 包含 IMFMediaEngineExtension 介面的指標。
ms.assetid: D2F3F41D-086A-4DEB-99D0-07574BC8F0D7
title: 'MF_MEDIA_ENGINE_EXTENSION 屬性 (Mfmediaengine) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4496b40e9b69091b588ad38ad47d943dce5e1966
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104386326"
---
# <a name="mf_media_engine_extension-attribute"></a>MF \_ 媒體 \_ 引擎 \_ 延伸模組屬性

包含 [**IMFMediaEngineExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineextension) 介面的指標。

## <a name="data-type"></a>資料類型

**IMFMediaEngineExtension \* *_ 儲存為 _* IUnknown\***

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)。

## <a name="remarks"></a>備註

這個屬性會與 [**IMFMediaEngineClassFactory：： CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) 方法搭配使用，以初始化 Media Engine。

此屬性是選擇性的。 您可以使用它來提供可實 [**IMFMediaEngineExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineextension) 介面的物件。 此介面可讓應用程式載入自訂媒體資源。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | Windows Server 2012 \[ desktop app \| UWP 應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Mfmediaengine。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 





---
description: 指定媒體引擎是否會播放受保護的內容。
ms.assetid: 2A593499-BF40-440E-AF1D-3B0E7732489A
title: 'MF_MEDIA_ENGINE_CONTENT_PROTECTION_FLAGS 屬性 (Mfmediaengine) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec1cb6b9c9a49c690af84678435ac2bb4fdab76a2fb13c95fecd9ddc33771d7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119956438"
---
# <a name="mf_media_engine_content_protection_flags-attribute"></a>MF \_ 媒體 \_ 引擎 \_ 內容 \_ 保護 \_ 旗標屬性

指定媒體引擎是否會播放受保護的內容。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="remarks"></a>備註

這個屬性的值是來自于 [**MF \_ 媒體 \_ 引擎 \_ 保護 \_ 旗標**](/windows/desktop/api/mfmediaengine/ne-mfmediaengine-mf_media_engine_protection_flags)列舉的位 **or** of 旗標。 若要啟用受保護內容的播放，請設定 [ **MF \_ 媒體 \_ 引擎 \_ 啟用 \_ 受保護的 \_ 內容** ] 旗標。

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

[媒體引擎屬性](media-engine-attributes.md)
</dt> <dt>

[**IMFMediaEngineClassFactory：： CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance)
</dt> </dl>

 

 





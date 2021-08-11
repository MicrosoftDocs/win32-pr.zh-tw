---
description: 讓媒體引擎播放受保護的內容。
ms.assetid: F6F17EC7-6553-4127-B691-C20C945DD4D8
title: 'MF_MEDIA_ENGINE_CONTENT_PROTECTION_MANAGER 屬性 (Mfmediaengine) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe80e619f3b256f6aa587f32d9ee5b6f43cd2978a5dfb043c62536ff5315bacb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118244687"
---
# <a name="mf_media_engine_content_protection_manager-attribute"></a>MF \_ 媒體 \_ 引擎 \_ 內容 \_ 保護 \_ 管理員屬性

讓媒體引擎播放受保護的內容。

## <a name="data-type"></a>資料類型

**IUnknown\***

## <a name="remarks"></a>備註

這個屬性的值是 [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) 介面的指標。 呼叫端必須執行介面。

這個屬性可以是傳遞給 [**IMFMediaEngineClassFactory：： CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance)的其中一個屬性。 如果要播放受保護的內容，則為必要項。

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

 

 





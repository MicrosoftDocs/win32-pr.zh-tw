---
description: 設定媒體引擎的呈現目標格式。
ms.assetid: 70FFDD44-9FDE-4D86-AD65-60019AC4A2BC
title: 'MF_MEDIA_ENGINE_VIDEO_OUTPUT_FORMAT 屬性 (Mfmediaengine) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eaa0dab3c3ea1c9ce23d767458df0b68a9b3c787f80ca1af786061536343a356
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973727"
---
# <a name="mf_media_engine_video_output_format-attribute"></a>MF \_ 媒體 \_ 引擎 \_ 影片 \_ 輸出 \_ 格式屬性

設定媒體引擎的呈現目標格式。

## <a name="data-type"></a>資料類型

**DXGI \_** 儲存為 **UINT32** 的格式

## <a name="remarks"></a>備註

如果您在框架伺服器模式下建立媒體引擎，請設定此屬性。 如需詳細資訊，請參閱 [**IMFMediaEngineClassFactory：： CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance)。 屬性的值為 [DXGI \_ 格式](../direct3d9/d3dformat.md) 值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[桌面應用程式 \| UWP 應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | Windows Server 2012 \[桌面應用程式 \| UWP 應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Mfmediaengine。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 

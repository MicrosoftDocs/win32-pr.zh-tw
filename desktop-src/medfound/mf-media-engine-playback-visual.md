---
description: 將 Microsoft DirectComposition 視覺效果設定為媒體引擎的播放區域。
ms.assetid: C381D28E-B7A1-4A1A-9F8D-42A4ABB1C633
title: 'MF_MEDIA_ENGINE_PLAYBACK_VISUAL 屬性 (Mfmediaengine) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25e9c7366bd0fbf4bf36523cf7a68f2d6da70bc3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "107000524"
---
# <a name="mf_media_engine_playback_visual-attribute"></a>MF \_ 媒體 \_ 引擎 \_ 播放 \_ 視覺化屬性

將 Microsoft DirectComposition 視覺效果設定為媒體引擎的播放區域。

## <a name="data-type"></a>資料類型

**IDCompositionVisual \* *_ 儲存為 _* IUnknown\***

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)。

## <a name="remarks"></a>備註

如需 DirectComposition 的詳細資訊，請參閱 [DirectComposition](../directcomp/directcomposition-portal.md) 和 [**IDCompositionVisual**](/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual)。

這個屬性會與 [**IMFMediaEngineClassFactory：： CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) 方法搭配使用，以初始化 Media Engine。

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

 

 

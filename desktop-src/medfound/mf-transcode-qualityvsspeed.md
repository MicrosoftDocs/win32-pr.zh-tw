---
description: 指定介於0和100之間的數位，指出編碼品質與編碼速度之間的取捨。
ms.assetid: 872140e8-fd39-446c-a84f-1e04ea95076e
title: 'MF_TRANSCODE_QUALITYVSSPEED 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7498cd319f347d8509f42e1713e1b2e267b32406eceb073ea9ca1e4cb4ea8d80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119604667"
---
# <a name="mf_transcode_qualityvsspeed-attribute"></a>MF \_ 轉碼 \_ QUALITYVSSPEED 屬性

指定介於0和100之間的數位，指出編碼品質與編碼速度之間的取捨。

## <a name="data-type"></a>資料類型

**UINT32**

這個屬性的值具有下列範圍。



| 值                                                                          | 意義                                     |
|--------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>0</dt> </dl>   | 較低的品質、更快速的編碼方式。<br/>  |
| <dl> <dt>100</dt> </dl> | 品質較高、速度較慢的編碼。<br/> |



 

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。

## <a name="remarks"></a>備註

這個屬性的 GUID 值與針對 [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi)定義的 [AVEncCommonQualityVsSpeed](../directshow/avenccommonqualityvsspeed-property.md)屬性相同，而且具有相同的轉譯。

在建立 Windows 媒體編解碼器的轉碼拓朴之前，應用程式可以在轉碼設定檔上設定此屬性。 值必須在0到100的範圍內。 針對影片串流，轉碼拓撲產生器會將值對應到應用程式指定的值，並將對應的值提供給編碼器的 **MFPKEY \_ COMPLEXITYEX** 屬性。 較低的值可讓編碼器使用較不復雜的編碼演算法。 使用較簡單的演算法會產生較低品質的輸出，但編碼程式較快，而且需要較少的處理能力。

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[轉碼 API](transcode-api.md)
</dt> <dt>

[**IMFTranscodeProfile::SetVideoAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes)
</dt> </dl>

 

 

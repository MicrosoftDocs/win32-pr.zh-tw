---
description: 指定音訊資料流程的類別。
ms.assetid: 0F2DB9A7-64ED-4952-BCB3-F2B15BA37D2A
title: MF_MEDIA_ENGINE_AUDIO_CATEGORY 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d22cd3795886b78afae03ba4b592d4657857f76b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "103945627"
---
# <a name="mf_media_engine_audio_category-attribute"></a>MF \_ 媒體 \_ 引擎 \_ 音訊 \_ 類別目錄屬性

指定音訊資料流程的類別。

## <a name="data-type"></a>資料類型

**[**音訊 \_ 串流 \_ 類別**](/windows/win32/api/audiosessiontypes/ne-audiosessiontypes-audio_stream_category)**

## <a name="remarks"></a>備註

這個屬性的值是 [**音訊 \_ 串流 \_ 類別**](/windows/win32/api/audiosessiontypes/ne-audiosessiontypes-audio_stream_category) 列舉的成員。

這個屬性會與 [**IMFMediaEngineClassFactory：： CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) 方法搭配使用，以初始化 Media Engine。 屬性是選擇性的。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | Windows Server 2012 \[ desktop app \| UWP 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Mfmediaengine .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 

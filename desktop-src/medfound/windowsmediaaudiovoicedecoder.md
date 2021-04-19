---
description: Windows Media 音訊的語音編碼器會將 Windows Media 音訊語音編碼器編碼的資料流程解碼。
ms.assetid: 8bb5c8bd-949f-4faa-b679-8854f78076a4
title: 'Windows Media 音訊語音解碼器 (Wmcodecdsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4565a511f2816d2914ec96f3ae89f3af5dd19016
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001814"
---
# <a name="windows-media-audio-voice-decoder"></a>Windows Media 音訊語音解碼器

Windows Media 音訊的語音編碼器會將 [**Windows Media 音訊語音編碼器**](windowsmediaaudiovoiceencoder.md)編碼的資料流程解碼。

## <a name="class-identifier"></a>類別識別碼

Windows Media 音訊語音解碼 (CLSID) 的類別識別碼是以常數 **CLSID \_ CWMSPDecMediaObject** 表示。 您可以藉由呼叫 **CoCreateInstance** 來建立語音解碼的實例。

## <a name="input-formats"></a>輸入格式

Windows Media 音訊的語音編碼內容是以格式標記0x00A 來識別。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-----------------------------------------------------------------------------------------|
| 用戶端<br/> | Windows XP、Windows Vista 或 Windows 7<br/>                                       |
| 標頭<br/> | <dl> <dt>Wmcodecdsp。h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Wmspdmod.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[編解碼器物件](codecobjects.md)
</dt> <dt>

[使用 Windows Media 音訊語音編解碼器](usingthewindowsmediaaudio9voicecodec.md)
</dt> <dt>

[Windows Media 音訊語音編碼器](windowsmediaaudiovoiceencoder.md)
</dt> </dl>

 

 





---
description: Windows Media 音訊聲音編碼程式已針對以高壓縮率編碼人類聲音進行優化。 這是最適合串流的編碼程式，大部分是由說出的單字所組成。
ms.assetid: b3cfa845-4fe1-405f-88e5-4555398639ef
title: 'Windows Media 音訊語音編碼器 (Wmcodecdsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bef79f2c3d0c48fee8ec33e08bfb9fdf21c3656b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001172"
---
# <a name="windows-media-audio-voice-encoder"></a>Windows Media 音訊語音編碼器

Windows Media 音訊聲音編碼程式已針對以高壓縮率編碼人類聲音進行優化。 這是最適合串流的編碼程式，大部分是由說出的單字所組成。

## <a name="class-identifier"></a>類別識別碼

Windows Media 音訊聲音編碼器 (CLSID) 的類別識別碼會以常數 **CLSID \_ CWMSPEncMediaObject2** 表示。 您可以藉由呼叫 **CoCreateInstance** 來建立語音編碼器的實例。

## <a name="output-formats"></a>輸出格式

Windows Media 音訊的語音編碼內容是以格式標記0x00A 來識別。

## <a name="encoder-properties"></a>編碼器屬性

Windows Media 音訊語音編碼器支援下列屬性。



<table>
<thead>
<tr class="header">
<th>屬性</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mfpkey-wmavoice-enc-bufferwindowproperty.md">MFPKEY_WMAVOICE_ENC_BufferWindow</a></td>
<td>指定用於語音編解碼器的緩衝區視窗（以毫秒為單位）。<br/> <dl> Windows XP （含）以後版本。<br />
唯寫。<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmavoice-enc-decoderdelayproperty.md">MFPKEY_WMAVOICE_ENC_DecoderDelay</a></td>
<td>指定包單位中的編碼器延遲。<br/> <dl> Windows XP （含）以後版本。<br />
唯寫。<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-wmavoice-enc-edlproperty.md">MFPKEY_WMAVOICE_ENC_EDL</a></td>
<td>指定要使用語音編解碼器將內容編碼為音樂的部分內容。<br/> <dl> Windows XP （含）以後版本。<br />
讀取/寫入<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md">MFPKEY_WMAVOICE_ENC_MusicSpeechClassMode</a></td>
<td>指定語音編解碼器的模式。<br/> <dl> Windows XP （含）以後版本。<br />
讀取/寫入<br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-----------------------------------------------------------------------------------------|
| 用戶端<br/> | Windows XP、Windows Vista 或 Windows 7<br/>                                       |
| 標頭<br/> | <dl> <dt>Wmcodecdsp。h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Wmspdmoe.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[編解碼器物件](codecobjects.md)
</dt> <dt>

[使用 Windows Media 音訊語音編解碼器](usingthewindowsmediaaudio9voicecodec.md)
</dt> </dl>

 

 





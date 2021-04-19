---
description: DEVINTERFACE \_ XXX guid 是用來代表裝置介面的 guid。
ms.assetid: 2503463B-D7C6-4C82-8421-424D79FD1C2A
title: 'DEVINTERFACE_XXX Guid (Mmdeviceapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 796f113d26ebc351a4d576ed76485d24d89fdb04
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984136"
---
# <a name="devinterface_xxx-guids"></a>DEVINTERFACE \_ XXX guid

DEVINTERFACE \_ XXX guid 是用來代表裝置介面的 guid。

<dl> <dt>

<span id="DEVINTERFACE_AUDIO_CAPTURE"></span><span id="devinterface_audio_capture"></span>**DEVINTERFACE \_ 音訊 \_ 捕獲**
</dt> <dd> <dl> <dt>



指定用來列舉系統上所有音訊捕獲裝置的查詢字串。 [**MediaDevice：： GetAudioCaptureSelector**](/uwp/api/windows.media.devices.mediadevice.getaudiocaptureselector)會傳回這個值。

傳遞此值給 [**ActivateAudioInterfaceAsync**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync) 會在預設音訊捕獲裝置上啟用所要求的介面。


</dt> </dl> </dd> <dt>

<span id="DEVINTERFACE_AUDIO_RENDER"></span><span id="devinterface_audio_render"></span>**DEVINTERFACE \_ 音訊 \_ 轉譯**
</dt> <dd> <dl> <dt>



指定用來列舉系統上所有音訊轉譯裝置的查詢字串。 [**MediaDevice：： GetAudioRenderSelector**](/uwp/api/windows.media.devices.mediadevice.getaudiorenderselector)會傳回這個值。

傳遞此值給 [**ActivateAudioInterfaceAsync**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync) 會在預設音訊轉譯裝置上啟用所要求的介面。


</dt> </dl> </dd> <dt>

<span id="DEVINTERFACE_MIDI_INPUT"></span><span id="devinterface_midi_input"></span>**DEVINTERFACE \_ MIDI \_ 輸入**
</dt> <dd> <dl> <dt>



指定用來列舉系統上所有 [**MidiInPort**](/uwp/api/Windows.Devices.Midi.MidiInPort) 物件的查詢字串。 [**MidiInPort：： GetDeviceSelector**](/uwp/api/windows.devices.midi.midiinport.getdeviceselector)會傳回這個值。


</dt> </dl> </dd> <dt>

<span id="DEVINTERFACE_MIDI_OUTPUT"></span><span id="devinterface_midi_output"></span>**DEVINTERFACE \_ MIDI \_ 輸出**
</dt> <dd> <dl> <dt>



指定用來列舉系統上所有 [**MidiOutPort**](/uwp/api/Windows.Devices.Midi.MidiOutPort) 物件的查詢字串。 [**MidiOutPort：： GetDeviceSelector**](/uwp/api/windows.devices.midi.midioutport.getdeviceselector)會傳回這個值。


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Mmdeviceapi。h</dt> </dl> |



 


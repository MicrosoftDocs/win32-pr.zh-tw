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
# <a name="devinterface_xxx-guids"></a><span data-ttu-id="aa840-103">DEVINTERFACE \_ XXX guid</span><span class="sxs-lookup"><span data-stu-id="aa840-103">DEVINTERFACE\_XXX GUIDs</span></span>

<span data-ttu-id="aa840-104">DEVINTERFACE \_ XXX guid 是用來代表裝置介面的 guid。</span><span class="sxs-lookup"><span data-stu-id="aa840-104">The DEVINTERFACE\_XXX GUIDs are used to represent the GUIDs for device interfaces.</span></span>

<dl> <dt>

<span data-ttu-id="aa840-105"><span id="DEVINTERFACE_AUDIO_CAPTURE"></span><span id="devinterface_audio_capture"></span>**DEVINTERFACE \_ 音訊 \_ 捕獲**</span><span class="sxs-lookup"><span data-stu-id="aa840-105"><span id="DEVINTERFACE_AUDIO_CAPTURE"></span><span id="devinterface_audio_capture"></span>**DEVINTERFACE\_AUDIO\_CAPTURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="aa840-106">指定用來列舉系統上所有音訊捕獲裝置的查詢字串。</span><span class="sxs-lookup"><span data-stu-id="aa840-106">Specifies the query string used to enumerate all audio capture devices on the system.</span></span> <span data-ttu-id="aa840-107">[**MediaDevice：： GetAudioCaptureSelector**](/uwp/api/windows.media.devices.mediadevice.getaudiocaptureselector)會傳回這個值。</span><span class="sxs-lookup"><span data-stu-id="aa840-107">This value is returned by [**MediaDevice::GetAudioCaptureSelector**](/uwp/api/windows.media.devices.mediadevice.getaudiocaptureselector).</span></span>

<span data-ttu-id="aa840-108">傳遞此值給 [**ActivateAudioInterfaceAsync**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync) 會在預設音訊捕獲裝置上啟用所要求的介面。</span><span class="sxs-lookup"><span data-stu-id="aa840-108">Passing this value to [**ActivateAudioInterfaceAsync**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync) activates the requested interface on the default audio capture device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa840-109"><span id="DEVINTERFACE_AUDIO_RENDER"></span><span id="devinterface_audio_render"></span>**DEVINTERFACE \_ 音訊 \_ 轉譯**</span><span class="sxs-lookup"><span data-stu-id="aa840-109"><span id="DEVINTERFACE_AUDIO_RENDER"></span><span id="devinterface_audio_render"></span>**DEVINTERFACE\_AUDIO\_RENDER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="aa840-110">指定用來列舉系統上所有音訊轉譯裝置的查詢字串。</span><span class="sxs-lookup"><span data-stu-id="aa840-110">Specifies the query string used to enumerate all audio render devices on the system.</span></span> <span data-ttu-id="aa840-111">[**MediaDevice：： GetAudioRenderSelector**](/uwp/api/windows.media.devices.mediadevice.getaudiorenderselector)會傳回這個值。</span><span class="sxs-lookup"><span data-stu-id="aa840-111">This value is returned by [**MediaDevice::GetAudioRenderSelector**](/uwp/api/windows.media.devices.mediadevice.getaudiorenderselector).</span></span>

<span data-ttu-id="aa840-112">傳遞此值給 [**ActivateAudioInterfaceAsync**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync) 會在預設音訊轉譯裝置上啟用所要求的介面。</span><span class="sxs-lookup"><span data-stu-id="aa840-112">Passing this value to [**ActivateAudioInterfaceAsync**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync) activates the requested interface on the default audio render device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa840-113"><span id="DEVINTERFACE_MIDI_INPUT"></span><span id="devinterface_midi_input"></span>**DEVINTERFACE \_ MIDI \_ 輸入**</span><span class="sxs-lookup"><span data-stu-id="aa840-113"><span id="DEVINTERFACE_MIDI_INPUT"></span><span id="devinterface_midi_input"></span>**DEVINTERFACE\_MIDI\_INPUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="aa840-114">指定用來列舉系統上所有 [**MidiInPort**](/uwp/api/Windows.Devices.Midi.MidiInPort) 物件的查詢字串。</span><span class="sxs-lookup"><span data-stu-id="aa840-114">Specifies the query string used to enumerate all [**MidiInPort**](/uwp/api/Windows.Devices.Midi.MidiInPort) objects on the system.</span></span> <span data-ttu-id="aa840-115">[**MidiInPort：： GetDeviceSelector**](/uwp/api/windows.devices.midi.midiinport.getdeviceselector)會傳回這個值。</span><span class="sxs-lookup"><span data-stu-id="aa840-115">This value is returned by [**MidiInPort::GetDeviceSelector**](/uwp/api/windows.devices.midi.midiinport.getdeviceselector).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa840-116"><span id="DEVINTERFACE_MIDI_OUTPUT"></span><span id="devinterface_midi_output"></span>**DEVINTERFACE \_ MIDI \_ 輸出**</span><span class="sxs-lookup"><span data-stu-id="aa840-116"><span id="DEVINTERFACE_MIDI_OUTPUT"></span><span id="devinterface_midi_output"></span>**DEVINTERFACE\_MIDI\_OUTPUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="aa840-117">指定用來列舉系統上所有 [**MidiOutPort**](/uwp/api/Windows.Devices.Midi.MidiOutPort) 物件的查詢字串。</span><span class="sxs-lookup"><span data-stu-id="aa840-117">Specifies the query string used to enumerate all [**MidiOutPort**](/uwp/api/Windows.Devices.Midi.MidiOutPort) objects on the system.</span></span> <span data-ttu-id="aa840-118">[**MidiOutPort：： GetDeviceSelector**](/uwp/api/windows.devices.midi.midioutport.getdeviceselector)會傳回這個值。</span><span class="sxs-lookup"><span data-stu-id="aa840-118">This value is returned by [**MidiOutPort::GetDeviceSelector**](/uwp/api/windows.devices.midi.midioutport.getdeviceselector).</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="aa840-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="aa840-119">Requirements</span></span>



| <span data-ttu-id="aa840-120">需求</span><span class="sxs-lookup"><span data-stu-id="aa840-120">Requirement</span></span> | <span data-ttu-id="aa840-121">值</span><span class="sxs-lookup"><span data-stu-id="aa840-121">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa840-122">標頭</span><span class="sxs-lookup"><span data-stu-id="aa840-122">Header</span></span><br/> | <dl> <span data-ttu-id="aa840-123"><dt>Mmdeviceapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="aa840-123"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



 


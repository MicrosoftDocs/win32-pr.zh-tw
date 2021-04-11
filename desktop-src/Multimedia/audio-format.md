---
title: 音訊格式
description: 音訊格式
ms.assetid: a65dbd3f-1539-4f02-8573-c527c4e3c58d
keywords:
- WM_CAP_GET_AUDIOFORMAT 訊息
- capGetAudioFormat 宏
- capGetAudioFormatSize 宏
- WM_CAP_SET_AUDIOFORMAT 訊息
- capSetAudioFormat 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e362abd393097ae8763b44b3ee3474685ffd5c2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842147"
---
# <a name="audio-format"></a><span data-ttu-id="d7f4e-108">音訊格式</span><span class="sxs-lookup"><span data-stu-id="d7f4e-108">Audio Format</span></span>

<span data-ttu-id="d7f4e-109">您可以藉由將 [**WM \_ CAP \_ GET \_ AUDIOFORMAT**](wm-cap-get-audioformat.md) 訊息 (或 [**capGetAudioFormat**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformat) 和 [**capGetAudioFormatSize**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformatsize) 宏) 傳送至捕獲視窗，來取得音訊資料的目前捕捉格式或音訊格式結構的大小。</span><span class="sxs-lookup"><span data-stu-id="d7f4e-109">You can retrieve the current capture format for audio data or the size of the audio format structure by sending the [**WM\_CAP\_GET\_AUDIOFORMAT**](wm-cap-get-audioformat.md) message (or the [**capGetAudioFormat**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformat) and [**capGetAudioFormatSize**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformatsize) macros) to a capture window.</span></span> <span data-ttu-id="d7f4e-110">預設音訊捕捉格式為 mono、8位、11 kHz PCM (脈衝程式碼調製) 。</span><span class="sxs-lookup"><span data-stu-id="d7f4e-110">The default audio capture format is mono, 8-bit, 11 kHz PCM (Pulse Code Modulation).</span></span> <span data-ttu-id="d7f4e-111">當您使用 WM CAP GET AUDIOFORMAT 來取出格式時 \_ \_ \_ ，請一律使用 [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) 結構。</span><span class="sxs-lookup"><span data-stu-id="d7f4e-111">When you retrieve the format by using WM\_CAP\_GET\_AUDIOFORMAT, always use the [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) structure.</span></span>

<span data-ttu-id="d7f4e-112">您可以藉由將 [**WM \_ CAP \_ set \_ AUDIOFORMAT**](wm-cap-set-audioformat.md) message (或 [**capSetAudioFormat**](/windows/desktop/api/Vfw/nf-vfw-capsetaudioformat) 宏) 傳送至 capture 視窗，來設定音訊資料的捕捉格式。</span><span class="sxs-lookup"><span data-stu-id="d7f4e-112">You can set the capture format for audio data by sending the [**WM\_CAP\_SET\_AUDIOFORMAT**](wm-cap-set-audioformat.md) message (or the [**capSetAudioFormat**](/windows/desktop/api/Vfw/nf-vfw-capsetaudioformat) macro) to a capture window.</span></span> <span data-ttu-id="d7f4e-113">設定音訊格式時，您可以根據指定的音訊格式，將指標傳遞至 [**WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-waveformat)、 **WAVEFORMATEX** 或 [**PCMWAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-pcmwaveformat) 結構。</span><span class="sxs-lookup"><span data-stu-id="d7f4e-113">When setting the audio format, you can pass a pointer to a [**WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-waveformat), **WAVEFORMATEX**, or [**PCMWAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-pcmwaveformat) structure, depending on the specified audio format.</span></span>

 

 
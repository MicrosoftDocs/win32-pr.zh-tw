---
title: 波形音訊參考
description: 此區段會列出與波形音訊相關聯的函式、結構和訊息，這些功能是在 [多媒體參考] 下記載。 這些元素的分組方式如下。
ms.assetid: 723953f7-b38e-4f24-8d54-9849e013011d
keywords:
- Windows 多媒體，波形音訊參考
- 多媒體、波形音訊參考
- 多媒體音訊、波形參考
- 音訊、波形參考
- Windows 多媒體，波形音訊
- 多媒體、波形音訊
- 多媒體音訊、波形
- 音訊、波形
- 波形音訊，參考
- 波形音訊參考，關於
- wavefore 音訊的參考資料，關於
- 波形音訊參考，輔助裝置
- wavefore 音訊、輔助裝置的參考
- 波形音訊參考，播放
- wavefore 音訊、播放的參考
- 波形音訊參考，錯誤
- wavefore 音訊、錯誤的參考
- 波形音訊參考，開啟
- wavefore 音訊的參考，開啟
- 波形音訊參考，關閉
- wavefore 音訊的參考，關閉
- 波形音訊參考，音調
- wavefore 音訊、音調的參考
- 波形音訊參考，音量
- wavefore 音訊、磁片區的參考
- 波形音訊參考，訊息
- wavefore 音訊、訊息的參考
- 波形音訊參考，目前位置
- wavefore 音訊、目前位置的參考
- 波形音訊參考，錄製
- wavefore 音訊、錄製的參考
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c74b37984b2d3fab5dad1ea0df4f1f62dfa1855e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023386"
---
# <a name="waveform-audio-reference"></a>波形音訊參考

此區段會列出與波形音訊相關聯的函式、結構和訊息，這些功能是在 [ [多媒體參考](multimedia-reference.md)] 下記載。 這些元素的分組方式如下。

## <a name="auxiliary-devices"></a>輔助裝置

-   [**AUXCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-auxcaps)
-   [**auxGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetdevcaps)
-   [**auxGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs)
-   [**auxGetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetvolume)
-   [**auxOutMessage**](/windows/win32/api/mmeapi/nf-mmeapi-auxoutmessage)
-   [**auxSetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-auxsetvolume)

## <a name="easy-playback"></a>輕鬆播放

-   [**PlaySound**](/previous-versions//dd743680(v=vs.85))
-   [**sndPlaySound**](/previous-versions//dd798676(v=vs.85))

## <a name="errors"></a>Errors

-   [**waveInGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-waveingeterrortext)
-   [**waveOutGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgeterrortext)

## <a name="opening-and-closing"></a>開啟和關閉

-   [**PCMWAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-pcmwaveformat)
-   [**MM \_ WIM \_ 關閉**](mm-wim-close.md)
-   [**MM \_ WIM \_ 開啟**](mm-wim-open.md)
-   [**MM \_ WOM \_ 關閉**](mm-wom-close.md)
-   [**MM \_ WOM \_ 開啟**](mm-wom-open.md)
-   [**WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-waveformat)
-   [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex)
-   [**waveInClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveinclose)
-   [**waveInProc**](/previous-versions//dd743849(v=vs.85))
-   [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen)
-   [**waveOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutclose)
-   [**waveOutProc**](/previous-versions//dd743869(v=vs.85))
-   [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen)
-   [**WIM \_ 關閉**](wim-close.md)
-   [**WIM \_ 開啟**](wim-open.md)
-   [**WOM \_ 關閉**](wom-close.md)
-   [**WOM \_ 開啟**](wom-open.md)

## <a name="pitch"></a>音調

-   [**waveOutGetPitch**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetpitch)
-   [**waveOutSetPitch**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetpitch)

## <a name="playback-rate"></a>播放速率

-   [**waveOutGetPlaybackRate**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetplaybackrate)
-   [**waveOutSetPlaybackRate**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetplaybackrate)

## <a name="playback-progress"></a>播放進度

-   [**MM \_ WOM \_ 完成**](mm-wom-done.md)
-   [**waveOutBreakLoop**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutbreakloop)
-   [**waveOutPause**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutpause)
-   [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset)
-   [**waveOutRestart**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutrestart)
-   [**WOM \_ 完成**](wom-done.md)

## <a name="playing"></a>正在播放

-   [**MM \_ WOM \_ 完成**](mm-wom-done.md)
-   [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr)
-   [**waveOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader)
-   [**waveOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader)
-   [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite)
-   [**WOM \_ 完成**](wom-done.md)

## <a name="querying-a-device"></a>查詢裝置

-   [**WAVEINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveincaps)
-   [**waveInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetdevcaps)
-   [**waveInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetnumdevs)
-   [**WAVEOUTCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveoutcaps)
-   [**waveOutGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetdevcaps)
-   [**waveOutGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetnumdevs)

## <a name="recording"></a>記錄

-   [**MM \_ WIM \_ 資料**](mm-wim-data.md)
-   [**waveInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer)
-   [**waveInPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinprepareheader)
-   [**waveInReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset)
-   [**waveInStart**](/windows/win32/api/mmeapi/nf-mmeapi-waveinstart)
-   [**waveInStop**](/windows/win32/api/mmeapi/nf-mmeapi-waveinstop)
-   [**waveInUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinunprepareheader)
-   [**WIM \_ 資料**](wim-data.md)

## <a name="retrieving-device-identifiers"></a>正在抓取裝置識別碼

-   [**waveInGetID**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetid)
-   [**waveOutGetID**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetid)

## <a name="retrieving-the-current-position"></a>正在抓取目前的位置

-   [**waveInGetPosition**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetposition)
-   [**waveOutGetPosition**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetposition)

## <a name="sending-custom-messages"></a>傳送自訂訊息

-   [**waveInMessage**](/windows/win32/api/mmeapi/nf-mmeapi-waveinmessage)
-   [**waveOutMessage**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutmessage)

## <a name="volume"></a>磁碟區

-   [**waveOutGetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetvolume)
-   [**waveOutSetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetvolume)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[波形音訊](waveform-audio.md)
</dt> </dl>

 

 
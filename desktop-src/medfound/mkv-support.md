---
description: 本節說明 Matroska Media Container (.MKV) 檔的媒體基礎支援。
title: Matroska Media Container (.MKV) 支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aceb7a836b4a0409af3c359c8d81a0f232e6eb61082960cfb2b0705531de199c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119102138"
---
# <a name="matroska-media-container-mkv-support"></a>Matroska Media Container (.MKV) 支援

本節說明 Matroska Media Container (.MKV) 檔的媒體基礎支援。

.MKV 格式可支援多種影片和音訊編解碼器，例如 h.264 和 AAC 音訊。 一般而言，容器會描述影片和音訊資料的配置方式，以及用來描述這些 A/V 串流的補充資訊。 容器也可以包含輔助/V 資料流程的資料，例如標題、音訊串流的語言、副標題或字幕軌、這些字幕的字型、影像、章節資訊和功能表。 .MKV 是高度彈性的格式，可支援許多容器功能。 如需 .MKV 格式的詳細資訊，請參閱。 [https://matroska.org](https://matroska.org/)


## <a name="mkv-container-feature-support"></a>.MKV 容器功能支援
媒體基礎的 .MKV 容器功能可透過下列方式在中受到支援：
- 如果有一或多個影片曲目，將會播放第一個曲目。
- 如果有一或多個音訊曲目，將會播放第一個曲目。
- 支援字幕軌，但預設 (播放) 則不會選取這些字幕。
- 如果有一或多個字型或影像，則不會轉譯字幕和影像，雖然檔案將會載入並播放。
- 不支援且不會顯示功能表資訊，但會載入並播放檔案。
- 如果有章節的檔案參考補充檔案，則補充檔案將不會播放。
- 使用檔案瀏覽器流覽 USB 磁片磁碟機上的檔案時，可以使用縮圖影像。

如果包含支援的編解碼器，這組功能應該允許播放大部分的 .MKV 檔案。
支援包含以下節所列編解碼器編碼之影片和音訊播放軌的 .MKV 檔案。

## <a name="supported-mkv-codecs"></a>支援的 .MKV 編解碼器

### <a name="video-codec-support-for-mkv"></a>.MKV 的影片編解碼器支援

Matroska 識別碼： V_MPEG4/ISO/AVC

- MSFT 媒體基礎 MF_MT_SUBTYPE： MFVideoFormat_H264
- 描述： h.264 影片
- FourCC 或 WAV 識別碼： H264

Matroska 識別碼： V_MPEG2

- MSFT 媒體基礎 MF_MT_SUBTYPE： MFVideoFormat_MPEG2
- 描述： MPEG-2 影片

Matroska 識別碼： V_MPEG1

- MSFT 媒體基礎 MF_MT_SUBTYPE： MFVideoFormat_MPG1
- 描述： MPEG 1 影片
- FourCC 或 WAV 識別碼： MPG1

Matroska 識別碼： V_MPEG4/MS/V3

- MSFT 媒體基礎 MF_MT_SUBTYPE： MFVideoFormat_MP43
- 描述： Microsoft MPEG 4 編解碼器第3版
- FourCC 或 WAV 識別碼： MP43

Matroska 識別碼： V_MPEG4/ISO/ASP

- MSFT 媒體基礎 MF_MT_SUBTYPE： MFVideoFormat_MP4V
- 描述： MPEG 4 第2部分影片
- FourCC 或 WAV 識別碼： MP4V

Matroska 識別碼： V_MS/VFW/FOURCC

- 描述：地圖多個編解碼器，通常會以可在主控台上使用的 AVI 格式支援。

Matroska 識別碼： V_THEORA

- MSFT 媒體基礎 MF_MT_SUBTYPE： MFVideoFormat_Theora
- 描述： Theora
- FourCC 或 WAV 識別碼： theo

Matroska 識別碼： V_MPEG4/ISO/SP

- MSFT 媒體基礎 MF_MT_SUBTYPE： MFVideoFormat_MP4V
- 描述： MPEG4 ISO 簡單設定檔 (DivX4) 
- FourCC 或 WAV 識別碼： MP4V

Matroska 識別碼： V_MPEG4/ISO/AP

- MSFT 媒體基礎 MF_MT_SUBTYPE： MFVideoFormat_MP4V
- 描述： MPEG4 ISO advanced 簡單設定檔 (DivX5、XviD、FFMPEG) 
- FourCC 或 WAV 識別碼： MP4V


Matroska 識別碼： V_MPEGH/ISO/HEVC 

- MSFT 媒體基礎 MF_MT_SUBTYPE： MFVideoFormat_HEVC
- 描述： HEVC/。H
- FourCC 或 WAV 識別碼： 

Matroska 識別碼： V_VP8

- MSFT 媒體基礎 MF_MT_SUBTYPE： MFVideoFormat_VP80
- 描述： VP8 編解碼器格式
- FourCC 或 WAV 識別碼： VP80

Matroska 識別碼： V_VP9

- MSFT 媒體基礎 MF_MT_SUBTYPE： MFVideoFormat_VP90
- 描述： VP9 編解碼器格式
- FourCC 或 WAV 識別碼： VP90

Matroska 識別碼： V_MJPEG

- MSFT 媒體基礎 MF_MT_SUBTYPE： MFVideoFormat_MJPG
- 描述：動畫 JPEG
- FourCC 或 WAV 識別碼： MJPG

Matroska 識別碼： V_AV1

- MSFT 媒體基礎 MF_MT_SUBTYPE： MFVideoFormat_AV1
- 描述： AOMedia Video 1
- FourCC 或 WAV 識別碼： AV01

### <a name="audio-codec-support-for-mkv"></a>.MKV 的音訊編解碼器支援

Matroska 識別碼： A_AAC

- MSFT 媒體基礎 MF_MT_SUBTYPE： MFAudioFormat_AAC
- 描述： Advanced Audio 編碼 (AAC) 
- FourCC 或 WAV 識別碼： WAVE_FORMAT_MPEG_HEAAC

Matroska 識別碼： A_AC3

- MSFT 媒體基礎 MF_MT_SUBTYPE： MFAudioFormat_Dolby_AC3
- 描述：杜 AC3
- FourCC 或 WAV 識別碼： WAVE_FORMAT_DOLBY_AC3_SPDIF

Matroska 識別碼： A_MPEG/L3

- MSFT 媒體基礎 MF_MT_SUBTYPE： MFAudioFormat_MP3
- 描述： MPEG 音訊第3層 (MP3) 
- FourCC 或 WAV 識別碼： WAVE_FORMAT_MPEGLAYER3

Matroska 識別碼： A_MPEG/L1

- MSFT 媒體基礎 MF_MT_SUBTYPE： MFAudioFormat_MPEG
- 描述： MPEG-2 音訊承載
- FourCC 或 WAV 識別碼： WAVE_FORMAT_MPEG

Matroska 識別碼： A_PCM/INT/BIG

- MSFT 媒體基礎 MF_MT_SUBTYPE： MFAudioFormat_PCM
- 描述：未壓縮的 PCM 音訊
- FourCC 或 WAV 識別碼： WAVE_FORMAT_PCM

Matroska 識別碼： A_PCM/INT/LIT

- MSFT 媒體基礎 MF_MT_SUBTYPE： MFAudioFormat_PCM
- 描述：未壓縮的 PCM 音訊
- FourCC 或 WAV 識別碼： WAVE_FORMAT_PCM

Matroska 識別碼： A_PCM/FLOAT/IEEE

- MSFT 媒體基礎 MF_MT_SUBTYPE： MFAudioFormat_Float
- 描述：未壓縮的 IEEE 浮點音訊
- FourCC 或 WAV 識別碼： WAVE_FORMAT_IEEE_FLOAT

Matroska 識別碼： A_ALAC

- MSFT 媒體基礎 MF_MT_SUBTYPE： MFAudioFormat_ALAC
- 描述： Apple 無損音訊編解碼器
- FourCC 或 WAV 識別碼： 

Matroska 識別碼： A_MPEG/L2

- MSFT 媒體基礎 MF_MT_SUBTYPE： MFAudioFormat_MPEG
- 描述： MPEG 音訊1、2層 II
- FourCC 或 WAV 識別碼： WAVE_FORMAT_MPEG

Matroska 識別碼： A_DTS

- MSFT 媒體基礎 MF_MT_SUBTYPE： MEDIASUBTYPE_DTS_HD
- 描述：數位劇院系統
- FourCC 或 WAV 識別碼： WAVE_FORMAT_DTS

Matroska 識別碼： A_OPUS

- MSFT 媒體基礎 MF_MT_SUBTYPE： MFAudioFormat_Opus
- 描述： Opus
- FourCC 或 WAV 識別碼： WAVE_FORMAT_OPUS

Matroska 識別碼： A_VORBIS

- MSFT 媒體基礎 MF_MT_SUBTYPE： MFAudioFormat_Vorbis
- 描述： Vorbis
- FourCC 或 WAV 識別碼： 

Matroska 識別碼： A_FLAC

- MSFT 媒體基礎 MF_MT_SUBTYPE： MFAudioFormat_FLAC
- 描述：無失真音訊編解碼器
- FourCC 或 WAV 識別碼： WAVE_FORMAT_FLAC

Matroska ID： A_AAC/MAIN

- MSFT 媒體基礎 MF_MT_SUBTYPE： MFAudioFormat_AAC
- 描述： Advanced Audio 編碼 (AAC) 
- FourCC 或 WAV 識別碼： WAVE_FORMAT_MPEG_HEAAC

Matroska 識別碼： A_EAC3

- MSFT 媒體基礎 MF_MT_SUBTYPE： MFAudioFormat_Dolby_DDPlus
- 描述：增強的 AC-3
- FourCC 或 WAV 識別碼： 

Matroska 識別碼： A_TRUEHD

- MSFT 媒體基礎 MF_MT_SUBTYPE： MEDIASUBTYPE_DOLBY_TRUEHD
- 描述：杜 TrueHD
- FourCC 或 WAV 識別碼： 

Matroska 識別碼： A_MS/ACM

- MSFT 媒體基礎 MF_MT_SUBTYPE：地圖至 mmreg 中定義的數個 WAVE_FORMAT 音訊類型


### <a name="subtitles-codec-support-for-mkv"></a>.MKV 的字幕編解碼器支援

Matroska 識別碼： S_TEXT/ASCII

- MSFT 媒體基礎 MF_MT_SUBTYPE： MFSubtitleFormat_SRT
- 描述： ASCII 文字

Matroska 識別碼： S_TEXT/UTF8

- MSFT 媒體基礎 MF_MT_SUBTYPE： MFSubtitleFormat_SRT
- 描述： UTF-8 純文字

Matroska 識別碼： S_TEXT/SSA

- MSFT 媒體基礎 MF_MT_SUBTYPE： MFSubtitleFormat_SSA
- 描述：字幕格式

Matroska 識別碼： S_TEXT/ASS

- MSFT 媒體基礎 MF_MT_SUBTYPE： MFSubtitleFormat_SSA
- 描述： Advanced 字幕格式

Matroska 識別碼： S_VOBSUB

- MSFT 媒體基礎 MF_MT_SUBTYPE： MFSubtitleFormat_VobSub
- 描述： VobSub 字幕

Matroska 識別碼： S_HDMV/PGS

- MSFT 媒體基礎 MF_MT_SUBTYPE： MFSubtitleFormat_PGS
- 描述： HDMV 簡報圖形副標題 (PG) 


## <a name="technical-details-regarding-codecs"></a>編解碼器的相關技術詳細資料

如需編解碼器的相關技術詳細資料，請參閱下列各項。

- [Matroska 編解碼器規格](http://www.matroska.org/technical/specs/codecid/index.html)
- [音訊子類型 Guid](audio-subtype-guids.md)
- [影片子類型 Guid](video-subtype-guids.md)


## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體基礎中支援的媒體格式](supported-media-formats-in-media-foundation.md)
</dt> <dt>

[媒體基礎程式設計指南](media-foundation-programming-guide.md)
</dt> </dl>

 

 




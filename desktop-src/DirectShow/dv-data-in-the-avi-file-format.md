---
description: AVI 檔案格式的 DV 資料
ms.assetid: ae1ec184-afc3-4ec1-9b92-f53656293446
title: AVI 檔案格式的 DV 資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c048cb42fa3ba49457c115944075c064b9cfd4c31263519e9d5af3e5f0a268a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749108"
---
# <a name="dv-data-in-the-avi-file-format"></a>AVI 檔案格式的 DV 資料

Microsoft 已指定在 AVI 檔案中儲存數位視訊 (DV) 資料的格式。 符合此規格可確保以這種格式撰寫的 AVI 檔案，將與 Windowsplatform 的 DirectShow 數位影片架構的未來版本相容。

本文描述包含 DV 資料的 AVI 檔案格式。 特定 FOURCCs (四個字元的程式碼) ，用於交錯式 DV 資料流程和 DV 壓縮/解壓縮程式串流處理常式。 已定義 DV 資料的資料流程格式結構。 指定以 AVI 檔案格式儲存 DV 資料的兩種方法規格。

假設讀者已熟悉 DV 資料格式。  (此格式定義于取用 *者使用的數位 Vcr 規格* 中，也稱為藍色書籍。 ) 

有兩種類型的 DV AVI 檔案： AVI 檔案，其中包含一個 DV 資料流程，稱為 *type-1* files;以及包含 DV 影片作為「vids」資料流程和 DV 音訊做為「auds」串流（稱為 *類型 2* 檔案）的 AVI 檔。

**包含一個 DV 資料流程的 AVI 檔案 (類型 1)**

交錯的 DV 資料可以用原生格式儲存為 AVI RIFF 檔中的單一資料流程。 這有一個優點，就是使用 DV 的資料儲存體的最小數量。 主要的缺點是，這種檔案格式與影片的 Windows 不相容，因為它不包含影片 ' vids ' 或音訊 ' auds ' 資料流程。 支援是透過 DirectShow 所提供的[Dv Muxer](dv-muxer-filter.md)和[dv 分隔](dv-splitter-filter.md)器篩選器，提供給交錯的 dv 串流使用。

您可以藉由指定 ' iavs ' (交錯音訊和影片資料流程，將 DV 資料儲存在單一資料流程中，) FOURCC (**fccType** 成員中的四字元程式碼) ，以及 ' dvsd ' 資料流程標頭區塊之 **dvhd** 成員中的 ' dvsl '、' FOURCCs ' 或 ' fccHandler ' strh。 影片串流的每秒畫面格必須指定在 **dwRate** 和 **dwScale** 成員中，以及 **dwLength** 成員中 ' movi ' 區塊內的影片區塊總數。

' Dvsd ' 資料流程處理常式 FOURCC 指定 DV 資料在取用 *者使用數位 vcr* 的第2部分中定義。 影片的格式為525行 29.97 Hz (525-60) 或625線，25.00 Hz (625-50) 。

' Dvhd ' 資料流程處理常式 FOURCC 指定 DV 資料在取用 *者-使用數位 Vcr 規格* 的第3部分中定義。 影片的格式為1125行 30.00 Hz (1125-60) 或1250線，25.00 Hz (1250-50) 。

' Dvsl ' 資料流程處理常式 FOURCC 指定 DV 資料在取用 *者使用數位 vcr* 的第6部分中定義。 影片的格式為高壓縮 SD (SDL) 。

> [!Note]  
> 本文的其餘部分會提供 ' dvsd ' 資料流程的定義。

 

資料流程標頭區塊後面必須接著 [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo) 資料流程格式區塊。

實際的 DV 資料會在 \# \# ' movi ' 區塊中儲存為 ' dc ' 區塊 (\# \# 格式代表資料流程識別碼) 。 每個區塊都包含一個資料框架，分別是10或12個適用于525-60 或625-50 系統的 DV DIF 序列。 DV SD ( ' dvsd ' ) DIF 順序格式，定義于取用 *者使用數位 vcr* 的第2部分。

下列範例顯示具有一個 DV 資料流程之 AVI 檔案的 .AIFF RIFF 表單，以已完成的標頭區塊擴充。


```C++
00000000 RIFF (0FAE35D4) 'AVI '
0000000C     LIST (00000106) 'hdrl'
00000018         avih (00000038)
                     dwMicroSecPerFrame    : 33367
                     dwMaxBytesPerSec      : 3728000
                     dwPaddingGranularity  : 0
                     dwFlags               : 0x810 HASINDEX | TRUSTCKTYPE
                     dwTotalFrames         : 2192
                     dwInitialFrames       : 0
                     dwStreams             : 1
                     dwSuggestedBufferSize : 120000
                     dwWidth               : 720
                     dwHeight              : 480
                     dwReserved            : 0x0
00000058         LIST (0000006C) 'strl'
00000064             strh (00000038)
                         fccType               : 'iavs'
                         fccHandler            : 'dvsd'
                         dwFlags               : 0x0
                         wPriority             : 0
                         wLanguage             : 0x0 undefined
                         dwInitialFrames       : 0
                         dwScale               : 100 (29.970 Frames/Sec)
                         dwRate                : 2997
                         dwStart               : 0
                         dwLength              : 2192
                         dwSuggestedBufferSize : 120000
                         dwQuality             : 0
                         dwSampleSize          : 0
                         rcFrame               : 0,0,720,480
000000A4             strf (00000020)
                         dwDVAAuxSrc     : 0x........
                         dwDVAAuxCtl     : 0x........
                         dwDVAAuxSrc1    : 0x........
                         dwDVAAuxCtl1    : 0x........
                         dwDVVAuxSrc     : 0x........
                         dwDVVAuxCtl     : 0x........
                         dwDVReserved[2] : 0,0
000000CC     LIST (0FADAC00) 'movi'
0FADACD4     idx1 (00008900)
```



**包含 DV 影片和 DV 音訊串流的 AVI 檔案 (類型 2)**

交錯的 DV 資料可以分割成影片串流，以及 AVI RIFF 檔案內的一到四個音訊串流。 這項功能的優點是與影片進行回溯相容，以進行 Windows，因為它包含標準的影片 ' vids ' 資料流程和至少一個標準音頻 ' auds ' 資料流程，主要的缺點是此檔案格式需要將音訊資料重複儲存為音訊串流。 「影片」資料流程實際上是原生交錯的 DV 資料流程。 但是，如果是處理類型為 ' dvsd ' 的標準 ' vids ' 資料流程，則會使用 [DV 影片解碼](dv-video-decoder-filter.md) 。 此格式也需要使用 [DV 分隔](dv-splitter-filter.md) 器篩選器來分割「已捕捉」檔案，然後再將它們寫入為 AVI 檔案。

DV 資料可以儲存為具有 AVI RIFF 檔中不同音訊串流數目的影片串流。 影片資料流程是使用標準的影片資料流程標頭所指定 (**fccType** 成員值為 ' vids ' ) 。 **FccHandler** 成員指定為 ' dvsd '、' dvhd ' 或 ' dvsl '。 影片串流的每秒畫面格必須指定在 **dwRate** 和 **dwScale** 成員中，以及 **dwLength** 成員中 ' movi ' 區塊內的影片區塊總數。

在這個包含 DV 影片的 AVI 檔案中，以「vids」資料流程和 DV 音訊做為「auds」資料流程形式的 DV，影片串流格式區塊是標準的 [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) 結構。 您可以選擇性地擴充資料流程格式區塊，以包含 [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo) 區塊，方法是將資料流程格式區塊大小從40個位元組增加 (**BITMAPINFOHEADER** 結構的大小) 為72個位元組 (**BITMAPINFOHEADER** 加 **DVINFO**) 結構的大小，然後緊接在 **BITMAPINFOHEADER** 資料結構 **的 DVINFO 資料** 結構後面。

音訊串流 (s) 是使用標準音頻資料流程標頭所指定， (**fccType** 成員值為 ' auds ' ) 。 **FccHandler** 成員不會用於音訊串流。

DV 影片資料會以「dc」 \# \# 區塊的形式儲存（如先前的 AVI 檔案描述中所定義，其中包含一個 DV 資料），而音訊資料會 \# \# 在 ' movi ' 區塊中儲存為 ' wb ' 區塊。

> [!Note]  
> 某些語言和國家/地區可能不提供取用 *者使用數位 vcr 的規格* 。

 

下列範例顯示包含 DV 影片作為「vids」資料流程的 AVI 檔案的 .AIFF RIFF 表單，以及以已完成的標頭區塊擴充的 DV 音訊做為 ' auds ' 資料流程的表單 (包括在 ' BITMAPINFO ' 子區塊的 [**strf**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo)中，于 "vids ' 資料流程) 之後的選擇性 [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo)資料。


```C++
00000000 RIFF (103E2920) 'AVI '
0000000C     LIST (00000146) 'hdrl'
00000018         avih (00000038)
                     dwMicroSecPerFrame    : 33367
                     dwMaxBytesPerSec      : 3728000
                     dwPaddingGranularity  : 0
                     dwFlags               : 0x810 HASINDEX | TRUSTCKTYPE
                     dwTotalFrames         : 2192
                     dwInitialFrames       : 0
                     dwStreams             : 2
                     dwSuggestedBufferSize : 120000
                     dwWidth               : 720
                     dwHeight              : 480
                     dwReserved            : 0x0
00000058         LIST (00000094) 'strl'
00000064             strh (00000038)
                         fccType               : 'vids'
                         fccHandler            : 'dvsd'
                         dwFlags               : 0x0
                         wPriority             : 0
                         wLanguage             : 0x0 undefined
                         dwInitialFrames       : 0
                         dwScale               : 100 (29.970 Frames/Sec)
                         dwRate                : 2997
                         dwStart               : 0
                         dwLength              : 2192
                         dwSuggestedBufferSize : 120000
                         dwQuality             : 0
                         dwSampleSize          : 0
                         rcFrame               : 0,0,720,480
000000A4             strf (00000048)
                         biSize          : 40
                         biWidth         : 720
                         biHeight        : 480
                         biPlanes        : 1
                         biBitCount      : 24
                         biCompression   : 0x64737664 'dvsd'
                         biSizeImage     : 120000
                         biXPelsPerMeter : 0
                         biYPelsPerMeter : 0
                         biClrUsed       : 0
                         biClrImportant  : 0
                         dwDVAAuxSrc     : 0x........
                         dwDVAAuxCtl     : 0x........
                         dwDVAAuxSrc1    : 0x........
                         dwDVAAuxCtl1    : 0x........
                         dwDVVAuxSrc     : 0x........
                         dwDVVAuxCtl     : 0x........
                         dwDVReserved[2] : 0,0
000000F4         LIST (0000005E) 'strl'
00000100             strh (00000038)
                         fccType               : 'auds'
                         fccHandler            : '    '
                         dwFlags               : 0x0
                         wPriority             : 0
                         wLanguage             : 0x0 undefined
                         dwInitialFrames       : 0
                         dwScale               : 1 (32000.000 Samples/Sec)
                         dwRate                : 32000
                         dwStart               : 0
                         dwLength              : 2340474
                         dwSuggestedBufferSize : 4272
                         dwQuality             : 0
                         dwSampleSize          : 4
                         rcFrame               : 0,0,0,0
00000140             strf (00000012)
                         wFormatTag      : 1 PCM
                         nChannels       : 2
                         nSamplesPerSec  : 32000
                         nAvgBytesPerSec : 128000
                         nBlockAlign     : 4
                         wBitsPerSample  : 16
                         cbSize          : 0
00000814     LIST (103D0EF4) 'movi'
103D1710     idx1 (00011210)
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[AVI 檔案格式](avi-file-format.md)
</dt> </dl>

 

 

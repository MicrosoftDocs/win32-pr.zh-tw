---
title: AVIFile 參考
description: AVIFile 參考
ms.assetid: 73532d83-89c2-4911-8558-ce110e9f0f95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0291d0ac5864a9b370e79a98fa061770d05bca03
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104022001"
---
# <a name="avifile-reference"></a>AVIFile 參考

本節說明使用 AVIFile 服務之應用程式的函式、結構和宏。 這些元素的分組方式如下：

## <a name="avifile-library-operations"></a>AVIFile 程式庫作業

-   [**AVIFileInit**](/windows/desktop/api/Vfw/nf-vfw-avifileinit)
-   [**AVIFileExit**](/windows/desktop/api/Vfw/nf-vfw-avifileexit)

## <a name="opening-and-closing-avi-files"></a>開啟和關閉 AVI 檔案

-   [**AVIFileOpen**](/windows/desktop/api/Vfw/nf-vfw-avifileopen)
-   [**AVIFileAddRef**](/windows/desktop/api/Vfw/nf-vfw-avifileaddref)
-   [**AVIFileRelease**](/windows/desktop/api/Vfw/nf-vfw-avifilerelease)
-   [**GetOpenFileNamePreview**](/windows/desktop/api/Vfw/nf-vfw-getopenfilenamepreviewa)

## <a name="reading-from-a-file"></a>從檔案讀取

-   [**AVIFileInfo**](/windows/desktop/api/Vfw/nf-vfw-avifileinfo)
-   [**AVIFILEINFO**](/windows/desktop/api/Vfw/ns-vfw-avifileinfoa)
-   [**AVIFileReadData**](/windows/desktop/api/Vfw/nf-vfw-avifilereaddata)

## <a name="writing-to-a-file"></a>寫入檔案

-   [**AVIFileWriteData**](/windows/desktop/api/Vfw/nf-vfw-avifilewritedata)

## <a name="using-the-clipboard"></a>使用剪貼簿

-   [**AVIPutFileOnClipboard**](/windows/desktop/api/Vfw/nf-vfw-aviputfileonclipboard)
-   [**AVIGetFromClipboard**](/windows/desktop/api/Vfw/nf-vfw-avigetfromclipboard)
-   [**AVIClearClipboard**](/windows/desktop/api/Vfw/nf-vfw-aviclearclipboard)

## <a name="opening-and-closing-streams"></a>開啟和關閉資料流程

-   [**AVIFileGetStream**](/windows/desktop/api/Vfw/nf-vfw-avifilegetstream)
-   [**AVIStreamOpenFromFile**](/windows/desktop/api/Vfw/nf-vfw-avistreamopenfromfilea)
-   [**AVIStreamAddRef**](/windows/desktop/api/Vfw/nf-vfw-avistreamaddref)
-   [**AVIStreamRelease**](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease)

## <a name="reading-stream-information"></a>讀取資料流程資訊

-   [**AVISTREAMINFO**](/windows/desktop/api/Vfw/ns-vfw-avistreaminfoa)
-   [**AVIStreamReadData**](/windows/desktop/api/Vfw/nf-vfw-avistreamreaddata)
-   [**AVIStreamDataSize**](/windows/desktop/api/Vfw/nf-vfw-avistreamdatasize)
-   [**AVIStreamReadFormat**](/windows/desktop/api/Vfw/nf-vfw-avistreamreadformat)
-   [**AVIStreamFormatSize**](/windows/desktop/api/Vfw/nf-vfw-avistreamformatsize)
-   [**AVIStreamRead**](/windows/desktop/api/Vfw/nf-vfw-avistreamread)
-   [**AVIStreamSampleSize**](/windows/desktop/api/Vfw/nf-vfw-avistreamsamplesize)
-   [**AVIStreamBeginStreaming**](/windows/desktop/api/Vfw/nf-vfw-avistreambeginstreaming)
-   [**AVIStreamEndStreaming**](/windows/desktop/api/Vfw/nf-vfw-avistreamendstreaming)

## <a name="decompressing-video-data-in-a-stream"></a>在資料流程中解壓縮影片資料

-   [**AVIStreamGetFrameOpen**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframeopen)
-   [**AVIStreamGetFrame**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframe)
-   [**AVIStreamGetFrameClose**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframeclose)

## <a name="creating-a-file-from-existing-streams"></a>從現有的資料流程建立檔案

-   [**AVISave**](/windows/desktop/api/Vfw/nf-vfw-avisavea)
-   [**AVISaveV**](/windows/desktop/api/Vfw/nf-vfw-avisaveva)
-   [**AVISaveOptions**](/windows/desktop/api/Vfw/nf-vfw-avisaveoptions)
-   [**GetSaveFileNamePreview**](/windows/desktop/api/Vfw/nf-vfw-getsavefilenamepreviewa)
-   [**AVIMakeFileFromStreams**](/windows/desktop/api/Vfw/nf-vfw-avimakefilefromstreams)

## <a name="writing-individual-streams"></a>撰寫個別資料流程

-   [**AVIFileCreateStream**](/windows/desktop/api/Vfw/nf-vfw-avifilecreatestream)
-   [**AVIStreamSetFormat**](/windows/desktop/api/Vfw/nf-vfw-avistreamsetformat)
-   [**AVIStreamWrite**](/windows/desktop/api/Vfw/nf-vfw-avistreamwrite)
-   [**AVIFileWriteData**](/windows/desktop/api/Vfw/nf-vfw-avifilewritedata)
-   [**AVIStreamWriteData**](/windows/desktop/api/Vfw/nf-vfw-avistreamwritedata)
-   [**AVIStreamRelease**](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease)

## <a name="finding-the-starting-position-in-a-stream"></a>尋找資料流程中的開始位置

-   [**AVIStreamStart**](/windows/desktop/api/Vfw/nf-vfw-avistreamstart)
-   [**AVIStreamStartTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamstarttime)
-   [**AVIStreamLength**](/windows/desktop/api/Vfw/nf-vfw-avistreamlength)
-   [**AVIStreamLengthTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamlengthtime)
-   [**AVIStreamFindSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamfindsample)
-   [**AVIStreamEnd**](/windows/desktop/api/Vfw/nf-vfw-avistreamend)
-   [**AVIStreamEndTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamendtime)

## <a name="finding-sample-and-key-frames"></a>尋找範例和主要畫面格

-   [**AVIStreamFindSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamfindsample)
-   [**AVIStreamIsKeyFrame**](/windows/desktop/api/Vfw/nf-vfw-avistreamiskeyframe)
-   [**AVIStreamNearestKeyFrame**](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestkeyframe)
-   [**AVIStreamNearestKeyFrameTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestkeyframetime)
-   [**AVIStreamNearestSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestsample)
-   [**AVIStreamNearestSampleTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestsampletime)
-   [**AVIStreamNextKeyFrame**](/windows/desktop/api/Vfw/nf-vfw-avistreamnextkeyframe)
-   [**AVIStreamNextKeyFrameTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamnextkeyframetime)
-   [**AVIStreamNextSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamnextsample)
-   [**AVIStreamNextSampleTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamnextsampletime)
-   [**AVIStreamPrevKeyFrame**](/windows/desktop/api/Vfw/nf-vfw-avistreamprevkeyframe)
-   [**AVIStreamPrevKeyFrameTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamprevkeyframetime)
-   [**AVIStreamPrevSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamprevsample)
-   [**AVIStreamPrevSampleTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamprevsampletime)
-   [**AVIStreamSampleToSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamsampletosample)

## <a name="switching-between-samples-and-time"></a>在範例和時間之間切換

-   [**AVIStreamSampleToTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamsampletotime)
-   [**AVIStreamTimeToSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamtimetosample)

## <a name="creating-temporary-streams"></a>建立暫存資料流程

-   [**AVIStreamCreate**](/windows/desktop/api/Vfw/nf-vfw-avistreamcreate)
-   [**AVIMakeCompressedStream**](/windows/desktop/api/Vfw/nf-vfw-avimakecompressedstream)
-   [**AVIStreamRelease**](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease)

## <a name="editing-avi-streams"></a>編輯 AVI 資料流程

-   [**CreateEditableStream**](/windows/desktop/api/Vfw/nf-vfw-createeditablestream)
-   [**EditStreamCut**](/windows/desktop/api/Vfw/nf-vfw-editstreamcut)
-   [**EditStreamCopy**](/windows/desktop/api/Vfw/nf-vfw-editstreamcopy)
-   [**EditStreamPaste**](/windows/desktop/api/Vfw/nf-vfw-editstreampaste)
-   [**EditStreamClone**](/windows/desktop/api/Vfw/nf-vfw-editstreamclone)
-   [**EditStreamSetInfo**](/windows/desktop/api/Vfw/nf-vfw-editstreamsetinfoa)
-   [**EditStreamSetName**](/windows/desktop/api/Vfw/nf-vfw-editstreamsetnamea)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[AVIFile 函式和宏](avifile-functions-and-macros.md)
</dt> </dl>

 

 





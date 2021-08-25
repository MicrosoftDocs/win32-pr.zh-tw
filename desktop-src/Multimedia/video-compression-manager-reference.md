---
title: 影片壓縮管理員參考
description: 影片壓縮管理員參考
ms.assetid: dd678b24-62af-495f-bdd6-3082c1a753dd
keywords:
- '影片 Windows (VFW) 、視訊壓縮管理員 (bc-vcm-lvm-hyperv) '
- '適用于 Windows) 的 VFW (影片、視訊壓縮管理員 (bc-vcm-lvm-hyperv) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adffe57bd731736ed434dfdfa3c4ded4e643c66a0b5f9ea1c6085a71285e45c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119804268"
---
# <a name="video-compression-manager-reference"></a>影片壓縮管理員參考

本節說明與 BC-VCM-LVM-HYPERV 相關聯的函式、結構、訊息和宏。 這些元素的分組方式如下。

## <a name="compressor-installation-and-removal"></a>壓縮安裝和移除

-   [**ICInstall**](/windows/desktop/api/Vfw/nf-vfw-icinstall)
-   [**ICLocate**](/windows/desktop/api/Vfw/nf-vfw-iclocate)
-   [**ICOPEN**](/windows/desktop/api/Vfw/ns-vfw-icopen)
-   [**ICClose**](/windows/desktop/api/Vfw/nf-vfw-icclose)
-   [**ICRemove**](/windows/desktop/api/Vfw/nf-vfw-icremove)
-   [**ICOpenFunction**](/windows/desktop/api/Vfw/nf-vfw-icopenfunction)

## <a name="locating-and-opening-a-compressor"></a>尋找和開啟壓縮

-   [**ICLocate**](/windows/desktop/api/Vfw/nf-vfw-iclocate)
-   [**ICOPEN**](/windows/desktop/api/Vfw/ns-vfw-icopen)
-   [**ICDecompressOpen**](/windows/desktop/api/Vfw/nf-vfw-icdecompressopen)
-   [**ICDrawOpen**](/windows/desktop/api/Vfw/nf-vfw-icdrawopen)
-   [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo)
-   [**ICClose**](/windows/desktop/api/Vfw/nf-vfw-icclose)

## <a name="selecting-compressors"></a>選取壓縮機

-   [**ICCompressorChoose**](/windows/desktop/api/Vfw/nf-vfw-iccompressorchoose)
-   [**ICCompressorFree**](/windows/desktop/api/Vfw/nf-vfw-iccompressorfree)
-   [**COMPVARS**](/windows/desktop/api/Vfw/ns-vfw-compvars)

## <a name="configuring-compressors"></a>設定壓縮機

-   [**ICM \_配置**](icm-configure.md)
-   [**ICM \_>GETSTATE**](icm-getstate.md)
-   [**ICM \_SETSTATE**](icm-setstate.md)
-   [**ICSendMessage**](/windows/desktop/api/Vfw/nf-vfw-icsendmessage)

## <a name="compressor-information"></a>壓縮資訊

-   [**ICGetInfo**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo)
-   [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo)
-   [**ICM \_GETDEFAULTKEYFRAMERATE**](icm-getdefaultkeyframerate.md)
-   [**ICGetDisplayFormat**](/windows/desktop/api/Vfw/nf-vfw-icgetdisplayformat)
-   [**ICM \_GETDEFAULTQUALITY**](icm-getdefaultquality.md)
-   [**ICM \_詢問**](icm-about.md)

## <a name="single-image-compression"></a>單一影像壓縮

-   [**ICImageCompress**](/windows/desktop/api/Vfw/nf-vfw-icimagecompress)

## <a name="sequence-compression"></a>序列壓縮

-   [**ICSeqCompressFrame**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframe)
-   [**ICSeqCompressFrameStart**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframestart)
-   [**ICSeqCompressFrameEnd**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframeend)

## <a name="compvars"></a>COMPVARS

-   [**ICCompressorChoose**](/windows/desktop/api/Vfw/nf-vfw-iccompressorchoose)

## <a name="image-data-compression"></a>影像資料壓縮

-   [**ICCOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-iccompress)
-   [**ICM \_壓縮 \_ 取得 \_ 格式**](icm-compress-get-format.md)
-   [**ICM \_壓縮 \_ 查詢**](icm-compress-query.md)
-   [**ICM \_壓縮 \_ 取得 \_ 大小**](icm-compress-get-size.md)
-   [**ICM \_壓縮 \_ 開始**](icm-compress-begin.md)
-   [**ICM \_壓縮 \_ 結束**](icm-compress-end.md)

## <a name="compressor-monitoring"></a>壓縮監視

-   [**ICSETSTATUSPROC**](/windows/desktop/api/Vfw/ns-vfw-icsetstatusproc)

## <a name="decompressing-single-images"></a>解壓縮單一映射

-   [**ICImageDecompress**](/windows/desktop/api/Vfw/nf-vfw-icimagedecompress)

## <a name="decompressing-image-data"></a>解壓縮映射資料

-   [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex)
-   [**ICDecompressExBegin**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexbegin)
-   [**ICM \_DECOMPRESSEX \_ 結束**](icm-decompressex-end.md)
-   [**ICM \_解壓縮 \_ 取得 \_ 格式**](icm-decompress-get-format.md)
-   [**ICM \_解壓縮 \_ 取得 \_ 調色板**](icm-decompress-get-palette.md)
-   [**ICDecompressExQuery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexquery)
-   [**ICDECOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-icdecompress)
-   [**ICM \_解壓縮 \_ 開始**](icm-decompress-begin.md)
-   [**ICM \_解壓縮 \_ 結束**](icm-decompress-end.md)
-   [**ICM \_解壓縮 \_ 查詢**](icm-decompress-query.md)

## <a name="using-hardware-drawing-capabilities"></a>使用 Hardware-Drawing 功能

-   [**ICGetInfo**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo)
-   [**ICDRAWBEGIN**](/windows/desktop/api/Vfw/ns-vfw-icdrawbegin)
-   [**ICM \_繪製 \_ 結束**](icm-draw-end.md)
-   [**ICM \_繪製 \_ FLUSH**](icm-draw-flush.md)
-   [**ICM \_繪製 \_ 查詢**](icm-draw-query.md)
-   [**ICDrawSuggestFormat**](/windows/desktop/api/Vfw/nf-vfw-icdrawsuggestformat)
-   [**ICM \_繪製 \_ 開始**](icm-draw-start.md)
-   [**ICM \_繪圖 \_ 停止**](icm-draw-stop.md)
-   [**ICM \_GETBUFFERSWANTED**](icm-getbufferswanted.md)
-   [**ICM \_繪圖 \_ 實現**](icm-draw-realize.md)
-   [**ICDrawOpen**](/windows/desktop/api/Vfw/nf-vfw-icdrawopen)
-   [**ICDRAW**](/windows/desktop/api/Vfw/ns-vfw-icdraw)
-   [**ICM \_繪製 \_ GETTIME**](icm-draw-gettime.md)
-   [**ICM \_繪製 \_ SETTIME**](icm-draw-settime.md)
-   [**ICM \_繪圖 \_ 視窗**](icm-draw-window.md)
-   [**ICM \_繪圖 \_ 實現**](icm-draw-realize.md)
-   [**ICM \_繪製 \_ CHANGEPALETTE**](icm-draw-changepalette.md)
-   [**ICM \_繪製 \_ RENDERBUFFER**](icm-draw-renderbuffer.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[影片壓縮管理員](video-compression-manager.md)
</dt> </dl>

 

 





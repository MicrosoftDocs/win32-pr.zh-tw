---
description: 檔案編碼和解碼介面
ms.assetid: 5456392d-2557-43b6-93b7-b2ebde218d12
title: 檔案編碼和解碼介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f73de2304f2b473a634127755ca900b99592ed63
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109897"
---
# <a name="file-encoding-and-decoding-interfaces"></a>檔案編碼和解碼介面

這些介面支援檔案編碼和解碼。



| 介面                                                    | 描述                                                                                                  |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent)                   | 從資料流程中取出中繼資料，例如作者和標題。                                              |
| [**IAMOpenProgress**](/windows/desktop/api/Strmif/nn-strmif-iamopenprogress)                   | 判斷檔案開啟操作的進度。                                                             |
| [**IAMParse**](/previous-versions/windows/desktop/api/Amparse/nn-amparse-iamparse)                                 | 查詢並設定 MPEG 資料流程中目前位置的剖析時間。                                     |
| [**IAMStreamSelect**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect)                   | 控制要播放的邏輯資料流程，並取得其相關資訊。                               |
| [**IAMVfwCompressDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs)       | VFW 編解碼器所提供的顯示對話方塊。                                                                 |
| [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression)           | 設定影片壓縮參數。                                                                            |
| [**IConfigAsfWriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter)                 | 控制 [WM Asf 寫入](wm-asf-writer-filter.md) 器篩選器如何將 Advanced 系統格式寫入 (ASF) 檔。 |
| [**IConfigAviMux**](/windows/desktop/api/Strmif/nn-strmif-iconfigavimux)                       | 控制 [Avi Mux](avi-mux-filter.md) 篩選寫入 avi 檔案的方式。                                       |
| [**IConfigInterleaving**](/windows/desktop/api/Strmif/nn-strmif-iconfiginterleaving)           | 當 AVI Mux 篩選寫入 AVI 檔案時，請設定交錯。                                             |
| [**IDVEnc**](/windows/desktop/api/Strmif/nn-strmif-idvenc)                                     | 在 [DV 影片編碼器](dv-video-encoder-filter.md) 篩選器上設定編碼解析度。                   |
| [**IDVSplitter**](/windows/desktop/api/Strmif/nn-strmif-idvsplitter)                           |  (DV) 串流的數位視訊降級畫面播放速率                                                      |
| [**IIPDVDec**](/windows/desktop/api/Strmif/nn-strmif-iipdvdec)                                 | 在 [DV 影片解碼](dv-video-decoder-filter.md) 篩選器上設定解碼解析度。                   |
| [**IPersistMediaPropertyBag**](/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag) | 設定及取出 AVI 資料流程中的資訊並將區塊。                                                        |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[介面](interfaces.md)
</dt> </dl>

 

 




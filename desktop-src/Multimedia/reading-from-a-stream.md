---
title: 從資料流程讀取
description: 從資料流程讀取
ms.assetid: be961f06-cf5f-4093-9b31-7d1d69e62fec
keywords:
- AVIStreamInfo 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38c56e1bd34fb9b0555c4eb0ed86944be3b7603645865144ac053604cd515cb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118371648"
---
# <a name="reading-from-a-stream"></a>從資料流程讀取

您可以使用 [**AVIStreamInfo**](/windows/desktop/api/Vfw/nf-vfw-avistreaminfoa) 函式來取得開啟之資料流程的相關資訊。 此函式會使用資料流程中的資料類型、寫入資料流程資料時所使用的壓縮方法、建議的緩衝區大小、播放速率，以及資料流程的文字描述等資訊，填滿 [**AVISTREAMINFO**](/windows/desktop/api/Vfw/ns-vfw-avistreaminfoa) 結構。

[**AVISTREAMINFO**](/windows/desktop/api/Vfw/ns-vfw-avistreaminfoa)結構的某些成員也會出現在 [**AVIFILEINFO**](/windows/desktop/api/Vfw/ns-vfw-avifileinfoa)結構中。 **AVIFILEINFO** 結構中的資訊會套用至整個檔案。 **AVISTREAMINFO** 結構中的資訊是所存取資料流程的特定資訊，其優先順序高於 **AVIFILEINFO** 結構中的資訊。

如果串流具有與其相關聯的補充資訊，您可以使用 [**AVIStreamReadData**](/windows/desktop/api/Vfw/nf-vfw-avistreamreaddata) 函式來取得此資訊。 此函式會在應用程式提供的緩衝區中傳回信息。 補充資料流程資訊可能包含用於資料流程的壓縮和解壓縮方法的設定。 您可以使用 [**AVIStreamDataSize**](/windows/desktop/api/Vfw/nf-vfw-avistreamdatasize) 宏來取得所需的緩衝區大小。

您可以使用 [**AVIStreamReadFormat**](/windows/desktop/api/Vfw/nf-vfw-avistreamreadformat) 函式來取出資料流程的格式資訊。 此函式會在應用程式提供的緩衝區中傳回資料流程特定結構。 若為影片資料流程，緩衝區會在 [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) 結構中包含格式資訊。 若是音訊串流，緩衝區會包含 [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) 或 [**PCMWAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-pcmwaveformat) 結構中的格式資訊。 針對其他資料流程類型，資料流程處理常式會傳回資料流程的特定資訊。 您可以使用 **AVIStreamReadFormat** ，並指定 **Null** 緩衝區位址或使用 [**AVIStreamFormatSize**](/windows/desktop/api/Vfw/nf-vfw-avistreamformatsize) 宏，來判斷所需的緩衝區大小。

您可以使用 [**AVIStreamRead**](/windows/desktop/api/Vfw/nf-vfw-avistreamread) 函式，在資料流程中取出多媒體內容。 此函數會將原始資料從資料流程複製到應用程式提供的緩衝區。 若為影片串流，此函式會抓取組成框架內容的點陣圖影像。 針對音訊串流，此函式會抓取組成音效內容的波形音訊樣本。 您可以使用 **AVIStreamRead** ，並指定 **Null** 緩衝區位址或使用 [**AVIStreamSampleSize**](/windows/desktop/api/Vfw/nf-vfw-avistreamsamplesize) 宏，來判斷所需的緩衝區大小。

某些 AVI 串流處理常式會導致與軟體和硬體初始化或協調相關的延遲。 您可以使用 [**AVIStreamBeginStreaming**](/windows/desktop/api/Vfw/nf-vfw-avistreambeginstreaming) 函式來通知這些處理常式，以準備進行資料串流。 此函式可讓資料流程處理常式配置和初始化其所需的資源。 若要在串流處理結束時通知這些處理常式，請使用 [**AVIStreamEndStreaming**](/windows/desktop/api/Vfw/nf-vfw-avistreamendstreaming) 函數。 此函式可讓資料流程處理常式解除配置其配置給 **AVIStreamBeginStreaming** 的資源。

[**AVIStreamRead**](/windows/desktop/api/Vfw/nf-vfw-avistreamread)函式不提供解壓縮服務。 如需有關壓縮和解壓縮音訊串流的詳細資訊，請參閱 [音訊壓縮管理員](audio-compression-manager.md)。 如需有關壓縮和解壓縮影片資料流程的詳細資訊，請參閱 [影片壓縮管理員](video-compression-manager.md)。 如需有關在影片串流中壓縮和解壓縮個別框架的詳細資訊，請參閱 [在資料流程中使用壓縮的影片資料](working-with-compressed-video-data-in-a-stream.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[資料流作業](stream-operations.md)
</dt> </dl>

 

 
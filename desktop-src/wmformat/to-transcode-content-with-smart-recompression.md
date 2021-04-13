---
title: 使用智慧型 Recompression 轉碼內容
description: 使用智慧型 Recompression 轉碼內容
ms.assetid: 02398462-b0a4-4a17-84e3-4c6f9f26639f
keywords:
- Windows Media Format SDK，轉碼內容
- Windows Media Format SDK、smart recompression
- Windows Media Format SDK、recompression
- Windows Media 格式 SDK，Windows Media 音訊編解碼器
- Advanced Systems Format (ASF) 、轉碼內容
- ASF (Advanced Systems Format) 、轉碼內容
- Advanced Systems Format (ASF) 、smart recompression
- ASF (Advanced Systems Format) 、smart recompression
- Advanced Systems Format (ASF) ，recompression
- ASF (Advanced Systems Format) ，recompression
- Advanced Systems Format (ASF) 、Windows Media 音訊編解碼器
- ASF (Advanced Systems Format) Windows Media 音訊編解碼器
- 轉碼內容
- 智慧型 recompression
- recompression
- Windows Media 音訊編解碼器、轉碼內容
- 編解碼器，Windows Media 音訊編解碼器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a1317989ea9384d4a9747d712af1ce5c61d484c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314292"
---
# <a name="to-transcode-content-with-smart-recompression"></a>使用智慧型 Recompression 轉碼內容

您可以使用 Windows Media Format SDK，從一個位元速率轉碼內容到另一個位元速率。 一般來說，這牽涉到直接解碼內容，再將它編碼為所需的位元速率。 Windows Media 音訊9編解碼器支援智慧型 recompression，可讓轉碼比平常更高的品質。

針對智慧型 recompression，原始音訊資料流程必須以 Windows Media 音訊編解碼器編碼。 所有版本的編解碼器都受到支援，但特製化音訊編解碼器 (Windows Media 音訊 9 Professional 和 Windows Media 音訊 9 Voice) 不會。 如果原始音訊使用 Windows Media 音訊9無失真編解碼器編碼，則不需要使用智慧型 recompression，因為原始編碼未遺失任何資訊。

若要使用智慧型 recompression，請執行下列步驟。

1.  設定讀取來源檔案的讀取器物件。 如需詳細資訊，請參閱 [讀取 ASF](reading-asf-files.md)檔。
2.  設定要用於轉碼檔案的寫入器物件。 設定新檔案的檔案名。 選取要用於新檔案的設定檔。 在寫入器物件中設定選取的設定檔。 如需詳細資訊，請參閱 [寫入 ASF](writing-asf-files.md)檔。
3.  藉由呼叫 **IWMReader：： QueryInterface**，取得讀取器物件之 [**IWMProfile**](iwmprofile.md)介面的指標。
4.  藉由呼叫 [**IWMProfile：： GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream)，取得要轉碼之音訊資料流程的 [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig)介面。
5.  藉由呼叫 **IWMStreamConfig：： QueryInterface** 來取得資料流程設定物件的 [**IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)介面。
6.  對 [**IWMMediaProps：： GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype)進行兩次呼叫，以抓取資料流程的 [**WM \_ 媒體 \_ 類型**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type)結構。 在第一次呼叫時取得結構的大小，並為緩衝區配置記憶體，以在第二次呼叫時傳遞。
7.  藉由呼叫 [**IWMWriter：： GetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops)，取得寫入器中輸入的 [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops)介面指標。
8.  藉由呼叫 **IWMInputMediaProps：： QueryInterface** 來取得輸入媒體屬性物件的 [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault)介面。
9.  使用 [**IWMPropertyVault：： SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) 方法來設定 g \_ wszOriginalWaveFormat 屬性。 使用在步驟6中取得的 **WAVEFORMATEX** 結構做為屬性的值。
10. 藉由呼叫 [**IWMWriter：： SetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops) ，並將指標傳遞至 **IWMInputMediaProps** 介面，來包含對輸入媒體屬性所做的變更。
11. 開始讀取原始檔案中的範例，並透過呼叫 [**IWMWriter：： WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample)將它們傳遞給寫入器。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**Advanced 主題**](advanced-topics.md)
</dt> <dt>

[**IWMInputMediaProps 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops)
</dt> <dt>

[**IWMMediaProps 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)
</dt> <dt>

[**IWMProfile 介面**](iwmprofile.md)
</dt> <dt>

[**IWMPropertyVault 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault)
</dt> <dt>

[**IWMStreamConfig 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig)
</dt> </dl>

 

 





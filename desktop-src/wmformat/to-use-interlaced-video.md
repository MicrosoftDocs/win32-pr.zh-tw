---
title: 使用交錯式影片
description: 使用交錯式影片
ms.assetid: cb77bac7-bea8-4f1b-8302-fee9a43d4815
keywords:
- Windows Media Format SDK，交錯式影片
- Windows Media Format SDK、影片編碼交錯式
- Windows Media Format SDK，編碼交錯式影片
- Windows Media Format SDK，解碼交錯式影片
- Windows Media Format SDK，欄位順序
- Advanced Systems Format (ASF) 、交錯式影片
- ASF (Advanced Systems Format) 、交錯式影片
- Advanced Systems Format (ASF) 、影片編碼交錯式
- ASF (Advanced Systems Format) 、影片編碼交錯式
- Advanced Systems Format (ASF) 、編碼交錯式影片
- ASF (Advanced Systems Format) 、編碼交錯式影片
- Advanced Systems Format (ASF) ，解碼交錯式影片
- ASF (Advanced Systems Format) ，解碼交錯式影片
- Advanced Systems Format (ASF) ，欄位順序
- ASF (Advanced Systems Format) ，欄位順序
- 交錯式影片，關於
- 交錯式影片，編碼
- 交錯式影片，解碼
- 交錯式影片，欄位順序
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a093ddd6d9d9487ffcd4b73e1f5c75b849cdcdc1
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "103841900"
---
# <a name="to-use-interlaced-video"></a>使用交錯式影片

有兩種基本類型的影片編碼：漸進式和交錯式。 在漸進式編碼中，每個畫面格都是一段影片的編碼標記法。 在交錯編碼中，每個畫面格都是一種編碼的標記法，表示影片中的所有資料列或所有奇數資料列。 每個交錯框架稱為 *欄位*，因此有奇數位段甚至是欄位。 交錯顯示 (像是電視) 會一次轉譯一個欄位，也就是替代欄位。 漸進式顯示器會一次呈現全部的畫面格。

Windows Media 視訊 9 Advanced Profile 編解碼器可支援在壓縮的資料流程中維持交錯。

## <a name="when-to-use-interlaced-video"></a>使用交錯式影片的時機

只有在交錯式裝置上顯示內容時，才會對交錯式影片進行編碼。 想要透過機上盒或其他裝置在電視上觀看 (的內容，) 可能需要進行交錯。 要以獨佔方式在電腦顯示器上查看的內容不應編碼為交錯式。

若要將交錯式影片編碼為漸進式影片，您必須設定輸入設定。 如需詳細資訊，請參閱 [將影片進行逐行掃描](to-deinterlace-video.md)。

## <a name="field-order"></a>欄位順序

交錯影片的大部分來源（例如影片捕獲卡）都會提供影片範例，其中包含兩個欄位交錯。 結果就像是完整的影片框架，不同的是，奇數甚至線條會稍微移動一段時間。 在交錯的影片範例中，第一次發生的欄位並沒有通用標準。

您應該讓使用者在傳遞交錯式範例至您的應用程式時指定欄位順序。

## <a name="encoding-interlaced-video"></a>編碼交錯式影片

若要使用交錯編碼，請執行下列步驟：

1.  藉由呼叫 [**IWMStreamConfig2：： AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) 方法，在設定檔中設定影片串流以使用內容類型的資料單位延伸。 內容類型延伸模組的範例延伸模組 GUID 是 WM \_ SampleExtensionsGUID \_ ContentType。
2.  設定設定檔中的資料流程，並將寫入器設定為一般設定檔。
3.  將交錯式範例傳遞給寫入器之前，請先呼叫 [**IWMWriterAdvanced2：： SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) 方法，將 g \_ wszInterlacedCoding 輸入設定設定為 **TRUE**。
4.  針對您傳遞至寫入器的每個交錯樣本，呼叫 [**INSSBuffer3：： SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) 方法以設定內容類型。 內容類型值是下表中的旗標組合。



| 旗標                         | 描述                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WM \_ CT \_ 交錯式           | 編碼交錯的內容時，一律設定此旗標。 如果您在沒有設定欄位順序旗標的情況下使用此旗標 (WM \_ ct \_ \_ \_ 第一個欄位或 WM \_ ct \_ 頂端 \_ 欄位 \_) 編解碼器將會假設頂端欄位是第一個。 如果編解碼器使用錯誤的欄位順序，就不會對影像品質產生任何影響，但編碼效率將會受到影響。 |
| WM \_ CT \_ 下 \_ \_ 一個欄位 | 當結合了 WM \_ CT \_ 交錯旗標時，此旗標會指出底部欄位 (第二行開始的欄位，) 會先發生。                                                                                                                                                                                          |
| WM \_ CT \_ 頂端 \_ 欄位 \_ 優先    | 當結合了 WM \_ CT \_ 交錯旗標時，此旗標會指出第一個欄位 (開頭為範例中第一行的欄位，) 第一次發生。                                                                                                                                                                                              |
| WM \_ CT \_ 重複 \_ 第一個 \_ 欄位 | 指出範例中的第一個欄位應該在播放時重複。 此旗標用於影片，該影片是由電影程式從電影建立的。如果未將任何欄位順序旗標與此旗標一起設定，則會假設頂端欄位是在第一次發生。<br/>                                                                             |



 

> [!Note]  
> 如果 \_ \_ 未設定 WM CT 交錯旗標，則會假設範例包含漸進式的影片畫面。

 

## <a name="decoding-interlaced-video"></a>解碼交錯式影片

解碼交錯式影片時，您必須 \_ 使用 [**IWMReaderAdvanced2：： SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting)方法，將 g wszAllowInterlacedOutput 設定設為 **TRUE** 。 否則編解碼器將會提供漸進式的框架。

內容類型資料單位延伸是在輸出範例上進行維護。 您應該將欄位方向傳遞到轉譯裝置，以確保能正常播放。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**Advanced 主題**](advanced-topics.md)
</dt> </dl>

 

 






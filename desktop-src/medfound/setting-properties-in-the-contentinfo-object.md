---
description: 建立 ASF 檔案時，ContentInfo 物件必須知道媒體內容的特性，才能以正確的值填入不同的標頭物件。
ms.assetid: 30e3c10b-1310-4194-8b83-221dfe73b03c
title: 在 ContentInfo 物件中設定屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e386d5eb33dd1893b195a870425b2336ab9c316f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114357"
---
# <a name="setting-properties-in-the-contentinfo-object"></a>在 ContentInfo 物件中設定屬性

建立 ASF 檔案時，ContentInfo 物件必須知道媒體內容的特性，才能以正確的值填入不同的標頭物件。

-   [ContentInfo 物件中的內容相關設定](#content-related-settings-in-the-contentinfo-object)
-   [使用編碼器設定來設定 ContentInfo 物件](#configuring-the-contentinfo-object-with-encoder-settings)
-   [相關主題](#related-topics)

## <a name="content-related-settings-in-the-contentinfo-object"></a>ContentInfo 物件中的內容相關設定

內容設定是包含在設定檔中的串流設定，並指定媒體接收器的串流識別碼、媒體類型和有漏洞 bucket 參數。 藉由呼叫 [**IMFASFContentInfo：： SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile)在 ContentInfo 物件上設定設定檔之後，這些值會反映在產生的 ASF 標頭物件中。 如需這些設定的詳細資訊，請參閱 [建立及設定 ASF 資料流程](creating-and-configuring-asf-streams.md)。

## <a name="configuring-the-contentinfo-object-with-encoder-settings"></a>使用編碼器設定來設定 ContentInfo 物件

數位媒體音訊或影片資料很複雜，並佔用海量儲存體。 在大部分的情況下，音訊和影片都會使用編碼器進行壓縮，然後再新增至 ASF 檔案。 在媒體基礎中，會使用一個輸入和一個輸出，將編碼器實作為 [媒體基礎轉換](media-foundation-transforms.md) (MFTs) 。 您必須根據輸入資料流程的媒體類型，以及您選擇用來壓縮資料流程的編碼類型，來選取輸出媒體類型。

在編碼會話之前，您必須根據編碼類型設定相關的屬性來設定編碼器。

設定編碼器之後，您必須使用編碼器值設定 ContentInfo 物件，因為 [asf](asf-multiplexer.md) 多工器和 Asf 媒體接收（以填入的 ContentInfo 物件初始化）會使用有漏洞值區值之類的設定來產生 ASF 資料封包。 這些值不會儲存在最終的 ASF 標頭物件中。 編碼設定會公開為屬性。 若要使用編碼器屬性來設定 ContentInfo 物件，請執行下列動作：

1.  直接針對 **IPropertyStore** 介面查詢編碼器 ([**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)) 介面，以取得編碼器屬性存放區的指標。
2.  呼叫 [**IMFASFContentInfo：： GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore)。 若要設定資料流程特定屬性，請在 *wStreamNumber* 參數中指定資料流程識別碼;若為檔案層級屬性，則傳遞0。 *PpIStore* 參數會接收 **IPropertyStore** 介面的指標。 收到的屬性存放區是空的。
3.  在編碼器上呼叫 **IPropertyStore：： GetValue** ，然後藉由指定屬性索引鍵常數來取得屬性值。 如需編碼屬性的完整清單，請參閱 [編解碼器程式設計參考](/previous-versions//aa384554(v=vs.85))。
4.  在 ContentInfo 物件上呼叫 **IPropertyStore：： SetValue** ，以設定屬性存放區中的必要屬性。
5.  針對您要設定的每個屬性重複步驟3和4。

您可以藉由呼叫 [**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate)，藉由使用啟用物件來建立 ASF 媒體接收器。 新的媒體接收物件是根據可在 ContentInfo 物件的屬性存放區中設定的媒體接收特定設定來設定。 下表顯示 ASF 媒體接收器屬性常數。



| 屬性                                                                                                     | 描述                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MFPKEY \_ ASFMEDIASINK \_ BASE \_ SENDTIME**](mfpkey-asfmediasink-base-sendtime-property.md)                   | 傳送時間會指出何時會釋放有漏洞 bucket 內的承載。 這個屬性值表示第一個傳送時間。 多工器會使用此值來計算所產生封包的後續傳送時間，並確保資料會透過有漏洞值區穩定流動。 |
| [**MFPKEY \_ ASFMEDIASINK \_ AUTOADJUST \_ 位元速率**](mfpkey-asfmediasink-autoadjust-bitrate-property.md)         | 這個 **BOOL** 值會指出多工器是否需要自動調整位元速率，以確保資料不會溢位有漏洞值區。                                                                                                                                              |
| [**MFPKEY \_ ASFMEDIASINK \_ DRMACTION**](mfpkey-asfmediasink-drmaction-property.md)                            | 這表示檔案產生的 ASF 媒體接收 DRM 動作。 在此版本中，只支援 DRM 轉碼。                                                                                                                                                                                   |
| [**MFPKEY \_ ASFSTREAMSINK 已 \_ 更正 \_ LEAKYBUCKET**](mfpkey-asfstreamsink-corrected-leakybucket-property.md) | 當編碼器決定要使用哪個緩衝區視窗和位元速率時，必須設定這個屬性。 若要設定這些值，請使用 [**IWMCodecLeakyBucket**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecleakybucket) 介面。 這必須針對 ASF 檔案中的每個資料流程進行設定。                                                     |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[為新檔案撰寫 ASF 標頭物件](writing-an-asf-header-object-for-a-new-file.md)
</dt> </dl>

 

 

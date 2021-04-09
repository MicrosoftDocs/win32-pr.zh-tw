---
description: 若要將媒體檔案轉換成 ASF 格式，您可以使用 Windows Media 編碼器。 若要使用這些編碼器，必須向系統註冊。
ms.assetid: 18c26619-6047-4f7f-bb65-ca418f02e5b1
title: 使用編碼器啟用物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfd44a1b97ad0f133b7215ff4474835ddfba66bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848699"
---
# <a name="using-an-encoders-activation-objects"></a>使用編碼器的啟用物件

若要將媒體檔案轉換成 ASF 格式，您可以使用 Windows Media 編碼器。 若要使用這些編碼器，必須向系統註冊。

如需編碼器註冊的相關資訊，請參閱具現 [化編碼器 MFT](instantiating-the-encoder-mft.md)。

-   [使用編碼器的啟用物件](#using-an-encoders-activation-objects)
-   [Windows 7 和更新版本中的編碼器列舉](#encoder-enumeration-in-windows-7-and-later)
-   [相關主題](#related-topics)

## <a name="using-an-encoders-activation-objects"></a>使用編碼器的啟用物件

另一種方法是使用編碼器的 [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) 介面 (在 [使用 CoCreateInstance 建立編碼器](using-an-encoder-s-imftransform--interface.md)) 中所述，您可以為編碼器建立啟用物件的實例。 啟用物件有助於建立編碼器，媒體基礎為此方法提供下列兩個功能：

-   [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) 可具現化 Windows Media 音訊編碼器。
-   用來具現化 Windows Media video 編碼器的 [**MFCreateWMVEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate) 。

這兩個函式都需要您先建立目標媒體類型並設定編碼屬性，然後再呼叫這些函式。 如果您的應用程式使用 [管線層 ASF 元件](pipeline-layer-asf-components.md) 將檔案編碼為 asf 格式，而且已經建立並設定 [asf 媒體接收器](asf-media-sinks.md)，您就可以從 asf 媒體接收器取得這組資訊。

[**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) 和 [**MFCreateWMVEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate) 會將編碼器的輸出類型設定為應用程式所指定的媒體類型。

**注意**  如果您使用 [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) 和 [**MFCreateWMVEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate) ，則可以藉由呼叫 [**IMFActivate：： ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) 來啟用編碼器，但無法變更編碼器的輸入和輸出媒體類型，也不能變更任何編碼屬性。

如需使用啟用物件建立媒體基礎物件的詳細資訊，請參閱 [啟用物件](activation-objects.md)。

**從 ASF 媒體接收器取得目標媒體類型**

1.  藉由在 ASF 媒體接收上呼叫 **IMFMediaSink：： QueryInterface** ，並傳遞 **IID \_ IMFASFContentInfo** 作為介面識別碼，取得 asf 媒體接收器的 [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo)指標指標。
2.  取得與 ContentInfo 物件相關聯的 ASF 設定檔物件。
3.  列舉設定檔中的串流，以取得資料流程的媒體類型。

**從 ASF 媒體接收器取得編碼屬性**

1.  如果您已在 [檔案接收) 中 [設定屬性](setting-properties-in-the-file-sink.md) (所述的媒體接收器中設定 [編碼屬性](configuring-the-encoder.md)，您就可以在 ASF 媒體接收上呼叫 **IMFMediaSink：： QueryInterface** 並傳遞 **IID \_ IPropertyStore** 作為介面識別碼，藉以參考接收的屬性存放區。
2.  如果您有接收器 ContentInfo 物件的指標，您可以呼叫 [**IMFASFContentInfo：： GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) 來取得媒體接收器屬性存放區的參考。

    請確定在 ASF 媒體接收上設定的所有編碼屬性都會反映在傳遞給 [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) 和 [**MFCreateWMVEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate)的屬性存放區中。 編碼器會根據應用程式所指定的設定自動設定。

在編碼拓撲中建立轉換節點時，您可以將物件類型設定為在這兩個呼叫中收到的 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) 指標。 當拓撲解決之後，媒體會話會使用啟用物件來建立編碼器 MFT 的實例。

## <a name="encoder-enumeration-in-windows-7-and-later"></a>Windows 7 和更新版本中的編碼器列舉

針對在 Windows 7 上執行的應用程式，除了 [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) 之外，您還可以藉由呼叫 [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)來列舉編碼器 MFTs。 此函式會傳回編碼器 MFT 之啟用物件的指標。 函式的結構與上述 **MFTEnum** 非常類似，但 **MFTEnumEx** 會針對符合搜尋準則的編碼器 MFTs 傳回 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) 指標的陣列。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[具現化編碼器 MFT](instantiating-the-encoder-mft.md)
</dt> <dt>

[Windows Media 編碼器](windows-media-encoders.md)
</dt> <dt>

[啟用物件](activation-objects.md)
</dt> </dl>

 

 




---
description: ASF 檔案接收是媒體基礎所提供的 IMFMediaSink，可讓應用程式用來將 ASF 媒體資料封存至檔案。 如需 ASF 媒體接收物件模型和一般使用方式的相關資訊，請參閱 ASF 媒體接收器。
ms.assetid: a47caabd-23e3-4d22-b4b6-5fdb79d62ca1
title: 設定 File 接收中的屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30af39cf13e88f6edf2a6ab68caac27c2400955a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318736"
---
# <a name="setting-properties-in-the-file-sink"></a>設定 File 接收中的屬性

ASF 檔案接收是媒體基礎所提供的 [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) ，可讓應用程式用來將 ASF 媒體資料封存至檔案。 如需 ASF 媒體接收器的物件模型和一般使用方式的相關資訊，請參閱 [Asf 媒體接收器](asf-media-sinks.md)。

[建立 ASF 檔案接收](creating-the-asf-file-sink.md)之後，必須使用輸出檔中的資料流程相關資訊進行設定。 [將資料流程資訊新增至 ASF 檔案接收](adding-stream-information-to-the-asf-file-sink.md)時，會說明此程式。 您可以根據編碼類型，在檔案接收上設定其他屬性。有漏洞 bucket;一般檔案屬性。 這些設定不會寫入最終的 ASF 標頭物件中。 本主題說明在檔案接收的屬性存放區中新增這些屬性的程式。

ContentInfo 物件會維護檔案接收的通用檔案屬性和個別資料流程屬性。 如需取得檔案接收之 ASF ContentInfo 物件參考的詳細資訊，請參閱 [建立 asf 檔案接收](creating-the-asf-file-sink.md)。

若要取得檔案接收之屬性存放區的參考 ([**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)) ，請在檔案接收的 ContentInfo 物件參考上呼叫 [**IMFASFContentInfo：： GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) 。

## <a name="stream-encoding-properties"></a>資料流程編碼屬性

為了適當地編碼內容，檔案需要知道某些編碼資訊，例如編碼類型和相關的編碼參數。 這些值會在檔案接收上設定為屬性值，在 ASF ContentInfo 物件所維護的內容存放區中。 如果您要在具現化相關的編碼器之前設定 file 接收器，您可以使用 ContentInfo 物件搭配所有填入的屬性來建立 Windows Media 編碼器。 在此情況下，會在具現化的編碼器上自動設定這些屬性。 相反地，如果您要在接收之前建立編碼器，請確定您在編碼器上設定的屬性會複製到檔案接收的屬性存放區。

若要設定編碼屬性，您需要存取 file 接收器的資料流程層級屬性存放區。 在 [**IMFASFContentInfo：： GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore)方法的 *wStreamNumber* 參數中傳遞資料流程號碼。 資料流程號碼必須符合在設定檔中設定每個資料流程時所設定的值。 藉由呼叫 [**IPropertyStore：： SetValue**](/windows/win32/api/propsys/nn-propsys-ipropertystore)來設定屬性值。 下表描述支援的屬性。

屬性取決於編碼類型。 如需屬性和您必須設定之個別值的相關資訊，請參閱 [編碼屬性](configuring-the-encoder.md)。

## <a name="leaky-bucket-property"></a>有漏洞 Bucket 屬性

有漏洞 bucket 參數會決定資料流程的編碼器所使用的實際緩衝區視窗。 File sink 的 [**MFPKEY \_ ASFSTREAMSINK \_ 更正 \_ LEAKYBUCKET**](mfpkey-asfstreamsink-corrected-leakybucket-property.md) 屬性包含有漏洞值區參數、位元速率、緩衝區視窗和初始緩衝區飽和。這個屬性是在檔案接收的資料流程層級屬性存放區中設定，而且必須在建立和設定編碼器之後設定。 這個值是在中設定。 在媒體類型協商期間，編碼器會決定要使用的緩衝區視窗和位元速率。 您可以使用 **IWMCodecLeakyBucket** 介面（定義于 wmcodecifaces 中）來取得這些值，而且必須連結至 wmcodecdspuuid 以呼叫其方法。

您可以針對 ASF 檔案接收中的每個資料流程，設定這個屬性的已抓取值。

## <a name="global-file-sink-properties"></a>通用檔案接收屬性

若要取得 file 接收器的全域屬性存放區，請在 [**IMFASFContentInfo：： GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore)方法的 *wStreamNumber* 參數中傳遞0。 藉由呼叫 [**IPropertyStore：： SetValue**](/windows/win32/api/propsys/nn-propsys-ipropertystore)來設定屬性值。 下表描述支援的屬性。

| 檔案層級屬性                                                                                | Description                                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MFPKEY \_ ASFMEDIASINK \_ BASE \_ SENDTIME**](mfpkey-asfmediasink-base-sendtime-property.md)           | 傳送時間會指出何時會釋放有漏洞 bucket 內的承載。 這個屬性值表示第一個傳送時間。 多工器會使用此值來計算所產生封包的後續傳送時間，並確保資料會透過有漏洞值區穩定流動。 |
| [**MFPKEY \_ ASFMEDIASINK \_ AUTOADJUST \_ 位元速率**](mfpkey-asfmediasink-autoadjust-bitrate-property.md) | 這個 BOOL 值會指出多工器是否需要自動調整位元速率，以確保資料不會溢位有漏洞值區。                                                                                                                                                  |
| [**MFPKEY \_ ASFMEDIASINK \_ DRMACTION**](mfpkey-asfmediasink-drmaction-property.md)                    | 這表示檔案產生的 ASF 媒體接收 DRM 動作。 在此版本中，只支援 DRM 轉碼。                                                                                                                                                                                   |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ASF 媒體接收](asf-media-sinks.md)
</dt> <dt>

[管線層 ASF 元件](pipeline-layer-asf-components.md)
</dt> <dt>

[媒體基礎中的 ASF 支援](asf-support-in-media-foundation.md)
</dt> </dl>

 

 

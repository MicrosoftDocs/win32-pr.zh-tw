---
description: ASF 媒體接收器是編碼管線中的最後一個元件，可讓應用程式寫入 ASF 檔。
ms.assetid: 65bb8822-5eb0-46a3-ab9e-c55ae466e982
title: ASF 媒體接收
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d6bcd3e6b91403185342607e8c4374eb32069c7
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106989121"
---
# <a name="asf-media-sinks"></a>ASF 媒體接收

ASF 媒體接收器是編碼管線中的最後一個元件，可讓應用程式寫入 ASF 檔。

媒體基礎提供兩種類型的 ASF 媒體接收器：

-   *Asf 檔案接收* 可用來將 asf 媒體資料封存至檔案。
-   *Asf 串流接收器* 用來在可透過網路串流處理的位元組資料流程中寫入 asf 內容。

ASF 媒體接收器包含一或多個資料流程接收，其代表要針對輸出 ASF 檔案中的每個資料流程寫入的資料。 針對在 Windows Vista 上執行的應用程式進行編碼，您必須建立及設定 ASF 媒體接收器，然後將它新增至拓撲，以手動方式設定編碼拓撲。 在 Windows 7 中，如果您使用快速轉碼物件來建立拓撲，則不會直接建立媒體接收器，而且應用程式不會呼叫媒體接收或任何資料流程接收上的任何方法。 Fast 轉碼物件可具現化所需的媒體接收，並將其新增至拓撲，然後再傳回呼叫端應用程式的參考。 不過，對於快速轉碼物件，有一些限制會根據編碼類型而套用。

-   [ASF 媒體接收物件模型](#asf-media-sink-object-model)
-   [ASF 檔接收器](#asf-file-sink)
-   [相關主題](#related-topics)

## <a name="asf-media-sink-object-model"></a>ASF 媒體接收物件模型

ASF 媒體接收器會執行 [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) 介面並公開下列介面。 應用程式可以在用來產生輸出範例的 ASF 媒體接收器上呼叫 [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) ，以取得這些介面的參考。



| 介面                                                  | 描述                                                                                                                                                                                            |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink)                       | 所有媒體接收都需要。                                                                                                                                                                          |
| [**IMFFinalizableMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imffinalizablemediasink) | 由可將產生的媒體內容寫入檔案的 ASF 檔案接收所執行。 您可以使用此介面上的方法來排清資料，並更新最終輸出檔案的 ASF 標頭物件。 |
| [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)             | 從呈現時鐘接收狀態變更通知。                                                                                                                                       |
| [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo)             | ASF ContentInfo 物件是 WMContainer 層級物件，主要儲存 ASF 標頭物件資訊。 這是用來建立 ASF 媒體接收器。                                                     |
| [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata)                         | 用來描述 ASF 檔案的中繼資料。                                                                                                                                                        |
| [**IMFMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider)         | 取得中繼資料的集合，不論是針對整個簡報，或是簡報中的一個資料流程。                                                                                          |



 

## <a name="asf-file-sink"></a>ASF 檔接收器

ASF 檔案接收是媒體基礎所提供的 [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) ，可讓應用程式用來將 ASF 媒體資料封存至檔案。

如果您使用管線層物件來寫入新的 ASF 檔案，您需要在檔案接收或其任何資料流程接收上建立、設定和呼叫方法。 設定檔案接收器之後，您可以將它新增至編碼管線。

以下是使用 ASF file 接收器的一般步驟：

1.  建立同進程或跨進程的檔案接收。
2.  使用所有資料流程、編碼屬性和中繼資料資訊來設定 file sink。
3.  藉由列舉資料流程接收或在接收中追蹤資料流程號碼，來將檔案接收與輸出拓撲節點建立關聯。

下列主題包含有關使用 ASF 檔案接收的詳細資訊：

-   [建立 ASF 檔接收器](creating-the-asf-file-sink.md)
-   [將資料流程資訊新增至 ASF 檔案接收](adding-stream-information-to-the-asf-file-sink.md)
-   [設定 File 接收中的屬性](setting-properties-in-the-file-sink.md)
-   [將中繼資料新增至 File 接收器](adding-metadata-to-the-file-sink.md)
-   [有漏洞 Bucket 緩衝區模型](the-leaky-bucket-buffer-model.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[管線層 ASF 元件](pipeline-layer-asf-components.md)
</dt> <dt>

[媒體基礎中的 ASF 支援](asf-support-in-media-foundation.md)
</dt> </dl>

 

 

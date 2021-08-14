---
title: 使用寫入器接收器
description: 使用寫入器接收器
ms.assetid: 1ad28684-47d2-4ddb-bf18-22310f0392a0
keywords:
- Advanced Systems Format (ASF) 、寫入器接收
- ASF (Advanced 系統格式) 、寫入器接收
- Advanced Systems Format (ASF) 、接收
- ASF (Advanced 系統格式) 、接收
- 接收，寫入器接收
- 寫入器接收器，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 407e5bf2e87bfbf3084d19f75170a12be693d804d4d902f919096dca5aeab057
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118194865"
---
# <a name="working-with-writer-sinks"></a>使用寫入器接收器

Windows 媒體格式 SDK 的寫入器物件會將輸入媒體資料處理成位串流。 但是，寫入器物件不會將位資料流程傳遞至其最終目的地 () 的檔案或網路位置。 若要將 ASF 內容寫入可使用的格式，您必須使用寫入器接收器。

寫入器物件支援三種接收類型：檔接收、網路接收和推播接收。 File 接收會將 ASF 內容寫入磁片上的 ASF 檔案。 網路接收會從網路位址廣播 ASF 內容。 推播接收會將資料傳遞至執行 Windows Media Services 的伺服器，讓伺服器可以將內容提供給其預定的物件。 您也可以建立自己的接收器，以應用程式所需的任何方式來傳遞 ASF 資料。 如需網路接收和推播接收的詳細資訊，請參閱透過 [網路傳送 ASF 資料](sending-asf-data-over-a-network.md)。 本節的其餘部分將討論寫入器接收器。

您可以為所使用的每個寫入器實例設定一或多個接收。 每個接收只會處理單一目的地。 例如，如果您想要一次寫入三個檔案，您必須為每個檔案建立和設定個別的檔案接收。

下列各節說明寫入器接收器的使用。



| 區段                                                                      | 描述                                                                      |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [將接收器新增至寫入器](adding-sinks-to-the-writer.md)                 | 描述如何將接收器新增至寫入器。                                        |
| [列舉接收](enumerating-sinks.md)                                   | 描述如何列舉已新增至寫入器的接收。         |
| [從接收取得錯誤訊息](getting-error-messages-from-a-sink.md) | 說明如何設定接收以將狀態訊息傳遞給您的應用程式。 |
| [使用檔案接收](using-file-sinks.md)                                     | 說明如何使用寫入器檔案接收在磁片上建立 ASF 檔案。           |
| [使用自訂接收器](using-custom-sinks.md)                                 | 說明如何建立及使用您自己的自訂接收來傳遞 ASF 資料。       |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IWMWriterAdvanced 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)
</dt> <dt>

[**IWMWriterSink 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink)
</dt> <dt>

[**寫入 ASF 檔案**](writing-asf-files.md)
</dt> </dl>

 

 





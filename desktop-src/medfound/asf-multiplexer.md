---
description: ASF 多工器
ms.assetid: 007a6da5-47cf-476a-b0f7-566a68ad19ce
title: ASF 多工器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86e1577f005004dbbe6bbb27e1ce7af346e56e134aff2b3201f5670175b015c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035558"
---
# <a name="asf-multiplexer"></a>ASF 多工器

ASF 多工器是 *一種 WMContainer* 層物件，可與 [asf 資料物件](asf-file-structure.md) 搭配使用，並讓應用程式能夠產生 asf 容器的資料封包。 多工器接受媒體 [範例](media-samples.md) 形式的媒體資料，並根據 [Asf 標頭物件](asf-file-structure.md)中所定義的串流和 asf 封包參數輸出媒體範例。 輸出媒體範例會保存包含 packetized 數位媒體資料的一或多個媒體緩衝區的參考。您可以在檔案編碼案例中使用這個物件，它會從編碼器接收編碼的資料流程範例，或使用 ASF ASF 轉碼 (remuxing) 。

下圖說明使用多工器的 asf 檔案產生的 ASF 資料封包。

![顯示 asf 資料封包產生的圖表](images/bb2da6a9-5e50-4dea-9b79-ae32759ac48a.gif)

如需 ASF 檔案結構的詳細資訊，請參閱 [asf 檔案結構](asf-file-structure.md)。

本節包含下列主題：



| 主題                                                                  | 描述                                                       |
|------------------------------------------------------------------------|-------------------------------------------------------------------|
| [建立多工器物件](creating-the-multiplexer-object.md) | 如何建立及初始化多工器。                     |
| [產生新的 ASF 資料封包](generating-new-asf-data-packets.md) | 如何產生資料封包，以構成新的 ASF 資料物件。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[WMContainer ASF 元件](wmcontainer-asf-components.md)
</dt> <dt>

[教學課程：將 ASF 資料流程從一個檔案複製到另一個檔案](tutorial--copying-asf-streams-from-one-file-to-another.md)
</dt> <dt>

[教學課程：使用 CBR 編碼方式撰寫 WMA 檔案](tutorial--writing-a-wma-file-by-using-cbr-encoding.md)
</dt> </dl>

 

 




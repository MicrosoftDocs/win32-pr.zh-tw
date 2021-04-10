---
title: 寫入器檔案接收物件
description: 寫入器檔案接收物件
ms.assetid: 93f44579-fb2d-498e-a271-5bc91d6f0321
keywords:
- Windows Media Format SDK，寫入器檔案接收物件
- Advanced Systems Format (ASF) 、writer file sink 物件
- ASF (Advanced Systems Format) 、writer file sink 物件
- 物件，寫入器檔案接收物件
- 寫入器檔案接收物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82009e5be74cfc23e687001a2a81cd4546812af9
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "104023174"
---
# <a name="writer-file-sink-object"></a>寫入器檔案接收物件

寫入 Windows Media 輸出至檔案時，會使用寫入器檔案接收物件。

寫入器檔案接收物件是由函式 [**WMCreateWriterFileSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterfilesink)所建立，它會將指標設定為 **IWMWriterFileSink** 介面。 您可以藉由呼叫 **QueryInterface** 方法來取得寫入器檔案接收物件的其他介面。

寫入器檔案接收物件支援下列介面。



| 介面                                          | 描述                                                                                                                     |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [**IWMRegisterCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback) | 讓應用程式從物件取得狀態訊息。                                                                 |
| [**IWMWriterFileSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink)     | 開啟寫入器物件可以寫入資料的檔案。                                                                         |
| [**IWMWriterFileSink2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink2)   | 提供檔案接收物件的擴充管理。 繼承 **IWMWriterFileSink** 的所有方法。                       |
| [**IWMWriterFileSink3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink3)   | 提供用來寫入檔案的其他選項。 繼承 **IWMWriterFileSink** 和 **IWMWriterFileSink2** 的所有方法。 |
| [**IWMWriterSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink)             | 配置記憶體、判斷接收是否即時運作，以及處理數個回呼函數。                |



 

應用程式應該執行下列回呼介面，以追蹤寫入器檔案接收物件的進度。



| 介面                                      | 描述                                                                    |
|------------------------------------------------|--------------------------------------------------------------------------------|
| [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | 必須將狀態資訊傳達給主應用程式時，才需要此資訊。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**物件**](objects.md)
</dt> <dt>

[**使用寫入器接收器**](working-with-writer-sinks.md)
</dt> </dl>

 

 





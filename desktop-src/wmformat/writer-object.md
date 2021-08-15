---
title: 寫入器物件
description: 寫入器物件
ms.assetid: 8058b7fe-7d02-4572-ad43-6867d4ceb7e9
keywords:
- Windows媒體格式 SDK，寫入器物件
- Advanced Systems Format (ASF) 、writer 物件
- ASF (Advanced Systems Format) 、writer 物件
- 物件、寫入器物件
- 寫入器物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f76ad82cb56317cef9b70b0412fb79662ef89eacace8668b08a06f4cc5bf420
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119392318"
---
# <a name="writer-object"></a>寫入器物件

寫入器物件是用來寫入使用 advanced systems 格式的數位媒體檔案， (ASF) 檔案結構。 寫入數位媒體檔案的程式牽涉到寫入器內部的許多步驟，這些步驟會協調壓縮、packetization 和多工處理。

寫入器物件包含輸出至檔案或網路的介面、支援一個回呼介面，並且可以建立一或多個輸入媒體屬性物件。

寫入器物件是由函式 [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter)所建立，它會將指標設定為 **IWMWriter** 介面。 您可以藉由呼叫 **QueryInterface** 方法來取得寫入器物件的其他介面。

寫入器物件支援下列介面。



| 介面                                          | 描述                                                                                                                                                                                               |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMDRMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter)               | 提供產生 [*DRM*](wmformat-glossary.md) 金鑰的方法。                                                                                                |
| [**IWMDRMWriter2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter2)             | 設定寫入器物件，以寫入檔案，其中包含符合網路裝置通訊協定 Windows 媒體 DRM 10 的預先加密資料流。                                                    |
| [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)             | 管理標頭資訊的規格和抓取，例如中繼資料、 [*標記*](wmformat-glossary.md)等等。                                                           |
| [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2)           | 管理列舉可用的編解碼器資訊。 繼承 **IWMHeaderInfo** 的所有方法。                                                                                            |
| [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3)           | 管理列舉可用的編解碼器資訊。 繼承 **IWMHeaderInfo** 和 **IWMHeaderInfo2** 的所有方法。                                                                     |
| [**IWMWatermarkInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwatermarkinfo)       | 提供有關系統上浮水印系統資訊的存取權。                                                                                                                          |
| [**IWMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)                     | 啟動和停止寫入 ASF 檔案;它包含配置緩衝區、設定和取出輸入屬性、設定設定檔和輸出檔名稱，以及解除鎖定寫入器的方法。         |
| [**IWMWriterAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)     | 新增、取得和移除指定的接收物件;抓取統計資料、接收數目以及寫入器所使用的時鐘時間;並執行其他 advanced 函數。                                |
| [**IWMWriterAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2)   | 提供一些先進的功能，特別是處理 deinterlaced 影片。 繼承 **IWMWriterAdvanced** 的所有方法。                                                                 |
| [**IWMWriterAdvanced3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced3)   | 提供額外的寫入器功能，包括取得詳細寫入器統計資料的能力。 繼承 **IWMWriterAdvanced** 和 **IWMWriterAdvanced2** 的所有方法。                       |
| [**IWMWriterPostView**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostview)     | 管理與 postviewing 範例相關的一些先進寫入功能。 Postviewing 正在查看輸出（通常是從編碼器）來檢查編碼/解碼程式是否正常運作。 |
| [**IWMWriterPreprocess**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpreprocess) | 管理寫入器所做的前置處理傳遞。 前置處理階段用來改善編碼輸出的品質。                                                                                  |



 

應用程式必須執行下列回呼介面，才能追蹤 postviewing 的進度。



| 介面                                                      | 描述                                                                                              |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**IWMWriterPostViewCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostviewcallback) | 管理如何從寫入器物件接收未壓縮的樣本，以預覽編解碼器的執行情況。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**物件**](objects.md)
</dt> <dt>

[**寫入 ASF 檔案**](writing-asf-files.md)
</dt> </dl>

 

 





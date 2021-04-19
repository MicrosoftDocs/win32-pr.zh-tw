---
title: 同步讀取器物件
description: 同步讀取器物件
ms.assetid: 52a4891f-03bf-4d8a-ab7b-e9739db30bc3
keywords:
- Windows Media Format SDK，同步讀取器物件
- Advanced Systems Format (ASF) ，同步讀取器物件
- ASF (Advanced Systems Format) ，同步讀取器物件
- 物件、同步讀取器物件
- 同步讀取器，物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 491fed915a049dbfc52acc24d06a0344d8e3109c
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "106969094"
---
# <a name="synchronous-reader-object"></a>同步讀取器物件

同步讀取器物件是用來讀取使用同步呼叫的數位媒體檔案。

同步讀取器物件是由函式 [**WMCreateSyncReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatesyncreader)所建立，它會將指標設定為 **IWMSyncReader** 介面。 同步讀取器介面所支援的其他介面可以藉由呼叫 **QueryInterface** 方法來取得。

同步讀取器物件支援下列介面。



| 介面                                | 描述                                                                                                                                                        |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)   | 設定和抓取標頭資訊，例如中繼資料、 [*標記*](wmformat-glossary.md)等等。                                            |
| [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2) | 列舉可用的編解碼器資訊。 繼承 **IWMHeaderInfo** 的所有方法。                                                                      |
| [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) | 支援大型屬性大小、重複的屬性名稱，以及多語言支援。 繼承 **IWMHeaderInfo** 和 **IWMHeaderInfo2** 的所有方法。 |
| [**IWMProfile**](iwmprofile.md)         | 提供對載入至讀取器之 Windows Media 檔案的設定檔資訊的存取。                                                                       |
| [**IWMProfile2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2)       | 抓取與設定檔相關聯 (GUID) 的全域唯一識別碼（如果有的話）。 繼承 **IWMProfile** 的所有方法。                               |
| [**IWMProfile3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3)       | 支援設定檔中的頻寬共用和串流優先順序資訊。 繼承 **IWMProfile** 和 **IWMProfile2** 的所有方法。                |
| [**IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)   | 提供數位媒體檔案的同步讀取功能。                                                                                                 |
| [**IWMSyncReader2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader2) | 提供搜尋至 SMPTE 時間碼以及手動設定樣本的支援。 繼承 **IWMSyncReader** 的所有方法。                            |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**物件**](objects.md)
</dt> <dt>

[**讀取器物件**](reader-object.md)
</dt> <dt>

[**使用同步讀取器讀取檔案**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 





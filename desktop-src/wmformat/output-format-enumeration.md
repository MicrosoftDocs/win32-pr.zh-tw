---
title: 輸出格式列舉
description: 輸出格式列舉
ms.assetid: 53d5724b-f875-4b2e-92fa-279f46111f29
keywords:
- Windows媒體格式 SDK，輸出格式列舉
- Advanced Systems Format (ASF) ，輸出格式列舉
- ASF (Advanced Systems Format) ，輸出格式列舉
- Windows媒體格式 SDK，IWMReaderTypeNegotiation 介面
- Advanced Systems Format (ASF) ，IWMReaderTypeNegotiation 介面
- ASF (Advanced Systems Format) ，IWMReaderTypeNegotiation 介面
- 輸出格式列舉
- IWMReaderTypeNegotiation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd1e6dacf4daac3f8c5f74fa1b4d9dd83c5cb3be538dc983b671a9f9096325f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027356"
---
# <a name="output-format-enumeration"></a>輸出格式列舉

讀取器物件和同步讀取器物件都會與編解碼器通訊，以列舉壓縮資料流程的可能輸出格式。 當您讀取包含以一或多個 Windows 媒體編解碼器壓縮之內容的檔案時，您可以檢查可能的輸出格式，以選擇最適合您需求的輸出格式。 為了方便起見，每個編解碼器都有預設輸出格式，它會設定為最常用的格式。 如需有關輸出列舉的詳細資訊，請參閱 [使用輸出](working-with-outputs.md)。

您可以根據媒體類型，對輸出格式進行某些變更。 例如，您可以變更影片串流的畫面格大小和色彩深度。 讀取物件都支援介面，以測試您對輸出格式（稱為 [**IWMReaderTypeNegotiation**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadertypenegotiation)）所做的變更。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**檔案讀取功能**](file-reading-features.md)
</dt> </dl>

 

 





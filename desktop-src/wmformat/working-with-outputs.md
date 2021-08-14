---
title: 使用輸出
description: 使用輸出
ms.assetid: e2e14e88-dddc-496d-8087-1455da0821e3
keywords:
- Windows媒體格式 SDK，使用輸出
- Advanced Systems Format (ASF) ，使用輸出
- ASF (Advanced Systems Format) ，使用輸出
- Advanced Systems Format (ASF) 、output 數位和格式
- ASF (Advanced Systems Format) 、output 數位和格式
- 輸出數位和格式，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 274e5b4980ef14126006d3f19fe0717aa9eb6fd5c1a8f7baaf91e35084faeacb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118697722"
---
# <a name="working-with-outputs"></a>使用輸出

根據預設，您從任一個 reader 物件收到的每個範例都會與一個輸出編號相關聯。 每個輸出編號都會對應到 ASF 檔案中的資料流程。 當檔案開啟時，讀取器會將輸出編號指派給檔案中的資料流程。 一般來說，檔案中的每個資料流程都會有一個輸出。 但是，如果檔案使用相互排除，則會為每個互斥資料流程群組指派一個輸出編號。 對應至互斥資料流程輸出數目的資料流程是由讀取器所決定，在多個位速率 (MBR) 檔，或您的應用程式中，如果您使用手動資料流程選取專案的話。

因為設定檔中設定的連接名稱不會保存在檔案中，所以讀取器會為每個輸出建立預設的連接名稱，而這只是輸出數位的字串表示，例如 "1"、"2"、"3" 等等。 連接名稱可讓應用程式和讀取器本身將輸出與資料流程產生相互關聯。 在多位元率檔案中，有數個串流共用一個連接名稱。 這對讀取器並不重要，因為每個 MBR 資料流程的輸出屬性都相同。

每個輸出都有一或多個支援的輸出格式。 輸出格式是由讀取器所提供的未壓縮範例所使用的格式。 當讀取器開啟檔案時，它會將每個輸出的格式設定為媒體子類型的預設值。 支援的輸出格式數目和類型是由解壓縮媒體資料的編解碼器所決定。

下列主題說明如何使用輸出：

-   [識別輸出編號](to-identify-output-numbers.md)
-   [指派輸出格式](assigning-output-formats.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IWMReader 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[**IWMSyncReader 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**讀取 ASF 檔案**](reading-asf-files.md)
</dt> </dl>

 

 





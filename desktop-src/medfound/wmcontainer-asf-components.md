---
description: WMContainer 物件提供對剖析和寫入 Advanced 系統格式 (ASF) 檔的低層級控制。
ms.assetid: 258ea139-581f-4b94-9655-43ecf1e77f10
title: WMContainer ASF 元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d7d1c1b76683cfe01dc0970ab1c077580215d2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944381"
---
# <a name="wmcontainer-asf-components"></a>WMContainer ASF 元件

WMContainer 物件提供對剖析和寫入 Advanced 系統格式 (ASF) 檔的低層級控制。

[管線層 ASF 元件](pipeline-layer-asf-components.md)會在內部使用 WMContainer 物件。 大部分的應用程式都應該使用管線元件，而不是使用 WMContainer 物件。 只有當您需要對剖析和寫入 ASF 檔案的低層級控制時，才能使用 WMContainer。

WMContainer 層包含下列物件：

-   [ASF 設定檔](asf-profile.md)
-   [ASF ContentInfo 物件](asf-contentinfo-object.md)
-   [ASF 分隔器](asf-splitter.md)
-   [ASF 多工器](asf-multiplexer.md)
-   [ASF 索引子](asf-index-object.md)

下列主題包含有關使用 WMContainer 來讀取或寫入 ASF 檔案的逐步指示。

-   [教學課程：使用 WMContainer 物件讀取 ASF 檔案](tutorial--reading-an-asf-file.md)
-   [教學課程：使用 WMContainer 物件複製 ASF 資料流程](tutorial--copying-asf-streams-from-one-file-to-another.md)
-   [教學課程：使用 WMContainer 物件撰寫 WMA 檔案](tutorial--writing-a-wma-file-by-using-cbr-encoding.md)

## <a name="about-wm-container"></a>關於 WM 容器

WMContainer 物件會直接與 ASF 檔案物件互動。 下圖顯示 ASF 檔案結構和對應的 WMContainer 物件。

![顯示 asf 檔案結構和對應的 media foundation 物件的圖表](images/asf-components01.png)

除了分隔器和多工器之外，每個物件都支援剖析 (讀取) 和寫入 ASF 檔。 分隔器只會用來讀取 ASF 檔。 多工器只用于撰寫新的 ASF 檔案。

WMContainer 物件所執行的所有作業都是同步的，這表示它們會封鎖呼叫執行緒。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體基礎中的 ASF 支援](asf-support-in-media-foundation.md)
</dt> </dl>

 

 




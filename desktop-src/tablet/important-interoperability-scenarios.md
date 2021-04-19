---
description: 為了讓 Tablet PC 應用程式能夠有效地操作筆墨，該應用程式應該能夠：
ms.assetid: 64a7b773-35c9-42f7-aec4-7fed34fa84d9
title: 重要互通性案例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6dca3bcbf52d673131122615fa5a08317dbf10c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106967091"
---
# <a name="important-interoperability-scenarios"></a>重要互通性案例

為了讓 Tablet PC 應用程式能夠有效地操作筆墨，該應用程式應該能夠：

-   將檔儲存為應用程式的原生二進位格式，而不會遺失檔的筆墨。
-   以任何格式儲存檔，讓應用程式正常支援 (例如 HTML 或 Rtf 格式 (RTF) ) ，而不會遺失檔的筆跡。
-   使用剪貼簿，將筆墨從某個應用程式複製到另一個應用程式。 如果另一個應用程式只會辨識特定格式，例如 HTML、RTF 或點陣圖 (BMP) ，這會很有用。 它也適用于目的地應用程式是否辨識筆跡。 如果它辨識筆墨，目的地應用程式就能夠解讀已複製為筆墨的筆墨，而不只是影像。
-   在辨識筆墨的兩個應用程式之間複製筆跡和文字，其中每一個都有一個以上的 [**筆墨**](inkdisp-class.md) 物件。 這需要 HTML、RTF 或類似的格式。
-   在兩個應用程式之間複製筆跡，每個應用程式都有一個 [**ink**](inkdisp-class.md) 物件。 筆跡序列化格式 (ISF) 即已足夠。
-   從具有一個以上 [**筆墨**](inkdisp-class.md) 物件的應用程式，將筆墨複製到只有一個 **筆墨** 物件的應用程式。 在此情況下，具有一個以上 **筆墨** 物件的應用程式必須能夠產生筆跡序列化格式 (ISF) 。
-   從具有一個 [**筆墨**](inkdisp-class.md) 物件的應用程式，將筆墨複製到具有多個 **筆墨** 物件的應用程式。 在此情況下，具有一個以上 **筆墨** 物件的應用程式必須能夠辨識 ISF。

 

 




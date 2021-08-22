---
description: 使用編解碼器
ms.assetid: c69e0ecf-5f72-4d77-90e6-0f493325c0f4
title: 使用編解碼器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 462a1340ef7e6a64aada586addcc73d95a993884fe2b026e74acde5fd286638c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118650617"
---
# <a name="working-with-codecs"></a>使用編解碼器

Microsoft Windows 提供數個編解碼器作為作業系統元件。 可用的編解碼器一律會包含隨附于任何版本的 DirectX 和 Windows Media Player 隨附于 Windows 版本中的編解碼器。 安裝較新版本的 DirectX 或 Windows Media Player 或安裝 Windows 媒體 SDK 執行時間時，可能會安裝其他編解碼器。 協力廠商可能會在主機系統上安裝其他編解碼器;這些編解碼器可以設計成隻能搭配特定應用程式使用，或可支援任何 DirectShow 應用程式的一般用途。

編解碼器可以用三種不同的方式來實行：

-   以視訊壓縮管理員所載入的 Windows 類型音訊或可安裝影片編解碼器的影片 (bc-vcm-lvm-hyperv) 或音訊壓縮管理員 (進行中) 。 一般而言，這項技術會被視為已淘汰，不建議使用。 可安裝的編解碼器會透過 AVI 解壓縮程式包裝函式篩選來參與 DirectShow 篩選圖形。
-   做為 DirectShow 的篩選準則。 許多協力廠商編解碼器會實作為原生 DirectShow 篩選準則。 其中一個篩選準則是 Frauenhofer MP3 解壓縮程式篩選器。 一般而言，這些篩選器可能會以一般方式新增至篩選圖形。 這項規則的唯一例外是某些 Windows 媒體™音訊或 Windows Media 視訊編解碼器，以及 Microsoft mpeg-2 編解碼器，無法手動新增至篩選圖形。 這些篩選準則只能由 ASF 讀取器和 ASF 寫入器篩選準則新增。
-   作為 DirectX 媒體物件 (DMOs) 。 DMOs 是執行編解碼器的建議方式，因為它們可以在 DirectShow 的篩選圖形內使用 DMO 包裝函式篩選器，或在任何其他非 DirectShow 型串流應用程式中獨立使用。 某些 Windows Media 音訊和 Windows Media 視訊編解碼器會實作為 DMOs。 如同 Windows 媒體篩選器，這些 DMOs 無法在 Windows 媒體 SDK 的內容之外使用。 這表示在 DirectShow 中，只能透過 asf 讀取器或 asf 寫入器篩選器，將它們新增至圖形。

在 GraphEdit 中，所有不同類型的編解碼器都會出現在下列類別之下：

-   音訊壓縮
-   影片壓縮
-   DirectShow 篩選

不過，其中許多編解碼器都是由協力廠商或其他 Microsoft 應用程式或作業系統元件所安裝，而不是供其他 DirectShow 應用程式使用。 GraphEdit 中顯示的編解碼器清單也取決於主機系統上執行的 Windows 版本，以及安裝的 DirectShow SDK 版本。

 

 




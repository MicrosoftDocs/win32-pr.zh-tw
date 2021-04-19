---
description: 使用編解碼器
ms.assetid: c69e0ecf-5f72-4d77-90e6-0f493325c0f4
title: 使用編解碼器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbe6d45608c3d95fee8f67344bdec0fc77431919
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106988687"
---
# <a name="working-with-codecs"></a>使用編解碼器

Microsoft Windows 提供數個編解碼器作為作業系統元件。 可用的編解碼器一律會包含隨附于任何版本的 DirectX 和 Windows Media Player 隨附于 Windows 版本中的編解碼器。 安裝較新版本的 DirectX 或 Windows Media Player 或 Windows Media SDK 執行時間時，可能會安裝其他編解碼器。 協力廠商可能會在主機系統上安裝其他編解碼器;這些編解碼器可以設計成隻能搭配特定應用程式使用，或可支援任何 DirectShow 應用程式一般使用。

編解碼器可以用三種不同的方式來實行：

-   影片壓縮管理員所載入的 Windows 類型音訊或可安裝影片的編解碼器， (BC-VCM-LVM-HYPERV) 或音訊壓縮管理員)  (的。 一般而言，這項技術會被視為已淘汰，不建議使用。 可安裝的編解碼器會透過 AVI 解壓縮程式包裝函式篩選器，參與 DirectShow 篩選圖形。
-   作為 DirectShow 篩選。 許多協力廠商編解碼器會實作為原生的 DirectShow 篩選。 其中一個篩選準則是 Frauenhofer MP3 解壓縮程式篩選器。 一般而言，這些篩選器可能會以一般方式新增至篩選圖形。 這項規則的唯一例外狀況是，某些 Windows Media™音訊或 Windows Media 視訊編解碼器，而 Microsoft MPEG-2 編解碼器無法手動新增至篩選圖形。 這些篩選準則只能由 ASF 讀取器和 ASF 寫入器篩選準則新增。
-   作為 DirectX 媒體物件 (DMOs) 。 DMOs 是執行編解碼器的建議方式，因為它們可以在使用 SQL-DMO 包裝函式的 DirectShow 篩選圖形內使用，或在任何其他非 DirectShow 串流應用程式中獨立使用。 某些 Windows Media 音訊和 Windows Media 視訊編解碼器會實作為 DMOs。 如同 Windows Media 篩選器，這些 DMOs 無法在 Windows Media SDK 的內容之外使用。 這表示在 DirectShow 中，只能透過 ASF 讀取器或 ASF 寫入器篩選器，將它們新增至圖形。

在 GraphEdit 中，所有不同類型的編解碼器都會出現在下列類別之下：

-   音訊壓縮
-   影片壓縮
-   DirectShow 篩選

不過，其中許多編解碼器都是由協力廠商或其他 Microsoft 應用程式或作業系統元件所安裝，而不是供其他的 DirectShow 應用程式使用。 GraphEdit 中顯示的編解碼器清單也取決於主機系統上執行的 Windows 版本，以及已安裝的 DirectShow SDK 版本。

 

 




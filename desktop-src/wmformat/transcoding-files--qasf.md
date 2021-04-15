---
title: '轉碼檔案 (QASF) '
description: '轉碼檔案 (QASF) '
ms.assetid: c6dad6cf-4781-4204-883b-cdb33aff5e27
keywords:
- 'Windows Media Format SDK、轉碼檔案 (QASF) '
- Windows Media Format SDK、DirectShow
- 'Advanced Systems Format (ASF) 、轉碼檔案 (QASF) '
- 'ASF (Advanced Systems Format) 、轉碼檔案 (QASF) '
- Advanced Systems Format (ASF) 、DirectShow
- ASF (Advanced Systems Format) ，DirectShow
- 'DirectShow、轉碼檔案 (QASF) '
- Windows Media Format SDK、QASF
- Advanced Systems Format (ASF) ，QASF
- ASF (Advanced Systems Format) ，QASF
- DirectShow、QASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14387a65538d411bcd41b4b907f2adbab2089f71
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104568202"
---
# <a name="transcoding-files-qasf"></a>轉碼檔案 (QASF) 

您可以透過各種方式使用 [WM ASF 寫入器](wm-asf-writer-filter.md) 來建立檔案轉碼篩選圖形。 最簡單的方式是將 WM ASF 寫入器共同建立、設定和新增至篩選圖形，然後使用 **IGraphBuilder：： RenderFile** 方法自動建立圖形。

另一種方式是將每個篩選手動新增至圖形並連接釘選。 新增 WM ASF 寫入器之後，如果預設設定檔不適用，請使用 **IConfigAsfWriter** 方法進行設定，並將 WM ASF 寫入器輸入接點連接到上游篩選器上對應的輸出圖釘。

下圖顯示典型的 WM ASF 寫入器轉碼篩選圖形設定。

![一般轉碼篩選圖形](images/asf-transcode.png)

 

 





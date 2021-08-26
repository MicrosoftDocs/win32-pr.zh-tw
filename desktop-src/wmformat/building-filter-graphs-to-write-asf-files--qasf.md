---
title: '建立篩選圖形來將 ASF 檔案寫入 (QASF) '
description: '建立篩選圖形來將 ASF 檔案寫入 (QASF) '
ms.assetid: 45583c97-4e59-4a6a-987b-5486e6f33990
keywords:
- 'Windows媒體格式 SDK，建立篩選圖形 (QASF) '
- Windows媒體格式 SDK，DirectShow
- 'Windows媒體格式 SDK， (QASF 寫入 ASF 檔案) '
- 'Advanced Systems Format (ASF) 、建立篩選圖形 (QASF) '
- 'ASF (Advanced Systems Format) ，建立篩選圖形 (QASF) '
- 'Advanced Systems Format (ASF) 、撰寫 (QASF) '
- 'ASF (Advanced Systems Format) 、撰寫 (QASF) '
- Advanced Systems Format (ASF) ，DirectShow
- ASF (Advanced Systems Format) ，DirectShow
- 'DirectShow，建立篩選圖形 (QASF) '
- 'DirectShow， (QASF 撰寫 ASF 檔案) '
- Windows媒體格式 SDK，QASF
- Advanced Systems Format (ASF) ，QASF
- ASF (Advanced Systems Format) ，QASF
- DirectShow、QASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6128fb7578d829579aad7e8895be9db4d5a842aa785866253b553d4deb8b3b8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055578"
---
# <a name="building-filter-graphs-to-write-asf-files-qasf"></a>建立篩選圖形來將 ASF 檔案寫入 (QASF) 

以 DirectShow 為基礎的應用程式通常會在建立 Windows 媒體型內容時，使用三種基本類型的篩選圖形之一：

-   篩選圖形，可將內容從其他格式轉換或轉碼成 Windows 媒體格式。
-   用來將不 Windows 媒體型 (原生串流) 格式的內容，插入至 ASF 檔案的篩選圖形。
-   在將即時資料儲存至磁片之前，先篩選圖形來取得即時資料，並立即將其編碼為 Windows 媒體格式。

下列各節將詳細說明每一種篩選圖形類型。



| 區段                                                                                                             | 描述                                                                                           |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [轉碼檔案 (QASF) ](transcoding-files--qasf.md)                                                             | 描述如何建立檔轉碼篩選圖形。                                               |
| [將原生串流格式插入到 ASF 檔案 (QASF) ](inserting-native-stream-formats-into-asf-files--qasf.md)   | 說明如何將任何類型的壓縮或未壓縮的音訊或影片資料放入 ASF 檔案中。 |
| [將裝置直接從裝置捕獲到 ASF 檔案 (QASF) ](capturing-directly-from-a-device-to-an-asf-file--qasf.md) | 描述如何建立輸出至 ASF 檔案的捕獲篩選圖形。                             |



 

 

 





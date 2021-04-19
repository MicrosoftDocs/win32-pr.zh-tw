---
title: '將裝置直接從裝置捕獲到 ASF 檔案 (QASF) '
description: '將裝置直接從裝置捕獲到 ASF 檔案 (QASF) '
ms.assetid: 684a11e3-d507-4219-bc0b-6dfe5e85dad1
keywords:
- 'Windows Media 格式 SDK，從裝置到 ASF 檔案 (QASF) '
- Windows Media Format SDK、DirectShow
- 'Advanced Systems Format (ASF) ，從裝置 (QASF) '
- 'ASF (Advanced Systems Format) ，從裝置 (QASF) '
- Advanced Systems Format (ASF) 、DirectShow
- ASF (Advanced Systems Format) ，DirectShow
- 'DirectShow，從裝置到 ASF 檔案 (QASF) '
- Windows Media Format SDK、QASF
- Advanced Systems Format (ASF) ，QASF
- ASF (Advanced Systems Format) ，QASF
- DirectShow、QASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faaf5ba8df3cffbb2121451d3bd1b456fc994078
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968243"
---
# <a name="capturing-directly-from-a-device-to-an-asf-file-qasf"></a>將裝置直接從裝置捕獲到 ASF 檔案 (QASF) 

當直接將音訊或影片捕獲到 ASF 檔案時，篩選圖形看起來會像下圖，視所使用的捕獲裝置類型而定。

![網路攝影機到 wmv 的拍攝圖](images/asf-webcam.png)

DirectShow SDK 檔會詳細說明如何建立捕獲圖形，但在使用 WM ASF 寫入器建立「capture graph」時，有一個重點需要注意：如果您的所有 pin 都已連接，則不會執行 WM ASF 寫入器。 如果您使用預設系統設定檔來設定 WM ASF 寫入器 (不建議使用) ，或任何包含音訊和影片串流的設定檔，則會為每個串流建立輸入 pin，而且必須連線到每個輸出。 例如，如果您不想要捕獲音訊，請務必使用僅限影片的設定檔來設定篩選，如此就不會建立音訊 pin。

 

 





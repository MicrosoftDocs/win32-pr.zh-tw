---
title: '將原生串流格式插入到 ASF 檔案 (QASF) '
description: '將原生串流格式插入到 ASF 檔案 (QASF) '
ms.assetid: ec7a69f3-0d4c-43dd-8d4b-fe066329a98f
keywords:
- 'Windows Media Format SDK、原生串流格式 (QASF) '
- 'Windows Media Format SDK，將原生串流格式插入到 ASF 檔案 (QASF) '
- Windows Media Format SDK、DirectShow
- 'Advanced Systems Format (ASF) ， (QASF 插入原生串流格式) '
- 'ASF (Advanced Systems Format) ， (QASF 插入原生串流格式) '
- 'Advanced Systems Format (ASF) 、原生串流格式 (QASF) '
- 'ASF (Advanced Systems Format) ，原生串流格式 (QASF) '
- Advanced Systems Format (ASF) 、DirectShow
- ASF (Advanced Systems Format) ，DirectShow
- 'DirectShow、原生串流格式 (QASF) '
- 'DirectShow，將原生串流格式插入到 ASF 檔案 (QASF) '
- Windows Media Format SDK、QASF
- Advanced Systems Format (ASF) ，QASF
- ASF (Advanced Systems Format) ，QASF
- DirectShow、QASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af4736c450b3620a05fe01dcc1808adc297ebbd1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840576"
---
# <a name="inserting-native-stream-formats-into-asf-files-qasf"></a>將原生串流格式插入到 ASF 檔案 (QASF) 

根據預設， [WM ASF 寫入器](wm-asf-writer-filter.md) 預期會在其輸入 pin 上使用未壓縮的音訊和影片串流，並且會使用 Windows MEDIA 格式 SDK 來存取 Windows Media 音訊，並 Windows Media 視訊可壓縮資料流程的編解碼器。 但是 ASF 檔案容器可以用於任何類型的資料。 藉由將數位媒體資料放入 ASF 檔案容器中，您可以新增 ASF 提供的功能，例如中繼資料和數位版權管理 (DRM) ，而不需要轉碼您的內容。

若要建立包含非以 Windows Media 為基礎之內容的 ASF 檔案，應用程式必須在 WM ASF 寫入器的篩選圖形上游中壓縮資料流程，然後藉由呼叫 [**IConfigAsfWriter2：： SetParam**](iconfigasfwriter2-setparam.md) 來略過 Wm Asf 寫入器的壓縮機制，如下所示：


```C++
pConfigAsfWriter2->SetParam(AM_CONFIGASFWRITER_PARAM_DONTCOMPRESS,TRUE,0)

```



然後使用所需的設定檔來設定篩選。 輸入資料流程的媒體類型必須完全符合設定檔中的格式。 在某些情況下，您可能需要檢查輸入資料流程的格式，並建立自訂設定檔以符合此格式。 如需詳細資訊，請參閱 [使用協力廠商編解碼器建立 ASF](to-create-asf-files-using-third-party-codecs.md)檔案。

當您將 WM ASF 寫入器連線到上游篩選器時，請使用 **IGraphBuilder：： ConnectDirect** 方法。 請勿使用任何 "智慧型 connect" 方法（例如 **IGraphBuilder：： connect** 或 **IGraphBuilder：： RenderFile** ）來連接篩選，因為這樣會停用篩選準則的「略過壓縮」模式。

 

 





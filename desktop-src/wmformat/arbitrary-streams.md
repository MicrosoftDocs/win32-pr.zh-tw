---
title: 任意資料流程
description: 任意資料流程
ms.assetid: 81fd3b07-7cf2-4013-97ed-9718142ca4c3
keywords:
- Windows媒體格式 SDK，任意資料流程
- Advanced Systems Format (ASF) ，任意串流
- ASF (Advanced Systems Format) ，任意串流
- Windows媒體格式 SDK，資料流程
- Advanced Systems Format (ASF) 、串流
- ASF (Advanced Systems Format) ，資料流程
- 任意資料流程
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b2cc0587758af8dfa3d4ee05b1a51943a89684629fe2182f5a33fdabbdb68e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118434714"
---
# <a name="arbitrary-streams"></a>任意資料流程

除了音訊和影片串流和影像串流之外，ASF 檔案也可以容納包含各種資料的資料流程。 Windows 媒體格式 SDK 的物件提供腳本資料流程、檔案傳輸資料流程、Web 資料流程和任意資料流程的支援。 這些資料流程類型全都是任意的，這表示讀取物件不會執行任何資料驗證。 當您在檔案中包含這些類型的資料流程時，請確定讀取應用程式會執行驗證或資料檢查，以確保您的內容未損毀或刻意遭到惡意的協力廠商損害。

雖然此 SDK 的物件不會驗證或驗證任意資料流程中的資料，但原生支援數種類型的任意資料流程。 下表列出預先定義的任意資料流程類型。 此外，也支援腳本資料流程，但在 [指令碼命令](script-commands.md) 區段中會另外討論。 如需建立自訂類型的詳細資訊，請參閱 [自訂任意資料流程](custom-arbitrary-data-streams.md)。



| 任意類型                   | 描述                                                       |
|----------------------------------|-------------------------------------------------------------------|
| [文字資料流](text-streams.md) | 包含文字字串。                                             |
| [檔案資料流程](file-streams.md) | 包含一或多個資料檔案。                                   |
| [Web 串流](web-streams.md)   | 包含相當於網頁快取版本的資料檔案。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**ASF 檔案功能**](asf-file-features.md)
</dt> <dt>

[**音訊和影片串流**](audio-and-video-streams.md)
</dt> <dt>

[**設定任意資料流程類型**](configuring-arbitrary-stream-types.md)
</dt> </dl>

 

 





---
description: 本節說明如何使用轉碼 API 來重新編碼媒體檔案。 轉碼 API 是在 Windows 7 中引進的。
ms.assetid: 24bf68a8-39bf-4302-b28c-71bb23b63469
title: 轉碼 API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9783c6f99a25ba6835171dcc7f7555a1f747c72b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848703"
---
# <a name="transcode-api"></a>轉碼 API

本節說明如何使用轉碼 API 來重新編碼媒體檔案。 轉碼 API 是在 Windows 7 中引進的。

*轉碼* 是將數位媒體檔案從一種格式轉換成另一種格式。 轉碼 API 是設計來搭配 [媒體會話](media-session.md)使用。 它簡化了某些轉碼應用程式類型的媒體會話使用：

-   固定位元速率 (CBR) 編碼方式，這是預先知道的目標位速率。
-   最多一個音訊串流和一個影片串流。
-   從檔案和檔案進行編碼。

轉碼 API 不支援下列各項：

-   變數位元速率 (VBR) 或多重傳遞編碼。
-   多個音訊串流或多個影片串流。
-   受 DRM 保護的內容，而不是以 WMDRM 保護的 ASF 檔案。
-   即時串流，例如即時至檔案串流或即時串流。

如果您的編碼應用程式符合這些條件約束，轉碼 API 會比單獨使用媒體會話更簡單的程式設計模型。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                          | 描述                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [關於轉碼 API](about-the-transcode-api.md)<br/>                              | 提供轉碼 API 的一般總覽。<br/>                                                                                                                                                                |
| [使用轉碼 API](fast-transcode-objects.md)<br/>                               | 描述應用程式如何使用轉碼 API。<br/>                                                                                                                                                             |
| [教學課程：編碼的檔](tutorial--encoding-an-mp4-file-.md)<br/>               | 說明如何使用轉碼 API 來編碼數量檔案的逐步教學課程。<br/>                                                                                                                           |
| [教學課程：編碼 WMA 檔案](tutorial--converting-an-mp3-file-to-a-wma-file.md)<br/> | 示範如何使用轉碼 API 將 WMA 檔案編碼。 本教學課程會修改教學課程中所顯示的 [程式碼：編碼的檔](tutorial--encoding-an-mp4-file-.md)，因此您應該先閱讀該教學課程。<br/> |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[編碼與檔案編寫](encoding-and-file-authoring.md)
</dt> <dt>

[媒體基礎：基本概念](media-foundation-programming--essential-concepts.md)
</dt> <dt>

[媒體基礎中的編碼總覽](overview-of-encoding-in-media-foundation.md)
</dt> </dl>

 

 





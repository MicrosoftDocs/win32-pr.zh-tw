---
description: 當您提供預覽時，應遵循下列指導方針。
title: 預覽處理常式指導方針
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 3538cc5d-afb6-4d43-b527-6c6e1d773b41
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 2ed9250e06d2b970ba92bffd10bf80fc6495793b8a9b0237d257b45feb10a99a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118719626"
---
# <a name="preview-handler-guidelines"></a>預覽處理常式指導方針

當您提供預覽時，應遵循下列指導方針。

-   預覽版應包含基本的 UI，只是預覽。 它應該只顯示檔案內容。 它不應該顯示對話方塊、啟動顯示畫面、工具列或工作窗格。 讀取窗格通常會與搜尋搭配使用，以快速識別檔案。 Clutters [閱讀] 窗格或從檔案內容會使或在預覽顯示期間造成延遲的任何事，都應予以避免。
-   預覽版應可讓使用者在檔中流覽。 使用者也應該可以選取和複製文字。
-   預覽應該不需要海量儲存體，應該耗用最少量的資源，而且應該要有快速的啟動時間。
-   基於安全性和隱私權目的，應封鎖正在預覽的檔案中的所有腳本和宏。
-   預覽版應該支援應用程式所支援的導覽和選取的鍵盤快速鍵。 當您按一下滑鼠右鍵時，也應該會顯示內容功能表。
-   當檔案顯示為預覽時，預覽不應鎖定檔案本身。 您可以同時在其相關聯的應用程式中預覽及開啟檔案。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[預覽處理常式和 Shell 預覽主機](preview-handlers.md)
</dt> <dt>

[建立預覽處理常式](building-preview-handlers.md)
</dt> </dl>

 

 




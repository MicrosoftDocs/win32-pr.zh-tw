---
title: 索引
description: 索引
ms.assetid: 54c694f6-3c10-4d7c-bcd1-f2b17d652e8e
keywords:
- Windows Media Format SDK，索引
- Advanced Systems Format (ASF) 、索引
- ASF (Advanced Systems Format) ，索引
- Windows Media Format SDK，時態索引
- Advanced Systems Format (ASF) 、時態性索引
- ASF (Advanced Systems Format) ，時態索引
- Windows Media 格式 SDK，以框架為基礎的索引
- Advanced Systems Format (ASF) ，以框架為基礎的索引
- ASF (Advanced Systems Format) ，以框架為基礎的索引
- Windows Media Format SDK、SMPTE 時間碼
- Advanced Systems Format (ASF) 、SMPTE 時間碼
- ASF (Advanced Systems Format) ，SMPTE 時間碼
- 索引，關於
- 時態性索引
- 以框架為基礎的索引
- SMPTE 時間代碼，索引
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d2e5a194f9c495720cbc40ccdb192509723eee0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840580"
---
# <a name="indexes"></a>索引

讀取數位媒體檔案的應用程式，常見的需求是能夠搜尋內容中的特定點。 搜尋可能很困難，因為無法保證檔案中的各種資料流程都具有並行開始時間的範例。 使用 *索引* 時，會解決此問題。 索引是一種 ASF 檔案中的物件，其呈現時間與影片範例相同。 音訊串流不需要任何索引，因為音訊資料比影片資料更緊密地與展示時間連接。

Windows Media 格式 SDK 的索引子物件可以建立三種不同類型的索引：時態性索引、以框架為基礎的索引，以及 SMPTE 時間碼索引。

時態性索引是最常見的類型。 它們只是將影片範例等同于相對應的呈現時間。

以畫面格為基礎的索引等於影片範例與影片框架數位和呈現時間。 框架數位在編輯影片的應用程式中特別有用。

SMTPE 時間代碼索引是索引的碩果僅存類型。 它會使用 SMPTE 時間碼作為索引的基礎，而且只能用於其範例內含 SMPTE 時間戳記的資料流程。 如需有關 SMPTE 時間代碼的詳細資訊，請參閱 [Smpte 時間程式碼支援](smpte-time-code-support.md)。

ASF 檔案可以針對其所包含的每個影片資料流程，包含每個類型的索引。 根據預設，在寫入器物件所建立的檔案中，每個影片資料流程都會包含時態索引。 您可以變更檔案的自動編制索引設定，以符合您的需求。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**ASF 檔案功能**](asf-file-features.md)
</dt> <dt>

[**使用索引**](working-with-indexes.md)
</dt> <dt>

[**使用非同步讀取器讀取檔案**](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[**使用同步讀取器讀取檔案**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 





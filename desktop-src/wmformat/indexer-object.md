---
title: 索引子物件
description: 索引子物件
ms.assetid: 652e04a5-ed6e-4e92-acf4-55ed82f77ef1
keywords:
- Windows Media Format SDK，索引子物件
- Advanced Systems Format (ASF) 、索引子物件
- ASF (Advanced 系統格式) 、索引子物件
- 物件、索引子物件
- 索引子物件
- 索引，索引子物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71c9aa8c1c3ff694ae8e125e17dc0190451c7f21
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/21/2020
ms.locfileid: "104023153"
---
# <a name="indexer-object"></a>索引子物件

索引子物件會在 ASF 檔案中建立索引。 索引是一種 ASF 檔案的標準部分，其等同于具有時間、框架數位或 (的影片樣本（如果適用) 的運動圖片和電視工程師 (SMPTE) 標準時間戳）。 如果沒有索引，讀取器物件和同步讀取器物件都無法搜尋檔案中間的某個點。

只有當檔案包含一或多個影片資料流程時，才需要這個物件所建立的索引。 這是因為音訊資料未暫時壓縮，因此可讓您輕鬆地在音訊串流中尋找指定的時間。

索引子物件是由 [**WMCreateIndexer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateindexer) 函式所建立，它會將指標設定為 **IWMIndexer** 介面。 您可以藉由呼叫 **QueryInterface** 方法來取得索引子物件的其他介面。

下列是索引子物件支援的介面。



| 介面                          | 描述                                                                         |
|------------------------------------|-------------------------------------------------------------------------------------|
| [**IWMIndexer**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmindexer)   | 啟動和停止編制索引程式。                                              |
| [**IWMIndexer2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmindexer2) | 設定索引子，依框架、時間或 SMPTE 時間程式碼啟用索引編制。 |



 

下列回呼介面必須由應用程式執行，才能使用索引子物件。



| 介面                                      | 描述                                                                |
|------------------------------------------------|----------------------------------------------------------------------------|
| [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | 接收在個別執行緒中執行之進程的狀態訊息。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**物件**](objects.md)
</dt> <dt>

[**使用索引**](working-with-indexes.md)
</dt> </dl>

 

 





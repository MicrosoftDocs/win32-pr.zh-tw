---
title: 將資料從一個檔案複製到另一個檔案
description: 將資料從一個檔案複製到另一個檔案
ms.assetid: 1403c396-46ea-48b1-a535-922ffca31bc2
keywords:
- Windows媒體格式 SDK，複製資料
- Advanced Systems Format (ASF) ，複製資料
- ASF (Advanced Systems Format) ，複製資料
- 資料流程，複製資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e2fe8369a8e3ebef6bca191ceffdac7c284889b0afdb4145fbec9c44702a1a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118705073"
---
# <a name="copying-data-from-one-file-to-another"></a>將資料從一個檔案複製到另一個檔案

在最基本的層級上，將資料流程從一個 ASF 檔案複製到另一個 ASF 檔案相當簡單。 不過，在處理來自多個輸入檔的資料流程或複製您先解壓縮並重新編碼的資料流程時，需要考慮一些問題。

下列各節說明複製資料流程。



| 區段                                                                                              | Descripiton                                                                                    |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [複製資料流程而不解壓縮資料](copying-streams-without-decompressing-the-data.md) | 描述如何使用壓縮的範例複製資料流程，以保留內容的品質。 |
| [使用解壓縮的範例複製資料流程](copying-streams-using-decompressed-samples.md)         | 描述使用解壓縮的範例複製資料流程時的困難之處。                      |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**設定檔管理員物件**](profile-manager-object.md)
</dt> <dt>

[**串流設定物件**](stream-configuration-object.md)
</dt> <dt>

[**同步讀取器物件**](synchronous-reader-object.md)
</dt> <dt>

[**寫入器物件**](writer-object.md)
</dt> </dl>

 

 





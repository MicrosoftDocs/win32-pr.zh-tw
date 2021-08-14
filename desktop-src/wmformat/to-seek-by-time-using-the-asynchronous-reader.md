---
title: 使用非同步讀取器依時間進行搜尋
description: 使用非同步讀取器依時間進行搜尋
ms.assetid: 731b0a6e-1472-45a7-998c-e395be86036f
keywords:
- Advanced Systems Format (ASF) ，依時間搜尋
- ASF (Advanced Systems Format) ，依時間搜尋
- Advanced Systems Format (ASF) 、非同步讀取器
- ASF (Advanced 系統格式) 、非同步讀取器
- 非同步讀取器，依時間搜尋
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 070d480cade395cdbead99b1aedde8928c6fb18b4af15bf6b72c1bcc0dcd6dc3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118196457"
---
# <a name="to-seek-by-time-using-the-asynchronous-reader"></a>使用非同步讀取器依時間進行搜尋

如果您想要在 ASF 檔案中搜尋特定的呈現時間，必須正確設定檔案。 根據預設，您只能搜尋音訊檔案，但必須先編制影片檔案的索引，才能進行搜尋。 如果您不確定如何建立檔案，您可以藉 \_ 由呼叫 [**IWMHeaderInfo：： GetAttributeByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname)來檢查檔案標頭中的 g wszWMSeekable 屬性。

若要使用非同步讀取器以展示時間來搜尋 ASF 檔案中的資料，請呼叫 [**IWMReader：： Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start)，然後將您想要讀取之檔案部分的所需時間和持續時間，傳遞為 *cnsStart* 和 *cnsDuration* 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IWMReader 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[**使用非同步讀取器讀取檔案**](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[**在播放時讀取中繼資料**](reading-metadata-at-playback.md)
</dt> <dt>

[**使用索引**](working-with-indexes.md)
</dt> </dl>

 

 





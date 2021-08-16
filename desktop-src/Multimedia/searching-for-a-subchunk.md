---
title: 搜尋 Subchunk
description: 搜尋 Subchunk
ms.assetid: c494a57f-6395-40a4-a4f2-d200d7ad6223
keywords:
- 多媒體檔案 i/o，搜尋 RIFF 區塊
- 檔案 i/o，搜尋 RIFF 區塊
- 輸入和輸出 (i/o) ，搜尋 RIFF 區塊
- I/o (輸入和輸出) ，搜尋 RIFF 區塊
- 搜尋 RIFF 區塊
- " (RIFF) 的資源交換檔案格式"
- 'RIFF (資源交換檔案格式) '
- RIFF I/O
- RIFF 區塊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9f77cc4d3b9640e0d262a113d3c8f352bb30fce625737b1bf13dde24adbe578
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118371136"
---
# <a name="searching-for-a-subchunk"></a>搜尋 Subchunk

下列範例會使用 [**mmioDescend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend) 函數來搜尋先前範例 "RIFF" 區塊中的 "bcp.fmt" 區塊。


```C++
// Find the format chunk (form type "FMT"); it should be 
// a subchunk of the "RIFF" parent chunk. 
mmckinfoSubchunk.ckid = mmioFOURCC('f', 'm', 't', ' '); 
if (mmioDescend(hmmio, &mmckinfoSubchunk, &mmckinfoParent, 
    MMIO_FINDCHUNK)) 
    // Error, cannot find the "FMT" chunk. 
else 
    // "FMT" chunk found. 
```



若要搜尋 subchunk (也就是 "RIFF" 或 "LIST" 區塊以外的任何區塊) ，請在 [**mmioDescend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend)函數的 *lpckParent* 參數中識別其父區塊。

如果您未指定父區塊，則在呼叫 **mmioDescend** 函式之前，目前的檔案位置應該在區塊的開頭。 如果您指定了父區塊，則目前的檔案位置可以是該區塊中的任何位置。

如果搜尋 subchunk 失敗，則表示目前的檔案位置是未定義的。 您可以使用 [**mmioSeek**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek)函式和 [**MMCKINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-mmckinfo)結構的 **dwDataOffset** 成員來描述父區塊，以向後搜尋至父區塊的開頭，如下列範例所示：


```C++
mmioSeek(hmmio, mmckinfoParent.dwDataOffset + 4, SEEK_SET); 
```



因為 **dwDataOffset** 指定了區塊資料部分開頭的位移，所以您必須搜尋4位元組之前的 **dwDataOffset** ，以設定表單類型之後的檔案位置。

 

 
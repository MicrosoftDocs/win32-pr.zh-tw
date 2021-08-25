---
title: 使用 mmioOpen 開啟檔案
description: 使用 mmioOpen 開啟檔案
ms.assetid: 947d1b1c-ec00-4bd9-948a-4b8e3bfb84f6
keywords:
- 多媒體檔案 i/o，開啟檔案
- 檔案 i/o，開啟檔案
- 輸入和輸出 (i/o) ，開啟檔案
- I/o (輸入和輸出) ，開啟檔案
- 多媒體檔案 i/o，mmioOpen 函式
- file i/o，mmioOpen 函式
- 輸入和輸出 (i/o) ，mmioOpen 函式
- I/o (輸入和輸出) ，mmioOpen 函式
- mmioOpen 函式
- 開啟 i/o 檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffbd323e888b181b0166572d11687d3dde66e83f0ce73541555b1f49083564ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893188"
---
# <a name="opening-a-file-with-mmioopen"></a>使用 mmioOpen 開啟檔案

若要開啟基本 i/o 作業的檔案，請將 [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen)函數的 *lpmmioinfo* 參數設定為 **Null**。 下列範例會開啟名為 "C： \\ SAMPLES \\SAMPLE1.TXT" 的檔案進行讀取，並檢查錯誤的傳回值。


```C++
HMMIO hFile; 

if ((hFile = mmioOpen("C:\\SAMPLES\\SAMPLE1.TXT", NULL, 
    MMIO_READ)) != NULL) 
    // File opened successfully. 
else 
    // File cannot be opened. 
```



使用 **mmioOpen** 的 *dwFlags* 參數來指定用來開啟檔案的旗標。

 

 
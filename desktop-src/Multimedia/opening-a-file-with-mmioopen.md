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
ms.openlocfilehash: c2123b73c5f3a93cbb6e72711a7137652f7534b2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104463121"
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

 

 
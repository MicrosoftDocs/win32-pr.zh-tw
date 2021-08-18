---
title: 建立和刪除檔案
description: 建立和刪除檔案
ms.assetid: a4b4a310-7230-4f1d-b084-c47db39adaac
keywords:
- 多媒體檔案 i/o，建立檔案
- 檔案 i/o，建立檔案
- 輸入和輸出 (i/o) ，建立檔案
- I/o (輸入和輸出) ，建立檔案
- 建立 i/o 檔案
- 多媒體檔案 i/o，刪除檔案
- 檔案 i/o，刪除檔案
- 輸入和輸出 (i/o) ，刪除檔案
- I/o (輸入和輸出) ，刪除檔案
- 刪除 i/o 檔案
- mmioOpen 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91a2ee8e70508e2c5dc3b24c084cf0b081b6629a519703ef43a15845ef3ec76a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119785728"
---
# <a name="creating-and-deleting-a-file"></a>建立和刪除檔案

若要建立檔案，請將 [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen)函數的 *dwOpenFlags* 參數設定為 MMIO \_ create。 下列範例會建立檔案，並將它開啟以供讀取和寫入。


```C++
HMMIO hFile; 

hFile = mmioOpen("NEWFILE.TXT", NULL, MMIO_CREATE | MMIO_READWRITE); 
if (hFile != NULL) 
    // File created successfully. 
else 
    // File cannot be created. 
```



如果您要建立的檔案已經存在，則會截斷為零長度。

若要刪除檔案，請將 **mmioOpen** 函數的 *dwOpenFlags* 參數設定為 MMIO \_ delete。 當您刪除檔案之後，就無法以任何標準方法復原。 如果您的應用程式在使用者要求時刪除檔案，請在刪除該檔案之前先查詢使用者，以確定使用者想要刪除它。

 

 
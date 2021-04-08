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
ms.openlocfilehash: c22cd6330874d0b5da74d69193359c025c709c79
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103681875"
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

 

 
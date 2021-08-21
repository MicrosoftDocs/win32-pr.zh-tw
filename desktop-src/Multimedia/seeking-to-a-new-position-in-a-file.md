---
title: 搜尋檔案中的新位置
description: 搜尋檔案中的新位置
ms.assetid: 276c3e43-bf9f-4a0a-b33a-7eaa701e92a6
keywords:
- 多媒體檔案 i/o，移至檔案開頭
- 檔案 i/o，移至檔案開頭
- 輸入和輸出 (i/o) ，移至檔案開頭
- I/o (輸入和輸出) ，移至檔案開頭
- 移至 i/o 檔案的開頭
- 多媒體檔案 i/o，搜尋檔案中的新位置
- 檔案 i/o，搜尋檔案中的新位置
- 輸入和輸出 (i/o) ，以搜尋檔案中的新位置
- I/o (輸入和輸出) ，搜尋檔案中的新位置
- 搜尋 i/o 檔案中的新位置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97e51ab51065bcdf89af84f2fd622558261dd4cf42cac3e50fe54fb116a7ad9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118136582"
---
# <a name="seeking-to-a-new-position-in-a-file"></a>搜尋檔案中的新位置

下列範例會使用 [**mmioSeek**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek) 函數，移至開啟檔案的開頭。


```C++
mmioSeek(hFile, 0L, SEEK_SET); 
```



下列範例會移至開啟檔案的結尾。


```C++
mmioSeek(hFile, 0L, SEEK_END); 
```



下列範例會從開啟的檔案結尾移至10個位元組的位置。


```C++
mmioSeek(hFile, -10L, SEEK_END); 

```



 

 
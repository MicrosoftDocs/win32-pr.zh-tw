---
title: 產生 Four-Character 碼
description: 產生 Four-Character 碼
ms.assetid: dfb771f1-9273-4f60-a3af-3a62a3794e59
keywords:
- 多媒體檔案 i/o，四個字元的代碼
- 檔案 i/o，四個字元的代碼
- 輸入和輸出 (i/o) ，四個字元的代碼
- I/o (輸入和輸出) 四個字元的代碼
- 四個字元的代碼
- mmioStringToFOURCC 函式
- mmioFOURCC 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96dd724876a3c4b6ac37424b49411edac5929c61d1fcf6c8c18275b1d6ae9dd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119785308"
---
# <a name="generating-four-character-codes"></a>產生 Four-Character 碼

您可以使用 [**mmioFOURCC**](/windows/win32/api/vfw/nf-vfw-mmiofourcc) 宏或 [**mmioStringToFOURCC**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc) 函數來產生四個字元的代碼。 下列範例會使用 **mmioFOURCC** ，為 "WAVE" 產生四個字元的代碼。


```C++
FOURCC fourccID; 
. 
. 
. 
fourccID = mmioFOURCC('W', 'A', 'V', 'E'); 
 
```



下列範例會使用 [**mmioStringToFOURCC**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc) ，為 "WAVE" 產生四個字元的代碼。


```C++
FOURCC fourccID; 
. 
. 
. 
fourccID = mmioStringToFOURCC("WAVE", 0); 
```



[**MmioStringToFOURCC**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc)中的第二個參數會指定用來將字串轉換成四個字元代碼的旗標。 如果您指定 MMIO \_ TOUPPER 旗標， **mmioStringToFOURCC** 會將字串中的所有字母字元轉換成大寫。 當您需要指定四個字元的代碼來識別自訂 i/o 程式時，這會很有用，因為識別副檔名的四個字元的程式碼必須全部都是大寫。

 

 
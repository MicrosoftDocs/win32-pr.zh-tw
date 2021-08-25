---
title: 搜尋 RIFF 區塊
description: 搜尋 RIFF 區塊
ms.assetid: ce974fb3-3af0-4400-8f55-65d63627592a
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
ms.openlocfilehash: acbb09c7777cf675ceb0f11ae84fb50a3b9deaa73910ca9e15280c3fb88c42cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119782088"
---
# <a name="searching-for-a-riff-chunk"></a>搜尋 RIFF 區塊

下列範例會使用 [**mmioDescend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend) 函式來搜尋格式為 "WAVE" 的 "RIFF" 區塊，以確認剛開啟的檔案是波形音訊檔案。


```C++
HMMIO    hmmio; 
MMCKINFO mmckinfoParent; 
MMCKINFO mmckinfoSubchunk; 
. 
. 
. 
// Locate a "RIFF" chunk with a "WAVE" form type to make 
// sure the file is a waveform-audio file. 
mmckinfoParent.fccType = mmioFOURCC('W', 'A', 'V', 'E'); 
if (mmioDescend(hmmio, (LPMMCKINFO) &mmckinfoParent, NULL, 
    MMIO_FINDRIFF)) 
    // The file is not a waveform-audio file. 
else 
    // The file is a waveform-audio file 

```



 

 
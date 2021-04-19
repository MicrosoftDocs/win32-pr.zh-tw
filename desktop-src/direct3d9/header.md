---
description: 直接讀取和寫入二進位標頭時，應使用下列定義。
ms.assetid: 19c36f94-8088-417d-867d-3a02912087dc
title: 標頭
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cfaa589382812cfd752d47cc8b95cda0139385b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106973542"
---
# <a name="header"></a>標頭

直接讀取和寫入二進位標頭時，應使用下列定義。

> [!Note]  
> 目前不支援壓縮的資料流程，因此此處不詳述。

 


```
#define XOFFILE_FORMAT_MAGIC \
  ((long)'x' + ((long)'o' << 8) + ((long)'f' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_VERSION \
  ((long)'0' + ((long)'3' << 8) + ((long)'0' << 16) + ((long)'2' << 24))

#define XOFFILE_FORMAT_BINARY \
  ((long)'b' + ((long)'i' << 8) + ((long)'n' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_TEXT   \
  ((long)'t' + ((long)'x' << 8) + ((long)'t' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_COMPRESSED \
  ((long)'c' + ((long)'m' << 8) + ((long)'p' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_FLOAT_BITS_32 \
  ((long)'0' + ((long)'0' << 8) + ((long)'3' << 16) + ((long)'2' << 24))

#define XOFFILE_FORMAT_FLOAT_BITS_64 \
  ((long)'0' + ((long)'0' << 8) + ((long)'6' << 16) + ((long)'4' << 24))
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[二進位編碼方式](binary-encoding.md)
</dt> </dl>

 

 




---
title: 呈現時間
description: 呈現時間
ms.assetid: 856e1783-85b4-4195-970f-3d7b5612672b
keywords:
- Windows Media Format SDK，簡報時間
- Advanced Systems Format (ASF) ，簡報時間
- ASF (Advanced Systems Format) ，簡報時間
- 展示時間
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bc88dbba93d1fc68905a4bfea92328a4ef600eb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301732"
---
# <a name="presentation-time"></a>呈現時間

呈現時間是從 ASF 檔案中第一個資料流程的第一個範例測量時間。 這項測量，以及此 SDK 的物件所使用的大部分其他時間測量值為 100-毫微秒單位。 簡報時間很重要，因為它們可讓檔案中的各種資料流程進行同步處理。 您必須為您傳遞至寫入器的每個輸入範例提供呈現時間。 ASF 檔案的 [資料] 區段中的每個資料物件都有相關聯的呈現時間。 讀取器取出的每個輸出範例也都有呈現時間。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**概念**](concepts.md)
</dt> <dt>

[**輸入、串流和輸出**](inputs-streams-and-outputs.md)
</dt> <dt>

[**媒體範例**](media-samples.md)
</dt> </dl>

 

 





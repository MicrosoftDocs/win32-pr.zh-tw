---
description: TSPI 使用的資料結構與 TAPI 結構中所定義的結構相同，但 TUISPICREATEDIALOGINSTANCEPARAMS 除外。
ms.assetid: 99d966ea-49b5-4a84-83a1-99dc8465c751
title: TSPI 結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e3468171bc160ca03ac9f5501a9eba7fd9221ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106985650"
---
# <a name="tspi-structures"></a>TSPI 結構

TSPI 使用的資料結構與 [TAPI 結構](./tapi-structures.md)中所定義的結構相同，但 [**TUISPICREATEDIALOGINSTANCEPARAMS**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams)除外。

如果是大部分較大型的資料結構，則填寫成員的責任會在服務提供者和 TAPI 之間劃分。 服務提供者必須保留出現在 TAPI 所擁有之成員的值。 服務提供者必須設定哪些成員的描述，而且必須保留這些成員的描述，會在參考該資料結構之函式的函數區段中提供。

針對每個結構，參考區段會列出下列專案：

-   結構的用途
-   值或欄位的描述
-   結構延伸的描述
-   使用結構的選擇性批註
-   其他函數、訊息、常數或結構的選擇性參考。

所有資料結構的記憶體（其表示由 TAPI 和服務提供者發佈並共用）都是由 TAPI 或使用 TAPI 的應用程式所配置。 TAPI 會將指標傳遞至 TSPI 函式，以傳回信息。 TSPI 會以所要求的資訊填入資料結構。 如果作業是非同步，則在非同步回復回呼表示成功之前，將無法使用該資訊。

> [!Note]  
> 某些結構包含大小和位移欄位，可在結構的變數部分中定義字串的位置和長度。 如果要求服務提供者加入字串，但沒有任何可用的字串，服務提供者必須以下列其中一種方式來指出這個狀況：
>
> -   將 [大小] 和 [位移] 欄位設定為0。
> -   將 [位移] 欄位設定為非零，但將大小設定為0。
> -   將 Offset 欄位設定為非零、將大小設定為1，並將位移的位元組設定為0。

 

 

 

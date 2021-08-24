---
description: Imagehlp.dll 函式大多是由程式設計工具、應用程式設定公用程式，以及需要存取 PE 映射中所含資料的其他程式所使用。
ms.assetid: 831d7bb2-bf01-4422-a940-173f9856a513
title: 關於 Imagehlp.dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4aee63eba22293fe1fb56cb6608110f4343a0c6bc26a4be597bfbd884cdf87cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815648"
---
# <a name="about-imagehlp"></a>關於 Imagehlp.dll

Imagehlp.dll 函式大多是由程式設計工具、應用程式設定公用程式，以及需要存取 PE 映射中所含資料的其他程式所使用。 所有 Imagehlp.dll 函數都是單一執行緒。 因此，從多個執行緒到此函式的呼叫可能會導致非預期的行為或記憶體損毀。 若要避免這種情況，您必須將多個執行緒的所有並行呼叫，同步處理至此函式。

下列主題描述 PE 映射以及 Imagehlp.dll 函數所提供的功能。

-   [PE 格式](pe-format.md)
-   [影像存取函式](image-access-functions.md)
-   [映射完整性函式](image-integrity-functions.md)
-   [影像修改函式](image-modification-functions.md)

 

 




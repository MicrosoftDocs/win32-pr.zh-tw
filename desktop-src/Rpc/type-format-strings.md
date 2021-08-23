---
title: 類型格式字串
description: 格式字元代表 NDR 引擎感興趣的物件。
ms.assetid: 71117082-07b0-4ba4-a920-09be8d8427ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42f4aa17494cbef0f3bcc232f89104e3502f94de4a3285a1da6cc0229af0fe26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011116"
---
# <a name="type-format-strings"></a>類型格式字串

格式字元代表 NDR 引擎感興趣的物件。 每個基本類型都有格式字元，適用于各種複雜類型，以及指標、封裝、對齊和其他其他物件的描述。 如果是複合類型，則會根據其效能屬性來辨識結構和陣列的數個類別。 每個類別的格式字串都會以識別特定格式字串的 FC 權杖開頭。 結構和陣列類別目錄的格式字元可能會在下表所示的開頭 FC 權杖名稱中共用修正。



| 格式字元 | 說明                                    |
|------------------|------------------------------------------------|
| C                | 表示類型中的一致性資訊。 |
| V                | 表示類型中的差異資訊。    |
| P                | 指出指標是類型的一部分。     |



 

例如，FC \_ CSTRUCT 和 fc \_ CARRAY 會分別識別符合標準的結構和一致的陣列描述項。

以下是具有特殊意義的格式字元。



| 格式字元 | 說明                                                                         |
|------------------|-------------------------------------------------------------------------------------|
| FC \_ PP           | 指出結構或陣列的指標描述區段開始。 |



 

下列主題會更詳細地描述 RPC NDR 類型格式字串：

-   [簡單類型](simple-types-tfs.md)
-   [指標](pointers-tfs.md)
-   [陣列](arrays-tfs.md)
-   [字串](strings-tfs.md)
-   [相互關聯描述元](correlation-descriptors-tfs.md)
-   [結構](structures-tfs.md)
-   [指標版面配置](pointer-layout-tfs.md)
-   [等位](unions-tfs.md)
-   [傳送 \_ as 和表示 \_ 為](transmit-as-and-represent-as-tfs.md)
-   [使用者封送處理](user-marshal-tfs.md)

 

 





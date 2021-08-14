---
title: 強型別
description: C 是弱型別語言，也就是，編譯器允許在不同類型的變數之間進行指派和比較等作業。
ms.assetid: 5f52adcc-22b9-4b4f-b921-5996d278b10e
keywords:
- 遠端程序呼叫 RPC，描述，資料類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae47746119f4c1b22bc066075ed484ef836fa6a68ee103e06975018a6ae49012
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118924844"
---
# <a name="strong-typing"></a>強型別

C 是弱型別語言，也就是，編譯器允許在不同類型的變數之間進行指派和比較等作業。 例如，C 允許將變數的值轉換成另一種類型。 在相同的運算式中使用不同類型變數的能力，可提升彈性和效率。

強型別語言會對不同類型的變數之間的作業強加限制。 在這些情況下，編譯器會發出錯誤，導致作業無法運作。 這些有關資料類型的嚴格指導方針是設計來避免可能發生的錯誤。

使用弱式類型語言（例如 C）進行遠端程序呼叫的困難之處在于，分散式應用程式可以在具有不同 C 編譯器和不同架構的數部不同電腦上執行。 當應用程式只在一部電腦上執行時，您不需要擔心內部資料格式，因為資料是以一致的方式處理。 不過，在分散式運算環境中，不同的電腦可以針對其基底資料類型使用不同的定義。 例如，某些電腦會定義 **int** 類型，因此其內部標記法為16位，而其他電腦則使用32位。 一種電腦架構，稱為「位元組由小到小」，會將最少的資料位元組指派給最小的記憶體位址，最重要的位元組則指派到最高的位址。 另一種架構（稱為「大 endian」）會將最不重要的位元組指派給與該資料相關聯的最高記憶體位址。

遠端程序呼叫需要嚴格控制參數類型。 為了處理透過網路的資料傳輸和轉換，MIDL 嚴格強制執行透過網路傳送之資料的類型限制。 基於這個理由，MIDL 包含一組定義完善的 [基底類型](base-types.md)。 MIDL 強制執行強型別，方法是強制使用可明確定義資料大小和類型的關鍵字。 強式類型的最明顯效果是 MIDL 不允許類型為 **void \*** 的變數。

在下列主題中，本節討論會強制執行強式資料類型的 MIDL 語言功能：

-   [基底類型](base-types.md)
-   [帶正負號和不帶正負號類型](signed-and-unsigned-types.md)
-   [寬字元類型](wide-character-types.md)
-   [結構](structures.md)
-   [等位](unions.md)
-   [列舉類型](enumerated-types.md)
-   [陣列](arrays.md)
-   [函數屬性](function-attributes.md)
-   [欄位屬性](field-attributes.md)
-   [三種指標類型](three-pointer-types.md)
-   [類型屬性](type-attributes.md)

 

 





---
title: " (功能表和其他資源的預處理器指示詞) "
description: 您可以視需要在資源腳本中使用下表所述的指示詞。 它們指示 RC 執行動作或指派值給名稱。
ms.assetid: 162f946e-54d8-4e23-9aa7-8e91eda4ee68
keywords:
- 資源編譯器，預處理器指示詞
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43e8c32f1d32dab784d5d947fdf64b7018451a5a
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104317072"
---
# <a name="preprocessor-directives-menus-and-other-resources"></a> (功能表和其他資源的預處理器指示詞) 

您可以視需要在資源腳本中使用下表所述的指示詞。 它們指示 RC 執行動作或指派值給名稱。



| 指示詞                     | Description                                                           |
|-------------------------------|-----------------------------------------------------------------------|
| [**\#定義**](-define.md)   | 藉由將指定的值指派給指定的名稱，以定義指定的名稱。               |
| [**\#elif**](-elif.md)       | 標記條件式編譯區塊的選擇性子句。          |
| [**\#else**](-else.md)       | 標記條件式編譯區塊的最後一個選擇性子句。    |
| [**\#endif**](-endif.md)     | 標記條件式編譯區塊的結尾。                     |
| [**\#如果**](-if.md)           | 如果指定的運算式為 true，則會有條件地編譯腳本。  |
| [**\#ifdef**](-ifdef.md)     | 如果已定義指定的名稱，則會有條件地編譯腳本。     |
| [**\#ifndef**](-ifndef.md)   | 如果未定義指定的名稱，則會有條件地編譯腳本。 |
| [**\#包括**](-include.md) | 將檔案的內容複寫到資源定義檔中。      |
| [**\#undef**](-undef.md)     | 移除指定之名稱的定義。                         |



 

若要定義資源識別碼的符號，請使用 **\# define** 指示詞在標頭檔中定義符號。 在資源腳本和您的應用程式原始程式碼中包含此標頭。 同樣地，您可以在資源腳本中包含 Windows .h 來定義資源屬性和樣式的值。

RC 以特殊方式將檔案與 .c 和 .h 延伸。 它會假設具有其中一個擴充功能的檔案不包含資源。 如果檔案的副檔名為 .c 或 .h，RC 會忽略檔案中的所有行（預處理器指示詞除外）。 因此，若要在另一個資源腳本中包含包含資源的檔案，請將檔案包含在 .c 或 .h 以外的副檔名。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Pragma 指示詞](pragma-directives.md)
</dt> </dl>

 

 





---
title: 關於資源檔
description: 說明如何將資源包含在以 RC Windows 為基礎的應用程式中。
ms.assetid: af7c7aed-5d28-40ac-ad00-da0986fd89c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24f351592c57cb628204ad6528a48bfa1a10507f5e7aad90a524ea2f6034f304
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034466"
---
# <a name="about-resource-files"></a>關於資源檔

若要在具有 RC 的 Windows 應用程式中包含資源，請執行下列動作：

1.  為您的游標、圖示、點陣圖、對話方塊和字型建立個別檔案。
2.  建立資源定義腳本 ( .rc 檔) ，以描述您的應用程式所使用的資源。
3.  使用 RC 編譯腳本。 如需詳細資訊，請參閱 [使用 rc (Rc 命令列) ](using-rc-the-rc-command-line-.md)。
4.  將已編譯的資源 ( .res) 檔連結至應用程式的可執行檔。

資源檔是副檔名為 .rc 的文字檔。 檔案可以使用單一位元組、雙位元組或 Unicode 字元。 RC 預處理器的語法和語義類似于 Microsoft C/c + + 編譯器。 不過，RC 支援在腳本中使用預處理器指示詞、定義和 pragma 的子集。

腳本檔案會定義資源。 針對存在於個別檔案中的資源（例如圖示或游標），腳本會指定資源和包含它的檔案。 對於某些資源（例如功能表），該資源的整個定義都會存在於腳本中。

下列主題描述腳本檔案可以包含的資訊：

-   [批註](comments.md)，也就是 RC 要忽略的附注。
-   [預先定義的宏](predefined-macros.md)，不採用任何引數，也無法重新定義。
-   [預處理器](preprocessor-directives.md)指示詞，指示 RC 先對腳本執行動作，再進行編譯。
-   [預處理器運算子](preprocessor-operators.md)，用於 **\# 定義** 指示詞。
-   [Pragma 指示詞](pragma-directives.md)
-   [資源定義語句](resource-definition-statements.md)，其名稱和描述資源。

 

 





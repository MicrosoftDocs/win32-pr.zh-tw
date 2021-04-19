---
description: Tablet PC 包含的技術可辨識最常用於手寫形式的筆墨輸入。
ms.assetid: 614971a8-2b56-40d4-abb6-aba5ded01883
title: 關於手寫辨識
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ff794f018cd0019a5013bacf8b9edfbe45018d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985147"
---
# <a name="about-handwriting-recognition"></a>關於手寫辨識

Tablet PC 包含的技術可辨識最常用於手寫形式的筆墨輸入。 提供辨識的軟體模組稱為辨識器。 辨識器會辨識一種語言、一組相關的語言，或相關物件（例如，音樂筆記、系統手勢或幾何圖形）的類別。 您可以動態地將辨識器新增至 ink 服務系統。

## <a name="recognition-steps"></a>辨識步驟

辨識會透過使用辨識器內容來處理。 辨識包含四個基本步驟：

1.  設定辨識條件約束的依據：
    -   選取 (幾何條件約束) 的辨識器和輸入模式。
    -   設定語言條件約束。 例如，您可以將輸入限制為英數位元，也可以傳遞架構來協助辨識器。
2.  將筆墨傳送到辨識器。
3.  處理輸入 (辨識) 。
4.  傳回識別的結果。

步驟2和3可能會在迴圈中重複，或在嘗試辨識之前，將所有筆墨筆劃新增至筆墨。

## <a name="samples-and-related-topics"></a>範例和相關主題

[Advanced 辨識範例](advanced-recognition-sample.md) 示範如何搭配使用辨識器與 [**ink**](inkdisp-class.md) 物件來執行筆跡辨識。

辨識[器 Dll 範例範本](recognizer-dll-sample-template.md)包含用來建立辨識器 dll 的範本。 範本包含用來註冊和取消註冊伺服器的功能，以及主要辨識器函式的骨架。

下列各節說明 Tablet PC 辨識技術背後的基本概念。 如需建立自訂辨識器的詳細資訊，請參閱 [建立辨識器](creating-a-recognizer.md)。

-   [文字辨識器](text-recognizers.md)
-   [物件辨識器](object-recognizers.md)
-   [使用辨識器集合](using-the-recognizers-collection.md)
-   [辨識器內容](recognizer-context.md)
-   [辨識區段](recognition-segments.md)
-   [角度文字的辨識](recognition-of-angled-text.md)
-   [辨識器筆觸重新排序支援](recognizer-stroke-reordering-support.md)
-   [字典和 Factoids](dictionaries-and-factoids.md)
-   [關於辨識的信賴財產 \[\]](confidence-property--about-recognition.md)
-   [替代項目](alternates.md)
-   [筆跡區段和替代項](ink-segments-and-alternates.md)

 

 




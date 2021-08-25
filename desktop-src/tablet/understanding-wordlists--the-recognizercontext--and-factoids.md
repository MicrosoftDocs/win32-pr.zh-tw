---
description: 所有應用程式字典都是使用單詞表物件來執行。
ms.assetid: 805788ec-1672-462a-b188-c680f56c2641
title: 瞭解單字清單、辨識器內容和 Factoids
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e60fbfc7a3a3099a1146307637d20e777cca416789a61f5dd034f9d86911f1a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119842808"
---
# <a name="understanding-word-lists-recognizer-context-and-factoids"></a>瞭解單字清單、辨識器內容和 Factoids

所有應用程式字典都是使用 [**單詞表**](inkwordlist-class.md) 物件來執行。 [**RecognizerCoNtext**](inkrecognizercontext-class.md)物件會透過該物件的 [**單詞表**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist)屬性來管理辨識。 **RecognizerCoNtext** 物件會將單字清單傳遞給辨識器。 您可以藉由設定 **RecognizerCoNtext** 物件的 [**單詞表**] 屬性，在應用程式中的任何 **RecognizerCoNtext** 啟用應用程式字典。 若要讓 word 清單可供整個應用程式使用，您必須在應用程式中設定每個 **RecognizerCoNtext** 物件的 [**單詞表**] 屬性。

在辨識器層級，系統字典以外的所有字典都會實作為字組清單。 不過，辨識器一次只能有一個作用中的字組清單。 這表示您不能同時使用應用程式字典和使用者字典。 另一方面，除非設定了可關閉系統字典的模擬程式，否則系統字典一律可供使用。

使用者字典是使用者已新增至其 Tablet PC 的單字清單。 如果未設定 [**RecognizerCoNtext**](inkrecognizercontext-class.md)的 [**單詞表**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist)屬性， **RecognizerCoNtext** 會將使用者字典以單字清單傳遞給辨識器。 但是，如果已設定 **RecognizerCoNtext** 物件的 [**單詞表**] 屬性，則會將此字組傳遞給辨識器，而不是使用者字典。

> [!Note]  
> 在您設定 [[**單詞表**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist)] 屬性之前， [**RecognizerCoNtext**](inkrecognizercontext-class.md)物件的 [[**筆劃**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_strokes)] 屬性必須是空的。 如果 **筆觸** 屬性不是空的，則會擲回例外狀況。 在將單字指派給 **RecognizerCoNtext** 物件之後，不應該將它們新增至字組清單。

 

在 [**RecognizerCoNtext**](inkrecognizercontext-class.md) 物件上設定模擬程式也會影響辨識器使用應用程式字典的方式。 影響字典行為的 factoids 如下：

-   **單詞表**
-   **SystemDictionary**
-   **None**

目前，應用程式字典最有用的模擬程式是 **單詞表** 模擬。 **單詞表** 模擬會將辨識器偏移，使其只傳回單字清單中找到的單字。 除了字組清單之外，此模擬程式會關閉其他所有字典。 如果設定了 **單詞表** 模擬程式，且在辨識器內容中未指定任何單字清單，則會使用使用者字典作為字組清單。

例如，如果您要設計飛機元件應用程式，且其欄位接受其中十個特製化元件的其中一個，您可以建立只包含這些元件名稱的單字清單。 設定欄位的 **單詞表** 標記，可大幅改善該欄位中所輸入文字的辨識。 辨識器不需要在系統字典中的單字和單字清單中的單字之間進行選擇。

**SystemDictionary** 模擬模擬僅啟用系統字典。 **None** 模擬會停用所有詞典。 這兩個 factoids 可用來提高某些實例的辨識精確度。 不過，因為它們會停用應用程式字典，很少會與應用程式字典搭配使用。

如需 factoids 如何影響辨識的詳細資訊，請參閱 [使用內容改善精確度](using-context-to-improve-accuracy.md)。

如需 **SystemDictionary** 和 **None** factoids 的詳細資訊，請參閱 [第1版所支援的 factoids](supported-factoids-from-version-1.md)。

 

 




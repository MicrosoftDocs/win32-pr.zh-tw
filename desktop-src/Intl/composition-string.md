---
description: 組合字元串是撰寫視窗中的目前文字。
ms.assetid: ab226567-f68d-4fa4-9ead-e9bfabde927e
title: 組合字元串
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e5cb63163ca9a8076edc4d01053e4baeffc619c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944371"
---
# <a name="composition-string"></a>組合字元串

組合字元串是撰寫視窗中的目前文字。 這是 IME 轉換成最後字元的文字。 每個組合字元串都包含一個或多個「子句」。 子句是 IME 可以轉換成最後一個字元的最小字元組合。 為了取得並設定組合字元串，應用程式會分別呼叫 [**ImmGetCompositionString**](/windows/desktop/api/Imm/nf-imm-immgetcompositionstringa) 和 [**ImmSetCompositionString**](/windows/desktop/api/Imm/nf-imm-immsetcompositionstringa) 函數。

當使用者在撰寫視窗中輸入文字時，IME 會追蹤組合字元串的狀態。 此狀態包括屬性資訊、子句資訊、輸入資訊和游標位置。 應用程式可以使用 [**ImmGetCompositionString**](/windows/desktop/api/Imm/nf-imm-immgetcompositionstringa) 函數來取得撰寫狀態。

屬性資訊會轉譯成8位值的陣列，這些值會指定組合字元串中的字元狀態。 一個子句的所有字元都必須具有相同的屬性。 陣列中的每個位元組都包含一個值，其中每個位元組都包含一個位元組，而字串中任何雙位元組字元的第二個位元組。 針對陣列中的每個值，位0至3可以是下列值的其中一個組合。



| 值                      | 意義                                                                                                   |
|----------------------------|-----------------------------------------------------------------------------------------------------------|
| ATTR \_ 輸入                | 使用者輸入的字元。 輸入法尚未轉換此字元。                           |
| ATTR \_ 輸入 \_ 錯誤         | IME 無法轉換的錯誤字元。 例如，輸入法不能將部分子音放在一起。 |
| 已 \_ 轉換 ATTR 目標 \_    | 使用者選取的字元，然後由 IME 進行轉換。                                             |
| 已 \_ 轉換 ATTR            | IME 已轉換的字元。                                                             |
| ATTR \_ 目標 \_ NOTCONVERTED | 要轉換的字元。 使用者已選取此字元，但輸入法尚未轉換。     |
| ATTR \_ FIXEDCONVERTED       | 輸入法將不再轉換的字元。                                                           |



 

所有其他值都是保留的。 在日文中，任何具有 ATTR \_ 輸入屬性的未轉換字元都是平假名、片假名或英數位元。 在韓文中，這個屬性代表 IME 尚未轉換的韓文字元。 在繁體中文和簡體中文中，每個 IME 都可以限制其在某個範圍內的字元。

組合字元串狀態中包含的子句資訊是32位值的陣列，可指定子句在組合字元串中的位置。 陣列包含每個子句的一個值，以及指定完整字串長度的最後一個值。 陣列中的每個值都會指定從字串開頭到子句的位移（以位元組為單位）。 第一個值一律為0，因為第一個子句一律會從字串的開頭開始。 例如，如果字串有兩個子句，子句資訊會有三個值：第一個值是0，第二個值是第二個子句的位移，而第三個值是字串的長度。 若為 Unicode，子句的位置會以 Unicode 字元計算，而字串的長度則為 Unicode 字元的大小。

組合字元串狀態中包含的輸入資訊是以 null 結束的字元字串，代表使用者在鍵盤上輸入的字元。

組合字元串狀態中包含的資料指標位置是一個值，表示游標相對於組合字元串中字元的位置。 值是從字串開頭算起的位移（以位元組為單位）。 如果這個值為0，則資料指標緊接在字串中的第一個字元之前。 如果值等於字串的長度，則資料指標緊接在最後一個字元之後。 如果值為1，表示資料指標不存在。 若為 Unicode，則會以 Unicode 字元來測量位置和長度。

您的應用程式可以使用 [**ImmSetCompositionString**](/windows/desktop/api/Imm/nf-imm-immsetcompositionstringa) 函式，設定組合字元串或組合狀態的元素。 為了確保撰寫視窗根據這些變更來更新其外觀，此函式可讓應用程式將通知訊息傳送至視窗。 設定組合狀態專案組合的應用程式通常會停用此函式的所有通知（除了最後一次呼叫此函式），如此一來，撰寫視窗只會產生一個通知訊息。

最後，編輯控制項支援兩個訊息來變更輸入法的組合字元串處理。 如需詳細資訊，請參閱 [**em \_ GETIMESTATUS**](../controls/em-getimestatus.md) 和 [**em \_ SETIMESTATUS**](../controls/em-setimestatus.md)。 如需編輯控制項的詳細資訊，請參閱 [編輯控制項](../controls/edit-controls.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於輸入方法管理員](about-input-method-manager.md)
</dt> </dl>

 

 

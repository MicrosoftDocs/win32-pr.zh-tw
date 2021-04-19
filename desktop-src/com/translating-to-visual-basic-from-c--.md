---
title: 從 c + + 翻譯為 Visual Basic
description: 從 c + + 翻譯為 Visual Basic
ms.assetid: fce7ea25-cb24-4cc4-8f36-0e8aed2f3ada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffba519cbdb0305fe3a2eae4cc8e658fdde1eac3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968645"
---
# <a name="translating-to-visual-basic-from-c"></a>從 c + + 翻譯為 Visual Basic

使用 c + + 程式設計語言，開發人員可以直接存取儲存特定變數的記憶體。 記憶體指標可提供此直接存取。 在 Visual Basic 中，系統會為您處理指標。 例如，在 c + + 中宣告為 **int** 之指標的參數，相當於 Visual Basic 中宣告為 **ByRef** **整數** 的參數。

在 Visual Basic 中宣告 **為字串** 的參數會宣告為 c + + 中的 **BSTR** 指標。 在 c + + 中將字串指標設定為 **Null** ，相當於將字串設定為 Visual Basic 中的 **vbNullString** 常數。 傳入零長度的字串 ( "" ) 至設計用來接收 **Null** 的函式無效，因為這樣會將指標傳遞至長度為零的字串，而不是零指標。

C + + 支援在舊版 Visual Basic 中沒有對等的資料容器，亦即結構和等位。 基於這個理由，COM 物件通常會包裝通常儲存在物件類別結構和等位中的資訊。 不過，某些 COM 物件可能包含結構，而導致物件的部分方法或功能無法 Visual Basic 存取。

某些 c + + 資料類型在 Visual Basic 中不受支援，例如不帶正負號的類型和 **HWND** 類型。 Visual Basic 不提供接受或傳回這些資料類型的方法。

Visual Basic 使用 Automation 相容的資料類型作為其內部資料類型。 因此，與自動化相容的 c + + 資料類型也會與 Visual Basic 相容。 非自動化相容的資料類型可能無法轉換成 Visual Basic。

下表列出 Visual Basic 所支援的資料類型及其 **VARTYPE** 。 **VARTYPE** 是列出 Automation variant 類型的列舉。



| Visual Basic 資料類型  | VARTYPE 相等                |
|-------------------------|-----------------------------------|
| **整數**<br/>  | 16位、帶正負號、VT \_ I2<br/> |
| **Long**<br/>     | 32位、帶正負號、VT \_ I4<br/> |
| **日期**<br/>     | VT \_ 日期<br/>               |
| **貨幣**<br/> | VT \_ CY<br/>                 |
| **Object**<br/>   | \*VT \_ 分派<br/>         |
| **String**<br/>   | VT \_ BSTR<br/>               |
| **布林值**<br/>  | VT \_ BOOL<br/>               |
| **貨幣**<br/> | VT \_ DECIMAL<br/>            |
| **Single**<br/>   | VT \_ R4<br/>                 |
| **Double**<br/>   | VT \_ R8<br/>                 |
| **十進位**<br/>  | VT \_ DECIMAL<br/>            |
| **位元組**<br/>     | VT \_ DECIMAL<br/>            |
| **變異**<br/>  | VT \_ 變異<br/>            |



 

除非以關鍵字 **ByVal** 標記，否則 Visual Basic 中的所有參數會以傳址方式傳遞 (做為指標) ，而不是以傳值方式傳遞。

C + + 和 Visual Basic 在其代表屬性的方式上稍有不同。 在 c + + 中，屬性是以一組存取子函式來表示，其中一個設定屬性值，另一個則會抓取屬性值。 在 Visual Basic 中，屬性會以單一專案的形式表示，可用於抓取或設定屬性值。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[翻譯為 Visual Basic](translating-to-visual-basic.md)
</dt> </dl>

 

 






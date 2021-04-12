---
title: 語法差異
description: 當您在程式設計語言之間移動時，最明顯的變更是語法中的變更。
ms.assetid: 179efb69-3794-4a06-b770-2b3dc8409172
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d3a9c2123d8b94f9fc6fe79d4ab48188830c7a1
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104463761"
---
# <a name="syntax-differences"></a>語法差異

當您在程式設計語言之間移動時，最明顯的變更是語法中的變更。

請考慮 EnhEvents 物件的 Add 方法，因為它是以三種不同的語言所宣告的。

``` syntax
object.Add(Time As Double, Name As String) As Variant

HRESULT Add(
  double Time, 
  BSTR Name, 
  VARIANT* pVal
);
 
public com.ms.com.Variant Add( 
  double Time, 
  java.lang.String Name
);
 
```

雖然每種語言的語法都以不同的方式來表示方法，但功能是相同的。 在每一種語言中，Add 方法都採用參數 *Time* 和 *Name* ，並傳回 EnhEvent 物件。 在 c + + 範例中，方法會使用第三個輸出參數 *pVal* 傳回物件。

一般而言，COM 物件的功能在程式設計語言中是相同的。 基於這個原因，即使物件所記錄的程式語言與您所使用的程式設計語言不同，COM 物件的檔還是很有用。 物件的功能、參數和傳回值的描述，有少數例外狀況，適用于所有語言。

如需如何將 COM 物件的語法轉換成另一種程式設計語言的詳細資訊，請參閱轉譯 [程式設計語言的 Com 物件語法](translating-com-object-syntax-for-programming-languages.md)。

指令碼語言 JavaScript、JScript 和 VBScript 之間的語法差異，比上述程式設計語言之間的語法差異更不明顯。 例如，假設正方形函式是在這三種指令碼語言中的每一種中執行：

``` syntax
Function square(x)
  square = x*x
End Function
 
function square(x){ return x*x; }
 
function square(x){ return x*x; }
 
```

請注意，與程式設計語言不同的指令碼語言是弱式型別。 換句話說，當您宣告函式時，不需要指定參數或傳回值的資料類型。 相反地，變數會自動轉換成適當的資料類型。 在 VBScript 的案例中，所有變數的資料類型都相同，也就是 **Variant**。

平方的 JavaScript 和 JScript 語法是相同的。 JScript 大多與 JavaScript 相容。 但是，JScript 包含一些 JavaScript 目前不支援的物件，例如 **ActiveXObject**、 **列舉** 值、 **Error**、 **Global** 和 **VBArray**。 如需這些物件的詳細資訊，請參閱 [JScript 語言參考](/previous-versions/visualstudio/visual-studio-2010/ye921ye4(v=vs.100))。

在表面上，JavaScript 和 JScript 語法類似 JAVA 語法。 這種相似性只有表面。 JAVA 語言是從 JavaScript 和 JScript 獨立開發而成，而且與兩者無關。

另一方面，VBScript 是 Visual Basic 程式設計語言的子集。 因此，VBScript 語法是 Visual Basic 語法的子集，而且通常可透過 Visual Basic 語法來交換。

如需在指令碼語言中使用 COM 物件的詳細資訊，請參閱 [使用 Com 物件編寫腳本](scripting-with-com-objects.md)。

 

 
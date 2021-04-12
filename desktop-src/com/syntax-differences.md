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
# <a name="syntax-differences"></a><span data-ttu-id="4bf3b-103">語法差異</span><span class="sxs-lookup"><span data-stu-id="4bf3b-103">Syntax Differences</span></span>

<span data-ttu-id="4bf3b-104">當您在程式設計語言之間移動時，最明顯的變更是語法中的變更。</span><span class="sxs-lookup"><span data-stu-id="4bf3b-104">The most apparent change as you move between programming languages is the change in syntax.</span></span>

<span data-ttu-id="4bf3b-105">請考慮 EnhEvents 物件的 Add 方法，因為它是以三種不同的語言所宣告的。</span><span class="sxs-lookup"><span data-stu-id="4bf3b-105">Consider the EnhEvents object's Add method, shown as it is declared in three different languages.</span></span>

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

<span data-ttu-id="4bf3b-106">雖然每種語言的語法都以不同的方式來表示方法，但功能是相同的。</span><span class="sxs-lookup"><span data-stu-id="4bf3b-106">Although the syntax of each language expresses the method differently, the functionality is the same.</span></span> <span data-ttu-id="4bf3b-107">在每一種語言中，Add 方法都採用參數 *Time* 和 *Name* ，並傳回 EnhEvent 物件。</span><span class="sxs-lookup"><span data-stu-id="4bf3b-107">In each language, the Add method takes the parameters *Time* and *Name* and returns an EnhEvent object.</span></span> <span data-ttu-id="4bf3b-108">在 c + + 範例中，方法會使用第三個輸出參數 *pVal* 傳回物件。</span><span class="sxs-lookup"><span data-stu-id="4bf3b-108">In the C++ example, the method returns the object by using a third, output parameter, *pVal*.</span></span>

<span data-ttu-id="4bf3b-109">一般而言，COM 物件的功能在程式設計語言中是相同的。</span><span class="sxs-lookup"><span data-stu-id="4bf3b-109">Typically, the functionality of a COM object is the same across programming languages.</span></span> <span data-ttu-id="4bf3b-110">基於這個原因，即使物件所記錄的程式語言與您所使用的程式設計語言不同，COM 物件的檔還是很有用。</span><span class="sxs-lookup"><span data-stu-id="4bf3b-110">Because of this, documentation for a COM object is useful even if the object is documented in another programming language than the one you are using.</span></span> <span data-ttu-id="4bf3b-111">物件的功能、參數和傳回值的描述，有少數例外狀況，適用于所有語言。</span><span class="sxs-lookup"><span data-stu-id="4bf3b-111">The descriptions of the object's functionality, parameters, and return values are, with few exceptions, valid for all languages.</span></span>

<span data-ttu-id="4bf3b-112">如需如何將 COM 物件的語法轉換成另一種程式設計語言的詳細資訊，請參閱轉譯 [程式設計語言的 Com 物件語法](translating-com-object-syntax-for-programming-languages.md)。</span><span class="sxs-lookup"><span data-stu-id="4bf3b-112">For information about how to convert the syntax of a COM object to another programming language, see [Translating COM Object Syntax for Programming Languages](translating-com-object-syntax-for-programming-languages.md).</span></span>

<span data-ttu-id="4bf3b-113">指令碼語言 JavaScript、JScript 和 VBScript 之間的語法差異，比上述程式設計語言之間的語法差異更不明顯。</span><span class="sxs-lookup"><span data-stu-id="4bf3b-113">The syntax differences among the scripting languages JavaScript, JScript, and VBScript are less pronounced than the syntax differences among the programming languages shown preceding.</span></span> <span data-ttu-id="4bf3b-114">例如，假設正方形函式是在這三種指令碼語言中的每一種中執行：</span><span class="sxs-lookup"><span data-stu-id="4bf3b-114">For example, consider the square function as it is implemented in each of these three scripting languages:</span></span>

``` syntax
Function square(x)
  square = x*x
End Function
 
function square(x){ return x*x; }
 
function square(x){ return x*x; }
 
```

<span data-ttu-id="4bf3b-115">請注意，與程式設計語言不同的指令碼語言是弱式型別。</span><span class="sxs-lookup"><span data-stu-id="4bf3b-115">Notice that the scripting languages, unlike the programming languages, are weakly typed.</span></span> <span data-ttu-id="4bf3b-116">換句話說，當您宣告函式時，不需要指定參數或傳回值的資料類型。</span><span class="sxs-lookup"><span data-stu-id="4bf3b-116">In other words, you do not have to specify the data type of a parameter or return value when you declare a function.</span></span> <span data-ttu-id="4bf3b-117">相反地，變數會自動轉換成適當的資料類型。</span><span class="sxs-lookup"><span data-stu-id="4bf3b-117">Instead, the variables are automatically cast to the appropriate data type.</span></span> <span data-ttu-id="4bf3b-118">在 VBScript 的案例中，所有變數的資料類型都相同，也就是 **Variant**。</span><span class="sxs-lookup"><span data-stu-id="4bf3b-118">In the case of VBScript, all variables are of the same data type, **Variant**.</span></span>

<span data-ttu-id="4bf3b-119">平方的 JavaScript 和 JScript 語法是相同的。</span><span class="sxs-lookup"><span data-stu-id="4bf3b-119">The JavaScript and JScript syntax for square is the same.</span></span> <span data-ttu-id="4bf3b-120">JScript 大多與 JavaScript 相容。</span><span class="sxs-lookup"><span data-stu-id="4bf3b-120">JScript is largely compatible with JavaScript.</span></span> <span data-ttu-id="4bf3b-121">但是，JScript 包含一些 JavaScript 目前不支援的物件，例如 **ActiveXObject**、 **列舉** 值、 **Error**、 **Global** 和 **VBArray**。</span><span class="sxs-lookup"><span data-stu-id="4bf3b-121">However, JScript includes some objects not currently supported by JavaScript, such as **ActiveXObject**, **Enumerator**, **Error**, **Global**, and **VBArray**.</span></span> <span data-ttu-id="4bf3b-122">如需這些物件的詳細資訊，請參閱 [JScript 語言參考](/previous-versions/visualstudio/visual-studio-2010/ye921ye4(v=vs.100))。</span><span class="sxs-lookup"><span data-stu-id="4bf3b-122">For more information about these objects, see the [JScript Language Reference](/previous-versions/visualstudio/visual-studio-2010/ye921ye4(v=vs.100)).</span></span>

<span data-ttu-id="4bf3b-123">在表面上，JavaScript 和 JScript 語法類似 JAVA 語法。</span><span class="sxs-lookup"><span data-stu-id="4bf3b-123">On the surface, JavaScript and JScript syntax resembles Java syntax.</span></span> <span data-ttu-id="4bf3b-124">這種相似性只有表面。</span><span class="sxs-lookup"><span data-stu-id="4bf3b-124">This similarity is only superficial.</span></span> <span data-ttu-id="4bf3b-125">JAVA 語言是從 JavaScript 和 JScript 獨立開發而成，而且與兩者無關。</span><span class="sxs-lookup"><span data-stu-id="4bf3b-125">The Java language was developed independently from both JavaScript and JScript and is not related to either.</span></span>

<span data-ttu-id="4bf3b-126">另一方面，VBScript 是 Visual Basic 程式設計語言的子集。</span><span class="sxs-lookup"><span data-stu-id="4bf3b-126">VBScript, on the other hand, is a subset of the Visual Basic programming language.</span></span> <span data-ttu-id="4bf3b-127">因此，VBScript 語法是 Visual Basic 語法的子集，而且通常可透過 Visual Basic 語法來交換。</span><span class="sxs-lookup"><span data-stu-id="4bf3b-127">Because of this, VBScript syntax is a subset of Visual Basic syntax and is often interchangeable with Visual Basic syntax.</span></span>

<span data-ttu-id="4bf3b-128">如需在指令碼語言中使用 COM 物件的詳細資訊，請參閱 [使用 Com 物件編寫腳本](scripting-with-com-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="4bf3b-128">For information on using COM objects in scripting languages, see [Scripting with COM Objects](scripting-with-com-objects.md).</span></span>

 

 
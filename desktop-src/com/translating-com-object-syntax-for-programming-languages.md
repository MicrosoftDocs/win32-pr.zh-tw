---
title: 轉換程式設計語言的 COM 物件語法
description: 轉換程式設計語言的 COM 物件語法
ms.assetid: 021e0085-c720-401e-9637-76580e67b307
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf9d1ec65e5b4ff8f3b61106a4b7a8c9ee3134b3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839883"
---
# <a name="translating-com-object-syntax-for-programming-languages"></a><span data-ttu-id="c30a5-103">轉換程式設計語言的 COM 物件語法</span><span class="sxs-lookup"><span data-stu-id="c30a5-103">Translating COM Object Syntax for Programming Languages</span></span>

<span data-ttu-id="c30a5-104">若要從以程式設計語言撰寫的應用程式呼叫 COM 物件，而非用來寫入 COM 物件的應用程式，您必須先將物件的語法轉譯為程式設計語言。</span><span class="sxs-lookup"><span data-stu-id="c30a5-104">To call a COM object from an application written in a programming language other than the one used to write the COM object, you must first translate the object's syntax to your programming language.</span></span> <span data-ttu-id="c30a5-105">您可以使用下列步驟來完成此動作：</span><span class="sxs-lookup"><span data-stu-id="c30a5-105">This can be done using the following steps:</span></span>

1.  <span data-ttu-id="c30a5-106">以程式設計語言的語法來查看 COM 物件的類型程式庫。</span><span class="sxs-lookup"><span data-stu-id="c30a5-106">View the COM object's type library in your programming language's syntax.</span></span> <span data-ttu-id="c30a5-107">這樣做會以您所使用的語言語法，提供物件的類別、介面、方法、屬性和事件的描述。</span><span class="sxs-lookup"><span data-stu-id="c30a5-107">Doing this provides you with descriptions of the object's classes, interfaces, methods, properties and events in the language syntax you use.</span></span>

    <span data-ttu-id="c30a5-108">Microsoft 開發人員產品提供數個工具，可協助您流覽和轉換型別程式庫。</span><span class="sxs-lookup"><span data-stu-id="c30a5-108">Microsoft developer products provide several tools to assist you in viewing and converting type libraries.</span></span> <span data-ttu-id="c30a5-109">如需詳細資訊，請參閱 [類型程式庫檢視器和轉換工具](type-library-viewers-and-conversion-tools.md) ，以及 [開發人員工具使用類型程式庫的方式](how-developer-tools-use-type-libraries.md)。</span><span class="sxs-lookup"><span data-stu-id="c30a5-109">For more information, see [Type Library Viewers and Conversion Tools](type-library-viewers-and-conversion-tools.md) and [How Developer Tools Use Type Libraries](how-developer-tools-use-type-libraries.md).</span></span>

    <span data-ttu-id="c30a5-110">一旦您可以用慣用的程式設計語言來查看物件的類型程式庫，您就可以在物件的檔中比較其語法。</span><span class="sxs-lookup"><span data-stu-id="c30a5-110">Once you can view the object's type library in your preferred programming language, you can compare its syntax to that in the documentation for the object.</span></span> <span data-ttu-id="c30a5-111">如果物件是以您所使用的程式設計語言所記載，則資料類型和語法可能會不同，但參數、傳回值和物件功能的描述應該相同。</span><span class="sxs-lookup"><span data-stu-id="c30a5-111">If the object is documented in a programming language other than the one you are using, the data types and syntax may differ, but descriptions of parameters, return values, and the object's functionality should be the same.</span></span>

2.  <span data-ttu-id="c30a5-112">將翻譯成您的程式設計語言的任何特殊考慮納入考慮。</span><span class="sxs-lookup"><span data-stu-id="c30a5-112">Take into account any special considerations for translating to your programming language.</span></span>

    <span data-ttu-id="c30a5-113">因為每種程式設計語言都定義了在其他語言中可能沒有對等的概念，所以某些物件的功能可能會以不同的方式運作，或完全無法使用。</span><span class="sxs-lookup"><span data-stu-id="c30a5-113">Because each programming language defines concepts that may not have an equivalent in other languages, some of an object's functionality may work differently in another language, or not be available at all.</span></span> <span data-ttu-id="c30a5-114">例如，Visual Basic 程式設計語言無法辨識 c + + 不帶正負號的資料類型，例如 **unsignedÂ long**。</span><span class="sxs-lookup"><span data-stu-id="c30a5-114">For example, the Visual Basic programming language does not recognize C++ unsigned data types, such as **unsignedÂ long**.</span></span> <span data-ttu-id="c30a5-115">以 Visual Basic 撰寫的應用程式無法使用接受或傳回未簽署資料類型變數的 COM 方法。</span><span class="sxs-lookup"><span data-stu-id="c30a5-115">An application written in Visual Basic cannot use COM methods that accept or return unsigned data type variables.</span></span>

3.  <span data-ttu-id="c30a5-116">將 COM 物件的已編譯器代碼加入至您的專案。</span><span class="sxs-lookup"><span data-stu-id="c30a5-116">Add the COM object's compiled code to your project.</span></span> <span data-ttu-id="c30a5-117">編譯的程式碼通常包含在 .dll 或 .ocx 檔案中。</span><span class="sxs-lookup"><span data-stu-id="c30a5-117">The compiled code is typically contained in a .dll or .ocx file.</span></span> <span data-ttu-id="c30a5-118">編譯器必須要有這個步驟，才能辨識 COM 物件的類別。</span><span class="sxs-lookup"><span data-stu-id="c30a5-118">This step is necessary for the compiler to recognize the COM object's classes.</span></span> <span data-ttu-id="c30a5-119">新增 COM 物件之後，您的應用程式可以使用其類別和介面。</span><span class="sxs-lookup"><span data-stu-id="c30a5-119">After you add the COM object, your application can use its classes and interfaces.</span></span>

<span data-ttu-id="c30a5-120">下列主題描述如何以各種程式設計語言轉譯和使用 COM 物件：</span><span class="sxs-lookup"><span data-stu-id="c30a5-120">The following topics describe how to translate and use COM objects in a variety of programming languages:</span></span>

-   [<span data-ttu-id="c30a5-121">轉換成 c + +</span><span class="sxs-lookup"><span data-stu-id="c30a5-121">Translating to C++</span></span>](translating-to-c--.md)
-   [<span data-ttu-id="c30a5-122">翻譯為 Visual Basic</span><span class="sxs-lookup"><span data-stu-id="c30a5-122">Translating to Visual Basic</span></span>](translating-to-visual-basic.md)
-   [<span data-ttu-id="c30a5-123">轉換成 JAVA</span><span class="sxs-lookup"><span data-stu-id="c30a5-123">Translating to Java</span></span>](translating-to-java.md)

<span data-ttu-id="c30a5-124">這些主題說明 Microsoft developer 產品所提供的轉換工具和流程。</span><span class="sxs-lookup"><span data-stu-id="c30a5-124">These topics describe conversion tools and processes provided by Microsoft developer products.</span></span> <span data-ttu-id="c30a5-125">如需有關如何使用其他公司所建立的開發工具來撰寫 COM 物件的指示，請參閱這些開發工具的檔。</span><span class="sxs-lookup"><span data-stu-id="c30a5-125">For instructions on how to program COM objects using development tools created by other companies, see those development tools' documentation.</span></span>

 

 





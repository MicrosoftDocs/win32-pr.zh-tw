---
title: 存取控制項方法、屬性和事件
description: 存取控制項方法、屬性和事件
ms.assetid: 70a3b011-0290-4df4-9b66-23b27bcb14e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 750ad6280b521cf50c2ecd1fb7f1fcec3e2c4164
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372121"
---
# <a name="accessing-the-controls-methods-properties-and-events"></a><span data-ttu-id="5980f-103">存取控制項方法、屬性和事件</span><span class="sxs-lookup"><span data-stu-id="5980f-103">Accessing the Controls Methods, Properties, and Events</span></span>

<span data-ttu-id="5980f-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="5980f-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="5980f-105">使用 Microsoft Agent 的 control 搭配 Visual Basic 與使用 VBScript 的控制項非常類似，不同之處在于 Visual Basic 中的事件必須包含所傳遞參數的資料類型。</span><span class="sxs-lookup"><span data-stu-id="5980f-105">Using Microsoft Agent's control with Visual Basic is very similar to using the control with VBScript, except that events in Visual Basic must include the data type of passed parameters.</span></span> <span data-ttu-id="5980f-106">將 Microsoft Agent 控制項新增至表單時，會自動包含 Microsoft Agent 的事件及其適當的參數。</span><span class="sxs-lookup"><span data-stu-id="5980f-106">Adding the Microsoft Agent control to a form will automatically include Microsoft Agent's events with their appropriate parameters.</span></span> <span data-ttu-id="5980f-107">它也會在應用程式執行時，自動建立與代理程式伺服器的連接。</span><span class="sxs-lookup"><span data-stu-id="5980f-107">It will also automatically create a connection to the Agent server when the application runs.</span></span>

<span data-ttu-id="5980f-108">您也可以使用程式設計語言的 object's 建立語法，在執行時間建立控制項的實例。</span><span class="sxs-lookup"><span data-stu-id="5980f-108">You may also be able to use your programming language's object's creation syntax to create an instance of the control at runtime.</span></span> <span data-ttu-id="5980f-109">例如，在 Visual Basic (5.0 或更新版本的) 中，如果您將 Microsoft Agent 2.0 控制項包含在專案的參考中，您可以使用 [**With 事件**](https://www.bing.com/search?q=**With+Events**)。[**新**](https://www.bing.com/search?q=**New**) 宣告。</span><span class="sxs-lookup"><span data-stu-id="5980f-109">For example, in Visual Basic (5.0 or later), if you include the Microsoft Agent 2.0 Control in your project's references, you can use a [**With Events**](https://www.bing.com/search?q=**With+Events**)..[**New**](https://www.bing.com/search?q=**New**) declaration.</span></span> <span data-ttu-id="5980f-110">如果您未包含參考，VB 會引發錯誤，指出 Microsoft Agent 無法啟動 (錯誤碼 80042502) 。</span><span class="sxs-lookup"><span data-stu-id="5980f-110">If you do not include the reference, VB raises an error indicating that Microsoft Agent was unable to start (error code 80042502).</span></span>

``` syntax
   ' Declare a global variable for the control
   Dim WithEvents MyAgent as Agent

   ' Create an instance of the control using New
   Set MyAgent = New Agent

' Load a character
   MyAgent.Characters.Load "Genie", " Genie.acs"

   ' Display the character
   MyAgent.Characters("Genie").Show
```

<span data-ttu-id="5980f-111">針對5.0 之前的 VB 版本，您可以使用不含 [**WithEvents**](https://www.bing.com/search?q=**WithEvents**)宣告或 vb [**CreateObject**](https://msdn.microsoft.com/library/Bb545141(v=VS.85).aspx)函式的 vb [**New**](https://www.bing.com/search?q=**New**)關鍵字，但這些慣例不會公開 Agent 控制項的事件。</span><span class="sxs-lookup"><span data-stu-id="5980f-111">For versions of VB prior to 5.0, you can use the VB [**New**](https://www.bing.com/search?q=**New**) keyword without [**WithEvents**](https://www.bing.com/search?q=**WithEvents**) declaration or the VB [**CreateObject**](https://msdn.microsoft.com/library/Bb545141(v=VS.85).aspx) function, but these conventions will not expose the Agent control's events.</span></span> <span data-ttu-id="5980f-112">您也必須先使用 [**連接**](https://www.bing.com/search?q=**Connected**) 的屬性，才能參考任何代理程式方法或屬性。</span><span class="sxs-lookup"><span data-stu-id="5980f-112">You also need to use the [**Connected**](https://www.bing.com/search?q=**Connected**) property before you reference any Agent methods or properties.</span></span> <span data-ttu-id="5980f-113">如果未這麼做，VB 將會引發錯誤，指出 Microsoft Agent 無法啟動 (錯誤碼 80042502) 。</span><span class="sxs-lookup"><span data-stu-id="5980f-113">If this is not done, VB will raise an error indicating that Microsoft Agent was unable to start (error code 80042502).</span></span>

<span data-ttu-id="5980f-114">同樣地，對於其他程式設計語言，您可能必須使用 [**連接**](https://www.bing.com/search?q=**Connected**) 的屬性來建立與代理程式元件物件模型的連接， (COM) server，然後您的程式碼才能呼叫任何 agent 控制項的方法或屬性。</span><span class="sxs-lookup"><span data-stu-id="5980f-114">Similarly for other programming languages, you may have to use the [**Connected**](https://www.bing.com/search?q=**Connected**) property to establish a connection to the Agent Component Object Model (COM) server before your code can call any of the Agent control's methods or properties.</span></span> <span data-ttu-id="5980f-115">此外，針對某些程式設計語言，除非您使用它的型別來宣告 Agent 控制項，否則可能不會直接公開代理程式的方法和屬性。</span><span class="sxs-lookup"><span data-stu-id="5980f-115">In addition, for some programming languages, Agent's methods and properties may not be directly exposed unless you declare the Agent control using its type.</span></span> <span data-ttu-id="5980f-116">例如，在 Microsoft Access 97 中，當您輸入時，您必須將物件宣告為類型代理程式，才能看到 [自動清單成員] 下拉式方塊中顯示的方法和屬性。</span><span class="sxs-lookup"><span data-stu-id="5980f-116">For example, in Microsoft Access 97, you will need to declare the object as type Agent to see the methods and properties display in the Auto List Members drop-down box when you type.</span></span>

<span data-ttu-id="5980f-117">大部分支援 ActiveX 控制項的程式設計語言都遵循類似 Visual Basic 的慣例。</span><span class="sxs-lookup"><span data-stu-id="5980f-117">Most programming languages that support ActiveX controls follow conventions similar to Visual Basic.</span></span> <span data-ttu-id="5980f-118">針對不支持對象集合的程式設計語言，您可以使用 [**字元**](https://www.bing.com/search?q=**Character**) 方法和 [**命令**](https://www.bing.com/search?q=**Command**) 方法來存取集合中專案的方法和屬性。</span><span class="sxs-lookup"><span data-stu-id="5980f-118">For programming languages that do not support object collections, you can use the [**Character**](https://www.bing.com/search?q=**Character**) method and [**Command**](https://www.bing.com/search?q=**Command**) method to access methods and properties of items in the collection.</span></span>

<span data-ttu-id="5980f-119">程式設計語言（例如 Visual Basic）可提供 Agent 控制項所公開之物件類型的存取權，讓您在物件宣告中使用這些語言。</span><span class="sxs-lookup"><span data-stu-id="5980f-119">Programming languages like Visual Basic, that provide access to the object types exposed by the Agent control, enable you to use these in your object declarations.</span></span> <span data-ttu-id="5980f-120">例如，不會將物件宣告為泛型型別：</span><span class="sxs-lookup"><span data-stu-id="5980f-120">For example, instead of declaring an object as a generic type:</span></span>

``` syntax
   Dim Genie as Object
```

<span data-ttu-id="5980f-121">您可以將物件宣告為特定類型：</span><span class="sxs-lookup"><span data-stu-id="5980f-121">You can declare an object as a specific type:</span></span>

``` syntax
   Dim Genie as IAgentCtlCharacterEx
```

<span data-ttu-id="5980f-122">這可能會改善您應用程式的整體效能。</span><span class="sxs-lookup"><span data-stu-id="5980f-122">This may improve the overall performance of your application.</span></span>

<span data-ttu-id="5980f-123">針對某些物件類型，您可能會發現兩種類型都相同，但 "Ex" 尾碼除外。</span><span class="sxs-lookup"><span data-stu-id="5980f-123">For some object types, you may find two types that are the same except for the "Ex" suffix.</span></span> <span data-ttu-id="5980f-124">兩者都存在，請使用 "Ex" 類型，因為這會提供代理程式的完整功能。</span><span class="sxs-lookup"><span data-stu-id="5980f-124">Where both exist, use the "Ex" type because this provides the full functionality of Agent.</span></span> <span data-ttu-id="5980f-125">非「Ex」的對應專案只是為了與舊版相容。</span><span class="sxs-lookup"><span data-stu-id="5980f-125">The non-"Ex" counterparts are included only for backward compatibility.</span></span>

 

 





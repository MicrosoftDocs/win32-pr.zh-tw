---
title: Request 物件
description: Request 物件
ms.assetid: d8b37164-6855-48c0-bcf8-a86c0f8b3a59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a50d554a5799af9a434b456113d7c826d2a0aa2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106966030"
---
# <a name="the-request-object"></a><span data-ttu-id="53364-103">Request 物件</span><span class="sxs-lookup"><span data-stu-id="53364-103">The Request Object</span></span>

<span data-ttu-id="53364-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="53364-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="53364-105">伺服器會以非同步方式處理一些方法。</span><span class="sxs-lookup"><span data-stu-id="53364-105">The server processes some methods asynchronously.</span></span> <span data-ttu-id="53364-106">這可讓您的應用程式程式碼在方法完成時繼續執行。</span><span class="sxs-lookup"><span data-stu-id="53364-106">This enables your application code to continue while the method is completing.</span></span> <span data-ttu-id="53364-107">當用戶端應用程式呼叫其中一個方法時，控制項會建立並傳回要求的 [**要求**](/windows/desktop/lwef/the-request-object) 物件。</span><span class="sxs-lookup"><span data-stu-id="53364-107">When a client application calls one of these methods, the control creates and returns a [**Request**](/windows/desktop/lwef/the-request-object) object for the request.</span></span> <span data-ttu-id="53364-108">您可以藉由將物件變數指派給方法，使用 **Request** 物件來追蹤方法的狀態。</span><span class="sxs-lookup"><span data-stu-id="53364-108">You can use the **Request** object to track the status of the method by assigning an object variable to the method.</span></span> <span data-ttu-id="53364-109">在 Visual Basic 中，先宣告物件變數：</span><span class="sxs-lookup"><span data-stu-id="53364-109">In Visual Basic, first declare an object variable:</span></span>


```
   Dim MyRequest as Object
```



<span data-ttu-id="53364-110">在 VBScript 中，您不會在宣告中包含變數類型：</span><span class="sxs-lookup"><span data-stu-id="53364-110">In VBScript, you don't include the variable type in your declaration:</span></span>


```
   Dim MyRequest
```



<span data-ttu-id="53364-111">然後使用 Visual Basic 的 Set 語句，將變數指派給方法呼叫：</span><span class="sxs-lookup"><span data-stu-id="53364-111">And use Visual Basic's Set statement to assign the variable to the method call:</span></span>


```
   Set MyRequest = <i>agent</i>.Characters("<i>CharacterID</i>").<i>method</i> (<i>parameter</i>[s])
```



<span data-ttu-id="53364-112">這會將參考加入至 [**要求**](/windows/desktop/lwef/the-request-object) 物件。</span><span class="sxs-lookup"><span data-stu-id="53364-112">This adds a reference to the [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span> <span data-ttu-id="53364-113">當 **要求** 物件沒有其他參考時，就會終結要求物件。</span><span class="sxs-lookup"><span data-stu-id="53364-113">The **Request** object will be destroyed when there are no more references to it.</span></span> <span data-ttu-id="53364-114">當您宣告 **要求** 物件和使用它的方式時，會決定其存留期。</span><span class="sxs-lookup"><span data-stu-id="53364-114">Where you declare the **Request** object and how you use it determines its lifetime.</span></span> <span data-ttu-id="53364-115">如果在副程式或函式的區域變數中宣告物件，則會在超出範圍時終結該物件;也就是說，當副程式或函式結束時。</span><span class="sxs-lookup"><span data-stu-id="53364-115">If the object is declared local to a subroutine or function, it will be destroyed when it goes out of scope; that is, when the subroutine or function ends.</span></span> <span data-ttu-id="53364-116">如果物件是全域宣告，則在程式終止或新值 (或將值設定為 "empty" ) 指派給物件之前，將不會終結該物件。</span><span class="sxs-lookup"><span data-stu-id="53364-116">If the object is declared globally, it will not be destroyed until either the program terminates or a new value (or a value set to "empty") is assigned to the object.</span></span>

<span data-ttu-id="53364-117">[**Request**](/windows/desktop/lwef/the-request-object)物件提供數個可供您查詢的屬性。</span><span class="sxs-lookup"><span data-stu-id="53364-117">The [**Request**](/windows/desktop/lwef/the-request-object) object provides several properties you can query.</span></span> <span data-ttu-id="53364-118">例如， [**status**](status-property.md) 屬性會傳回要求的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="53364-118">For example, the [**Status**](status-property.md) property returns the current status of the request.</span></span> <span data-ttu-id="53364-119">您可以使用這個屬性來檢查要求的狀態：</span><span class="sxs-lookup"><span data-stu-id="53364-119">You can use this property to check the status of your request:</span></span>


```
   Dim MyRequest
   
   Set MyRequest = Agent1.Characters.Load ("Genie", "https://agent.microsoft.com/characters/v2/genie/genie.acf")

   If (MyRequest.Status = 2) then
      'do something

   Else If (MyRequest.Status = 0) then
      'do something right away

   End If
```



<span data-ttu-id="53364-120">[**Status**](status-property.md)屬性會以長整數值的形式傳回 [**要求**](/windows/desktop/lwef/the-request-object)物件的狀態。</span><span class="sxs-lookup"><span data-stu-id="53364-120">The [**Status**](status-property.md) property returns the status of a [**Request**](/windows/desktop/lwef/the-request-object) object as a Long integer value.</span></span>



| <span data-ttu-id="53364-121">狀態</span><span class="sxs-lookup"><span data-stu-id="53364-121">Status</span></span> | <span data-ttu-id="53364-122">定義</span><span class="sxs-lookup"><span data-stu-id="53364-122">Definition</span></span>                                        |
|--------|---------------------------------------------------|
| <span data-ttu-id="53364-123">0</span><span class="sxs-lookup"><span data-stu-id="53364-123">0</span></span>      | <span data-ttu-id="53364-124">要求已成功完成。</span><span class="sxs-lookup"><span data-stu-id="53364-124">Request successfully completed.</span></span>                   |
| <span data-ttu-id="53364-125">1</span><span class="sxs-lookup"><span data-stu-id="53364-125">1</span></span>      | <span data-ttu-id="53364-126">要求失敗。</span><span class="sxs-lookup"><span data-stu-id="53364-126">Request failed.</span></span>                                   |
| <span data-ttu-id="53364-127">2</span><span class="sxs-lookup"><span data-stu-id="53364-127">2</span></span>      | <span data-ttu-id="53364-128">要求佇列中的暫止 (，但未完成) 。</span><span class="sxs-lookup"><span data-stu-id="53364-128">Request pending (in the queue, but not complete).</span></span> |
| <span data-ttu-id="53364-129">3</span><span class="sxs-lookup"><span data-stu-id="53364-129">3</span></span>      | <span data-ttu-id="53364-130">要求已中斷。</span><span class="sxs-lookup"><span data-stu-id="53364-130">Request interrupted.</span></span>                              |
| <span data-ttu-id="53364-131">4</span><span class="sxs-lookup"><span data-stu-id="53364-131">4</span></span>      | <span data-ttu-id="53364-132">要求進行中。</span><span class="sxs-lookup"><span data-stu-id="53364-132">Request in progress.</span></span>                              |



 

<span data-ttu-id="53364-133">[**Request**](/windows/desktop/lwef/the-request-object)物件也會在 [**Number**](https://www.bing.com/search?q=**Number**)屬性中包含一個長整數值，此值會傳回錯誤或 [**狀態**](status-property.md)代碼的原因。</span><span class="sxs-lookup"><span data-stu-id="53364-133">The [**Request**](/windows/desktop/lwef/the-request-object) object also includes a Long integer value in the [**Number**](https://www.bing.com/search?q=**Number**) property that returns the error or cause of the [**Status**](status-property.md) code.</span></span> <span data-ttu-id="53364-134">如果沒有，則這個值為零 (0) 。</span><span class="sxs-lookup"><span data-stu-id="53364-134">If none, this value is zero (0).</span></span> <span data-ttu-id="53364-135">[**Description**](description-property.md)屬性包含對應至錯誤號碼的字串值。</span><span class="sxs-lookup"><span data-stu-id="53364-135">The [**Description**](description-property.md) property contains a string value that corresponds to the error number.</span></span> <span data-ttu-id="53364-136">如果字串不存在， **描述** 會包含「應用程式定義或物件定義的錯誤」。</span><span class="sxs-lookup"><span data-stu-id="53364-136">If the string doesn't exist, **Description** contains "Application-defined or object-defined error".</span></span>

<span data-ttu-id="53364-137">如需 [**Number**](https://www.bing.com/search?q=**Number**) 屬性所傳回的值和意義，請參閱 [錯誤碼](microsoft-agent-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="53364-137">For the values and meaning returned by the [**Number**](https://www.bing.com/search?q=**Number**) property, see [Error Codes](microsoft-agent-error-codes.md).</span></span>

<span data-ttu-id="53364-138">伺服器會將動畫要求放在指定的字元佇列中。</span><span class="sxs-lookup"><span data-stu-id="53364-138">The server places animation requests in the specified character's queue.</span></span> <span data-ttu-id="53364-139">這可讓伺服器在不同的執行緒上播放動畫，而您的應用程式程式碼可以在動畫播放時繼續。</span><span class="sxs-lookup"><span data-stu-id="53364-139">This enables the server to play the animation on a separate thread, and your application's code can continue while animations play.</span></span> <span data-ttu-id="53364-140">如果您建立 [**要求**](/windows/desktop/lwef/the-request-object) 物件參考，伺服器會在動畫要求透過 [**RequestStart**](https://www.bing.com/search?q=**RequestStart**) 和 [**RequestComplete**](https://www.bing.com/search?q=**RequestComplete**) 事件啟動或完成時，自動通知您。</span><span class="sxs-lookup"><span data-stu-id="53364-140">If you create a [**Request**](/windows/desktop/lwef/the-request-object) object reference, the server automatically notifies you when an animation request has started or completed through the [**RequestStart**](https://www.bing.com/search?q=**RequestStart**) and [**RequestComplete**](https://www.bing.com/search?q=**RequestComplete**) events.</span></span> <span data-ttu-id="53364-141">因為傳回 **要求** 物件的方法是非同步，而且可能不會在呼叫函式的範圍內完成，所以請將您的參考全域宣告給您的 **要求** 物件。</span><span class="sxs-lookup"><span data-stu-id="53364-141">Because methods that return **Request** objects are asynchronous and may not complete during the scope of the calling function, declare your reference to the **Request** object globally.</span></span>

<span data-ttu-id="53364-142">下列方法可以用來傳回 [**Request**](/windows/desktop/lwef/the-request-object)物件： [**GestureAt**](gestureat-method.md)、 [**Get**](get-method.md)、 [**Hide**](hide-method.md)、插斷、 [\*\*\*\*](interrupt-method.md)[**載入**](load-method.md)、 [**MoveTo**](moveto-method.md)、[**播放**](play-method.md)、[**顯示**](show-method.md)、[**說話**](speak-method.md)和 [**等候**](https://www.bing.com/search?q=**Wait**)。</span><span class="sxs-lookup"><span data-stu-id="53364-142">The following methods can be used to return a [**Request**](/windows/desktop/lwef/the-request-object) object: [**GestureAt**](gestureat-method.md), [**Get**](get-method.md), [**Hide**](hide-method.md), [**Interrupt**](interrupt-method.md), [**Load**](load-method.md), [**MoveTo**](moveto-method.md), [**Play**](play-method.md), [**Show**](show-method.md), [**Speak**](speak-method.md), and [**Wait**](https://www.bing.com/search?q=**Wait**).</span></span>

 

 
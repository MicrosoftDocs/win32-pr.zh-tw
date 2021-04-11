---
title: 字元物件方法
description: 字元物件方法
ms.assetid: 0f926b7b-c1cf-4bd6-ba8c-1b2877eb1d24
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19bb0dbb256c99660cbce1613c9fdd27d85a92dc
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933104"
---
# <a name="character-object-methods"></a><span data-ttu-id="9f89a-103">字元物件方法</span><span class="sxs-lookup"><span data-stu-id="9f89a-103">Character Object Methods</span></span>

<span data-ttu-id="9f89a-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="9f89a-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="9f89a-105">伺服器也會公開 [**字元**](/windows/desktop/lwef/the-characters-object) 集合中每個字元的方法。</span><span class="sxs-lookup"><span data-stu-id="9f89a-105">The server also exposes methods for each character in a [**Characters**](/windows/desktop/lwef/the-characters-object) collection.</span></span> <span data-ttu-id="9f89a-106">以下是支援的方法：</span><span class="sxs-lookup"><span data-stu-id="9f89a-106">The following methods are supported:</span></span>

-   [<span data-ttu-id="9f89a-107">**啟動**</span><span class="sxs-lookup"><span data-stu-id="9f89a-107">**Activate**</span></span>](activate-method.md)
-   [<span data-ttu-id="9f89a-108">**GestureAt**</span><span class="sxs-lookup"><span data-stu-id="9f89a-108">**GestureAt**</span></span>](gestureat-method.md)
-   [<span data-ttu-id="9f89a-109">**Get**</span><span class="sxs-lookup"><span data-stu-id="9f89a-109">**Get**</span></span>](get-method.md)
-   [<span data-ttu-id="9f89a-110">**隱藏**</span><span class="sxs-lookup"><span data-stu-id="9f89a-110">**Hide**</span></span>](hide-method.md)
-   [<span data-ttu-id="9f89a-111">**中斷**</span><span class="sxs-lookup"><span data-stu-id="9f89a-111">**Interrupt**</span></span>](interrupt-method.md)
-   [<span data-ttu-id="9f89a-112">**接聽**</span><span class="sxs-lookup"><span data-stu-id="9f89a-112">**Listen**</span></span>](listen-method.md)
-   [<span data-ttu-id="9f89a-113">**MoveTo**</span><span class="sxs-lookup"><span data-stu-id="9f89a-113">**MoveTo**</span></span>](moveto-method.md)
-   [<span data-ttu-id="9f89a-114">**播放**</span><span class="sxs-lookup"><span data-stu-id="9f89a-114">**Play**</span></span>](play-method.md)
-   [<span data-ttu-id="9f89a-115">**顯示**</span><span class="sxs-lookup"><span data-stu-id="9f89a-115">**Show**</span></span>](show-method.md)
-   [<span data-ttu-id="9f89a-116">**ShowPopupMenu**</span><span class="sxs-lookup"><span data-stu-id="9f89a-116">**ShowPopupMenu**</span></span>](showpopupmenu-method.md)
-   [<span data-ttu-id="9f89a-117">**Speak**</span><span class="sxs-lookup"><span data-stu-id="9f89a-117">**Speak**</span></span>](speak-method.md)
-   [<span data-ttu-id="9f89a-118">**停止**</span><span class="sxs-lookup"><span data-stu-id="9f89a-118">**Stop**</span></span>](stop-method.md)
-   [<span data-ttu-id="9f89a-119">**StopAll**</span><span class="sxs-lookup"><span data-stu-id="9f89a-119">**StopAll**</span></span>](stopall-method.md)
-   [<span data-ttu-id="9f89a-120">**認為**</span><span class="sxs-lookup"><span data-stu-id="9f89a-120">**Think**</span></span>](think-method.md)
-   [<span data-ttu-id="9f89a-121">**等候**</span><span class="sxs-lookup"><span data-stu-id="9f89a-121">**Wait**</span></span>](wait-method.md)

<span data-ttu-id="9f89a-122">若要使用方法，請參考集合中的字元。</span><span class="sxs-lookup"><span data-stu-id="9f89a-122">To use a method, reference the character in the collection.</span></span> <span data-ttu-id="9f89a-123">在 VBScript 和 Visual Basic 中，您可以藉由指定字元的識別碼來執行此動作：</span><span class="sxs-lookup"><span data-stu-id="9f89a-123">In VBScript and Visual Basic, you do this by specifying the ID for a character:</span></span>


```
   Sub FormLoad

   'Load the genie character into the Characters collection
   Agent1.Characters.Load "Genie", "Genie.acs"

   'Display the character
   Agent1.Characters("Genie").Show
   Agent1.Characters("Genie").Play "Greet"
   Agent1.Characters("Genie").Speak "Hello. "

   End Sub
```



<span data-ttu-id="9f89a-124">若要簡化程式碼的語法，您可以定義物件變數，並將它設定為參考 [**字元**](/windows/desktop/lwef/the-characters-object) 集合中的字元物件;然後，您可以使用變數來參考字元的方法或屬性。</span><span class="sxs-lookup"><span data-stu-id="9f89a-124">To simplify the syntax of your code, you can define an object variable and set it to reference a character object in the [**Characters**](/windows/desktop/lwef/the-characters-object) collection; then you can use your variable to reference methods or properties of the character.</span></span> <span data-ttu-id="9f89a-125">下列範例示範如何使用 Visual Basic Set 語句來執行這項作業：</span><span class="sxs-lookup"><span data-stu-id="9f89a-125">The following example demonstrates how you can do this using the Visual Basic Set statement:</span></span>


```
   'Define a global object variable
   Dim Genie as Object

   Sub FormLoad

   'Load the genie character into the Characters collection
   Agent1.Characters.Load "Genie", " Genie.acs"

   'Create a reference to the character
   Set Genie = Agent1.Characters("Genie")

   'Display the character
   Genie.Show

   'Get the Restpose animation
   Genie.Get "animation", "RestPose"

   'Make the character say Hello
   Genie.Speak "Hello."

   End Sub
```



<span data-ttu-id="9f89a-126">在 Visual Basic 5.0 中，您也可以將變數宣告為 [**字元**](/windows/desktop/lwef/the-characters-object)物件來建立參考：</span><span class="sxs-lookup"><span data-stu-id="9f89a-126">In Visual Basic 5.0, you can also create your reference by declaring your variable as a [**Character**](/windows/desktop/lwef/the-characters-object)object:</span></span>


```
   Dim Genie as IAgentCtlCharacterEx

   Sub FormLoad

   'Load the genie character into the Characters collection
   Agent1.Characters.Load "Genie", "Genie.acs"

   'Create a reference to the character
   Set Genie = Agent1.Characters("Genie")

   'Display the character
   Genie.Show

   End Sub
```



<span data-ttu-id="9f89a-127">宣告 IAgentCtlCharacterEx 型別的物件，可在物件上進行早期繫結，進而產生更好的效能。</span><span class="sxs-lookup"><span data-stu-id="9f89a-127">Declaring your object of type IAgentCtlCharacterEx enables early binding on the object, which results in better performance.</span></span>

<span data-ttu-id="9f89a-128">在 VBScript 中，您無法將參考宣告為特定類型。</span><span class="sxs-lookup"><span data-stu-id="9f89a-128">In VBScript, you cannot declare a reference as a particular type.</span></span> <span data-ttu-id="9f89a-129">不過，您可以直接宣告變數參考：</span><span class="sxs-lookup"><span data-stu-id="9f89a-129">However, you can simply declare the variable reference:</span></span>


```
<SCRIPT LANGUAGE = "VBSCRIPT">
<!—--

   Dim Genie
   
   Sub window_OnLoad
   
   'Load the character
   AgentCtl.Characters.Load "Genie", "https://agent.microsoft.com/characters/v2/genie/genie.acf"

   'Create an object reference to the character in the collection
   set Genie= AgentCtl.Characters ("Genie")

   'Get the Showing state animation
   Genie.Get "state", "Showing"

   'Display the character
   Genie.Show

   End Sub

-->
   </SCRIPT>
```



<span data-ttu-id="9f89a-130">某些程式設計語言不支援集合。</span><span class="sxs-lookup"><span data-stu-id="9f89a-130">Some programming languages do not support collections.</span></span> <span data-ttu-id="9f89a-131">不過，您可以使用 [**字元**](character-method.md)方法來存取 [**字元**](/windows/desktop/lwef/the-characters-object)物件的方法：</span><span class="sxs-lookup"><span data-stu-id="9f89a-131">However, you can access a [**Character**](/windows/desktop/lwef/the-characters-object) object's methods with the [**Character**](character-method.md) method:</span></span>


```
   agent.Characters.Character("CharacterID").method
```



<span data-ttu-id="9f89a-132">此外，您也可以建立 [**字元**](/windows/desktop/lwef/the-characters-object) 物件的參考，讓腳本程式碼更容易遵循：</span><span class="sxs-lookup"><span data-stu-id="9f89a-132">In addition, you can also create a reference to the [**Character**](/windows/desktop/lwef/the-characters-object) object to make your script code easier to follow:</span></span>


```
<SCRIPT LANGUAGE="JScript" FOR="window" EVENT="onLoad()">
<!--
   
   //Load the character's data
   AgentCtl.Characters.Load ("Genie", _
      "https://agent.microsoft.com/characters/v2/genie/genie.acf");   

   //Create a reference to this object
   Genie = AgentCtl.Characters.Character("Genie");
   
   //Get the Showing state animation
   Genie.Get("state", "Showing");

   //Display the character
   Genie.Show();

-->
</SCRIPT>
```



 

 
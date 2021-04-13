---
title: 連接屬性
description: 連接屬性
ms.assetid: 61b7f550-d8d6-4719-a0d4-0bf3a8cf096c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bba78358c7c42f0754da017aa0c188d41acd189
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301423"
---
# <a name="connected-property"></a><span data-ttu-id="d79bc-103">連接屬性</span><span class="sxs-lookup"><span data-stu-id="d79bc-103">Connected Property</span></span>

<span data-ttu-id="d79bc-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="d79bc-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="d79bc-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="d79bc-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="d79bc-106">傳回或設定目前的控制項是否連接至 Microsoft 代理程式伺服器。</span><span class="sxs-lookup"><span data-stu-id="d79bc-106">Returns or sets whether the current control is connected to the Microsoft Agent server.</span></span>

</dd> <dt>

<span data-ttu-id="d79bc-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="d79bc-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="d79bc-108">*代理程式。 \* \* \* 已連線* \*  \[  = *布林值*\]</span><span class="sxs-lookup"><span data-stu-id="d79bc-108">*agent.\*\*\*Connected*\* \[ = *boolean*\]</span></span>



| <span data-ttu-id="d79bc-109">部分</span><span class="sxs-lookup"><span data-stu-id="d79bc-109">Part</span></span>      | <span data-ttu-id="d79bc-110">描述</span><span class="sxs-lookup"><span data-stu-id="d79bc-110">Description</span></span>                                                                                                     |
|-----------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d79bc-111">*boolean*</span><span class="sxs-lookup"><span data-stu-id="d79bc-111">*boolean*</span></span> | <span data-ttu-id="d79bc-112">指定控制項是否已連接的布林運算式。</span><span class="sxs-lookup"><span data-stu-id="d79bc-112">A Boolean expression specifying whether the control is connected.</span></span> <span data-ttu-id="d79bc-113">**True** 控制項已連接。</span><span class="sxs-lookup"><span data-stu-id="d79bc-113">**True** The control is connected.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d79bc-114">備註</span><span class="sxs-lookup"><span data-stu-id="d79bc-114">Remarks</span></span>

<span data-ttu-id="d79bc-115">在許多情況下，指定控制項會自動建立與 Microsoft 代理程式伺服器之間的連接。</span><span class="sxs-lookup"><span data-stu-id="d79bc-115">In many situations, specifying the control automatically creates a connection with the Microsoft Agent server.</span></span> <span data-ttu-id="d79bc-116">例如，在網頁的標籤中指定 Microsoft Agent 控制項的 CLSID 時， <OBJECT> 會自動開啟伺服器連接，而結束頁面則會關閉連接。</span><span class="sxs-lookup"><span data-stu-id="d79bc-116">For example, specifying the Microsoft Agent control's CLSID in the <OBJECT> tag in a webpage automatically opens a server connection and exiting the page closes the connection.</span></span> <span data-ttu-id="d79bc-117">同樣地，對於可讓您將控制項放在表單上的 Visual Basic 或其他語言，執行程式會自動開啟連接，而結束程式則會關閉連接。</span><span class="sxs-lookup"><span data-stu-id="d79bc-117">Similarly, for Visual Basic or other languages that enable you to drop a control on a form, running the program automatically opens a connection and exiting the program closes the connection.</span></span> <span data-ttu-id="d79bc-118">如果伺服器目前不在執行中，則會自動啟動。</span><span class="sxs-lookup"><span data-stu-id="d79bc-118">If the server isn't currently running, it automatically starts.</span></span>

<span data-ttu-id="d79bc-119">但是，如果您想要在執行時間建立 Agent 控制項，您可能也需要使用 **連接** 的屬性來明確開啟伺服器的新連接。</span><span class="sxs-lookup"><span data-stu-id="d79bc-119">However, if you want to create an Agent control at run time, you may also need to explicitly open a new connection to the server using the **Connected** property.</span></span> <span data-ttu-id="d79bc-120">例如，在 Visual Basic 您可以在執行時間使用 Set 語句搭配 **New** 關鍵字 (或 CreateObject 函數) 來建立 ActiveX 物件。</span><span class="sxs-lookup"><span data-stu-id="d79bc-120">For example, in Visual Basic you can create an ActiveX object at run time using the Set statement with the **New** keyword (or CreateObject function).</span></span> <span data-ttu-id="d79bc-121">雖然這會建立物件，但它可能不會建立與伺服器的連接。</span><span class="sxs-lookup"><span data-stu-id="d79bc-121">While this creates the object, it may not create the connection to the server.</span></span> <span data-ttu-id="d79bc-122">您可以在呼叫 Microsoft 代理程式的程式設計介面的任何程式碼之前使用 **連接** 的屬性，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="d79bc-122">You can use the **Connected** property before any code that calls into Microsoft Agent's programming interface, as shown in the following example:</span></span>


```
   ' Declare a global variable for the control
   Dim MyAgent as Agent

   ' Create an instance of the control using New
   Set MyAgent = New Agent

   ' Open a connection to the server
   MyAgent.Connected = True

   ' Load a character
   MyAgent.Characters.Load "Genie", " Genie.acs"

   ' Display the character
   MyAgent.Characters("Genie").Show
```



<span data-ttu-id="d79bc-123">使用這項技術來建立控制項，並不會公開 Agent 控制項的事件。</span><span class="sxs-lookup"><span data-stu-id="d79bc-123">Creating a control using this technique does not expose the Agent control's events.</span></span> <span data-ttu-id="d79bc-124">在 Visual Basic 5.0 (和更新版本的) 中，您可以在專案的參考中包含控制項，以存取控制項的事件，並在您的變數宣告中使用 **WithEvents** 關鍵字：</span><span class="sxs-lookup"><span data-stu-id="d79bc-124">In Visual Basic 5.0 (and later), you can access the control's events by including the control in your project's references, and use the **WithEvents** keyword in your variable declaration:</span></span>


```
   Dim WithEvents MyAgent as Agent

   ' Create an instance of the control using New
   Set MyAgent = New Agent
```



<span data-ttu-id="d79bc-125">當您在執行時間使用 **WithEvents** 建立 Agent 控制項的實例時，會自動開啟與 Microsoft 代理程式伺服器之間的連接。</span><span class="sxs-lookup"><span data-stu-id="d79bc-125">Using **WithEvents** to create an instance of the Agent control at run time automatically opens the connection with the Microsoft Agent server.</span></span> <span data-ttu-id="d79bc-126">因此，您不需要包含 **連接** 的語句。</span><span class="sxs-lookup"><span data-stu-id="d79bc-126">Therefore, you don't need to include a **Connected** statement.</span></span>

<span data-ttu-id="d79bc-127">您可以將建立的所有參考釋出至代理程式物件（例如 IAgentCtlCharacterEx 和 IAgentCtlCommandEx），以關閉與伺服器的連接。</span><span class="sxs-lookup"><span data-stu-id="d79bc-127">You can close your connection to the server by releasing all references you created to Agent objects, such as IAgentCtlCharacterEx and IAgentCtlCommandEx.</span></span> <span data-ttu-id="d79bc-128">您也必須釋放 Agent 控制項本身的參考。</span><span class="sxs-lookup"><span data-stu-id="d79bc-128">You must also release your reference to the Agent control itself.</span></span> <span data-ttu-id="d79bc-129">在 Visual Basic 中，您可以藉由將物件的變數設定為 **Nothing** 來釋出物件的參考。</span><span class="sxs-lookup"><span data-stu-id="d79bc-129">In Visual Basic, you can release a reference to an object by setting its variable to **Nothing**.</span></span> <span data-ttu-id="d79bc-130">如果您已載入字元，請在釋放字元物件之前先將它們卸載。</span><span class="sxs-lookup"><span data-stu-id="d79bc-130">If you have loaded characters, unload them before releasing the character object.</span></span>


```
   Dim WithEvents MyAgent as Agent
   Dim Genie as IAgentCtlCharacterEx
   
   Sub Form_Load

   ' Create an instance of the control using New
   Set MyAgent = New Agent

   ' Open a connection to the server
   MyAgent.Connected = True

   ' Load the character into the Characters collection
   MyAgent.Characters.Load "Genie", " Genie.acs"

   ' Create a reference to the character
   Set Genie = MyAgent.Characters("Genie")

   End Sub

   Sub CloseConnection

   ' Unload the character
   MyAgent.Characters.Unload "Genie"

   ' Release the reference to the character object
   Set Genie = Nothing

   ' Release the reference to the Agent control
   Set MyAgent = Nothing
   End Sub
```



> [!Note]  
> <span data-ttu-id="d79bc-131">您無法藉由釋放已加入元件的參考，關閉與伺服器的連接。</span><span class="sxs-lookup"><span data-stu-id="d79bc-131">You cannot close your connection to the server by releasing references where the component has been added.</span></span> <span data-ttu-id="d79bc-132">例如，您無法在使用標記來宣告控制項的網頁上， <OBJECT> 或是在您將控制項放在表單上的 Visual Basic 應用程式中，關閉與伺服器的連接。</span><span class="sxs-lookup"><span data-stu-id="d79bc-132">For example, you cannot close your connection to the server on webpages where you use the <OBJECT> tag to declare the control or in a Visual Basic application where you drop the control on a form.</span></span> <span data-ttu-id="d79bc-133">釋放所有的代理程式參考時，將會降低代理程式的工作集，而在您流覽至下一個頁面或結束應用程式之前，連接都會保持不變。</span><span class="sxs-lookup"><span data-stu-id="d79bc-133">While releasing all Agent references will reduce Agent's working set, the connection remains until you navigate to the next page or exit the application.</span></span>

 

 

 






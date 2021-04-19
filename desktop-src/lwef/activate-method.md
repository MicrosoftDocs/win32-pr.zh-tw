---
title: Activate 方法
description: Activate 方法
ms.assetid: 8111139d-1453-416e-8f08-38c06669ff4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21df1965abaeed35e9e440a0f559f5e12d68d6fe
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106969099"
---
# <a name="activate-method"></a><span data-ttu-id="3233b-103">Activate 方法</span><span class="sxs-lookup"><span data-stu-id="3233b-103">Activate Method</span></span>

<span data-ttu-id="3233b-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="3233b-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="3233b-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>[**描述**](../wmformat/description.md)</span><span class="sxs-lookup"><span data-stu-id="3233b-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>[**Description**](../wmformat/description.md)</span></span>
</dt> <dd>

<span data-ttu-id="3233b-106">設定使用中的用戶端或字元。</span><span class="sxs-lookup"><span data-stu-id="3233b-106">Sets the active client or character.</span></span>

</dd> <dt>

<span data-ttu-id="3233b-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="3233b-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="3233b-108">\*代理程式 ***。 ( "*** CharacterID \* \* *" 的字元 ) 。啟用* \*  \[ *狀態*\]</span><span class="sxs-lookup"><span data-stu-id="3233b-108">*agent ***.Characters ("*** CharacterID\*\*\*").Activate*\* \[*State*\]</span></span>



| <span data-ttu-id="3233b-109">部分</span><span class="sxs-lookup"><span data-stu-id="3233b-109">Part</span></span>    | <span data-ttu-id="3233b-110">描述</span><span class="sxs-lookup"><span data-stu-id="3233b-110">Description</span></span>                                                                                                                                                                           |
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3233b-111">*State*</span><span class="sxs-lookup"><span data-stu-id="3233b-111">*State*</span></span> | <span data-ttu-id="3233b-112">選擇性。</span><span class="sxs-lookup"><span data-stu-id="3233b-112">Optional.</span></span> <span data-ttu-id="3233b-113">您可以為此參數指定下列值：0不是作用中的用戶端。</span><span class="sxs-lookup"><span data-stu-id="3233b-113">You can specify the following values for this parameter: 0 Not the active client.</span></span><br/> <span data-ttu-id="3233b-114">1個作用中用戶端。</span><span class="sxs-lookup"><span data-stu-id="3233b-114">1 The active client.</span></span> <br/> <span data-ttu-id="3233b-115">2 (預設) 最頂端的字元。</span><span class="sxs-lookup"><span data-stu-id="3233b-115">2 (Default) The topmost character.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3233b-116">備註</span><span class="sxs-lookup"><span data-stu-id="3233b-116">Remarks</span></span>

<span data-ttu-id="3233b-117">當有多個字元可見時，一次只能有一個字元接收語音輸入。</span><span class="sxs-lookup"><span data-stu-id="3233b-117">When multiple characters are visible, only one of the characters receives speech input at a time.</span></span> <span data-ttu-id="3233b-118">同樣地，當多個用戶端應用程式共用相同的字元時，只有其中一個用戶端會收到滑鼠輸入 (例如，Microsoft Agent control click 或拖曳 events) 。</span><span class="sxs-lookup"><span data-stu-id="3233b-118">Similarly, when multiple client applications share the same character, only one of the clients receives mouse input (for example, Microsoft Agent control click or drag events).</span></span> <span data-ttu-id="3233b-119">用來接收滑鼠和語音輸入的字元集是最上層的字元，而接收輸入的用戶端是該字元的作用中用戶端。</span><span class="sxs-lookup"><span data-stu-id="3233b-119">The character set to receive mouse and speech input is the topmost character and the client that receives the input is the active client of that character.</span></span> <span data-ttu-id="3233b-120"> (最頂端的字元視窗也會出現在字元視窗的迭置順序頂端。 ) 一般會明確地選取字元，以決定最頂端的字元。</span><span class="sxs-lookup"><span data-stu-id="3233b-120">(The topmost character's window also appears at the top of the character window's z-order.) Typically, the user determines the topmost character by explicitly selecting the character.</span></span> <span data-ttu-id="3233b-121">不過，當字元顯示或隱藏 (字元變成或不再是最上層時，最上層啟用也會變更。 ) </span><span class="sxs-lookup"><span data-stu-id="3233b-121">However, topmost activation also changes when a character is shown or hidden (the character becomes or is no longer topmost, respectively.)</span></span>

<span data-ttu-id="3233b-122">您也可以使用這個方法，在用戶端收到導向字元的輸入時明確管理，例如當您的應用程式本身變成作用中時。</span><span class="sxs-lookup"><span data-stu-id="3233b-122">You can also use this method to explicitly manage when your client receives input directed to the character such as when your application itself becomes active.</span></span> <span data-ttu-id="3233b-123">例如，將 [ *狀態* ] 設定為 [2] 會讓字元最上層，而您的用戶端會收到使用者與該字元互動所產生的所有滑鼠和語音輸入事件。</span><span class="sxs-lookup"><span data-stu-id="3233b-123">For example, setting *State* to 2 makes the character topmost and your client receives all mouse and speech input events generated from user interaction with the character.</span></span> <span data-ttu-id="3233b-124">因此，它也會讓您的用戶端成為字元的輸入主動用戶端。</span><span class="sxs-lookup"><span data-stu-id="3233b-124">Therefore, it also makes your client the input-active client of the character.</span></span>

<span data-ttu-id="3233b-125">不過，您也可以將自己設定為字元的作用中用戶端，而不讓字元最上層，方法是將 *狀態* 設定為1。</span><span class="sxs-lookup"><span data-stu-id="3233b-125">However, you can also set yourself to be the active client for a character without making the character topmost, by setting *State* to 1.</span></span> <span data-ttu-id="3233b-126">這可讓您的用戶端在字元變成最上層時，接收導向該字元的輸入。</span><span class="sxs-lookup"><span data-stu-id="3233b-126">This enables your client to receive input directed to that character when the character becomes topmost.</span></span> <span data-ttu-id="3233b-127">同樣地，您可以將用戶端設定為不是使用中的用戶端 (不會在字元變成最上層時，藉由將 *狀態* 設為0來接收輸入) 。</span><span class="sxs-lookup"><span data-stu-id="3233b-127">Similarly, you can set your client to not be the active client (not to receive input) when the character becomes topmost, by setting *State* to 0.</span></span>

<span data-ttu-id="3233b-128">避免直接在 [**Show**](/previous-versions/visualstudio/foxpro/d79z7xxa(v=vs.71)) 方法之後呼叫此方法。</span><span class="sxs-lookup"><span data-stu-id="3233b-128">Avoid calling this method directly after a [**Show**](/previous-versions/visualstudio/foxpro/d79z7xxa(v=vs.71)) method.</span></span> <span data-ttu-id="3233b-129">**顯示** 自動設定輸入-主動用戶端。</span><span class="sxs-lookup"><span data-stu-id="3233b-129">**Show** automatically sets the input-active client.</span></span> <span data-ttu-id="3233b-130">隱藏字元時，如果在 **Show** 方法完成之前處理，[**啟動**](/previous-versions/visualstudio/foxpro/01ayxx68(v=vs.71))呼叫可能會失敗。</span><span class="sxs-lookup"><span data-stu-id="3233b-130">When the character is hidden, the [**Activate**](/previous-versions/visualstudio/foxpro/01ayxx68(v=vs.71)) call may fail if it gets processed before the **Show** method completes.</span></span>

<span data-ttu-id="3233b-131">如果您將此方法呼叫至函式，它會傳回布林值，指出方法是否成功。</span><span class="sxs-lookup"><span data-stu-id="3233b-131">If you call this method to a function, it returns a Boolean value that indicates whether the method succeeded.</span></span> <span data-ttu-id="3233b-132">當指定的字元隱藏時，嘗試以 *State* 參數設定為2時，嘗試呼叫這個方法將會失敗。</span><span class="sxs-lookup"><span data-stu-id="3233b-132">Attempting to call this method with the *State* parameter set to 2 when the specified character is hidden will fail.</span></span> <span data-ttu-id="3233b-133">同樣地，如果您將 *狀態* 設定為0，而您的應用程式是唯一的用戶端，則此呼叫會失敗，因為字元一律必須有最上層的用戶端。</span><span class="sxs-lookup"><span data-stu-id="3233b-133">Similarly, if you set *State* to 0 and your application is the only client, this call fails because a character must always have a topmost client.</span></span>


```
   Dim Genie as Object

   Sub FormLoad()

   Agent1.Characters.Load "Genie", "Genie.acs"

   Set Genie = Agent1.Characters ("Genie")

   If (Genie. Activate = True) Then
      'I'm active

   Else
      'I must be hidden or something

   End If 
   
   End Sub
```



> [!Note]  
> <span data-ttu-id="3233b-134">除非沒有載入任何其他字元或您的應用程式已經輸入主動，否則以 *狀態* 設定為1來呼叫這個方法通常不會產生 [**ActivateInput**](https://www.bing.com/search?q=**ActivateInput**) 事件。</span><span class="sxs-lookup"><span data-stu-id="3233b-134">Calling this method with *State* set to 1 does not typically generate an [**ActivateInput**](https://www.bing.com/search?q=**ActivateInput**) event unless there are no other characters loaded or your application is already input-active.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="3233b-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3233b-135">See Also</span></span>

<span data-ttu-id="3233b-136">[**ActivateInput 事件**](activateinput-event.md)， [ **DeactivateInput 事件**](deactivateinput-event.md)</span><span class="sxs-lookup"><span data-stu-id="3233b-136">[**ActivateInput event**](activateinput-event.md), [**DeactivateInput event**](deactivateinput-event.md)</span></span>


 


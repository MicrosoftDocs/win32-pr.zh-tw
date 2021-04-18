---
title: Wait 方法
description: Wait 方法
ms.assetid: 968a3f19-6953-473b-ba98-0dc93696e703
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f2e94b0f765a9861c30b254761fbc4dc2e72763
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106968488"
---
# <a name="wait-method"></a><span data-ttu-id="a34de-103">Wait 方法</span><span class="sxs-lookup"><span data-stu-id="a34de-103">Wait Method</span></span>

<span data-ttu-id="a34de-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="a34de-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="a34de-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="a34de-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="a34de-106">使指定字元的動畫佇列等候，直到指定的動畫要求完成為止。</span><span class="sxs-lookup"><span data-stu-id="a34de-106">Causes the animation queue for the specified character to wait until the specified animation request completes.</span></span>

</dd> <dt>

<span data-ttu-id="a34de-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="a34de-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="a34de-108">*代理程式 ***。 ( "*** CharacterID ***" ) 的字元。等候*** 要求*</span><span class="sxs-lookup"><span data-stu-id="a34de-108">*agent ***.Characters ("*** CharacterID ***").Wait*** Request*</span></span>



| <span data-ttu-id="a34de-109">部分</span><span class="sxs-lookup"><span data-stu-id="a34de-109">Part</span></span>      | <span data-ttu-id="a34de-110">描述</span><span class="sxs-lookup"><span data-stu-id="a34de-110">Description</span></span>                                                                     |
|-----------|---------------------------------------------------------------------------------|
| <span data-ttu-id="a34de-111">*要求*</span><span class="sxs-lookup"><span data-stu-id="a34de-111">*Request*</span></span> | <span data-ttu-id="a34de-112">指定特定動畫的 [**要求**](/windows/desktop/lwef/the-request-object) 物件。</span><span class="sxs-lookup"><span data-stu-id="a34de-112">A [**Request**](/windows/desktop/lwef/the-request-object) object specifying a particular animation..</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a34de-113">備註</span><span class="sxs-lookup"><span data-stu-id="a34de-113">Remarks</span></span>

<span data-ttu-id="a34de-114">只有當您同時支援多個 (同時) 個字元，並嘗試排序字元的互動時，才使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="a34de-114">Use this method only when you support multiple (simultaneous) characters and are trying to sequence the interaction of characters.</span></span> <span data-ttu-id="a34de-115">針對單一字元 (，每個動畫要求都會依序播放--在先前的要求完成之後 ) 。如果您有兩個字元，而且想要讓字元的動畫要求等候到其他字元的動畫完成，請將 **wait** 方法設定為其他字元的動畫 [**要求**](/windows/desktop/lwef/the-request-object) 物件。</span><span class="sxs-lookup"><span data-stu-id="a34de-115">(For a single character, each animation request is played sequentially--after the previous request completes.) If you have two characters and you want a character's animation request to wait until the other character's animation completes, set the **Wait** method to the other character's animation [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span> <span data-ttu-id="a34de-116">若要指定要求參數，您必須建立變數，並指派您要中斷的動畫要求：</span><span class="sxs-lookup"><span data-stu-id="a34de-116">To specify the request parameter, you must create a variable and assign the animation request you want to interrupt:</span></span>


```
   Dim GenieRequest 
   Dim RobbyRequest 
   Dim Genie 
   Dim Robby 

   Sub window_Onload

   Agent1.Characters.Load "Genie", "https://agent.microsoft.com/characters/v2/genie/genie.acf"
   Agent1.Characters.Load "Robby", "https://agent.microsoft.com/characters/v2/robby/robby.acf"

   Set Genie = Agent1.Characters("Genie")
   Set Robby = Agent1.Characters("Robby")

   Genie.Get "State", "Showing"
   Robby.Get "State", "Showing"

   Genie.Get "Animation", "Announce, AnnounceReturn, Pleased, _ 
      PleasedReturn"
   
   Robby.Get "Animation", "Confused, ConfusedReturn, Sad, SadReturn"

   Set Genie = Agent1.Characters ("Genie")
   Set Robby = Agent1.Characters ("Robby")

   Genie.MoveTo 100,100
   Genie.Show

   Robby.MoveTo 250,100
   Robby.Show

   Genie.Play "Announce"
   Set GenieRequest = Genie.Speak ("Why did the chicken cross the road?")
   
   Robby.Wait GenieRequest
   Robby.Play "Confused"
   Set RobbyRequest = Robby.Speak ("I don't know. Why did the chicken _
      cross the road?")
   
   Genie.Wait RobbyRequest
   Genie.Play "Pleased"
   Set GenieRequest = Genie.Speak ("To get to the other side.")
   
   Robby.Wait GenieRequest
   Robby.Play "Sad"
   Robby.Speak "I never should have asked."

   End Sub
```



<span data-ttu-id="a34de-117">您也可以使用特定的動畫要求，直接呼叫 **等候** ，以簡化程式碼。</span><span class="sxs-lookup"><span data-stu-id="a34de-117">You can also streamline your code by just calling **Wait** directly, using a specific animation request.</span></span>


```
   Robby.Wait Genie.Play "GestureRight"
```



<span data-ttu-id="a34de-118">這可避免必須明確宣告 [**Request**](/windows/desktop/lwef/the-request-object) 物件。</span><span class="sxs-lookup"><span data-stu-id="a34de-118">This avoids having to explicitly declare a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span>

 

 
---
title: 中斷方法
description: 中斷方法
ms.assetid: b8442e25-a629-47c7-acdd-1d28e74d78a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d58050e181525cc4a4b9f35ec169e92d91ab28e7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375328"
---
# <a name="interrupt-method"></a><span data-ttu-id="a2bdf-103">中斷方法</span><span class="sxs-lookup"><span data-stu-id="a2bdf-103">Interrupt Method</span></span>

<span data-ttu-id="a2bdf-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="a2bdf-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="a2bdf-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="a2bdf-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="a2bdf-106">中斷指定字元的動畫。</span><span class="sxs-lookup"><span data-stu-id="a2bdf-106">Interrupts the animation for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="a2bdf-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="a2bdf-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="a2bdf-108">\*代理程式 ***。 ( "*** CharacterID \* \* *" 的字元 ) 。中斷* \*  *要求*</span><span class="sxs-lookup"><span data-stu-id="a2bdf-108">*agent ***.Characters ("*** CharacterID\*\*\*").Interrupt*\* *Request*</span></span>



| <span data-ttu-id="a2bdf-109">部分</span><span class="sxs-lookup"><span data-stu-id="a2bdf-109">Part</span></span>      | <span data-ttu-id="a2bdf-110">描述</span><span class="sxs-lookup"><span data-stu-id="a2bdf-110">Description</span></span>                                                                  |
|-----------|------------------------------------------------------------------------------|
| <span data-ttu-id="a2bdf-111">*要求*</span><span class="sxs-lookup"><span data-stu-id="a2bdf-111">*Request*</span></span> | <span data-ttu-id="a2bdf-112">特定動畫呼叫的 [**要求**](/windows/desktop/lwef/the-request-object) 物件。</span><span class="sxs-lookup"><span data-stu-id="a2bdf-112">A [**Request**](/windows/desktop/lwef/the-request-object) object for a particular animation call.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a2bdf-113">備註</span><span class="sxs-lookup"><span data-stu-id="a2bdf-113">Remarks</span></span>

<span data-ttu-id="a2bdf-114">您可以使用這個來同步處理字元之間的動畫。</span><span class="sxs-lookup"><span data-stu-id="a2bdf-114">You can use this to sync up animation between characters.</span></span> <span data-ttu-id="a2bdf-115">例如，如果另一個字元在迴圈動畫中，此方法將會停止迴圈，並移至字元佇列中的下一個動畫。</span><span class="sxs-lookup"><span data-stu-id="a2bdf-115">For example, if another character is in a looping animation, this method will stop the loop and move to the next animation in the character's queue.</span></span> <span data-ttu-id="a2bdf-116">您無法中斷未使用 (未) 載入的字元動畫。</span><span class="sxs-lookup"><span data-stu-id="a2bdf-116">You cannot interrupt a character animation that you are not using (that you have not loaded).</span></span>

<span data-ttu-id="a2bdf-117">若要指定要求參數，您必須建立變數，並指派您要中斷的動畫要求：</span><span class="sxs-lookup"><span data-stu-id="a2bdf-117">To specify the request parameter, you must create a variable and assign the animation request you want to interrupt:</span></span>


```
   Dim GenieRequest as Object
   Dim RobbyRequest as Object
   Dim Genie as Object
   Dim Robby as Object

   Sub FormLoad()

      MyAgent1.Characters.Load "Genie", "Genie.acs"

      MyAgent1.Characters.Load "Robby", "Robby.acs"

      Set Genie = MyAgent1.Characters ("Genie")
      Set Robby = MyAgent1.Characters ("Robby")

      Genie.Show

      Genie.Speak "Just a moment"

      Set GenieRequest = Genie.Play ("Processing")

      Robby.Show
      Robby.Play "confused"
      Robby.Speak "Hey, Genie. What are you doing?"
      Robby.Interrupt GenieRequest

      Genie.Speak "I was just checking on something."

   End Sub
```



<span data-ttu-id="a2bdf-118">您無法中斷您在此方法中指定之相同字元的動畫，因為伺服器會將該字元的動畫佇列中的 **中斷** 方法排入佇列。</span><span class="sxs-lookup"><span data-stu-id="a2bdf-118">You cannot interrupt the animation of the same character you specify in this method because the server queues the **Interrupt** method in that character's animation queue.</span></span> <span data-ttu-id="a2bdf-119">因此，您只能使用插 **斷來停止** 已載入之另一個字元的動畫。</span><span class="sxs-lookup"><span data-stu-id="a2bdf-119">Therefore, you can only use **Interrupt** to halt the animation of another character you have loaded.</span></span>

<span data-ttu-id="a2bdf-120">如果您宣告物件參考，並將它設定為此方法，則會傳回 [**Request**](/windows/desktop/lwef/the-request-object) 物件。</span><span class="sxs-lookup"><span data-stu-id="a2bdf-120">If you declare an object reference and set it to this method, it returns a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span>

> [!Note]  
> <span data-ttu-id="a2bdf-121">**中斷** 不會排清字元的佇列;它會中止現有的動畫，並移至字元佇列中的下一個動畫。</span><span class="sxs-lookup"><span data-stu-id="a2bdf-121">**Interrupt** does not flush the character's queue; it halts the existing animation and moves on to the next animation in the character's queue.</span></span> <span data-ttu-id="a2bdf-122">若要停止並清除字元的佇列，請使用 [**Stop**](stop-method.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="a2bdf-122">To halt and flush a character's queue, use the [**Stop**](stop-method.md) method.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="a2bdf-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a2bdf-123">See Also</span></span>

[<span data-ttu-id="a2bdf-124">**Stop 方法**</span><span class="sxs-lookup"><span data-stu-id="a2bdf-124">**Stop method**</span></span>](stop-method.md)


 

 
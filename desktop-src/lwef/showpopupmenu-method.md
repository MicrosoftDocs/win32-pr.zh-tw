---
title: ShowPopupMenu 方法
description: ShowPopupMenu 方法
ms.assetid: 7f964d53-2594-41b1-9450-1ba7e9f85882
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0325a552cc3c1f91a64c1240964f1d0c329292c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106964957"
---
# <a name="showpopupmenu-method"></a><span data-ttu-id="ee770-103">ShowPopupMenu 方法</span><span class="sxs-lookup"><span data-stu-id="ee770-103">ShowPopupMenu Method</span></span>

<span data-ttu-id="ee770-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="ee770-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="ee770-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="ee770-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="ee770-106">顯示指定位置的字元快顯功能表。</span><span class="sxs-lookup"><span data-stu-id="ee770-106">Displays the character's pop-up menu at the specified location.</span></span>

</dd> <dt>

<span data-ttu-id="ee770-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="ee770-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="ee770-108">*代理。\*\*\*字元 (*\*\* 」CharacterID ***") 。ShowPopupMenu*** x、y\*</span><span class="sxs-lookup"><span data-stu-id="ee770-108">*agent.\*\*\*Characters("*\*\* CharacterID ***").ShowPopupMenu*** x, y\*</span></span>



| <span data-ttu-id="ee770-109">部分</span><span class="sxs-lookup"><span data-stu-id="ee770-109">Part</span></span> | <span data-ttu-id="ee770-110">描述</span><span class="sxs-lookup"><span data-stu-id="ee770-110">Description</span></span>                                                                                                                                          |
|------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee770-111">*x*</span><span class="sxs-lookup"><span data-stu-id="ee770-111">*x*</span></span>  | <span data-ttu-id="ee770-112">必要。</span><span class="sxs-lookup"><span data-stu-id="ee770-112">Required.</span></span> <span data-ttu-id="ee770-113">整數值，表示用來顯示功能表的水準 (*x*) 螢幕座標。</span><span class="sxs-lookup"><span data-stu-id="ee770-113">An integer value that indicates the horizontal (*x*) screen coordinate to display the menu.</span></span> <span data-ttu-id="ee770-114">這些座標必須以圖元為單位來指定。</span><span class="sxs-lookup"><span data-stu-id="ee770-114">These coordinates must be specified in pixels.</span></span> |
| <span data-ttu-id="ee770-115">*y*</span><span class="sxs-lookup"><span data-stu-id="ee770-115">*y*</span></span>  | <span data-ttu-id="ee770-116">必要。</span><span class="sxs-lookup"><span data-stu-id="ee770-116">Required.</span></span> <span data-ttu-id="ee770-117">整數值，指出垂直 (*y*) 螢幕座標，以顯示功能表。</span><span class="sxs-lookup"><span data-stu-id="ee770-117">An integer value that indicates the vertical (*y*) screen coordinate to display the menu.</span></span> <span data-ttu-id="ee770-118">這些座標必須以圖元為單位來指定。</span><span class="sxs-lookup"><span data-stu-id="ee770-118">These coordinates must be specified in pixels.</span></span>   |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ee770-119">備註</span><span class="sxs-lookup"><span data-stu-id="ee770-119">Remarks</span></span>

<span data-ttu-id="ee770-120">當使用者以滑鼠右鍵按一下字元時，代理程式會自動顯示該字元的快顯功能表。</span><span class="sxs-lookup"><span data-stu-id="ee770-120">Agent automatically displays the character's pop-up menu when the user right-clicks the character.</span></span> <span data-ttu-id="ee770-121">如果您將 [**AutoPopupMenu**](autopopupmenu-property.md) 設定為 **False**，則可以使用這個方法來顯示功能表。</span><span class="sxs-lookup"><span data-stu-id="ee770-121">If you set [**AutoPopupMenu**](autopopupmenu-property.md) to **False**, you can use this method to display the menu.</span></span>

<span data-ttu-id="ee770-122">功能表會保持顯示，直到使用者選取命令或顯示其他功能表為止。</span><span class="sxs-lookup"><span data-stu-id="ee770-122">The menu remains displayed until the user selects a command or displays another menu.</span></span> <span data-ttu-id="ee770-123">一次只能顯示一個快顯功能表;因此，對此方法的呼叫將會取消 (移除) 前一個功能表中。</span><span class="sxs-lookup"><span data-stu-id="ee770-123">Only one pop-up menu can be displayed at a time; therefore, calls to this method will cancel (remove) the former menu.</span></span>

<span data-ttu-id="ee770-124">只有當您的用戶端應用程式是字元的作用中用戶端時，才應該呼叫這個方法。否則會失敗。</span><span class="sxs-lookup"><span data-stu-id="ee770-124">This method should be called only when your client application is the active client of the character; otherwise it fails.</span></span> <span data-ttu-id="ee770-125">若要判斷這個方法是否成功，您可以呼叫它作為函式，它會傳回布林值，指出方法是否成功。</span><span class="sxs-lookup"><span data-stu-id="ee770-125">To determine the success of this method you can call it as a function and it will return a Boolean value indicating whether the method succeeded.</span></span>


```
   If Genie.ShowPopupMenu (10,10) = True Then
      ' The menu will be displayed

   Else 
      ' The menu will not be displayed

   End If
```



## <a name="see-also"></a><span data-ttu-id="ee770-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ee770-126">See Also</span></span>

[<span data-ttu-id="ee770-127">**AutoPopupMenu 屬性**</span><span class="sxs-lookup"><span data-stu-id="ee770-127">**AutoPopupMenu property**</span></span>](autopopupmenu-property.md)


 

 





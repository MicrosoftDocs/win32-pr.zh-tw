---
title: 移動事件
description: 移動事件
ms.assetid: 973e9e68-edbb-4741-b50e-57db96712df8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31facb1d57b807fb0322783a291b77ef5a7c1487
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840092"
---
# <a name="move-event"></a><span data-ttu-id="e8542-103">移動事件</span><span class="sxs-lookup"><span data-stu-id="e8542-103">Move Event</span></span>

<span data-ttu-id="e8542-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="e8542-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="e8542-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="e8542-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="e8542-106">移動字元時發生。</span><span class="sxs-lookup"><span data-stu-id="e8542-106">Occurs when a character is moved.</span></span>

</dd> <dt>

<span data-ttu-id="e8542-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="e8542-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="e8542-108">**子\*\*\*代理程式* \_ **移動 (byval** *CharacterID*， **byval** *X*， **byval** *Y*， **byval** *原因 \* \* \* )**</span><span class="sxs-lookup"><span data-stu-id="e8542-108">**Sub** *agent*\_**Move (ByVal** *CharacterID*, **ByVal** *X*, **ByVal** *Y*, **ByVal** *Cause\*\*\*)*\*</span></span>



| <span data-ttu-id="e8542-109">部分</span><span class="sxs-lookup"><span data-stu-id="e8542-109">Part</span></span>          | <span data-ttu-id="e8542-110">描述</span><span class="sxs-lookup"><span data-stu-id="e8542-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                   |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8542-111">*CharacterID*</span><span class="sxs-lookup"><span data-stu-id="e8542-111">*CharacterID*</span></span> | <span data-ttu-id="e8542-112">傳回已移動之字元的識別碼。</span><span class="sxs-lookup"><span data-stu-id="e8542-112">Returns the ID of the character that moved.</span></span>                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="e8542-113">*X*</span><span class="sxs-lookup"><span data-stu-id="e8542-113">*X*</span></span>           | <span data-ttu-id="e8542-114">以圖元為單位，傳回字元框架新位置上邊緣的 x 座標 (（以圖元為單位) ）。</span><span class="sxs-lookup"><span data-stu-id="e8542-114">Returns the x-coordinate (in pixels) of the top edge of character frame's new location as an integer.</span></span>                                                                                                                                                                                                                                         |
| <span data-ttu-id="e8542-115">*Y*</span><span class="sxs-lookup"><span data-stu-id="e8542-115">*Y*</span></span>           | <span data-ttu-id="e8542-116">以圖元為單位，傳回字元框架的新位置左邊緣的 y 座標 (（以圖元為單位) ）。</span><span class="sxs-lookup"><span data-stu-id="e8542-116">Returns the y-coordinate (in pixels) of the left edge of character frame's new location as an integer.</span></span>                                                                                                                                                                                                                                        |
| <span data-ttu-id="e8542-117">*原因*</span><span class="sxs-lookup"><span data-stu-id="e8542-117">*Cause*</span></span>       | <span data-ttu-id="e8542-118">傳回值，這個值會指出造成字元移動的原因。</span><span class="sxs-lookup"><span data-stu-id="e8542-118">Returns a value that indicates what caused the character to move.</span></span> <span data-ttu-id="e8542-119">1使用者拖曳字元。</span><span class="sxs-lookup"><span data-stu-id="e8542-119">1 The user dragged the character.</span></span><br/> <span data-ttu-id="e8542-120">2您的用戶端應用程式移動字元。</span><span class="sxs-lookup"><span data-stu-id="e8542-120">2 Your client application moved the character.</span></span><br/> <span data-ttu-id="e8542-121">3其他用戶端應用程式移動字元。</span><span class="sxs-lookup"><span data-stu-id="e8542-121">3 Another client application moved the character.</span></span><br/> <span data-ttu-id="e8542-122">4代理程式伺服器移動字元，以在螢幕解析度變更之後讓它保持在畫面上。</span><span class="sxs-lookup"><span data-stu-id="e8542-122">4 The Agent server moved the character to keep it onscreen after a screen resolution change.</span></span><br/> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="e8542-123">備註</span><span class="sxs-lookup"><span data-stu-id="e8542-123">Remarks</span></span>

<span data-ttu-id="e8542-124">當使用者或應用程式變更字元的位置時，就會發生此事件。</span><span class="sxs-lookup"><span data-stu-id="e8542-124">This event occurs when the user or an application changes the character's position.</span></span> <span data-ttu-id="e8542-125">座標與畫面的左上角有關。</span><span class="sxs-lookup"><span data-stu-id="e8542-125">Coordinates are relevant to the upper left corner of the screen.</span></span> <span data-ttu-id="e8542-126">此事件只會傳送給已載入字元)  (應用程式的字元用戶端。</span><span class="sxs-lookup"><span data-stu-id="e8542-126">This event is sent only to the clients of the character (applications that have loaded the character).</span></span>

<span data-ttu-id="e8542-127">**另請參閱**</span><span class="sxs-lookup"><span data-stu-id="e8542-127">**See Also**</span></span>

<span data-ttu-id="e8542-128">[**MoveCause 屬性**](movecause-property.md)， [**大小事件**](size-event.md)</span><span class="sxs-lookup"><span data-stu-id="e8542-128">[**MoveCause property**](movecause-property.md), [**Size event**](size-event.md)</span></span>

 

 






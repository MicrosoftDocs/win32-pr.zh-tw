---
title: AutoPopupMenu 屬性
description: AutoPopupMenu 屬性
ms.assetid: 499092cb-0990-4edb-915c-12e3011de142
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25d4ebfc559c88c3750a338f30b5dee4aad66ec3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301644"
---
# <a name="autopopupmenu-property"></a><span data-ttu-id="fd059-103">AutoPopupMenu 屬性</span><span class="sxs-lookup"><span data-stu-id="fd059-103">AutoPopupMenu Property</span></span>

<span data-ttu-id="fd059-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="fd059-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="fd059-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="fd059-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="fd059-106">傳回或設定以滑鼠右鍵按一下字元或其工作列圖示，是否會自動顯示字元的快顯功能表。</span><span class="sxs-lookup"><span data-stu-id="fd059-106">Returns or sets whether right-clicking the character or its taskbar icon automatically displays the character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="fd059-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="fd059-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="fd059-108">*代理程式。\*\*\*字元 \* \*\*\*\* \* \* (」CharacterID \* \* \* ) 。AutoPopupMenu* \*  \[  =  *布林值*\]</span><span class="sxs-lookup"><span data-stu-id="fd059-108">*agent.\*\*\*Characters\*\*\*\*("*\*\* CharacterID\***").AutoPopupMenu** \[ = *boolean*\]</span></span>



| <span data-ttu-id="fd059-109">部分</span><span class="sxs-lookup"><span data-stu-id="fd059-109">Part</span></span>      | <span data-ttu-id="fd059-110">描述</span><span class="sxs-lookup"><span data-stu-id="fd059-110">Description</span></span>                                                                                                                                                                                                                                           |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd059-111">*boolean*</span><span class="sxs-lookup"><span data-stu-id="fd059-111">*boolean*</span></span> | <span data-ttu-id="fd059-112">布林運算式，指定伺服器是否在按一下滑鼠右鍵時，自動顯示該字元的快顯功能表。</span><span class="sxs-lookup"><span data-stu-id="fd059-112">A Boolean expression specifying whether the server automatically displays the character's pop-up menu on right-click.</span></span> <span data-ttu-id="fd059-113">**True** (預設) 在滑鼠右鍵按一下時顯示功能表。</span><span class="sxs-lookup"><span data-stu-id="fd059-113">**True** (Default) Displays the menu on right-click.</span></span> <br/> <span data-ttu-id="fd059-114">**False** 在滑鼠右鍵按一下時，不會顯示功能表。</span><span class="sxs-lookup"><span data-stu-id="fd059-114">**False** Does not display the menu on right-click.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fd059-115">備註</span><span class="sxs-lookup"><span data-stu-id="fd059-115">Remarks</span></span>

<span data-ttu-id="fd059-116">藉由將這個屬性設定為 **False**，您就可以建立自己的功能表處理行為。</span><span class="sxs-lookup"><span data-stu-id="fd059-116">By setting this property to **False**, you can create your own menu-handling behavior.</span></span> <span data-ttu-id="fd059-117">若要在將這個屬性設定為 **False** 之後顯示功能表，請使用 [**ShowPopupMenu**](showpopupmenu-method.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="fd059-117">To display the menu after setting this property to **False**, use the [**ShowPopupMenu**](showpopupmenu-method.md) method.</span></span>

<span data-ttu-id="fd059-118">這個屬性只適用于您的用戶端應用程式使用的字元;此設定不會影響用戶端應用程式中其他字元或其他字元的用戶端。</span><span class="sxs-lookup"><span data-stu-id="fd059-118">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="fd059-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fd059-119">See Also</span></span>

[<span data-ttu-id="fd059-120">**ShowPopupMenu 方法**</span><span class="sxs-lookup"><span data-stu-id="fd059-120">**ShowPopupMenu method**</span></span>](showpopupmenu-method.md)


 

 






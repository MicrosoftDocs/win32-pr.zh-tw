---
title: MoveCause 屬性
description: MoveCause 屬性
ms.assetid: 8f78a6da-8498-4a39-a4b9-5ab7a43d97f5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfc7f91d068befa2b919c04818c46dbc1a48faa0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840095"
---
# <a name="movecause-property"></a><span data-ttu-id="0f766-103">MoveCause 屬性</span><span class="sxs-lookup"><span data-stu-id="0f766-103">MoveCause Property</span></span>

<span data-ttu-id="0f766-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="0f766-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="0f766-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="0f766-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="0f766-106">傳回整數值，指定造成字元上一次移動的原因。</span><span class="sxs-lookup"><span data-stu-id="0f766-106">Returns an integer value that specifies what caused the character's last move.</span></span>

</dd> <dt>

<span data-ttu-id="0f766-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="0f766-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="0f766-108">*代理程式*。**( "***CharacterID***" ) 的字元。MoveCause**</span><span class="sxs-lookup"><span data-stu-id="0f766-108">*agent*.**Characters("***CharacterID***").MoveCause**</span></span>



| <span data-ttu-id="0f766-109">值</span><span class="sxs-lookup"><span data-stu-id="0f766-109">Value</span></span> | <span data-ttu-id="0f766-110">描述</span><span class="sxs-lookup"><span data-stu-id="0f766-110">Description</span></span>                                                                                |
|-------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f766-111">0</span><span class="sxs-lookup"><span data-stu-id="0f766-111">0</span></span>     | <span data-ttu-id="0f766-112">尚未移動字元。</span><span class="sxs-lookup"><span data-stu-id="0f766-112">The character has not been moved.</span></span>                                                          |
| <span data-ttu-id="0f766-113">1</span><span class="sxs-lookup"><span data-stu-id="0f766-113">1</span></span>     | <span data-ttu-id="0f766-114">使用者移動字元。</span><span class="sxs-lookup"><span data-stu-id="0f766-114">The user moved the character.</span></span>                                                              |
| <span data-ttu-id="0f766-115">2</span><span class="sxs-lookup"><span data-stu-id="0f766-115">2</span></span>     | <span data-ttu-id="0f766-116">您的應用程式移動了該字元。</span><span class="sxs-lookup"><span data-stu-id="0f766-116">Your application moved the character.</span></span>                                                      |
| <span data-ttu-id="0f766-117">3</span><span class="sxs-lookup"><span data-stu-id="0f766-117">3</span></span>     | <span data-ttu-id="0f766-118">另一個用戶端應用程式移動字元。</span><span class="sxs-lookup"><span data-stu-id="0f766-118">Another client application moved the character.</span></span>                                            |
| <span data-ttu-id="0f766-119">4</span><span class="sxs-lookup"><span data-stu-id="0f766-119">4</span></span>     | <span data-ttu-id="0f766-120">代理程式伺服器移動字元，以在螢幕解析度變更之後讓它保持在畫面上。</span><span class="sxs-lookup"><span data-stu-id="0f766-120">The Agent server moved the character to keep it onscreen after a screen resolution change.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0f766-121">備註</span><span class="sxs-lookup"><span data-stu-id="0f766-121">Remarks</span></span>

<span data-ttu-id="0f766-122">當有多個應用程式正在共用 (載入) 相同的字元時，您可以使用這個屬性來判斷造成字元移動的原因。</span><span class="sxs-lookup"><span data-stu-id="0f766-122">You can use this property to determine what caused the character to move, when more than one application is sharing (has loaded) the same character.</span></span> <span data-ttu-id="0f766-123">這些值與 [**移動**](move-event.md) 事件所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="0f766-123">These values are the same as those returned by the [**Move**](move-event.md) event.</span></span>

## <a name="see-also"></a><span data-ttu-id="0f766-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0f766-124">See Also</span></span>

<span data-ttu-id="0f766-125">[**移動事件**](move-event.md)， [ **MoveTo 方法**](moveto-method.md)</span><span class="sxs-lookup"><span data-stu-id="0f766-125">[**Move event**](move-event.md), [**MoveTo method**](moveto-method.md)</span></span>


 

 





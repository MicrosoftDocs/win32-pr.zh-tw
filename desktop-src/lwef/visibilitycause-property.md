---
title: VisibilityCause 屬性
description: VisibilityCause 屬性
ms.assetid: 106574ef-af5f-44cf-9efb-9e6da19ebc1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a6e21e2cda201f8d04837d2b10efc757b93f824
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372226"
---
# <a name="visibilitycause-property"></a><span data-ttu-id="447c4-103">VisibilityCause 屬性</span><span class="sxs-lookup"><span data-stu-id="447c4-103">VisibilityCause Property</span></span>

<span data-ttu-id="447c4-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="447c4-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="447c4-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="447c4-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="447c4-106">傳回整數值，指定造成字元可見狀態的原因。</span><span class="sxs-lookup"><span data-stu-id="447c4-106">Returns an integer value that specifies what caused the character's visible state.</span></span>

</dd> <dt>

<span data-ttu-id="447c4-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="447c4-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="447c4-108">*代理程式*。**( "***CharacterID***" ) 的字元。VisibilityCause**</span><span class="sxs-lookup"><span data-stu-id="447c4-108">*agent*.**Characters("***CharacterID***").VisibilityCause**</span></span>



| <span data-ttu-id="447c4-109">值</span><span class="sxs-lookup"><span data-stu-id="447c4-109">Value</span></span> | <span data-ttu-id="447c4-110">描述</span><span class="sxs-lookup"><span data-stu-id="447c4-110">Description</span></span>                                                                                                  |
|-------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="447c4-111">0</span><span class="sxs-lookup"><span data-stu-id="447c4-111">0</span></span>     | <span data-ttu-id="447c4-112">未顯示字元。</span><span class="sxs-lookup"><span data-stu-id="447c4-112">The character has not been shown.</span></span>                                                                            |
| <span data-ttu-id="447c4-113">1</span><span class="sxs-lookup"><span data-stu-id="447c4-113">1</span></span>     | <span data-ttu-id="447c4-114">使用者會在字元的工作列圖示快顯功能表上使用命令或使用語音輸入來隱藏字元。</span><span class="sxs-lookup"><span data-stu-id="447c4-114">User hid the character using the command on the character's taskbar icon pop-up menu or using speech input..</span></span> |
| <span data-ttu-id="447c4-115">2</span><span class="sxs-lookup"><span data-stu-id="447c4-115">2</span></span>     | <span data-ttu-id="447c4-116">使用者顯示字元。</span><span class="sxs-lookup"><span data-stu-id="447c4-116">The user showed the character.</span></span>                                                                               |
| <span data-ttu-id="447c4-117">3</span><span class="sxs-lookup"><span data-stu-id="447c4-117">3</span></span>     | <span data-ttu-id="447c4-118">您的應用程式會隱藏該字元。</span><span class="sxs-lookup"><span data-stu-id="447c4-118">Your application hid the character.</span></span>                                                                          |
| <span data-ttu-id="447c4-119">4</span><span class="sxs-lookup"><span data-stu-id="447c4-119">4</span></span>     | <span data-ttu-id="447c4-120">您的應用程式會顯示該字元。</span><span class="sxs-lookup"><span data-stu-id="447c4-120">Your application showed the character.</span></span>                                                                       |
| <span data-ttu-id="447c4-121">5</span><span class="sxs-lookup"><span data-stu-id="447c4-121">5</span></span>     | <span data-ttu-id="447c4-122">另一個用戶端應用程式會隱藏該字元。</span><span class="sxs-lookup"><span data-stu-id="447c4-122">Another client application hid the character.</span></span>                                                                |
| <span data-ttu-id="447c4-123">6</span><span class="sxs-lookup"><span data-stu-id="447c4-123">6</span></span>     | <span data-ttu-id="447c4-124">另一個用戶端應用程式會顯示該字元。</span><span class="sxs-lookup"><span data-stu-id="447c4-124">Another client application showed the character.</span></span>                                                             |
| <span data-ttu-id="447c4-125">7</span><span class="sxs-lookup"><span data-stu-id="447c4-125">7</span></span>     | <span data-ttu-id="447c4-126">使用者會使用字元快顯功能表上的命令，將字元隱藏起來。</span><span class="sxs-lookup"><span data-stu-id="447c4-126">The user hid the character using the command on the character's pop-up menu.</span></span>                                 |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="447c4-127">備註</span><span class="sxs-lookup"><span data-stu-id="447c4-127">Remarks</span></span>

<span data-ttu-id="447c4-128">您可以使用這個屬性來判斷當有多個應用程式正在共用 (載入) 相同字元時，造成字元移動的原因。</span><span class="sxs-lookup"><span data-stu-id="447c4-128">You can use this property to determine what caused the character to move when more than one application is sharing (has loaded) the same character.</span></span> <span data-ttu-id="447c4-129">這些值與 [**顯示**](show-event.md) 和 [**隱藏**](hide-event.md) 事件所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="447c4-129">These values are the same as those returned by the [**Show**](show-event.md) and [**Hide**](hide-event.md) events.</span></span>

## <a name="see-also"></a><span data-ttu-id="447c4-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="447c4-130">See Also</span></span>

<span data-ttu-id="447c4-131">[**隱藏事件**](hide-event.md)、 [**顯示事件**](show-event.md)、 [**隱藏方法**](hide-method.md)、 [**顯示方法**](show-method.md)</span><span class="sxs-lookup"><span data-stu-id="447c4-131">[**Hide event**](hide-event.md), [**Show event**](show-event.md), [**Hide method**](hide-method.md), [**Show method**](show-method.md)</span></span>


 

 





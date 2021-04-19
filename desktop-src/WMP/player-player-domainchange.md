---
title: DomainChange 事件
description: 當 DVD 網域變更時，就會發生 DomainChange 事件。 |DomainChange 事件
ms.assetid: 01965492-276e-4d30-99eb-767e0776b423
keywords:
- DomainChange 事件 Windows Media Player
- DomainChange 事件 Windows Media Player，Player 類別
- Player 類別 Windows Media Player，DomainChange 事件
topic_type:
- apiref
api_name:
- Player.DomainChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa9637913451aa5bba937906130899c46e0bd34d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989859"
---
# <a name="playerdomainchange-event"></a><span data-ttu-id="2cd58-107">DomainChange 事件</span><span class="sxs-lookup"><span data-stu-id="2cd58-107">Player.DomainChange event</span></span>

<span data-ttu-id="2cd58-108">當 DVD 網域變更時，就會發生 **DomainChange** 事件。</span><span class="sxs-lookup"><span data-stu-id="2cd58-108">The **DomainChange** event occurs when the DVD domain changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cd58-109">語法</span><span class="sxs-lookup"><span data-stu-id="2cd58-109">Syntax</span></span>


```JScript
Player.DomainChange(
  strDomain
)
```



## <a name="parameters"></a><span data-ttu-id="2cd58-110">參數</span><span class="sxs-lookup"><span data-stu-id="2cd58-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2cd58-111">*strDomain*</span><span class="sxs-lookup"><span data-stu-id="2cd58-111">*strDomain*</span></span> 
</dt> <dd>

<span data-ttu-id="2cd58-112">表示新網域的 **字串**。</span><span class="sxs-lookup"><span data-stu-id="2cd58-112">**String** indicating the new domain.</span></span> <span data-ttu-id="2cd58-113">包含下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="2cd58-113">Contains one of the following values.</span></span>



| <span data-ttu-id="2cd58-114">String</span><span class="sxs-lookup"><span data-stu-id="2cd58-114">String</span></span>            | <span data-ttu-id="2cd58-115">Description</span><span class="sxs-lookup"><span data-stu-id="2cd58-115">Description</span></span>                                                          |
|-------------------|----------------------------------------------------------------------|
| <span data-ttu-id="2cd58-116">firstplay</span><span class="sxs-lookup"><span data-stu-id="2cd58-116">firstplay</span></span>         | <span data-ttu-id="2cd58-117">執行 DVD 光碟的預設初始化。</span><span class="sxs-lookup"><span data-stu-id="2cd58-117">Performing default initialization of a DVD disc.</span></span>                     |
| <span data-ttu-id="2cd58-118">videoManagerMenu</span><span class="sxs-lookup"><span data-stu-id="2cd58-118">videoManagerMenu</span></span>  | <span data-ttu-id="2cd58-119">顯示整個光碟的功能表。也稱為根功能表或 topMenu。</span><span class="sxs-lookup"><span data-stu-id="2cd58-119">Displaying menus for whole disc. Also known as Root Menu or topMenu.</span></span> |
| <span data-ttu-id="2cd58-120">videoTitleSetMenu</span><span class="sxs-lookup"><span data-stu-id="2cd58-120">videoTitleSetMenu</span></span> | <span data-ttu-id="2cd58-121">顯示目前標題集的功能表。</span><span class="sxs-lookup"><span data-stu-id="2cd58-121">Displaying menus for current title set.</span></span> <span data-ttu-id="2cd58-122">也稱為 titleMenu。</span><span class="sxs-lookup"><span data-stu-id="2cd58-122">Also known as titleMenu.</span></span>     |
| <span data-ttu-id="2cd58-123">title</span><span class="sxs-lookup"><span data-stu-id="2cd58-123">title</span></span>             | <span data-ttu-id="2cd58-124">顯示目前的標題。</span><span class="sxs-lookup"><span data-stu-id="2cd58-124">Displaying the current title.</span></span>                                        |
| <span data-ttu-id="2cd58-125">stop</span><span class="sxs-lookup"><span data-stu-id="2cd58-125">stop</span></span>              | <span data-ttu-id="2cd58-126">DVD 導覽器位於 DVD 停止網域中。</span><span class="sxs-lookup"><span data-stu-id="2cd58-126">The DVD Navigator is in the DVD Stop domain.</span></span>                         |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2cd58-127">傳回值</span><span class="sxs-lookup"><span data-stu-id="2cd58-127">Return value</span></span>

<span data-ttu-id="2cd58-128">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="2cd58-128">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2cd58-129">備註</span><span class="sxs-lookup"><span data-stu-id="2cd58-129">Remarks</span></span>

<span data-ttu-id="2cd58-130">事件參數的值是由 Windows Media Player 指定，而且可以使用指定的參數名稱，存取或傳遞至匯入之 JScript 檔案中的方法。</span><span class="sxs-lookup"><span data-stu-id="2cd58-130">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="2cd58-131">此參數名稱的類型必須完全如所示，包括大小寫。</span><span class="sxs-lookup"><span data-stu-id="2cd58-131">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="2cd58-132">**Windows Media Player 10** 行動裝置版：不支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="2cd58-132">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="2cd58-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="2cd58-133">Requirements</span></span>



| <span data-ttu-id="2cd58-134">需求</span><span class="sxs-lookup"><span data-stu-id="2cd58-134">Requirement</span></span> | <span data-ttu-id="2cd58-135">值</span><span class="sxs-lookup"><span data-stu-id="2cd58-135">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2cd58-136">版本</span><span class="sxs-lookup"><span data-stu-id="2cd58-136">Version</span></span><br/> | <span data-ttu-id="2cd58-137">適用于 Windows XP 或更新版本的 Windows Media Player。</span><span class="sxs-lookup"><span data-stu-id="2cd58-137">Windows Media Player for Windows XP or later.</span></span><br/>                           |
| <span data-ttu-id="2cd58-138">DLL</span><span class="sxs-lookup"><span data-stu-id="2cd58-138">DLL</span></span><br/>     | <dl> <span data-ttu-id="2cd58-139"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2cd58-139"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2cd58-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2cd58-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cd58-141">**DVD 物件**</span><span class="sxs-lookup"><span data-stu-id="2cd58-141">**DVD Object**</span></span>](dvd-object.md)
</dt> <dt>

[<span data-ttu-id="2cd58-142">**Player 物件**</span><span class="sxs-lookup"><span data-stu-id="2cd58-142">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 






---
title: OnColorChange 事件
description: 請注意，本主題將說明針對線上商店使用而設計的功能。 |OnColorChange 事件
ms.assetid: f2cd44b1-c813-479b-b847-96ddb9572697
keywords:
- External. OnColorChange 事件 Windows Media Player
topic_type:
- apiref
api_name:
- External.OnColorChange Event
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 029c8bb860443ed026737c7413be2bed8862c6d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985567"
---
# <a name="externaloncolorchange-event"></a><span data-ttu-id="8147e-105">OnColorChange 事件</span><span class="sxs-lookup"><span data-stu-id="8147e-105">External.OnColorChange Event</span></span>

> [!Note]  
> <span data-ttu-id="8147e-106">本主題說明針對線上商店使用而設計的功能。</span><span class="sxs-lookup"><span data-stu-id="8147e-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="8147e-107">不支援在線上商店的內容之外使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="8147e-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="8147e-108">當 Windows Media Player 使用者介面的色彩變更時，就會發生 **OnColorChange** 事件。</span><span class="sxs-lookup"><span data-stu-id="8147e-108">The **OnColorChange** event occurs when the color of the Windows Media Player user interface changes.</span></span>

``` syntax
window.external.OnColorChange = FunctionName
```

## <a name="possible-values"></a><span data-ttu-id="8147e-109">可能的值</span><span class="sxs-lookup"><span data-stu-id="8147e-109">Possible Values</span></span>

<span data-ttu-id="8147e-110">這是唯讀屬性，它會指定腳本中的函式名稱，此函式會在事件發生時 Windows Media Player 呼叫。</span><span class="sxs-lookup"><span data-stu-id="8147e-110">This is a write-only property that specifies the name of the function in script that Windows Media Player calls when the event occurs.</span></span>

## <a name="parameters"></a><span data-ttu-id="8147e-111">參數</span><span class="sxs-lookup"><span data-stu-id="8147e-111">Parameters</span></span>

<span data-ttu-id="8147e-112">處理此事件的函式不會使用任何參數。</span><span class="sxs-lookup"><span data-stu-id="8147e-112">The function that handles this event takes no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="8147e-113">備註</span><span class="sxs-lookup"><span data-stu-id="8147e-113">Remarks</span></span>

<span data-ttu-id="8147e-114">使用者可以變更 Windows Media Player 使用者介面的色彩。</span><span class="sxs-lookup"><span data-stu-id="8147e-114">Users can change the color of the Windows Media Player user interface.</span></span> <span data-ttu-id="8147e-115">您可以使用此事件來自訂您的託管網頁外觀，以符合播放程式。</span><span class="sxs-lookup"><span data-stu-id="8147e-115">You can use this event to customize the appearance of your hosted webpage to match the Player.</span></span>

## <a name="requirements"></a><span data-ttu-id="8147e-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="8147e-116">Requirements</span></span>



| <span data-ttu-id="8147e-117">需求</span><span class="sxs-lookup"><span data-stu-id="8147e-117">Requirement</span></span> | <span data-ttu-id="8147e-118">值</span><span class="sxs-lookup"><span data-stu-id="8147e-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8147e-119">版本</span><span class="sxs-lookup"><span data-stu-id="8147e-119">Version</span></span><br/> | <span data-ttu-id="8147e-120">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="8147e-120">Windows Media Player 9 Series or later</span></span><br/>                                  |
| <span data-ttu-id="8147e-121">DLL</span><span class="sxs-lookup"><span data-stu-id="8147e-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="8147e-122"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8147e-122"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8147e-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8147e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8147e-124">**類型2線上商店的外部物件**</span><span class="sxs-lookup"><span data-stu-id="8147e-124">**External Object for Type 2 Online Stores**</span></span>](external-object-for-type-2-online-stores.md)
</dt> </dl>

 

 






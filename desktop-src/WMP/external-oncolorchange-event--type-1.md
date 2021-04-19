---
title: 'OnColorChange 事件 (類型 1) '
description: '請注意，本主題將說明針對線上商店使用而設計的功能。 |OnColorChange 事件 (類型 1) '
ms.assetid: 45e6ec4a-e680-4d50-8fb7-410f12383eef
keywords:
- OnColorChange 事件 (類型 1) Windows Media Player
topic_type:
- apiref
api_name:
- External.OnColorChange Event (Type 1)
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11805cc154c60b8a765f46041f74d40929df418d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990750"
---
# <a name="externaloncolorchange-event-type-1"></a><span data-ttu-id="a28af-105">OnColorChange 事件 (類型 1) </span><span class="sxs-lookup"><span data-stu-id="a28af-105">External.OnColorChange Event (Type 1)</span></span>

> [!Note]  
> <span data-ttu-id="a28af-106">本主題說明針對線上商店使用而設計的功能。</span><span class="sxs-lookup"><span data-stu-id="a28af-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="a28af-107">不支援在線上商店的內容之外使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="a28af-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="a28af-108">當 Windows Media Player 使用者介面的色彩變更時，就會發生 **OnColorChange** 事件。</span><span class="sxs-lookup"><span data-stu-id="a28af-108">The **OnColorChange** event occurs when the color of the Windows Media Player user interface changes.</span></span>

``` syntax
window.external.OnColorChange = FunctionName
```

## <a name="possible-values"></a><span data-ttu-id="a28af-109">可能的值</span><span class="sxs-lookup"><span data-stu-id="a28af-109">Possible Values</span></span>

<span data-ttu-id="a28af-110">這是唯讀屬性，它會指定腳本中的函式名稱，此函式會在事件發生時 Windows Media Player 呼叫。</span><span class="sxs-lookup"><span data-stu-id="a28af-110">This is a write-only property that specifies the name of the function in script that Windows Media Player calls when the event occurs.</span></span>

## <a name="parameters"></a><span data-ttu-id="a28af-111">參數</span><span class="sxs-lookup"><span data-stu-id="a28af-111">Parameters</span></span>

<span data-ttu-id="a28af-112">處理此事件的函式不會使用任何參數。</span><span class="sxs-lookup"><span data-stu-id="a28af-112">The function that handles this event takes no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="a28af-113">備註</span><span class="sxs-lookup"><span data-stu-id="a28af-113">Remarks</span></span>

<span data-ttu-id="a28af-114">使用者可以變更 Windows Media Player 使用者介面的色彩。</span><span class="sxs-lookup"><span data-stu-id="a28af-114">Users can change the color of the Windows Media Player user interface.</span></span> <span data-ttu-id="a28af-115">您可以使用此事件來自訂您的託管網頁外觀，以符合播放程式。</span><span class="sxs-lookup"><span data-stu-id="a28af-115">You can use this event to customize the appearance of your hosted webpage to match the Player.</span></span>

## <a name="requirements"></a><span data-ttu-id="a28af-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="a28af-116">Requirements</span></span>



| <span data-ttu-id="a28af-117">需求</span><span class="sxs-lookup"><span data-stu-id="a28af-117">Requirement</span></span> | <span data-ttu-id="a28af-118">值</span><span class="sxs-lookup"><span data-stu-id="a28af-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a28af-119">版本</span><span class="sxs-lookup"><span data-stu-id="a28af-119">Version</span></span><br/> | <span data-ttu-id="a28af-120">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="a28af-120">Windows Media Player 9 Series or later</span></span><br/>                                  |
| <span data-ttu-id="a28af-121">DLL</span><span class="sxs-lookup"><span data-stu-id="a28af-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="a28af-122"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a28af-122"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a28af-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a28af-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a28af-124">**類型1線上商店的外部物件**</span><span class="sxs-lookup"><span data-stu-id="a28af-124">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 






---
title: MarkerHit 事件
description: 當到達標記時，就會發生 MarkerHit 事件。 |MarkerHit 事件
ms.assetid: c97aff61-6f06-4589-a75b-ac2af340cb1d
keywords:
- MarkerHit 事件 Windows Media Player
- MarkerHit 事件 Windows Media Player，Player 類別
- Player 類別 Windows Media Player，MarkerHit 事件
topic_type:
- apiref
api_name:
- Player.MarkerHit
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cce6b9ca7c103e9a9e9151a7ff0467a59786b1e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000724"
---
# <a name="playermarkerhit-event"></a><span data-ttu-id="c3886-107">MarkerHit 事件</span><span class="sxs-lookup"><span data-stu-id="c3886-107">Player.MarkerHit event</span></span>

<span data-ttu-id="c3886-108">當到達標記時，就會發生 **MarkerHit** 事件。</span><span class="sxs-lookup"><span data-stu-id="c3886-108">The **MarkerHit** event occurs when a marker is reached.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3886-109">語法</span><span class="sxs-lookup"><span data-stu-id="c3886-109">Syntax</span></span>


```JScript
Player.MarkerHit(
  MarkerNum
)
```



## <a name="parameters"></a><span data-ttu-id="c3886-110">參數</span><span class="sxs-lookup"><span data-stu-id="c3886-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3886-111">*MarkerNum*</span><span class="sxs-lookup"><span data-stu-id="c3886-111">*MarkerNum*</span></span> 
</dt> <dd>

<span data-ttu-id="c3886-112">**Number** (**Long**) ，表示已點擊的標記數目。</span><span class="sxs-lookup"><span data-stu-id="c3886-112">**Number** (**long**) indicating the number of the marker that was hit.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3886-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="c3886-113">Return value</span></span>

<span data-ttu-id="c3886-114">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="c3886-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3886-115">備註</span><span class="sxs-lookup"><span data-stu-id="c3886-115">Remarks</span></span>

<span data-ttu-id="c3886-116">事件參數的值是由 Windows Media Player 指定，而且可以使用指定的參數名稱，存取或傳遞至匯入之 JScript 檔案中的方法。</span><span class="sxs-lookup"><span data-stu-id="c3886-116">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="c3886-117">此參數名稱的類型必須完全如所示，包括大小寫。</span><span class="sxs-lookup"><span data-stu-id="c3886-117">This parameter name must be typed exactly as shown, including capitalization.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3886-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="c3886-118">Requirements</span></span>



| <span data-ttu-id="c3886-119">需求</span><span class="sxs-lookup"><span data-stu-id="c3886-119">Requirement</span></span> | <span data-ttu-id="c3886-120">值</span><span class="sxs-lookup"><span data-stu-id="c3886-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c3886-121">版本</span><span class="sxs-lookup"><span data-stu-id="c3886-121">Version</span></span><br/> | <span data-ttu-id="c3886-122">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="c3886-122">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="c3886-123">DLL</span><span class="sxs-lookup"><span data-stu-id="c3886-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="c3886-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c3886-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3886-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c3886-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3886-126">**Player 物件**</span><span class="sxs-lookup"><span data-stu-id="c3886-126">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 






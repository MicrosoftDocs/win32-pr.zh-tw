---
title: CdromMediaChange 事件
description: 從 CD 或 DVD 光碟機插入或退出 CD 或 DVD 時，就會發生 CdromMediaChange 事件。 |CdromMediaChange 事件
ms.assetid: d31a791a-55e5-49ee-bfe5-7488277e3fda
keywords:
- CdromMediaChange 事件 Windows Media Player
- CdromMediaChange 事件 Windows Media Player，Player 類別
- Player 類別 Windows Media Player，CdromMediaChange 事件
topic_type:
- apiref
api_name:
- Player.CdromMediaChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c3125235d5f8d19963b85284e7dbe40c7af408d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995697"
---
# <a name="playercdrommediachange-event"></a><span data-ttu-id="48573-107">CdromMediaChange 事件</span><span class="sxs-lookup"><span data-stu-id="48573-107">Player.CdromMediaChange event</span></span>

<span data-ttu-id="48573-108">從 CD 或 DVD 光碟機插入或退出 CD 或 DVD 時，就會發生 **CdromMediaChange** 事件。</span><span class="sxs-lookup"><span data-stu-id="48573-108">The **CdromMediaChange** event occurs when a CD or DVD is inserted into or ejected from a CD or DVD drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="48573-109">語法</span><span class="sxs-lookup"><span data-stu-id="48573-109">Syntax</span></span>


```JScript
Player.CdromMediaChange(
  CdromNum
)
```



## <a name="parameters"></a><span data-ttu-id="48573-110">參數</span><span class="sxs-lookup"><span data-stu-id="48573-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48573-111">*CdromNum*</span><span class="sxs-lookup"><span data-stu-id="48573-111">*CdromNum*</span></span> 
</dt> <dd>

<span data-ttu-id="48573-112">指定 CD 或 DVD 光碟機索引的 (**長**) **數目**。</span><span class="sxs-lookup"><span data-stu-id="48573-112">**Number** (**long**) specifying the index of the CD or DVD drive.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48573-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="48573-113">Return value</span></span>

<span data-ttu-id="48573-114">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="48573-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="48573-115">備註</span><span class="sxs-lookup"><span data-stu-id="48573-115">Remarks</span></span>

<span data-ttu-id="48573-116">CD 光碟機的索引會對應到 **CdromCollection** 中之 **Cdrom** 物件的索引。</span><span class="sxs-lookup"><span data-stu-id="48573-116">The index of the CD drive corresponds to the index of a **Cdrom** object in the **CdromCollection**.</span></span>

<span data-ttu-id="48573-117">事件參數的值是由 Windows Media Player 指定，而且可以使用指定的參數名稱，存取或傳遞至匯入之 JScript 檔案中的方法。</span><span class="sxs-lookup"><span data-stu-id="48573-117">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="48573-118">此參數名稱的類型必須完全如所示，包括大小寫。</span><span class="sxs-lookup"><span data-stu-id="48573-118">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="48573-119">**Windows Media Player 10** 行動裝置版：不支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="48573-119">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="48573-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="48573-120">Requirements</span></span>



| <span data-ttu-id="48573-121">需求</span><span class="sxs-lookup"><span data-stu-id="48573-121">Requirement</span></span> | <span data-ttu-id="48573-122">值</span><span class="sxs-lookup"><span data-stu-id="48573-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="48573-123">版本</span><span class="sxs-lookup"><span data-stu-id="48573-123">Version</span></span><br/> | <span data-ttu-id="48573-124">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="48573-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="48573-125">DLL</span><span class="sxs-lookup"><span data-stu-id="48573-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="48573-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="48573-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48573-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="48573-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48573-128">**Cdrom 物件**</span><span class="sxs-lookup"><span data-stu-id="48573-128">**Cdrom Object**</span></span>](cdrom-object.md)
</dt> <dt>

[<span data-ttu-id="48573-129">**CdromCollection 物件**</span><span class="sxs-lookup"><span data-stu-id="48573-129">**CdromCollection Object**</span></span>](cdromcollection-object.md)
</dt> <dt>

[<span data-ttu-id="48573-130">**Player 物件**</span><span class="sxs-lookup"><span data-stu-id="48573-130">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 






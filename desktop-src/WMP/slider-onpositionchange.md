---
title: 滑杆. onPositionChange
description: OnPositionChange 事件處理常式會處理當滑杆的位置由於使用者按一下或拖曳而變更時所發生的事件。 |滑杆. onPositionChange
ms.assetid: c18e9a49-9576-42ae-9f30-249c44d40f41
keywords:
- OnPositionChange Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.onPositionChange
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd68faa9e7addd85b9b5f02b8a6c445e7ddf54e9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000425"
---
# <a name="slideronpositionchange"></a><span data-ttu-id="abba3-105">滑杆. onPositionChange</span><span class="sxs-lookup"><span data-stu-id="abba3-105">SLIDER.onPositionChange</span></span>

<span data-ttu-id="abba3-106">**OnPositionChange** 事件處理常式會處理當滑杆的位置由於使用者按一下或拖曳而變更時所發生的事件。</span><span class="sxs-lookup"><span data-stu-id="abba3-106">The **onPositionChange** event handler handles an event that occurs when the position of the slider changes as a result of the user clicking or dragging.</span></span>

``` syntax
onPositionChange
```

## <a name="remarks"></a><span data-ttu-id="abba3-107">備註</span><span class="sxs-lookup"><span data-stu-id="abba3-107">Remarks</span></span>

<span data-ttu-id="abba3-108">如果滑杆的位置因為腳本中的 **值** 屬性修改而變更，則不會引發此事件。</span><span class="sxs-lookup"><span data-stu-id="abba3-108">If the position of the slider changes as a result of the **value** attribute being modified in script, this event is not fired.</span></span> <span data-ttu-id="abba3-109">為了滿足這種可能性，請改為執行 **值 \_ onchange** 事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="abba3-109">To accommodate this possibility, implement the **value\_onchange** event handler instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="abba3-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="abba3-110">Requirements</span></span>



| <span data-ttu-id="abba3-111">需求</span><span class="sxs-lookup"><span data-stu-id="abba3-111">Requirement</span></span> | <span data-ttu-id="abba3-112">值</span><span class="sxs-lookup"><span data-stu-id="abba3-112">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="abba3-113">版本</span><span class="sxs-lookup"><span data-stu-id="abba3-113">Version</span></span><br/> | <span data-ttu-id="abba3-114">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="abba3-114">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="abba3-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="abba3-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abba3-116">**滑杆元素**</span><span class="sxs-lookup"><span data-stu-id="abba3-116">**SLIDER Element**</span></span>](slider-element.md)
</dt> </dl>

 

 






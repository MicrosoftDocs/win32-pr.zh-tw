---
title: ScrollingDelay
description: ScrollingDelay 屬性會指定或抓取滾動移動之間的時間延遲。
ms.assetid: b965fe8f-c809-431f-b8fe-f7c3060068ac
keywords:
- ScrollingDelay Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.scrollingDelay
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e81259ca84c62327bea67ae70d3f9ec3363450fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987142"
---
# <a name="textscrollingdelay"></a><span data-ttu-id="ee575-104">ScrollingDelay</span><span class="sxs-lookup"><span data-stu-id="ee575-104">TEXT.scrollingDelay</span></span>

<span data-ttu-id="ee575-105">**ScrollingDelay** 屬性會指定或抓取滾動移動之間的時間延遲。</span><span class="sxs-lookup"><span data-stu-id="ee575-105">The **scrollingDelay** attribute specifies or retrieves the time delay between scrolling movements.</span></span>

``` syntax
        elementID.scrollingDelay
```

## <a name="possible-values"></a><span data-ttu-id="ee575-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="ee575-106">Possible Values</span></span>

<span data-ttu-id="ee575-107">此屬性是讀取/寫入 **號碼** (**int**) 指定延遲（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="ee575-107">This attribute is a read/write **Number** (**int**) specifying the delay in milliseconds.</span></span> <span data-ttu-id="ee575-108">其最小值為30，預設值為85。</span><span class="sxs-lookup"><span data-stu-id="ee575-108">It has a minimum value of 30, and a default value of 85.</span></span> <span data-ttu-id="ee575-109">如果指定的值小於最小值，則會使用預設值。</span><span class="sxs-lookup"><span data-stu-id="ee575-109">If a value less than the minimum is specified, the default is used.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee575-110">備註</span><span class="sxs-lookup"><span data-stu-id="ee575-110">Remarks</span></span>

<span data-ttu-id="ee575-111">如果 [ **滾動** ] 設定為 [false]，則會忽略 **scrollingDelay** 。</span><span class="sxs-lookup"><span data-stu-id="ee575-111">If **scrolling** is set to false, **scrollingDelay** is ignored.</span></span>

<span data-ttu-id="ee575-112">如需說明如何使用 **TEXT** 元素屬性的範例，請參閱 [value](text-value.md)屬性。</span><span class="sxs-lookup"><span data-stu-id="ee575-112">See the [value](text-value.md) attribute for a sample illustrating how the attributes of the **TEXT** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee575-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="ee575-113">Requirements</span></span>



| <span data-ttu-id="ee575-114">需求</span><span class="sxs-lookup"><span data-stu-id="ee575-114">Requirement</span></span> | <span data-ttu-id="ee575-115">值</span><span class="sxs-lookup"><span data-stu-id="ee575-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="ee575-116">版本</span><span class="sxs-lookup"><span data-stu-id="ee575-116">Version</span></span><br/> | <span data-ttu-id="ee575-117">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="ee575-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ee575-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ee575-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee575-119">**TEXT 元素**</span><span class="sxs-lookup"><span data-stu-id="ee575-119">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="ee575-120">**文字。滾動**</span><span class="sxs-lookup"><span data-stu-id="ee575-120">**TEXT.scrolling**</span></span>](text-scrolling.md)
</dt> </dl>

 

 






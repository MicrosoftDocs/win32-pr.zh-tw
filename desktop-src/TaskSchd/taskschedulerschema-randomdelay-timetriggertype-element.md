---
title: RandomDelay (timeTriggerType) 元素
description: 包含隨機新增至觸發程式開始時間的延遲時間。 |RandomDelay (timeTriggerType) 元素
ms.assetid: 84dffd18-651d-4e81-8c02-6cee9759a9b9
keywords:
- RandomDelay 元素工作排程器
topic_type:
- apiref
api_name:
- RandomDelay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a28613cb236b6dc8a3ae77dce9452423a992a866
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106998573"
---
# <a name="randomdelay-timetriggertype-element"></a><span data-ttu-id="2f480-105">RandomDelay (timeTriggerType) 元素</span><span class="sxs-lookup"><span data-stu-id="2f480-105">RandomDelay (timeTriggerType) Element</span></span>

<span data-ttu-id="2f480-106">包含隨機新增至觸發程式開始時間的延遲時間。</span><span class="sxs-lookup"><span data-stu-id="2f480-106">Contains the delay time that is randomly added to the start time of the trigger.</span></span> <span data-ttu-id="2f480-107">此字串的格式為 PnYnMnDTnHnMnS，其中 nY 是年數，nM 是月數，nD 是天數、t ' 是日期/時間分隔符號、nH 是時數、nM 為分鐘數，而 nS 是以秒為單位的秒數，例如，PT5M 指定 (5 分鐘，P1M4DT2H5M 指定一個月、四天、兩小時和五分鐘的) 。</span><span class="sxs-lookup"><span data-stu-id="2f480-107">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="2f480-108">如需持續時間類型的詳細資訊，請參閱 <https://go.microsoft.com/fwlink/p/?linkid=106886> 。</span><span class="sxs-lookup"><span data-stu-id="2f480-108">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span>

``` syntax
<xs:element name="RandomDelay"
    type="duration"
    default="PT0M"
    minOccurs="0"
 />
```

<span data-ttu-id="2f480-109">元素是由 [**timeTriggerType**](taskschedulerschema-timetriggertype-complextype.md) 複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="2f480-109">The element is defined by the [**timeTriggerType**](taskschedulerschema-timetriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="2f480-110">父元素</span><span class="sxs-lookup"><span data-stu-id="2f480-110">Parent element</span></span>



| <span data-ttu-id="2f480-111">元素</span><span class="sxs-lookup"><span data-stu-id="2f480-111">Element</span></span>                                                                                    | <span data-ttu-id="2f480-112">衍生自</span><span class="sxs-lookup"><span data-stu-id="2f480-112">Derived from</span></span>                                                               | <span data-ttu-id="2f480-113">Description</span><span class="sxs-lookup"><span data-stu-id="2f480-113">Description</span></span>                                                                      |
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="2f480-114">**TimeTrigger (triggerGroup)**</span><span class="sxs-lookup"><span data-stu-id="2f480-114">**TimeTrigger (triggerGroup)**</span></span>](taskschedulerschema-timetrigger-triggergroup-element.md) | [<span data-ttu-id="2f480-115">**timeTriggerType**</span><span class="sxs-lookup"><span data-stu-id="2f480-115">**timeTriggerType**</span></span>](taskschedulerschema-timetriggertype-complextype.md) | <span data-ttu-id="2f480-116">指定啟動觸發程式時啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="2f480-116">Specifies a trigger that starts a task when the trigger is activated.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="2f480-117">備註</span><span class="sxs-lookup"><span data-stu-id="2f480-117">Remarks</span></span>

<span data-ttu-id="2f480-118">針對 c + + 開發，請參閱 [**ITimeTrigger 的 RandomDelay 屬性**](/windows/desktop/api/taskschd/nf-taskschd-itimetrigger-get_randomdelay)。</span><span class="sxs-lookup"><span data-stu-id="2f480-118">For C++ development, see [**RandomDelay Property of ITimeTrigger**](/windows/desktop/api/taskschd/nf-taskschd-itimetrigger-get_randomdelay).</span></span>

<span data-ttu-id="2f480-119">如需腳本開發，請參閱 [**TimeTrigger. RandomDelay**](timetrigger-randomdelay.md)。</span><span class="sxs-lookup"><span data-stu-id="2f480-119">For script development, see [**TimeTrigger.RandomDelay**](timetrigger-randomdelay.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2f480-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="2f480-120">Requirements</span></span>



| <span data-ttu-id="2f480-121">需求</span><span class="sxs-lookup"><span data-stu-id="2f480-121">Requirement</span></span> | <span data-ttu-id="2f480-122">值</span><span class="sxs-lookup"><span data-stu-id="2f480-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2f480-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2f480-123">Minimum supported client</span></span><br/> | <span data-ttu-id="2f480-124">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2f480-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2f480-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2f480-125">Minimum supported server</span></span><br/> | <span data-ttu-id="2f480-126">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2f480-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 






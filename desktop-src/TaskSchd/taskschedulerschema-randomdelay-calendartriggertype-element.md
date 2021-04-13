---
title: RandomDelay (calendarTriggerType) 元素
description: 包含隨機新增至觸發程式開始時間的延遲時間。 |RandomDelay (calendarTriggerType) 元素
ms.assetid: 497fab4e-ad63-43e6-a086-2d77b43662d9
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
ms.openlocfilehash: d71149bfeceeb6c17cafa27f56bb15bb184ead06
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322328"
---
# <a name="randomdelay-calendartriggertype-element"></a><span data-ttu-id="3d1b2-105">RandomDelay (calendarTriggerType) 元素</span><span class="sxs-lookup"><span data-stu-id="3d1b2-105">RandomDelay (calendarTriggerType) Element</span></span>

<span data-ttu-id="3d1b2-106">包含隨機新增至觸發程式開始時間的延遲時間。</span><span class="sxs-lookup"><span data-stu-id="3d1b2-106">Contains the delay time that is randomly added to the start time of the trigger.</span></span> <span data-ttu-id="3d1b2-107">此字串的格式為 PnYnMnDTnHnMnS，其中 nY 是年數，nM 是月數，nD 是天數、t ' 是日期/時間分隔符號、nH 是時數、nM 為分鐘數，而 nS 是以秒為單位的秒數，例如，PT5M 指定 (5 分鐘，P1M4DT2H5M 指定一個月、四天、兩小時和五分鐘的) 。</span><span class="sxs-lookup"><span data-stu-id="3d1b2-107">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="3d1b2-108">如需持續時間類型的詳細資訊，請參閱 <https://go.microsoft.com/fwlink/p/?linkid=106886> 。</span><span class="sxs-lookup"><span data-stu-id="3d1b2-108">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span>

``` syntax
<xs:element name="RandomDelay"
    type="duration"
    default="PT0M"
    minOccurs="0"
 />
```

<span data-ttu-id="3d1b2-109">**RandomDelay** 元素是由 [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="3d1b2-109">The **RandomDelay** element is defined by the [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="3d1b2-110">父元素</span><span class="sxs-lookup"><span data-stu-id="3d1b2-110">Parent element</span></span>



| <span data-ttu-id="3d1b2-111">元素</span><span class="sxs-lookup"><span data-stu-id="3d1b2-111">Element</span></span>                                                                                            | <span data-ttu-id="3d1b2-112">衍生自</span><span class="sxs-lookup"><span data-stu-id="3d1b2-112">Derived from</span></span>                                                                       | <span data-ttu-id="3d1b2-113">Description</span><span class="sxs-lookup"><span data-stu-id="3d1b2-113">Description</span></span>                                                                                 |
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3d1b2-114">**CalendarTrigger (triggerGroup)**</span><span class="sxs-lookup"><span data-stu-id="3d1b2-114">**CalendarTrigger (triggerGroup)**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md) | [<span data-ttu-id="3d1b2-115">**calendarTriggerType**</span><span class="sxs-lookup"><span data-stu-id="3d1b2-115">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md) | <span data-ttu-id="3d1b2-116">指定每日、每週、每月或每週 (DOW) 觸發程式。</span><span class="sxs-lookup"><span data-stu-id="3d1b2-116">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="3d1b2-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="3d1b2-117">Requirements</span></span>



| <span data-ttu-id="3d1b2-118">需求</span><span class="sxs-lookup"><span data-stu-id="3d1b2-118">Requirement</span></span> | <span data-ttu-id="3d1b2-119">值</span><span class="sxs-lookup"><span data-stu-id="3d1b2-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3d1b2-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3d1b2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3d1b2-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3d1b2-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3d1b2-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3d1b2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3d1b2-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3d1b2-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 






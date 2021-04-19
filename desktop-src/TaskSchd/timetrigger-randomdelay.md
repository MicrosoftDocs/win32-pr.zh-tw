---
title: TimeTrigger. RandomDelay 屬性
description: 針對腳本，取得或設定隨機加入至觸發程式開始時間的延遲時間。 |TimeTrigger. RandomDelay 屬性
ms.assetid: ee55dd85-9696-4872-8670-f919fca7481d
keywords:
- RandomDelay 屬性工作排程器
- RandomDelay 屬性工作排程器，TimeTrigger 物件
- TimeTrigger 物件工作排程器、RandomDelay 屬性
topic_type:
- apiref
api_name:
- TimeTrigger.RandomDelay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39c4acf4f38670332e723ac0824276695919cb1d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106995888"
---
# <a name="timetriggerrandomdelay-property"></a><span data-ttu-id="f84e9-107">TimeTrigger. RandomDelay 屬性</span><span class="sxs-lookup"><span data-stu-id="f84e9-107">TimeTrigger.RandomDelay property</span></span>

<span data-ttu-id="f84e9-108">針對腳本，取得或設定隨機加入至觸發程式開始時間的延遲時間。</span><span class="sxs-lookup"><span data-stu-id="f84e9-108">For scripting, gets or sets a delay time that is randomly added to the start time of the trigger.</span></span>

## <a name="syntax"></a><span data-ttu-id="f84e9-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="f84e9-109">Syntax</span></span>


```VB
TimeTrigger.RandomDelay As String
```



## <a name="property-value"></a><span data-ttu-id="f84e9-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="f84e9-110">Property value</span></span>

<span data-ttu-id="f84e9-111">隨機新增至觸發程式開始時間的延遲時間。</span><span class="sxs-lookup"><span data-stu-id="f84e9-111">The delay time that is randomly added to the start time of the trigger.</span></span> <span data-ttu-id="f84e9-112">此字串的格式為 PnYnMnDTnHnMnS，其中 nY 是年數，nM 是月數，nD 是天數、t ' 是日期/時間分隔符號、nH 是時數、nM 為分鐘數，而 nS 是以秒為單位的秒數，例如，PT5M 指定 (5 分鐘，P1M4DT2H5M 指定一個月、四天、兩小時和五分鐘的) 。</span><span class="sxs-lookup"><span data-stu-id="f84e9-112">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span>

## <a name="requirements"></a><span data-ttu-id="f84e9-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="f84e9-113">Requirements</span></span>



| <span data-ttu-id="f84e9-114">需求</span><span class="sxs-lookup"><span data-stu-id="f84e9-114">Requirement</span></span> | <span data-ttu-id="f84e9-115">值</span><span class="sxs-lookup"><span data-stu-id="f84e9-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f84e9-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f84e9-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f84e9-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f84e9-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="f84e9-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f84e9-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f84e9-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f84e9-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f84e9-120">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="f84e9-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="f84e9-121"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f84e9-121"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f84e9-122">DLL</span><span class="sxs-lookup"><span data-stu-id="f84e9-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f84e9-123"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f84e9-123"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 






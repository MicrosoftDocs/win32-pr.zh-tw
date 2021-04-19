---
title: WeeklyTrigger. RandomDelay 屬性
description: 針對腳本，取得或設定隨機加入至觸發程式開始時間的延遲時間。 |WeeklyTrigger. RandomDelay 屬性
ms.assetid: 711b188d-b283-4c99-b43d-644f39a31cdc
keywords:
- RandomDelay 屬性工作排程器
- RandomDelay 屬性工作排程器，WeeklyTrigger 物件
- WeeklyTrigger 物件工作排程器、RandomDelay 屬性
topic_type:
- apiref
api_name:
- WeeklyTrigger.RandomDelay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3a7d955956c119244a5b92a1ee0d81cd5add9b7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "107001474"
---
# <a name="weeklytriggerrandomdelay-property"></a><span data-ttu-id="949c8-107">WeeklyTrigger. RandomDelay 屬性</span><span class="sxs-lookup"><span data-stu-id="949c8-107">WeeklyTrigger.RandomDelay property</span></span>

<span data-ttu-id="949c8-108">針對腳本，取得或設定隨機加入至觸發程式開始時間的延遲時間。</span><span class="sxs-lookup"><span data-stu-id="949c8-108">For scripting, gets or sets a delay time that is randomly added to the start time of the trigger.</span></span>

## <a name="syntax"></a><span data-ttu-id="949c8-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="949c8-109">Syntax</span></span>


```VB
WeeklyTrigger.RandomDelay As String
```



## <a name="property-value"></a><span data-ttu-id="949c8-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="949c8-110">Property value</span></span>

<span data-ttu-id="949c8-111">隨機新增至觸發程式開始時間的延遲時間。</span><span class="sxs-lookup"><span data-stu-id="949c8-111">The delay time that is randomly added to the start time of the trigger.</span></span> <span data-ttu-id="949c8-112">此字串的格式為 P <days> DT <hours> H <minutes> M <seconds> S (例如，P2DT5S 是2天、5秒的延遲) 。</span><span class="sxs-lookup"><span data-stu-id="949c8-112">The format for this string is P<days>DT<hours>H<minutes>M<seconds>S (for example, P2DT5S is a 2 day, 5 second delay).</span></span>

## <a name="requirements"></a><span data-ttu-id="949c8-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="949c8-113">Requirements</span></span>



| <span data-ttu-id="949c8-114">需求</span><span class="sxs-lookup"><span data-stu-id="949c8-114">Requirement</span></span> | <span data-ttu-id="949c8-115">值</span><span class="sxs-lookup"><span data-stu-id="949c8-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="949c8-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="949c8-116">Minimum supported client</span></span><br/> | <span data-ttu-id="949c8-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="949c8-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="949c8-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="949c8-118">Minimum supported server</span></span><br/> | <span data-ttu-id="949c8-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="949c8-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="949c8-120">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="949c8-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="949c8-121"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="949c8-121"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="949c8-122">DLL</span><span class="sxs-lookup"><span data-stu-id="949c8-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="949c8-123"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="949c8-123"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 






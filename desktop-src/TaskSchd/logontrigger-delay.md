---
title: LogonTrigger Delay 屬性
description: 針對腳本，取得或設定值，這個值表示使用者登入和工作啟動時間之間的時間量。
ms.assetid: 42198357-18e9-4fff-a8bf-f2da36148dc8
keywords:
- Delay 屬性工作排程器
- Delay 屬性工作排程器，LogonTrigger 物件
- LogonTrigger 物件工作排程器，Delay 屬性
topic_type:
- apiref
api_name:
- LogonTrigger.Delay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce709b5095ffaeb9fdb5a4532f496ffa34c24e5b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384109"
---
# <a name="logontriggerdelay-property"></a><span data-ttu-id="36086-106">LogonTrigger Delay 屬性</span><span class="sxs-lookup"><span data-stu-id="36086-106">LogonTrigger.Delay property</span></span>

<span data-ttu-id="36086-107">針對腳本，取得或設定值，這個值表示使用者登入和工作啟動時間之間的時間量。</span><span class="sxs-lookup"><span data-stu-id="36086-107">For scripting, gets or sets a value that indicates the amount of time between when the user logs on and when the task is started.</span></span>

## <a name="syntax"></a><span data-ttu-id="36086-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="36086-108">Syntax</span></span>


```VB
LogonTrigger.Delay As String
```



## <a name="property-value"></a><span data-ttu-id="36086-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="36086-109">Property value</span></span>

<span data-ttu-id="36086-110">值，指出使用者登入和工作啟動時間之間的時間量。</span><span class="sxs-lookup"><span data-stu-id="36086-110">A value that indicates the amount of time between when the user logs on and when the task is started.</span></span> <span data-ttu-id="36086-111">此字串的格式為 PnYnMnDTnHnMnS，其中 nY 是年數，nM 是月數，nD 是天數、t ' 是日期/時間分隔符號、nH 是時數、nM 為分鐘數，而 nS 是以秒為單位的秒數，例如，PT5M 指定 (5 分鐘，P1M4DT2H5M 指定一個月、四天、兩小時和五分鐘的) 。</span><span class="sxs-lookup"><span data-stu-id="36086-111">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span>

## <a name="remarks"></a><span data-ttu-id="36086-112">備註</span><span class="sxs-lookup"><span data-stu-id="36086-112">Remarks</span></span>

<span data-ttu-id="36086-113">讀取或寫入工作的 XML 時，會使用工作排程器架構的 [**delay**](taskschedulerschema-delay-logontriggertype-element.md) 元素指定登入觸發程式延遲。</span><span class="sxs-lookup"><span data-stu-id="36086-113">When reading or writing XML for a task, the logon trigger delay is specified using the [**Delay**](taskschedulerschema-delay-logontriggertype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="36086-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="36086-114">Requirements</span></span>



| <span data-ttu-id="36086-115">需求</span><span class="sxs-lookup"><span data-stu-id="36086-115">Requirement</span></span> | <span data-ttu-id="36086-116">值</span><span class="sxs-lookup"><span data-stu-id="36086-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="36086-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="36086-117">Minimum supported client</span></span><br/> | <span data-ttu-id="36086-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="36086-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="36086-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="36086-119">Minimum supported server</span></span><br/> | <span data-ttu-id="36086-120">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="36086-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="36086-121">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="36086-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="36086-122"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="36086-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="36086-123">DLL</span><span class="sxs-lookup"><span data-stu-id="36086-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="36086-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="36086-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36086-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="36086-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36086-126">**LogonTrigger**</span><span class="sxs-lookup"><span data-stu-id="36086-126">**LogonTrigger**</span></span>](logontrigger.md)
</dt> <dt>

[<span data-ttu-id="36086-127">工作排程器</span><span class="sxs-lookup"><span data-stu-id="36086-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 






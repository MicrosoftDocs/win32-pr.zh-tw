---
title: RegistrationInfo。 Date 屬性
description: 針對腳本，取得或設定註冊工作的日期和時間。
ms.assetid: ecff01b6-a1de-458a-9728-34169f17d42b
keywords:
- Date 屬性工作排程器
- Date 屬性工作排程器，RegistrationInfo 物件
- RegistrationInfo 物件工作排程器，日期屬性
topic_type:
- apiref
api_name:
- RegistrationInfo.Date
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: adfdfa8b2dd3f8dcaa3b2fd5778b1e50dabfab51
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966489"
---
# <a name="registrationinfodate-property"></a><span data-ttu-id="0445b-106">RegistrationInfo。 Date 屬性</span><span class="sxs-lookup"><span data-stu-id="0445b-106">RegistrationInfo.Date property</span></span>

<span data-ttu-id="0445b-107">針對腳本，取得或設定註冊工作的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="0445b-107">For scripting, gets or sets the date and time when the task is registered.</span></span>

## <a name="syntax"></a><span data-ttu-id="0445b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="0445b-108">Syntax</span></span>


```VB
RegistrationInfo.Date As String
```



## <a name="property-value"></a><span data-ttu-id="0445b-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="0445b-109">Property value</span></span>

<span data-ttu-id="0445b-110">工作的註冊日期。</span><span class="sxs-lookup"><span data-stu-id="0445b-110">The registration date of the task.</span></span>

## <a name="remarks"></a><span data-ttu-id="0445b-111">備註</span><span class="sxs-lookup"><span data-stu-id="0445b-111">Remarks</span></span>

<span data-ttu-id="0445b-112">讀取或寫入工作的 XML 時，會使用工作排程器架構的 [**日期**](taskschedulerschema-date-registrationinfotype-element.md) 元素來指定註冊日期。</span><span class="sxs-lookup"><span data-stu-id="0445b-112">When reading or writing XML for a task, the registration date is specified using the [**Date**](taskschedulerschema-date-registrationinfotype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="0445b-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="0445b-113">Requirements</span></span>



| <span data-ttu-id="0445b-114">需求</span><span class="sxs-lookup"><span data-stu-id="0445b-114">Requirement</span></span> | <span data-ttu-id="0445b-115">值</span><span class="sxs-lookup"><span data-stu-id="0445b-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0445b-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0445b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0445b-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0445b-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="0445b-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0445b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0445b-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0445b-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0445b-120">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="0445b-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="0445b-121"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="0445b-121"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="0445b-122">DLL</span><span class="sxs-lookup"><span data-stu-id="0445b-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0445b-123"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0445b-123"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0445b-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0445b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0445b-125">工作排程器</span><span class="sxs-lookup"><span data-stu-id="0445b-125">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 






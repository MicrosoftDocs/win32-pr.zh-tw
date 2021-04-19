---
title: RegistrationInfo. SecurityDescriptor 屬性
description: 針對腳本，取得或設定工作的安全描述項。
ms.assetid: e03607f0-c2a0-4aa1-a2b0-915b03aae968
keywords:
- SecurityDescriptor 屬性工作排程器
- SecurityDescriptor 屬性工作排程器，RegistrationInfo 物件
- RegistrationInfo 物件工作排程器、SecurityDescriptor 屬性
topic_type:
- apiref
api_name:
- RegistrationInfo.SecurityDescriptor
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 379e42f41387a40b160a73ec3457d3d5b9feaf59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "107001290"
---
# <a name="registrationinfosecuritydescriptor-property"></a><span data-ttu-id="8e76e-106">RegistrationInfo. SecurityDescriptor 屬性</span><span class="sxs-lookup"><span data-stu-id="8e76e-106">RegistrationInfo.SecurityDescriptor property</span></span>

<span data-ttu-id="8e76e-107">針對腳本，取得或設定工作的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="8e76e-107">For scripting, gets or sets the security descriptor of the task.</span></span> <span data-ttu-id="8e76e-108">如果在工作註冊期間提供不同的安全描述項，則會取代此屬性所設定的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="8e76e-108">If a different security descriptor is supplied during task registration, it will supersede the security descriptor set with this property.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e76e-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="8e76e-109">Syntax</span></span>


```VB
RegistrationInfo.SecurityDescriptor As String
```



## <a name="property-value"></a><span data-ttu-id="8e76e-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="8e76e-110">Property value</span></span>

<span data-ttu-id="8e76e-111">與工作相關聯的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="8e76e-111">The security descriptor that is associated with the task.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e76e-112">備註</span><span class="sxs-lookup"><span data-stu-id="8e76e-112">Remarks</span></span>

<span data-ttu-id="8e76e-113">讀取或寫入工作的 XML 時，會使用工作排程器架構的 [**SecurityDescriptor**](taskschedulerschema-securitydescriptor-registrationinfotype-element.md) 元素來指定工作的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="8e76e-113">When reading or writing XML for a task, the security descriptor of the task is specified using the [**SecurityDescriptor**](taskschedulerschema-securitydescriptor-registrationinfotype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e76e-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="8e76e-114">Requirements</span></span>



| <span data-ttu-id="8e76e-115">需求</span><span class="sxs-lookup"><span data-stu-id="8e76e-115">Requirement</span></span> | <span data-ttu-id="8e76e-116">值</span><span class="sxs-lookup"><span data-stu-id="8e76e-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8e76e-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8e76e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8e76e-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8e76e-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="8e76e-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8e76e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8e76e-120">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8e76e-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8e76e-121">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="8e76e-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="8e76e-122"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8e76e-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="8e76e-123">DLL</span><span class="sxs-lookup"><span data-stu-id="8e76e-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8e76e-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8e76e-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e76e-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8e76e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e76e-126">工作排程器</span><span class="sxs-lookup"><span data-stu-id="8e76e-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 






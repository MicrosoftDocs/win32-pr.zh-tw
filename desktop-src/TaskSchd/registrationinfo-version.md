---
title: RegistrationInfo 版本屬性
description: 針對腳本，取得或設定工作的版本號碼。
ms.assetid: 5f200948-b4ff-495c-9578-2a93b34fd75b
keywords:
- Version 屬性工作排程器
- Version 屬性工作排程器，RegistrationInfo 物件
- RegistrationInfo 物件工作排程器，Version 屬性
topic_type:
- apiref
api_name:
- RegistrationInfo.Version
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c312878383c5361317a765cbf84a503244c188a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024772"
---
# <a name="registrationinfoversion-property"></a><span data-ttu-id="75a5f-106">RegistrationInfo 版本屬性</span><span class="sxs-lookup"><span data-stu-id="75a5f-106">RegistrationInfo.Version property</span></span>

<span data-ttu-id="75a5f-107">針對腳本，取得或設定工作的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="75a5f-107">For scripting, gets or sets the version number of the task.</span></span>

## <a name="syntax"></a><span data-ttu-id="75a5f-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="75a5f-108">Syntax</span></span>


```VB
RegistrationInfo.Version As String
```



## <a name="property-value"></a><span data-ttu-id="75a5f-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="75a5f-109">Property value</span></span>

<span data-ttu-id="75a5f-110">工作的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="75a5f-110">The version number of the task.</span></span>

## <a name="remarks"></a><span data-ttu-id="75a5f-111">備註</span><span class="sxs-lookup"><span data-stu-id="75a5f-111">Remarks</span></span>

<span data-ttu-id="75a5f-112">讀取或寫入工作的 XML 時，會使用工作排程器架構的 [**version**](taskschedulerschema-version-registrationinfotype-element.md) 元素來指定工作的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="75a5f-112">When reading or writing XML for a task, the version number of the task is specified using the [**Version**](taskschedulerschema-version-registrationinfotype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="75a5f-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="75a5f-113">Requirements</span></span>



| <span data-ttu-id="75a5f-114">需求</span><span class="sxs-lookup"><span data-stu-id="75a5f-114">Requirement</span></span> | <span data-ttu-id="75a5f-115">值</span><span class="sxs-lookup"><span data-stu-id="75a5f-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="75a5f-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="75a5f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="75a5f-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="75a5f-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="75a5f-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="75a5f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="75a5f-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="75a5f-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="75a5f-120">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="75a5f-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="75a5f-121"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="75a5f-121"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="75a5f-122">DLL</span><span class="sxs-lookup"><span data-stu-id="75a5f-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75a5f-123"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75a5f-123"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75a5f-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="75a5f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75a5f-125">工作排程器</span><span class="sxs-lookup"><span data-stu-id="75a5f-125">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 






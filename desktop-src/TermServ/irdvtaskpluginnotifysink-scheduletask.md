---
title: IRDVTaskPluginNotifySink ScheduleTask 方法
description: 由工作代理程式呼叫以排程工作。
ms.assetid: 06793439-cf16-40ca-8a91-08acc22c73ed
ms.tgt_platform: multiple
keywords:
- ScheduleTask 方法遠端桌面服務
- ScheduleTask 方法遠端桌面服務，IRDVTaskPluginNotifySink 介面
- IRDVTaskPluginNotifySink 介面遠端桌面服務，ScheduleTask 方法
topic_type:
- apiref
api_name:
- IRDVTaskPluginNotifySink.ScheduleTask
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c9bde92992eec9c4ab3d4151c59e6d687ec2f3fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844279"
---
# <a name="irdvtaskpluginnotifysinkscheduletask-method"></a><span data-ttu-id="9a1cd-106">IRDVTaskPluginNotifySink：： ScheduleTask 方法</span><span class="sxs-lookup"><span data-stu-id="9a1cd-106">IRDVTaskPluginNotifySink::ScheduleTask method</span></span>

<span data-ttu-id="9a1cd-107">由工作代理程式呼叫以排程工作。</span><span class="sxs-lookup"><span data-stu-id="9a1cd-107">Called by the task agent to schedule a task.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a1cd-108">語法</span><span class="sxs-lookup"><span data-stu-id="9a1cd-108">Syntax</span></span>


```C++
HRESULT ScheduleTask(
  [in] FILETIME        ftStartTime,
  [in] FILETIME        ftEndTime,
  [in] FILETIME        ftDeadline,
  [in] BSTR            bstrLabel,
  [in] BSTR            bstrIdentifier,
  [in] SAFEARRAY(BYTE) saContext
);
```



## <a name="parameters"></a><span data-ttu-id="9a1cd-109">參數</span><span class="sxs-lookup"><span data-stu-id="9a1cd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a1cd-110">*ftStartTime* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9a1cd-110">*ftStartTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a1cd-111">類型： **[ **FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)**</span><span class="sxs-lookup"><span data-stu-id="9a1cd-111">Type: **[**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)**</span></span>

<span data-ttu-id="9a1cd-112">最早的工作開始時間（UTC）。</span><span class="sxs-lookup"><span data-stu-id="9a1cd-112">The earliest task start time, in UTC.</span></span>

</dd> <dt>

<span data-ttu-id="9a1cd-113">*ftEndTime* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9a1cd-113">*ftEndTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a1cd-114">類型： **[ **FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)**</span><span class="sxs-lookup"><span data-stu-id="9a1cd-114">Type: **[**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)**</span></span>

<span data-ttu-id="9a1cd-115">工作結束時間（UTC）。</span><span class="sxs-lookup"><span data-stu-id="9a1cd-115">The task end time, in UTC.</span></span> <span data-ttu-id="9a1cd-116">如果未指定任何結束時間，則將 [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) 集合傳遞至全部零。</span><span class="sxs-lookup"><span data-stu-id="9a1cd-116">Pass a [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) set to all zeros if no end time is specified.</span></span>

</dd> <dt>

<span data-ttu-id="9a1cd-117">*ftDeadline* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9a1cd-117">*ftDeadline* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a1cd-118">類型： **[ **FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)**</span><span class="sxs-lookup"><span data-stu-id="9a1cd-118">Type: **[**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)**</span></span>

<span data-ttu-id="9a1cd-119">工作期限（UTC 格式）。</span><span class="sxs-lookup"><span data-stu-id="9a1cd-119">The task deadline, in UTC.</span></span> <span data-ttu-id="9a1cd-120">這是用來設定其開始視窗內多個工作的優先順序。</span><span class="sxs-lookup"><span data-stu-id="9a1cd-120">This is used to set priority for multiple tasks that are within their start window.</span></span> <span data-ttu-id="9a1cd-121">如果應啟動多項工作，則會先啟動具有最早期限的工作。</span><span class="sxs-lookup"><span data-stu-id="9a1cd-121">If more than one task should be started, the one with the earliest deadline will be started first.</span></span>

</dd> <dt>

<span data-ttu-id="9a1cd-122">*bstrLabel* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9a1cd-122">*bstrLabel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a1cd-123">類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="9a1cd-123">Type: **BSTR**</span></span>

<span data-ttu-id="9a1cd-124">工作的標籤。</span><span class="sxs-lookup"><span data-stu-id="9a1cd-124">The label for the task.</span></span> <span data-ttu-id="9a1cd-125">這會傳遞至 [**StartTask**](irdvtaskplugin-starttask.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="9a1cd-125">This is passed to the [**StartTask**](irdvtaskplugin-starttask.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="9a1cd-126">*bstrIdentifier* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9a1cd-126">*bstrIdentifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a1cd-127">類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="9a1cd-127">Type: **BSTR**</span></span>

<span data-ttu-id="9a1cd-128">工作的識別碼。</span><span class="sxs-lookup"><span data-stu-id="9a1cd-128">The identifier of the task.</span></span> <span data-ttu-id="9a1cd-129">這會傳遞至 [**StartTask**](irdvtaskplugin-starttask.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="9a1cd-129">This is passed to the [**StartTask**](irdvtaskplugin-starttask.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="9a1cd-130">*saCoNtext* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9a1cd-130">*saContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a1cd-131">類型： **SAFEARRAY (BYTE)**</span><span class="sxs-lookup"><span data-stu-id="9a1cd-131">Type: **SAFEARRAY(BYTE)**</span></span>

<span data-ttu-id="9a1cd-132">工作的選擇性資料。</span><span class="sxs-lookup"><span data-stu-id="9a1cd-132">Optional data for the task.</span></span> <span data-ttu-id="9a1cd-133">這會傳遞至 [**StartTask**](irdvtaskplugin-starttask.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="9a1cd-133">This is passed to the [**StartTask**](irdvtaskplugin-starttask.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a1cd-134">傳回值</span><span class="sxs-lookup"><span data-stu-id="9a1cd-134">Return value</span></span>

<span data-ttu-id="9a1cd-135">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="9a1cd-135">Type: **HRESULT**</span></span>

<span data-ttu-id="9a1cd-136">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="9a1cd-136">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9a1cd-137">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="9a1cd-137">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a1cd-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="9a1cd-138">Requirements</span></span>



| <span data-ttu-id="9a1cd-139">需求</span><span class="sxs-lookup"><span data-stu-id="9a1cd-139">Requirement</span></span> | <span data-ttu-id="9a1cd-140">值</span><span class="sxs-lookup"><span data-stu-id="9a1cd-140">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="9a1cd-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9a1cd-141">Minimum supported client</span></span><br/> | <span data-ttu-id="9a1cd-142">Windows 7 Enterprise</span><span class="sxs-lookup"><span data-stu-id="9a1cd-142">Windows 7 Enterprise</span></span><br/>   |
| <span data-ttu-id="9a1cd-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9a1cd-143">Minimum supported server</span></span><br/> | <span data-ttu-id="9a1cd-144">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9a1cd-144">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9a1cd-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9a1cd-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a1cd-146">**IRDVTaskPluginNotifySink**</span><span class="sxs-lookup"><span data-stu-id="9a1cd-146">**IRDVTaskPluginNotifySink**</span></span>](irdvtaskpluginnotifysink.md)
</dt> </dl>

 


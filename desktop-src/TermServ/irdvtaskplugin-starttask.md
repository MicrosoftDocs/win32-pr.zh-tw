---
title: IRDVTaskPlugin StartTask 方法
description: 呼叫以啟動虛擬機器上的更新工作。
ms.assetid: c1e9f18b-1e83-4a29-8646-8adde94e8c14
ms.tgt_platform: multiple
keywords:
- StartTask 方法遠端桌面服務
- StartTask 方法遠端桌面服務，IRDVTaskPlugin 介面
- IRDVTaskPlugin 介面遠端桌面服務，StartTask 方法
topic_type:
- apiref
api_name:
- IRDVTaskPlugin.StartTask
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 51c499549378700a90d8fc78d075bc07c1f874cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465781"
---
# <a name="irdvtaskpluginstarttask-method"></a><span data-ttu-id="b7665-106">IRDVTaskPlugin：： StartTask 方法</span><span class="sxs-lookup"><span data-stu-id="b7665-106">IRDVTaskPlugin::StartTask method</span></span>

<span data-ttu-id="b7665-107">呼叫以啟動虛擬機器上的更新工作。</span><span class="sxs-lookup"><span data-stu-id="b7665-107">Called to start the update task on the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7665-108">語法</span><span class="sxs-lookup"><span data-stu-id="b7665-108">Syntax</span></span>


```C++
HRESULT StartTask(
  [in] BSTR            Label,
  [in] BSTR            Identifier,
  [in] SAFEARRAY(BYTE) *Context
);
```



## <a name="parameters"></a><span data-ttu-id="b7665-109">參數</span><span class="sxs-lookup"><span data-stu-id="b7665-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7665-110">*標籤* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b7665-110">*Label* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7665-111">工作的標籤。</span><span class="sxs-lookup"><span data-stu-id="b7665-111">The label for the task.</span></span> <span data-ttu-id="b7665-112">這是在 [**ScheduleTask**](irdvtaskpluginnotifysink-scheduletask.md) 方法中傳遞給觸發程式代理程式的標籤。</span><span class="sxs-lookup"><span data-stu-id="b7665-112">This is the label that was passed to the trigger agent in the [**ScheduleTask**](irdvtaskpluginnotifysink-scheduletask.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="b7665-113">*識別碼* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b7665-113">*Identifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7665-114">工作的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b7665-114">The identifier of the task.</span></span> <span data-ttu-id="b7665-115">這是在 [**ScheduleTask**](irdvtaskpluginnotifysink-scheduletask.md) 方法中傳遞給觸發程式代理程式的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b7665-115">This is the identifier that was passed to the trigger agent in the [**ScheduleTask**](irdvtaskpluginnotifysink-scheduletask.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="b7665-116">*內容* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b7665-116">*Context* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7665-117">工作的選擇性資料。</span><span class="sxs-lookup"><span data-stu-id="b7665-117">Optional data for the task.</span></span> <span data-ttu-id="b7665-118">這是在 [**ScheduleTask**](irdvtaskpluginnotifysink-scheduletask.md) 方法中傳遞給觸發程式代理程式的資料。</span><span class="sxs-lookup"><span data-stu-id="b7665-118">This is the data that was passed to the trigger agent in the [**ScheduleTask**](irdvtaskpluginnotifysink-scheduletask.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7665-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="b7665-119">Return value</span></span>

<span data-ttu-id="b7665-120">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="b7665-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b7665-121">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b7665-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7665-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="b7665-122">Requirements</span></span>



| <span data-ttu-id="b7665-123">需求</span><span class="sxs-lookup"><span data-stu-id="b7665-123">Requirement</span></span> | <span data-ttu-id="b7665-124">值</span><span class="sxs-lookup"><span data-stu-id="b7665-124">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="b7665-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b7665-125">Minimum supported client</span></span><br/> | <span data-ttu-id="b7665-126">Windows 7 Enterprise</span><span class="sxs-lookup"><span data-stu-id="b7665-126">Windows 7 Enterprise</span></span><br/>   |
| <span data-ttu-id="b7665-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b7665-127">Minimum supported server</span></span><br/> | <span data-ttu-id="b7665-128">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b7665-128">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b7665-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b7665-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7665-130">**IRDVTaskPlugin**</span><span class="sxs-lookup"><span data-stu-id="b7665-130">**IRDVTaskPlugin**</span></span>](irdvtaskplugin.md)
</dt> </dl>

 

 






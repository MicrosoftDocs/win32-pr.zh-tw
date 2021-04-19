---
title: IRDVTaskPluginNotifySink OnTaskStateChange 方法
description: 用來通知觸發程式代理程式工作的狀態已變更。
ms.assetid: 3021ea7a-2627-48d1-8df5-c40e7a9b51c5
ms.tgt_platform: multiple
keywords:
- OnTaskStateChange 方法遠端桌面服務
- OnTaskStateChange 方法遠端桌面服務，IRDVTaskPluginNotifySink 介面
- IRDVTaskPluginNotifySink 介面遠端桌面服務，OnTaskStateChange 方法
topic_type:
- apiref
api_name:
- IRDVTaskPluginNotifySink.OnTaskStateChange
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c3e3acf1a2d47b1721ef90554f7a11714c02e6df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106998029"
---
# <a name="irdvtaskpluginnotifysinkontaskstatechange-method"></a><span data-ttu-id="788bb-106">IRDVTaskPluginNotifySink：： OnTaskStateChange 方法</span><span class="sxs-lookup"><span data-stu-id="788bb-106">IRDVTaskPluginNotifySink::OnTaskStateChange method</span></span>

<span data-ttu-id="788bb-107">用來通知觸發程式代理程式工作的狀態已變更。</span><span class="sxs-lookup"><span data-stu-id="788bb-107">Used to notify the trigger agent that the state of a task has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="788bb-108">語法</span><span class="sxs-lookup"><span data-stu-id="788bb-108">Syntax</span></span>


```C++
HRESULT OnTaskStateChange(
  [in] BSTR            bstrIdentifier,
  [in] RDV_TASK_STATUS status
);
```



## <a name="parameters"></a><span data-ttu-id="788bb-109">參數</span><span class="sxs-lookup"><span data-stu-id="788bb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="788bb-110">*bstrIdentifier* \[在\]</span><span class="sxs-lookup"><span data-stu-id="788bb-110">*bstrIdentifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="788bb-111">類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="788bb-111">Type: **BSTR**</span></span>

<span data-ttu-id="788bb-112">工作的識別碼。</span><span class="sxs-lookup"><span data-stu-id="788bb-112">The identifier of the task.</span></span> <span data-ttu-id="788bb-113">這是傳遞給 [**StartTask**](irdvtaskplugin-starttask.md) 方法的識別碼。</span><span class="sxs-lookup"><span data-stu-id="788bb-113">This is the identifier passed to the [**StartTask**](irdvtaskplugin-starttask.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="788bb-114">*狀態* \[在\]</span><span class="sxs-lookup"><span data-stu-id="788bb-114">*status* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="788bb-115">類型： **[ **RDV \_ 工作 \_ 狀態**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status)**</span><span class="sxs-lookup"><span data-stu-id="788bb-115">Type: **[**RDV\_TASK\_STATUS**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status)**</span></span>

<span data-ttu-id="788bb-116">[**RDV 工作 \_ \_ 狀態**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status)列舉值，這個值會指定工作的新狀態。</span><span class="sxs-lookup"><span data-stu-id="788bb-116">A value of the [**RDV\_TASK\_STATUS**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status) enumeration that specifies the new state of the task.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="788bb-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="788bb-117">Return value</span></span>

<span data-ttu-id="788bb-118">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="788bb-118">Type: **HRESULT**</span></span>

<span data-ttu-id="788bb-119">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="788bb-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="788bb-120">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="788bb-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="788bb-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="788bb-121">Requirements</span></span>



| <span data-ttu-id="788bb-122">需求</span><span class="sxs-lookup"><span data-stu-id="788bb-122">Requirement</span></span> | <span data-ttu-id="788bb-123">值</span><span class="sxs-lookup"><span data-stu-id="788bb-123">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="788bb-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="788bb-124">Minimum supported client</span></span><br/> | <span data-ttu-id="788bb-125">Windows 7 Enterprise</span><span class="sxs-lookup"><span data-stu-id="788bb-125">Windows 7 Enterprise</span></span><br/>   |
| <span data-ttu-id="788bb-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="788bb-126">Minimum supported server</span></span><br/> | <span data-ttu-id="788bb-127">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="788bb-127">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="788bb-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="788bb-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="788bb-129">**RDV \_ 工作 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="788bb-129">**RDV\_TASK\_STATUS**</span></span>](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status)
</dt> <dt>

[<span data-ttu-id="788bb-130">**IRDVTaskPluginNotifySink**</span><span class="sxs-lookup"><span data-stu-id="788bb-130">**IRDVTaskPluginNotifySink**</span></span>](irdvtaskpluginnotifysink.md)
</dt> </dl>

 

 






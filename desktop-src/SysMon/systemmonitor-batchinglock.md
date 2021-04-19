---
title: SystemMonitor.BatchingLock 方法
description: 鎖定系統監視器，以防止它從新加入的計數器或記錄檔取樣計數器資料。
ms.assetid: 6b9d683a-7a97-44a4-9eb6-6caaafe2abdd
keywords:
- BatchingLock 方法 SysMon
- BatchingLock 方法 SysMon，SystemMonitor 物件
- SystemMonitor 物件 SysMon，BatchingLock 方法
topic_type:
- apiref
api_name:
- SystemMonitor.BatchingLock
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b858a6920b039d911ae571d81744eb99dea4ef4f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965911"
---
# <a name="systemmonitorbatchinglock-method"></a><span data-ttu-id="4b832-106">SystemMonitor.BatchingLock 方法</span><span class="sxs-lookup"><span data-stu-id="4b832-106">SystemMonitor.BatchingLock method</span></span>

<span data-ttu-id="4b832-107">鎖定系統監視器，以防止它從新加入的計數器或記錄檔取樣計數器資料。</span><span class="sxs-lookup"><span data-stu-id="4b832-107">Locks the System Monitor to prevent it from sampling counter data from the newly added counter or log file.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b832-108">語法</span><span class="sxs-lookup"><span data-stu-id="4b832-108">Syntax</span></span>


```VB
SystemMonitor.BatchingLock( _
  ByVal lock As Boolean, _
  ByVal batchReason As SysmonBatchReason _
)
```



## <a name="parameters"></a><span data-ttu-id="4b832-109">參數</span><span class="sxs-lookup"><span data-stu-id="4b832-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b832-110">*鎖定* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4b832-110">*lock* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b832-111">設定為 True 可鎖定系統監視器，以防止它從新加入的計數器或記錄檔取樣計數器資料。</span><span class="sxs-lookup"><span data-stu-id="4b832-111">Set to True to lock the System Monitor to prevent it from sampling counter data from the newly added counter or log file.</span></span> <span data-ttu-id="4b832-112">設定為 False 以移除鎖定。</span><span class="sxs-lookup"><span data-stu-id="4b832-112">Set to False to remove the lock.</span></span>

</dd> <dt>

<span data-ttu-id="4b832-113">*batchReason* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4b832-113">*batchReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b832-114">識別您要鎖定之資料的來源。</span><span class="sxs-lookup"><span data-stu-id="4b832-114">Identifies the source of the data that you are locking.</span></span> <span data-ttu-id="4b832-115">鎖定和解除鎖定資源時，請使用相同的原因值。</span><span class="sxs-lookup"><span data-stu-id="4b832-115">Use the same reason value when locking and unlocking the resource.</span></span> <span data-ttu-id="4b832-116">如需可能的值，請參閱 [**SysmonBatchReason**](/windows/win32/api/isysmon/ne-isysmon-sysmonbatchreason) 列舉。</span><span class="sxs-lookup"><span data-stu-id="4b832-116">For possible values, see the [**SysmonBatchReason**](/windows/win32/api/isysmon/ne-isysmon-sysmonbatchreason) enumeration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b832-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="4b832-117">Return value</span></span>

<span data-ttu-id="4b832-118">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="4b832-118">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b832-119">備註</span><span class="sxs-lookup"><span data-stu-id="4b832-119">Remarks</span></span>

<span data-ttu-id="4b832-120">您必須呼叫這個方法兩次，一次是鎖定來源 (True) 和一次，以 (False) 解除鎖定來源。</span><span class="sxs-lookup"><span data-stu-id="4b832-120">You must call this method twice, once to lock the source (True) and once to unlock the source (False).</span></span>

<span data-ttu-id="4b832-121">您只能放置一個鎖定。</span><span class="sxs-lookup"><span data-stu-id="4b832-121">You can place only one lock.</span></span> <span data-ttu-id="4b832-122">例如，如果您設定 SysmonBatchAddFiles 的鎖定，然後使用 SysmonBatchAddCounters 做為原因來進行第二次呼叫，則第二個呼叫會移除第一個呼叫所放置的鎖定。</span><span class="sxs-lookup"><span data-stu-id="4b832-122">For example, if you set the lock for SysmonBatchAddFiles and then make a second call using SysmonBatchAddCounters as the reason, the second call removes the lock placed by the first call.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b832-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="4b832-123">Requirements</span></span>



| <span data-ttu-id="4b832-124">需求</span><span class="sxs-lookup"><span data-stu-id="4b832-124">Requirement</span></span> | <span data-ttu-id="4b832-125">值</span><span class="sxs-lookup"><span data-stu-id="4b832-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4b832-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4b832-126">Minimum supported client</span></span><br/> | <span data-ttu-id="4b832-127">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4b832-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4b832-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4b832-128">Minimum supported server</span></span><br/> | <span data-ttu-id="4b832-129">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4b832-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4b832-130">DLL</span><span class="sxs-lookup"><span data-stu-id="4b832-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b832-131"><dt>Sysmon .ocx</dt></span><span class="sxs-lookup"><span data-stu-id="4b832-131"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b832-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4b832-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b832-133">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="4b832-133">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 






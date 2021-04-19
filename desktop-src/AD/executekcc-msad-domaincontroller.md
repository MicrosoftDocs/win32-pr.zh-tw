---
title: MSAD_DomainController 類別的 ExecuteKCC 方法
description: 呼叫 DsReplicaConsistencyCheck 函式，此函式會叫用知識一致性檢查程式 (KCC) 來確認複寫拓撲。
ms.assetid: 958c9a15-cde2-4c74-bd4c-c2d53551cfb0
ms.tgt_platform: multiple
keywords:
- ExecuteKCC 方法 Active Directory
- ExecuteKCC 方法 Active Directory，MSAD_DomainController 類別
- MSAD_DomainController 類別 Active Directory，ExecuteKCC 方法
topic_type:
- apiref
api_name:
- MSAD_DomainController.ExecuteKCC
api_location:
- replprov.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcce017f86042181d2e80ae3614e3fc1cbccc676
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969182"
---
# <a name="executekcc-method-of-the-msad_domaincontroller-class"></a><span data-ttu-id="1e489-106">MSAD 控制器類別的 ExecuteKCC 方法 \_</span><span class="sxs-lookup"><span data-stu-id="1e489-106">ExecuteKCC method of the MSAD\_DomainController class</span></span>

<span data-ttu-id="1e489-107">呼叫 [**DsReplicaConsistencyCheck**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaconsistencycheck) 函式，此函式會叫用知識一致性檢查程式 (KCC) 來確認複寫拓撲。</span><span class="sxs-lookup"><span data-stu-id="1e489-107">Calls the [**DsReplicaConsistencyCheck**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaconsistencycheck) function, which invokes the Knowledge Consistency Checker (KCC) to verify the replication topology.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e489-108">語法</span><span class="sxs-lookup"><span data-stu-id="1e489-108">Syntax</span></span>


```mof
void ExecuteKCC(
  [in] uint32 TaskID,
  [in] uint32 dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="1e489-109">參數</span><span class="sxs-lookup"><span data-stu-id="1e489-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e489-110">*TaskID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1e489-110">*TaskID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e489-111">KCC 應執行的工作。</span><span class="sxs-lookup"><span data-stu-id="1e489-111">The task that the KCC should execute.</span></span> <span data-ttu-id="1e489-112">**DS \_KCC \_ TASKID \_ 更新 \_ 拓撲** 是目前唯一支援的值。</span><span class="sxs-lookup"><span data-stu-id="1e489-112">**DS\_KCC\_TASKID\_UPDATE\_TOPOLOGY** is the only value that is currently supported.</span></span>

</dd> <dt>

<span data-ttu-id="1e489-113">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1e489-113">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e489-114">一組旗標，可修改 **ExecuteKCC** 方法的行為。</span><span class="sxs-lookup"><span data-stu-id="1e489-114">A set of flags that modify the behavior of the **ExecuteKCC** method.</span></span> <span data-ttu-id="1e489-115">這個參數可以是零或一或多個下列值的組合。</span><span class="sxs-lookup"><span data-stu-id="1e489-115">This parameter can be zero or a combination of one or more of the following values.</span></span>

<dt>

<span id="DS_KCC_FLAG_ASYNC_OP"></span><span id="ds_kcc_flag_async_op"></span>

<span data-ttu-id="1e489-116"><span id="DS_KCC_FLAG_ASYNC_OP"></span><span id="ds_kcc_flag_async_op"></span>**DS \_ KCC \_ 旗標 \_ 非同步 \_ OP**</span><span class="sxs-lookup"><span data-stu-id="1e489-116"><span id="DS_KCC_FLAG_ASYNC_OP"></span><span id="ds_kcc_flag_async_op"></span>**DS\_KCC\_FLAG\_ASYNC\_OP**</span></span>


</dt> <dd>

<span data-ttu-id="1e489-117">工作會排入佇列，然後函式會傳回，而不會等候工作完成。</span><span class="sxs-lookup"><span data-stu-id="1e489-117">The task is queued and then the function returns without waiting for the task to complete.</span></span>

</dd> <dt>

<span id="DS_KCC_FLAG_DAMPED"></span><span id="ds_kcc_flag_damped"></span>

<span data-ttu-id="1e489-118"><span id="DS_KCC_FLAG_DAMPED"></span><span id="ds_kcc_flag_damped"></span>**DS \_ KCC \_ 旗標 \_ 禁止**</span><span class="sxs-lookup"><span data-stu-id="1e489-118"><span id="DS_KCC_FLAG_DAMPED"></span><span id="ds_kcc_flag_damped"></span>**DS\_KCC\_FLAG\_DAMPED**</span></span>


</dt> <dd>

<span data-ttu-id="1e489-119">如果有其他已排入佇列的工作即將執行，則工作不會新增至佇列。</span><span class="sxs-lookup"><span data-stu-id="1e489-119">The task will not be added to the queue if another queued task will run soon.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e489-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="1e489-120">Return value</span></span>

<span data-ttu-id="1e489-121">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="1e489-121">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e489-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="1e489-122">Requirements</span></span>



| <span data-ttu-id="1e489-123">需求</span><span class="sxs-lookup"><span data-stu-id="1e489-123">Requirement</span></span> | <span data-ttu-id="1e489-124">值</span><span class="sxs-lookup"><span data-stu-id="1e489-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1e489-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1e489-125">Minimum supported client</span></span><br/> | <span data-ttu-id="1e489-126">都不支援</span><span class="sxs-lookup"><span data-stu-id="1e489-126">None supported</span></span><br/>                                                               |
| <span data-ttu-id="1e489-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1e489-127">Minimum supported server</span></span><br/> | <span data-ttu-id="1e489-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1e489-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1e489-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="1e489-129">Namespace</span></span><br/>                | <span data-ttu-id="1e489-130">根 \\ MicrosoftActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="1e489-130">Root\\MicrosoftActiveDirectory</span></span><br/>                                               |
| <span data-ttu-id="1e489-131">MOF</span><span class="sxs-lookup"><span data-stu-id="1e489-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1e489-132"><dt>Replprov.dll mof</dt></span><span class="sxs-lookup"><span data-stu-id="1e489-132"><dt>Replprov.mof</dt></span></span> </dl> |
| <span data-ttu-id="1e489-133">DLL</span><span class="sxs-lookup"><span data-stu-id="1e489-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e489-134"><dt>Replprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e489-134"><dt>Replprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e489-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1e489-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e489-136">**MSAD 的 \_ 控制器**</span><span class="sxs-lookup"><span data-stu-id="1e489-136">**MSAD\_DomainController**</span></span>](msad-domaincontroller.md)
</dt> </dl>

 

 






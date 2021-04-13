---
title: MSAD_ReplNeighbor 類別的 SyncNamingCoNtext 方法
description: 呼叫 DsReplicaSync 函式，此函式會將目的地命名內容與其中一個來源進行同步處理。
ms.assetid: 005053c4-8d9c-42f6-bae6-3ecdedd5ac2b
ms.tgt_platform: multiple
keywords:
- SyncNamingCoNtext 方法 Active Directory
- SyncNamingCoNtext 方法 Active Directory，MSAD_ReplNeighbor 類別
- MSAD_ReplNeighbor 類別 Active Directory，SyncNamingCoNtext 方法
topic_type:
- apiref
api_name:
- MSAD_ReplNeighbor.SyncNamingContext
api_location:
- replprov.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 691bd3e943f491ba93d867097ac0167c97be6108
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466353"
---
# <a name="syncnamingcontext-method-of-the-msad_replneighbor-class"></a><span data-ttu-id="1bab6-106">MSAD ReplNeighbor 類別的 SyncNamingCoNtext 方法 \_</span><span class="sxs-lookup"><span data-stu-id="1bab6-106">SyncNamingContext method of the MSAD\_ReplNeighbor class</span></span>

<span data-ttu-id="1bab6-107">呼叫 [**DsReplicaSync**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicasynca) 函式，此函式會將目的地命名內容與其中一個來源進行同步處理。</span><span class="sxs-lookup"><span data-stu-id="1bab6-107">Calls the [**DsReplicaSync**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicasynca) function that synchronizes a destination naming context with one of its sources.</span></span>

## <a name="syntax"></a><span data-ttu-id="1bab6-108">語法</span><span class="sxs-lookup"><span data-stu-id="1bab6-108">Syntax</span></span>


```mof
void SyncNamingContext(
  [in] uint32 Options
);
```



## <a name="parameters"></a><span data-ttu-id="1bab6-109">參數</span><span class="sxs-lookup"><span data-stu-id="1bab6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1bab6-110">*選項* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1bab6-110">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1bab6-111">決定方法如何處理要求的其他資料。</span><span class="sxs-lookup"><span data-stu-id="1bab6-111">Additional data that determines how the method processes the request.</span></span> <span data-ttu-id="1bab6-112">這個參數可以是下列值的組合。</span><span class="sxs-lookup"><span data-stu-id="1bab6-112">This parameter can be a combination of the following values.</span></span>

<dt>

<span id="DS_REPSYNC_ADD_REFERENCE"></span><span id="ds_repsync_add_reference"></span>

<span data-ttu-id="1bab6-113"><span id="DS_REPSYNC_ADD_REFERENCE"></span><span id="ds_repsync_add_reference"></span>**DS \_ REPSYNC \_ 新增 \_ 參考**</span><span class="sxs-lookup"><span data-stu-id="1bab6-113"><span id="DS_REPSYNC_ADD_REFERENCE"></span><span id="ds_repsync_add_reference"></span>**DS\_REPSYNC\_ADD\_REFERENCE**</span></span>


</dt> <dd>

<span data-ttu-id="1bab6-114">導致來源目錄服務代理程式 (DSA) 驗證 [來源複寫至] 清單中是否有本機 DSA。</span><span class="sxs-lookup"><span data-stu-id="1bab6-114">Causes the source directory system agent (DSA) to verify that the local DSA is present in the source replicates-to list.</span></span> <span data-ttu-id="1bab6-115">如果未出現本機 DSA，則會新增它。</span><span class="sxs-lookup"><span data-stu-id="1bab6-115">If the local DSA is not present, it is added.</span></span> <span data-ttu-id="1bab6-116">這可確保來源傳送變更通知。</span><span class="sxs-lookup"><span data-stu-id="1bab6-116">This ensures that the source sends change notifications.</span></span>

</dd> <dt>

<span id="DS_REPSYNC_ALL_SOURCES"></span><span id="ds_repsync_all_sources"></span>

<span data-ttu-id="1bab6-117"><span id="DS_REPSYNC_ALL_SOURCES"></span><span id="ds_repsync_all_sources"></span>**DS \_ REPSYNC \_ 所有 \_ 來源**</span><span class="sxs-lookup"><span data-stu-id="1bab6-117"><span id="DS_REPSYNC_ALL_SOURCES"></span><span id="ds_repsync_all_sources"></span>**DS\_REPSYNC\_ALL\_SOURCES**</span></span>


</dt> <dd>

<span data-ttu-id="1bab6-118">不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="1bab6-118">This value is not supported.</span></span>

<span data-ttu-id="1bab6-119">**Windows server 2008 R2、Windows server 2008 和 Windows server 2003：** 從所有來源進行同步處理。</span><span class="sxs-lookup"><span data-stu-id="1bab6-119">**Windows Server 2008 R2, Windows Server 2008 and Windows Server 2003:** Synchronizes from all sources.</span></span>

</dd> <dt>

<span id="DS_REPSYNC_ASYNCHRONOUS_OPERATION"></span><span id="ds_repsync_asynchronous_operation"></span>

<span data-ttu-id="1bab6-120"><span id="DS_REPSYNC_ASYNCHRONOUS_OPERATION"></span><span id="ds_repsync_asynchronous_operation"></span>**DS \_ REPSYNC \_ 非同步 \_ 操作**</span><span class="sxs-lookup"><span data-stu-id="1bab6-120"><span id="DS_REPSYNC_ASYNCHRONOUS_OPERATION"></span><span id="ds_repsync_asynchronous_operation"></span>**DS\_REPSYNC\_ASYNCHRONOUS\_OPERATION**</span></span>


</dt> <dd>

<span data-ttu-id="1bab6-121">以非同步方式執行此作業。</span><span class="sxs-lookup"><span data-stu-id="1bab6-121">Performs this operation asynchronously.</span></span>

<span data-ttu-id="1bab6-122">**Windows server 2008 R2、Windows server 2008 和 Windows server 2003：** 使用 **DS \_ REPSYNC \_ 所有 \_ 來源** 時的必要。</span><span class="sxs-lookup"><span data-stu-id="1bab6-122">**Windows Server 2008 R2, Windows Server 2008 and Windows Server 2003:** Required when using **DS\_REPSYNC\_ALL\_SOURCES**.</span></span>

</dd> <dt>

<span id="DS_REPSYNC_FORCE"></span><span id="ds_repsync_force"></span>

<span data-ttu-id="1bab6-123"><span id="DS_REPSYNC_FORCE"></span><span id="ds_repsync_force"></span>**DS \_ REPSYNC \_ 強制**</span><span class="sxs-lookup"><span data-stu-id="1bab6-123"><span id="DS_REPSYNC_FORCE"></span><span id="ds_repsync_force"></span>**DS\_REPSYNC\_FORCE**</span></span>


</dt> <dd>

<span data-ttu-id="1bab6-124">即使連結目前已停用，也會進行同步處理。</span><span class="sxs-lookup"><span data-stu-id="1bab6-124">Synchronizes even if the link is currently disabled.</span></span>

</dd> <dt>

<span id="DS_REPSYNC_FULL"></span><span id="ds_repsync_full"></span>

<span data-ttu-id="1bab6-125"><span id="DS_REPSYNC_FULL"></span><span id="ds_repsync_full"></span>**DS \_ REPSYNC 已 \_ 滿**</span><span class="sxs-lookup"><span data-stu-id="1bab6-125"><span id="DS_REPSYNC_FULL"></span><span id="ds_repsync_full"></span>**DS\_REPSYNC\_FULL**</span></span>


</dt> <dd>

<span data-ttu-id="1bab6-126">從第一個更新序號開始同步處理 (USN) 。</span><span class="sxs-lookup"><span data-stu-id="1bab6-126">Synchronizes starting from the first Update Sequence Number (USN).</span></span>

</dd> <dt>

<span id="DS_REPSYNC_INTERSITE_MESSAGING"></span><span id="ds_repsync_intersite_messaging"></span>

<span data-ttu-id="1bab6-127"><span id="DS_REPSYNC_INTERSITE_MESSAGING"></span><span id="ds_repsync_intersite_messaging"></span>**DS \_ REPSYNC 網站 \_ 間 \_ 訊息**</span><span class="sxs-lookup"><span data-stu-id="1bab6-127"><span id="DS_REPSYNC_INTERSITE_MESSAGING"></span><span id="ds_repsync_intersite_messaging"></span>**DS\_REPSYNC\_INTERSITE\_MESSAGING**</span></span>


</dt> <dd>

<span data-ttu-id="1bab6-128">使用 ISM 進行同步處理。</span><span class="sxs-lookup"><span data-stu-id="1bab6-128">Synchronizes using an ISM.</span></span>

</dd> <dt>

<span id="DS_REPSYNC_NO_DISCARD"></span><span id="ds_repsync_no_discard"></span>

<span data-ttu-id="1bab6-129"><span id="DS_REPSYNC_NO_DISCARD"></span><span id="ds_repsync_no_discard"></span>**DS \_ REPSYNC \_ 沒有 \_ 捨棄**</span><span class="sxs-lookup"><span data-stu-id="1bab6-129"><span id="DS_REPSYNC_NO_DISCARD"></span><span id="ds_repsync_no_discard"></span>**DS\_REPSYNC\_NO\_DISCARD**</span></span>


</dt> <dd>

<span data-ttu-id="1bab6-130">不捨棄此同步處理要求，即使類似的同步處理已暫止也一樣。</span><span class="sxs-lookup"><span data-stu-id="1bab6-130">Does not discard this synchronization request, even if a similar synchronization is pending.</span></span>

</dd> <dt>

<span id="DS_REPSYNC_PERIODIC"></span><span id="ds_repsync_periodic"></span>

<span data-ttu-id="1bab6-131"><span id="DS_REPSYNC_PERIODIC"></span><span id="ds_repsync_periodic"></span>**DS \_ REPSYNC \_ 定期**</span><span class="sxs-lookup"><span data-stu-id="1bab6-131"><span id="DS_REPSYNC_PERIODIC"></span><span id="ds_repsync_periodic"></span>**DS\_REPSYNC\_PERIODIC**</span></span>


</dt> <dd>

<span data-ttu-id="1bab6-132">指出此作業是由系統管理員排程的定期同步處理要求。</span><span class="sxs-lookup"><span data-stu-id="1bab6-132">Indicates that this operation is a periodic synchronization request that is scheduled by the administrator.</span></span>

</dd> <dt>

<span id="DS_REPSYNC_URGENT"></span><span id="ds_repsync_urgent"></span>

<span data-ttu-id="1bab6-133"><span id="DS_REPSYNC_URGENT"></span><span id="ds_repsync_urgent"></span>**DS \_ REPSYNC \_ 緊急**</span><span class="sxs-lookup"><span data-stu-id="1bab6-133"><span id="DS_REPSYNC_URGENT"></span><span id="ds_repsync_urgent"></span>**DS\_REPSYNC\_URGENT**</span></span>


</dt> <dd>

<span data-ttu-id="1bab6-134">指出此作業是標示為緊急更新的通知。</span><span class="sxs-lookup"><span data-stu-id="1bab6-134">Indicates that this operation is a notification of an update that is marked as urgent.</span></span>

</dd> <dt>

<span id="DS_REPSYNC_WRITEABLE"></span><span id="ds_repsync_writeable"></span>

<span data-ttu-id="1bab6-135"><span id="DS_REPSYNC_WRITEABLE"></span><span id="ds_repsync_writeable"></span>**DS \_ REPSYNC 可 \_ 寫入**</span><span class="sxs-lookup"><span data-stu-id="1bab6-135"><span id="DS_REPSYNC_WRITEABLE"></span><span id="ds_repsync_writeable"></span>**DS\_REPSYNC\_WRITEABLE**</span></span>


</dt> <dd>

<span data-ttu-id="1bab6-136">表示這個複本是可寫入的。</span><span class="sxs-lookup"><span data-stu-id="1bab6-136">Indicates that this replica is writable.</span></span> <span data-ttu-id="1bab6-137">如果未設定此旗標，則複本會是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="1bab6-137">If this flag is not set, the replica is read-only.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1bab6-138">傳回值</span><span class="sxs-lookup"><span data-stu-id="1bab6-138">Return value</span></span>

<span data-ttu-id="1bab6-139">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="1bab6-139">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="1bab6-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="1bab6-140">Requirements</span></span>



| <span data-ttu-id="1bab6-141">需求</span><span class="sxs-lookup"><span data-stu-id="1bab6-141">Requirement</span></span> | <span data-ttu-id="1bab6-142">值</span><span class="sxs-lookup"><span data-stu-id="1bab6-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1bab6-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1bab6-143">Minimum supported client</span></span><br/> | <span data-ttu-id="1bab6-144">都不支援</span><span class="sxs-lookup"><span data-stu-id="1bab6-144">None supported</span></span><br/>                                                               |
| <span data-ttu-id="1bab6-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1bab6-145">Minimum supported server</span></span><br/> | <span data-ttu-id="1bab6-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1bab6-146">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1bab6-147">命名空間</span><span class="sxs-lookup"><span data-stu-id="1bab6-147">Namespace</span></span><br/>                | <span data-ttu-id="1bab6-148">根 \\ MicrosoftActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="1bab6-148">Root\\MicrosoftActiveDirectory</span></span><br/>                                               |
| <span data-ttu-id="1bab6-149">MOF</span><span class="sxs-lookup"><span data-stu-id="1bab6-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1bab6-150"><dt>Replprov.dll mof</dt></span><span class="sxs-lookup"><span data-stu-id="1bab6-150"><dt>Replprov.mof</dt></span></span> </dl> |
| <span data-ttu-id="1bab6-151">DLL</span><span class="sxs-lookup"><span data-stu-id="1bab6-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1bab6-152"><dt>Replprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1bab6-152"><dt>Replprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1bab6-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1bab6-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bab6-154">**MSAD \_ ReplNeighbor**</span><span class="sxs-lookup"><span data-stu-id="1bab6-154">**MSAD\_ReplNeighbor**</span></span>](msad-replneighbor.md)
</dt> </dl>

 

 






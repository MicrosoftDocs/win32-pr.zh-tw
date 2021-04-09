---
title: " (Fwpmu) 存取右邊識別碼"
description: Windows 篩選平台 (WFP) 使用標準的 Win32 存取權限，以及一組在篩選平臺內建的 WFP 特定存取權限。
ms.assetid: 77f0a1ac-3e99-4cba-a7c6-b8747f35cd0c
topic_type:
- apiref
api_name:
- FWPM_ACTRL_ADD
- FWPM_ACTRL_ADD_LINK
- FWPM_ACTRL_BEGIN_READ_TXN
- FWPM_ACTRL_BEGIN_WRITE_TXN
- FWPM_ACTRL_CLASSIFY
- FWPM_ACTRL_ENUM
- FWPM_ACTRL_OPEN
- FWPM_ACTRL_READ
- FWPM_ACTRL_READ_STATS
- FWPM_ACTRL_SUBSCRIBE
- FWPM_ACTRL_WRITE
- FWPM_GENERIC_READ
- FWPM_GENERIC_EXECUTE
- FWPM_GENERIC_WRITE
- FWPM_GENERIC_ALL
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8af182a087ade590e278bd3dd1d2bb1a64b5c598
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935047"
---
# <a name="access-right-identifiers"></a><span data-ttu-id="8ee90-103">存取正確的識別碼</span><span class="sxs-lookup"><span data-stu-id="8ee90-103">Access Right Identifiers</span></span>

<span data-ttu-id="8ee90-104">Windows 篩選平台 (WFP) 使用 [標準的 Win32 存取權限](/windows/desktop/SecAuthZ/standard-access-rights) ，以及一組在篩選平臺內建的 WFP 特定存取權限。</span><span class="sxs-lookup"><span data-stu-id="8ee90-104">Windows Filtering Platform (WFP) uses the [standard Win32 access rights](/windows/desktop/SecAuthZ/standard-access-rights) plus a set of WFP-specific access rights built into the filtering platform.</span></span> <span data-ttu-id="8ee90-105">只有在使用者模式下，才會使用這些存取權限來保護物件的安全。</span><span class="sxs-lookup"><span data-stu-id="8ee90-105">These access rights are used to secure objects in user mode only.</span></span> <span data-ttu-id="8ee90-106">核心模式呼叫端略過所有存取檢查。</span><span class="sxs-lookup"><span data-stu-id="8ee90-106">Kernel-mode callers bypass all access checks.</span></span>

<span data-ttu-id="8ee90-107">WFP 特定的存取權限識別碼如下所示。</span><span class="sxs-lookup"><span data-stu-id="8ee90-107">WFP specific access right identifiers are as follows.</span></span>

<dl> <dt>

<span data-ttu-id="8ee90-108"><span id="FWPM_ACTRL_ADD"></span><span id="fwpm_actrl_add"></span>**FWPM \_ ACTRL \_ 新增**</span><span class="sxs-lookup"><span data-stu-id="8ee90-108"><span id="FWPM_ACTRL_ADD"></span><span id="fwpm_actrl_add"></span>**FWPM\_ACTRL\_ADD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8ee90-109">將物件新增至基底篩選引擎 (BFE) 。</span><span class="sxs-lookup"><span data-stu-id="8ee90-109">Add an object to the Base Filtering Engine (BFE).</span></span> <span data-ttu-id="8ee90-110">需要有此存取權限，才能呼叫 [**Fwpm \* Add0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0) 函數。</span><span class="sxs-lookup"><span data-stu-id="8ee90-110">This access right is needed in order to call [**Fwpm\*Add0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0) functions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8ee90-111"><span id="FWPM_ACTRL_ADD_LINK"></span><span id="fwpm_actrl_add_link"></span>**FWPM \_ ACTRL \_ 新增 \_ 連結**</span><span class="sxs-lookup"><span data-stu-id="8ee90-111"><span id="FWPM_ACTRL_ADD_LINK"></span><span id="fwpm_actrl_add_link"></span>**FWPM\_ACTRL\_ADD\_LINK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8ee90-112">新增透過連結所參考的物件。</span><span class="sxs-lookup"><span data-stu-id="8ee90-112">Add an object referenced through a link.</span></span> <span data-ttu-id="8ee90-113">例如，透過 Guid 參考的標注需要此存取權。</span><span class="sxs-lookup"><span data-stu-id="8ee90-113">For example, this access right is needed for callouts referenced through GUIDs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8ee90-114"><span id="FWPM_ACTRL_BEGIN_READ_TXN"></span><span id="fwpm_actrl_begin_read_txn"></span>**FWPM \_ ACTRL \_ 開始 \_ 閱讀 \_ TXN**</span><span class="sxs-lookup"><span data-stu-id="8ee90-114"><span id="FWPM_ACTRL_BEGIN_READ_TXN"></span><span id="fwpm_actrl_begin_read_txn"></span>**FWPM\_ACTRL\_BEGIN\_READ\_TXN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8ee90-115">開始唯讀交易。</span><span class="sxs-lookup"><span data-stu-id="8ee90-115">Begin a read-only transaction.</span></span> <span data-ttu-id="8ee90-116">需要此存取權限才能呼叫 [**FwpmTransactionBegin0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0)。</span><span class="sxs-lookup"><span data-stu-id="8ee90-116">This access right is needed in order to call [**FwpmTransactionBegin0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8ee90-117"><span id="FWPM_ACTRL_BEGIN_WRITE_TXN"></span><span id="fwpm_actrl_begin_write_txn"></span>**FWPM \_ ACTRL \_ 開始 \_ 寫入 \_ TXN**</span><span class="sxs-lookup"><span data-stu-id="8ee90-117"><span id="FWPM_ACTRL_BEGIN_WRITE_TXN"></span><span id="fwpm_actrl_begin_write_txn"></span>**FWPM\_ACTRL\_BEGIN\_WRITE\_TXN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8ee90-118">開始讀取/寫入交易。</span><span class="sxs-lookup"><span data-stu-id="8ee90-118">Begin a read/write transaction.</span></span> <span data-ttu-id="8ee90-119">需要有此存取權限，才能呼叫 [**FwpmTransactionBegin0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0) 進行讀取/寫入交易。</span><span class="sxs-lookup"><span data-stu-id="8ee90-119">This access right is needed in order to call [**FwpmTransactionBegin0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0) for a read/write transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8ee90-120"><span id="FWPM_ACTRL_CLASSIFY"></span><span id="fwpm_actrl_classify"></span>**FWPM \_ ACTRL \_ 分類**</span><span class="sxs-lookup"><span data-stu-id="8ee90-120"><span id="FWPM_ACTRL_CLASSIFY"></span><span id="fwpm_actrl_classify"></span>**FWPM\_ACTRL\_CLASSIFY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8ee90-121">將遠端程序呼叫分類 (RPC) 。</span><span class="sxs-lookup"><span data-stu-id="8ee90-121">Classify Remote Procedure Call (RPC).</span></span> <span data-ttu-id="8ee90-122">RPC 執行時間需要此存取權，才能強制執行 RPC 篩選器。</span><span class="sxs-lookup"><span data-stu-id="8ee90-122">This access right is needed by the RPC run-time in order to enforce RPC filters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8ee90-123"><span id="FWPM_ACTRL_ENUM"></span><span id="fwpm_actrl_enum"></span>**FWPM \_ ACTRL \_ 列舉**</span><span class="sxs-lookup"><span data-stu-id="8ee90-123"><span id="FWPM_ACTRL_ENUM"></span><span id="fwpm_actrl_enum"></span>**FWPM\_ACTRL\_ENUM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8ee90-124">枚舉。</span><span class="sxs-lookup"><span data-stu-id="8ee90-124">Enumerate.</span></span> <span data-ttu-id="8ee90-125">需要有此存取權限，才能呼叫 [**Fwpm \* CreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutcreateenumhandle0) 函數。</span><span class="sxs-lookup"><span data-stu-id="8ee90-125">This access right is needed in order to call [**Fwpm\*CreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutcreateenumhandle0) functions.</span></span> <span data-ttu-id="8ee90-126">若要列舉物件，呼叫端也需要 \_ \_ 物件的 FWPM ACTRL READ 存取權。</span><span class="sxs-lookup"><span data-stu-id="8ee90-126">To enumerate an object, the caller also needs FWPM\_ACTRL\_READ access to the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8ee90-127"><span id="FWPM_ACTRL_OPEN"></span><span id="fwpm_actrl_open"></span>**FWPM \_ ACTRL \_ OPEN**</span><span class="sxs-lookup"><span data-stu-id="8ee90-127"><span id="FWPM_ACTRL_OPEN"></span><span id="fwpm_actrl_open"></span>**FWPM\_ACTRL\_OPEN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8ee90-128">開啟篩選引擎的會話。</span><span class="sxs-lookup"><span data-stu-id="8ee90-128">Open a session to the filter engine.</span></span> <span data-ttu-id="8ee90-129">需要此存取權限才能呼叫 [**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0)。</span><span class="sxs-lookup"><span data-stu-id="8ee90-129">This access right is needed in order to call [**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8ee90-130"><span id="FWPM_ACTRL_READ"></span><span id="fwpm_actrl_read"></span>**FWPM \_ ACTRL \_ READ**</span><span class="sxs-lookup"><span data-stu-id="8ee90-130"><span id="FWPM_ACTRL_READ"></span><span id="fwpm_actrl_read"></span>**FWPM\_ACTRL\_READ**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8ee90-131">讀取。</span><span class="sxs-lookup"><span data-stu-id="8ee90-131">Read.</span></span> <span data-ttu-id="8ee90-132">需要有此存取權限，才能呼叫 [**Fwpm \* GetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutgetbyid0) 和 [**Fwpm \* GetByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutgetbykey0) 函數。</span><span class="sxs-lookup"><span data-stu-id="8ee90-132">This access right is needed in order to call [**Fwpm\*GetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutgetbyid0) and [**Fwpm\*GetByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutgetbykey0) functions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8ee90-133"><span id="FWPM_ACTRL_READ_STATS"></span><span id="fwpm_actrl_read_stats"></span>**FWPM \_ ACTRL \_ READ \_ STATS**</span><span class="sxs-lookup"><span data-stu-id="8ee90-133"><span id="FWPM_ACTRL_READ_STATS"></span><span id="fwpm_actrl_read_stats"></span>**FWPM\_ACTRL\_READ\_STATS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8ee90-134">讀取統計資料。</span><span class="sxs-lookup"><span data-stu-id="8ee90-134">Read statistics.</span></span> <span data-ttu-id="8ee90-135">需要有此存取權限，才能呼叫 [**IPsecGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecgetstatistics0) 和 [**IkeextGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextgetstatistics0)。</span><span class="sxs-lookup"><span data-stu-id="8ee90-135">This access right is needed in order to call [**IPsecGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecgetstatistics0) and [**IkeextGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextgetstatistics0).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8ee90-136"><span id="FWPM_ACTRL_SUBSCRIBE"></span><span id="fwpm_actrl_subscribe"></span>**FWPM \_ ACTRL \_ 訂閱**</span><span class="sxs-lookup"><span data-stu-id="8ee90-136"><span id="FWPM_ACTRL_SUBSCRIBE"></span><span id="fwpm_actrl_subscribe"></span>**FWPM\_ACTRL\_SUBSCRIBE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8ee90-137">訂閱。</span><span class="sxs-lookup"><span data-stu-id="8ee90-137">Subscribe.</span></span> <span data-ttu-id="8ee90-138">需要有此存取權限，才能呼叫 [**Fwpm \* SubscribeChanges0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidersubscribechanges0) 函數。</span><span class="sxs-lookup"><span data-stu-id="8ee90-138">This access right is needed in order to call [**Fwpm\*SubscribeChanges0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidersubscribechanges0) functions.</span></span> <span data-ttu-id="8ee90-139">若要接收物件的通知，訂閱者也需要 \_ \_ 物件的 FWPM ACTRL READ 存取權。</span><span class="sxs-lookup"><span data-stu-id="8ee90-139">To receive a notification for an object, a subscriber also needs FWPM\_ACTRL\_READ access to the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8ee90-140"><span id="FWPM_ACTRL_WRITE"></span><span id="fwpm_actrl_write"></span>**FWPM \_ ACTRL \_ 寫入**</span><span class="sxs-lookup"><span data-stu-id="8ee90-140"><span id="FWPM_ACTRL_WRITE"></span><span id="fwpm_actrl_write"></span>**FWPM\_ACTRL\_WRITE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8ee90-141">撰寫引擎選項。</span><span class="sxs-lookup"><span data-stu-id="8ee90-141">Write engine options.</span></span> <span data-ttu-id="8ee90-142">需要此存取權限才能呼叫 [**FwpmEngineSetOption0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0)。</span><span class="sxs-lookup"><span data-stu-id="8ee90-142">This access right is needed in order to call [**FwpmEngineSetOption0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8ee90-143"><span id="FWPM_GENERIC_READ"></span><span id="fwpm_generic_read"></span>**FWPM \_ 一般 \_ 讀取**</span><span class="sxs-lookup"><span data-stu-id="8ee90-143"><span id="FWPM_GENERIC_READ"></span><span id="fwpm_generic_read"></span>**FWPM\_GENERIC\_READ**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8ee90-144">標準 \_ 許可權 \_ 讀取 \| FWPM \_ ACTRL \_ 開始 \_ 閱讀 \_ TXN \| FWPM \_ ACTRL \_ 分類 \| FWPM \_ ACTRL \_ 開啟 \| FWPM \_ ACTRL \_ 讀取 \| FWPM \_ ACTRL \_ 讀取 \_ 統計資料</span><span class="sxs-lookup"><span data-stu-id="8ee90-144">STANDARD\_RIGHTS\_READ \| FWPM\_ACTRL\_BEGIN\_READ\_TXN \| FWPM\_ACTRL\_CLASSIFY \| FWPM\_ACTRL\_OPEN \| FWPM\_ACTRL\_READ \| FWPM\_ACTRL\_READ\_STATS</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8ee90-145"><span id="FWPM_GENERIC_EXECUTE"></span><span id="fwpm_generic_execute"></span>**FWPM \_ 一般 \_ 執行**</span><span class="sxs-lookup"><span data-stu-id="8ee90-145"><span id="FWPM_GENERIC_EXECUTE"></span><span id="fwpm_generic_execute"></span>**FWPM\_GENERIC\_EXECUTE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8ee90-146">標準 \_ RIGHTS \_ EXECUTE \| FWPM \_ ACTRL \_ ENUM \| FWPM \_ ACTRL \_ 訂閱</span><span class="sxs-lookup"><span data-stu-id="8ee90-146">STANDARD\_RIGHTS\_EXECUTE \| FWPM\_ACTRL\_ENUM \| FWPM\_ACTRL\_SUBSCRIBE</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8ee90-147"><span id="FWPM_GENERIC_WRITE"></span><span id="fwpm_generic_write"></span>**FWPM \_ 一般 \_ 寫入**</span><span class="sxs-lookup"><span data-stu-id="8ee90-147"><span id="FWPM_GENERIC_WRITE"></span><span id="fwpm_generic_write"></span>**FWPM\_GENERIC\_WRITE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8ee90-148">標準 \_ 許可權 \_ 寫入 \| 刪除 \| FWPM \_ ACTRL \_ 新增 \| FWPM \_ ACTRL \_ 新增 \_ 連結 \| FWPM \_ ACTRL \_ 開始 \_ 寫入 \_ TXN \| \_ \_ FWPM ACTRL 寫入</span><span class="sxs-lookup"><span data-stu-id="8ee90-148">STANDARD\_RIGHTS\_WRITE \| DELETE \| FWPM\_ACTRL\_ADD \| FWPM\_ACTRL\_ADD\_LINK \| FWPM\_ACTRL\_BEGIN\_WRITE\_TXN \| FWPM\_ACTRL\_WRITE</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8ee90-149"><span id="FWPM_GENERIC_ALL"></span><span id="fwpm_generic_all"></span>**FWPM \_ 泛型 \_ 全部**</span><span class="sxs-lookup"><span data-stu-id="8ee90-149"><span id="FWPM_GENERIC_ALL"></span><span id="fwpm_generic_all"></span>**FWPM\_GENERIC\_ALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8ee90-150">標準 \_ 許可權 \_ 需要 \| FWPM \_ ACTRL \_ ADD \| FWPM \_ ACTRL \_ ADD \_ LINK \| FWPM \_ ACTRL \_ BEGIN \_ READ \_ TXN \| FWPM \_ ACTRL \_ BEGIN \_ WRITE \_ TXN \| FWPM \_ ACTRL FWPM ACTRL \_ \| \_ FWPM \_ ENUM \| ACTRL \_ FWPM \_ OPEN \| ACTRL \_ FWPM \_ READ \| ACTRL \_ FWPM \_ READ \_ STATS \| ACTRL \_ FWPM \_ 訂閱 \| ACTRL \_ \_ WRITE</span><span class="sxs-lookup"><span data-stu-id="8ee90-150">STANDARD\_RIGHTS\_REQUIRED \| FWPM\_ACTRL\_ADD \| FWPM\_ACTRL\_ADD\_LINK \| FWPM\_ACTRL\_BEGIN\_READ\_TXN \| FWPM\_ACTRL\_BEGIN\_WRITE\_TXN \| FWPM\_ACTRL\_CLASSIFY \| FWPM\_ACTRL\_ENUM \| FWPM\_ACTRL\_OPEN \| FWPM\_ACTRL\_READ \| FWPM\_ACTRL\_READ\_STATS \| FWPM\_ACTRL\_SUBSCRIBE \| FWPM\_ACTRL\_WRITE</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8ee90-151">規格需求</span><span class="sxs-lookup"><span data-stu-id="8ee90-151">Requirements</span></span>



| <span data-ttu-id="8ee90-152">需求</span><span class="sxs-lookup"><span data-stu-id="8ee90-152">Requirement</span></span> | <span data-ttu-id="8ee90-153">值</span><span class="sxs-lookup"><span data-stu-id="8ee90-153">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8ee90-154">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8ee90-154">Minimum supported client</span></span><br/> | <span data-ttu-id="8ee90-155">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8ee90-155">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="8ee90-156">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8ee90-156">Minimum supported server</span></span><br/> | <span data-ttu-id="8ee90-157">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8ee90-157">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="8ee90-158">標頭</span><span class="sxs-lookup"><span data-stu-id="8ee90-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ee90-159"><dt>Fwpmu。h</dt></span><span class="sxs-lookup"><span data-stu-id="8ee90-159"><dt>Fwpmu.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ee90-160">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8ee90-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ee90-161">Windows 篩選平台存取控制模型</span><span class="sxs-lookup"><span data-stu-id="8ee90-161">Windows Filtering Platform Access Control Model</span></span>](access-control.md)
</dt> <dt>

[<span data-ttu-id="8ee90-162">標準存取權限</span><span class="sxs-lookup"><span data-stu-id="8ee90-162">Standard Access Rights</span></span>](/windows/desktop/SecAuthZ/standard-access-rights)
</dt> </dl>

 


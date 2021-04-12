---
title: MSAD_ReplPendingOp 類別
description: 表示 DS 複寫 \_ 作業 \_ 結構，描述目前正在執行或暫止執行的複寫工作。
ms.assetid: d1c101fa-ae33-48da-9b00-93fde553a4f9
ms.tgt_platform: multiple
keywords:
- MSAD_ReplPendingOp 類別 Active Directory
- MSAD_ReplPendingOp 類別 Active Directory，描述
topic_type:
- apiref
api_name:
- MSAD_ReplPendingOp
- MSAD_ReplPendingOp.SerialNumber
- MSAD_ReplPendingOp.PositionInQ
- MSAD_ReplPendingOp.OpStartTime
- MSAD_ReplPendingOp.TimeEnqueued
- MSAD_ReplPendingOp.Priority
- MSAD_ReplPendingOp.OpType
- MSAD_ReplPendingOp.Options
- MSAD_ReplPendingOp.NamingContextDN
- MSAD_ReplPendingOp.NamingContextObjGuid
- MSAD_ReplPendingOp.DsaDN
- MSAD_ReplPendingOp.DsaAddress
- MSAD_ReplPendingOp.DsaObjGuid
api_location:
- replprov.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f1c3faddac915f602104d7e5dc4e9b6bc7d6944
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384681"
---
# <a name="msad_replpendingop-class"></a><span data-ttu-id="8f642-105">MSAD \_ ReplPendingOp 類別</span><span class="sxs-lookup"><span data-stu-id="8f642-105">MSAD\_ReplPendingOp class</span></span>

<span data-ttu-id="8f642-106">表示 [**DS 複寫 \_ 作業 \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_opw) 結構，描述目前正在執行或暫止執行的複寫工作。</span><span class="sxs-lookup"><span data-stu-id="8f642-106">Represents the [**DS\_REPL\_OP**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_opw) structure, which describes a replication task that is currently executing or pending execution.</span></span> <span data-ttu-id="8f642-107">[**DsReplicaGetInfo**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicagetinfow)函數會傳回這個結構。</span><span class="sxs-lookup"><span data-stu-id="8f642-107">This structure is returned by the [**DsReplicaGetInfo**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicagetinfow) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f642-108">語法</span><span class="sxs-lookup"><span data-stu-id="8f642-108">Syntax</span></span>

``` syntax
[dynamic, provider("ReplProv1")]
class MSAD_ReplPendingOp
{
  uint32   SerialNumber;
  uint32   PositionInQ;
  datetime OpStartTime;
  datetime TimeEnqueued;
  uint32   Priority;
  uint32   OpType;
  uint32   Options;
  String   NamingContextDN;
  String   NamingContextObjGuid;
  String   DsaDN;
  String   DsaAddress;
  String   DsaObjGuid;
};
```

## <a name="members"></a><span data-ttu-id="8f642-109">成員</span><span class="sxs-lookup"><span data-stu-id="8f642-109">Members</span></span>

<span data-ttu-id="8f642-110">**MSAD \_ ReplPendingOp** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="8f642-110">The **MSAD\_ReplPendingOp** class has these types of members:</span></span>

-   [<span data-ttu-id="8f642-111">屬性</span><span class="sxs-lookup"><span data-stu-id="8f642-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8f642-112">屬性</span><span class="sxs-lookup"><span data-stu-id="8f642-112">Properties</span></span>

<span data-ttu-id="8f642-113">**MSAD \_ ReplPendingOp** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="8f642-113">The **MSAD\_ReplPendingOp** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8f642-114">**DsaAddress**</span><span class="sxs-lookup"><span data-stu-id="8f642-114">**DsaAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f642-115">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8f642-115">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="8f642-116">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f642-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f642-117">取得與此作業相關聯之遠端伺服器的傳輸特定網路位址。</span><span class="sxs-lookup"><span data-stu-id="8f642-117">Gets the transport-specific network address of the remote server that is associated with this operation.</span></span> <span data-ttu-id="8f642-118">如果沒有與這項作業相關聯的遠端伺服器，則 **為 Null** 。</span><span class="sxs-lookup"><span data-stu-id="8f642-118">**NULL** if there is no remote server that is associated with this operation.</span></span>

</dd> <dt>

<span data-ttu-id="8f642-119">**DsaDN**</span><span class="sxs-lookup"><span data-stu-id="8f642-119">**DsaDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f642-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8f642-120">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="8f642-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f642-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f642-122">取得與此作業對應的遠端伺服器相關聯的 DSA 的 X-y 路徑。</span><span class="sxs-lookup"><span data-stu-id="8f642-122">Gets the X.500 path of the DSA that is associated with the remote server that corresponds to this operation.</span></span> <span data-ttu-id="8f642-123">如果沒有與此作業對應的遠端伺服器，則 **為 Null** 。</span><span class="sxs-lookup"><span data-stu-id="8f642-123">**NULL** if no remote server corresponds to this operation.</span></span>

</dd> <dt>

<span data-ttu-id="8f642-124">**DsaObjGuid**</span><span class="sxs-lookup"><span data-stu-id="8f642-124">**DsaObjGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f642-125">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8f642-125">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="8f642-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f642-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f642-127">取得 **DsaDN** 屬性所識別 DSA 的 [**objectGuid**](/windows/desktop/ADSchema/a-objectguid)屬性值。</span><span class="sxs-lookup"><span data-stu-id="8f642-127">Gets the value of the [**objectGuid**](/windows/desktop/ADSchema/a-objectguid) attribute of the DSA that is identified by the **DsaDN** property.</span></span>

</dd> <dt>

<span data-ttu-id="8f642-128">**NamingCoNtextDN**</span><span class="sxs-lookup"><span data-stu-id="8f642-128">**NamingContextDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f642-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8f642-129">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="8f642-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f642-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f642-131">取得與這項作業相關聯之命名內容 (NC) 的 x.500 路徑。</span><span class="sxs-lookup"><span data-stu-id="8f642-131">Gets the X.500 path of the naming context (NC) that is associated with this operation.</span></span>

</dd> <dt>

<span data-ttu-id="8f642-132">**NamingCoNtextObjGuid**</span><span class="sxs-lookup"><span data-stu-id="8f642-132">**NamingContextObjGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f642-133">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8f642-133">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="8f642-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f642-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f642-135">取得 **NamingCoNtextDN** 屬性所識別之 NC 的 [**objectGuid**](/windows/desktop/ADSchema/a-objectguid)屬性。</span><span class="sxs-lookup"><span data-stu-id="8f642-135">Gets the [**objectGuid**](/windows/desktop/ADSchema/a-objectguid) attribute of the NC that is identified by the **NamingContextDN** property.</span></span>

</dd> <dt>

<span data-ttu-id="8f642-136">**OpStartTime**</span><span class="sxs-lookup"><span data-stu-id="8f642-136">**OpStartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f642-137">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="8f642-137">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8f642-138">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f642-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f642-139">取得作業開始的時間。</span><span class="sxs-lookup"><span data-stu-id="8f642-139">Gets the time when the operation was started.</span></span> <span data-ttu-id="8f642-140">如果這項作業仍在佇列中，則 **為 Null** 。</span><span class="sxs-lookup"><span data-stu-id="8f642-140">**NULL** if this operation is still in the queue.</span></span>

</dd> <dt>

<span data-ttu-id="8f642-141">**選項**</span><span class="sxs-lookup"><span data-stu-id="8f642-141">**Options**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f642-142">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8f642-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f642-143">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f642-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f642-144">取得一組旗標，這些旗標會提供有關作業的其他資料。</span><span class="sxs-lookup"><span data-stu-id="8f642-144">Gets the set of flags that provides additional data about the operation.</span></span> <span data-ttu-id="8f642-145">此成員的內容是由 **OpType** 屬性的值所決定。</span><span class="sxs-lookup"><span data-stu-id="8f642-145">The contents of this member are determined by the value of the **OpType** property.</span></span>

<dt>

<span id="DS_REPL_OP_TYPE_SYNC"></span><span id="ds_repl_op_type_sync"></span>

<span data-ttu-id="8f642-146"><span id="DS_REPL_OP_TYPE_SYNC"></span><span id="ds_repl_op_type_sync"></span>**DS \_ 複製 \_ 作業 \_ 類型 \_ 同步處理**</span><span class="sxs-lookup"><span data-stu-id="8f642-146"><span id="DS_REPL_OP_TYPE_SYNC"></span><span id="ds_repl_op_type_sync"></span>**DS\_REPL\_OP\_TYPE\_SYNC**</span></span>


</dt> <dd>

<span data-ttu-id="8f642-147">包含在 [**DsReplicaSync**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicasynca)中針對 _Options \* 參數定義的一或多個 \**DS \_ REPSYNC \_ \** _ 值的零或組合。</span><span class="sxs-lookup"><span data-stu-id="8f642-147">Contains zero or a combination of one or more of the **DS\_REPSYNC\_\** _ values as defined for the _Options* parameter in [**DsReplicaSync**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicasynca).</span></span>

</dd> <dt>

<span id="DS_REPL_OP_TYPE_ADD"></span><span id="ds_repl_op_type_add"></span>

<span data-ttu-id="8f642-148"><span id="DS_REPL_OP_TYPE_ADD"></span><span id="ds_repl_op_type_add"></span>**DS \_ 複製 \_ 作業 \_ 類型 \_ 新增**</span><span class="sxs-lookup"><span data-stu-id="8f642-148"><span id="DS_REPL_OP_TYPE_ADD"></span><span id="ds_repl_op_type_add"></span>**DS\_REPL\_OP\_TYPE\_ADD**</span></span>


</dt> <dd>

<span data-ttu-id="8f642-149">包含在 [**DsReplicaAdd**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaadda)中針對 _Options \* 參數定義的一或多個 \**DS \_ REPADD \_ \** _ 值的零或組合。</span><span class="sxs-lookup"><span data-stu-id="8f642-149">Contains zero or a combination of one or more of the **DS\_REPADD\_\** _ values as defined for the _Options* parameter in [**DsReplicaAdd**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaadda).</span></span>

</dd> <dt>

<span id="DS_REPL_OP_TYPE_DELETE"></span><span id="ds_repl_op_type_delete"></span>

<span data-ttu-id="8f642-150"><span id="DS_REPL_OP_TYPE_DELETE"></span><span id="ds_repl_op_type_delete"></span>**DS \_ 複製 \_ 作業 \_ 類型 \_ 刪除**</span><span class="sxs-lookup"><span data-stu-id="8f642-150"><span id="DS_REPL_OP_TYPE_DELETE"></span><span id="ds_repl_op_type_delete"></span>**DS\_REPL\_OP\_TYPE\_DELETE**</span></span>


</dt> <dd>

<span data-ttu-id="8f642-151">包含在 [**DsReplicaDel**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicadela)中針對 _Options \* 參數定義的一或多個 \**DS \_ REPDEL \_ \** _ 值的零或組合。</span><span class="sxs-lookup"><span data-stu-id="8f642-151">Contains zero or a combination of one or more of the **DS\_REPDEL\_\** _ values as defined for the _Options* parameter in [**DsReplicaDel**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicadela).</span></span>

</dd> <dt>

<span id="DS_REPL_OP_TYPE_MODIFY"></span><span id="ds_repl_op_type_modify"></span>

<span data-ttu-id="8f642-152"><span id="DS_REPL_OP_TYPE_MODIFY"></span><span id="ds_repl_op_type_modify"></span>**DS \_ 複製 \_ 作業 \_ 類型 \_ 修改**</span><span class="sxs-lookup"><span data-stu-id="8f642-152"><span id="DS_REPL_OP_TYPE_MODIFY"></span><span id="ds_repl_op_type_modify"></span>**DS\_REPL\_OP\_TYPE\_MODIFY**</span></span>


</dt> <dd>

<span data-ttu-id="8f642-153">包含在 [**DsReplicaModify**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicamodifya)中針對 _Options \* 參數定義的一或多個 \**DS \_ REPMOD \_ \** _ 值的零或組合。</span><span class="sxs-lookup"><span data-stu-id="8f642-153">Contains zero or a combination of one or more of the **DS\_REPMOD\_\** _ values as defined for the _Options* parameter in [**DsReplicaModify**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicamodifya).</span></span>

</dd> <dt>

<span id="DS_REPL_OP_TYPE_UPDATE_REFS"></span><span id="ds_repl_op_type_update_refs"></span>

<span data-ttu-id="8f642-154"><span id="DS_REPL_OP_TYPE_UPDATE_REFS"></span><span id="ds_repl_op_type_update_refs"></span>**DS 複寫作業 \_ \_ \_ 類型 \_ 更新 \_ REFS**</span><span class="sxs-lookup"><span data-stu-id="8f642-154"><span id="DS_REPL_OP_TYPE_UPDATE_REFS"></span><span id="ds_repl_op_type_update_refs"></span>**DS\_REPL\_OP\_TYPE\_UPDATE\_REFS**</span></span>


</dt> <dd>

<span data-ttu-id="8f642-155">包含在 [**DsReplicaUpdateRefs**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaupdaterefsa)中針對 _Options \* 參數定義的一或多個 \**DS \_ REPSUPD \_ \** _ 值的零或組合。</span><span class="sxs-lookup"><span data-stu-id="8f642-155">Contains zero or a combination of one or more of the **DS\_REPSUPD\_\** _ values as defined for the _Options* parameter in [**DsReplicaUpdateRefs**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaupdaterefsa).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f642-156">**OpType**</span><span class="sxs-lookup"><span data-stu-id="8f642-156">**OpType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f642-157">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8f642-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f642-158">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f642-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f642-159">取得 [**DS 複寫 \_ 操作 \_ \_ 類型**](/windows/desktop/api/Ntdsapi/ne-ntdsapi-ds_repl_op_type) 值，指出這個類別所代表的作業類型。</span><span class="sxs-lookup"><span data-stu-id="8f642-159">Gets the [**DS\_REPL\_OP\_TYPE**](/windows/desktop/api/Ntdsapi/ne-ntdsapi-ds_repl_op_type) value that indicates the type of operation that this class represents.</span></span>

</dd> <dt>

<span data-ttu-id="8f642-160">**PositionInQ**</span><span class="sxs-lookup"><span data-stu-id="8f642-160">**PositionInQ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f642-161">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8f642-161">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f642-162">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f642-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f642-163">取得此作業在佇列中的位置。</span><span class="sxs-lookup"><span data-stu-id="8f642-163">Gets the position of this operation in the queue.</span></span>

</dd> <dt>

<span data-ttu-id="8f642-164">**優先順序**</span><span class="sxs-lookup"><span data-stu-id="8f642-164">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f642-165">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8f642-165">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f642-166">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f642-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f642-167">取得這項作業的優先順序。</span><span class="sxs-lookup"><span data-stu-id="8f642-167">Gets the priority of this operation.</span></span> <span data-ttu-id="8f642-168">較高優先順序的工作會先執行。</span><span class="sxs-lookup"><span data-stu-id="8f642-168">Higher-priority tasks are executed first.</span></span> <span data-ttu-id="8f642-169">優先順序是由伺服器根據此類別所代表的作業類型和作業的參數來計算。</span><span class="sxs-lookup"><span data-stu-id="8f642-169">The priority is calculated by the server based on the type of operation that this class represents and the parameters of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="8f642-170">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="8f642-170">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f642-171">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8f642-171">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f642-172">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f642-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f642-173">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8f642-173">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8f642-174">取得作業的識別碼，這是每一電腦和每次開機的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="8f642-174">Gets the ID of the operation, which is unique per-machine and per-boot.</span></span>

</dd> <dt>

<span data-ttu-id="8f642-175">**TimeEnqueued**</span><span class="sxs-lookup"><span data-stu-id="8f642-175">**TimeEnqueued**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f642-176">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="8f642-176">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8f642-177">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f642-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f642-178">取得將此作業排入佇列的時間。</span><span class="sxs-lookup"><span data-stu-id="8f642-178">Gets the time at which this operation was added to the queue.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8f642-179">規格需求</span><span class="sxs-lookup"><span data-stu-id="8f642-179">Requirements</span></span>



| <span data-ttu-id="8f642-180">需求</span><span class="sxs-lookup"><span data-stu-id="8f642-180">Requirement</span></span> | <span data-ttu-id="8f642-181">值</span><span class="sxs-lookup"><span data-stu-id="8f642-181">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8f642-182">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8f642-182">Minimum supported client</span></span><br/> | <span data-ttu-id="8f642-183">都不支援</span><span class="sxs-lookup"><span data-stu-id="8f642-183">None supported</span></span><br/>                                                               |
| <span data-ttu-id="8f642-184">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8f642-184">Minimum supported server</span></span><br/> | <span data-ttu-id="8f642-185">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8f642-185">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8f642-186">命名空間</span><span class="sxs-lookup"><span data-stu-id="8f642-186">Namespace</span></span><br/>                | <span data-ttu-id="8f642-187">根 \\ MicrosoftActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="8f642-187">Root\\MicrosoftActiveDirectory</span></span><br/>                                               |
| <span data-ttu-id="8f642-188">MOF</span><span class="sxs-lookup"><span data-stu-id="8f642-188">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8f642-189"><dt>Replprov.dll mof</dt></span><span class="sxs-lookup"><span data-stu-id="8f642-189"><dt>Replprov.mof</dt></span></span> </dl> |
| <span data-ttu-id="8f642-190">DLL</span><span class="sxs-lookup"><span data-stu-id="8f642-190">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f642-191"><dt>Replprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f642-191"><dt>Replprov.dll</dt></span></span> </dl> |



 


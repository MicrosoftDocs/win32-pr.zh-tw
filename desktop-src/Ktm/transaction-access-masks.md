---
description: KTM 會定義下列交易存取遮罩，以在開啟交易時使用。
ms.assetid: 93ef3098-b3cc-4b24-ae82-1c10d937f14f
title: '交易存取遮罩 (WinNT. h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b815bcb04a97dbd059c85c6c615a7d607bf77ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107000110"
---
# <a name="transaction-access-masks"></a><span data-ttu-id="1fa2d-103">交易存取遮罩</span><span class="sxs-lookup"><span data-stu-id="1fa2d-103">Transaction Access Masks</span></span>

<span data-ttu-id="1fa2d-104">KTM 會定義下列交易存取遮罩，以在開啟交易時使用。</span><span class="sxs-lookup"><span data-stu-id="1fa2d-104">KTM defines the following transaction access masks to be used when opening a transaction.</span></span>

<dl> <dt>

<span data-ttu-id="1fa2d-105"><span id="TRANSACTION_QUERY_INFORMATION"></span><span id="transaction_query_information"></span>**交易 \_ 查詢 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="1fa2d-105"><span id="TRANSACTION_QUERY_INFORMATION"></span><span id="transaction_query_information"></span>**TRANSACTION\_QUERY\_INFORMATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fa2d-106">0x000001</span><span class="sxs-lookup"><span data-stu-id="1fa2d-106">0x000001</span></span>
</dt> <dt>



<span data-ttu-id="1fa2d-107">呼叫者可以查詢交易資訊。</span><span class="sxs-lookup"><span data-stu-id="1fa2d-107">The caller can query transaction information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1fa2d-108"><span id="TRANSACTION_SET_INFORMATION"></span><span id="transaction_set_information"></span>**交易 \_ 集 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="1fa2d-108"><span id="TRANSACTION_SET_INFORMATION"></span><span id="transaction_set_information"></span>**TRANSACTION\_SET\_INFORMATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fa2d-109">0x000002</span><span class="sxs-lookup"><span data-stu-id="1fa2d-109">0x000002</span></span>
</dt> <dt>



<span data-ttu-id="1fa2d-110">呼叫端可以設定交易資訊。</span><span class="sxs-lookup"><span data-stu-id="1fa2d-110">The caller can set transaction information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1fa2d-111"><span id="TRANSACTION_ENLIST"></span><span id="transaction_enlist"></span>**交易 \_ 登記**</span><span class="sxs-lookup"><span data-stu-id="1fa2d-111"><span id="TRANSACTION_ENLIST"></span><span id="transaction_enlist"></span>**TRANSACTION\_ENLIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fa2d-112">0x000004</span><span class="sxs-lookup"><span data-stu-id="1fa2d-112">0x000004</span></span>
</dt> <dt>



<span data-ttu-id="1fa2d-113">呼叫者可以在此交易中登記。</span><span class="sxs-lookup"><span data-stu-id="1fa2d-113">The caller can enlist in this transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1fa2d-114"><span id="TRANSACTION_COMMIT"></span><span id="transaction_commit"></span>**交易 \_ 認可**</span><span class="sxs-lookup"><span data-stu-id="1fa2d-114"><span id="TRANSACTION_COMMIT"></span><span id="transaction_commit"></span>**TRANSACTION\_COMMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fa2d-115">0x000008</span><span class="sxs-lookup"><span data-stu-id="1fa2d-115">0x000008</span></span>
</dt> <dt>



<span data-ttu-id="1fa2d-116">呼叫者可以認可此交易。</span><span class="sxs-lookup"><span data-stu-id="1fa2d-116">The caller can commit this transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1fa2d-117"><span id="TRANSACTION_ROLLBACK"></span><span id="transaction_rollback"></span>**交易 \_ 回復**</span><span class="sxs-lookup"><span data-stu-id="1fa2d-117"><span id="TRANSACTION_ROLLBACK"></span><span id="transaction_rollback"></span>**TRANSACTION\_ROLLBACK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fa2d-118">0x000010</span><span class="sxs-lookup"><span data-stu-id="1fa2d-118">0x000010</span></span>
</dt> <dt>



<span data-ttu-id="1fa2d-119">呼叫端可以回復此交易。</span><span class="sxs-lookup"><span data-stu-id="1fa2d-119">The caller can roll back this transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1fa2d-120"><span id="TRANSACTION_PROPAGATE"></span><span id="transaction_propagate"></span>**交易 \_ 傳播**</span><span class="sxs-lookup"><span data-stu-id="1fa2d-120"><span id="TRANSACTION_PROPAGATE"></span><span id="transaction_propagate"></span>**TRANSACTION\_PROPAGATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fa2d-121">0x000020</span><span class="sxs-lookup"><span data-stu-id="1fa2d-121">0x000020</span></span>
</dt> <dt>



<span data-ttu-id="1fa2d-122">呼叫端可以將此交易傳播至上層資源管理員，例如分散式交易協調器 (DTC) 。</span><span class="sxs-lookup"><span data-stu-id="1fa2d-122">The caller can propagate this transaction to a superior resource manager, such as the Distributed Transaction Coordinator (DTC).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1fa2d-123"><span id="TRANSACTION_GENERIC_READ"></span><span id="transaction_generic_read"></span>**交易 \_ 一般 \_ 讀取**</span><span class="sxs-lookup"><span data-stu-id="1fa2d-123"><span id="TRANSACTION_GENERIC_READ"></span><span id="transaction_generic_read"></span>**TRANSACTION\_GENERIC\_READ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fa2d-124">0x120001</span><span class="sxs-lookup"><span data-stu-id="1fa2d-124">0x120001</span></span>
</dt> <dt>



<span data-ttu-id="1fa2d-125">呼叫端具有下列許可權： **標準 \_ 許可權 \_ 讀取**、 **交易 \_ 查詢 \_ 資訊**，以及 **同步處理**。</span><span class="sxs-lookup"><span data-stu-id="1fa2d-125">The caller has the following privileges: **STANDARD\_RIGHTS\_READ**, **TRANSACTION\_QUERY\_INFORMATION**, and **SYNCHRONIZE**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1fa2d-126"><span id="TRANSACTION_GENERIC_WRITE"></span><span id="transaction_generic_write"></span>**交易 \_ 一般 \_ 寫入**</span><span class="sxs-lookup"><span data-stu-id="1fa2d-126"><span id="TRANSACTION_GENERIC_WRITE"></span><span id="transaction_generic_write"></span>**TRANSACTION\_GENERIC\_WRITE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fa2d-127">0x12003E</span><span class="sxs-lookup"><span data-stu-id="1fa2d-127">0x12003E</span></span>
</dt> <dt>



<span data-ttu-id="1fa2d-128">呼叫端具有下列許可權： **標準的 \_ 許可權 \_ 寫入**、 **交易 \_ 集 \_ 資訊**、 **交易 \_ 認可**、 **交易 \_ 登記**、 **交易 \_ 回復**、 **交易 \_ 傳播** 和 **同步處理**。</span><span class="sxs-lookup"><span data-stu-id="1fa2d-128">The caller has the following privileges: **STANDARD\_RIGHTS\_WRITE**, **TRANSACTION\_SET\_INFORMATION**, **TRANSACTION\_COMMIT**, **TRANSACTION\_ENLIST**, **TRANSACTION\_ROLLBACK**, **TRANSACTION\_PROPAGATE**, and **SYNCHRONIZE**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1fa2d-129"><span id="TRANSACTION_GENERIC_EXECUTE"></span><span id="transaction_generic_execute"></span>**交易 \_ 一般 \_ 執行**</span><span class="sxs-lookup"><span data-stu-id="1fa2d-129"><span id="TRANSACTION_GENERIC_EXECUTE"></span><span id="transaction_generic_execute"></span>**TRANSACTION\_GENERIC\_EXECUTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fa2d-130">0x120018</span><span class="sxs-lookup"><span data-stu-id="1fa2d-130">0x120018</span></span>
</dt> <dt>



<span data-ttu-id="1fa2d-131">呼叫端具有下列許可權： **標準 \_ 許可權 \_ 執行**、 **交易 \_ 認可**、 **交易 \_ 回復**，以及 **同步處理**。</span><span class="sxs-lookup"><span data-stu-id="1fa2d-131">The caller has the following privileges: **STANDARD\_RIGHTS\_EXECUTE**, **TRANSACTION\_COMMIT**, **TRANSACTION\_ROLLBACK**, and **SYNCHRONIZE**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1fa2d-132"><span id="TRANSACTION_ALL_ACCESS"></span><span id="transaction_all_access"></span>**交易 \_ 所有 \_ 存取**</span><span class="sxs-lookup"><span data-stu-id="1fa2d-132"><span id="TRANSACTION_ALL_ACCESS"></span><span id="transaction_all_access"></span>**TRANSACTION\_ALL\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fa2d-133">0x12003F</span><span class="sxs-lookup"><span data-stu-id="1fa2d-133">0x12003F</span></span>
</dt> <dt>



<span data-ttu-id="1fa2d-134">呼叫端具有下列許可權： **需要標準 \_ 許可權 \_**、 **交易 \_ 一般 \_ 讀取**、 **交易 \_ 一般 \_ 寫入** 和 **交易 \_ 一般 \_ 執行**。</span><span class="sxs-lookup"><span data-stu-id="1fa2d-134">The caller has the following privilege: **STANDARD\_RIGHTS\_REQUIRED**, **TRANSACTION\_GENERIC\_READ**, **TRANSACTION\_GENERIC\_WRITE**, and **TRANSACTION\_GENERIC\_EXECUTE**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1fa2d-135"><span id="TRANSACTION_RESOURCE_MANAGER_RIGHTS"></span><span id="transaction_resource_manager_rights"></span>**交易 \_ 資源 \_ 管理員 \_ 許可權**</span><span class="sxs-lookup"><span data-stu-id="1fa2d-135"><span id="TRANSACTION_RESOURCE_MANAGER_RIGHTS"></span><span id="transaction_resource_manager_rights"></span>**TRANSACTION\_RESOURCE\_MANAGER\_RIGHTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fa2d-136">0x120037</span><span class="sxs-lookup"><span data-stu-id="1fa2d-136">0x120037</span></span>
</dt> <dt>



<span data-ttu-id="1fa2d-137">呼叫端具有下列許可權： **交易 \_ 一般 \_ 讀取**、 **標準 \_ 許可權 \_ 寫入**、 **交易 \_ 集 \_ 資訊**、 **交易 \_ 回復**、 **交易 \_ 登記**、 **交易 \_ 傳播**，以及 **同步** 處理。</span><span class="sxs-lookup"><span data-stu-id="1fa2d-137">The caller has the following privileges: **TRANSACTION\_GENERIC\_READ**, **STANDARD\_RIGHTS\_WRITE**, **TRANSACTION\_SET\_INFORMATION**, **TRANSACTION\_ROLLBACK**, **TRANSACTION\_ENLIST**, **TRANSACTION\_PROPAGATE**, and **SYNCHRONIZE**.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1fa2d-138">備註</span><span class="sxs-lookup"><span data-stu-id="1fa2d-138">Remarks</span></span>

<span data-ttu-id="1fa2d-139">當您在交易中登記時，建議使用資源管理員，在開啟交易時指定 **交易 \_ 資源 \_ 管理員 \_ 許可權** 。</span><span class="sxs-lookup"><span data-stu-id="1fa2d-139">It is recommended that resource managers, when enlisting in a transaction, specify **TRANSACTION\_RESOURCE\_MANAGER\_RIGHTS** when opening a transaction.</span></span>

## <a name="requirements"></a><span data-ttu-id="1fa2d-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="1fa2d-140">Requirements</span></span>



| <span data-ttu-id="1fa2d-141">需求</span><span class="sxs-lookup"><span data-stu-id="1fa2d-141">Requirement</span></span> | <span data-ttu-id="1fa2d-142">值</span><span class="sxs-lookup"><span data-stu-id="1fa2d-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1fa2d-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1fa2d-143">Minimum supported client</span></span><br/> | <span data-ttu-id="1fa2d-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1fa2d-144">Windows Vista</span></span><br/>                                                           |
| <span data-ttu-id="1fa2d-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1fa2d-145">Minimum supported server</span></span><br/> | <span data-ttu-id="1fa2d-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1fa2d-146">Windows Server 2008</span></span><br/>                                                     |
| <span data-ttu-id="1fa2d-147">標頭</span><span class="sxs-lookup"><span data-stu-id="1fa2d-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="1fa2d-148"><dt>WinNT。h</dt></span><span class="sxs-lookup"><span data-stu-id="1fa2d-148"><dt>WinNT.h</dt></span></span> </dl> |



 

 





---
description: KTM 會定義在開啟交易管理員 (TM) 時要使用的下列登記存取遮罩。
ms.assetid: 8f9b9d3d-e7ea-4df2-82b1-2d4c3e0766c0
title: '交易管理員存取遮罩 (WinNT. h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efae6c0bac1fc2bfa117e74e38aff8d439eb2f25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849015"
---
# <a name="transaction-manager-access-masks"></a><span data-ttu-id="ee17f-103">交易管理員存取遮罩</span><span class="sxs-lookup"><span data-stu-id="ee17f-103">Transaction Manager Access Masks</span></span>

<span data-ttu-id="ee17f-104">KTM 會定義在開啟交易管理員 (TM) 時要使用的下列登記存取遮罩。</span><span class="sxs-lookup"><span data-stu-id="ee17f-104">KTM defines the following enlistment access masks to be used when opening a transaction manager (TM).</span></span>

<dl> <dt>

<span data-ttu-id="ee17f-105"><span id="TRANSACTIONMANAGER_QUERY_INFORMATION"></span><span id="transactionmanager_query_information"></span>**TRANSACTIONMANAGER \_ 查詢 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="ee17f-105"><span id="TRANSACTIONMANAGER_QUERY_INFORMATION"></span><span id="transactionmanager_query_information"></span>**TRANSACTIONMANAGER\_QUERY\_INFORMATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee17f-106">0x00001</span><span class="sxs-lookup"><span data-stu-id="ee17f-106">0x00001</span></span>
</dt> <dt>



<span data-ttu-id="ee17f-107">呼叫者可以查詢此 TM 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ee17f-107">The caller can query information about this TM.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee17f-108"><span id="TRANSACTIONMANAGER_SET_INFORMATION"></span><span id="transactionmanager_set_information"></span>**TRANSACTIONMANAGER \_ 設定 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="ee17f-108"><span id="TRANSACTIONMANAGER_SET_INFORMATION"></span><span id="transactionmanager_set_information"></span>**TRANSACTIONMANAGER\_SET\_INFORMATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee17f-109">0x00002</span><span class="sxs-lookup"><span data-stu-id="ee17f-109">0x00002</span></span>
</dt> <dt>



<span data-ttu-id="ee17f-110">呼叫者可以設定此 TM 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ee17f-110">The caller can set information about this TM.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee17f-111"><span id="TRANSACTIONMANAGER_RECOVER"></span><span id="transactionmanager_recover"></span>**TRANSACTIONMANAGER \_ 復原**</span><span class="sxs-lookup"><span data-stu-id="ee17f-111"><span id="TRANSACTIONMANAGER_RECOVER"></span><span id="transactionmanager_recover"></span>**TRANSACTIONMANAGER\_RECOVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee17f-112">0x00004</span><span class="sxs-lookup"><span data-stu-id="ee17f-112">0x00004</span></span>
</dt> <dt>



<span data-ttu-id="ee17f-113">呼叫者可以復原此 TM。</span><span class="sxs-lookup"><span data-stu-id="ee17f-113">The caller can recover this TM.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee17f-114"><span id="TRANSACTIONMANAGER_RENAME"></span><span id="transactionmanager_rename"></span>**TRANSACTIONMANAGER \_ 重新命名**</span><span class="sxs-lookup"><span data-stu-id="ee17f-114"><span id="TRANSACTIONMANAGER_RENAME"></span><span id="transactionmanager_rename"></span>**TRANSACTIONMANAGER\_RENAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee17f-115">0x00008</span><span class="sxs-lookup"><span data-stu-id="ee17f-115">0x00008</span></span>
</dt> <dt>



<span data-ttu-id="ee17f-116">呼叫端可以重新命名 TM 實例。</span><span class="sxs-lookup"><span data-stu-id="ee17f-116">The caller can rename a TM instance.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee17f-117"><span id="TRANSACTIONMANAGER_CREATE_RM"></span><span id="transactionmanager_create_rm"></span>**TRANSACTIONMANAGER \_ 建立 \_ RM**</span><span class="sxs-lookup"><span data-stu-id="ee17f-117"><span id="TRANSACTIONMANAGER_CREATE_RM"></span><span id="transactionmanager_create_rm"></span>**TRANSACTIONMANAGER\_CREATE\_RM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee17f-118">0x00010</span><span class="sxs-lookup"><span data-stu-id="ee17f-118">0x00010</span></span>
</dt> <dt>



<span data-ttu-id="ee17f-119">呼叫者可以建立與此 TM 相關聯的資源管理員。</span><span class="sxs-lookup"><span data-stu-id="ee17f-119">The caller can create a resource manager that is associated with this TM.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee17f-120"><span id="TRANSACTIONMANAGER_BIND_TRANSACTION"></span><span id="transactionmanager_bind_transaction"></span>**TRANSACTIONMANAGER 系結 \_ \_ 交易**</span><span class="sxs-lookup"><span data-stu-id="ee17f-120"><span id="TRANSACTIONMANAGER_BIND_TRANSACTION"></span><span id="transactionmanager_bind_transaction"></span>**TRANSACTIONMANAGER\_BIND\_TRANSACTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee17f-121">0x00020</span><span class="sxs-lookup"><span data-stu-id="ee17f-121">0x00020</span></span>
</dt> <dt>



<span data-ttu-id="ee17f-122">此值為 reserved。</span><span class="sxs-lookup"><span data-stu-id="ee17f-122">This value is reserved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee17f-123"><span id="TRANSACTIONMANAGER_GENERIC_READ"></span><span id="transactionmanager_generic_read"></span>**將 \_ 一般 \_ 讀取**</span><span class="sxs-lookup"><span data-stu-id="ee17f-123"><span id="TRANSACTIONMANAGER_GENERIC_READ"></span><span id="transactionmanager_generic_read"></span>**TRANSACTIONMANAGER\_GENERIC\_READ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee17f-124">0x20001</span><span class="sxs-lookup"><span data-stu-id="ee17f-124">0x20001</span></span>
</dt> <dt>



<span data-ttu-id="ee17f-125">呼叫端具有下列許可權： **標準 \_ 許可權 \_ 讀取** 和 **TRANSACTIONMANAGER \_ 查詢 \_ 資訊**。</span><span class="sxs-lookup"><span data-stu-id="ee17f-125">The caller has the following privileges: **STANDARD\_RIGHTS\_READ** and **TRANSACTIONMANAGER\_QUERY\_INFORMATION**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee17f-126"><span id="TRANSACTIONMANAGER_GENERIC_WRITE"></span><span id="transactionmanager_generic_write"></span>**TRANSACTIONMANAGER \_ 泛型 \_ 寫入**</span><span class="sxs-lookup"><span data-stu-id="ee17f-126"><span id="TRANSACTIONMANAGER_GENERIC_WRITE"></span><span id="transactionmanager_generic_write"></span>**TRANSACTIONMANAGER\_GENERIC\_WRITE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee17f-127">0x2001E</span><span class="sxs-lookup"><span data-stu-id="ee17f-127">0x2001E</span></span>
</dt> <dt>



<span data-ttu-id="ee17f-128">呼叫端具有下列許可權： **標準 \_ 許可權 \_ 寫入**、 **transactionmanager \_ 設定 \_ 資訊**、 **transactionmanager \_ 復原**、 **TRANSACTIONMANAGER \_ 重新命名** 和 **transactionmanager \_ 建立 \_ RM**。</span><span class="sxs-lookup"><span data-stu-id="ee17f-128">The caller has the following privileges: **STANDARD\_RIGHTS\_WRITE**, **TRANSACTIONMANAGER\_SET\_INFORMATION**, **TRANSACTIONMANAGER\_RECOVER**, **TRANSACTIONMANAGER\_RENAME**, and **TRANSACTIONMANAGER\_CREATE\_RM**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee17f-129"><span id="TRANSACTIONMANAGER_GENERIC_EXECUTE"></span><span id="transactionmanager_generic_execute"></span>**TRANSACTIONMANAGER \_ 泛型 \_ EXECUTE**</span><span class="sxs-lookup"><span data-stu-id="ee17f-129"><span id="TRANSACTIONMANAGER_GENERIC_EXECUTE"></span><span id="transactionmanager_generic_execute"></span>**TRANSACTIONMANAGER\_GENERIC\_EXECUTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee17f-130">0x20000</span><span class="sxs-lookup"><span data-stu-id="ee17f-130">0x20000</span></span>
</dt> <dt>



<span data-ttu-id="ee17f-131">呼叫端具有下列許可權： **標準 \_ 許可權 \_ 執行**。</span><span class="sxs-lookup"><span data-stu-id="ee17f-131">The caller has the following privilege: **STANDARD\_RIGHTS\_EXECUTE**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee17f-132"><span id="TRANSACTIONMANAGER_ALL_ACCESS"></span><span id="transactionmanager_all_access"></span>**TRANSACTIONMANAGER \_ 所有 \_ 存取**</span><span class="sxs-lookup"><span data-stu-id="ee17f-132"><span id="TRANSACTIONMANAGER_ALL_ACCESS"></span><span id="transactionmanager_all_access"></span>**TRANSACTIONMANAGER\_ALL\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee17f-133">0xF003F</span><span class="sxs-lookup"><span data-stu-id="ee17f-133">0xF003F</span></span>
</dt> <dt>



<span data-ttu-id="ee17f-134">此值會設定 TM 存取值的所有有效位。</span><span class="sxs-lookup"><span data-stu-id="ee17f-134">This value sets all valid bits for a TM access value.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ee17f-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="ee17f-135">Requirements</span></span>



| <span data-ttu-id="ee17f-136">需求</span><span class="sxs-lookup"><span data-stu-id="ee17f-136">Requirement</span></span> | <span data-ttu-id="ee17f-137">值</span><span class="sxs-lookup"><span data-stu-id="ee17f-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ee17f-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ee17f-138">Minimum supported client</span></span><br/> | <span data-ttu-id="ee17f-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ee17f-139">Windows Vista</span></span><br/>                                                           |
| <span data-ttu-id="ee17f-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ee17f-140">Minimum supported server</span></span><br/> | <span data-ttu-id="ee17f-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ee17f-141">Windows Server 2008</span></span><br/>                                                     |
| <span data-ttu-id="ee17f-142">標頭</span><span class="sxs-lookup"><span data-stu-id="ee17f-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee17f-143"><dt>WinNT。h</dt></span><span class="sxs-lookup"><span data-stu-id="ee17f-143"><dt>WinNT.h</dt></span></span> </dl> |



 

 





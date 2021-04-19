---
description: KTM 會定義下列登記存取遮罩，以在開啟登記時使用。
ms.assetid: 93773eb7-141a-49f3-9306-ffbda2f4ab9f
title: '登錄存取遮罩 (WinNT. h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63e4ebd67f93368215ebcdcd362595d0341adb52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997205"
---
# <a name="enlistment-access-masks"></a><span data-ttu-id="d0a5f-103">登記存取遮罩</span><span class="sxs-lookup"><span data-stu-id="d0a5f-103">Enlistment Access Masks</span></span>

<span data-ttu-id="d0a5f-104">KTM 會定義下列登記存取遮罩，以在開啟登記時使用。</span><span class="sxs-lookup"><span data-stu-id="d0a5f-104">KTM defines the following enlistment access masks to be used when opening enlistments.</span></span>

<dl> <dt>

<span data-ttu-id="d0a5f-105"><span id="ENLISTMENT_QUERY_INFORMATION"></span><span id="enlistment_query_information"></span>**登記 \_ 查詢 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="d0a5f-105"><span id="ENLISTMENT_QUERY_INFORMATION"></span><span id="enlistment_query_information"></span>**ENLISTMENT\_QUERY\_INFORMATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0a5f-106">0x00001</span><span class="sxs-lookup"><span data-stu-id="d0a5f-106">0x00001</span></span>
</dt> <dt>



<span data-ttu-id="d0a5f-107">呼叫者可以查詢 KTM 以取得登記的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d0a5f-107">The caller can query KTM for information about the enlistment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d0a5f-108"><span id="ENLISTMENT_SET_INFORMATION"></span><span id="enlistment_set_information"></span>**登記 \_ 設定 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="d0a5f-108"><span id="ENLISTMENT_SET_INFORMATION"></span><span id="enlistment_set_information"></span>**ENLISTMENT\_SET\_INFORMATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0a5f-109">0x00002</span><span class="sxs-lookup"><span data-stu-id="d0a5f-109">0x00002</span></span>
</dt> <dt>



<span data-ttu-id="d0a5f-110">呼叫端可以設定登記的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d0a5f-110">The caller can set information about the enlistment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d0a5f-111"><span id="ENLISTMENT_RECOVER"></span><span id="enlistment_recover"></span>**登記 \_ 復原**</span><span class="sxs-lookup"><span data-stu-id="d0a5f-111"><span id="ENLISTMENT_RECOVER"></span><span id="enlistment_recover"></span>**ENLISTMENT\_RECOVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0a5f-112">0x00004</span><span class="sxs-lookup"><span data-stu-id="d0a5f-112">0x00004</span></span>
</dt> <dt>



<span data-ttu-id="d0a5f-113">呼叫端可以復原登記。</span><span class="sxs-lookup"><span data-stu-id="d0a5f-113">The caller can recover an enlistment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d0a5f-114"><span id="ENLISTMENT_SUBORDINATE_RIGHTS"></span><span id="enlistment_subordinate_rights"></span>**登記 \_ 次級 \_ 許可權**</span><span class="sxs-lookup"><span data-stu-id="d0a5f-114"><span id="ENLISTMENT_SUBORDINATE_RIGHTS"></span><span id="enlistment_subordinate_rights"></span>**ENLISTMENT\_SUBORDINATE\_RIGHTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0a5f-115">0x00008</span><span class="sxs-lookup"><span data-stu-id="d0a5f-115">0x00008</span></span>
</dt> <dt>



<span data-ttu-id="d0a5f-116">呼叫端可以完成資源管理員代表交易執行的動作。</span><span class="sxs-lookup"><span data-stu-id="d0a5f-116">The caller can complete actions that a resource manager does on behalf of the transaction.</span></span> <span data-ttu-id="d0a5f-117">以下是動作的清單：</span><span class="sxs-lookup"><span data-stu-id="d0a5f-117">The following is a list of actions:</span></span>

-   [<span data-ttu-id="d0a5f-118">**CommitComplete**</span><span class="sxs-lookup"><span data-stu-id="d0a5f-118">**CommitComplete**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete)
-   [<span data-ttu-id="d0a5f-119">**PrepareComplete**</span><span class="sxs-lookup"><span data-stu-id="d0a5f-119">**PrepareComplete**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete)
-   [<span data-ttu-id="d0a5f-120">**PrePrepareComplete**</span><span class="sxs-lookup"><span data-stu-id="d0a5f-120">**PrePrepareComplete**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-prepreparecomplete)
-   [<span data-ttu-id="d0a5f-121">**RollbackComplete**</span><span class="sxs-lookup"><span data-stu-id="d0a5f-121">**RollbackComplete**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackcomplete)
-   [<span data-ttu-id="d0a5f-122">**ReadOnlyEnlistment**</span><span class="sxs-lookup"><span data-stu-id="d0a5f-122">**ReadOnlyEnlistment**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-readonlyenlistment)
-   [<span data-ttu-id="d0a5f-123">**RollbackEnlistment**</span><span class="sxs-lookup"><span data-stu-id="d0a5f-123">**RollbackEnlistment**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackenlistment)
-   [<span data-ttu-id="d0a5f-124">**SinglePhaseReject**</span><span class="sxs-lookup"><span data-stu-id="d0a5f-124">**SinglePhaseReject**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-singlephasereject)


</dt> </dl> </dd> <dt>

<span data-ttu-id="d0a5f-125"><span id="ENLISTMENT_SUPERIOR_RIGHTS"></span><span id="enlistment_superior_rights"></span>**登記 \_ 優異 \_ 許可權**</span><span class="sxs-lookup"><span data-stu-id="d0a5f-125"><span id="ENLISTMENT_SUPERIOR_RIGHTS"></span><span id="enlistment_superior_rights"></span>**ENLISTMENT\_SUPERIOR\_RIGHTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0a5f-126">0x00010</span><span class="sxs-lookup"><span data-stu-id="d0a5f-126">0x00010</span></span>
</dt> <dt>



<span data-ttu-id="d0a5f-127">呼叫端可以在交易中登記為高階交易管理員。</span><span class="sxs-lookup"><span data-stu-id="d0a5f-127">The caller can enlist in the transaction as a superior transaction manager.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d0a5f-128"><span id="ENLISTMENT_GENERIC_READ"></span><span id="enlistment_generic_read"></span>**登記 \_ 一般 \_ 讀取**</span><span class="sxs-lookup"><span data-stu-id="d0a5f-128"><span id="ENLISTMENT_GENERIC_READ"></span><span id="enlistment_generic_read"></span>**ENLISTMENT\_GENERIC\_READ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0a5f-129">0x20001</span><span class="sxs-lookup"><span data-stu-id="d0a5f-129">0x20001</span></span>
</dt> <dt>



<span data-ttu-id="d0a5f-130">呼叫端具有下列許可權： **標準 \_ 許可權 \_ 讀取** 和 **登記 \_ 查詢 \_ 資訊**。</span><span class="sxs-lookup"><span data-stu-id="d0a5f-130">The caller has the following privileges: **STANDARD\_RIGHTS\_READ** and **ENLISTMENT\_QUERY\_INFORMATION**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d0a5f-131"><span id="ENLISTMENT_GENERIC_WRITE"></span><span id="enlistment_generic_write"></span>**登記 \_ 一般 \_ 寫入**</span><span class="sxs-lookup"><span data-stu-id="d0a5f-131"><span id="ENLISTMENT_GENERIC_WRITE"></span><span id="enlistment_generic_write"></span>**ENLISTMENT\_GENERIC\_WRITE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0a5f-132">0x2001E</span><span class="sxs-lookup"><span data-stu-id="d0a5f-132">0x2001E</span></span>
</dt> <dt>



<span data-ttu-id="d0a5f-133">呼叫端具有下列許可權： **標準 \_ 許可權 \_ 寫入**、登錄 **\_ 集 \_ 資訊** 和 **登記 \_ 復原**。</span><span class="sxs-lookup"><span data-stu-id="d0a5f-133">The caller has the following privileges: **STANDARD\_RIGHTS\_WRITE**, **ENLISTMENT\_SET\_INFORMATION**, and **ENLISTMENT\_RECOVER**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d0a5f-134"><span id="ENLISTMENT_GENERIC_EXECUTE"></span><span id="enlistment_generic_execute"></span>**登記 \_ 泛型 \_ 執行**</span><span class="sxs-lookup"><span data-stu-id="d0a5f-134"><span id="ENLISTMENT_GENERIC_EXECUTE"></span><span id="enlistment_generic_execute"></span>**ENLISTMENT\_GENERIC\_EXECUTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0a5f-135">0x2001C</span><span class="sxs-lookup"><span data-stu-id="d0a5f-135">0x2001C</span></span>
</dt> <dt>



<span data-ttu-id="d0a5f-136">呼叫端具有下列許可權： **標準 \_ 許可權 \_ 執行**、 **登記 \_ 復原** 和 **登記 \_ 次級 \_ 許可權**。</span><span class="sxs-lookup"><span data-stu-id="d0a5f-136">The caller has the following privileges: **STANDARD\_RIGHTS\_EXECUTE**, **ENLISTMENT\_RECOVER**, and **ENLISTMENT\_SUBORDINATE\_RIGHTS**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d0a5f-137"><span id="ENLISTMENT_ALL_ACCESS"></span><span id="enlistment_all_access"></span>**登記 \_ 所有 \_ 存取**</span><span class="sxs-lookup"><span data-stu-id="d0a5f-137"><span id="ENLISTMENT_ALL_ACCESS"></span><span id="enlistment_all_access"></span>**ENLISTMENT\_ALL\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0a5f-138">0xF001F</span><span class="sxs-lookup"><span data-stu-id="d0a5f-138">0xF001F</span></span>
</dt> <dt>



<span data-ttu-id="d0a5f-139">此值會設定登記存取值的所有有效位。</span><span class="sxs-lookup"><span data-stu-id="d0a5f-139">This value sets all valid bits for an enlistment access value.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d0a5f-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="d0a5f-140">Requirements</span></span>



| <span data-ttu-id="d0a5f-141">需求</span><span class="sxs-lookup"><span data-stu-id="d0a5f-141">Requirement</span></span> | <span data-ttu-id="d0a5f-142">值</span><span class="sxs-lookup"><span data-stu-id="d0a5f-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d0a5f-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d0a5f-143">Minimum supported client</span></span><br/> | <span data-ttu-id="d0a5f-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d0a5f-144">Windows Vista</span></span><br/>                                                           |
| <span data-ttu-id="d0a5f-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d0a5f-145">Minimum supported server</span></span><br/> | <span data-ttu-id="d0a5f-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d0a5f-146">Windows Server 2008</span></span><br/>                                                     |
| <span data-ttu-id="d0a5f-147">標頭</span><span class="sxs-lookup"><span data-stu-id="d0a5f-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0a5f-148"><dt>WinNT。h</dt></span><span class="sxs-lookup"><span data-stu-id="d0a5f-148"><dt>WinNT.h</dt></span></span> </dl> |



 

 





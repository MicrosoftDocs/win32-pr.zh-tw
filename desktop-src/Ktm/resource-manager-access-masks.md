---
description: KTM 定義了在開啟資源管理員時要使用的下列登記存取遮罩。
ms.assetid: 6b901b73-516d-4f27-b258-3b93a8f9675f
title: 'Resource Manager 存取遮罩 (WinNT) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f0f579a96ed80de100a5cb41cb9c4e9b847a060
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115401"
---
# <a name="resource-manager-access-masks"></a><span data-ttu-id="0853b-103">Resource Manager 存取遮罩</span><span class="sxs-lookup"><span data-stu-id="0853b-103">Resource Manager Access Masks</span></span>

<span data-ttu-id="0853b-104">KTM 定義了在開啟資源管理員時要使用的下列登記存取遮罩。</span><span class="sxs-lookup"><span data-stu-id="0853b-104">KTM defines the following enlistment access masks to be used when opening a resource manager.</span></span>

<dl> <dt>

<span data-ttu-id="0853b-105"><span id="RESOURCEMANAGER_QUERY_INFORMATION"></span><span id="resourcemanager_query_information"></span>**RESOURCEMANAGER \_ 查詢 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="0853b-105"><span id="RESOURCEMANAGER_QUERY_INFORMATION"></span><span id="resourcemanager_query_information"></span>**RESOURCEMANAGER\_QUERY\_INFORMATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0853b-106">呼叫端可以查詢資源管理員 (RM) 資訊。</span><span class="sxs-lookup"><span data-stu-id="0853b-106">The caller can query for the resource manager (RM) information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0853b-107"><span id="RESOURCEMANAGER_SET_INFORMATION"></span><span id="resourcemanager_set_information"></span>**RESOURCEMANAGER \_ 設定 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="0853b-107"><span id="RESOURCEMANAGER_SET_INFORMATION"></span><span id="resourcemanager_set_information"></span>**RESOURCEMANAGER\_SET\_INFORMATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0853b-108">呼叫端可以設定 RM 資訊。</span><span class="sxs-lookup"><span data-stu-id="0853b-108">The caller can set the RM information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0853b-109"><span id="RESOURCEMANAGER_RECOVER"></span><span id="resourcemanager_recover"></span>**RESOURCEMANAGER \_ 復原**</span><span class="sxs-lookup"><span data-stu-id="0853b-109"><span id="RESOURCEMANAGER_RECOVER"></span><span id="resourcemanager_recover"></span>**RESOURCEMANAGER\_RECOVER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0853b-110">呼叫端可以復原指定的 RM。</span><span class="sxs-lookup"><span data-stu-id="0853b-110">The caller can recover the specified RM.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0853b-111"><span id="RESOURCEMANAGER_ENLIST"></span><span id="resourcemanager_enlist"></span>**RESOURCEMANAGER \_ 登錄**</span><span class="sxs-lookup"><span data-stu-id="0853b-111"><span id="RESOURCEMANAGER_ENLIST"></span><span id="resourcemanager_enlist"></span>**RESOURCEMANAGER\_ENLIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0853b-112">呼叫端可以在交易中登記 RM。</span><span class="sxs-lookup"><span data-stu-id="0853b-112">The caller can enlist an RM in a transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0853b-113"><span id="RESOURCEMANAGER_GET_NOTIFICATION"></span><span id="resourcemanager_get_notification"></span>**RESOURCEMANAGER \_ 取得 \_ 通知**</span><span class="sxs-lookup"><span data-stu-id="0853b-113"><span id="RESOURCEMANAGER_GET_NOTIFICATION"></span><span id="resourcemanager_get_notification"></span>**RESOURCEMANAGER\_GET\_NOTIFICATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0853b-114">呼叫端可能會收到 RM 的通知。</span><span class="sxs-lookup"><span data-stu-id="0853b-114">The caller can receive a notification for an RM.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0853b-115"><span id="RESOURCEMANAGER_GENERIC_READ"></span><span id="resourcemanager_generic_read"></span>**RESOURCEMANAGER \_ 一般 \_ 讀取**</span><span class="sxs-lookup"><span data-stu-id="0853b-115"><span id="RESOURCEMANAGER_GENERIC_READ"></span><span id="resourcemanager_generic_read"></span>**RESOURCEMANAGER\_GENERIC\_READ**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0853b-116">呼叫端具有下列許可權：標準 \_ 許可權 \_ 讀取、RESOURCEMANAGER \_ 查詢 \_ 資訊，以及 RESOURCEMANAGER \_ 復原。</span><span class="sxs-lookup"><span data-stu-id="0853b-116">The caller has the following privileges: STANDARD\_RIGHTS\_READ, RESOURCEMANAGER\_QUERY\_INFORMATION, and RESOURCEMANAGER\_RECOVER.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0853b-117"><span id="RESOURCEMANAGER_GENERIC_WRITE"></span><span id="resourcemanager_generic_write"></span>**RESOURCEMANAGER \_ 一般 \_ 寫入**</span><span class="sxs-lookup"><span data-stu-id="0853b-117"><span id="RESOURCEMANAGER_GENERIC_WRITE"></span><span id="resourcemanager_generic_write"></span>**RESOURCEMANAGER\_GENERIC\_WRITE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0853b-118">呼叫端具有下列許可權：標準 \_ 許可權 \_ 寫入、resourcemanager \_ 設定 \_ 資訊、resourcemanager 登錄 \_ 和 RESOURCEMANAGER \_ 取得 \_ 通知。</span><span class="sxs-lookup"><span data-stu-id="0853b-118">The caller has the following privileges: STANDARD\_RIGHTS\_WRITE, RESOURCEMANAGER\_SET\_INFORMATION, RESOURCEMANAGER\_ENLIST, and RESOURCEMANAGER\_GET\_NOTIFICATION.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0853b-119"><span id="RESOURCEMANAGER_GENERIC_EXECUTE"></span><span id="resourcemanager_generic_execute"></span>**RESOURCEMANAGER \_ 泛型 \_ 執行**</span><span class="sxs-lookup"><span data-stu-id="0853b-119"><span id="RESOURCEMANAGER_GENERIC_EXECUTE"></span><span id="resourcemanager_generic_execute"></span>**RESOURCEMANAGER\_GENERIC\_EXECUTE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0853b-120">呼叫端具有下列許可權：標準 \_ 許可權 \_ 執行、RESOURCEMANAGER 登錄 \_ 和 RESOURCEMANAGER \_ 取得 \_ 通知。</span><span class="sxs-lookup"><span data-stu-id="0853b-120">The caller has the following privileges: STANDARD\_RIGHTS\_EXECUTE, RESOURCEMANAGER\_ENLIST, and RESOURCEMANAGER\_GET\_NOTIFICATION.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0853b-121"><span id="RESOURCEMANAGER_ALL_ACCESS"></span><span id="resourcemanager_all_access"></span>**RESOURCEMANAGER \_ 所有 \_ 存取**</span><span class="sxs-lookup"><span data-stu-id="0853b-121"><span id="RESOURCEMANAGER_ALL_ACCESS"></span><span id="resourcemanager_all_access"></span>**RESOURCEMANAGER\_ALL\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0853b-122">呼叫端具有下列許可權：需要標準 \_ 許可權 \_ 。</span><span class="sxs-lookup"><span data-stu-id="0853b-122">The caller has the following privilege: STANDARD\_RIGHTS\_REQUIRED.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0853b-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="0853b-123">Requirements</span></span>



| <span data-ttu-id="0853b-124">需求</span><span class="sxs-lookup"><span data-stu-id="0853b-124">Requirement</span></span> | <span data-ttu-id="0853b-125">值</span><span class="sxs-lookup"><span data-stu-id="0853b-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0853b-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0853b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="0853b-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0853b-127">Windows Vista</span></span><br/>                                                           |
| <span data-ttu-id="0853b-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0853b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="0853b-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0853b-129">Windows Server 2008</span></span><br/>                                                     |
| <span data-ttu-id="0853b-130">標頭</span><span class="sxs-lookup"><span data-stu-id="0853b-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="0853b-131"><dt>WinNT。h</dt></span><span class="sxs-lookup"><span data-stu-id="0853b-131"><dt>WinNT.h</dt></span></span> </dl> |



 

 





---
title: 網域控制站和複寫管理結構
description: 網域控制站和複寫管理函數會使用下列結構。
ms.assetid: 42b20d3b-1799-4f5f-b74e-fe9284dd8ac3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4afe084e4285f4851457f9a519e747952e3bbd67
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103842088"
---
# <a name="domain-controller-and-replication-management-structures"></a><span data-ttu-id="6e620-103">網域控制站和複寫管理結構</span><span class="sxs-lookup"><span data-stu-id="6e620-103">Domain Controller and Replication Management Structures</span></span>

<span data-ttu-id="6e620-104">網域控制站和複寫管理函數會使用下列結構：</span><span class="sxs-lookup"><span data-stu-id="6e620-104">The domain controller and replication management functions use the following structures:</span></span>

-   [<span data-ttu-id="6e620-105">**DS \_ 域 \_ 控制器 \_ 資訊 \_ 1**</span><span class="sxs-lookup"><span data-stu-id="6e620-105">**DS\_DOMAIN\_CONTROLLER\_INFO\_1**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_domain_controller_info_1a)
-   [<span data-ttu-id="6e620-106">**DS \_ 域 \_ 控制器 \_ 資訊 \_ 2**</span><span class="sxs-lookup"><span data-stu-id="6e620-106">**DS\_DOMAIN\_CONTROLLER\_INFO\_2**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_domain_controller_info_2a)
-   [<span data-ttu-id="6e620-107">**DS \_ 域 \_ 控制器 \_ 資訊 \_ 3**</span><span class="sxs-lookup"><span data-stu-id="6e620-107">**DS\_DOMAIN\_CONTROLLER\_INFO\_3**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_domain_controller_info_3a)
-   [<span data-ttu-id="6e620-108">**DS \_ 名稱 \_ 結果**</span><span class="sxs-lookup"><span data-stu-id="6e620-108">**DS\_NAME\_RESULT**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_name_resulta)
-   [<span data-ttu-id="6e620-109">**DS \_ 名稱 \_ 結果 \_ 專案**</span><span class="sxs-lookup"><span data-stu-id="6e620-109">**DS\_NAME\_RESULT\_ITEM**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_name_result_itema)
-   [<span data-ttu-id="6e620-110">**DS \_ 複製 \_ ATTR \_ 元 \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="6e620-110">**DS\_REPL\_ATTR\_META\_DATA**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_attr_meta_data)
-   [<span data-ttu-id="6e620-111">**DS \_ 複製 \_ ATTR \_ 元 \_ 資料 \_ 2**</span><span class="sxs-lookup"><span data-stu-id="6e620-111">**DS\_REPL\_ATTR\_META\_DATA\_2**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_attr_meta_data_2)
-   [<span data-ttu-id="6e620-112">**DS \_ 複製 \_ ATTR \_ 元 \_ 資料 \_ BLOB**</span><span class="sxs-lookup"><span data-stu-id="6e620-112">**DS\_REPL\_ATTR\_META\_DATA\_BLOB**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_attr_meta_data_blob)
-   [<span data-ttu-id="6e620-113">**DS \_ 複製 \_ ATTR \_ 值 \_ 元 \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="6e620-113">**DS\_REPL\_ATTR\_VALUE\_META\_DATA**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_attr_value_meta_data)
-   [<span data-ttu-id="6e620-114">**DS \_ 複製 \_ ATTR \_ 值 \_ META \_ DATA \_ 2**</span><span class="sxs-lookup"><span data-stu-id="6e620-114">**DS\_REPL\_ATTR\_VALUE\_META\_DATA\_2**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_attr_value_meta_data_2)
-   [<span data-ttu-id="6e620-115">**DS \_ 複製 \_ ATTR \_ 值 \_ META \_ DATA \_ EXT**</span><span class="sxs-lookup"><span data-stu-id="6e620-115">**DS\_REPL\_ATTR\_VALUE\_META\_DATA\_EXT**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_attr_value_meta_data_ext)
-   [<span data-ttu-id="6e620-116">**DS 複寫資料 \_ \_ 指標**</span><span class="sxs-lookup"><span data-stu-id="6e620-116">**DS\_REPL\_CURSOR**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursor)
-   [<span data-ttu-id="6e620-117">**DS 複寫資料 \_ \_ 指標 \_ 2**</span><span class="sxs-lookup"><span data-stu-id="6e620-117">**DS\_REPL\_CURSOR\_2**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursor_2)
-   [<span data-ttu-id="6e620-118">**DS 複寫資料 \_ \_ 指標 \_ 3**</span><span class="sxs-lookup"><span data-stu-id="6e620-118">**DS\_REPL\_CURSOR\_3**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursor_3w)
-   [<span data-ttu-id="6e620-119">**DS 複寫資料 \_ \_ 指標 \_ BLOB**</span><span class="sxs-lookup"><span data-stu-id="6e620-119">**DS\_REPL\_CURSOR\_BLOB**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursor_blob)
-   [<span data-ttu-id="6e620-120">**DS 複寫資料 \_ \_ 指標**</span><span class="sxs-lookup"><span data-stu-id="6e620-120">**DS\_REPL\_CURSORS**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursors)
-   [<span data-ttu-id="6e620-121">**DS 複寫資料 \_ \_ 指標 \_ 2**</span><span class="sxs-lookup"><span data-stu-id="6e620-121">**DS\_REPL\_CURSORS\_2**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursors_2)
-   [<span data-ttu-id="6e620-122">**DS 複寫資料 \_ \_ 指標 \_ 3**</span><span class="sxs-lookup"><span data-stu-id="6e620-122">**DS\_REPL\_CURSORS\_3**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursors_3w)
-   [<span data-ttu-id="6e620-123">**DS \_ 複寫 \_ KCC \_ DSA \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="6e620-123">**DS\_REPL\_KCC\_DSA\_FAILURE**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_kcc_dsa_failurew)
-   [<span data-ttu-id="6e620-124">**DS \_ 複寫 \_ KCC \_ DSA \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="6e620-124">**DS\_REPL\_KCC\_DSA\_FAILURES**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_kcc_dsa_failuresw)
-   [<span data-ttu-id="6e620-125">**DS \_ 複寫 \_ KCC \_ DSA \_ FAILUREW \_ BLOB**</span><span class="sxs-lookup"><span data-stu-id="6e620-125">**DS\_REPL\_KCC\_DSA\_FAILUREW\_BLOB**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_kcc_dsa_failurew_blob)
-   [<span data-ttu-id="6e620-126">**DS \_ 複寫 \_ 鄰近**</span><span class="sxs-lookup"><span data-stu-id="6e620-126">**DS\_REPL\_NEIGHBOR**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_neighborw)
-   [<span data-ttu-id="6e620-127">**DS \_ 複寫 \_ 鄰近專案**</span><span class="sxs-lookup"><span data-stu-id="6e620-127">**DS\_REPL\_NEIGHBORS**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_neighborsw)
-   [<span data-ttu-id="6e620-128">**DS \_ 複寫 \_ NEIGHBORW \_ BLOB**</span><span class="sxs-lookup"><span data-stu-id="6e620-128">**DS\_REPL\_NEIGHBORW\_BLOB**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_neighborw_blob)
-   [<span data-ttu-id="6e620-129">**DS \_ 複寫 \_ OBJ \_ 元 \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="6e620-129">**DS\_REPL\_OBJ\_META\_DATA**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_obj_meta_data)
-   [<span data-ttu-id="6e620-130">**DS \_ 複寫 \_ OBJ \_ 元 \_ 資料 \_ 2**</span><span class="sxs-lookup"><span data-stu-id="6e620-130">**DS\_REPL\_OBJ\_META\_DATA\_2**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_obj_meta_data_2)
-   [<span data-ttu-id="6e620-131">**DS \_ 複製 \_ 作業**</span><span class="sxs-lookup"><span data-stu-id="6e620-131">**DS\_REPL\_OP**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_opw)
-   [<span data-ttu-id="6e620-132">**DS \_ 複寫 \_ OPW \_ BLOB**</span><span class="sxs-lookup"><span data-stu-id="6e620-132">**DS\_REPL\_OPW\_BLOB**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_opw_blob)
-   [<span data-ttu-id="6e620-133">**DS 複寫擱置中的 \_ \_ \_ OPS**</span><span class="sxs-lookup"><span data-stu-id="6e620-133">**DS\_REPL\_PENDING\_OPS**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_pending_opsw)
-   [<span data-ttu-id="6e620-134">**DS \_ 複寫 \_ 佇列 \_ STATISTICSW**</span><span class="sxs-lookup"><span data-stu-id="6e620-134">**DS\_REPL\_QUEUE\_STATISTICSW**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_queue_statisticsw)
-   <span data-ttu-id="6e620-135">[**DS \_ 複寫 \_ 佇列 \_ STATISTICSW \_ BLOB**](/previous-versions/windows/desktop/legacy/ms676274(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6e620-135">[**DS\_REPL\_QUEUE\_STATISTICSW\_BLOB**](/previous-versions/windows/desktop/legacy/ms676274(v=vs.85))</span></span>
-   [<span data-ttu-id="6e620-136">**DS \_ 複寫 \_ 值 \_ 元 \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="6e620-136">**DS\_REPL\_VALUE\_META\_DATA**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_value_meta_data)
-   [<span data-ttu-id="6e620-137">**DS \_ 複寫 \_ 值 \_ 元 \_ 資料 \_ 2**</span><span class="sxs-lookup"><span data-stu-id="6e620-137">**DS\_REPL\_VALUE\_META\_DATA\_2**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_value_meta_data_2)
-   [<span data-ttu-id="6e620-138">**DS \_ 複寫 \_ 值 \_ 元 \_ 資料 \_ EXT**</span><span class="sxs-lookup"><span data-stu-id="6e620-138">**DS\_REPL\_VALUE\_META\_DATA\_EXT**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_value_meta_data_ext)
-   [<span data-ttu-id="6e620-139">**DS \_ 複寫 \_ 值 \_ 元 \_ 資料 \_ BLOB**</span><span class="sxs-lookup"><span data-stu-id="6e620-139">**DS\_REPL\_VALUE\_META\_DATA\_BLOB**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_value_meta_data_blob)
-   [<span data-ttu-id="6e620-140">**DS \_ 複寫 \_ 值 \_ 元 \_ 資料 \_ BLOB \_ EXT**</span><span class="sxs-lookup"><span data-stu-id="6e620-140">**DS\_REPL\_VALUE\_META\_DATA\_BLOB\_EXT**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_value_meta_data_blob_ext)
-   [<span data-ttu-id="6e620-141">**DS \_ REPSYNCALL \_ ERRINFO**</span><span class="sxs-lookup"><span data-stu-id="6e620-141">**DS\_REPSYNCALL\_ERRINFO**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repsyncall_errinfoa)
-   [<span data-ttu-id="6e620-142">**DS \_ REPSYNCALL \_ 同步處理**</span><span class="sxs-lookup"><span data-stu-id="6e620-142">**DS\_REPSYNCALL\_SYNC**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repsyncall_synca)
-   [<span data-ttu-id="6e620-143">**DS \_ REPSYNCALL \_ 更新**</span><span class="sxs-lookup"><span data-stu-id="6e620-143">**DS\_REPSYNCALL\_UPDATE**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repsyncall_updatea)
-   [<span data-ttu-id="6e620-144">**DS \_ 架構 \_ GUID \_ 對應**</span><span class="sxs-lookup"><span data-stu-id="6e620-144">**DS\_SCHEMA\_GUID\_MAP**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_schema_guid_mapa)
-   [<span data-ttu-id="6e620-145">**DS \_ 網站 \_ 成本 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="6e620-145">**DS\_SITE\_COST\_INFO**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_site_cost_info)
-   [<span data-ttu-id="6e620-146">**附表**</span><span class="sxs-lookup"><span data-stu-id="6e620-146">**SCHEDULE**</span></span>](/windows/desktop/api/Schedule/ns-schedule-schedule)
-   [<span data-ttu-id="6e620-147">**排程 \_ 標頭**</span><span class="sxs-lookup"><span data-stu-id="6e620-147">**SCHEDULE\_HEADER**</span></span>](/windows/desktop/api/Schedule/ns-schedule-schedule_header)

## <a name="related-topics"></a><span data-ttu-id="6e620-148">相關主題</span><span class="sxs-lookup"><span data-stu-id="6e620-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e620-149">Active Directory Domain Services 中的結構</span><span class="sxs-lookup"><span data-stu-id="6e620-149">Structures in Active Directory Domain Services</span></span>](structures-in-active-directory-domain-services.md)
</dt> </dl>

 

 
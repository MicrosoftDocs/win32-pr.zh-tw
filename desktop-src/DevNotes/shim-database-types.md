---
description: 代表主要和自訂填充碼資料庫的類型。
ms.assetid: e893963a-6130-4f65-b925-6f3d292fc86d
title: 填充碼資料庫類型
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 789265ea945ce068d2b0b74e3358582d5e4ccd78
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103688515"
---
# <a name="shim-database-types"></a><span data-ttu-id="9855f-103">填充碼資料庫類型</span><span class="sxs-lookup"><span data-stu-id="9855f-103">Shim Database Types</span></span>

<span data-ttu-id="9855f-104">代表主要和自訂填充碼資料庫的類型。</span><span class="sxs-lookup"><span data-stu-id="9855f-104">Represent the types for main and custom shim databases.</span></span>



| <span data-ttu-id="9855f-105">常數/值</span><span class="sxs-lookup"><span data-stu-id="9855f-105">Constant/value</span></span>                                                                                                                                                                                                                                                | <span data-ttu-id="9855f-106">Description</span><span class="sxs-lookup"><span data-stu-id="9855f-106">Description</span></span>                                                                                   |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| <span id="SDB_DATABASE_MAIN"></span><span id="sdb_database_main"></span><dl> <span data-ttu-id="9855f-107"><dt>**SDB \_資料庫 \_ 主要**</dt> <dt>0x80000000</dt></span><span class="sxs-lookup"><span data-stu-id="9855f-107"><dt>**SDB\_DATABASE\_MAIN**</dt> <dt>0x80000000</dt></span></span> </dl>                    | <span data-ttu-id="9855f-108">主資料庫。</span><span class="sxs-lookup"><span data-stu-id="9855f-108">The main database.</span></span> <span data-ttu-id="9855f-109">如果這個旗標不存在，則表示資料庫是自訂資料庫。</span><span class="sxs-lookup"><span data-stu-id="9855f-109">If this flag is not present, the database is a custom database.</span></span><br/> |
| <span id="SDB_DATABASE_SHIM"></span><span id="sdb_database_shim"></span><dl> <span data-ttu-id="9855f-110"><dt>**SDB \_資料庫 \_ 填充碼**</dt> <dt>0x00010000</dt></span><span class="sxs-lookup"><span data-stu-id="9855f-110"><dt>**SDB\_DATABASE\_SHIM**</dt> <dt>0x00010000</dt></span></span> </dl>                    | <span data-ttu-id="9855f-111">資料庫包含要填充的應用程式專案。</span><span class="sxs-lookup"><span data-stu-id="9855f-111">The database contains application entries to be shimmed.</span></span><br/>                           |
| <span id="SDB_DATABASE_MSI"></span><span id="sdb_database_msi"></span><dl> <span data-ttu-id="9855f-112"><dt>**SDB \_資料庫 \_ MSI**</dt> <dt>0x00020000</dt></span><span class="sxs-lookup"><span data-stu-id="9855f-112"><dt>**SDB\_DATABASE\_MSI**</dt> <dt>0x00020000</dt></span></span> </dl>                       | <span data-ttu-id="9855f-113">資料庫包含 MSI 專案。</span><span class="sxs-lookup"><span data-stu-id="9855f-113">The database contains MSI entries.</span></span><br/>                                                 |
| <span id="SDB_DATABASE_DRIVERS"></span><span id="sdb_database_drivers"></span><dl> <span data-ttu-id="9855f-114"><dt>**SDB \_資料庫 \_ 驅動程式**</dt> <dt>0x00040000</dt></span><span class="sxs-lookup"><span data-stu-id="9855f-114"><dt>**SDB\_DATABASE\_DRIVERS**</dt> <dt>0x00040000</dt></span></span> </dl>           | <span data-ttu-id="9855f-115">資料庫包含驅動程式區塊專案。</span><span class="sxs-lookup"><span data-stu-id="9855f-115">The database contains driver block entries.</span></span><br/>                                        |
| <span id="SDB_DATABASE_DETAILS"></span><span id="sdb_database_details"></span><dl> <span data-ttu-id="9855f-116"><dt>**SDB \_資料庫 \_ 詳細資料**</dt> <dt>0x00080000</dt></span><span class="sxs-lookup"><span data-stu-id="9855f-116"><dt>**SDB\_DATABASE\_DETAILS**</dt> <dt>0x00080000</dt></span></span> </dl>           | <span data-ttu-id="9855f-117">資料庫包含 Apphelp 詳細資料。</span><span class="sxs-lookup"><span data-stu-id="9855f-117">The database contains Apphelp details.</span></span><br/>                                             |
| <span id="SDB_DATABASE_SP_DETAILS"></span><span id="sdb_database_sp_details"></span><dl> <span data-ttu-id="9855f-118"><dt>**SDB \_資料庫 \_ SP \_ 詳細資料**</dt> <dt>0x00100000</dt></span><span class="sxs-lookup"><span data-stu-id="9855f-118"><dt>**SDB\_DATABASE\_SP\_DETAILS**</dt> <dt>0x00100000</dt></span></span> </dl> | <span data-ttu-id="9855f-119">資料庫包含 SP Apphelp 詳細資料。</span><span class="sxs-lookup"><span data-stu-id="9855f-119">The database contains SP Apphelp details.</span></span><br/>                                          |
| <span id="SDB_DATABASE_RESOURCE"></span><span id="sdb_database_resource"></span><dl> <span data-ttu-id="9855f-120"><dt>**SDB \_資料庫 \_ 資源**</dt> <dt>0x00200000</dt></span><span class="sxs-lookup"><span data-stu-id="9855f-120"><dt>**SDB\_DATABASE\_RESOURCE**</dt> <dt>0x00200000</dt></span></span> </dl>        | <span data-ttu-id="9855f-121">資源 DLL 包含 Apphelp 詳細資料。</span><span class="sxs-lookup"><span data-stu-id="9855f-121">The resource DLL contains Apphelp details.</span></span><br/>                                         |
| <span id="SDB_DATABASE_TYPE_MASK"></span><span id="sdb_database_type_mask"></span><dl> <span data-ttu-id="9855f-122"><dt>**SDB \_資料庫 \_ 類型 \_ 遮罩**</dt> <dt>0xF02F0000</dt></span><span class="sxs-lookup"><span data-stu-id="9855f-122"><dt>**SDB\_DATABASE\_TYPE\_MASK**</dt> <dt>0xF02F0000</dt></span></span> </dl>    | <span data-ttu-id="9855f-123">用來解壓縮主要資料庫資訊的遮罩。</span><span class="sxs-lookup"><span data-stu-id="9855f-123">A mask used to extract main database information.</span></span><br/>                                  |
| <span id="SDB_DATABASE_MAIN_SHIM"></span><span id="sdb_database_main_shim"></span><dl> <span data-ttu-id="9855f-124"><dt>**SDB \_ 資料庫 \_ 主要 \_ 填充碼**</dt></span><span class="sxs-lookup"><span data-stu-id="9855f-124"><dt>**SDB\_DATABASE\_MAIN\_SHIM**</dt></span></span> </dl>                                                                    | <span data-ttu-id="9855f-125">SDB \_ 資料庫 \_ 填充碼 \| SDB \_ 資料庫 \_ MSI \| SDB \_ 資料庫 \_ 主資料庫</span><span class="sxs-lookup"><span data-stu-id="9855f-125">SDB\_DATABASE\_SHIM \| SDB\_DATABASE\_MSI \| SDB\_DATABASE\_MAIN</span></span><br/>                   |
| <span id="SDB_DATABASE_MAIN_MSI"></span><span id="sdb_database_main_msi"></span><dl> <span data-ttu-id="9855f-126"><dt>**SDB \_ 資料庫 \_ 主要 \_ MSI**</dt></span><span class="sxs-lookup"><span data-stu-id="9855f-126"><dt>**SDB\_DATABASE\_MAIN\_MSI**</dt></span></span> </dl>                                                                       | <span data-ttu-id="9855f-127">SDB \_ 資料庫 \_ MSI \| SDB \_ 資料庫 \_ 主資料庫</span><span class="sxs-lookup"><span data-stu-id="9855f-127">SDB\_DATABASE\_MSI \| SDB\_DATABASE\_MAIN</span></span><br/>                                          |
| <span id="SDB_DATABASE_MAIN_DRIVERS"></span><span id="sdb_database_main_drivers"></span><dl> <span data-ttu-id="9855f-128"><dt>**SDB \_ 資料庫 \_ 主要 \_ 驅動程式**</dt></span><span class="sxs-lookup"><span data-stu-id="9855f-128"><dt>**SDB\_DATABASE\_MAIN\_DRIVERS**</dt></span></span> </dl>                                                           | <span data-ttu-id="9855f-129">SDB \_ 資料庫 \_ 驅動程式 \| SDB \_ 資料庫 \_ 主要</span><span class="sxs-lookup"><span data-stu-id="9855f-129">SDB\_DATABASE\_DRIVERS \| SDB\_DATABASE\_MAIN</span></span><br/>                                      |
| <span id="SDB_DATABASE_MAIN_DETAILS"></span><span id="sdb_database_main_details"></span><dl> <span data-ttu-id="9855f-130"><dt>**SDB \_ 資料庫 \_ 主要 \_ 詳細資料**</dt></span><span class="sxs-lookup"><span data-stu-id="9855f-130"><dt>**SDB\_DATABASE\_MAIN\_DETAILS**</dt></span></span> </dl>                                                           | <span data-ttu-id="9855f-131">SDB \_ 資料庫 \_ 詳細說明 \| SDB \_ 資料庫 \_ 主資料庫</span><span class="sxs-lookup"><span data-stu-id="9855f-131">SDB\_DATABASE\_DETAILS \| SDB\_DATABASE\_MAIN</span></span><br/>                                      |
| <span id="SDB_DATABASE_MAIN_SP_DETAILS"></span><span id="sdb_database_main_sp_details"></span><dl> <span data-ttu-id="9855f-132"><dt>**SDB \_ 資料庫 \_ 主要的 \_ SP \_ 詳細資料**</dt></span><span class="sxs-lookup"><span data-stu-id="9855f-132"><dt>**SDB\_DATABASE\_MAIN\_SP\_DETAILS**</dt></span></span> </dl>                                                 | <span data-ttu-id="9855f-133">SDB \_ 資料庫 \_ SP \_ 詳細資料 \| SDB \_ 資料庫 \_ 主資料庫</span><span class="sxs-lookup"><span data-stu-id="9855f-133">SDB\_DATABASE\_SP\_DETAILS \| SDB\_DATABASE\_MAIN</span></span><br/>                                  |
| <span id="SDB_DATABASE_MAIN_RESOURCE"></span><span id="sdb_database_main_resource"></span><dl> <span data-ttu-id="9855f-134"><dt>**SDB \_ 資料庫 \_ 主要 \_ 資源**</dt></span><span class="sxs-lookup"><span data-stu-id="9855f-134"><dt>**SDB\_DATABASE\_MAIN\_RESOURCE**</dt></span></span> </dl>                                                        | <span data-ttu-id="9855f-135">SDB \_ 資料庫 \_ 資源 \| SDB \_ 資料庫 \_ 主資料庫</span><span class="sxs-lookup"><span data-stu-id="9855f-135">SDB\_DATABASE\_RESOURCE \| SDB\_DATABASE\_MAIN</span></span><br/>                                     |



## <a name="requirements"></a><span data-ttu-id="9855f-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="9855f-136">Requirements</span></span>



| <span data-ttu-id="9855f-137">需求</span><span class="sxs-lookup"><span data-stu-id="9855f-137">Requirement</span></span> | <span data-ttu-id="9855f-138">值</span><span class="sxs-lookup"><span data-stu-id="9855f-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9855f-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9855f-139">Minimum supported client</span></span><br/> | <span data-ttu-id="9855f-140">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9855f-140">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9855f-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9855f-141">Minimum supported server</span></span><br/> | <span data-ttu-id="9855f-142">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9855f-142">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9855f-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9855f-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9855f-144">**SdbOpenDatabase**</span><span class="sxs-lookup"><span data-stu-id="9855f-144">**SdbOpenDatabase**</span></span>](sdbopendatabase.md)
</dt> </dl>

 

 





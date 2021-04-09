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
# <a name="domain-controller-and-replication-management-structures"></a>網域控制站和複寫管理結構

網域控制站和複寫管理函數會使用下列結構：

-   [**DS \_ 域 \_ 控制器 \_ 資訊 \_ 1**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_domain_controller_info_1a)
-   [**DS \_ 域 \_ 控制器 \_ 資訊 \_ 2**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_domain_controller_info_2a)
-   [**DS \_ 域 \_ 控制器 \_ 資訊 \_ 3**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_domain_controller_info_3a)
-   [**DS \_ 名稱 \_ 結果**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_name_resulta)
-   [**DS \_ 名稱 \_ 結果 \_ 專案**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_name_result_itema)
-   [**DS \_ 複製 \_ ATTR \_ 元 \_ 資料**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_attr_meta_data)
-   [**DS \_ 複製 \_ ATTR \_ 元 \_ 資料 \_ 2**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_attr_meta_data_2)
-   [**DS \_ 複製 \_ ATTR \_ 元 \_ 資料 \_ BLOB**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_attr_meta_data_blob)
-   [**DS \_ 複製 \_ ATTR \_ 值 \_ 元 \_ 資料**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_attr_value_meta_data)
-   [**DS \_ 複製 \_ ATTR \_ 值 \_ META \_ DATA \_ 2**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_attr_value_meta_data_2)
-   [**DS \_ 複製 \_ ATTR \_ 值 \_ META \_ DATA \_ EXT**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_attr_value_meta_data_ext)
-   [**DS 複寫資料 \_ \_ 指標**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursor)
-   [**DS 複寫資料 \_ \_ 指標 \_ 2**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursor_2)
-   [**DS 複寫資料 \_ \_ 指標 \_ 3**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursor_3w)
-   [**DS 複寫資料 \_ \_ 指標 \_ BLOB**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursor_blob)
-   [**DS 複寫資料 \_ \_ 指標**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursors)
-   [**DS 複寫資料 \_ \_ 指標 \_ 2**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursors_2)
-   [**DS 複寫資料 \_ \_ 指標 \_ 3**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursors_3w)
-   [**DS \_ 複寫 \_ KCC \_ DSA \_ 失敗**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_kcc_dsa_failurew)
-   [**DS \_ 複寫 \_ KCC \_ DSA \_ 失敗**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_kcc_dsa_failuresw)
-   [**DS \_ 複寫 \_ KCC \_ DSA \_ FAILUREW \_ BLOB**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_kcc_dsa_failurew_blob)
-   [**DS \_ 複寫 \_ 鄰近**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_neighborw)
-   [**DS \_ 複寫 \_ 鄰近專案**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_neighborsw)
-   [**DS \_ 複寫 \_ NEIGHBORW \_ BLOB**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_neighborw_blob)
-   [**DS \_ 複寫 \_ OBJ \_ 元 \_ 資料**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_obj_meta_data)
-   [**DS \_ 複寫 \_ OBJ \_ 元 \_ 資料 \_ 2**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_obj_meta_data_2)
-   [**DS \_ 複製 \_ 作業**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_opw)
-   [**DS \_ 複寫 \_ OPW \_ BLOB**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_opw_blob)
-   [**DS 複寫擱置中的 \_ \_ \_ OPS**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_pending_opsw)
-   [**DS \_ 複寫 \_ 佇列 \_ STATISTICSW**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_queue_statisticsw)
-   [**DS \_ 複寫 \_ 佇列 \_ STATISTICSW \_ BLOB**](/previous-versions/windows/desktop/legacy/ms676274(v=vs.85))
-   [**DS \_ 複寫 \_ 值 \_ 元 \_ 資料**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_value_meta_data)
-   [**DS \_ 複寫 \_ 值 \_ 元 \_ 資料 \_ 2**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_value_meta_data_2)
-   [**DS \_ 複寫 \_ 值 \_ 元 \_ 資料 \_ EXT**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_value_meta_data_ext)
-   [**DS \_ 複寫 \_ 值 \_ 元 \_ 資料 \_ BLOB**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_value_meta_data_blob)
-   [**DS \_ 複寫 \_ 值 \_ 元 \_ 資料 \_ BLOB \_ EXT**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_value_meta_data_blob_ext)
-   [**DS \_ REPSYNCALL \_ ERRINFO**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repsyncall_errinfoa)
-   [**DS \_ REPSYNCALL \_ 同步處理**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repsyncall_synca)
-   [**DS \_ REPSYNCALL \_ 更新**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repsyncall_updatea)
-   [**DS \_ 架構 \_ GUID \_ 對應**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_schema_guid_mapa)
-   [**DS \_ 網站 \_ 成本 \_ 資訊**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_site_cost_info)
-   [**附表**](/windows/desktop/api/Schedule/ns-schedule-schedule)
-   [**排程 \_ 標頭**](/windows/desktop/api/Schedule/ns-schedule-schedule_header)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Active Directory Domain Services 中的結構](structures-in-active-directory-domain-services.md)
</dt> </dl>

 

 
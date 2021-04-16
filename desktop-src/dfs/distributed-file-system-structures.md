---
description: 以下是分散式檔案系統 DFS 結構
ms.assetid: f55ad3c0-0457-4d5a-a7d3-8eff744d573d
title: 分散式檔案系統結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42fc3351402c4721952cbfc4dc3fe3c6ac6d3a76
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468472"
---
# <a name="distributed-file-system-structures"></a>分散式檔案系統結構

以下是 DFS) 結構的分散式檔案系統 (：

## <a name="in-this-section"></a>本節內容

<dl> <dt>

[**DFS_GET_PKT_ENTRY_STATE_ARG**](/windows/win32/api/lmdfs/ns-lmdfs-dfs_get_pkt_entry_state_arg)
</dt> <dd>

搭配 [**FSCTL_DFS_GET_PKT_ENTRY_STATE**](fsctl-dfs-get-pkt-entry-state.md) 控制程式代碼使用的輸入緩衝區
</dd> <dt>

[_DFS_INFO_1 結構](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_1)
</dt> <dd>
包含分散式檔案系統 (DFS) 根目錄或連結的名稱。

</dd> <dt>

[_DFS_INFO_2 結構](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_2)
</dt> <dd>
包含分散式檔案系統 (DFS) 根或連結的相關資訊。 此結構包含根或連結的名稱、狀態和 DFS 目標數目。

</dd> <dt>

[_DFS_INFO_3 結構](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_3)
</dt> <dd>
包含分散式檔案系統 (DFS) 根或連結的相關資訊。 此結構包含名稱、狀態、DFS 目標數目，以及根或連結的每個目標的相關資訊。

</dd> <dt>

[_DFS_INFO_4 結構](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_4)
</dt> <dd>
包含分散式檔案系統 (DFS) 根或連結的相關資訊。 此結構包含名稱、狀態、 **GUID**、超時時間、目標數目，以及根或連結的每個目標的相關資訊。

</dd> <dt>

[_DFS_INFO_5 結構](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_5)
</dt> <dd>
包含分散式檔案系統 (DFS) 根或連結的相關資訊。 此結構包含名稱、狀態、 **GUID**、超時、命名空間/根/連結屬性、中繼資料大小，以及根或連結的目標數目。

</dd> <dt>

[_DFS_INFO_6 結構](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_6)
</dt> <dd>
包含分散式檔案系統 (DFS) 根或連結的相關資訊。 此結構包含名稱、狀態、 **GUID**、超時、命名空間/根/連結屬性、中繼資料大小、目標數目，以及每個根或連結目標的相關資訊。

</dd> <dt>

[_DFS_INFO_7 結構](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_7)
</dt> <dd>
包含 DFS 命名空間的相關資訊。 此結構包含命名空間中繼資料的版本 **GUID** 。

</dd> <dt>

[_DFS_INFO_8 結構](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_8)
</dt> <dd>
包含根或連結的名稱、狀態、 **GUID**、超時、屬性旗標、中繼資料大小、DFS 目標資訊，以及連結重新分析點安全描述項。

</dd> <dt>

[_DFS_INFO_9 結構](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_9)
</dt> <dd>
包含名稱、狀態、 **GUID**、超時、屬性旗標、中繼資料大小、DFS 目標資訊、連結重新分析點安全描述項，以及根或連結的 DFS 目標清單。

</dd> <dt>

[_DFS_INFO_50 結構](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_50)
</dt> <dd>
包含現有 DFS 命名空間的 DFS 中繼資料版本和功能。

</dd> <dt>

[_DFS_INFO_100 結構](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_100)
</dt> <dd>
包含與分散式檔案系統 (DFS) 根或連結相關聯的批註。

</dd> <dt>

[_DFS_INFO_101 結構](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_101)
</dt> <dd>
描述 DFS 根目錄、連結、根目標或連結目標上的儲存狀態。

</dd> <dt>

[_DFS_INFO_102 結構](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_102)
</dt> <dd>
包含與指定的 DFS 根目錄中的分散式檔案系統 (DFS) 根目錄或連結相關聯的超時值。

</dd> <dt>

[_DFS_INFO_103 結構](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_103)
</dt> <dd>
包含屬性，這些屬性會設定 DFS 根目錄或連結的特定行為。

</dd> <dt>

[_DFS_INFO_104 結構](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_104)
</dt> <dd>
包含 DFS 根目標或連結目標的優先順序。

</dd> <dt>

[_DFS_INFO_105 結構](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_105)
</dt> <dd>
包含有關 DFS 根目錄或連結的資訊，包括批註、狀態、超時，以及屬性旗標所指定的 DFS 行為。

</dd> <dt>

[_DFS_INFO_106 結構](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_106)
</dt> <dd>
包含 DFS 根目標或連結目標的儲存狀態和優先順序。 此結構只適用于 [**NetDfsSetInfo**](netdfssetinfo.md) 函數。

</dd> <dt>

[_DFS_INFO_107 結構](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_107)
</dt> <dd>
包含有關 DFS 根目錄或連結的資訊，包括批註、狀態、超時、屬性旗標和連結重新分析點安全描述項。

</dd> <dt>

[_DFS_INFO_150 結構](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_150)
</dt> <dd>
包含 DFS 連結的重新分析點的安全描述項。

</dd> <dt>

[_DFS_INFO_200 結構](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_200)
</dt> <dd>
包含以網域為基礎的分散式檔案系統名稱 (DFS) 命名空間。

</dd> <dt>

[_DFS_INFO_300 結構](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_300)
</dt> <dd>
包含 DFS 命名空間 (網域型或獨立) 的名稱和類型。

</dd> <dt>

[_DFS_STORAGE_INFO 結構](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_storage_info)
</dt> <dd>
包含 dfs 命名空間或 DFS 用戶端所維護的快取中，DFS 根目錄或連結目標的相關資訊。

</dd> <dt>

[_DFS_STORAGE_INFO_1 結構](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_storage_info_1)
</dt> <dd>
包含 DFS 目標的相關資訊，包括 DFS 目標伺服器名稱和共用名稱，以及目標的狀態和優先順序。

</dd> <dt>

[_DFS_SUPPORTED_NAMESPACE_VERSION_INFO 結構](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_supported_namespace_version_info)
</dt> <dd>
包含 DFS 命名空間的版本資訊。

</dd> <dt>

[_DFS_TARGET_PRIORITY 結構](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_target_priority)
</dt> <dd>
包含特定 DFS 目標的優先順序類別和等級。

</dd> </dl>

---
title: 分散式檔案系統函式
description: 以下是分散式檔案系統 (DFS) 函式的功能。
ms.assetid: 8f86b717-fe26-4550-8b71-8f7df5ca6022
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 463c085115f6d3e88f9a3be80a890caa0aacb340
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468469"
---
# <a name="distributed-file-system-functions"></a>分散式檔案系統函式

以下是分散式檔案系統 (DFS) 函式的功能。

## <a name="in-this-section"></a>本節內容

<dl> <dt>

[NetDfsAdd](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsadd)
</dt> <dd>
建立新的分散式檔案系統 (DFS) 連結，或將目標新增至 DFS 命名空間中的現有連結。

</dd> <dt>

[NetDfsAddFtRoot](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsaddftroot)
</dt> <dd>
建立以網域為基礎的新分散式檔案系統 (DFS) 命名空間。 如果命名空間已存在，則函式會將指定的根目標新增至該命名空間。

</dd> <dt>

[NetDfsAddRootTarget](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsaddroottarget)
</dt> <dd>
建立網域型或獨立 DFS 命名空間，或將新的根目標新增至現有網域型命名空間。

</dd> <dt>

[NetDfsAddStdRoot](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsaddstdroot)
</dt> <dd>
建立新的獨立分散式檔案系統 (DFS) 命名空間。

</dd> <dt>

[NetDfsEnum](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsenum)
</dt> <dd>
列舉伺服器上裝載的分散式檔案系統 (DFS) 命名空間，或是由伺服器主控之命名空間的 DFS 連結。

</dd> <dt>

[NetDfsGetClientInfo](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo)
</dt> <dd>
從 DFS 用戶端所維護的快取中，抓取分散式檔案系統 (DFS) 根目錄或連結的相關資訊。

</dd> <dt>

[NetDfsGetFtContainerSecurity](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetftcontainersecurity)
</dt> <dd>
針對指定 Active Directory 網域中的網域型 DFS 命名空間，抓取容器物件的安全描述項。

</dd> <dt>

[NetDfsGetInfo](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetinfo)
</dt> <dd>
抓取 DFS 命名空間中指定的分散式檔案系統 (DFS) 根目錄或連結的相關資訊。

</dd> <dt>

[NetDfsGetSecurity](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetsecurity)
</dt> <dd>
抓取指定 DFS 命名空間之根物件的安全描述項。

</dd> <dt>

[NetDfsGetStdContainerSecurity](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetstdcontainersecurity)
</dt> <dd>
抓取指定獨立 DFS 命名空間之容器物件的安全描述項。

</dd> <dt>

[NetDfsGetSupportedNamespaceVersion](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetsupportednamespaceversion)
</dt> <dd>
判斷支援的中繼資料版本號碼。

</dd> <dt>

[NetDfsMove](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsmove)
</dt> <dd>
重新命名或移動 DFS 連結。

</dd> <dt>

[NetDfsRemove](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremove)
</dt> <dd>
移除 dfs 命名空間中 dfs 連結的分散式檔案系統 (DFS) 連結或特定連結目標。 移除特定連結目標時，如果已移除連結的最後一個連結目標，則會移除連結本身。

</dd> <dt>

[NetDfsRemoveFtRoot](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremoveftroot)
</dt> <dd>
從以網域為基礎的分散式檔案系統中移除指定的根目標 (DFS) 命名空間。 如果要移除 DFS 命名空間的最後一個根目標，此函數也會刪除 DFS 命名空間。 您可以刪除 DFS 命名空間，而不需要先刪除其中的所有連結。

</dd> <dt>

[NetDfsRemoveFtRootForced](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremoveftrootforced)
</dt> <dd>
從網域分散式檔案系統 (DFS) 命名空間移除指定的根目標，即使根目標伺服器已離線也一樣。 如果要移除 DFS 命名空間的最後一個根目標，此函數也會刪除 DFS 命名空間。 您可以刪除 DFS 命名空間，而不需要先刪除其中的所有連結。

> [!Note]
> [**NetDfsRemoveFtRootForced**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremoveftrootforced)函數不會更新 DFS 根目標伺服器上的登錄。 如需詳細資訊，請參閱＜備註＞一節。

</dd> <dt>

[NetDfsRemoveRootTarget](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremoveroottarget)
</dt> <dd>
從以網域為基礎的 DFS 命名空間移除 DFS 根目標。 如果根目標是 DFS 命名空間中的最後一個根目標，此函式會移除 DFS 命名空間。 此函式也可以用來移除獨立 DFS 命名空間。

</dd> <dt>

[NetDfsRemoveStdRoot](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremovestdroot)
</dt> <dd>
刪除獨立分散式檔案系統 (DFS) 命名空間。

</dd> <dt>

[NetDfsSetClientInfo](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetclientinfo)
</dt> <dd>
在 DFS 用戶端所維護的快取中，修改分散式檔案系統 (DFS) 根目錄或連結的相關資訊。

</dd> <dt>

[NetDfsSetFtContainerSecurity](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetftcontainersecurity)
</dt> <dd>
針對指定之 Active Directory 網域中的網域型 DFS 命名空間，設定容器物件的安全描述項。

</dd> <dt>

[NetDfsSetInfo](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetinfo)
</dt> <dd>
設定或修改特定分散式檔案系統 (DFS) 根、根目標、連結或連結目標的相關資訊。

</dd> <dt>

[NetDfsSetSecurity](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetsecurity)
</dt> <dd>
設定指定 DFS 命名空間之根物件的安全描述項。

</dd> <dt>

[NetDfsSetStdContainerSecurity](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetstdcontainersecurity)
</dt> <dd>
設定指定之獨立 DFS 命名空間之容器物件的安全描述項。

</dd> </dl>

請注意，叫用任何函式的應用程式可能會間接讓本機 DFS 命名空間伺服器服務函式呼叫，從該網域的 PDC 模擬器主機執行相關命名空間中繼資料的完整同步處理。 即使已針對該命名空間設定根擴充性模式，也可能會發生這項完整的同步處理。

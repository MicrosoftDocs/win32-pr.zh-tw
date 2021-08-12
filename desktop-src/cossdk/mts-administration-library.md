---
description: 隨附于 COM + 系統管理介面的 MTS 管理程式庫會提供與 MTS 2.0 管理程式庫的回溯相容性。
ms.assetid: 5eb9e68c-4f3b-4d57-bd51-704211d817fe
title: MTS 管理程式庫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51e449e99ef675f7f8ce893a358806926cd3d1a63ed13e5cc9fff01b97d0742d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118306156"
---
# <a name="mts-administration-library"></a>MTS 管理程式庫

隨附于 COM + 系統管理介面的 MTS 管理程式庫會提供與 MTS 2.0 管理程式庫的回溯相容性。 大部分現有的 MTS 2.0 管理程式碼仍可與提供的 MTSAdmin 程式庫搭配使用;不過，某些功能已變更。

若要利用新功能或第一次撰寫管理程式碼，您應該使用 COMAdmin 程式庫。

目前的 MTS 管理程式庫中的下列元素會從 MTS 2.0 管理程式庫變更：

-   **IRemoteComponentUtil** 介面無法再使用。
-   無法再使用 **RemoteComponents** 集合。
-   RoleID 屬性已無法再使用，角色名稱現在會做為此的索引鍵。
-   **ExportPackage** 方法不再匯出 client.exe。
-   RemoteComponentInstallPath 屬性不再于 [**LocalComputer**](localcomputer.md) 集合公開。
-   ApplicationInstallPath 屬性將不再于 [**LocalComputer**](localcomputer.md) 集合公開。
-   系統封裝現在已命名為 [系統應用程式]。
-   公用程式套件現在已命名為 COM + 公用程式。
-   IsSystem 屬性存在於 MTSAdmin 中的 [**元件**](components.md) 集合中，但會在核取時傳回 ">notimpl"，如果設定，將不會儲存。
-   [**元件**](components.md)集合已不再支援 PackageName 屬性。 若要找出套件的名稱，您現在需要取得 PackageID，然後在封裝集合中尋找相符的封裝。
-   下列屬性已不再存在於 [**InterfacesForComponent**](interfacesforcomponent.md) 集合上：
    -   **ProxyCLSID**
    -   **ProxyDLL**
    -   **ProxyThreadingModel**
    -   **TypeLibFile**
    -   **TypeLibID**
    -   **TypeLibLangID**
    -   **TypeLibPlatform**
    -   **TypeLibVersion**

## <a name="related-topics"></a>相關主題

<dl> <dt>

[從 MTS 自動轉換](automatic-conversion-from-mts.md)
</dt> <dt>

[COM + 轉換結果和問題](com--conversion-results-and-issues.md)
</dt> <dt>

[從 MTS 手動轉換](manual-conversion-from-mts.md)
</dt> </dl>

 

 




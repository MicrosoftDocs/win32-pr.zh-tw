---
description: 依賴網路資源進行隨選安裝的應用程式，可能會因為來源位置因任何原因而變更或損毀，而受到來源失敗的影響。
ms.assetid: 3d6a0524-d5df-4d4c-b861-d4a7da95ce40
title: 來源復原
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46944804db1c4b91c6c6757303fd2af90638b12e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936644"
---
# <a name="source-resiliency"></a>來源復原

依賴網路資源進行 [隨選安裝](installation-on-demand.md) 的應用程式，可能會因為來源位置因任何原因而變更或損毀，而受到來源失敗的影響。 Windows Installer 會使用來源清單，為隨選安裝的功能提供來源復原功能。 來源清單包含安裝套件安裝程式所搜尋的位置。 這份清單中的專案可以是網路位置、統一資源定位器 (Url) 或 compact 光碟。 如果其中一項來源失敗，安裝程式可以快速且順暢地嘗試下一個。

應用程式開發人員不需要將任何特殊資訊納入安裝程式套件，以確保來源復原。 一旦安裝應用程式，安裝程式就會將最後一個成功使用的來源新增為來源清單中的專案。 根據預設，此來源是安裝程式套件最初安裝所在的位置，與 [**SourceDir**](sourcedir.md) 屬性相同。

系統管理員可以藉由套用 [轉換](merges-and-transforms.md)或從命令列或在 [屬性工作表](property-table.md)中變更 [**SOURCELIST**](sourcelist.md)屬性，來變更來源清單。

安裝程式會藉由檢查來源清單中最近使用的來源位置，開始搜尋來源。 如果此搜尋失敗，安裝程式會搜尋網路來源清單、媒體來源和最後的 URL 來源。 系統管理員可以使用 [SearchOrder](searchorder.md) 系統原則來變更此搜尋順序。 如果這些搜尋失敗，安裝程式可能會顯示 [流覽對話方塊](browse-dialog.md) ，讓使用者可以手動搜尋來源。 如果使用者介面層級設定為 [無]，則無法顯示 [流覽] 對話方塊。 如需詳細資訊，請參閱 [消費者介面層級](user-interface-levels.md)。

通常，如果目前的使用者是系統管理員，或如果安裝不需要較高的許可權，安裝程式應該只顯示 [流覽] 對話方塊。 系統管理員可以控制具有 [DisableBrowse](disablebrowse.md) 和 [AllowLockDownBrowse](allowlockdownbrowse.md) 原則的使用者對 [流覽] 對話方塊的顯示。 系統管理員也會控制使用者是否可以使用 [DisableMedia](disablemedia.md) 和 [AllowLockDownMedia](allowlockdownmedia.md) 原則，從位於媒體的來源安裝應用程式。 使用這些原則取決於 Windows Installer 版本。 如需詳細資訊，請參閱下列內容：

-   [來源復原原則](source-resiliency-policy-windows-installer-version-2-0.md)

 

 




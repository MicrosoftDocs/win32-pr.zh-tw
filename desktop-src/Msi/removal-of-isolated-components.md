---
description: 當封裝包含隔離的元件時，Windows Installer 在移除應用程式期間執行下列動作。 通常， \_ 共用元件是元件 \_ 應用程式和其他用戶端可執行檔共用的 DLL。
ms.assetid: 26343a01-9a06-43d5-bbe3-959faf51739d
title: 移除隔離的元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adf19769067230b82f68a35f7b9fbedcd1c56440
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107000298"
---
# <a name="removal-of-isolated-components"></a>移除隔離的元件

當封裝包含隔離的元件時，Windows Installer 在移除應用程式期間執行下列動作。 通常， \_ 共用元件是元件 \_ 應用程式和其他用戶端可執行檔共用的 DLL。

## <a name="uninstall"></a>解除安裝

-   \_ \_ 只有在同時移除元件應用程式時，才移除包含元件應用程式之資料夾中共用的元件檔案 \_ 。
-   如果 msidbComponentAttributesSharedDllRefCount 位設定在 [元件資料表](component-table.md) 中，則會遞減 SharedDLL refcount。
-   移除。包含元件應用程式之資料夾中的本機零位元組檔案 \_ 。
-   \_從共用的元件用戶端清單中移除元件應用程式 \_ 。
-   照常移除元件應用程式的所有資源 \_ 。

如果已共用元件的用戶端清單中剩餘其他產品 \_ ：

-   從共用的元件共用位置移除沒有任何檔案 \_ 。

如果共用元件的 SharedDLL refcount 在 \_ 遞減之後為0，或者，如果沒有其他剩餘的元件共用用戶端 \_ ：

-   移除共用位置共用的元件檔案 \_ 。
-   處理與此元件相關的所有卸載動作。

 

 




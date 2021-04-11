---
description: 當套件包含隔離的元件時，Windows Installer 在重新安裝應用程式期間執行下列動作。 通常， \_ 共用元件是元件 \_ 應用程式和其他用戶端可執行檔共用的 DLL。
ms.assetid: 65909b47-dc09-4e9a-920a-9cb3f55b2e67
title: 重新安裝隔離的元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68ad1c7fb53eb09e96882209f7738e95be9b4a64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849146"
---
# <a name="reinstallation-of-isolated-components"></a>重新安裝隔離的元件

當套件包含隔離的元件時，Windows Installer 在重新安裝應用程式期間執行下列動作。 通常， \_ 共用元件是元件 \_ 應用程式和其他用戶端可執行檔共用的 DLL。

## <a name="reinstallation"></a>重新安裝

-   \_ \_ 只有在 \_ 同時重新安裝元件應用程式時，才將與元件應用程式共用的元件檔案重新安裝在同一個資料夾中。
-   請勿遞增共用元件的用戶端清單 \_ ，也不會遞增 SharedDLL 計數。
-   使用元件應用程式金鑰檔的簡短檔案名來重新建立零位元組檔案 \_ 。 這個檔案必須位於與元件應用程式相同的資料夾中 \_ ，而且副檔名為。當地。
-   照常重新安裝元件應用程式的所有資源 \_ 。

如果共用元件的 SharedDLL refcount \_ 超過1，或其他產品仍在共用的元件用戶端清單上 \_ ：

-   將任何檔案重新安裝至共用的元件共用位置 \_ 。

如果共用之元件的 SharedDLL refcount \_ 等於1，或沒有其他剩餘的元件共用用戶端 \_ ：

-   \_使用檔案[版本控制規則](file-versioning-rules.md)，重新安裝共用位置中共用的元件檔案。
-   處理元件共用的所有重新安裝動作 \_ 。
-   如果元件 \_ 共用是 com 元件，請註冊完整的 com 路徑，讓安裝程式語法 \[ $Component \] 和 \[ \# FileKey \] 指向共用的元件共用位置 \_ 。

 

 




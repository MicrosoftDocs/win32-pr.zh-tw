---
description: 當封裝包含隔離的元件時，Windows Installer 在安裝應用程式期間執行下列動作。 通常， \_ 共用元件是元件 \_ 應用程式和其他用戶端可執行檔共用的 DLL。
ms.assetid: fbc5dd86-5d38-4ce8-ab38-03c84cc77e80
title: 獨立元件的安裝
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3c1b9a7e21c212474701409e887d0afd5517774
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691560"
---
# <a name="installation-of-isolated-components"></a>獨立元件的安裝

當封裝包含隔離的元件時，Windows Installer 在安裝應用程式期間執行下列動作。 通常， \_ 共用元件是元件 \_ 應用程式和其他用戶端可執行檔共用的 DLL。

## <a name="installation"></a>安裝

-   \_ \_ 只有在同時安裝元件應用程式時，才將共用的元件檔案複製到與元件應用程式相同的資料夾中 \_ 。
-   使用元件應用程式金鑰檔的簡短檔案名來建立零位元組檔案 \_ 。 在與元件應用程式相同的資料夾中找到這個檔案 \_ 。 附加延伸模組。這個檔案名的本機。
-   如果在 [元件資料表](component-table.md)的 [屬性] 資料行中設定了 msidbComponentAttributesSharedDllRefCount 位，則遞增 SharedDLL refcount。
-   將元件 \_ 應用程式註冊為共用元件的用戶端 \_ ，並註冊指向共用元件共用位置的金鑰路徑 \_ 。
-   照常安裝元件應用程式的所有資源 \_ 。

如果 \_ 電腦上已安裝元件共用或其金鑰檔，則不會將檔案複製到共用的元件共用位置 \_ 。

如果 \_ 電腦上尚未安裝元件共用或其金鑰檔：

-   將共用的元件檔案複製 \_ 到共用位置。
-   處理元件共用的所有安裝動作 \_ 。
-   如果元件 \_ 共用是 com 元件，請註冊完整的 com 路徑，讓語法 \[ $Component \] 和 \[ \# FileKey \] 指向共用的元件共用位置 \_ 。

 

 




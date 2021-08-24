---
description: UnregisterMIMEInfo 動作會從系統中取消註冊 MIME 相關的登錄資訊。 動作會從 MIME 資料表中取消註冊伺服器的 MIME 資訊，而這項功能目前已選取要卸載的對應功能。
ms.assetid: 9a5c12da-e78f-4c99-9b82-d41624593c61
title: UnregisterMIMEInfo 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e03ea1c50aa543615edc0ed875bd83b3338cdb261d09e01232e0fe76f7aa51ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810138"
---
# <a name="unregistermimeinfo-action"></a>UnregisterMIMEInfo 動作

UnregisterMIMEInfo 動作會從系統中取消註冊 MIME 相關的登錄資訊。 動作會從 [mime 資料表](mime-table.md) 中取消註冊伺服器的 mime 資訊，而這項功能目前已選取要卸載的對應功能。

## <a name="sequence-restrictions"></a>順序限制

UnregisterMIMEInfo 動作必須位於 [InstallInitialize](installinitialize-action.md) 動作、 [UnregisterClassInfo](unregisterclassinfo-action.md) 動作、 [UnregisterExtensionInfo](unregisterextensioninfo-action.md) 動作和 [RegisterMIMEInfo](registermimeinfo-action.md) 動作之前。

[RemoveRegistryValues](removeregistryvalues-action.md) 必須在順序中 UnregisterMIMEInfo 之前。

下列群組中的動作順序會受到限制。 如果這些動作的任何子集在順序資料表中一起發生，它們必須具有相同的相對順序順序，如下所示：

-   [UnregisterClassInfo](unregisterclassinfo-action.md)
-   [UnregisterExtensionInfo](unregisterextensioninfo-action.md)
-   [UnregisterProgIdInfo](unregisterprogidinfo-action.md)
-   UnregisterMIMEInfo
-   [RegisterClassInfo](registerclassinfo-action.md)
-   [RegisterExtensionInfo](registerextensioninfo-action.md)
-   [RegisterProgIdInfo](registerprogidinfo-action.md)
-   [RegisterMIMEInfo](registermimeinfo-action.md)

例如，UnregisterMIMEInfo 必須在順序資料表的 [RegisterExtensionInfo](registerextensioninfo-action.md) 之前。

## <a name="actiondata-messages"></a>ActionData 訊息



| 欄位 | 動作資料的描述                    |
|-------|-----------------------------------------------|
| \[1\] | 未註冊 MIME 內容類型的識別碼。 |
| \[2\] | 與 MIME 內容類型相關聯的副檔名。  |



 

 

 




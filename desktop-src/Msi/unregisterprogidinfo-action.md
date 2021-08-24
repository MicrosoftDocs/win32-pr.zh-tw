---
description: UnregisterProgIdInfo 動作會管理將 OLE ProgId 資訊與系統的註冊。
ms.assetid: c9837845-4ffc-4496-8330-11b46d27ec7a
title: UnregisterProgIdInfo 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6666e5648cba220dbb9bbc6e2d50c3959c1d73c98f97dcfd8c45cb3de8d94c82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119786958"
---
# <a name="unregisterprogidinfo-action"></a>UnregisterProgIdInfo 動作

UnregisterProgIdInfo 動作會管理將 OLE ProgId 資訊與系統的註冊。

## <a name="sequence-restrictions"></a>順序限制

UnregisterProgIdInfo 動作必須位於 [InstallInitialize](installinitialize-action.md) 動作、 [UnregisterClassInfo](unregisterclassinfo-action.md) 動作、 [UnregisterExtensioninfo](unregisterextensioninfo-action.md) 動作和 [RegisterProgIdInfo](registerprogidinfo-action.md) 動作之前。

[RemoveRegistryValues](removeregistryvalues-action.md) 必須在順序中 UnregisterProgIdInfo 之前。

下列群組中的動作順序會受到限制。 如果這些動作的任何子集在順序資料表中一起發生，它們必須具有相同的相對順序順序，如下所示：

-   [UnregisterClassInfo](unregisterclassinfo-action.md)
-   [UnregisterExtensioninfo](unregisterextensioninfo-action.md)
-   UnregisterProgIdInfo
-   [UnregisterMIMEInfo](unregistermimeinfo-action.md)
-   [RegisterClassInfo](registerclassinfo-action.md)
-   [RegisterExtensionInfo](registerextensioninfo-action.md)
-   [RegisterProgIdInfo](registerprogidinfo-action.md)
-   [RegisterMIMEInfo](registermimeinfo-action.md)

例如，UnregisterProgIdInfo 必須在順序資料表的 [UnregisterMIMEInfo](unregistermimeinfo-action.md) 之前。

## <a name="actiondata-messages"></a>ActionData 訊息



| 欄位 | 動作資料的描述                |
|-------|-------------------------------------------|
| \[1\] | 已註冊程式的程式識別碼。 |



 

## <a name="remarks"></a>備註

UnregisterProgIdInfo 動作會從登錄中移除 ProgId 資訊 ([Progid 資料表](progid-table.md)) 針對連接到擴充功能資訊 ([延伸模組資料表](extension-table.md)) 或類別資訊 ([類別表](class-table.md)) 和目前已選取要卸載的功能。

 

 




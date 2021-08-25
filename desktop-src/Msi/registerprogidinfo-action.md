---
description: RegisterProgIdInfo 動作會管理與系統之間的 OLE ProgId 資訊註冊。
ms.assetid: f6fd4d0d-d2dc-4953-9402-314c7932746b
title: RegisterProgIdInfo 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84cebf5ddb3bf8b9c98ebea0364b685016d343afa283b937400360f31bbcebd9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912828"
---
# <a name="registerprogidinfo-action"></a>RegisterProgIdInfo 動作

RegisterProgIdInfo 動作會管理與系統之間的 OLE ProgId 資訊註冊。

## <a name="sequence-restrictions"></a>順序限制

RegisterProgIdInfo 動作必須位於 [InstallFiles](installfiles-action.md) 動作、 [UnregisterProgIdInfo](unregisterprogidinfo-action.md) 動作、 [RegisterClassInfo](registerclassinfo-action.md) 動作和 [RegisterExtensionInfo](registerextensioninfo-action.md) 動作之後。

下列群組中的動作順序會受到限制。 如果這些動作的任何子集在順序資料表中一起發生，它們必須具有相同的相對順序順序，如下所示：

-   [UnregisterClassInfo](unregisterclassinfo-action.md)
-   [UnregisterExtensionInfo](unregisterextensioninfo-action.md)
-   [UnregisterProgIdInfo](unregisterprogidinfo-action.md)
-   [UnregisterMIMEInfo](unregistermimeinfo-action.md)
-   [RegisterClassInfo](registerclassinfo-action.md)
-   [RegisterExtensionInfo](registerextensioninfo-action.md)
-   RegisterProgIdInfo
-   [RegisterMIMEInfo](registermimeinfo-action.md)

例如，RegisterProgIdInfo 必須在 [RegisterExtensionInfo](registerextensioninfo-action.md) 的順序資料表中。

## <a name="actiondata-messages"></a>ActionData 訊息



| 欄位 | 動作資料的描述                |
|-------|-------------------------------------------|
| \[1\] | 已註冊程式的程式識別碼。 |



 

## <a name="remarks"></a>備註

RegisterProgIdInfo 動作會註冊 [progid 資料表](progid-table.md) 中指定之伺服器的所有 progid 資訊，以及已選取要安裝的對應類別伺服器或延伸模組伺服器。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[類別資料表](class-table.md)
</dt> <dt>

[延伸模組資料表](extension-table.md)
</dt> </dl>

 

 




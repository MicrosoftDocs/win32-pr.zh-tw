---
description: RegisterMIMEInfo 動作會向系統註冊 MIME 相關的登錄資訊。
ms.assetid: 2ba88b5f-bd8a-4572-af82-9c0b91b9b6d9
title: RegisterMIMEInfo 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 369f35eab4e6d4228167bfbeda48cf21249ea6a63297f5a9e893b84dcc4ed5bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041738"
---
# <a name="registermimeinfo-action"></a>RegisterMIMEInfo 動作

RegisterMIMEInfo 動作會向系統註冊 MIME 相關的登錄資訊。

## <a name="sequence-restrictions"></a>順序限制

RegisterMIMEInfo 動作必須位於 [InstallFiles](installfiles-action.md) 動作、 [UnregisterMIMEInfo](unregistermimeinfo-action.md) 動作、 [RegisterClassInfo](registerclassinfo-action.md) 動作和 [RegisterExtensionInfo](registerextensioninfo-action.md) 動作之後。

下列群組中的動作順序會受到限制。 如果這些動作的任何子集在順序資料表中一起發生，它們必須具有相同的相對順序順序，如下所示：

-   [UnregisterClassInfo](unregisterclassinfo-action.md)
-   [UnregisterExtensionInfo](unregisterextensioninfo-action.md)
-   [UnregisterProgIdInfo](unregisterprogidinfo-action.md)
-   [UnregisterMIMEInfo](unregistermimeinfo-action.md)
-   [RegisterClassInfo](registerclassinfo-action.md)
-   [RegisterExtensionInfo](registerextensioninfo-action.md)
-   [RegisterProgIdInfo](registerprogidinfo-action.md)
-   RegisterMIMEInfo

例如，RegisterMIMEInfo 必須在 [UnregisterMIMEInfo](unregistermimeinfo-action.md) 的順序資料表中。

## <a name="actiondata-messages"></a>ActionData 訊息



| 欄位 | 動作資料的描述                   |
|-------|----------------------------------------------|
| \[1\] | 已註冊之 MIME 內容類型的識別碼。  |
| \[2\] | 與 MIME 內容類型相關聯的副檔名。 |



 

## <a name="remarks"></a>備註

RegisterMIMEInfo 動作會註冊 [mime 資料表](mime-table.md) 中，已選取要安裝對應類別伺服器或延伸模組伺服器之伺服器的所有 mime 資訊。

 

 




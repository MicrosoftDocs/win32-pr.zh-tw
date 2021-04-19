---
description: RegisterClassInfo 動作會管理 COM 類別資訊與系統的註冊。 它會使用 AppId 資料表。
ms.assetid: f8b60a75-9c0e-41c5-b6af-6a05a26b2d71
title: RegisterClassInfo 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd916772bc236dfc86df336347514c10d5dfbce7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106988777"
---
# <a name="registerclassinfo-action"></a>RegisterClassInfo 動作

RegisterClassInfo 動作會管理 COM 類別資訊與系統的註冊。 它會使用 [AppId 資料表](appid-table.md)。

## <a name="sequence-restrictions"></a>順序限制

RegisterClassInfo 動作必須位於 [InstallFiles](installfiles-action.md) 動作和 [UnregisterClassInfo](unregisterclassinfo-action.md) 動作之後。

下列群組中的動作順序會受到限制。 如果這些動作的任何子集在順序資料表中一起發生，它們必須具有相同的相對順序順序，如下所示：

-   [UnregisterClassInfo](unregisterclassinfo-action.md)
-   [UnregisterExtensionInfo](unregisterextensioninfo-action.md)
-   [UnregisterProgIdInfo](unregisterprogidinfo-action.md)
-   [UnregisterMIMEInfo](unregistermimeinfo-action.md)
-   RegisterClassInfo
-   [RegisterExtensionInfo](registerextensioninfo-action.md)
-   [RegisterProgIdInfo](registerprogidinfo-action.md)
-   [RegisterMIMEInfo](registermimeinfo-action.md)

例如，RegisterClassInfo 必須在 [UnregisterMIMEInfo](unregistermimeinfo-action.md) 的順序資料表中。

## <a name="actiondata-messages"></a>ActionData 訊息



| 欄位 | 動作資料的描述                          |
|-------|-----------------------------------------------------|
| \[1\] | 已註冊 COM 伺服器的 GUID 類別識別碼。 |



 

## <a name="remarks"></a>備註

如果系統支援 OLE 伺服器的隨選安裝，RegisterClassInfo 會在與選取要安裝或通告之功能相關聯的 [類別資料表](class-table.md) 中註冊所有 COM 類別。 否則，此動作只會註冊與選取要安裝之功能相關聯的 COM 類別。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**OLEAdvtSupport 屬性**](oleadvtsupport.md)
</dt> </dl>

 

 




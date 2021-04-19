---
description: UnregisterClassInfo 動作會管理從系統登錄移除 COM 類別資訊。 它會使用 AppId 資料表。
ms.assetid: 579a69ee-92cd-4d4c-a007-998ec042f9fc
title: UnregisterClassInfo 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57ee701925e07e4f74439efb45da00d430d90304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107001454"
---
# <a name="unregisterclassinfo-action"></a>UnregisterClassInfo 動作

UnregisterClassInfo 動作會管理從系統登錄移除 COM 類別資訊。 它會使用 [AppId 資料表](appid-table.md)。

## <a name="sequence-restrictions"></a>順序限制

UnregisterClassInfo 動作必須在 [InstallInitialize](installinitialize-action.md) 動作之後，以及在 [RegisterClassInfo](registerclassinfo-action.md) 動作之前。

[RemoveRegistryValues](removeregistryvalues-action.md) 必須在順序中 UnregisterClassInfo 之前。

下列群組中的動作順序會受到限制。 如果這些動作的任何子集在順序資料表中一起發生，它們必須以與下表所示相同的相對順序發生：

-   UnregisterClassInfo
-   [UnregisterExtensionInfo](unregisterextensioninfo-action.md)
-   [UnregisterProgIdInfo](unregisterprogidinfo-action.md)
-   [UnregisterMIMEInfo](unregistermimeinfo-action.md)
-   [RegisterClassInfo](registerclassinfo-action.md)
-   [RegisterExtensionInfo](registerextensioninfo-action.md)
-   [RegisterProgIdInfo](registerprogidinfo-action.md)
-   [RegisterMIMEInfo](registermimeinfo-action.md)

例如， [RegisterExtensionInfo](registerextensioninfo-action.md) 必須在順序資料表的 UnregisterClassInfo 之前。

## <a name="actiondata-messages"></a>ActionData 訊息



| 欄位 | 動作資料的描述      |
|-------|---------------------------------|
| \[1\] | 未註冊 COM 類別的 GUID。 |



 

## <a name="remarks"></a>備註

當目前使用者的系統已升級為搭配透過 COM 的隨選安裝時，安裝程式會將 [**OLEAdvtSupport**](oleadvtsupport.md) 屬性設定為 true。 如果系統不支援透過 COM 進行隨選安裝，UnregisterClassInfo 會將與已卸載的功能或安裝的功能相關聯之 [類別資料表](class-table.md) 中所列的所有 COM 類別，從系統登錄中移除。 否則，此動作只會移除與選取要從系統登錄卸載之功能相關聯的 COM 類別。

 

 




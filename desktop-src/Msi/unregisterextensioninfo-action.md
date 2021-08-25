---
description: UnregisterExtensionInfo 動作會管理從系統登錄移除擴充功能相關資訊的功能。
ms.assetid: 62bb9d17-c221-4bd2-bd7f-9930e28bb946
title: UnregisterExtensionInfo 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e8dae707bc4dd517402d8a85fb64402637a815f8249d4677f18818c855ba4e1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810228"
---
# <a name="unregisterextensioninfo-action"></a>UnregisterExtensionInfo 動作

UnregisterExtensionInfo 動作會管理從系統登錄移除擴充功能相關資訊的功能。

## <a name="sequence-restrictions"></a>順序限制

UnregisterExtensionInfo 動作必須在 [InstallInitialize](installinitialize-action.md) 動作之後，以及在 [RegisterExtensionInfo](registerextensioninfo-action.md) 動作之前。

[RemoveRegistryValues](removeregistryvalues-action.md) 必須在順序中 UnregisterExtensionInfo 之前。

下列群組中的動作順序會受到限制。 如果這些動作的任何子集在順序資料表中一起發生，它們必須具有相同的相對順序順序，如下所示：

-   [UnregisterClassInfo](unregisterclassinfo-action.md)
-   UnregisterExtensionInfo
-   [UnregisterProgIdInfo](unregisterprogidinfo-action.md)
-   [UnregisterMIMEInfo](unregistermimeinfo-action.md)
-   [RegisterClassInfo](registerclassinfo-action.md)
-   [RegisterExtensionInfo](registerextensioninfo-action.md)
-   [RegisterProgIdInfo](registerprogidinfo-action.md)
-   [RegisterMIMEInfo](registermimeinfo-action.md)

例如，UnregisterExtensionInfo 必須在順序資料表的 [UnregisterProgIdInfo](unregisterprogidinfo-action.md) 之前。

## <a name="actiondata-messages"></a>ActionData 訊息



| 欄位 | 動作資料的描述 |
|-------|----------------------------|
| \[1\] | 已移除擴充功能。         |



 

## <a name="remarks"></a>備註

如果系統不支援擴充功能伺服器的隨選安裝，UnregisterExtensionInfo 會移除 [延伸模組資料表](extension-table.md) 中與已卸載的功能相關聯的所有擴充功能伺服器，或從登錄中安裝的功能。 否則，此動作會移除與已選取要從登錄中移除之功能相關聯的延伸模組伺服器。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**ShellAdvtSupport 屬性**](shelladvtsupport.md)
</dt> </dl>

 

 




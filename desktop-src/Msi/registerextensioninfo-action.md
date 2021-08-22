---
description: RegisterExtensionInfo 動作會管理與系統相關的擴充功能相關資訊的註冊。
ms.assetid: 3c243ca3-9fa7-41ec-968e-7954d7d45432
title: RegisterExtensionInfo 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c0541fc512c2300b0cb37f4a23305a3d312a4e60208890507fb7c6112e00c94
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119519378"
---
# <a name="registerextensioninfo-action"></a>RegisterExtensionInfo 動作

RegisterExtensionInfo 動作會管理與系統相關的擴充功能相關資訊的註冊。

## <a name="sequence-restrictions"></a>順序限制

RegisterExtensionInfo 動作必須位於 [InstallFiles](installfiles-action.md) 動作和 [UnregisterExtensionInfo](unregisterextensioninfo-action.md) 動作之後。

下列群組中的動作順序會受到限制。 如果這些動作的任何子集在順序資料表中一起發生，它們必須具有相同的相對順序順序，如下所示：

-   [UnregisterClassInfo](unregisterclassinfo-action.md)
-   [UnregisterExtensionInfo](unregisterextensioninfo-action.md)
-   [UnregisterProgIdInfo](unregisterprogidinfo-action.md)
-   [UnregisterMIMEInfo](unregistermimeinfo-action.md)
-   [RegisterClassInfo](registerclassinfo-action.md)
-   RegisterExtensionInfo
-   [RegisterProgIdInfo](registerprogidinfo-action.md)
-   [RegisterMIMEInfo](registermimeinfo-action.md)

例如，RegisterExtensionInfo 必須在 [UnregisterMIMEInfo](unregistermimeinfo-action.md) 的順序資料表中。

## <a name="actiondata-messages"></a>ActionData 訊息



| 欄位 | 動作資料的描述 |
|-------|----------------------------|
| \[1\] | 註冊的延伸模組。      |



 

## <a name="remarks"></a>備註

如果系統支援擴充功能伺服器的隨選安裝，RegisterExtensionInfo 會在與安裝或公告設定的功能相關聯的 [延伸模組表格](extension-table.md) 中註冊所有延伸模組伺服器。 否則，此動作只會註冊與設定為安裝的功能相關聯的延伸模組伺服器。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**ShellAdvtSupport 屬性**](shelladvtsupport.md)
</dt> </dl>

 

 




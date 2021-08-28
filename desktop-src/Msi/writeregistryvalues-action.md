---
description: WriteRegistryValues 動作會設定應用程式的登錄資訊。
ms.assetid: ab121de3-f07d-401a-b52a-246a555c142c
title: WriteRegistryValues 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e84fd6818ae1180665e523b19a2f674be0826361c76997b74966d3d719ed1d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117989824"
---
# <a name="writeregistryvalues-action"></a>WriteRegistryValues 動作

WriteRegistryValues 動作會設定應用程式的登錄資訊。 登錄資訊會由 [元件表格](component-table.md)進行閘道。 如果對應的元件已設定為要安裝在本機或從來源執行，則會將登錄值寫入登錄。 如需詳細資訊，請參閱登錄 [表](registry-table.md)。

## <a name="sequence-restrictions"></a>順序限制

[InstallValidate 動作](installvalidate-action.md)必須位於 WriteRegistryValues 動作之前。 如果有 [RemoveRegistryValues 動作](removeregistryvalues-action.md)，它必須在 WriteRegistryValues 動作之前。

自訂動作可在安裝、卸載或修復交易期間，用來將資料列新增至登錄 [資料表](registry-table.md) 。 這些資料列不會保存在登錄資料表中，而且只有在目前的交易期間，才可使用此資訊。 因此，自訂動作必須在需要這些額外資料列資訊的每個安裝、卸載或修復交易中執行。 自訂動作必須位於動作順序中的 [RemoveRegistryValues](removeregistryvalues-action.md) 和 WriteRegistryValues 動作之前。

## <a name="actiondata-messages"></a>ActionData 訊息



| 欄位 | 動作資料的描述                               |
|-------|----------------------------------------------------------|
| \[1\] | 寫入登錄之值的登錄機碼路徑。       |
| \[2\] | 寫入登錄之值的格式化文字字串名稱。 |
| \[3\] | 寫入登錄之值的格式化文字字串。      |



 

 

 




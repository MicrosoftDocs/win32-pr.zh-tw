---
description: RemoveRegistryValues 動作只能從已撰寫至登錄資料表或 RemoveRegistry 資料表的系統登錄中移除值。
ms.assetid: aa05eb75-15f2-4e2a-a8e2-a770ad078b41
title: RemoveRegistryValues 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0e6e7473be344faa08ed456e72e3b9c80c4aa8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975140"
---
# <a name="removeregistryvalues-action"></a>RemoveRegistryValues 動作

RemoveRegistryValues 動作只能從已撰寫至登錄 [資料表](registry-table.md) 或 [RemoveRegistry 資料表](removeregistry-table.md)的系統登錄中移除值。 如果相關聯的元件安裝在本機或從來源執行，而且現在已設定為要卸載，此動作會移除已在登錄表中撰寫的登錄值。 如果相關聯的元件設定為在本機安裝或從來源執行，此動作會移除已撰寫至 RemoveRegistry 資料表的登錄值。

## <a name="sequence-restrictions"></a>順序限制

呼叫 RemoveRegistryValues 之前，必須先呼叫 [InstallValidate](installvalidate-action.md) 動作。 如果使用 [WriteRegistryValues](writeregistryvalues-action.md) 動作，它必須在 RemoveRegistryValues 之後。 RemoveRegistryValues 必須位於 [UnregisterMIMEInfo](unregistermimeinfo-action.md) 或 [UnregisterProgIDInfo](unregisterprogidinfo-action.md)之前。

自訂動作可在安裝、卸載或修復交易期間，用來將資料列新增至登錄 [資料表](registry-table.md) 。 這些資料列不會保存在登錄資料表中，而且只有在目前的交易期間，才可使用此資訊。 因此，自訂動作必須在需要這些額外資料列資訊的每個安裝、卸載或修復交易中執行。 自訂動作必須位於動作順序中的 RemoveRegistryValues 和 [WriteRegistryValues](writeregistryvalues-action.md) 動作之前。

## <a name="actiondata-messages"></a>ActionData 訊息



| 欄位 | 動作資料的描述                          |
|-------|-----------------------------------------------------|
| \[1\] | 已移除登錄值之索引鍵的登錄路徑。     |
| \[2\] | 已移除之登錄值名稱的格式化字串。 |



 

## <a name="remarks"></a>備註

若要移除登錄值，請將值記錄在登錄資料表的 [值] 資料行中。 如果 WriteRegistryValues 動作已將 REG \_ 多重 \_ SZ 字串附加至登錄 [表](registry-table.md)中的值，則 RemoveRegistryValues 動作只會從登錄值移除這些字串。

 

 




---
description: CreateShortcuts 動作會管理快速鍵的建立。
ms.assetid: 2e8a30ec-e8e7-4855-addb-2501bf85ab54
title: CreateShortcuts 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 209dbd38d64abb2ddedb267512dd3872991d58071769d25606ed364a15c6d958
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649738"
---
# <a name="createshortcuts-action"></a>CreateShortcuts 動作

CreateShortcuts 動作會管理快速鍵的建立。

## <a name="sequence-restrictions"></a>順序限制

CreateShortcuts 動作必須位於 [InstallFiles](installfiles-action.md) 動作和 [RemoveShortcuts](removeshortcuts-action.md) 動作之後。

## <a name="actiondata-messages"></a>ActionData 訊息



| 欄位 | 動作資料的描述      |
|-------|---------------------------------|
| \[1\] | 已建立快捷方式的識別碼。 |



 

## <a name="remarks"></a>備註

[CreateShortcuts] 動作會建立所選功能元件之主要檔案的快捷方式，以供安裝或廣告之用。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[快速鍵資料表](shortcut-table.md)
</dt> <dt>

[MsiShortcutProperty 資料表](msishortcutproperty-table.md)
</dt> </dl>

 

 




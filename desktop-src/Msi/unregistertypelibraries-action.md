---
description: UnregisterTypeLibraries 動作會從系統中取消註冊類型程式庫。 此動作會套用至在 TypeLib 資料表中所列的每個檔案，該檔案會被觸發為已卸載。
ms.assetid: fea5bdc1-ac27-4d02-bcea-5c97366dd394
title: UnregisterTypeLibraries 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b399f80d940839c5e94028a9c32e706f4826341a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971650"
---
# <a name="unregistertypelibraries-action"></a>UnregisterTypeLibraries 動作

UnregisterTypeLibraries 動作會從系統中取消註冊類型程式庫。 此動作會套用至在 [TypeLib](typelib-table.md) 資料表中所列的每個檔案，該檔案會被觸發為已卸載。

## <a name="sequence-restrictions"></a>順序限制

UnregisterTypeLibraries 動作必須位於 [RemoveFiles](removefiles-action.md) 動作之前。

## <a name="actiondata-messages"></a>ActionData 訊息



| 欄位 | 動作資料的描述                        |
|-------|---------------------------------------------------|
| \[1\] | 未註冊之類型程式庫的[GUID](guid.md) 。 |



 

 

 




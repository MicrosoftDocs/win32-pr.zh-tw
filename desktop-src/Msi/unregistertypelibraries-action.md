---
description: UnregisterTypeLibraries 動作會從系統中取消註冊類型程式庫。 此動作會套用至在 TypeLib 資料表中所列的每個檔案，該檔案會被觸發為已卸載。
ms.assetid: fea5bdc1-ac27-4d02-bcea-5c97366dd394
title: UnregisterTypeLibraries 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6066dbac7e63696f838375261fbb63e8348faf630a7439ec7531cdd71d4ace97
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810118"
---
# <a name="unregistertypelibraries-action"></a>UnregisterTypeLibraries 動作

UnregisterTypeLibraries 動作會從系統中取消註冊類型程式庫。 此動作會套用至在 [TypeLib](typelib-table.md) 資料表中所列的每個檔案，該檔案會被觸發為已卸載。

## <a name="sequence-restrictions"></a>順序限制

UnregisterTypeLibraries 動作必須位於 [RemoveFiles](removefiles-action.md) 動作之前。

## <a name="actiondata-messages"></a>ActionData 訊息



| 欄位 | 動作資料的描述                        |
|-------|---------------------------------------------------|
| \[1\] | 未註冊之類型程式庫的[GUID](guid.md) 。 |



 

 

 




---
description: InstallInitialize 動作和 InstallFinalize 動作會標示變更系統的一連串動作的開頭和結尾。
ms.assetid: c2637070-3fd9-422c-9252-cf15045c6485
title: InstallInitialize 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7031ab79bc099ea067fd8d83cb83d8cefd1f36a1e83f696a1ee3b4487b3cac88
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996568"
---
# <a name="installinitialize-action"></a>InstallInitialize 動作

InstallInitialize 動作和 [InstallFinalize](installfinalize-action.md) 動作會標示變更系統的一連串動作的開頭和結尾。

## <a name="sequence-restrictions"></a>順序限制

InstallInitialize 動作必須在任何變更系統的動作之前排序，例如 [InstallFiles](installfiles-action.md) 動作、 [WriteRegistryValues](writeregistryvalues-action.md) 動作、 [SelfRegModules](selfregmodules-action.md) 動作和 [ProcessComponents](processcomponents-action.md) 動作。 因此，InstallInitialize 動作必須在 [InstallFinalize](installfinalize-action.md) 動作和 [InstallExecute](installexecute-action.md) 動作之前進行排序。

修改 Windows Installer 封裝的[自訂動作](custom-actions.md)（例如，將資料列加入至處理可安裝資源的資料表，例如登錄[資料表或](registry-table.md) [DuplicateFile](duplicatefile-table.md)資料表）必須在 InstallInitialize 動作之前排序。

## <a name="actiondata-messages"></a>ActionData 訊息

沒有任何 ActionData 訊息。

 

 




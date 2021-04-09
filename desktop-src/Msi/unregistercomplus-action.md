---
description: UnregisterComPlus 動作會從登錄中移除 COM + 應用程式。
ms.assetid: bcedc436-a048-487e-9a84-e766da57a0b3
title: UnregisterComPlus 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e32d39255229151757f7d6be0ada871f555f77e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945414"
---
# <a name="unregistercomplus-action"></a>UnregisterComPlus 動作

UnregisterComPlus 動作會從登錄中移除 COM + 應用程式。

## <a name="sequence-restrictions"></a>順序限制

[RegisterComPlus 動作](registercomplus-action.md)必須遵循[InstallFiles 動作](installfiles-action.md)和 UnregisterComPlus 動作。

## <a name="actiondata-messages"></a>ActionData 訊息



| 欄位 | 動作資料的描述                                    |
|-------|---------------------------------------------------------------|
| \[1\] | 要移除之 COM + 應用程式的應用程式識別碼。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[RegisterComPlus 動作](registercomplus-action.md)
</dt> <dt>

[Complus 資料表](complus-table.md)
</dt> <dt>

[安裝具有 Windows Installer 的 COM + 應用程式](installing-a-com--application-with-the-windows-installer.md)
</dt> </dl>

 

 




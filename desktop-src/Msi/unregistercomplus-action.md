---
description: UnregisterComPlus 動作會從登錄中移除 COM + 應用程式。
ms.assetid: bcedc436-a048-487e-9a84-e766da57a0b3
title: UnregisterComPlus 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc3ed5e8e4afd853294e7f5832662e9aaf1eb122d3573e7c384115c86d994588
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119499848"
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

[安裝具有 Windows Installer 的 com + 應用程式](installing-a-com--application-with-the-windows-installer.md)
</dt> </dl>

 

 




---
description: RegisterComPlus 動作會註冊 COM + 應用程式。
ms.assetid: e42bb993-7079-4d5b-bb2e-c958e99e705e
title: RegisterComPlus 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 046d1f40293888d3a1be48a3c55fd5082b6073828c8d5cc7d34c464556986d4f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082638"
---
# <a name="registercomplus-action"></a>RegisterComPlus 動作

RegisterComPlus 動作會註冊 COM + 應用程式。

## <a name="sequence-restrictions"></a>順序限制

RegisterComPlus 動作必須遵循 [InstallFiles 動作](installfiles-action.md) 和 [UnregisterComPlus 動作](unregistercomplus-action.md)。

## <a name="actiondata-messages"></a>ActionData 訊息



| 欄位 | 動作資料的描述              |
|-------|-----------------------------------------|
| \[1\] | COM + 應用程式的應用程式識別碼。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Complus 資料表](complus-table.md)
</dt> <dt>

[UnregisterComPlus 動作](unregistercomplus-action.md)
</dt> <dt>

[安裝具有 Windows Installer 的 com + 應用程式](installing-a-com--application-with-the-windows-installer.md)
</dt> </dl>

 

 




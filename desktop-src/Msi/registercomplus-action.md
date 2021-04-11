---
description: RegisterComPlus 動作會註冊 COM + 應用程式。
ms.assetid: e42bb993-7079-4d5b-bb2e-c958e99e705e
title: RegisterComPlus 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb824d67e776a99f8cd05c56f73f171f436c71d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115501"
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

[安裝具有 Windows Installer 的 COM + 應用程式](installing-a-com--application-with-the-windows-installer.md)
</dt> </dl>

 

 




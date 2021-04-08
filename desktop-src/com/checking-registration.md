---
title: 正在檢查註冊
description: 正在檢查註冊
ms.assetid: 7df63955-d838-4518-8473-0c1a24e90f69
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee215fd052ffc242900eead069a8b72fd25b31d5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932029"
---
# <a name="checking-registration"></a>正在檢查註冊

每次載入應用程式時，它應該會檢查其註冊以判斷下列各項：

-   Clsid 是否存在於登錄中。 如果不存在，應用程式應該註冊為原始設定。
-   應用程式的 Clsid 是否存在於登錄中，但其中沒有 OLE 2 相關的資訊。 如果是這種情況，應用程式應該註冊為原始設定。
-    ([LocalServer](localserver.md) 和 [LocalServer32](localserver32.md)、 [InprocServer](inprocserver.md) 和 [InprocServer32](inprocserver32.md)，以及 [DefaultIcon](defaulticon.md)) 包含伺服器專案的路徑，會指向目前安裝應用程式的位置。 如果路徑不存在，請重寫路徑專案以指向目前的位置。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[註冊 COM 應用程式](registering-com-applications.md)
</dt> </dl>

 

 





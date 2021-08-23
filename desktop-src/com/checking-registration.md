---
title: 正在檢查註冊
description: 正在檢查註冊
ms.assetid: 7df63955-d838-4518-8473-0c1a24e90f69
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd7d7f03f1d76b780b49bec5d744a02beca9a3dc45417bf8c6efddd8ff5a9e9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119501648"
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

 

 





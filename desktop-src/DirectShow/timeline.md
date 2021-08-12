---
description: 時間表
ms.assetid: 6cc36034-224c-4126-873b-0cfeceec9781
title: 時間表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d85809aed689d63ccdfc0b1dee1b5b792cafc9d7d0267d27e33bd7b6c1bea6cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118651250"
---
# <a name="timeline"></a>時間表

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

時間軸物件會管理影片編輯專案中的所有物件。 若要建立這個物件，請呼叫 **CoCreateInstance**。 類別識別碼是 CLSID \_ AMTimeline。

若要讀取 Windows 媒體™檔，應用程式必須提供軟體憑證，也稱為金鑰。 透過時間軸的 **IObjectWithSite** 介面，將應用程式註冊為金鑰提供者。 如需詳細資訊，請參閱[解除鎖定 Windows 媒體格式 SDK](unlocking-the-windows-media-format-sdk.md)。

時間軸物件會公開下列介面：

-   [**IAMSetErrorLog**](iamseterrorlog.md)
-   [**IAMTimeline**](iamtimeline.md)
-   **IObjectWithSite**
-   **IPersistStream**

## <a name="related-topics"></a>相關主題

<dl> <dt>

[時間軸模型](the-timeline-model.md)
</dt> <dt>

[建立時間軸](constructing-a-timeline.md)
</dt> </dl>

 

 




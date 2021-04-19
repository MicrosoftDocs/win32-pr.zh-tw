---
description: 時間表
ms.assetid: 6cc36034-224c-4126-873b-0cfeceec9781
title: 時間表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10d1f802f12df6ca3469b8283bd4fe8b27e22412
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985502"
---
# <a name="timeline"></a>時間表

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

時間軸物件會管理影片編輯專案中的所有物件。 若要建立這個物件，請呼叫 **CoCreateInstance**。 類別識別碼是 CLSID \_ AMTimeline。

若要讀取 Windows Media™檔案，應用程式必須提供軟體憑證，也稱為金鑰。 透過時間軸的 **IObjectWithSite** 介面，將應用程式註冊為金鑰提供者。 如需詳細資訊，請參閱 [解除鎖定 Windows Media FORMAT SDK](unlocking-the-windows-media-format-sdk.md)。

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

 

 




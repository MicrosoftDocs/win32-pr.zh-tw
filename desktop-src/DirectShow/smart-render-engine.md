---
description: 智慧型轉譯引擎
ms.assetid: 279be879-9728-4fa1-bdf7-6b48485fc75f
title: 智慧型轉譯引擎
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3472d096d1c3918a9bf1a45ae788a535fd65bfe4e4084c6b044516db01440d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072552"
---
# <a name="smart-render-engine"></a>智慧型轉譯引擎

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

智慧型轉譯引擎物件會從時間軸轉譯壓縮的輸出。 若要建立這個物件，請呼叫 **CoCreateInstance**。 針對未壓縮的輸出，請使用基本轉譯引擎。 類別識別碼是 CLSID \_ SmartRenderEngine。

智慧型轉譯引擎會公開下列介面：

-   [**IAMSetErrorLog**](iamseterrorlog.md)
-   **IObjectWithSite**
-   [**IRenderEngine**](irenderengine.md)
-   [**IRenderEngine2**](irenderengine2.md)
-   [**ISmartRenderEngine**](ismartrenderengine.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[轉譯 Project](rendering-a-project.md)
</dt> <dt>

[基本轉譯引擎](basic-render-engine.md)
</dt> </dl>

 

 




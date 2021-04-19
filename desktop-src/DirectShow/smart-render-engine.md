---
description: 智慧型轉譯引擎
ms.assetid: 279be879-9728-4fa1-bdf7-6b48485fc75f
title: 智慧型轉譯引擎
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fa727397f21aeba754cfe41f2dc4f9c1da1c91b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106972933"
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

[轉譯專案](rendering-a-project.md)
</dt> <dt>

[基本轉譯引擎](basic-render-engine.md)
</dt> </dl>

 

 




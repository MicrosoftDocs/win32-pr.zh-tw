---
description: 基本轉譯引擎
ms.assetid: 0a4fcf2a-dbad-4211-9a85-7741c8dfc95e
title: 基本轉譯引擎
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb9b51240b43c58de99b7d6fe1f7ad61f754c7ed
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510216"
---
# <a name="basic-render-engine"></a>基本轉譯引擎

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

基本轉譯引擎物件會從時間軸轉譯未壓縮的輸出。 若要建立這個物件，請呼叫 **CoCreateInstance**。 針對壓縮的輸出，請使用智慧型轉譯引擎。 類別識別碼是 CLSID \_ RenderEngine。

基本轉譯引擎會公開下列介面：

-   [**IAMSetErrorLog**](iamseterrorlog.md)
-   IObjectWithSite
-   [**IRenderEngine**](irenderengine.md)
-   [**IRenderEngine2**](irenderengine2.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[轉譯專案](rendering-a-project.md)
</dt> <dt>

[智慧型轉譯引擎](smart-render-engine.md)
</dt> </dl>

 

 




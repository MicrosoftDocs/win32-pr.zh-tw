---
title: 系結控制碼的類型
description: 系結控制碼可以是自動、隱含或明確。
ms.assetid: 7f026199-6045-4f60-9002-543636cf6275
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1a3db77f01bf0228623efe9d3dca5fbeb023d97fbe00e5da4d4ba070f323ba5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011069"
---
# <a name="types-of-binding-handles"></a>系結控制碼的類型

系結控制碼可以是自動、隱含或明確。 它們在應用程式對系結程式上的控制程度不同。 顧名思義，自動系結會處理自動化系結。 用戶端和伺服器應用程式不需要程式碼來處理系結程式。 隱含系結控制碼可讓用戶端程式在系結髮生之前設定系結控制碼。 在用戶端建立系結之後，RPC 執行時間程式庫會處理其餘部分。 明確系結控制碼可將系結程式的完整控制權移至用戶端和伺服器程式的原始程式碼中。 使用此控制項會增加複雜度。 您的應用程式必須呼叫 RPC 函數來管理系結。 它不會自動發生。 建議使用明確的系結控制碼。

下圖說明自動、隱含和明確系結控制碼之間的差異。

![自動、隱含和明確系結控制碼之間的差異](images/bhand.png)

此外，每個系結控制碼都是基本或自訂的。 下列主題將討論每種類型的系結控制碼：

-   [自動系結控制碼](automatic-binding-handles.md)
-   [隱含系結控制碼](implicit-binding-handles.md)
-   [明確的系結控制碼](explicit-binding-handles.md)
-   [基本和自訂系結控制碼](primitive-and-custom-binding-handles.md)

 

 





---
title: 系結控制碼的類型
description: 系結控制碼可以是自動、隱含或明確。
ms.assetid: 7f026199-6045-4f60-9002-543636cf6275
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60a09b858dfc677d06cf5885dc7a5f7a6ba599eb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021810"
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

 

 





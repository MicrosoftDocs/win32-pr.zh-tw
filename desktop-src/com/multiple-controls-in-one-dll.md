---
title: 一個 DLL 中的多個控制項
description: 一個 DLL 中的多個控制項
ms.assetid: 76c1c0ef-af24-43e8-b3a7-337841c338ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b571f307f3438ca8f8ce0a0a716af2042884520cd07746f8e6fa8c1739fae22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130060"
---
# <a name="multiple-controls-in-one-dll"></a>一個 DLL 中的多個控制項

單一 .ocx DLL 可以容器任意數量的 ActiveX 控制項，進而簡化一組相關控制項的散發和使用。

如果您在單一 DLL 中傳送多個控制項，請務必在封裝的每個控制項名稱中包含廠商名稱。 在每個控制項名稱中包含廠商的名稱，可讓使用者輕鬆地識別封裝內的控制項。 例如，如果您送出的 DLL 會執行三個控制項，Con1、Con2 和 Con3，則控制項名稱應該是：

-   *您的公司名稱* Con1 控制項

-   *您的公司名稱* Con2 控制項

-   *您的公司名稱* Con3 控制項

 

 





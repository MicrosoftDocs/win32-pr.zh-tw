---
description: 網路監視器或剖析器 DLL 可以格式化網路監視器 UI 的詳細資料窗格中所顯示的資料。
ms.assetid: 60ab9253-ec0f-4c97-a475-ce2a74d469c4
title: 設定已顯示之資料的格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d843214804e50d6baa7bd60f49da170dbe561029e0643c5a57c8677da3735936
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117982464"
---
# <a name="formatting-displayed-data"></a>設定已顯示之資料的格式

網路監視器或剖析器 DLL 可以格式化網路監視器 UI 的詳細資料窗格中所顯示的資料。

網路監視器提供一般格式器，提供顯示存在於通訊協定內的大部分資料類型所需的基本服務。 不過，一般格式子不支援所有資料類型。 例如，一般格式器不支援下列各項：

-   數種地址類型。
-   來源和目的易記名稱。
-   物件識別碼。
-   大型整數資料類型。
-   可變長度的小整數資料類型。

下列範例會識別許可權識別碼屬性的兩個格式化字串。

-   第一行程式碼會顯示一般格式器的輸出。 輸出是以資料類型為基礎。
-   第二行程式碼會顯示自訂格式器的輸出，以及屬性資料的字串。

``` syntax
Privilege ID (PID) = 0x0029
Privilege ID   (PID) = 0x0029   The Process has privileges
```

> [!Note]  
> 可能的話，請使用一般格式器來顯示您的資料，因為它可讓您控制剖析器 DLL 的大小，並為剖析器 DLL 提供更佳的跨平臺功能。

 

 

 




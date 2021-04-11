---
description: TAPI 1.4 將數個 Api、訊息、常數和結構元素新增至1.3 規格。
ms.assetid: 293f732f-0288-46d1-b542-d948c6179158
title: TAPI 1。4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c32f4320043ada2e2ae5477a698bde63f28d2f25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944205"
---
# <a name="tapi-14"></a>TAPI 1。4

TAPI 1.4 將數個 Api、訊息、常數和結構元素新增至1.3 規格。 TAPI 1.4 僅支援16位的 Tsp。 但是，它允許開發32位應用程式，而不需要擔心16位 Windows 的限制。

TAPI 和 TSPI 標頭檔用來同時針對 TAPI 1.4 和 TAPI 2.x 開發應用程式。 雖然這兩個規格之間的結構沒有許多變更，但對 API 的變更 (特別是 Unicode 支援) ，因此請務必注意，標頭會以不同的方式編譯，視 TAPI \_ 目前版本的常數而定 \_ 。 例如：

``` syntax
#define TAPI_CURRENT_VERSION 0x00010004
#include <tapi.h>
```

> [!Note]  
> \_ \_ 應針對所有 tapi 應用程式定義 tapi 目前的版本。 雖然 TAPI 2.x 開發並非絕對必要，但未來可能需要進行變更。

 

 

 




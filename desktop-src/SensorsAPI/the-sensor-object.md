---
description: 感應器物件代表特定的感應器。
ms.assetid: b969a153-d957-4323-bafe-6f8d62b0a627
title: 感應器物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6034c008edf75b16a8156ab53ff66a418261d965
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997165"
---
# <a name="the-sensor-object"></a>感應器物件

感應器物件代表特定的感應器。

感應器 API 會將每個感應器表示為感應器物件。 您可以透過其 [**ISensor**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) 介面使用特定的感應器物件。 這個介面可讓您：

-   取得感應器的相關中繼資料，例如其識別碼、類型或易記名稱。
-   取得感應器可提供之特定資料的相關資訊。
-   以同步方式取得資料。
-   取得狀態資訊，例如感應器是否就緒。
-   指定程式將接收的事件。
-   指定可供感應器 API 用來為您的程式提供事件通知的回呼介面。

 

 




---
description: 使用下列程式碼設定回呼頻率。
ms.assetid: fdcad3c2-7e36-4194-83c7-dccbd50762d5
title: 設定回呼頻率
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4f235377865583e48d6a4b9c16abce4209e6449f74ed3cf42688dfa417287bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118363244"
---
# <a name="setting-the-callback-frequency"></a>設定回呼頻率

使用下列程式碼設定回呼頻率：

**DWORD** 值 = 1;


```C++
rc = SetDwordInBlob(hNPPBlob, OWNER_NPP, CATEGORY_CONFIG,
                    TAG_UPDATE_FREQUENCY, Value);
```



此程式碼片段會將回呼頻率設定為1秒， (最小值) 。 最大值必須大於1。 如果網路封包提供者 (NPP) 緩衝區已滿，則 NPP 會儘快呼叫監視器。

 

 




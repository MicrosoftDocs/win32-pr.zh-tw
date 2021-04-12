---
description: 使用下列程式碼設定回呼頻率。
ms.assetid: fdcad3c2-7e36-4194-83c7-dccbd50762d5
title: 設定回呼頻率
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e03c260b6d289e473f27bb3ae6b84a3f42d0878
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318523"
---
# <a name="setting-the-callback-frequency"></a>設定回呼頻率

使用下列程式碼設定回呼頻率：

**DWORD** 值 = 1;


```C++
rc = SetDwordInBlob(hNPPBlob, OWNER_NPP, CATEGORY_CONFIG,
                    TAG_UPDATE_FREQUENCY, Value);
```



此程式碼片段會將回呼頻率設定為1秒， (最小值) 。 最大值必須大於1。 如果網路封包提供者 (NPP) 緩衝區已滿，則 NPP 會儘快呼叫監視器。

 

 




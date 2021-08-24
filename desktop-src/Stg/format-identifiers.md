---
title: 格式識別碼
description: 屬性集值會儲存在以唯一 FMTID 標記的區段中。
ms.assetid: 3ffb6c5e-72ce-4769-847a-72db6f145d61
keywords:
- 格式識別碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72ec9e9843b1dfe843e89ebf85eadbbcb5da8cb58dfc1b289eb88c844aae7456
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663148"
---
# <a name="format-identifiers"></a>格式識別碼

屬性集值會儲存在以唯一 FMTID 標記的區段中。 例如，COM 摘要資訊屬性集的 FMTID 為 **F29F85E0-4FF9-1068-AB91-08002B27B3D9**。

若要定義摘要資訊屬性集的 FMTID，請在操作屬性集的程式碼中，使用 include 檔中的 **定義 \_ GUID** 宏。


```C++
DEFINE_GUID(FMTID_SummaryInformation, 0xF29F85E0, 0x4FF9, 0x1068, 
0xAB, 0x91, 0x08, 0x00, 0x2B, 0x27, 0xB3, 0xD9);
```



任何需要摘要資訊屬性集之 FMTID 的程式碼，都可以透過 *FMTID \_ SummaryInformation* 變數來存取它。

將屬性集儲存在 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) 實例中時，請將 FMTID 轉換成儲存物件的字串名稱。

 

 





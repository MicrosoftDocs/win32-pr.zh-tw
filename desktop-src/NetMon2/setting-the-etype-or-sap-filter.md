---
description: 設定「捕獲篩選器」的 Etype 或 SAP 部分是「建立」篩選程式的第一個步驟。
ms.assetid: 0a22f74b-5bb1-43df-a70a-9f30195177ea
title: 設定 Etype 或 SAP 篩選器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abac637594debf03ca9f82c79382ababc4c696d79d5351b2d0be0a3e5b4ffa8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118363163"
---
# <a name="setting-the-etype-or-sap-filter"></a>設定 Etype 或 SAP 篩選器

設定「捕獲篩選器」的 Etype 或 SAP 部分是「建立」篩選程式的第一個步驟。

在下列範例中，capture 篩選器設定為只取出 IPX 流量：


```C++
BYTE Sap[]   = { 0x10, 0xE0 };
WORD Etype[] = { 0x8137 }; 

rc = SetNPPEtypeSapFilter(m_hBlob, 
     2,      //  nSaps,
     1,      //  nEtypes,
     &Sap,   //  LPBYTE lpSapTable,
     &Etype, //  LPWORD lpEtypeTable,
     0,      //  DWORD  FilterFlags,
     NULL
);
```



SAP 和 Etype 值通常會在 Rfc 中提供。 SAP 和 Etype 值都可以位於陣列中。

 

 




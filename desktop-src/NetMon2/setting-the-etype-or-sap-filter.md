---
description: 設定「捕獲篩選器」的 Etype 或 SAP 部分是「建立」篩選程式的第一個步驟。
ms.assetid: 0a22f74b-5bb1-43df-a70a-9f30195177ea
title: 設定 Etype 或 SAP 篩選器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aee117e992968265be5a973f3f4017832ee6ca0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943508"
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

 

 




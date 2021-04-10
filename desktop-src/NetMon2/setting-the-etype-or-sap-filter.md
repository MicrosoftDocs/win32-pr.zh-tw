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
# <a name="setting-the-etype-or-sap-filter"></a><span data-ttu-id="064eb-103">設定 Etype 或 SAP 篩選器</span><span class="sxs-lookup"><span data-stu-id="064eb-103">Setting the Etype or SAP Filter</span></span>

<span data-ttu-id="064eb-104">設定「捕獲篩選器」的 Etype 或 SAP 部分是「建立」篩選程式的第一個步驟。</span><span class="sxs-lookup"><span data-stu-id="064eb-104">Setting the Etype or SAP portion of the capture filter is the first step in the capture filter creation process.</span></span>

<span data-ttu-id="064eb-105">在下列範例中，capture 篩選器設定為只取出 IPX 流量：</span><span class="sxs-lookup"><span data-stu-id="064eb-105">In the following example, the capture filter is set to only retrieve IPX traffic:</span></span>


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



<span data-ttu-id="064eb-106">SAP 和 Etype 值通常會在 Rfc 中提供。</span><span class="sxs-lookup"><span data-stu-id="064eb-106">SAP and Etype values are usually available in RFCs.</span></span> <span data-ttu-id="064eb-107">SAP 和 Etype 值都可以位於陣列中。</span><span class="sxs-lookup"><span data-stu-id="064eb-107">Both SAP and Etype values can be in an array.</span></span>

 

 




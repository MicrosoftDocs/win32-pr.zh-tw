---
title: 格式識別碼
description: 屬性集值會儲存在以唯一 FMTID 標記的區段中。
ms.assetid: 3ffb6c5e-72ce-4769-847a-72db6f145d61
keywords:
- 格式識別碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0202cd1287c3b4fef6e9e2b56e272541a03425b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300651"
---
# <a name="format-identifiers"></a><span data-ttu-id="2ba09-104">格式識別碼</span><span class="sxs-lookup"><span data-stu-id="2ba09-104">Format Identifiers</span></span>

<span data-ttu-id="2ba09-105">屬性集值會儲存在以唯一 FMTID 標記的區段中。</span><span class="sxs-lookup"><span data-stu-id="2ba09-105">Property set values are stored in a section tagged with a unique FMTID.</span></span> <span data-ttu-id="2ba09-106">例如，COM 摘要資訊屬性集的 FMTID 為 **F29F85E0-4FF9-1068-AB91-08002B27B3D9**。</span><span class="sxs-lookup"><span data-stu-id="2ba09-106">For example, the FMTID for the COM Summary Information property set is **F29F85E0-4FF9-1068-AB91-08002B27B3D9**.</span></span>

<span data-ttu-id="2ba09-107">若要定義摘要資訊屬性集的 FMTID，請在操作屬性集的程式碼中，使用 include 檔中的 **定義 \_ GUID** 宏。</span><span class="sxs-lookup"><span data-stu-id="2ba09-107">To define a FMTID for the Summary Information property set, use the **DEFINE\_GUID** macro in an include file for the code that manipulates the property set.</span></span>


```C++
DEFINE_GUID(FMTID_SummaryInformation, 0xF29F85E0, 0x4FF9, 0x1068, 
0xAB, 0x91, 0x08, 0x00, 0x2B, 0x27, 0xB3, 0xD9);
```



<span data-ttu-id="2ba09-108">任何需要摘要資訊屬性集之 FMTID 的程式碼，都可以透過 *FMTID \_ SummaryInformation* 變數來存取它。</span><span class="sxs-lookup"><span data-stu-id="2ba09-108">Any code that requires the FMTID for the Summary Information property set, can access it through the *FMTID\_SummaryInformation* variable.</span></span>

<span data-ttu-id="2ba09-109">將屬性集儲存在 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) 實例中時，請將 FMTID 轉換成儲存物件的字串名稱。</span><span class="sxs-lookup"><span data-stu-id="2ba09-109">When storing property sets in [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) instances, convert the FMTID to a string name for the storage object.</span></span>

 

 





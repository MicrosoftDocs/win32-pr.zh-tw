---
title: 建立變數系結清單
description: SnmpCreateVbl 函式會建立新的變數系結清單。
ms.assetid: 18e8a04d-612f-4d85-9cff-8c541a4cdf71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34e9ef7aa208e2e2f887d14c0e124f3bb659ff8f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183629"
---
# <a name="creating-a-variable-binding-list"></a><span data-ttu-id="f3ab5-103">建立變數系結清單</span><span class="sxs-lookup"><span data-stu-id="f3ab5-103">Creating a Variable Binding List</span></span>

<span data-ttu-id="f3ab5-104">[**SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl)函式會建立新的變數系結清單。</span><span class="sxs-lookup"><span data-stu-id="f3ab5-104">The [**SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) function creates a new variable binding list.</span></span> <span data-ttu-id="f3ab5-105">如果 WinSNMP 應用程式指定變數名稱和值，此函式會建立清單，並新增名稱和值做為清單中的第一個專案。</span><span class="sxs-lookup"><span data-stu-id="f3ab5-105">If the WinSNMP application specifies a variable name and a value, the function creates the list and adds the name and value as the first entry in the list.</span></span> <span data-ttu-id="f3ab5-106">如果應用程式為變數名稱指定 **Null** ，則函式會建立空的清單。</span><span class="sxs-lookup"><span data-stu-id="f3ab5-106">If the application specifies **NULL** for the variable name, the function creates an empty list.</span></span>

<span data-ttu-id="f3ab5-107">若要複製變數系結清單，請呼叫 [**SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) 函數。</span><span class="sxs-lookup"><span data-stu-id="f3ab5-107">To copy a variable binding list, call the [**SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) function.</span></span> <span data-ttu-id="f3ab5-108">此函式會建立新的變數系結清單，並使用來源變數系結清單中的資料複本來初始化新的清單。</span><span class="sxs-lookup"><span data-stu-id="f3ab5-108">The function creates a new variable binding list and initializes the new list with a copy of the data in the source variable binding list.</span></span>

<span data-ttu-id="f3ab5-109">[**SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl)函式和 [**SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl)函式會為新的變數系結清單配置任何必要的記憶體。</span><span class="sxs-lookup"><span data-stu-id="f3ab5-109">The [**SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) function and the [**SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) function allocate any necessary memory for the new variable binding list.</span></span> <span data-ttu-id="f3ab5-110">WinSNMP 應用程式必須釋放與這些清單相關聯的資源。</span><span class="sxs-lookup"><span data-stu-id="f3ab5-110">The WinSNMP application must release the resources associated with these lists.</span></span> <span data-ttu-id="f3ab5-111">建議應用程式藉由比對 [**SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) 和 [**SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) 的每個呼叫，並在適當的情況下使用 [**SnmpFreeVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl) 函式來釋放已配置的記憶體，以進行這項作業。</span><span class="sxs-lookup"><span data-stu-id="f3ab5-111">It is recommended that the application do this by matching each call to [**SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) and [**SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) with a corresponding call to the [**SnmpFreeVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl) function when it is appropriate to free the allocated memory.</span></span>

 

 





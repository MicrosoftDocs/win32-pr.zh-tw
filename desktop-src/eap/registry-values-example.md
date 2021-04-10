---
title: 登錄值範例
description: 下列範例顯示某些驗證通訊協定登錄值的可能資料。
ms.assetid: 07772af0-db56-4cc6-ad72-cf79d3813883
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bcbc3d4ca10a3e9298177a5eea240d0d34ade04
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/26/2019
ms.locfileid: "104022886"
---
# <a name="registry-values-example"></a><span data-ttu-id="c436f-103">登錄值範例</span><span class="sxs-lookup"><span data-stu-id="c436f-103">Registry Values Example</span></span>

<span data-ttu-id="c436f-104">下列範例顯示某些驗證通訊協定登錄值的可能資料。</span><span class="sxs-lookup"><span data-stu-id="c436f-104">The following example shows possible data for some of the authentication protocol registry values.</span></span>

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            Rasman
               PPP
                  EAP
                     40
                        Path
                        FriendlyName
                        ConfigUIPath
                        IdentityPath
                        InteractiveUIPath
                        RequireConfigUI
                        ConfigCLSID
                        StandaloneSupported
```



| <span data-ttu-id="c436f-105">金鑰名稱</span><span class="sxs-lookup"><span data-stu-id="c436f-105">Key Name</span></span>            | <span data-ttu-id="c436f-106">Datatype</span><span class="sxs-lookup"><span data-stu-id="c436f-106">Datatype</span></span>        | <span data-ttu-id="c436f-107">值</span><span class="sxs-lookup"><span data-stu-id="c436f-107">Value</span></span>                                  |
|---------------------|-----------------|----------------------------------------|
| <span data-ttu-id="c436f-108">路徑</span><span class="sxs-lookup"><span data-stu-id="c436f-108">Path</span></span>                | <span data-ttu-id="c436f-109">REG \_ EXPAND \_ SZ</span><span class="sxs-lookup"><span data-stu-id="c436f-109">REG\_EXPAND\_SZ</span></span> | <span data-ttu-id="c436f-110">% SystemRoot% \\ system32 \\sample.dll</span><span class="sxs-lookup"><span data-stu-id="c436f-110">%SystemRoot%\\system32\\sample.dll</span></span>     |
| <span data-ttu-id="c436f-111">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="c436f-111">FriendlyName</span></span>        | <span data-ttu-id="c436f-112">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="c436f-112">REG\_SZ</span></span>         | <span data-ttu-id="c436f-113">EAP 通訊協定範例</span><span class="sxs-lookup"><span data-stu-id="c436f-113">Sample EAP Protocol</span></span>                    |
| <span data-ttu-id="c436f-114">ConfigUIPath</span><span class="sxs-lookup"><span data-stu-id="c436f-114">ConfigUIPath</span></span>        | <span data-ttu-id="c436f-115">REG \_ EXPAND \_ SZ</span><span class="sxs-lookup"><span data-stu-id="c436f-115">REG\_EXPAND\_SZ</span></span> | <span data-ttu-id="c436f-116">% SystemRoot% \\ system32 \\sample.dll</span><span class="sxs-lookup"><span data-stu-id="c436f-116">%SystemRoot%\\system32\\sample.dll</span></span>     |
| <span data-ttu-id="c436f-117">IdentityPath</span><span class="sxs-lookup"><span data-stu-id="c436f-117">IdentityPath</span></span>        | <span data-ttu-id="c436f-118">REG \_ EXPAND \_ SZ</span><span class="sxs-lookup"><span data-stu-id="c436f-118">REG\_EXPAND\_SZ</span></span> | <span data-ttu-id="c436f-119">% SystemRoot% \\ system32 \\sample.dll</span><span class="sxs-lookup"><span data-stu-id="c436f-119">%SystemRoot%\\system32\\sample.dll</span></span>     |
| <span data-ttu-id="c436f-120">InteractiveUIPath</span><span class="sxs-lookup"><span data-stu-id="c436f-120">InteractiveUIPath</span></span>   | <span data-ttu-id="c436f-121">REG \_ EXPAND \_ SZ</span><span class="sxs-lookup"><span data-stu-id="c436f-121">REG\_EXPAND\_SZ</span></span> | <span data-ttu-id="c436f-122">% SystemRoot% \\ system32 \\sample.dll</span><span class="sxs-lookup"><span data-stu-id="c436f-122">%SystemRoot%\\system32\\sample.dll</span></span>     |
| <span data-ttu-id="c436f-123">RequireConfigUI</span><span class="sxs-lookup"><span data-stu-id="c436f-123">RequireConfigUI</span></span>     | <span data-ttu-id="c436f-124">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="c436f-124">REG\_DWORD</span></span>      | <span data-ttu-id="c436f-125">1</span><span class="sxs-lookup"><span data-stu-id="c436f-125">1</span></span>                                      |
| <span data-ttu-id="c436f-126">ConfigCLSID</span><span class="sxs-lookup"><span data-stu-id="c436f-126">ConfigCLSID</span></span>         | <span data-ttu-id="c436f-127">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="c436f-127">REG\_SZ</span></span>         | <span data-ttu-id="c436f-128">{0000031A-0000-0000-C000-000000000046}</span><span class="sxs-lookup"><span data-stu-id="c436f-128">{0000031A-0000-0000-C000-000000000046}</span></span> |
| <span data-ttu-id="c436f-129">StandaloneSupported</span><span class="sxs-lookup"><span data-stu-id="c436f-129">StandaloneSupported</span></span> | <span data-ttu-id="c436f-130">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="c436f-130">REG\_DWORD</span></span>      | <span data-ttu-id="c436f-131">1</span><span class="sxs-lookup"><span data-stu-id="c436f-131">1</span></span>                                      |



 

 

 





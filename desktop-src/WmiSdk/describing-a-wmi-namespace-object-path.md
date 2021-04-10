---
description: 命名空間物件路徑描述伺服器上特定命名空間的位置。 命名空間物件路徑包含伺服器和命名空間元素，並使用正向或反斜線來格式化。
ms.assetid: 6d8da19e-0914-4267-870e-c203176b895e
ms.tgt_platform: multiple
title: 描述 WMI 命名空間物件路徑
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586104a1c193f1c229b0fbb27437d22e3686585b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026546"
---
# <a name="describing-a-wmi-namespace-object-path"></a><span data-ttu-id="1e2cf-104">描述 WMI 命名空間物件路徑</span><span class="sxs-lookup"><span data-stu-id="1e2cf-104">Describing a WMI Namespace Object Path</span></span>

<span data-ttu-id="1e2cf-105">命名空間物件路徑描述伺服器上特定命名空間的位置。</span><span class="sxs-lookup"><span data-stu-id="1e2cf-105">A namespace object path describes the location of a particular namespace on a server.</span></span> <span data-ttu-id="1e2cf-106">命名空間物件路徑包含伺服器和命名空間元素，並使用正向或反斜線來格式化。</span><span class="sxs-lookup"><span data-stu-id="1e2cf-106">A namespace object path contains server and namespace elements, and is formatted using either forward or backward slashes.</span></span>

<span data-ttu-id="1e2cf-107">Server 元素會指定裝載命名空間之電腦的網路名稱，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="1e2cf-107">The server element specifies the network name of the computer that is hosting the namespace, as shown in the following example.</span></span>

``` syntax
\\Server\Namespace
```

<span data-ttu-id="1e2cf-108">\- 或 -</span><span class="sxs-lookup"><span data-stu-id="1e2cf-108">\- or -</span></span>

``` syntax
//Server/Namespace
```

<span data-ttu-id="1e2cf-109">如果伺服器是本機電腦，請使用單一點而不是伺服器名稱，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="1e2cf-109">If the server is the local computer, use a single dot instead of the server name, as shown in the following example.</span></span>

``` syntax
\\.\Namespace
```

<span data-ttu-id="1e2cf-110">Namespace 元素會指定任何有效的命名空間。</span><span class="sxs-lookup"><span data-stu-id="1e2cf-110">The namespace element specifies any valid namespace.</span></span> <span data-ttu-id="1e2cf-111">命名空間會以階層式字串表示，其中包含以單一反斜線分隔的元素，例如根 \\ cimv2。</span><span class="sxs-lookup"><span data-stu-id="1e2cf-111">A namespace is represented with a hierarchical string containing elements delimited by single backslashes, such as root\\cimv2.</span></span> <span data-ttu-id="1e2cf-112">您無法在命名空間名稱內使用正斜線。</span><span class="sxs-lookup"><span data-stu-id="1e2cf-112">You cannot use forward slashes within namespace names.</span></span>

 

 




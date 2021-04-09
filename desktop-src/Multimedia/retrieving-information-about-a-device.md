---
title: 正在抓取裝置的相關資訊
description: 正在抓取裝置的相關資訊
ms.assetid: d038d3fb-43d0-4d9d-836c-205f6d8c98e3
keywords:
- MCI_GETDEVCAPS 命令
- MCI_STATUS 命令
- MCI_INFO 命令
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10acb53fa1a961fe7a70042350f8d889d9fdf572
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932536"
---
# <a name="retrieving-information-about-a-device"></a><span data-ttu-id="989ff-106">正在抓取裝置的相關資訊</span><span class="sxs-lookup"><span data-stu-id="989ff-106">Retrieving Information About a Device</span></span>

<span data-ttu-id="989ff-107">每部裝置都會回應 ([**mci \_ GETDEVCAPS**](mci-getdevcaps.md)) 、 [**status**](status.md) ([**Mci \_ status**](mci-status.md)) 和 [**info**](info.md) ([**mci \_ info**](mci-info.md)) 命令的 [**功能**](capability.md)。</span><span class="sxs-lookup"><span data-stu-id="989ff-107">Every device responds to the [**capability**](capability.md) ([**MCI\_GETDEVCAPS**](mci-getdevcaps.md)), [**status**](status.md) ([**MCI\_STATUS**](mci-status.md)), and [**info**](info.md) ([**MCI\_INFO**](mci-info.md)) commands.</span></span> <span data-ttu-id="989ff-108">這些命令會取得裝置的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="989ff-108">These commands obtain information about the device.</span></span> <span data-ttu-id="989ff-109">例如，如果 **cdaudio** 裝置可以退出光碟，則下列命令會傳回 "true"：</span><span class="sxs-lookup"><span data-stu-id="989ff-109">For example, the following command returns "true" if a **cdaudio** device can eject the disc:</span></span>


```C++
mciSendString(
    "capability cdaudio can eject", 
    lpszReturnString, lstrlen(lpszReturnString), NULL);
```



<span data-ttu-id="989ff-110">針對 [必要] 和 [基本] 命令列出的旗標，可提供裝置最少的資訊數量。</span><span class="sxs-lookup"><span data-stu-id="989ff-110">The flags listed for the required and basic commands provide a minimum amount of information about a device.</span></span> <span data-ttu-id="989ff-111">許多裝置都會使用擴充旗標來補充必要和基本命令，以提供裝置的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="989ff-111">Many devices supplement the required and basic commands with extended flags to provide additional information about the device.</span></span>

 

 





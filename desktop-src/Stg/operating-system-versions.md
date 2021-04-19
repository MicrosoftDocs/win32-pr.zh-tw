---
title: 作業系統版本
description: 此 DWORD 資料類型應將作業系統類型保存為高序位單字，並將作業系統的版本號碼保留在低序位字組中。 下表列出作業系統的可能值。
ms.assetid: 318e277b-a797-45a5-87c5-25b91fdf278d
keywords:
- 作業系統版本結構化儲存體
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd5de916d354a721834b9a10651c36d3bf389e28
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106978582"
---
# <a name="operating-system-versions"></a><span data-ttu-id="c0a36-105">作業系統版本</span><span class="sxs-lookup"><span data-stu-id="c0a36-105">Operating System Versions</span></span>

<span data-ttu-id="c0a36-106">此 **DWORD** 資料類型應將作業系統類型保存為高序位單字，並將作業系統的版本號碼保留在低序位字組中。</span><span class="sxs-lookup"><span data-stu-id="c0a36-106">This **DWORD** data type should hold the operating system type in the high-order word and the version number of the operating system in the low-order word.</span></span> <span data-ttu-id="c0a36-107">下表列出作業系統的可能值。</span><span class="sxs-lookup"><span data-stu-id="c0a36-107">Possible values for the operating system are listed in the following table.</span></span>



| <span data-ttu-id="c0a36-108">作業系統</span><span class="sxs-lookup"><span data-stu-id="c0a36-108">Operating system</span></span>       | <span data-ttu-id="c0a36-109">值</span><span class="sxs-lookup"><span data-stu-id="c0a36-109">Value</span></span>  |
|------------------------|--------|
| <span data-ttu-id="c0a36-110">32位 Windows (Win32) </span><span class="sxs-lookup"><span data-stu-id="c0a36-110">32-Bit Windows (Win32)</span></span> | <span data-ttu-id="c0a36-111">0x0002</span><span class="sxs-lookup"><span data-stu-id="c0a36-111">0x0002</span></span> |
| <span data-ttu-id="c0a36-112">Macintosh</span><span class="sxs-lookup"><span data-stu-id="c0a36-112">Macintosh</span></span>              | <span data-ttu-id="c0a36-113">0x0001</span><span class="sxs-lookup"><span data-stu-id="c0a36-113">0x0001</span></span> |
| <span data-ttu-id="c0a36-114">16位 Windows (Win16) </span><span class="sxs-lookup"><span data-stu-id="c0a36-114">16-Bit Windows (Win16)</span></span> | <span data-ttu-id="c0a36-115">0x0000</span><span class="sxs-lookup"><span data-stu-id="c0a36-115">0x0000</span></span> |



 

<span data-ttu-id="c0a36-116">針對 Microsoft Windows 作業系統，作業系統版本是由 [**GetVersion**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getversion) 函數傳回的低序位文字。</span><span class="sxs-lookup"><span data-stu-id="c0a36-116">For Microsoft Windows operating systems, the operating system version is the low-order word returned by the [**GetVersion**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getversion) function.</span></span> <span data-ttu-id="c0a36-117">針對 Microsoft Windows，下列範例程式碼會正確地設定來源作業系統的版本。</span><span class="sxs-lookup"><span data-stu-id="c0a36-117">For Microsoft Windows, the following example code correctly sets the version of the originating operating system.</span></span>

``` syntax
#ifdef WIN32 
    dwOSVer = (DWORD)MAKELONG( LOWORD(GetVersion()), 2 ) ; 
#else 
    dwOSVer = (DWORD)MAKELONG( LOWORD(GetVersion()), 0 ) ; 
#endif
```

 

 
---
title: 尋找特定的驅動程式
description: 尋找特定的驅動程式
ms.assetid: d48dc313-4606-4f70-b2fe-ed99160e53fc
keywords:
- 音訊壓縮管理員 (的) ，尋找驅動程式
- " (音效壓縮管理員) 、尋找驅動程式"
- 進行中的範例，尋找驅動程式
- 尋找驅動程式
- acmDriverEnum 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54d8e8198fdf3bc742c2705e1a83b3ea8036c80f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840639"
---
# <a name="finding-a-specific-driver"></a><span data-ttu-id="fdc3b-108">尋找特定的驅動程式</span><span class="sxs-lookup"><span data-stu-id="fdc3b-108">Finding a Specific Driver</span></span>

<span data-ttu-id="fdc3b-109">您可能會想要讓應用程式將訊息直接傳送到特定的驅動程式，或從清單中識別特定的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="fdc3b-109">You might want your application to send a message directly to a specific driver or to identify certain drivers from the list.</span></span> <span data-ttu-id="fdc3b-110">例如，您可能想要讓應用程式識別支援篩選的驅動程式，然後查詢每個驅動程式來判斷它支援的篩選標記。</span><span class="sxs-lookup"><span data-stu-id="fdc3b-110">For example, you might want your application to identify those drivers that support filters and then query each driver to determine which filter tags it supports.</span></span> <span data-ttu-id="fdc3b-111">您可以使用 [**acmDriverEnum**](/windows/desktop/api/Msacm/nf-msacm-acmdriverenum) 函數來取得所需驅動程式或驅動程式的控制碼;然後可以使用此控制碼來與該驅動程式通訊。</span><span class="sxs-lookup"><span data-stu-id="fdc3b-111">You can use the [**acmDriverEnum**](/windows/desktop/api/Msacm/nf-msacm-acmdriverenum) function to obtain a handle to the desired driver or drivers; this handle can then be used to communicate with that driver.</span></span>

<span data-ttu-id="fdc3b-112">請注意，當應用程式安裝本機驅動程式供自己使用時， [**acmDriverAdd**](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd) 函式會傳回驅動程式控制碼，可用來與驅動程式進行通訊。</span><span class="sxs-lookup"><span data-stu-id="fdc3b-112">Note that when an application installs a local driver for its own use, the [**acmDriverAdd**](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd) function returns a driver handle, which can be used to communicate with the driver.</span></span> <span data-ttu-id="fdc3b-113">在此情況下，不需要使用 **acmDriverEnum** 。</span><span class="sxs-lookup"><span data-stu-id="fdc3b-113">It is not necessary to use **acmDriverEnum** in this case.</span></span>

 

 





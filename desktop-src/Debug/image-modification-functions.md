---
description: 影像修改函式可讓您變更可執行檔映射。
ms.assetid: 195959cb-e1ab-4c76-b7f9-f20522feac8c
title: Imagehlp.dll 影像修改函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06f6be83457738d1237865940463f438d3b73afa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103688624"
---
# <a name="imagehlp-image-modification-functions"></a><span data-ttu-id="419c9-103">Imagehlp.dll 影像修改函式</span><span class="sxs-lookup"><span data-stu-id="419c9-103">ImageHlp Image Modification Functions</span></span>

<span data-ttu-id="419c9-104">影像修改函式可讓您變更可執行檔映射。</span><span class="sxs-lookup"><span data-stu-id="419c9-104">The image modification functions allow you to change the executable image.</span></span> <span data-ttu-id="419c9-105">它們大多用於開發工具和安裝程式。</span><span class="sxs-lookup"><span data-stu-id="419c9-105">They are mostly for use by development tools and install programs.</span></span> <span data-ttu-id="419c9-106">您可以使用它們來系結影像、計算其總和檢查碼 (，這對確保映射完整性) 、變更其載入位址，以及產生符號檔而言很重要。</span><span class="sxs-lookup"><span data-stu-id="419c9-106">They can be used to bind an image, compute its checksum (which is important for ensuring image integrity), change its load address, and produce symbol files.</span></span>

<span data-ttu-id="419c9-107">以下是影像修改函式。</span><span class="sxs-lookup"><span data-stu-id="419c9-107">The following are the image modification functions.</span></span>

-   [<span data-ttu-id="419c9-108">**BindImage**</span><span class="sxs-lookup"><span data-stu-id="419c9-108">**BindImage**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-bindimage)
-   [<span data-ttu-id="419c9-109">**BindImageEx**</span><span class="sxs-lookup"><span data-stu-id="419c9-109">**BindImageEx**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-bindimageex)
-   [<span data-ttu-id="419c9-110">**CheckSumMappedFile**</span><span class="sxs-lookup"><span data-stu-id="419c9-110">**CheckSumMappedFile**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-checksummappedfile)
-   [<span data-ttu-id="419c9-111">**MapFileAndCheckSum**</span><span class="sxs-lookup"><span data-stu-id="419c9-111">**MapFileAndCheckSum**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-mapfileandchecksuma)
-   [<span data-ttu-id="419c9-112">**ReBaseImage**</span><span class="sxs-lookup"><span data-stu-id="419c9-112">**ReBaseImage**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-rebaseimage)
-   [<span data-ttu-id="419c9-113">**SplitSymbols**</span><span class="sxs-lookup"><span data-stu-id="419c9-113">**SplitSymbols**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-splitsymbols)
-   [<span data-ttu-id="419c9-114">**StatusRoutine**</span><span class="sxs-lookup"><span data-stu-id="419c9-114">**StatusRoutine**</span></span>](/windows/desktop/api/Imagehlp/nc-imagehlp-pimagehlp_status_routine)
-   [<span data-ttu-id="419c9-115">**TouchFileTimes**</span><span class="sxs-lookup"><span data-stu-id="419c9-115">**TouchFileTimes**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-touchfiletimes)
-   [<span data-ttu-id="419c9-116">**UpdateDebugInfoFile**</span><span class="sxs-lookup"><span data-stu-id="419c9-116">**UpdateDebugInfoFile**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-updatedebuginfofile)
-   [<span data-ttu-id="419c9-117">**UpdateDebugInfoFileEx**</span><span class="sxs-lookup"><span data-stu-id="419c9-117">**UpdateDebugInfoFileEx**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-updatedebuginfofileex)

 

 




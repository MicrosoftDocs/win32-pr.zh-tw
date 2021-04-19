---
title: Desktop Win32 程式碼範例
description: 關於 Win32 的範例存放庫，以及如何在這些範例中進行搜尋。
ms.topic: article
ms.date: 03/19/2021
ms.openlocfilehash: 5a4083697d444f36b31c553a2d6159d4370565d4
ms.sourcegitcommit: 46e75903326c49a6c5cc576ee2b4f67f64a6d5ff
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/20/2021
ms.locfileid: "106976756"
---
# <a name="desktop-win32-code-samples"></a><span data-ttu-id="4be33-103">Desktop Win32 程式碼範例</span><span class="sxs-lookup"><span data-stu-id="4be33-103">Desktop Win32 code samples</span></span>

<span data-ttu-id="4be33-104">另請參閱程式 [代碼範例](https://developer.microsoft.com/windows/samples/)。</span><span class="sxs-lookup"><span data-stu-id="4be33-104">Also see [Code samples](https://developer.microsoft.com/windows/samples/).</span></span>

## <a name="find-a-sample-for-the-api-youre-interested-in"></a><span data-ttu-id="4be33-105">尋找您感興趣的 API 範例</span><span class="sxs-lookup"><span data-stu-id="4be33-105">Find a sample for the API you're interested in</span></span>

<span data-ttu-id="4be33-106">您可以使用 Microsoft Visual Studio 來搜尋整個存放庫的原始程式碼，以查看是否正在示範特定 Windows API 的使用方式。</span><span class="sxs-lookup"><span data-stu-id="4be33-106">You can use Microsoft Visual Studio to search an entire repo's source code to see whether the usage of a particular Windows API is being demonstrated.</span></span>

* <span data-ttu-id="4be33-107">複製下列各節中所列的任何存放庫， (或將 ZIP) 下載至本機檔案系統。</span><span class="sxs-lookup"><span data-stu-id="4be33-107">Clone any of the repos listed in the sections below (or download the ZIP) to your local file system.</span></span>
* <span data-ttu-id="4be33-108">然後在 Visual Studio 的檔案中 **尋找** 。</span><span class="sxs-lookup"><span data-stu-id="4be33-108">Then **Find in Files** in Visual Studio.</span></span> <span data-ttu-id="4be33-109">將 [ **查詢** ] 設定為您所複製或下載的資料夾，並搜尋您感興趣的 API 名稱。</span><span class="sxs-lookup"><span data-stu-id="4be33-109">Set **Look in** to the folder you cloned or downloaded into, and search for the name of the API you're interested in.</span></span> <span data-ttu-id="4be33-110">檢查 **相符的大小寫** 可提供最佳結果。</span><span class="sxs-lookup"><span data-stu-id="4be33-110">Checking **Match case** gives best results.</span></span>
* <span data-ttu-id="4be33-111">如果可在各種形式中呼叫 API &mdash; （例如， **CreateMutex**、 **CreateMutexA** 和 **CreateMutexW**），請小心檢查全字相符。</span><span class="sxs-lookup"><span data-stu-id="4be33-111">Be careful of checking **Match whole word** if the API can be called in various forms&mdash;for example, **CreateMutex**, **CreateMutexA**, and **CreateMutexW**.</span></span> <span data-ttu-id="4be33-112">在這種情況下，請在未核取 **全字** 的情況下搜尋 **CreateMutex** 。</span><span class="sxs-lookup"><span data-stu-id="4be33-112">In that case, search for **CreateMutex** with **Match whole word** unchecked.</span></span>

> [!NOTE]
> <span data-ttu-id="4be33-113">您可以安裝 [Visual Studio](https://visualstudio.microsoft.com/downloads/) 而不需要支付費用。</span><span class="sxs-lookup"><span data-stu-id="4be33-113">You can install [Visual Studio](https://visualstudio.microsoft.com/downloads/) without expense.</span></span> <span data-ttu-id="4be33-114">有提供 &mdash; 免費的學生、開放原始碼參與者及個人版的社區版。</span><span class="sxs-lookup"><span data-stu-id="4be33-114">A Community edition is available&mdash;it's free for students, open-source contributors, and individuals.</span></span> <span data-ttu-id="4be33-115">當然，您也可以使用任何範例存放庫來進行相同的動作。</span><span class="sxs-lookup"><span data-stu-id="4be33-115">Of course you can do the same thing with any samples repo.</span></span>

## <a name="the-windows-classic-samples-repo"></a><span data-ttu-id="4be33-116">Windows 傳統範例存放庫</span><span class="sxs-lookup"><span data-stu-id="4be33-116">The Windows classic samples repo</span></span>

<span data-ttu-id="4be33-117">包含使用 WIN32 API 之範例 Windows 應用程式的主要存放庫是 [Windows 傳統範例](https://github.com/Microsoft/Windows-classic-samples) 存放庫。</span><span class="sxs-lookup"><span data-stu-id="4be33-117">The main repo containing sample Windows apps using the Win32 API is the [Windows classic samples](https://github.com/Microsoft/Windows-classic-samples) repo.</span></span>

## <a name="directx-samples"></a><span data-ttu-id="4be33-118">DirectX 範例</span><span class="sxs-lookup"><span data-stu-id="4be33-118">DirectX samples</span></span>

<span data-ttu-id="4be33-119">請參閱適用于 DirectX 12 圖形範例的 [Directx 圖形範例](https://github.com/Microsoft/DirectX-Graphics-Samples) 存放庫，其示範如何針對 Windows 10 建立需要大量圖形的應用程式。</span><span class="sxs-lookup"><span data-stu-id="4be33-119">See the [DirectX-Graphics-Samples](https://github.com/Microsoft/DirectX-Graphics-Samples) repo for DirectX 12 Graphics samples that demonstrate how to build graphics-intensive applications for Windows 10.</span></span>

<span data-ttu-id="4be33-120">另請參閱 [DirectX 範例](/windows/uwp/gaming/directx-samples)。</span><span class="sxs-lookup"><span data-stu-id="4be33-120">Also see [DirectX samples](/windows/uwp/gaming/directx-samples).</span></span>

## <a name="older-samples"></a><span data-ttu-id="4be33-121">舊版範例</span><span class="sxs-lookup"><span data-stu-id="4be33-121">Older samples</span></span>

<span data-ttu-id="4be33-122">您可以在 [MSDN 程式碼庫 Microsoft 範例存放庫](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208.1%20desktop%20samples/%5BC%2B%2B%5D-Windows%208.1%20desktop%20samples) 中找到一些較舊的 Win32 範例應用程式。</span><span class="sxs-lookup"><span data-stu-id="4be33-122">You can find some older Win32 sample apps in the [MSDN Code Gallery Microsoft samples](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208.1%20desktop%20samples/%5BC%2B%2B%5D-Windows%208.1%20desktop%20samples) repo.</span></span>

## <a name="see-also"></a><span data-ttu-id="4be33-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4be33-123">See also</span></span>

* [<span data-ttu-id="4be33-124">程式碼範例</span><span class="sxs-lookup"><span data-stu-id="4be33-124">Code samples</span></span>](https://developer.microsoft.com/windows/samples/)
* [<span data-ttu-id="4be33-125">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="4be33-125">Visual Studio</span></span>](https://visualstudio.microsoft.com/downloads/)
* [<span data-ttu-id="4be33-126">Windows 傳統範例</span><span class="sxs-lookup"><span data-stu-id="4be33-126">Windows classic samples</span></span>](https://github.com/Microsoft/Windows-classic-samples)
* [<span data-ttu-id="4be33-127">DirectX-Graphics-Samples</span><span class="sxs-lookup"><span data-stu-id="4be33-127">DirectX-Graphics-Samples</span></span>](https://github.com/Microsoft/DirectX-Graphics-Samples)
* [<span data-ttu-id="4be33-128">DirectX 範例</span><span class="sxs-lookup"><span data-stu-id="4be33-128">DirectX samples</span></span>](/windows/uwp/gaming/directx-samples)
* [<span data-ttu-id="4be33-129">MSDN 程式碼庫 Microsoft 範例</span><span class="sxs-lookup"><span data-stu-id="4be33-129">MSDN Code Gallery Microsoft samples</span></span>](https://github.com/microsoftarchive/msdn-code-gallery-microsoft)

---
description: 您可能偶爾需要判斷應用程式是否在 Tablet PC 上執行，因為您可能會想要讓您的應用程式利用固有的筆墨、辨識和畫筆功能。
ms.assetid: 86a3eddb-6541-4b73-b2ca-6adedad1a1e5
title: 判斷電腦是否為 Tablet PC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c793d5531d6091d4bce73d99bfa32d100c2b9304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979313"
---
# <a name="determining-whether-a-pc-is-a-tablet-pc"></a><span data-ttu-id="98933-103">判斷電腦是否為 Tablet PC</span><span class="sxs-lookup"><span data-stu-id="98933-103">Determining Whether a PC is a Tablet PC</span></span>

<span data-ttu-id="98933-104">您可能偶爾需要判斷應用程式是否在 Tablet PC 上執行，因為您可能會想要讓您的應用程式利用固有的筆墨、辨識和畫筆功能。</span><span class="sxs-lookup"><span data-stu-id="98933-104">You may occasionally need to determine whether your application is running on a Tablet PC because you may want your applications to take advantage of inherent ink, recognition, and pen capabilities.</span></span> <span data-ttu-id="98933-105">為了協助您判斷您的應用程式是否能存取 Tablet PC 功能，您可以使用 GetSystemMetrics () Windows API 呼叫，如本主題中所述。</span><span class="sxs-lookup"><span data-stu-id="98933-105">To help you determine whether your application has access to the Tablet PC features, you can use the GetSystemMetrics() Windows API call as described in this topic.</span></span>

## <a name="client-side-applications"></a><span data-ttu-id="98933-106">Client-Side 應用程式</span><span class="sxs-lookup"><span data-stu-id="98933-106">Client-Side Applications</span></span>

<span data-ttu-id="98933-107">您可以使用下列技術，判斷您的程式碼是否在 Tablet PC 上執行。</span><span class="sxs-lookup"><span data-stu-id="98933-107">You can use the following techniques to determine whether your code is running on a Tablet PC.</span></span>

-   [<span data-ttu-id="98933-108">使用 GetSystemMetrics (SM \_ 平板) </span><span class="sxs-lookup"><span data-stu-id="98933-108">Using GetSystemMetrics (SM\_TABLETPC)</span></span>](/windows)
-   [<span data-ttu-id="98933-109">使用平板電腦平臺二進位檔的存在</span><span class="sxs-lookup"><span data-stu-id="98933-109">Using the Presence of Tablet Platform Binaries</span></span>](#using-the-presence-of-tablet-platform-binaries)
-   [<span data-ttu-id="98933-110">以 Web 為基礎的應用程式</span><span class="sxs-lookup"><span data-stu-id="98933-110">Web-Based Applications</span></span>](#web-based-applications)

### <a name="using-getsystemmetrics-sm_tabletpc"></a><span data-ttu-id="98933-111">使用 GetSystemMetrics (SM \_ 平板) </span><span class="sxs-lookup"><span data-stu-id="98933-111">Using GetSystemMetrics (SM\_TABLETPC)</span></span>

### <a name="windows-xp-tablet-pc-edition"></a><span data-ttu-id="98933-112">Windows XP Tablet PC Edition</span><span class="sxs-lookup"><span data-stu-id="98933-112">Windows XP Tablet PC Edition</span></span>

<span data-ttu-id="98933-113">在 Microsoft Windows XP Tablet PC Edition 中，請使用 GetSystemMetrics (SM \_ 平板電腦) 功能來判斷電腦是否為 TABLET PC。</span><span class="sxs-lookup"><span data-stu-id="98933-113">In Microsoft Windows XP Tablet PC Edition, use the GetSystemMetrics(SM\_TABLETPC) function to determine whether a computer is a Tablet PC.</span></span> <span data-ttu-id="98933-114">GetSystemMetrics (SM \_ 平板電腦) 是設計成在執行 WINDOWS XP TABLET PC Edition 的電腦上回到 TRUE。</span><span class="sxs-lookup"><span data-stu-id="98933-114">GetSystemMetrics(SM\_TABLETPC) is designed to return TRUE on a computer running Windows XP Tablet PC Edition.</span></span>

### <a name="windows-vista"></a><span data-ttu-id="98933-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="98933-115">Windows Vista</span></span>

<span data-ttu-id="98933-116">在 Windows Vista 中，不再有不同的 Tablet PC SDK。</span><span class="sxs-lookup"><span data-stu-id="98933-116">In Windows Vista, there is no longer a distinct Tablet PC SDK.</span></span> <span data-ttu-id="98933-117">Windows SDK 現在包含一個稱為「Tablet PC 和觸控技術」的區段，而 GetSystemMetrics (SM 平板電腦) 的邏輯已 \_ 變更為反映這一點。</span><span class="sxs-lookup"><span data-stu-id="98933-117">The Windows SDK now contains a section called "Tablet PC and Touch Technology" and the logic of GetSystemMetrics(SM\_TABLETPC) has been changed to reflect this.</span></span> <span data-ttu-id="98933-118">GetSystemMetrics (SM \_ 平板) 現在如果符合下列所有條件，則會傳回 true：</span><span class="sxs-lookup"><span data-stu-id="98933-118">GetSystemMetrics(SM\_TABLETPC) now returns true if all of the following are true:</span></span>

-   <span data-ttu-id="98933-119">系統上有一個整合式數位板，也就是筆觸或觸控。</span><span class="sxs-lookup"><span data-stu-id="98933-119">There is an integrated digitizer, either pen or touch, on the system.</span></span>
-   <span data-ttu-id="98933-120">已安裝 Tablet PC 選用元件。</span><span class="sxs-lookup"><span data-stu-id="98933-120">The Tablet PC optional component is installed.</span></span> <span data-ttu-id="98933-121">此元件包含 [Tablet PC 輸入面板] 和 [Windows 筆記本] 等功能。</span><span class="sxs-lookup"><span data-stu-id="98933-121">This component contains features such as Tablet PC Input Panel and Windows Journal.</span></span>
-   <span data-ttu-id="98933-122">電腦授權使用選用元件。</span><span class="sxs-lookup"><span data-stu-id="98933-122">The computer is licensed to use the optional component.</span></span> <span data-ttu-id="98933-123">高階版本的 Windows Vista （像是 Windows Vista Home Premium、Windows Vista Small Business、Windows Vista Professional、Windows Vista Enterprise 和 Windows Vista 旗艦版）是授權使用選用元件。</span><span class="sxs-lookup"><span data-stu-id="98933-123">Premium versions of Windows Vista—such as Windows Vista Home Premium, Windows Vista Small Business, Windows Vista Professional, Windows Vista Enterprise, and Windows Vista Ultimate—are licensed to use the optional component.</span></span>
-   <span data-ttu-id="98933-124">Tablet PC 輸入服務正在執行。</span><span class="sxs-lookup"><span data-stu-id="98933-124">Tablet PC Input Service is running.</span></span> <span data-ttu-id="98933-125">Tablet PC 輸入服務是 Windows Vista 的新服務，可控制 Tablet PC 輸入。</span><span class="sxs-lookup"><span data-stu-id="98933-125">Tablet PC Input Service is a new service for Windows Vista that controls Tablet PC input.</span></span>

<span data-ttu-id="98933-126">利用這種提高的精確度，GetSystemMetrics (SM \_ 平板電腦) 繼續建議用來判斷執行 Windows Vista 的電腦是否為 TABLET PC。</span><span class="sxs-lookup"><span data-stu-id="98933-126">With this increased accuracy, GetSystemMetrics(SM\_TABLETPC) continues to be the recommended way to determine whether a computer running Windows Vista is a Tablet PC.</span></span>

### <a name="using-the-presence-of-tablet-platform-binaries"></a><span data-ttu-id="98933-127">使用平板電腦平臺二進位檔的存在</span><span class="sxs-lookup"><span data-stu-id="98933-127">Using the Presence of Tablet Platform Binaries</span></span>

<span data-ttu-id="98933-128">在 Windows XP Tablet PC Edition 和 Windows Vista 中，您可以搜尋筆墨二進位檔（例如 inkobj.dll 和 Microsoft.Ink.dll）是否存在，並使用其支援的功能（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="98933-128">In both Windows XP Tablet PC Edition and Windows Vista, you can search for the presence of the ink binaries—such as inkobj.dll and Microsoft.Ink.dll—and use their supported functionality if they are present.</span></span>

<span data-ttu-id="98933-129">在 Windows Vista 中，預設會在所有的用戶端版本上安裝 Tablet PC 平臺二進位檔。</span><span class="sxs-lookup"><span data-stu-id="98933-129">In Windows Vista, the Tablet PC Platform binaries are installed on all client versions by default.</span></span> <span data-ttu-id="98933-130">這些版本有提供輸入和筆跡功能。</span><span class="sxs-lookup"><span data-stu-id="98933-130">Input and inking functionality are available on those versions.</span></span> <span data-ttu-id="98933-131">辨識僅適用于 premium 版本的 Windows Vista。</span><span class="sxs-lookup"><span data-stu-id="98933-131">Recognition is available only in premium versions of Windows Vista.</span></span>

### <a name="web-based-applications"></a><span data-ttu-id="98933-132">Web-Based 應用程式</span><span class="sxs-lookup"><span data-stu-id="98933-132">Web-Based Applications</span></span>

<span data-ttu-id="98933-133">在 Windows Vista 中，Internet Explorer 所報告的使用者代理程式字串包含 "Tablet PC 2.0"，如果根據 GetSystemMetrics (SM \_ 平板電腦) ，則裝置是 tablet pc。</span><span class="sxs-lookup"><span data-stu-id="98933-133">In Windows Vista, the user-agent string reported by Internet Explorer includes "Tablet PC 2.0" if, according to GetSystemMetrics(SM\_TABLETPC), the device is a Tablet PC.</span></span>

<span data-ttu-id="98933-134">在 Windows XP Tablet PC Edition 2005 中，使用者代理字串包含 Tablet PC 1.7。</span><span class="sxs-lookup"><span data-stu-id="98933-134">In Windows XP Tablet PC Edition 2005, the user-agent string includes Tablet PC 1.7.</span></span> <span data-ttu-id="98933-135">使用者代理程式字串看起來像下面這樣：</span><span class="sxs-lookup"><span data-stu-id="98933-135">The user-agent string looks something like the following:</span></span>

`Mozilla/4.0 (compatible; MSIE 6.0; Windows NT 5.1; .NET CLR 1.0.3705; Tablet PC 2.0)`

<span data-ttu-id="98933-136">您可以使用此值來判斷用戶端電腦是否為 Tablet PC，並支援以 Web 為基礎的筆墨控制項。</span><span class="sxs-lookup"><span data-stu-id="98933-136">Use this value to determine whether the client computer is a Tablet PC and supports Web-based inking controls.</span></span>

## <a name="related-topics"></a><span data-ttu-id="98933-137">相關主題</span><span class="sxs-lookup"><span data-stu-id="98933-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="98933-138">**GetSystemMetrics**</span><span class="sxs-lookup"><span data-stu-id="98933-138">**GetSystemMetrics**</span></span>](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics)
</dt> </dl>

 

 

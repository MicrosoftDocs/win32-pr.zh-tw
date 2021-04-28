---
description: Internet Explorer 相容性測試工具 (IECTT)
ms.assetid: 11169540-555A-48A9-A4CD-535D5765C005
title: Internet Explorer 相容性測試工具 (IECTT)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3a35b3120e95c668f2808c9c525d0c1d4f89f8f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088282"
---
# <a name="internet-explorer-compatibility-test-tool-iectt"></a><span data-ttu-id="0e510-103">Internet Explorer 相容性測試工具 (IECTT)</span><span class="sxs-lookup"><span data-stu-id="0e510-103">Internet Explorer Compatibility Test Tool (IECTT)</span></span>

<span data-ttu-id="0e510-104">Internet Explorer 相容性測試控管 (IECTT) 是 [Microsoft 應用程式相容性](/windows-hardware/get-started/adk-install)工具組的元件。</span><span class="sxs-lookup"><span data-stu-id="0e510-104">The Internet Explorer Compatibility Test Tool (IECTT) is a component of the [Microsoft Application Compatibility Toolkit](/windows-hardware/get-started/adk-install).</span></span> <span data-ttu-id="0e510-105">這項工具可協助您診斷 web 應用程式中的問題，方法是即時顯示問題，並選擇性地將結果上傳至 ACT 資料庫。</span><span class="sxs-lookup"><span data-stu-id="0e510-105">This tool can help you diagnose issues in your web applications by displaying issues in real time and optionally uploading the results to an ACT database.</span></span> <span data-ttu-id="0e510-106">結果包括有關可能的相容性問題的詳細資料，以及有關每個相容性問題的詳細資訊連結。</span><span class="sxs-lookup"><span data-stu-id="0e510-106">The results include details about possible compatibility issues and links for more information about each compatibility issue.</span></span> <span data-ttu-id="0e510-107">IECTT 也可讓您排除問題和修改可用的屬性。</span><span class="sxs-lookup"><span data-stu-id="0e510-107">IECTT also enables you to exclude issues and modify available attributes.</span></span>

## <a name="to-open-iectt"></a><span data-ttu-id="0e510-108">開啟 IECTT</span><span class="sxs-lookup"><span data-stu-id="0e510-108">To open IECTT</span></span>

1.  <span data-ttu-id="0e510-109">安裝 [Microsoft 應用程式相容性工具](/windows-hardware/get-started/adk-install)組。</span><span class="sxs-lookup"><span data-stu-id="0e510-109">Install the [Microsoft Application Compatibility Toolkit](/windows-hardware/get-started/adk-install).</span></span>
2.  <span data-ttu-id="0e510-110">按一下 [ **開始**]，依序指向 [ **程式**]、[ **Microsoft 應用程式相容性** 工具組 5.6]、[ **開發人員和測試人員工具**]，然後按一下 [ **Internet Explorer 相容性測試控管**]。</span><span class="sxs-lookup"><span data-stu-id="0e510-110">Click **Start**, point to **Programs**, point to **Microsoft Application Compatibility Toolkit 5.6**, point to **Developer and Tester Tools**, and then click **Internet Explorer Compatibility Test Tool**.</span></span>

<span data-ttu-id="0e510-111">下列各節說明常見的 IECTT 案例。</span><span class="sxs-lookup"><span data-stu-id="0e510-111">The following sections describe common IECTT scenarios.</span></span>

## <a name="view-issues-in-real-time"></a><span data-ttu-id="0e510-112">即時查看問題</span><span class="sxs-lookup"><span data-stu-id="0e510-112">View Issues in Real Time</span></span>

<span data-ttu-id="0e510-113">當您針對 Windows Internet Explorer 7 和 Windows Internet Explorer 8 測試網站和 web 應用程式時，可以即時找出並查看您的 web 架構問題。</span><span class="sxs-lookup"><span data-stu-id="0e510-113">You can locate and view your web-based issues in real time, while you are testing your websites and web applications against Windows Internet Explorer 7 and Windows Internet Explorer 8.</span></span> <span data-ttu-id="0e510-114">完成測試之後，您可以在 IECTT 的 [ **即時資料** ] 畫面中查看結果。</span><span class="sxs-lookup"><span data-stu-id="0e510-114">After you complete your testing, you can view your results in the **Live Data** screen of the IECTT.</span></span>

## <a name="upload-issues-to-your-act-database"></a><span data-ttu-id="0e510-115">將問題上傳至您的 ACT 資料庫</span><span class="sxs-lookup"><span data-stu-id="0e510-115">Upload Issues to Your ACT Database</span></span>

<span data-ttu-id="0e510-116">您可以將 web 式問題上傳至 ACT 資料庫，此資料庫會處理資訊，並可讓您在應用程式相容性管理員的 [ **分析** ] 畫面上查看結果。</span><span class="sxs-lookup"><span data-stu-id="0e510-116">You can upload your web-based issues to the ACT database, which processes the information and enables you to view your results on the **Analyze** screen of the Application Compatibility Manager.</span></span>

## <a name="collect-your-compatibility-data"></a><span data-ttu-id="0e510-117">收集您的相容性資料</span><span class="sxs-lookup"><span data-stu-id="0e510-117">Collect Your Compatibility Data</span></span>

<span data-ttu-id="0e510-118">您可以使用 Internet Explorer 7 或 Internet Explorer 7 的 IECTT 工具，收集您的網站和 web 應用程式相關的相容性資料。</span><span class="sxs-lookup"><span data-stu-id="0e510-118">You can collect your website and web application-related compatibility data by using the IECTT tool with either Internet Explorer 7 or Internet Explorer 7.</span></span>

<span data-ttu-id="0e510-119">**收集相容性資料**</span><span class="sxs-lookup"><span data-stu-id="0e510-119">**To collect your compatibility data**</span></span>

1.  <span data-ttu-id="0e510-120">關閉所有作用中的 Windows Internet Explorer 視窗。</span><span class="sxs-lookup"><span data-stu-id="0e510-120">Close all of your active Windows Internet Explorer windows.</span></span>
2.  <span data-ttu-id="0e510-121">在 IECTT 的 [ **Internet Explorer 相容性測試] 工具** 工具列上，按一下 [ **啟用**]。</span><span class="sxs-lookup"><span data-stu-id="0e510-121">In IECTT, on the **Internet Explorer Compatibility Test Tool** toolbar, click **Enable**.</span></span>
3.  <span data-ttu-id="0e510-122">開啟 Internet Explorer 7 或 Internet Explorer 8] 視窗。</span><span class="sxs-lookup"><span data-stu-id="0e510-122">Open an Internet Explorer 7 or Internet Explorer 8 window.</span></span>

    <span data-ttu-id="0e510-123">此時會出現一則訊息，指出相容性評估記錄已開啟。</span><span class="sxs-lookup"><span data-stu-id="0e510-123">A message appears and states that compatibility evaluation logging is turned on.</span></span>

4.  <span data-ttu-id="0e510-124">造訪您的組織所需的網站或 web 應用程式。</span><span class="sxs-lookup"><span data-stu-id="0e510-124">Visit the websites or web applications that are required for use by your organization.</span></span> <span data-ttu-id="0e510-125">當您造訪每個網站時，IECTT 工具會即時顯示您可能的相容性問題。</span><span class="sxs-lookup"><span data-stu-id="0e510-125">As you visit each site, the IECTT tool displays, in real-time, your potential compatibility issues.</span></span>
5.  <span data-ttu-id="0e510-126">在 [ **Internet Explorer 相容性測試控管** ] 工具列上，按一下 [ **停** 用] （當您完成時）。</span><span class="sxs-lookup"><span data-stu-id="0e510-126">On the **Internet Explorer Compatibility Test Tool** toolbar, click **Disable** when you are done.</span></span>

    <span data-ttu-id="0e510-127">相容性記錄程式完成並停止。</span><span class="sxs-lookup"><span data-stu-id="0e510-127">The compatibility logging process finishes and stops.</span></span>

## <a name="filter-your-issue-results"></a><span data-ttu-id="0e510-128">篩選您的問題結果</span><span class="sxs-lookup"><span data-stu-id="0e510-128">Filter Your Issue Results</span></span>

<span data-ttu-id="0e510-129">您可以依物件名稱、問題類型或兩者來篩選任何 IECTT 結果。</span><span class="sxs-lookup"><span data-stu-id="0e510-129">You can filter any of your IECTT results by object name, by issue type, or by both.</span></span>

<span data-ttu-id="0e510-130">**篩選您的問題結果**</span><span class="sxs-lookup"><span data-stu-id="0e510-130">**To filter your issue results**</span></span>

1.  <span data-ttu-id="0e510-131">在 [ **Internet Explorer 相容性測試] 工具** 畫面上，按一下 [ **篩選**]。</span><span class="sxs-lookup"><span data-stu-id="0e510-131">On the **Internet Explorer Compatibility Test Tool** screen, click **Filter**.</span></span>

    <span data-ttu-id="0e510-132">[ **問題篩選器** ] 對話方塊隨即出現。</span><span class="sxs-lookup"><span data-stu-id="0e510-132">The **Issues Filter** dialog box appears.</span></span>

2.  <span data-ttu-id="0e510-133">在 [ **輸入物件名稱來查看** box 的問題] 中，輸入您想要查看的物件名稱。</span><span class="sxs-lookup"><span data-stu-id="0e510-133">Enter the name of the object that you intend to view in the **Enter the name of the object to view issues for** box.</span></span>

<span data-ttu-id="0e510-134">如需此工具和其他開發人員工具的詳細資訊，請參閱 MSDN Library 中的 [Internet Explorer 相容性測試控管是什麼？](/previous-versions/windows/it-pro/windows-7/cc721989(v=ws.10)) 以及 IE8 blog 文章 [中的應用程式相容性記錄](/archive/blogs/ie/application-compatibility-logging-in-ie8) 。</span><span class="sxs-lookup"><span data-stu-id="0e510-134">For more information about this tool and other developers tools, see [What is the Internet Explorer Compatibility Test Tool?](/previous-versions/windows/it-pro/windows-7/cc721989(v=ws.10)) in the MSDN Library and the [Application Compatibility Logging in IE8](/archive/blogs/ie/application-compatibility-logging-in-ie8) blog post.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0e510-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="0e510-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e510-136">用於調試 Web 應用程式和附加元件的工具</span><span class="sxs-lookup"><span data-stu-id="0e510-136">Tools for Debugging Web Applications and Add-Ons</span></span>](tools-for-debugging-web-applications-and-add-ons.md)
</dt> </dl>

 

 

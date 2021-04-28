---
description: 移除 Windows Mail
ms.assetid: 356f0d79-12dd-49f0-b756-a46f20177efa
title: 移除 Windows Mail
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d50ad1008d9e252e1705a159f19d362677934023
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116276"
---
# <a name="removal-of-windows-mail"></a><span data-ttu-id="96864-103">移除 Windows Mail</span><span class="sxs-lookup"><span data-stu-id="96864-103">Removal of Windows Mail</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="96864-104">受影響的平臺</span><span class="sxs-lookup"><span data-stu-id="96864-104">Affected Platforms</span></span>

<span data-ttu-id="96864-105">**客戶** 端-Windows 7</span><span class="sxs-lookup"><span data-stu-id="96864-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="96864-106">**伺服器** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="96864-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="96864-107">功能影響</span><span class="sxs-lookup"><span data-stu-id="96864-107">Feature Impact</span></span>

<span data-ttu-id="96864-108">**嚴重性** -高</span><span class="sxs-lookup"><span data-stu-id="96864-108">**Severity** - High</span></span>  
<span data-ttu-id="96864-109">**頻率** -高</span><span class="sxs-lookup"><span data-stu-id="96864-109">**Frequency** - High</span></span>  









## <a name="description"></a><span data-ttu-id="96864-110">Description</span><span class="sxs-lookup"><span data-stu-id="96864-110">Description</span></span>

<span data-ttu-id="96864-111">Microsoft 正在淘汰 Windows Mail 公用程式，並停用 API CoStartOutlookExpress。</span><span class="sxs-lookup"><span data-stu-id="96864-111">Microsoft is deprecating the Windows Mail utility and disabling the API CoStartOutlookExpress.</span></span> <span data-ttu-id="96864-112">其他郵件 Api 已標示為已淘汰，並預定在稍後的 Windows 版本中移除。</span><span class="sxs-lookup"><span data-stu-id="96864-112">The other mail APIs have been marked as deprecated and are slated for removal in a later Windows version.</span></span> <span data-ttu-id="96864-113">不過，未標示為已淘汰或已淘汰的公開記錄 Api 將會在 Windows 7 中繼續運作。</span><span class="sxs-lookup"><span data-stu-id="96864-113">However, the publicly documented APIs that are not marked as deprecated or obsolete will continue to function in Windows 7.</span></span> <span data-ttu-id="96864-114">二進位檔會保留在使用者的系統上，而且會繼續透過 Api 存取，尤其是在上述情況下。</span><span class="sxs-lookup"><span data-stu-id="96864-114">Binaries will remain on the users' systems and will continue to be accessible via the APIs, specifically in the cases mentioned above.</span></span> <span data-ttu-id="96864-115">此外，使用者的電子郵件 ( .eml) 和新聞 ( nws) 檔會保留在系統上。</span><span class="sxs-lookup"><span data-stu-id="96864-115">In addition, the users' email (.eml) and news (.nws) files will remain on the system.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="96864-116">影響的表現</span><span class="sxs-lookup"><span data-stu-id="96864-116">Manifestation of Impact</span></span>

<span data-ttu-id="96864-117">移除 Windows Mail 會導致下列情況：</span><span class="sxs-lookup"><span data-stu-id="96864-117">Removal of Windows Mail results in the following:</span></span>

-   <span data-ttu-id="96864-118">所有進入 Windows Mail 和 Contacts 的進入點都 (例如，[開始] 功能表、使用者建立的快捷方式、[開始 > 執行]，) 移除或停用。</span><span class="sxs-lookup"><span data-stu-id="96864-118">All entry points to Windows Mail and Contacts (for example, Start Menu, user-created Shortcuts, Start -> Run, and so on) are removed or disabled.</span></span> <span data-ttu-id="96864-119">其中有些會完全移除，而其他則會在嘗試啟動時失敗。</span><span class="sxs-lookup"><span data-stu-id="96864-119">Some of these are completely removed, others will fail when trying to launch.</span></span>
-   <span data-ttu-id="96864-120">所有 Dll 都隨附于 box</span><span class="sxs-lookup"><span data-stu-id="96864-120">All DLLs ship in the box</span></span>
-   <span data-ttu-id="96864-121">公開記載的 Api 仍會像在 Windows Vista 中一樣繼續運作。</span><span class="sxs-lookup"><span data-stu-id="96864-121">Publicly documented APIs continue to work as they did in Windows Vista</span></span>
-   <span data-ttu-id="96864-122">任何嘗試啟動主要瀏覽器 UI 的 Api 都已經過修改，以建立無訊息失敗。</span><span class="sxs-lookup"><span data-stu-id="96864-122">Any APIs that attempt to launch the main browser UI have been modified to create a silent failure.</span></span> <span data-ttu-id="96864-123">函數會傳回成功，但不會向使用者顯示 UI。</span><span class="sxs-lookup"><span data-stu-id="96864-123">The function will return success, but will not show the UI to the user.</span></span> <span data-ttu-id="96864-124">呼叫其他對話方塊的 Api (例如，[多工緩衝處理器] 或 [帳戶] 對話方塊，) 繼續顯示該 UI</span><span class="sxs-lookup"><span data-stu-id="96864-124">APIs that call other dialog boxes (for example, the Spooler or the Accounts dialog) continue to show that UI</span></span>
-   <span data-ttu-id="96864-125">通訊協定 (mailto、ldap、news、snews、nntp) 處理常式將不會與 Windows Mail 或 Contacts 相關聯。</span><span class="sxs-lookup"><span data-stu-id="96864-125">Protocol (mailto, ldap, news, snews, nntp) handlers will not be associated with Windows Mail or Contacts.</span></span> <span data-ttu-id="96864-126">當您嘗試啟動這些專案時，客戶會看到錯誤對話方塊，指向可將這些關聯設定到其他程式的位置。</span><span class="sxs-lookup"><span data-stu-id="96864-126">When attempting to launch these, customers will see an error dialog pointing them to the location where they can set these associations to another program</span></span>
-   <span data-ttu-id="96864-127">檔案關聯 ( .eml、nws、. contact、. group、.wab、. p7c、. vfc) 已中斷或停用。</span><span class="sxs-lookup"><span data-stu-id="96864-127">File associations (.eml, .nws, .contact, .group, .wab, .p7c, .vfc) are broken or disabled.</span></span> <span data-ttu-id="96864-128">當嘗試使用這些延伸模組開啟檔案時，客戶會看到一個對話方塊，提供他們可使用的其他應用程式，並將其指向提供解決方案的網頁</span><span class="sxs-lookup"><span data-stu-id="96864-128">When attempting to open a file with these extensions, customers will get a dialog box offering them other apps that are installed that they can use and point them to a webpage that offers solutions</span></span>
-   <span data-ttu-id="96864-129">任何使用者檔案 (例如，連絡人檔案或訊息) 在升級案例中會保留在系統上</span><span class="sxs-lookup"><span data-stu-id="96864-129">Any user files (for example, contact files or messages) remain on the system in the upgrade scenario</span></span>
-   <span data-ttu-id="96864-130">[連絡人] 資料夾預設為隱藏，因此客戶不會看到它</span><span class="sxs-lookup"><span data-stu-id="96864-130">The Contacts folder is hidden by default so customers will not see it</span></span>
-   <span data-ttu-id="96864-131">Api 在 MSDN 中標示為已淘汰</span><span class="sxs-lookup"><span data-stu-id="96864-131">APIs are marked as deprecated in MSDN</span></span>
-   <span data-ttu-id="96864-132">檔案預覽功能已移除</span><span class="sxs-lookup"><span data-stu-id="96864-132">The file preview function is removed</span></span>
-   <span data-ttu-id="96864-133">滑鼠右鍵功能表中的 Shell 勾點已移除</span><span class="sxs-lookup"><span data-stu-id="96864-133">Shell hooks in the right-click menu are removed</span></span>
-   <span data-ttu-id="96864-134">檔案搜尋功能已移除</span><span class="sxs-lookup"><span data-stu-id="96864-134">The file search function is removed</span></span>

## <a name="mitigation"></a><span data-ttu-id="96864-135">降低</span><span class="sxs-lookup"><span data-stu-id="96864-135">Mitigation</span></span>

<span data-ttu-id="96864-136">使用者應該安裝 Windows Live Mail 或任何其他能夠讀取 .eml 和. nws 檔案的郵件產品。</span><span class="sxs-lookup"><span data-stu-id="96864-136">Users should install Windows Live Mail or any other mail product that is able to read .eml and .nws files.</span></span>

## <a name="solution"></a><span data-ttu-id="96864-137">解決方法</span><span class="sxs-lookup"><span data-stu-id="96864-137">Solution</span></span>

<span data-ttu-id="96864-138">偵測是否已安裝預設郵件處理常式。</span><span class="sxs-lookup"><span data-stu-id="96864-138">Detect if there is a default mail handler installed.</span></span> <span data-ttu-id="96864-139">如果沒有，請通知使用者安裝 Windows Live Mail 或任何能夠讀取 .eml 和. nws 檔案的其他產品。</span><span class="sxs-lookup"><span data-stu-id="96864-139">If not, advise user to install Windows Live Mail or any other product that is able to read .eml and .nws files.</span></span>

<span data-ttu-id="96864-140">請勿設計呼叫 Windows Mail UI API 的程式碼，因為它將無法運作。</span><span class="sxs-lookup"><span data-stu-id="96864-140">Do not design code that calls the Windows Mail UI API, since it will not work.</span></span> <span data-ttu-id="96864-141">您必須找到其他存取 .eml 和. nws 檔案的方式。</span><span class="sxs-lookup"><span data-stu-id="96864-141">You must find other ways to access the .eml and .nws files.</span></span> <span data-ttu-id="96864-142">此外，只要可行，就不再依賴所有其他 Windows Mail Api。</span><span class="sxs-lookup"><span data-stu-id="96864-142">In addition, as soon as is feasible, discontinue your reliance on all other Windows Mail APIs.</span></span>

## <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="96864-143">相容性、效能、可靠性和可用性測試</span><span class="sxs-lookup"><span data-stu-id="96864-143">Compatibility, Performance, Reliability, and Usability Testing</span></span>

-   <span data-ttu-id="96864-144">在 Windows 7 環境中練習您的應用程式，以確保應用程式不會嘗試呼叫 UI API。</span><span class="sxs-lookup"><span data-stu-id="96864-144">Exercise your application in a Windows 7 environment to ensure that the application does not try to call the UI API.</span></span>
-   <span data-ttu-id="96864-145">或者，您也可以使用 Windows 相容性評估工具 (ACT) 來執行應用程式相容性工具組 (WCE) ，以找出這項功能的取代可能發生的任何問題。</span><span class="sxs-lookup"><span data-stu-id="96864-145">Alternatively, you can run the Application Compatibility Toolkit (ACT) using the Windows Compatibility Evaluator (WCE) to locate any potential issues due to the deprecation of this functionality.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="96864-146">其他資源的連結</span><span class="sxs-lookup"><span data-stu-id="96864-146">Links to Other Resources</span></span>

<dl>

[<span data-ttu-id="96864-147">應用程式相容性工具組下載</span><span class="sxs-lookup"><span data-stu-id="96864-147">Application Compatibility Toolkit Download</span></span>](/windows-hardware/get-started/adk-install)  
</dl>

 

 

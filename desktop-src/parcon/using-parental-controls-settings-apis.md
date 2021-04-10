---
description: 使用家長監護設定 Api
ms.assetid: 77a239e9-1cec-4710-b673-7d0cebd502e9
title: 使用家長監護設定 Api
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dde4827dfe3ed5ee7eec6787744e6ff92f18775
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103693811"
---
# <a name="using-parental-controls-settings-apis"></a><span data-ttu-id="2669b-103">使用家長監護設定 Api</span><span class="sxs-lookup"><span data-stu-id="2669b-103">Using Parental Controls Settings APIs</span></span>

<span data-ttu-id="2669b-104">在記錄之前會討論設定，因為記錄是以使用者的設定為條件。</span><span class="sxs-lookup"><span data-stu-id="2669b-104">Settings are discussed ahead of logging because logging is conditional on the user's settings.</span></span>

## <a name="wmi-api-settings-writeread"></a><span data-ttu-id="2669b-105">WMI API 設定寫入/讀取</span><span class="sxs-lookup"><span data-stu-id="2669b-105">WMI API Settings Write/Read</span></span>

<span data-ttu-id="2669b-106">WMI API 提供的非抽象 (原始) 存取由家長監護基礎結構所具現化的所有設定，如 Wpcsprov. mof 架構檔案中所定義。</span><span class="sxs-lookup"><span data-stu-id="2669b-106">The WMI API provides non-abstracted (raw) access to all settings instantiated by the Parental Controls infrastructure as defined in the Wpcsprov.mof schema file.</span></span> <span data-ttu-id="2669b-107">設定存放區存在於 \\ 根 \\ CIMV2 \\ 應用程式 \\ WindowsParentalControls 命名空間中，並具有定義架構的下列類別定義。</span><span class="sxs-lookup"><span data-stu-id="2669b-107">The settings store exists in the \\root\\CIMV2\\Applications\\WindowsParentalControls namespace, with the following class definitions defining a schema.</span></span> <span data-ttu-id="2669b-108">會注明擴充性元素。</span><span class="sxs-lookup"><span data-stu-id="2669b-108">Extensibility elements are noted.</span></span>

<span data-ttu-id="2669b-109">每一電腦：</span><span class="sxs-lookup"><span data-stu-id="2669b-109">Per-computer:</span></span>

-   <span data-ttu-id="2669b-110">WpcSystemSettings (一個實例) </span><span class="sxs-lookup"><span data-stu-id="2669b-110">WpcSystemSettings (one instance)</span></span>
    -   <span data-ttu-id="2669b-111">AddUser () 和 RemoveUser () 方法，分別為指定的 SID 建立和刪除家長監護設定。</span><span class="sxs-lookup"><span data-stu-id="2669b-111">AddUser() and RemoveUser() methods to create and delete parental controls settings for a given SID, respectively.</span></span>
    -   <span data-ttu-id="2669b-112">系統會強制執行目前遊戲分級系統的屬性，以及與系統管理員檢查記錄相關的追蹤和通知。</span><span class="sxs-lookup"><span data-stu-id="2669b-112">Properties for current game ratings system in force, and tracking and notification related to admin checking of logs.</span></span>
    -   <span data-ttu-id="2669b-113">擴充性：唯讀和讀取/寫入 HTTP 應用程式的屬性，以及 web 內容篩選的 URL 豁免清單、Web 內容篩選覆寫識別碼和名稱資源 DLL 路徑與識別碼，以及自訂記錄檔事件的欄位和標頭名稱註冊數目。</span><span class="sxs-lookup"><span data-stu-id="2669b-113">Extensibility: Properties for read-only and read/write HTTP application and URL exemption lists for web content filtering, Web Content Filter override ID and name resource DLL path and ID, and custom log event number of fields and header name registration.</span></span>
-   <span data-ttu-id="2669b-114">WpcRatingsSystem (每個已安裝分級系統的一個實例) </span><span class="sxs-lookup"><span data-stu-id="2669b-114">WpcRatingsSystem (one instance per each ratings system installed)</span></span>
    -   <span data-ttu-id="2669b-115">WpcRating (每個評等層級) 的一個實例。</span><span class="sxs-lookup"><span data-stu-id="2669b-115">WpcRating (one instance per rating level).</span></span>
    -   <span data-ttu-id="2669b-116">WpcRatingDescriptor (每個評等描述項) 的一個實例。</span><span class="sxs-lookup"><span data-stu-id="2669b-116">WpcRatingDescriptor (one instance per rating descriptor).</span></span>
-   <span data-ttu-id="2669b-117">擴充性： WpcExtension (每個已新增) 的 [家長監護] 面板擴充性連結來一個實例。</span><span class="sxs-lookup"><span data-stu-id="2669b-117">Extensibility: WpcExtension (one instance per each Parental Controls Panel extensibility link added).</span></span>
    -   <span data-ttu-id="2669b-118">GUID、子系統、識別碼、映射資源路徑、停用狀態影像資源路徑、可執行檔路徑、顯示名稱資源 DLL 路徑和識別碼、子標題資源 DLL 路徑和識別碼的屬性。</span><span class="sxs-lookup"><span data-stu-id="2669b-118">Properties for GUID, subsystem, ID, image resource path, disabled state image resource path, executable path, display name resource DLL path and ID, subtitle resource DLL path and ID.</span></span>

<span data-ttu-id="2669b-119">每個控制的使用者：</span><span class="sxs-lookup"><span data-stu-id="2669b-119">Per-controlled user:</span></span>

-   <span data-ttu-id="2669b-120">WpcUserSettings (每個受控制使用者的一個實例) </span><span class="sxs-lookup"><span data-stu-id="2669b-120">WpcUserSettings (one instance per controlled user)</span></span>
    -   <span data-ttu-id="2669b-121">擁有 SID、家長監護 on/off 旗標、登入/關閉旗標、時間限制 on/off 旗標、覆寫啟用旗標、登入時間遮罩，以及一般應用程式限制 on/off 旗標的屬性。</span><span class="sxs-lookup"><span data-stu-id="2669b-121">Properties for owning SID, parental controls on/off flag, logging on/off flag, time limits on/off flag, overrides enabled flag, logon hours mask, and General Application Restrictions on/off flag.</span></span>
    -   <span data-ttu-id="2669b-122">在 Windows 8 現有的屬性工作表示每小時的前半小時。</span><span class="sxs-lookup"><span data-stu-id="2669b-122">In Windows 8 the existing property represents the first half-hour for each hour.</span></span> <span data-ttu-id="2669b-123">已加入新的半小時屬性來代表每個小時的後半部。</span><span class="sxs-lookup"><span data-stu-id="2669b-123">A new half-hour property has been added to represent the second half of each hour.</span></span> <span data-ttu-id="2669b-124">引進了額外的新屬性來表示每日額度。</span><span class="sxs-lookup"><span data-stu-id="2669b-124">An additional new property was introduced to represent daily time allowance.</span></span>

        <span data-ttu-id="2669b-125">**Windows 7 和 Windows Vista：** 計時器限制支援1小時的資料細微性。</span><span class="sxs-lookup"><span data-stu-id="2669b-125">**Windows 7 and Windows Vista:** Timer restrictions supported 1 hour granularity.</span></span>

-   <span data-ttu-id="2669b-126">WpcWebSettings (每個受控制使用者的一個實例) </span><span class="sxs-lookup"><span data-stu-id="2669b-126">WpcWebSettings (one instance per controlled user)</span></span>
    -   <span data-ttu-id="2669b-127">擁有 SID、篩選開啟/關閉旗標、篩選層級、檔案下載封鎖旗標、未分級的網站封鎖旗標的屬性。</span><span class="sxs-lookup"><span data-stu-id="2669b-127">Properties for owning SID, filter on/off flag, filter level, file downloads blocked flag, unrated sites blocked flag.</span></span>
-   <span data-ttu-id="2669b-128">WpcUrlOverride (在 URL 覆寫清單中明確允許或拒絕每個 URL 的一個實例，以做為 web 內容篩選的允許/封鎖清單) </span><span class="sxs-lookup"><span data-stu-id="2669b-128">WpcUrlOverride (one instance per URL explicitly allowed or denied in URL override list used as allow/block list for web content filtering)</span></span>
    -   <span data-ttu-id="2669b-129">擁有 SID、受影響的 URL、允許/封鎖狀態的屬性。</span><span class="sxs-lookup"><span data-stu-id="2669b-129">Properties for owning SID, URL affected, allowed/blocked state.</span></span>
-   <span data-ttu-id="2669b-130">WpcAppOverride (一般應用程式限制應用程式覆寫清單中明確允許的每個路徑一個實例) </span><span class="sxs-lookup"><span data-stu-id="2669b-130">WpcAppOverride (one instance per path explicitly allowed in General Application Restrictions application override list)</span></span>
    -   <span data-ttu-id="2669b-131">擁有 SID 的屬性。</span><span class="sxs-lookup"><span data-stu-id="2669b-131">Properties for owning SID.</span></span> <span data-ttu-id="2669b-132">更安全的規則識別碼、應用程式的路徑。</span><span class="sxs-lookup"><span data-stu-id="2669b-132">SAFER rule ID, path to application.</span></span>
-   <span data-ttu-id="2669b-133">WpcGamesSettings (每個受控制使用者的一個實例) </span><span class="sxs-lookup"><span data-stu-id="2669b-133">WpcGamesSettings (one instance per controlled user)</span></span>
    -   <span data-ttu-id="2669b-134">擁有 SID 的屬性、允許的遊戲旗標、這些設定的分級系統 GUID、允許未分級的遊戲旗標、目前系統下允許的最高評等識別碼、已拒絕的描述項集合。</span><span class="sxs-lookup"><span data-stu-id="2669b-134">Properties for owning SID, games permitted flag, GUID of ratings system for these settings, allow unrated games flag, ID of maximum allowed rating under current system, collection of denied descriptors.</span></span>
-   <span data-ttu-id="2669b-135">WpcGameOverride (明確允許或拒絕每個應用程式識別碼的一個實例) </span><span class="sxs-lookup"><span data-stu-id="2669b-135">WpcGameOverride (one instance per application ID explicitly allowed or denied)</span></span>
    -   <span data-ttu-id="2669b-136">擁有 SID、應用程式識別碼識別遊戲、允許/拒絕狀態的屬性。</span><span class="sxs-lookup"><span data-stu-id="2669b-136">Properties for owning SID, application ID identifying game, allowed/denied state.</span></span>

## <a name="data-representation-notes"></a><span data-ttu-id="2669b-137">資料表示注意事項</span><span class="sxs-lookup"><span data-stu-id="2669b-137">Data Representation Notes</span></span>

<span data-ttu-id="2669b-138">架構中的數個設定受限於屬性為非 null 的 mof 檔案 \_ 。</span><span class="sxs-lookup"><span data-stu-id="2669b-138">Several of the settings within the schema are constrained by the .mof file with attribute non\_null.</span></span> <span data-ttu-id="2669b-139">這些不能設定為 null 變異。</span><span class="sxs-lookup"><span data-stu-id="2669b-139">These cannot be set to a null variant.</span></span> <span data-ttu-id="2669b-140">針對所有非陣列類型，家長監護程式碼會初始化值。</span><span class="sxs-lookup"><span data-stu-id="2669b-140">For all non-array types, the Parental Controls code initializes values.</span></span> <span data-ttu-id="2669b-141">若為數組，可以使用 null variant、empty variant 或大小為零的 variant 陣列來寫入空白狀態。</span><span class="sxs-lookup"><span data-stu-id="2669b-141">For arrays, empty states may be written by using a null variant, empty variant, or zero-sized variant array.</span></span> <span data-ttu-id="2669b-142">WMI 提供者會在讀取時將所有這些值正規化為 null 變異狀態表示。</span><span class="sxs-lookup"><span data-stu-id="2669b-142">The WMI provider will normalize all of these to a null variant state representation on read.</span></span>

## <a name="user-interface-extensibility-link-notes"></a><span data-ttu-id="2669b-143">消費者介面擴充性連結注意事項</span><span class="sxs-lookup"><span data-stu-id="2669b-143">User Interface Extensibility Link Notes</span></span>

<span data-ttu-id="2669b-144">使用 WMI 註冊 UI 擴充性連結需要指定下列資訊：</span><span class="sxs-lookup"><span data-stu-id="2669b-144">Using WMI to register a UI extensibility link requires specifying the following information:</span></span>

-   <span data-ttu-id="2669b-145">GUID-如果是通用套件或套件的一部分，則多個連結可以共用相同的 GUID。</span><span class="sxs-lookup"><span data-stu-id="2669b-145">GUID - multiple links may share the same GUID if they are part of a common package or suite.</span></span>
-   <span data-ttu-id="2669b-146">子系統-用於表示連結類型的分類，例如套件或獨立相容的應用程式</span><span class="sxs-lookup"><span data-stu-id="2669b-146">Subsystem - intended to indicate classifications of link types, such as suites or standalone compliant applications</span></span>
-   <span data-ttu-id="2669b-147">名稱資源 DLL 路徑和識別碼-指定要為連結顯示之顯示名稱的資源。</span><span class="sxs-lookup"><span data-stu-id="2669b-147">Name resource DLL path and ID - specifies resource for display name to be displayed for the link.</span></span>
-   <span data-ttu-id="2669b-148">子標題資源 DLL 路徑和識別碼-指定資源，以取得名稱下方的其他文字。</span><span class="sxs-lookup"><span data-stu-id="2669b-148">Subtitle resource DLL path and ID - specifies resource for additional text below the name.</span></span>
-   <span data-ttu-id="2669b-149">影像路徑-24 ×24圖元點陣圖 (BMP) 的完整路徑，每圖元每圖元色深度，最好是 Alpha 色板。</span><span class="sxs-lookup"><span data-stu-id="2669b-149">Image path - full path of a 24 × 24 pixel bitmap (BMP), with 8 bits-per-pixel color depth and preferably an alpha channel.</span></span> <span data-ttu-id="2669b-150">這是以與 shell 擴充功能一致的方式來指定： <file system path> ， <negative resource ID> 。</span><span class="sxs-lookup"><span data-stu-id="2669b-150">This is specified in a manner consistent with shell extensions: <file system path>,<negative resource ID>.</span></span> <span data-ttu-id="2669b-151">例如： C： \\ Windows \\ System32 \\Wpccpl.dll，-20。</span><span class="sxs-lookup"><span data-stu-id="2669b-151">As an example: C:\\Windows\\System32\\Wpccpl.dll,-20.</span></span>
-   <span data-ttu-id="2669b-152">已停用的影像路徑-與上面的影像路徑相同，但顯示停用狀態的點陣圖變數除外。</span><span class="sxs-lookup"><span data-stu-id="2669b-152">Disabled image path - same as image path above, except variant of bitmap showing disabled state.</span></span> <span data-ttu-id="2669b-153">當家長監護關閉時，就會顯示此影像。</span><span class="sxs-lookup"><span data-stu-id="2669b-153">This image is shown when parental controls is off.</span></span>
-   <span data-ttu-id="2669b-154">Exe 路徑-要使用 ShellExecute () 叫用之可執行檔的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="2669b-154">Exe path - full path to an executable to be invoked by using ShellExecute().</span></span> <span data-ttu-id="2669b-155">此路徑必須以反斜線指定，否則連結不會叫用可執行檔。</span><span class="sxs-lookup"><span data-stu-id="2669b-155">This path must be specified with backslashes, or the link will not invoke the executable.</span></span> <span data-ttu-id="2669b-156">將% SID% 權杖新增至 exe 路徑之後，將會導致連結執行以 SID 字串取代目前正在查看其中樞頁面的使用者。</span><span class="sxs-lookup"><span data-stu-id="2669b-156">Addition of a %SID% token after the exe path will result in the link execution substituting the SID string for the user for which the hub page is currently being viewed.</span></span> <span data-ttu-id="2669b-157">然後，可執行檔會使用 SID 字串來管理指定使用者的功能。</span><span class="sxs-lookup"><span data-stu-id="2669b-157">The executable may then use the SID string to manage functionality for the specified user.</span></span>

<span data-ttu-id="2669b-158">應用程式卸載必須移除擴充性連結註冊。</span><span class="sxs-lookup"><span data-stu-id="2669b-158">Application uninstallation must remove an extensibility link registration.</span></span>

## <a name="web-extensibility-link-and-web-content-filter-override-notes"></a><span data-ttu-id="2669b-159">Web 擴充性連結和 Web 內容篩選覆寫附注</span><span class="sxs-lookup"><span data-stu-id="2669b-159">Web Extensibility Link and Web Content Filter Override Notes</span></span>

<span data-ttu-id="2669b-160">藉由將 FilterID 屬性設定為與現有註冊的 UI 擴充性連結相同的 GUID，顯示的連結將會從其他設定中的一般連結升級到專屬的 Web 限制連結。</span><span class="sxs-lookup"><span data-stu-id="2669b-160">By setting the FilterID property to the same GUID as an existing registered UI extensibility link, the link displayed will be promoted from a generic link in Other Settings to the exclusive Web Restrictions link.</span></span> <span data-ttu-id="2669b-161">這是全電腦的設定，因此會導致內建的 Web 內容篩選 LSP 略過所有受控制使用者的篩選。</span><span class="sxs-lookup"><span data-stu-id="2669b-161">This is a computer-wide setting, and so will cause the in-box Web Content Filter LSP to bypass all filtering for all controlled users.</span></span> <span data-ttu-id="2669b-162">您也應該在 FilterName 屬性中設定描述性名稱，這個屬性是由資源 DLL 和識別碼的路徑所指定。</span><span class="sxs-lookup"><span data-stu-id="2669b-162">A descriptive name should also be set in the FilterName property, which is specified by a path to resource DLL and ID.</span></span>

<span data-ttu-id="2669b-163">家長監護系統會從任何覆寫的網頁篩選器中建議下列內容：</span><span class="sxs-lookup"><span data-stu-id="2669b-163">The Parental Controls system recommends the following from any overriding web filter:</span></span>

-   <span data-ttu-id="2669b-164">接受使用者的整體家長監護開啟/關閉狀態。</span><span class="sxs-lookup"><span data-stu-id="2669b-164">Honor the overall Parental Controls on/off state for a user.</span></span>
-   <span data-ttu-id="2669b-165">接受使用者的活動報告設定。</span><span class="sxs-lookup"><span data-stu-id="2669b-165">Honor the Activity Reporting settings for a user.</span></span>
-   <span data-ttu-id="2669b-166">監視 FilterID 屬性。</span><span class="sxs-lookup"><span data-stu-id="2669b-166">Monitor the FilterID property.</span></span> <span data-ttu-id="2669b-167">如果從廠商的指定 GUID 變更，其他篩選器就會取得擁有權，而廠商的篩選器應該停用它本身。</span><span class="sxs-lookup"><span data-stu-id="2669b-167">If it changes from the vendor's specified GUID, another filter has taken ownership and the vendor's filter should disable itself.</span></span> <span data-ttu-id="2669b-168">已加入 COM 介面，以降低定期檢查這項變更與 WMI 呼叫的額外負荷。</span><span class="sxs-lookup"><span data-stu-id="2669b-168">A COM interface has been added to reduce the overhead of checking periodically for this change versus a WMI call.</span></span>
-   <span data-ttu-id="2669b-169">強烈建議您同時接受唯讀和讀取/寫入 HTTP 應用程式和 URL 豁免清單專案。</span><span class="sxs-lookup"><span data-stu-id="2669b-169">Highly recommended to honor both the read-only and read/write HTTP application and URL exemption list entries.</span></span>
-   <span data-ttu-id="2669b-170">建議接受每位使用者的 URL 覆寫清單 (允許/封鎖清單) 。</span><span class="sxs-lookup"><span data-stu-id="2669b-170">Recommended to honor the per-user URL override list (allow/block list).</span></span>
-   <span data-ttu-id="2669b-171">很健全，可快速切換使用者。</span><span class="sxs-lookup"><span data-stu-id="2669b-171">Be robust to fast user switching.</span></span>

<span data-ttu-id="2669b-172">家長監護不會限制 web 或其他內容篩選器如何插入 Windows 以進行篩選。</span><span class="sxs-lookup"><span data-stu-id="2669b-172">Parental Controls does not place any limitations on how a web or other content filter plugs in to Windows for implementing filtering.</span></span> <span data-ttu-id="2669b-173">廠商可能會利用其目前的投資或慣用技術 (LSP、TDI、其他) 。</span><span class="sxs-lookup"><span data-stu-id="2669b-173">Vendors may leverage their current investments or preferred technologies (LSP, TDI, other).</span></span>

<span data-ttu-id="2669b-174">卸載廠商的篩選準則時，必須取消註冊 FilterID 和 FilterName 專案。</span><span class="sxs-lookup"><span data-stu-id="2669b-174">Uninstallation of the vendor's filter must unregister the FilterID and FilterName entries.</span></span> <span data-ttu-id="2669b-175">這是藉由將 FilterID 設定為 GUID \_ null，並將 FilterName 設定為 variant null 來執行。</span><span class="sxs-lookup"><span data-stu-id="2669b-175">This is performed by setting FilterID to GUID\_NULL and FilterName to a variant null.</span></span> <span data-ttu-id="2669b-176">然後會重新啟用內建的 web 內容篩選器。</span><span class="sxs-lookup"><span data-stu-id="2669b-176">The in-box web content filter will then be re-enabled.</span></span>

<span data-ttu-id="2669b-177">請注意，重新啟用內建的網頁篩選器只會篩選新的會話，而不會篩選切換之前的作用中會話。</span><span class="sxs-lookup"><span data-stu-id="2669b-177">Note that re-enabling of the in-box web filter will only filter new sessions, and not sessions active from before the switch.</span></span>

## <a name="web-content-filter-allowblock-list-exportimport-format"></a><span data-ttu-id="2669b-178">Web 內容篩選允許/封鎖清單匯出/匯入格式</span><span class="sxs-lookup"><span data-stu-id="2669b-178">Web Content Filter Allow/Block List Export/Import Format</span></span>

<span data-ttu-id="2669b-179">Windows 8 不支援這項功能。</span><span class="sxs-lookup"><span data-stu-id="2669b-179">This feature is not supported on Windows 8.</span></span>

<span data-ttu-id="2669b-180">**Windows 7 和 Windows Vista：** 支援這項功能。</span><span class="sxs-lookup"><span data-stu-id="2669b-180">**Windows 7 and Windows Vista:** This feature is supported.</span></span>

<WebAddresses>

<URL AllowBlock="1">https://alloweddomain.com/</URL>

<URL AllowBlock="1">https://allowedurl.com/allowed/default.html</URL>

<URL AllowBlock="2">https://blockeddomain.com/</URL>

<URL AllowBlock="2">https://blockedurl.com/blocked/default.html</URL>

</WebAddresses>

## <a name="application-restrictions-override-notes"></a><span data-ttu-id="2669b-181">應用程式限制覆寫附注</span><span class="sxs-lookup"><span data-stu-id="2669b-181">Application Restrictions Override Notes</span></span>

<span data-ttu-id="2669b-182">應用程式限制覆寫是以每個使用者為基礎來設定，以允許特定的二進位檔或路徑。</span><span class="sxs-lookup"><span data-stu-id="2669b-182">Application restrictions overrides are set on a per user basis to allow specific binaries or paths.</span></span> <span data-ttu-id="2669b-183">如果已設定新的 parentally 控制使用者，且該使用者需要應用程式限制覆寫，建議您將登錄中的 Windows Run 機碼與標示為需要提高許可權的小型應用程式搭配使用，以寫入覆寫。</span><span class="sxs-lookup"><span data-stu-id="2669b-183">If a new parentally controlled user is configured and application restrictions overrides are needed for that user, it is recommended that the Windows Run key in the registry be used with a small application marked as requiring elevation deployed to write the overrides.</span></span> <span data-ttu-id="2669b-184">這將會產生一次性的認證提示，以設定使用者的覆寫，之後覆寫的目標二進位檔將不會對使用者造成干擾，因為會有進一步的系統管理員覆寫提示。</span><span class="sxs-lookup"><span data-stu-id="2669b-184">This will result in a one-time credentials prompt to configure the overrides for the user, after which the target binaries for the overrides will not be a nuisance to users due to further administrator override prompts.</span></span>

## <a name="actions-required-for-settings-changes-to-become-effective"></a><span data-ttu-id="2669b-185">設定變更生效所需的動作</span><span class="sxs-lookup"><span data-stu-id="2669b-185">Actions Required for Settings Changes to Become Effective</span></span>

<span data-ttu-id="2669b-186">如果系統管理員變更已登入標準使用者的設定，則會產生警告訊息。</span><span class="sxs-lookup"><span data-stu-id="2669b-186">If an Administrator changes settings for a logged-in standard user, a warning message is generated.</span></span> <span data-ttu-id="2669b-187">這表示在受控制的使用者登出後重新登入之前，設定變更可能不會生效。</span><span class="sxs-lookup"><span data-stu-id="2669b-187">It states the settings changes may not take effect until the controlled user logs out and back in again.</span></span> <span data-ttu-id="2669b-188">這是保守的設計。</span><span class="sxs-lookup"><span data-stu-id="2669b-188">This is conservative design.</span></span> <span data-ttu-id="2669b-189">當受控制的使用者登入時，大部分的設定幾乎會立即生效。</span><span class="sxs-lookup"><span data-stu-id="2669b-189">Most settings will take effect nearly immediately while the controlled user is logged in.</span></span> <span data-ttu-id="2669b-190">其中一個例外狀況是遊戲，在下一次執行遊戲瀏覽器或叫用遊戲時，設定將會生效。</span><span class="sxs-lookup"><span data-stu-id="2669b-190">One exception is for games, where settings will take effect the next time the Games Explorer is run or invoking the game is attempted.</span></span>

## <a name="sample-code"></a><span data-ttu-id="2669b-191">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="2669b-191">Sample code</span></span>

<span data-ttu-id="2669b-192">SDK 中提供的 c + + 範例會示範設定擴充功能的使用方式。</span><span class="sxs-lookup"><span data-stu-id="2669b-192">C++ samples are provided in the SDK demonstrating use of the settings extensibility features.</span></span> <span data-ttu-id="2669b-193">請參閱家長監護範例一節。</span><span class="sxs-lookup"><span data-stu-id="2669b-193">Please see the Parental Controls Samples section.</span></span>

## <a name="independent-test-tools"></a><span data-ttu-id="2669b-194">獨立測試工具</span><span class="sxs-lookup"><span data-stu-id="2669b-194">Independent Test Tools</span></span>

<span data-ttu-id="2669b-195">Wmimgmt.msc services.msc 外掛程式和 Wbemtest.exe 工具可促進類別和實例的檢查。</span><span class="sxs-lookup"><span data-stu-id="2669b-195">Inspection of classes and instances is facilitated by the Wmimgmt.msc plug-in and the Wbemtest.exe tool.</span></span>

## <a name="64-bit-considerations"></a><span data-ttu-id="2669b-196">64位考慮</span><span class="sxs-lookup"><span data-stu-id="2669b-196">64-Bit Considerations</span></span>

<span data-ttu-id="2669b-197">64位 Windows 作業系統版本目前已安裝32位 WMI 提供者和64位提供者。</span><span class="sxs-lookup"><span data-stu-id="2669b-197">64-bit Windows operating system versions currently have both a 32-bit WMI provider and a 64-bit provider installed.</span></span>

## <a name="general-code-development-and-debugging"></a><span data-ttu-id="2669b-198">一般程式碼開發和偵錯工具</span><span class="sxs-lookup"><span data-stu-id="2669b-198">General Code Development and Debugging</span></span>

<span data-ttu-id="2669b-199">如果 Visual Studio 用於設定管理程式碼開發，本機的偵錯工具將需要以系統管理員許可權執行 Visual Studio， (使用命令列或右鍵選項) 叫用 [以系統管理員身分執行]。</span><span class="sxs-lookup"><span data-stu-id="2669b-199">If Visual Studio is used for settings management code development, local debugging will require running Visual Studio with administrator rights (invoking with Run as Administrator using command line or right-click option).</span></span> <span data-ttu-id="2669b-200">這是由 UAC 所實行的進程和訊息隔離所致。</span><span class="sxs-lookup"><span data-stu-id="2669b-200">This is due to process and message isolation implemented by UAC.</span></span>

## <a name="minimum-compliance-api-settings-read"></a><span data-ttu-id="2669b-201">讀取的最小合規性 API 設定</span><span class="sxs-lookup"><span data-stu-id="2669b-201">Minimum Compliance API Settings Read</span></span>

### <a name="interfaces-and-methods"></a><span data-ttu-id="2669b-202">介面和方法</span><span class="sxs-lookup"><span data-stu-id="2669b-202">Interfaces and Methods</span></span>

<span data-ttu-id="2669b-203">標頭檔 Wpcapi 所控制的合規性 API 可使用 COM 介面，提供下列設定的簡化唯讀存取。</span><span class="sxs-lookup"><span data-stu-id="2669b-203">The Compliance API controlled by header file Wpcapi.h provides simplified read-only access to the following settings by using COM interfaces.</span></span>

<span data-ttu-id="2669b-204">[**IWindowsParentalControls**](/windows/desktop/api/Wpcapi/nn-wpcapi-iwindowsparentalcontrols) 根介面方法可讓您存取：</span><span class="sxs-lookup"><span data-stu-id="2669b-204">[**IWindowsParentalControls**](/windows/desktop/api/Wpcapi/nn-wpcapi-iwindowsparentalcontrols) root interface methods provide access to:</span></span>

-   <span data-ttu-id="2669b-205">IWPCSettings 方法：</span><span class="sxs-lookup"><span data-stu-id="2669b-205">IWPCSettings methods:</span></span>
    -   <span data-ttu-id="2669b-206">IsLoggingRequired () -是否已為使用者將活動報告設定為 on？</span><span class="sxs-lookup"><span data-stu-id="2669b-206">IsLoggingRequired()—is activity reporting configured as on for the user?</span></span>
    -   <span data-ttu-id="2669b-207">GetLastSettingsChangeTime () —應用程式可以知道是否有任何設定原則在先前的檢查之後變更。</span><span class="sxs-lookup"><span data-stu-id="2669b-207">GetLastSettingsChangeTime()—application can be aware if any settings policies have changed since a previous check.</span></span>
    -   <span data-ttu-id="2669b-208">GetRestrictions () —閱讀 web 限制、時間限制、遊戲限制或應用程式限制是否設定為 on。</span><span class="sxs-lookup"><span data-stu-id="2669b-208">GetRestrictions()—read whether web restrictions, time limits, game restrictions, or application restrictions are set to on.</span></span>
-   <span data-ttu-id="2669b-209">IWPCWebSettings 方法：</span><span class="sxs-lookup"><span data-stu-id="2669b-209">IWPCWebSettings methods:</span></span>
    -   <span data-ttu-id="2669b-210">GetSettings () –抓取或關閉篩選的旗標，並封鎖下載。</span><span class="sxs-lookup"><span data-stu-id="2669b-210">GetSettings()– retrieves flags for filter on or off and downloads blocked.</span></span>
    -   <span data-ttu-id="2669b-211">RequestURLOverride () -將要求輸入至系統管理員覆寫 (過度使用的核准) 機制，以顯示包含要核准之 Url 的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="2669b-211">RequestURLOverride()—input a request into the administrator override (over-the-shoulder approval) mechanism that will present a dialog box that contains the URLs to be approved.</span></span>
-   <span data-ttu-id="2669b-212">IWPCGamesSettings 方法：</span><span class="sxs-lookup"><span data-stu-id="2669b-212">IWPCGamesSettings methods:</span></span>
    -   <span data-ttu-id="2669b-213">IsBlocked () —針對指定的遊戲應用程式識別碼，這是由家長監護封鎖的遊戲，以及原因。</span><span class="sxs-lookup"><span data-stu-id="2669b-213">IsBlocked()—for a given game application ID, is the game blocked by parental controls and for what reason.</span></span>
-   <span data-ttu-id="2669b-214">GetVisibility () ：提供是否目前隱藏家長監護 UI 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2669b-214">GetVisibility()—provides information on whether the Parental Controls UI is currently hidden.</span></span>
-   <span data-ttu-id="2669b-215">GetWebFilterInfo () ：提供介面來取得目前使用中 Web 內容篩選器的識別碼。</span><span class="sxs-lookup"><span data-stu-id="2669b-215">GetWebFilterInfo()—provides an interface for obtaining the ID of the currently active Web Content Filter.</span></span>

### <a name="sample-code"></a><span data-ttu-id="2669b-216">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="2669b-216">Sample code</span></span>

<span data-ttu-id="2669b-217">SDK 中提供的 c + + 範例會示範如何使用合規性 API。</span><span class="sxs-lookup"><span data-stu-id="2669b-217">C++ samples are provided in the SDK demonstrating use of the Compliance API.</span></span> <span data-ttu-id="2669b-218">請參閱家長監護範例一節。</span><span class="sxs-lookup"><span data-stu-id="2669b-218">Please see the Parental Controls Samples section.</span></span>

 

 




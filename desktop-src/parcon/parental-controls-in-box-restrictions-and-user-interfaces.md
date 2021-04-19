---
description: 提供數個限制的實現。
ms.assetid: a00d9a3a-d052-492c-b9e7-3ecb1455a392
title: 家長監護 & 使用者介面 In-Box 限制
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e5f155f8323fd6b006e510d75865ea25e278c70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980044"
---
# <a name="parental-controls-in-box-restrictions--user-interfaces"></a><span data-ttu-id="e5817-103">家長監護 & 使用者介面 In-Box 限制</span><span class="sxs-lookup"><span data-stu-id="e5817-103">Parental Controls In-Box Restrictions & User Interfaces</span></span>

<span data-ttu-id="e5817-104">提供數個限制的實現。</span><span class="sxs-lookup"><span data-stu-id="e5817-104">Several restrictions implementations are provided.</span></span>

-   [<span data-ttu-id="e5817-105">Web 限制</span><span class="sxs-lookup"><span data-stu-id="e5817-105">Web Restrictions</span></span>](#web-restrictions)
-   [<span data-ttu-id="e5817-106">時間限制</span><span class="sxs-lookup"><span data-stu-id="e5817-106">Time Limits</span></span>](#time-limits)
-   [<span data-ttu-id="e5817-107">遊戲</span><span class="sxs-lookup"><span data-stu-id="e5817-107">Games</span></span>](#games)
-   [<span data-ttu-id="e5817-108">允許和封鎖特定程式</span><span class="sxs-lookup"><span data-stu-id="e5817-108">Allow and Block Specific Programs</span></span>](#allow-and-block-specific-programs)

## <a name="web-restrictions"></a><span data-ttu-id="e5817-109">Web 限制</span><span class="sxs-lookup"><span data-stu-id="e5817-109">Web Restrictions</span></span>

-   <span data-ttu-id="e5817-110">使用免費動態評等服務的現成 Web 內容篩選器。</span><span class="sxs-lookup"><span data-stu-id="e5817-110">In-box Web Content Filter using a free dynamic rating service.</span></span> <span data-ttu-id="e5817-111">可個別設定每個受控制的使用者。</span><span class="sxs-lookup"><span data-stu-id="e5817-111">Individually configurable per controlled user.</span></span>
-   <span data-ttu-id="e5817-112">會在啟用時篩選所有 HTTP 流量，如果遭到封鎖，則會傳回自訂格式的頁面。</span><span class="sxs-lookup"><span data-stu-id="e5817-112">Filters all HTTP traffic when enabled, returns custom formatted page if blocked.</span></span> <span data-ttu-id="e5817-113">可接受所有主要瀏覽器的功能。</span><span class="sxs-lookup"><span data-stu-id="e5817-113">Allows acceptable functionality with all major browsers.</span></span> <span data-ttu-id="e5817-114">藉由監視頁面的所有 HTTP Get 和 Post 要求，可讓個別網頁元件遭到封鎖。</span><span class="sxs-lookup"><span data-stu-id="e5817-114">By monitoring all HTTP Get and Post requests for a page, allows individual webpage parts to be blocked.</span></span>
-   <span data-ttu-id="e5817-115">您可以使用允許或封鎖 URL 清單、簡化分級分類預設值的使用者介面，或 12 + 類別的 ActiveX 控制項，以及封鎖檔案下載的原則，來進行高度可設定。</span><span class="sxs-lookup"><span data-stu-id="e5817-115">Highly configurable by using user interface that allows or blocks URL lists, simplified rating category presets, or ActiveX control of 12+ categories, as well as a policy for blocking file downloads.</span></span>

> [!Note]  
> <span data-ttu-id="e5817-116">實際的檔案下載封鎖需要應用程式執行限制，並遵循所提供的設定。</span><span class="sxs-lookup"><span data-stu-id="e5817-116">Actual file download blocking requires applications to implement the restriction, complying with the provided setting.</span></span>

 

-   <span data-ttu-id="e5817-117">實作為 Windows 篩選平台 (WFP) 驅動程式與在使用者會話中執行的家庭安全監視程式進行通訊。</span><span class="sxs-lookup"><span data-stu-id="e5817-117">Implemented as a Windows Filtering Platform (WFP) driver communicating with the Family Safety monitoring process running in the users' sessions.</span></span> <span data-ttu-id="e5817-118">執行已從多層式服務提供者變更 (LSP) 篩選至 Windows 篩選平台 (WFP) 驅動程式與使用者會話中執行的家庭安全監視程式進行通訊。</span><span class="sxs-lookup"><span data-stu-id="e5817-118">Implementation has changed from a Layered Service Provider (LSP) filter to a Windows Filtering Platform (WFP) driver communicating with the Family Safety monitoring process running in the users' sessions.</span></span>

    <span data-ttu-id="e5817-119">**Windows 7 和 Windows Vista：** 實作為多層式服務提供者 (LSP) 篩選與低許可權服務進行通訊，以進行整體的管理和監視。</span><span class="sxs-lookup"><span data-stu-id="e5817-119">**Windows 7 and Windows Vista:** Implemented as a Layered Service Provider (LSP) filter communicating with a low-rights service for overall management and monitoring.</span></span> <span data-ttu-id="e5817-120">當停用時，篩選會保留在 LSP 鏈中，但會通過所有流量。</span><span class="sxs-lookup"><span data-stu-id="e5817-120">The filter remains in the LSP chain when disabled, but passes all traffic through.</span></span> <span data-ttu-id="e5817-121">只有列出的作業系統才支援此執行。</span><span class="sxs-lookup"><span data-stu-id="e5817-121">This implementation is supported only for the operating systems listed.</span></span>

-   <span data-ttu-id="e5817-122">應用程式可能會提供使用者介面來顯示部分頁面封鎖，並接受原則來封鎖檔案下載。</span><span class="sxs-lookup"><span data-stu-id="e5817-122">Applications may provide user interface to show partial page blocking and honor the policy to block file downloads.</span></span> <span data-ttu-id="e5817-123">他們也可以叫用 API，讓使用者可以要求許可權來查看已封鎖的頁面。</span><span class="sxs-lookup"><span data-stu-id="e5817-123">They may also invoke an API to allow the user to request permission to view a blocked page.</span></span> <span data-ttu-id="e5817-124">此系統管理覆寫會叫用小型應用程式，以顯示已嘗試的 Url，並要求認證以允許它們。</span><span class="sxs-lookup"><span data-stu-id="e5817-124">This administrative override invokes a small application that shows the attempted URLs and that requests credentials to allow them.</span></span>
-   <span data-ttu-id="e5817-125">當應用程式需要註冊來略過篩選，或一律允許特定的 Url 時，會提供 API 給您的特殊情況。</span><span class="sxs-lookup"><span data-stu-id="e5817-125">An API is provided for special cases where an application needs to register to bypass filtering, or specific URLs are to be always allowed.</span></span>
-   <span data-ttu-id="e5817-126">由於一次只能執行一個 Web 內容篩選，因此協力廠商可能會註冊成為作用中篩選，並停用內建篩選準則。</span><span class="sxs-lookup"><span data-stu-id="e5817-126">Because only one Web Content Filter should ever be running at a time, third parties may register as the active filter and disable the in-box filter.</span></span> <span data-ttu-id="e5817-127">此擴充性結合了在 UI 中顯示協力廠商篩選的功能，可讓您進行簡單的取代。</span><span class="sxs-lookup"><span data-stu-id="e5817-127">This extensibility, coupled with the ability to show a third-party filter in the UI, allows for simple replacement.</span></span> <span data-ttu-id="e5817-128">篩選準則必須在卸載時移除其註冊。</span><span class="sxs-lookup"><span data-stu-id="e5817-128">Filters must remove their registration when uninstalled.</span></span>

## <a name="time-limits"></a><span data-ttu-id="e5817-129">時間限制</span><span class="sxs-lookup"><span data-stu-id="e5817-129">Time Limits</span></span>

-   <span data-ttu-id="e5817-130">內建的時間限制已增強，可讓您控制電腦可用的總時間量 (時間額度) 除了能夠控制電腦可用的時間之外，還可以在舊版 Windows 中使用 (curfew) 。</span><span class="sxs-lookup"><span data-stu-id="e5817-130">The in-box time restrictions were enhanced by providing ability to control total amount of time per day computer can be used (time allowance) in addition to ability to control times when computer can be used (curfew) which was available in previous versions of Windows.</span></span>
-   <span data-ttu-id="e5817-131">適用于 curfew 的 UI 可讓您在一周的每一天進行獨立控制，並提供半小時的資料細微性</span><span class="sxs-lookup"><span data-stu-id="e5817-131">UI for curfew allows independent control for each day of the week with half-hour granularity</span></span>
-   <span data-ttu-id="e5817-132">時間額度的 UI 可讓您在一周中的每一天進行工作日和週末的控制，或使用15分鐘的資料細微性進行獨立控制</span><span class="sxs-lookup"><span data-stu-id="e5817-132">UI for time allowance allows controls for weekdays and weekends or independent control for each day of the week with 15 minute granularity</span></span>
-   <span data-ttu-id="e5817-133">在封鎖的時間週期內，快速使用者切換 (FUS) 機制不再用來強制鎖定或封鎖受控制使用者的登入。</span><span class="sxs-lookup"><span data-stu-id="e5817-133">Fast User Switch (FUS) mechanism is no longer used to forcibly lock out or block login of the controlled user when in blocked time period.</span></span> <span data-ttu-id="e5817-134">切換至不同的桌面會用於這些用途。</span><span class="sxs-lookup"><span data-stu-id="e5817-134">A switch to a separate desktop is used for these purposes.</span></span> <span data-ttu-id="e5817-135">請注意，FUS 會在鎖定時保留使用者的狀態。</span><span class="sxs-lookup"><span data-stu-id="e5817-135">Note that the FUS does preserve the state of the user when locked out.</span></span>

## <a name="games"></a><span data-ttu-id="e5817-136">遊戲</span><span class="sxs-lookup"><span data-stu-id="e5817-136">Games</span></span>

-   <span data-ttu-id="e5817-137">與遊戲瀏覽器搭配運作。</span><span class="sxs-lookup"><span data-stu-id="e5817-137">Works in conjunction with the Games Explorer.</span></span>
-   <span data-ttu-id="e5817-138">可讓系統管理員控制哪些遊戲可透過豐富的 UI 來播放，以選取遊戲分級系統和層級 (加描述項（如果有的話）) ，以及/或明確允許或封鎖標題。</span><span class="sxs-lookup"><span data-stu-id="e5817-138">Allows administrators to control which games may be played through a rich UI for selecting a games ratings system and level (plus descriptors if present), and/or by specifically allowing or blocking titles.</span></span>
-   <span data-ttu-id="e5817-139">遊戲分級的中繼資料是以下列兩種方式之一來取得：</span><span class="sxs-lookup"><span data-stu-id="e5817-139">Metadata on games ratings are obtained in one of two ways:</span></span>
    -   <span data-ttu-id="e5817-140">支援的標題會將自己的遊戲定義檔案部署 (GDFs) 。</span><span class="sxs-lookup"><span data-stu-id="e5817-140">Supported titles deploy their own Game Definition Files (GDFs).</span></span>
    -   <span data-ttu-id="e5817-141">現成的資料庫涵蓋大約2000個舊版的標題。</span><span class="sxs-lookup"><span data-stu-id="e5817-141">Approximately 2000 legacy titles are covered by an in-box database.</span></span>
-   <span data-ttu-id="e5817-142">有三種機制可用於強制執行：</span><span class="sxs-lookup"><span data-stu-id="e5817-142">Three mechanisms are used for enforcement:</span></span>
    -   <span data-ttu-id="e5817-143">拒絕控制使用者對遊戲資料夾的寫入權限 Acl。</span><span class="sxs-lookup"><span data-stu-id="e5817-143">Deny ACLs for controlled user write access to the game folder.</span></span>
    -   <span data-ttu-id="e5817-144">使用應用程式相容性填充碼技術處理舊版標題的程式。</span><span class="sxs-lookup"><span data-stu-id="e5817-144">Process termination for legacy titles using application compatibility shim technology.</span></span>
    -   <span data-ttu-id="e5817-145">由支援的標題進行的自我檢查 API 使用，以封鎖執行。</span><span class="sxs-lookup"><span data-stu-id="e5817-145">Self-check API use by supported titles to block run.</span></span>
-   <span data-ttu-id="e5817-146">建議您知道上一節所述的時間限制事件。</span><span class="sxs-lookup"><span data-stu-id="e5817-146">Awareness of Time Limits events explained in the section above is recommended.</span></span>
-   <span data-ttu-id="e5817-147">GDFs 和遊戲瀏覽器的檔主要是透過 DirectX SDK 版本來提供。</span><span class="sxs-lookup"><span data-stu-id="e5817-147">Documentation for GDFs and the Games Explorer will be provided primarily through DirectX SDK releases.</span></span>

## <a name="allow-and-block-specific-programs"></a><span data-ttu-id="e5817-148">允許和封鎖特定程式</span><span class="sxs-lookup"><span data-stu-id="e5817-148">Allow and Block Specific Programs</span></span>

-   <span data-ttu-id="e5817-149">也稱為 (GAR) 的一般應用程式限制。</span><span class="sxs-lookup"><span data-stu-id="e5817-149">Also referred to as General Application Restrictions (GAR).</span></span>
-   <span data-ttu-id="e5817-150">預設為關閉狀態。</span><span class="sxs-lookup"><span data-stu-id="e5817-150">Off by default.</span></span> <span data-ttu-id="e5817-151">如果開啟，它只允許受控制的使用者執行系統管理員核准的應用程式，並具有合理的例外狀況。</span><span class="sxs-lookup"><span data-stu-id="e5817-151">If turned on, it only allows a controlled user to run applications approved by an administrator, with reasonable exceptions.</span></span>
-   <span data-ttu-id="e5817-152">UI 提供具有對應路徑的程式名稱清單，每個名稱都有一個 [允許] 核取方塊。</span><span class="sxs-lookup"><span data-stu-id="e5817-152">UI provides a list of program names with corresponding paths, each with an allow checkbox.</span></span> <span data-ttu-id="e5817-153">也會提供 [流覽] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="e5817-153">A browse button is also provided.</span></span>
-   <span data-ttu-id="e5817-154">使用軟體限制原則來實行 (SRP) ，也稱為更安全：</span><span class="sxs-lookup"><span data-stu-id="e5817-154">Implemented using Software Restriction Policies (SRP), also known as SAFER:</span></span>
    -   <span data-ttu-id="e5817-155">防止 (USB 金鑰、磁片等) 的所有媒體執行。</span><span class="sxs-lookup"><span data-stu-id="e5817-155">Prevents execution from all media (USB keys, floppy disks, and so on).</span></span>
    -   <span data-ttu-id="e5817-156">使用路徑規則來指定允許執行的程式。</span><span class="sxs-lookup"><span data-stu-id="e5817-156">Uses path rules to specify programs allowed to run.</span></span>
    -   <span data-ttu-id="e5817-157">NTFS ACL 寫入權限會從受控制的使用者可執行檔任何作業撤銷。</span><span class="sxs-lookup"><span data-stu-id="e5817-157">NTFS ACL write permissions are revoked from anything allowed for the controlled user to run.</span></span>
    -   <span data-ttu-id="e5817-158">如果已封鎖，之後又覆寫為 [允許]，則必須手動 relaunched 應用程式。</span><span class="sxs-lookup"><span data-stu-id="e5817-158">If blocked and subsequently overridden to allow, the application must be relaunched manually.</span></span>
-   <span data-ttu-id="e5817-159">例外狀況包括：</span><span class="sxs-lookup"><span data-stu-id="e5817-159">Exceptions include:</span></span>
    -   <span data-ttu-id="e5817-160">要運作的基本 Windows 子集所需的所有二進位檔。</span><span class="sxs-lookup"><span data-stu-id="e5817-160">All binaries required for a basic subset of Windows to function.</span></span>
    -   <span data-ttu-id="e5817-161">使用 API 註冊的所有可執行檔都可供指定的使用者使用。</span><span class="sxs-lookup"><span data-stu-id="e5817-161">All executable files that register by using an API are to be allowed for a given user.</span></span>
    -   <span data-ttu-id="e5817-162">遊戲限制下所指定為允許的遊戲。</span><span class="sxs-lookup"><span data-stu-id="e5817-162">Games specified as being allowed under Games Restrictions.</span></span>
-   <span data-ttu-id="e5817-163">請注意，當 GAR 為 on 時，會針對使用者的設計封鎖 RunAs 命令。</span><span class="sxs-lookup"><span data-stu-id="e5817-163">Note that the RunAs command is blocked by design for a user when GAR is on.</span></span>

 

 




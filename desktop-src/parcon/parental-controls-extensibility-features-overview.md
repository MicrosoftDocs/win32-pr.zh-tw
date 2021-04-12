---
description: 您可以使用設定和記錄 Api 來擴充家長監護。
ms.assetid: f0fc1b11-6de4-48f6-afc9-f05c8812d2bd
title: 家長監護擴充功能總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fe150c5955881b8038cdca9a1e4562ee28093f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320619"
---
# <a name="parental-controls-extensibility-features-overview"></a><span data-ttu-id="2f497-103">家長監護擴充功能總覽</span><span class="sxs-lookup"><span data-stu-id="2f497-103">Parental Controls Extensibility Features Overview</span></span>

<span data-ttu-id="2f497-104">您可以使用設定和記錄 Api 來擴充家長監護。</span><span class="sxs-lookup"><span data-stu-id="2f497-104">Parental controls can be extended by using the settings and logging APIs.</span></span>

-   [<span data-ttu-id="2f497-105">記錄-背景</span><span class="sxs-lookup"><span data-stu-id="2f497-105">Logging—Background</span></span>](/windows)
-   [<span data-ttu-id="2f497-106">記錄延伸</span><span class="sxs-lookup"><span data-stu-id="2f497-106">Logging Extensibility</span></span>](#logging-extensibility)
-   [<span data-ttu-id="2f497-107">父控制項面板一般 UI 擴充性連結新增</span><span class="sxs-lookup"><span data-stu-id="2f497-107">Parental Controls Panel General UI Extensibility Link Addition</span></span>](#parental-controls-panel-general-ui-extensibility-link-addition)
-   [<span data-ttu-id="2f497-108">取代網路內容篩選</span><span class="sxs-lookup"><span data-stu-id="2f497-108">Web Content Filter Replacement</span></span>](#web-content-filter-replacement)

## <a name="loggingbackground"></a><span data-ttu-id="2f497-109">記錄-背景</span><span class="sxs-lookup"><span data-stu-id="2f497-109">Logging—Background</span></span>

<span data-ttu-id="2f497-110">Microsoft 已定義一些標準事件來解決常見的活動：</span><span class="sxs-lookup"><span data-stu-id="2f497-110">Microsoft has defined a number of standard events to address common activities:</span></span>

-   <span data-ttu-id="2f497-111">System：家長監護設定變更、帳戶變更、系統時鐘變更、失敗的登入嘗試。</span><span class="sxs-lookup"><span data-stu-id="2f497-111">System: parental controls settings changes, account changes, system clock change, failed logon attempts.</span></span>
-   <span data-ttu-id="2f497-112">使用者：</span><span class="sxs-lookup"><span data-stu-id="2f497-112">User:</span></span>
    -   <span data-ttu-id="2f497-113">系統/時間限制：登入時間、登出、應用程式執行嘗試和應用程式執行持續時間 (請參閱) 的附注。</span><span class="sxs-lookup"><span data-stu-id="2f497-113">System/time limits: logon times, logout, application run attempts, and application run duration (see note).</span></span>
    -   <span data-ttu-id="2f497-114">Web 限制：已造訪和封鎖網站，檔案下載嘗試。</span><span class="sxs-lookup"><span data-stu-id="2f497-114">Web restrictions: websites visited and blocked, file download attempts.</span></span> <span data-ttu-id="2f497-115">Web 瀏覽器和類似瀏覽器的應用程式不需要記錄這些，因為 Web 內容篩選器會執行這項操作。</span><span class="sxs-lookup"><span data-stu-id="2f497-115">Web browsers and browser-like applications do not need to log these, as the Web Content Filter LSP does so.</span></span> <span data-ttu-id="2f497-116">取代的網頁篩選器需要產生這些事件。</span><span class="sxs-lookup"><span data-stu-id="2f497-116">Replacement web filters would need to generate these events.</span></span>
    -   <span data-ttu-id="2f497-117">遊戲：遊戲的遊戲和封鎖、遊戲結束 (事件，以及提供) 播放的持續時間。</span><span class="sxs-lookup"><span data-stu-id="2f497-117">Games: games played and blocked, game end (events together provide duration played).</span></span>
    -   <span data-ttu-id="2f497-118">允許和封鎖特定程式：執行嘗試、關機、受一般應用程式限制封鎖。</span><span class="sxs-lookup"><span data-stu-id="2f497-118">Allow and block specific programs: run attempt, shutdown, blocked by General Application Restrictions.</span></span>
    -   <span data-ttu-id="2f497-119">立即訊息：轉換初始嘗試、對話聯結嘗試、對話離開、影片/音訊/遊戲/短訊息服務/檔案傳輸/URL 交換功能、連絡人清單變更嘗試。</span><span class="sxs-lookup"><span data-stu-id="2f497-119">Instant Messaging: conversion initiation attempt, conversation join attempt, conversation leave, video/audio/game/short message service/file transfer/URL swap feature, contact list change attempt.</span></span>
    -   <span data-ttu-id="2f497-120">電子郵件：已接收或接收封鎖、傳送嘗試、連絡人清單變更嘗試。</span><span class="sxs-lookup"><span data-stu-id="2f497-120">Email: received or receive blocked, send attempt, contact list change attempt.</span></span>
    -   <span data-ttu-id="2f497-121">媒體：媒體已播放並嘗試。</span><span class="sxs-lookup"><span data-stu-id="2f497-121">Media: media played and attempted.</span></span>

<span data-ttu-id="2f497-122">並非所有先前的事件都適合應用程式使用。</span><span class="sxs-lookup"><span data-stu-id="2f497-122">Not all of the previous events are suitable for use by applications.</span></span> <span data-ttu-id="2f497-123">帳戶變更、系統時鐘變更，以及登入和登出事件記錄只會由作業系統執行，因此不會公開。</span><span class="sxs-lookup"><span data-stu-id="2f497-123">Account changes, the system clock change, and logon and logoff event logging are implemented only by the operating system and so are not exposed publicly.</span></span>

> [!Note]  
> <span data-ttu-id="2f497-124">應用程式專案和結束事件的檢測可在 Windows Vista 中使用，並由家長監護設定以記錄此資料。</span><span class="sxs-lookup"><span data-stu-id="2f497-124">Instrumentation of application entry and exit events is available within Windows Vista, and is configured by Parental Controls to log this data.</span></span>

 

## <a name="logging-extensibility"></a><span data-ttu-id="2f497-125">記錄延伸</span><span class="sxs-lookup"><span data-stu-id="2f497-125">Logging Extensibility</span></span>

<span data-ttu-id="2f497-126">一般自訂事件也會以3個可用的標籤/值來定義，因此 Isv 通常不需要在資訊清單中定義自己的標記/值。</span><span class="sxs-lookup"><span data-stu-id="2f497-126">A generic custom event is also defined with 3 tags/values available so ISVs usually will not need to define their own in a manifest.</span></span> <span data-ttu-id="2f497-127">記錄檢視器會辨識並顯示標籤標頭和值（如果使用 (1 到3的欄位數目）) ，而且每個欄位的標題都是使用 WMI API 來註冊。</span><span class="sxs-lookup"><span data-stu-id="2f497-127">The Log Viewer will recognize and display the tag headers and values if the number of fields used (1 to 3) and headings for each field are registered using the WMI API.</span></span> <span data-ttu-id="2f497-128">一般事件檢視器也可以用來查看自訂事件。</span><span class="sxs-lookup"><span data-stu-id="2f497-128">The generic Event Viewer may also be used to view custom events.</span></span>

<span data-ttu-id="2f497-129">如果泛型自訂事件不適合，ISV 可以使用應用程式資訊清單來定義它自己，而且可以使用相同的 WMI API 來註冊最多三個欄位的標頭。</span><span class="sxs-lookup"><span data-stu-id="2f497-129">If the generic custom event is not suitable, an ISV can define its own by using an application manifest and it can register headers for up to three fields by using the same WMI API.</span></span>

<span data-ttu-id="2f497-130">Isv 可以選擇定義自己的事件，並透過公用 Windows Api 獨立于記錄檢視器中使用它們。</span><span class="sxs-lookup"><span data-stu-id="2f497-130">ISVs may choose to define their own events and consume them independently of the Log Viewer through public Windows APIs.</span></span> <span data-ttu-id="2f497-131">這並沒有完整記錄集中的優點。</span><span class="sxs-lookup"><span data-stu-id="2f497-131">This does not have the benefit of full log centralization.</span></span>

## <a name="parental-controls-panel-general-ui-extensibility-link-addition"></a><span data-ttu-id="2f497-132">父控制項面板一般 UI 擴充性連結新增</span><span class="sxs-lookup"><span data-stu-id="2f497-132">Parental Controls Panel General UI Extensibility Link Addition</span></span>

<span data-ttu-id="2f497-133">一般用途的使用者介面擴充性連結是透過 WMI 存取設定來公開，並以名稱資源 DLL 路徑和識別碼、影像 (點陣圖) 路徑、已停用狀態影像 (點陣圖) 路徑、子標題資源 DLL 路徑和識別碼，以及可執行檔路徑規格來建立延伸模組實例。</span><span class="sxs-lookup"><span data-stu-id="2f497-133">A general-purpose user interface extensibility link is exposed by accessing settings through WMI, creating an extension instance from passed in name resource DLL path and ID, image (bitmap) path, disabled state image (bitmap) path, subtitle resource DLL path and ID, and executable path specifications.</span></span> <span data-ttu-id="2f497-134">註冊之後，連結會出現在 [家長監護] 面板的 [更多設定] 區域中，然後按一下它將會叫用指定的可執行檔。</span><span class="sxs-lookup"><span data-stu-id="2f497-134">After registered, the link will appear in the More Settings area of the Parental Controls Panel, and clicking it will invoke the specified executable.</span></span>

<span data-ttu-id="2f497-135">可執行檔路徑字串可以選擇性地包含目前使用者的 SID 的標記，以在叫用之前加以取代。</span><span class="sxs-lookup"><span data-stu-id="2f497-135">The executable path string may optionally include a token for the current user's SID to be substituted prior to invocation.</span></span> <span data-ttu-id="2f497-136">如果可執行檔需要知道 SID，則這可讓連結執行在目前正在查看其中樞頁面的使用者內容中運作。</span><span class="sxs-lookup"><span data-stu-id="2f497-136">This allows the link execution to operate in the context of the user for which the hub page is currently being viewed, if the executable needs to know the SID.</span></span>

## <a name="web-content-filter-replacement"></a><span data-ttu-id="2f497-137">取代網路內容篩選</span><span class="sxs-lookup"><span data-stu-id="2f497-137">Web Content Filter Replacement</span></span>

<span data-ttu-id="2f497-138">如主題中所述，「家長監護」 [In-Box 限制和使用者介面](parental-controls-in-box-restrictions-and-user-interfaces.md)，可以使用廠商提供的篩選來取代內建的 Web 內容篩選器。</span><span class="sxs-lookup"><span data-stu-id="2f497-138">As noted in the topic, [Parental Controls In-Box Restrictions and User Interfaces](parental-controls-in-box-restrictions-and-user-interfaces.md), the in-box Web Content Filter can be replaced with a vendor-supplied filter.</span></span> <span data-ttu-id="2f497-139">這是透過 WMI 存取設定來執行，以設定擁有篩選的 GUID 和名稱。</span><span class="sxs-lookup"><span data-stu-id="2f497-139">This is performed by accessing settings through WMI to set a GUID and name owning the filtering.</span></span>

<span data-ttu-id="2f497-140">一般 UI 擴充性機制可用來公開協力廠商篩選。</span><span class="sxs-lookup"><span data-stu-id="2f497-140">The general UI extensibility mechanism is used to expose a third-party filter.</span></span> <span data-ttu-id="2f497-141">這與在最上層家長監護台的 [更多設定] 區段中所要顯示的任何延伸模組所使用的機制相同。</span><span class="sxs-lookup"><span data-stu-id="2f497-141">This is the same mechanism as used for any extension that wants to appear in the More Settings section of the top-level Parental Control Panel.</span></span> <span data-ttu-id="2f497-142">若要在系統層級篩選設定中將相同的 GUID 和適當的名稱資源 DLL 路徑與識別碼設定為額外的步驟，將會隱藏內建的篩選器連結，而協力廠商專案則會顯示在 [更多設定] 區段的上方。</span><span class="sxs-lookup"><span data-stu-id="2f497-142">Taking the additional step of setting the same GUID and an appropriate name resource DLL path and ID into the system-level filter settings will cause the in-box displayed filter link to be hidden and the third-party entry to be shown at the top of the More Settings section.</span></span> <span data-ttu-id="2f497-143">針對篩選所註冊的名稱將會顯示在 [摘要] 區段中。</span><span class="sxs-lookup"><span data-stu-id="2f497-143">The name registered for the filter will be shown in the summary section.</span></span>

<span data-ttu-id="2f497-144">重設篩選 GUID 和名稱路徑/識別碼設定會導致內建的 Web 內容篩選器將本身重新建立為作用中的篩選器，然後再次出現在 [Windows 設定] 區段中。</span><span class="sxs-lookup"><span data-stu-id="2f497-144">Resetting the filter GUID and name path/ID settings will result in the in-box Web Content Filter re-establishing itself as the active filter and appearing again in the Windows Settings section.</span></span>

<span data-ttu-id="2f497-145">請注意，協力廠商篩選器不受限於用來插入 Windows 通訊的技術。</span><span class="sxs-lookup"><span data-stu-id="2f497-145">Note that third-party filters are not constrained in the technologies used to plug into Windows communications.</span></span> <span data-ttu-id="2f497-146">篩選器只必須使用擴充性連結來公開其設定，並接受適當的家長監護設定。</span><span class="sxs-lookup"><span data-stu-id="2f497-146">A filter must merely expose its settings by using an extensibility link and honor appropriate Parental Controls settings.</span></span>

 

 

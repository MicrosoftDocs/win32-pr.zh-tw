---
title: 啟動預設的網頁瀏覽器或 Windows Store 應用程式之後，可能看不到桌面應用程式
description: 啟動預設的網頁瀏覽器或 Windows Store 應用程式之後，可能看不到桌面應用程式
ms.assetid: 5D2CE14B-111D-4987-A9AA-B04AC030F9F0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20c80541a860bd29f207ab99eba6ab4cb629a666
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/01/2020
ms.locfileid: "104316582"
---
# <a name="desktop-apps-may-not-be-visible-after-launching-the-default-web-browser-or-windows-store-apps"></a><span data-ttu-id="27fd3-103">啟動預設的網頁瀏覽器或 Windows Store 應用程式之後，可能看不到桌面應用程式</span><span class="sxs-lookup"><span data-stu-id="27fd3-103">Desktop apps may not be visible after launching the default web browser or Windows Store apps</span></span>

## <a name="platforms"></a><span data-ttu-id="27fd3-104">平台</span><span class="sxs-lookup"><span data-stu-id="27fd3-104">Platforms</span></span>

<span data-ttu-id="27fd3-105">**用戶端** – Windows 8</span><span class="sxs-lookup"><span data-stu-id="27fd3-105">**Clients** – Windows 8</span></span>  
<span data-ttu-id="27fd3-106">**伺服器** – Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="27fd3-106">**Servers** – Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="27fd3-107">Description</span><span class="sxs-lookup"><span data-stu-id="27fd3-107">Description</span></span>

<span data-ttu-id="27fd3-108">Windows Store 應用程式使用者體驗一次著重在單一應用程式，其中包含多工、應用程式切換，以及 Windows UI 提供的通知。</span><span class="sxs-lookup"><span data-stu-id="27fd3-108">The Windows Store app user experience is focused on a single app at a time, with multitasking, app switching, and notifications provided by the Windows UI.</span></span> <span data-ttu-id="27fd3-109">Windows Store 應用程式會調整大小以填滿螢幕上的可用空間，最常見的觀點是全螢幕。</span><span class="sxs-lookup"><span data-stu-id="27fd3-109">Windows Store apps are sized to fill available space on screen, with the most common view being full screen.</span></span> <span data-ttu-id="27fd3-110">因此，當系統上的另一個應用程式啟動時，您就無法再假設新的應用程式會在桌面應用程式中開啟。</span><span class="sxs-lookup"><span data-stu-id="27fd3-110">Therefore, when another app on the system is launched, you can no longer assume that the new app will open in a desktop window alongside your desktop app.</span></span> <span data-ttu-id="27fd3-111">這永遠適用于選擇參與新的 Windows UI 體驗的 Windows Store 應用程式和瀏覽器。</span><span class="sxs-lookup"><span data-stu-id="27fd3-111">This is always true of Windows Store apps and browsers that choose to participate in the new Windows UI experience.</span></span> <span data-ttu-id="27fd3-112">您可以同時繼續查看其他應用程式，例如，如果您在桌面上，然後啟動另一個桌面應用程式，或者您的應用程式處於已貼齊的狀態。</span><span class="sxs-lookup"><span data-stu-id="27fd3-112">You may continue to see other apps at the same time, for example, if you are on the Desktop and launch another desktop application or you have applications in a snapped state.</span></span>

## <a name="manifestation"></a><span data-ttu-id="27fd3-113">表現</span><span class="sxs-lookup"><span data-stu-id="27fd3-113">Manifestation</span></span>

<span data-ttu-id="27fd3-114">當傳統型應用程式使用一般的應用程式啟用技術，例如在檔案或通訊協定上使用 ShellExecute API 時，Windows 會啟動與該註冊相關聯的應用程式，這可能是 Windows Store 應用程式及/或使用者的預設網頁瀏覽器 (預設的網頁瀏覽器可能會選擇參與桌面或新的 Windows UI) 。</span><span class="sxs-lookup"><span data-stu-id="27fd3-114">When a desktop app uses common app activation techniques such as using the ShellExecute API on a file or protocol, Windows launches the app associated with that registration, which may be a Windows Store app and / or the user’s default web browser (the default web browser might choose to participate in either the desktop or the new Windows UI).</span></span> <span data-ttu-id="27fd3-115">Windows Store 應用程式是使用全螢幕來啟動，隱藏桌面以及從中啟動的桌面應用程式。</span><span class="sxs-lookup"><span data-stu-id="27fd3-115">Windows Store apps are launched using the full screen, hiding the desktop and the desktop app from which it was launched.</span></span>

> [!Note]  
> <span data-ttu-id="27fd3-116">在 Windows 8 中，Internet Explorer 10 已設定為使用者的預設瀏覽器，但使用者可以選擇安裝並設定另一個瀏覽器，做為預設 (不會變更 Windows 7) 。</span><span class="sxs-lookup"><span data-stu-id="27fd3-116">In Windows 8, Internet Explorer 10 is configured as the user’s default browser, but the user may choose to install and set another browser as the default (no change from Windows 7).</span></span> <span data-ttu-id="27fd3-117">在 Internet Explorer 10 中，從桌面應用程式開啟連結時，會在桌面上開啟 Internet Explorer。</span><span class="sxs-lookup"><span data-stu-id="27fd3-117">In Internet Explorer 10, when a link is opened from a desktop application, Internet Explorer will open on the desktop.</span></span> <span data-ttu-id="27fd3-118">但使用者可以變更此設定，讓 Internet Explorer 以 Windows Store 應用程式的形式開啟。</span><span class="sxs-lookup"><span data-stu-id="27fd3-118">But this setting can be changed by users so that Internet Explorer is opened as a Windows Store app.</span></span> <span data-ttu-id="27fd3-119">我們鼓勵瀏覽器廠商採用類似的「內容啟動」體驗;不過，開發人員應該規劃不是所有瀏覽器的行為都同樣的事實。</span><span class="sxs-lookup"><span data-stu-id="27fd3-119">Browser vendors have been encouraged to adopt a similar ”contextual launching” experience; however, developers should plan for the fact that not all browsers will behave similarly.</span></span>

 

## <a name="mitigation"></a><span data-ttu-id="27fd3-120">降低</span><span class="sxs-lookup"><span data-stu-id="27fd3-120">Mitigation</span></span>

<span data-ttu-id="27fd3-121">雖然開發人員無法對其應用程式進行任何變更，以減輕這種行為，但一般使用者可以執行哪些動作，讓您可以進行通訊。</span><span class="sxs-lookup"><span data-stu-id="27fd3-121">While there is no change that developers can make to their apps to mitigate this behavior, there are things the end user can do that you should communicate to them.</span></span> <span data-ttu-id="27fd3-122">請考慮使用擴充 ShellExecuteEx () API 所收集的資訊來填入內容適當的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="27fd3-122">Consider using the info gathered by the extended ShellExecuteEx() API to populate a contextually appropriate dialog.</span></span> <span data-ttu-id="27fd3-123">在該對話方塊中，向使用者指出將會啟動哪個應用程式，以及該應用程式是 Windows Store 應用程式還是桌面應用程式。</span><span class="sxs-lookup"><span data-stu-id="27fd3-123">In that dialog, indicate to the user what app will be launched and whether that app is a Windows Store app or a desktop app.</span></span> <span data-ttu-id="27fd3-124">您可以使用 CLSID 來區別 Windows Store 應用程式與桌面應用程式。</span><span class="sxs-lookup"><span data-stu-id="27fd3-124">The CLSID can be used to distinguish Windows Store apps from desktop apps.</span></span> <span data-ttu-id="27fd3-125">使用者選項：</span><span class="sxs-lookup"><span data-stu-id="27fd3-125">User options:</span></span>

-   <span data-ttu-id="27fd3-126">具有全螢幕監視器的使用者可以將 Windows Store 應用程式貼齊螢幕邊緣，以公開桌面，同時同時查看 Windows Store 應用程式和桌面應用程式。</span><span class="sxs-lookup"><span data-stu-id="27fd3-126">Users who have a wide-screen monitor can snap the Windows Store app to the edge of the screen to expose the desktop and thereby view both the Windows Store app and the desktop app at the same time.</span></span>
-   <span data-ttu-id="27fd3-127">如果 Internet Explorer 已設定為使用者的預設瀏覽器，則使用者可以變更控制台中的網際網路選項來變更其行為。</span><span class="sxs-lookup"><span data-stu-id="27fd3-127">If Internet Explorer is configured as the user’s default browser, users can change its behavior by changing the Internet Options in the Control Panel.</span></span> <span data-ttu-id="27fd3-128">在 [程式] 索引標籤上，使用者可以變更 Internet Explorer 處理連結的方式。</span><span class="sxs-lookup"><span data-stu-id="27fd3-128">On the Programs tab, users can change how Internet Explorer handles links.</span></span> <span data-ttu-id="27fd3-129">其他瀏覽器可能會提供類似的設定。</span><span class="sxs-lookup"><span data-stu-id="27fd3-129">Other browsers may offer a similar setting.</span></span>

 

 





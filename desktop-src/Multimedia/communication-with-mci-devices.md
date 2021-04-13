---
title: 與 MCI 裝置通訊
description: 與 MCI 裝置通訊
ms.assetid: a2532c29-553f-4ae3-8ad5-319fd9470e76
keywords:
- MCI 裝置，通訊
- MCIWndGetDeviceID 宏
- mciSendCommand 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1b5bfb7909b94bf8e71745adeeaeda61cae20ae
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314710"
---
# <a name="communication-with-mci-devices"></a><span data-ttu-id="e78bb-106">與 MCI 裝置通訊</span><span class="sxs-lookup"><span data-stu-id="e78bb-106">Communication with MCI Devices</span></span>

<span data-ttu-id="e78bb-107">每個 MCI 裝置都可以使用下列一或多個做為識別碼：</span><span class="sxs-lookup"><span data-stu-id="e78bb-107">It is possible for each MCI device to use one or more of the following as identifiers:</span></span>

-   <span data-ttu-id="e78bb-108">裝置識別碼</span><span class="sxs-lookup"><span data-stu-id="e78bb-108">a device identifier</span></span>
-   <span data-ttu-id="e78bb-109">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="e78bb-109">a device name</span></span>
-   <span data-ttu-id="e78bb-110">別名</span><span class="sxs-lookup"><span data-stu-id="e78bb-110">an alias</span></span>
-   <span data-ttu-id="e78bb-111">目前載入之內容的檔案名。</span><span class="sxs-lookup"><span data-stu-id="e78bb-111">the filename of the currently loaded content.</span></span>

<span data-ttu-id="e78bb-112">MCIWnd 提供可讓您用來取得此資訊的宏。</span><span class="sxs-lookup"><span data-stu-id="e78bb-112">MCIWnd provides macros you can use to retrieve this information.</span></span> <span data-ttu-id="e78bb-113">然後，您可以使用此資訊，透過 MCI 與 MCIWnd windows 相關聯的 MCI 裝置直接進行通訊。</span><span class="sxs-lookup"><span data-stu-id="e78bb-113">You can then use this information to communicate through MCI directly with MCI devices associated with MCIWnd windows.</span></span>

<span data-ttu-id="e78bb-114">您可以使用 [**MCIWndGetDeviceID**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdeviceid) 宏來取得目前 MCI 裝置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="e78bb-114">You can retrieve the identifier of the current MCI device by using the [**MCIWndGetDeviceID**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdeviceid) macro.</span></span> <span data-ttu-id="e78bb-115">MCI 裝置識別碼是識別應用程式所使用之 MCI 裝置實例的數值。</span><span class="sxs-lookup"><span data-stu-id="e78bb-115">The MCI device identifier is a numerical value that identifies the instance of the MCI device your application is using.</span></span> <span data-ttu-id="e78bb-116">當您的應用程式使用 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函式與 MCI 裝置進行通訊時，您的應用程式可以使用此識別碼。</span><span class="sxs-lookup"><span data-stu-id="e78bb-116">Your application can use this identifier when communicating with an MCI device by using the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function.</span></span>

<span data-ttu-id="e78bb-117">若要取出目前 MCI 裝置的名稱，請使用 [**MCIWndGetDevice**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdevice) 宏。</span><span class="sxs-lookup"><span data-stu-id="e78bb-117">To retrieve the name of the current MCI device, use the [**MCIWndGetDevice**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdevice) macro.</span></span> <span data-ttu-id="e78bb-118">MCI 裝置名稱是以 null 終止的字串，可識別與 MCIWnd 視窗相關聯的裝置類型。</span><span class="sxs-lookup"><span data-stu-id="e78bb-118">The MCI device name is a null-terminated string that identifies the device type associated with an MCIWnd window.</span></span> <span data-ttu-id="e78bb-119">當您的應用程式使用 **mciSendCommand** 與 MCI 裝置通訊時，您的應用程式可以使用這個名稱。</span><span class="sxs-lookup"><span data-stu-id="e78bb-119">Your application can use this name when communicating with an MCI device by using **mciSendCommand**.</span></span>

<span data-ttu-id="e78bb-120">您可以使用 [**MCIWndGetAlias**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetalias) 宏來取得目前 MCI 裝置的別名。</span><span class="sxs-lookup"><span data-stu-id="e78bb-120">You can retrieve the alias of the current MCI device by using the [**MCIWndGetAlias**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetalias) macro.</span></span> <span data-ttu-id="e78bb-121">當您的應用程式使用 [**mciSendString**](/previous-versions//dd757161(v=vs.85)) 函式與 MCI 裝置進行通訊時，您的應用程式可以使用此別名。</span><span class="sxs-lookup"><span data-stu-id="e78bb-121">Your application can use this alias when communicating with an MCI device by using the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function.</span></span>

<span data-ttu-id="e78bb-122">最後，您可以使用 [**MCIWndGetFileName**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetfilename) 宏取出 MCI 裝置所使用的檔案名。</span><span class="sxs-lookup"><span data-stu-id="e78bb-122">Finally, you can retrieve the filename used by an MCI device by using the [**MCIWndGetFileName**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetfilename) macro.</span></span> <span data-ttu-id="e78bb-123">檔案名會識別目前與 MCIWnd 視窗相關聯的內容。</span><span class="sxs-lookup"><span data-stu-id="e78bb-123">The filename identifies the content currently associated with an MCIWnd window.</span></span> <span data-ttu-id="e78bb-124">當您的應用程式使用 **mciSendCommand** 或 **mciSendString** 與 MCI 裝置進行通訊時，您的應用程式可以使用此檔案名。</span><span class="sxs-lookup"><span data-stu-id="e78bb-124">Your application can use this filename when communicating with a MCI device by using **mciSendCommand** or **mciSendString**.</span></span>

 

 
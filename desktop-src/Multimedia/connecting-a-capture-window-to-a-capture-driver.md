---
title: 將捕獲視窗連接至 Capture 驅動程式
description: 將捕獲視窗連接至 Capture 驅動程式
ms.assetid: 78d4aaf5-6216-4eec-84d4-6727d1822983
keywords:
- WM_CAP_DRIVER_CONNECT 訊息
- capDriverConnect 宏
- capGetDriverDescription 函式
- WM_CAP_DRIVER_GET_NAME 訊息
- capDriverGetName 宏
- WM_CAP_DRIVER_GET_VERSION 訊息
- capDriverGetVersion 宏
- WM_CAP_DRIVER_DISCONNECT 訊息
- capDriverDisconnect 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c189ad3ea5631e269ffbe85f20a143b074486f22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672971"
---
# <a name="connecting-a-capture-window-to-a-capture-driver"></a><span data-ttu-id="17d43-112">將捕獲視窗連接至 Capture 驅動程式</span><span class="sxs-lookup"><span data-stu-id="17d43-112">Connecting a Capture Window to a Capture Driver</span></span>

<span data-ttu-id="17d43-113">您可以將捕獲視窗動態連線或中斷連接到 capture 驅動程式。</span><span class="sxs-lookup"><span data-stu-id="17d43-113">You can dynamically connect or disconnect a capture window to a capture driver.</span></span> <span data-ttu-id="17d43-114">您可以使用 [ [**WM \_ CAP \_ 驅動程式 \_ 連接**](wm-cap-driver-connect.md) 訊息 (] 或 [ [**capDriverConnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverconnect) 宏) ，以連接或關聯捕獲視窗與 capture 驅動程式。</span><span class="sxs-lookup"><span data-stu-id="17d43-114">You can connect or associate a capture window with a capture driver by using the [**WM\_CAP\_DRIVER\_CONNECT**](wm-cap-driver-connect.md) message (or the [**capDriverConnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverconnect) macro).</span></span> <span data-ttu-id="17d43-115">連接 capture 視窗和 capture 驅動程式之後，您可以將裝置專屬的訊息傳送至與捕捉視窗相關聯的捕獲驅動程式。</span><span class="sxs-lookup"><span data-stu-id="17d43-115">After a capture window and capture driver are connected, you can send device-specific messages to the capture driver associated with a capture window.</span></span>

<span data-ttu-id="17d43-116">如果您在系統上安裝了一部以上的捕獲裝置，您可以針對 WM  \_ CAP \_ 驅動程式連線訊息的 wParam 參數指定整數，以將捕獲視窗連線到特定的影片擷取裝置磁碟機 \_ 。</span><span class="sxs-lookup"><span data-stu-id="17d43-116">If you have more than one capture device installed on a system, you can connect a capture window to a particular video capture device driver by specifying an integer for the *wParam* parameter of the WM\_CAP\_DRIVER\_CONNECT message.</span></span> <span data-ttu-id="17d43-117">整數是索引，可識別登錄或 SYSTEM.INI 檔案的 [驅動程式] 區段中所列的影片捕獲驅動程式 \[ \] 。</span><span class="sxs-lookup"><span data-stu-id="17d43-117">The integer is an index that identifies a video capture driver listed in the registry or in the \[drivers\] section of the SYSTEM.INI file.</span></span> <span data-ttu-id="17d43-118">第一個索引項目使用零。</span><span class="sxs-lookup"><span data-stu-id="17d43-118">Use zero for the first index entry.</span></span>

<span data-ttu-id="17d43-119">您可以使用 [**capGetDriverDescription**](/windows/desktop/api/Vfw/nf-vfw-capgetdriverdescriptiona) 函式來取得已安裝之 capture 驅動程式的名稱和版本。</span><span class="sxs-lookup"><span data-stu-id="17d43-119">You can retrieve the name and version of an installed capture driver by using the [**capGetDriverDescription**](/windows/desktop/api/Vfw/nf-vfw-capgetdriverdescriptiona) function.</span></span> <span data-ttu-id="17d43-120">您的應用程式可以使用此函式來列舉已安裝的捕獲裝置和驅動程式，讓使用者可以選取要連接到捕捉視窗的擷取裝置。</span><span class="sxs-lookup"><span data-stu-id="17d43-120">Your application can use this function to enumerate the installed capture devices and drivers, so the user can select a capture device to connect to a capture window.</span></span>

<span data-ttu-id="17d43-121">您可以使用 [ [**WM \_ CAP \_ 驅動程式 \_ 取得 \_ 名稱**](wm-cap-driver-get-name.md) 訊息 (] 或 [ [**capDriverGetName**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetname) 宏) ]，以抓取連接至 [捕獲] 視窗的擷取裝置磁碟機的名稱。</span><span class="sxs-lookup"><span data-stu-id="17d43-121">You can retrieve the name of the capture device driver connected to a capture window by using the [**WM\_CAP\_DRIVER\_GET\_NAME**](wm-cap-driver-get-name.md) message (or the [**capDriverGetName**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetname) macro).</span></span> <span data-ttu-id="17d43-122">若要取得已安裝的 capture 驅動程式版本，請使用 [ [**WM \_ CAP \_ 驅動程式 \_ 取得 \_ 版本**](wm-cap-driver-get-version.md) 訊息 (或 [**capDriverGetVersion**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetversion) 宏) 。</span><span class="sxs-lookup"><span data-stu-id="17d43-122">To retrieve the version of an installed capture driver, use the [**WM\_CAP\_DRIVER\_GET\_VERSION**](wm-cap-driver-get-version.md) message (or the [**capDriverGetVersion**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetversion) macro).</span></span>

<span data-ttu-id="17d43-123">您可以使用 [ [**WM \_ CAP \_ 驅動程式 \_ 中斷**](wm-cap-driver-disconnect.md) 連線訊息 (] 或 [ [**capDriverDisconnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverdisconnect) 宏) ，從 capture 驅動程式中斷連線捕獲視窗。</span><span class="sxs-lookup"><span data-stu-id="17d43-123">You can disconnect a capture window from a capture driver by using the [**WM\_CAP\_DRIVER\_DISCONNECT**](wm-cap-driver-disconnect.md) message (or the [**capDriverDisconnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverdisconnect) macro).</span></span>

<span data-ttu-id="17d43-124">當捕捉視窗終結時，任何連線的影片擷取裝置磁碟機都會自動中斷連線。</span><span class="sxs-lookup"><span data-stu-id="17d43-124">When an capture window is destroyed, any connected video capture device drivers are automatically disconnected.</span></span>

 

 





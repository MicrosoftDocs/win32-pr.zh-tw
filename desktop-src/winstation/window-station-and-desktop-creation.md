---
title: 視窗工作站和桌面建立
description: 系統會自動建立互動式視窗工作站。
ms.assetid: 5b908cb6-3a72-4afc-aed0-8411e8d0888f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34aff24a29432e3e394a199bf881aa386bf17e71
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315142"
---
# <a name="window-station-and-desktop-creation"></a><span data-ttu-id="48610-103">視窗工作站和桌面建立</span><span class="sxs-lookup"><span data-stu-id="48610-103">Window Station and Desktop Creation</span></span>

<span data-ttu-id="48610-104">系統會自動建立互動式視窗工作站。</span><span class="sxs-lookup"><span data-stu-id="48610-104">The system automatically creates the interactive window station.</span></span> <span data-ttu-id="48610-105">當互動式使用者登入時，系統會將互動式視窗工作站與使用者登入會話產生關聯。</span><span class="sxs-lookup"><span data-stu-id="48610-105">When an interactive user logs on, the system associates the interactive window station with the user logon session.</span></span> <span data-ttu-id="48610-106">系統也會為互動式視窗工作站建立預設的輸入桌面 (Winsta0 \\ 預設) 。</span><span class="sxs-lookup"><span data-stu-id="48610-106">The system also creates the default input desktop for the interactive window station (Winsta0\\default).</span></span> <span data-ttu-id="48610-107">由登入的使用者啟動的進程會與 Winsta0 \\ 預設桌面相關聯。</span><span class="sxs-lookup"><span data-stu-id="48610-107">Processes started by the logged-on user are associated with the Winsta0\\default desktop.</span></span>

<span data-ttu-id="48610-108">進程可以使用 [**CreateWindowStation**](/windows/win32/api/winuser/nf-winuser-createwindowstationa) 函式來建立新的視窗工作站，並使用 **CreateDesktop** 或 [**CreateDesktopEx**](/windows/win32/api/winuser/nf-winuser-createdesktopexa) 函式來建立新的桌面。</span><span class="sxs-lookup"><span data-stu-id="48610-108">A process can use the [**CreateWindowStation**](/windows/win32/api/winuser/nf-winuser-createwindowstationa) function to create a new window station, and the **CreateDesktop** or [**CreateDesktopEx**](/windows/win32/api/winuser/nf-winuser-createdesktopexa) function to create a new desktop.</span></span> <span data-ttu-id="48610-109">可以建立的桌面數目受限於系統桌面堆積的大小。</span><span class="sxs-lookup"><span data-stu-id="48610-109">The number of desktops that can be created is limited by the size of the system desktop heap.</span></span> <span data-ttu-id="48610-110">如需詳細資訊，請參閱 [**CreateDesktop**](/windows/win32/api/winuser/nf-winuser-createdesktopa)。</span><span class="sxs-lookup"><span data-stu-id="48610-110">For more information, see [**CreateDesktop**](/windows/win32/api/winuser/nf-winuser-createdesktopa).</span></span>

<span data-ttu-id="48610-111">當非互動式進程（例如服務應用程式）嘗試連接到視窗工作站，而進程登入會話沒有任何視窗工作站時，系統會嘗試建立會話的視窗工作站和桌面。</span><span class="sxs-lookup"><span data-stu-id="48610-111">When a noninteractive process such as a service application attempts to connect to a window station and no window station exists for the process logon session, the system attempts to create a window station and desktop for the session.</span></span> <span data-ttu-id="48610-112">所建立之視窗工作站的名稱是以登入會話識別碼為基礎，而桌面名為預設值，如下所述：</span><span class="sxs-lookup"><span data-stu-id="48610-112">The name of the created window station is based on the logon session identifier, and the desktop is named default, as described here:</span></span>

-   <span data-ttu-id="48610-113">如果服務是在 LocalSystem 帳戶的安全性內容中執行，但是未包含服務 \_ 互動式 \_ 進程屬性，它會使用下列視窗站和 desktop： 3e7 $ \\ default。</span><span class="sxs-lookup"><span data-stu-id="48610-113">If a service is running in the security context of the LocalSystem account but does not include the SERVICE\_INTERACTIVE\_PROCESS attribute, it uses the following window station and desktop: Service-0x0-3e7$\\default.</span></span> <span data-ttu-id="48610-114">此視窗站並非互動式，因此服務無法顯示使用者介面。</span><span class="sxs-lookup"><span data-stu-id="48610-114">This window station is not interactive, so the service cannot display a user interface.</span></span> <span data-ttu-id="48610-115">此外，服務所建立的進程也無法顯示使用者介面。</span><span class="sxs-lookup"><span data-stu-id="48610-115">In addition, processes created by the service cannot display a user interface.</span></span>
-   <span data-ttu-id="48610-116">如果服務是在使用者帳戶的安全性內容中執行，則視窗工作站的名稱是以使用者 SID 服務-0x *Z1* - *Z2*$ 為基礎，其中 *Z1* 是登入 sid 的最高部分，而 *Z2* 是登入 sid 的低部分。</span><span class="sxs-lookup"><span data-stu-id="48610-116">If the service is running in the security context of a user account, the name of the window station is based on the user SID Service-0x *Z1*-*Z2*$, where *Z1* is the high part of the logon SID and *Z2* is the low part of the logon SID.</span></span> <span data-ttu-id="48610-117">由於 SID 對登入會話而言是唯一的，因此在相同安全性內容中執行的兩個服務會接收唯一的視窗工作站。</span><span class="sxs-lookup"><span data-stu-id="48610-117">Because a SID is unique to the logon session, two services running in the same security context receive unique window stations.</span></span> <span data-ttu-id="48610-118">這些視窗站並非互動式。</span><span class="sxs-lookup"><span data-stu-id="48610-118">These window stations are not interactive.</span></span>

<span data-ttu-id="48610-119">適用于 windows 工作站和桌面的任意存取控制清單 (DACL) 包含下列服務使用者帳戶的存取權限：</span><span class="sxs-lookup"><span data-stu-id="48610-119">The discretionary access control list (DACL) for the window station and desktop includes the following access rights for the service's user account:</span></span>

<span data-ttu-id="48610-120">視窗站：</span><span class="sxs-lookup"><span data-stu-id="48610-120">Window Station:</span></span>

<dl> <span data-ttu-id="48610-121">WINSTA \_ ACCESSCLIPBOARD</span><span class="sxs-lookup"><span data-stu-id="48610-121">WINSTA\_ACCESSCLIPBOARD</span></span>  
<span data-ttu-id="48610-122">WINSTA \_ ACCESSGLOBALATOMS</span><span class="sxs-lookup"><span data-stu-id="48610-122">WINSTA\_ACCESSGLOBALATOMS</span></span>  
<span data-ttu-id="48610-123">WINSTA \_ CREATEDESKTOP</span><span class="sxs-lookup"><span data-stu-id="48610-123">WINSTA\_CREATEDESKTOP</span></span>  
<span data-ttu-id="48610-124">WINSTA \_ EXITWINDOWS</span><span class="sxs-lookup"><span data-stu-id="48610-124">WINSTA\_EXITWINDOWS</span></span>  
<span data-ttu-id="48610-125">WINSTA \_ READATTRIBUTES</span><span class="sxs-lookup"><span data-stu-id="48610-125">WINSTA\_READATTRIBUTES</span></span>  
<span data-ttu-id="48610-126">\_需要標準許可權 \_</span><span class="sxs-lookup"><span data-stu-id="48610-126">STANDARD\_RIGHTS\_REQUIRED</span></span>  
</dl>

<span data-ttu-id="48610-127">桌上型電腦：</span><span class="sxs-lookup"><span data-stu-id="48610-127">Desktop:</span></span>

<dl> <span data-ttu-id="48610-128">桌面 \_ CREATEMENU</span><span class="sxs-lookup"><span data-stu-id="48610-128">DESKTOP\_CREATEMENU</span></span>  
<span data-ttu-id="48610-129">電腦 \_ CREATEWINDOW</span><span class="sxs-lookup"><span data-stu-id="48610-129">DESKTOP\_CREATEWINDOW</span></span>  
<span data-ttu-id="48610-130">桌面 \_ 列舉</span><span class="sxs-lookup"><span data-stu-id="48610-130">DESKTOP\_ENUMERATE</span></span>  
<span data-ttu-id="48610-131">桌面 \_ HOOKCONTROL</span><span class="sxs-lookup"><span data-stu-id="48610-131">DESKTOP\_HOOKCONTROL</span></span>  
<span data-ttu-id="48610-132">桌面 \_ READOBJECTS</span><span class="sxs-lookup"><span data-stu-id="48610-132">DESKTOP\_READOBJECTS</span></span>  
<span data-ttu-id="48610-133">桌面 \_ WRITEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="48610-133">DESKTOP\_WRITEOBJECTS</span></span>  
<span data-ttu-id="48610-134">\_需要標準許可權 \_</span><span class="sxs-lookup"><span data-stu-id="48610-134">STANDARD\_RIGHTS\_REQUIRED</span></span>  
</dl>

 

 
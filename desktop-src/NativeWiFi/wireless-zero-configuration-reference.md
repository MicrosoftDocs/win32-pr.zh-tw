---
description: 包含 Windows XP 和 Windows Server 2003 上的無線零設定服務之程式設計介面的相關資訊。
ms.assetid: cd9e8fc0-0a65-4654-95aa-201751183521
title: 無線零設定參考
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ebe202e16aa38fef617f382559f124772d50a58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192640"
---
# <a name="wireless-zero-configuration-reference"></a><span data-ttu-id="7ef7c-103">無線零設定參考</span><span class="sxs-lookup"><span data-stu-id="7ef7c-103">Wireless Zero Configuration Reference</span></span>

<span data-ttu-id="7ef7c-104">\[Windows Vista 和 Windows Server 2008 不再支援無線零設定程式設計介面。</span><span class="sxs-lookup"><span data-stu-id="7ef7c-104">\[The Wireless Zero Configuration programming interface is no longer supported as of Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="7ef7c-105">相反地，請使用 [原生 WIFI API](native-wifi-reference.md)，它會提供類似的功能。</span><span class="sxs-lookup"><span data-stu-id="7ef7c-105">Instead, use the [Native Wifi API](native-wifi-reference.md), which provides similar functionality.</span></span> <span data-ttu-id="7ef7c-106">如需詳細資訊，請參閱 [關於原生 WIFI API](about-the-native-wifi-api.md)。\]</span><span class="sxs-lookup"><span data-stu-id="7ef7c-106">For more information, see [About the Native Wifi API](about-the-native-wifi-api.md).\]</span></span>

<span data-ttu-id="7ef7c-107">本節包含 Windows XP 和 Windows Server 2003 上的無線零設定服務之程式設計介面的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="7ef7c-107">This section contains information on the programming interface for the Wireless Zero Configuration service on Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="7ef7c-108">主題包括：</span><span class="sxs-lookup"><span data-stu-id="7ef7c-108">The topics include:</span></span>

-   [<span data-ttu-id="7ef7c-109">無線零設定函數</span><span class="sxs-lookup"><span data-stu-id="7ef7c-109">Wireless Zero Configuration Functions</span></span>](wireless-zero-configuration-functions.md)
-   [<span data-ttu-id="7ef7c-110">無線零設定結構</span><span class="sxs-lookup"><span data-stu-id="7ef7c-110">Wireless Zero Configuration Structures</span></span>](wireless-zero-configuration-structures.md)

<span data-ttu-id="7ef7c-111">無線零設定是 Windows XP 和 Windows Server 2003 上的 Windows 服務，可用來設定和管理無線介面卡上的無線網路連線。</span><span class="sxs-lookup"><span data-stu-id="7ef7c-111">Wireless Zero Configuration is a Windows service on Windows XP and Windows Server 2003 that is used to configure and manage wireless network connections on a wireless adapter.</span></span> <span data-ttu-id="7ef7c-112">無線零設定的服務名稱是 WZCSVC。</span><span class="sxs-lookup"><span data-stu-id="7ef7c-112">The service name for Wireless Zero Configuration is WZCSVC.</span></span> <span data-ttu-id="7ef7c-113">在 Windows XP 上，WZCSVC 服務的顯示名稱為「無線零設定」。</span><span class="sxs-lookup"><span data-stu-id="7ef7c-113">On Windows XP, the display name for the WZCSVC service is Wireless Zero Configuration.</span></span> <span data-ttu-id="7ef7c-114">在 Windows Server 2003 上，WZCSVC 服務的顯示名稱為「無線設定」。</span><span class="sxs-lookup"><span data-stu-id="7ef7c-114">On Windows Server 2003, the display name for the WZCSVC service is Wireless Configuration.</span></span>

<span data-ttu-id="7ef7c-115">無線零設定服務通常是在開機時啟動。</span><span class="sxs-lookup"><span data-stu-id="7ef7c-115">The Wireless Zero Configuration service is normally started at boot time.</span></span> <span data-ttu-id="7ef7c-116">只有在無線零設定服務啟動時，才能使用無線零設定服務的程式設計介面。</span><span class="sxs-lookup"><span data-stu-id="7ef7c-116">The programming interface for the Wireless Zero Configuration service can be used only if the Wireless Zero Configuration service has been started.</span></span> <span data-ttu-id="7ef7c-117">如果未啟動無線零設定服務，無線零設定函數將會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="7ef7c-117">If the Wireless Zero Configuration service is not started, then the Wireless Zero Configuration functions will return an error.</span></span>

<span data-ttu-id="7ef7c-118">若要啟用無線零設定服務，讓它自動啟動，請移至 [ **開始** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="7ef7c-118">To enable the Wireless Zero Configuration service so it starts up automatically, go to the **Start** button.</span></span> <span data-ttu-id="7ef7c-119">選取 [ **設定** ] 選項，然後選取 [ **主控台**]。</span><span class="sxs-lookup"><span data-stu-id="7ef7c-119">Select the **Settings** option and then select **Control Panel**.</span></span> <span data-ttu-id="7ef7c-120">如果您使用的是 Windows XP view，請選取 [ **效能及維護** ] 類別，然後選取 [系統 **管理工具**]。</span><span class="sxs-lookup"><span data-stu-id="7ef7c-120">If you are using the Windows XP view, select the **Performance and Maintenance** category and then select **Administrative Tools**.</span></span> <span data-ttu-id="7ef7c-121">如果您使用的是傳統視圖，請選取 [系統 **管理工具**]。</span><span class="sxs-lookup"><span data-stu-id="7ef7c-121">If you are using the Classic View, then select **Administrative Tools**.</span></span> <span data-ttu-id="7ef7c-122">按一下左窗格中的 [ **服務** ] 圖示。</span><span class="sxs-lookup"><span data-stu-id="7ef7c-122">Click the **Services** icon in the left pane.</span></span> <span data-ttu-id="7ef7c-123">按一下右窗格中的 [無線零設定] 圖示，並將 [dropbox] 的 [ **啟動類型** ] 變更為 [ **自動**]。</span><span class="sxs-lookup"><span data-stu-id="7ef7c-123">Click the Wireless Zero Configuration icon in the right pane and change the **Startup Type** dropbox to **Automatic**.</span></span> <span data-ttu-id="7ef7c-124">此設定會將服務設定為在開機時自動啟動。</span><span class="sxs-lookup"><span data-stu-id="7ef7c-124">This setting will set the service to start automatically at boot time.</span></span> <span data-ttu-id="7ef7c-125">然後按一下 [ **開始** ] 按鈕，啟動無線零無線零設定服務，然後按一下 [ **確定]** 按鈕。</span><span class="sxs-lookup"><span data-stu-id="7ef7c-125">Then click the **Start** button to start the Wireless Zero Wireless Zero Configuration service and click the **OK** button.</span></span>

<span data-ttu-id="7ef7c-126">您也可以從命令提示字元啟動和停止無線零設定。</span><span class="sxs-lookup"><span data-stu-id="7ef7c-126">The Wireless Zero Configuration can also be started and stopped from a command prompt.</span></span> <span data-ttu-id="7ef7c-127">若要啟動無線零設定，請執行下列命令：</span><span class="sxs-lookup"><span data-stu-id="7ef7c-127">To start the Wireless Zero Configuration, run the following command:</span></span>

<span data-ttu-id="7ef7c-128">**net start wzcsvc**</span><span class="sxs-lookup"><span data-stu-id="7ef7c-128">**net start wzcsvc**</span></span>

<span data-ttu-id="7ef7c-129">若要停止無線零設定，請執行下列命令：</span><span class="sxs-lookup"><span data-stu-id="7ef7c-129">To stop the Wireless Zero Configuration, run the following command:</span></span>

<span data-ttu-id="7ef7c-130">**net stop wzcsvc**</span><span class="sxs-lookup"><span data-stu-id="7ef7c-130">**net stop wzcsvc**</span></span>

 

 




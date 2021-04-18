---
title: WNet 函式
description: Windows 網路功能提供管理網路資源的資訊與公用程式。
ms.assetid: 8a83186f-a912-4c61-8137-1f6be1f3afd6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 623de7adfdb57e21f01bff8b9647d6d2d175bd63
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104186066"
---
# <a name="wnet-functions"></a><span data-ttu-id="0c225-103">WNet 函式</span><span class="sxs-lookup"><span data-stu-id="0c225-103">WNet Functions</span></span>

<span data-ttu-id="0c225-104">Windows 網路功能提供管理網路資源的資訊與公用程式。</span><span class="sxs-lookup"><span data-stu-id="0c225-104">Windows Networking functions provide information and utilities for managing network resources.</span></span> <span data-ttu-id="0c225-105">Windows 網路功能可以依下列方式分組：</span><span class="sxs-lookup"><span data-stu-id="0c225-105">The Windows Networking functions can be grouped as follows:</span></span>

-   [<span data-ttu-id="0c225-106">連接函數</span><span class="sxs-lookup"><span data-stu-id="0c225-106">Connection functions</span></span>](#connection-functions)
-   [<span data-ttu-id="0c225-107">列舉函數</span><span class="sxs-lookup"><span data-stu-id="0c225-107">Enumeration functions</span></span>](#enumeration-functions)
-   [<span data-ttu-id="0c225-108">資訊函數</span><span class="sxs-lookup"><span data-stu-id="0c225-108">Information functions</span></span>](#information-functions)
-   [<span data-ttu-id="0c225-109">使用者函式</span><span class="sxs-lookup"><span data-stu-id="0c225-109">User functions</span></span>](#user-functions)

## <a name="connection-functions"></a><span data-ttu-id="0c225-110">連接函數</span><span class="sxs-lookup"><span data-stu-id="0c225-110">Connection Functions</span></span>

<span data-ttu-id="0c225-111">呼叫下列 WNet 連線函式，將本機裝置連線到網路資源，並取消網路連線。</span><span class="sxs-lookup"><span data-stu-id="0c225-111">Call the following WNet connection functions to connect a local device to a network resource, and to cancel network connections.</span></span>



| <span data-ttu-id="0c225-112">函式</span><span class="sxs-lookup"><span data-stu-id="0c225-112">Function</span></span>                                                                     | <span data-ttu-id="0c225-113">描述</span><span class="sxs-lookup"><span data-stu-id="0c225-113">Description</span></span>                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0c225-114">**MultinetGetConnectionPerformance**</span><span class="sxs-lookup"><span data-stu-id="0c225-114">**MultinetGetConnectionPerformance**</span></span>](/windows/win32/api/winnetwk/nf-winnetwk-multinetgetconnectionperformancea) | <span data-ttu-id="0c225-115">傳回網路資源連線的預期效能相關資訊。</span><span class="sxs-lookup"><span data-stu-id="0c225-115">Returns information about the expected performance of a connection to a network resource.</span></span>                                                                                                                                      |
| [<span data-ttu-id="0c225-116">**WNetAddConnection**</span><span class="sxs-lookup"><span data-stu-id="0c225-116">**WNetAddConnection**</span></span>](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnectiona)                               | <span data-ttu-id="0c225-117">將本機裝置連接到網路資源。</span><span class="sxs-lookup"><span data-stu-id="0c225-117">Connects a local device to a network resource.</span></span> <span data-ttu-id="0c225-118">提供的 (是為了與16位版本的 Windows 相容。 ) </span><span class="sxs-lookup"><span data-stu-id="0c225-118">(Provided for compatibility with 16-bit versions of Windows.)</span></span>                                                                                                                   |
| [<span data-ttu-id="0c225-119">**WNetAddConnection2**</span><span class="sxs-lookup"><span data-stu-id="0c225-119">**WNetAddConnection2**</span></span>](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a)                             | <span data-ttu-id="0c225-120">將本機裝置連接到網路資源。</span><span class="sxs-lookup"><span data-stu-id="0c225-120">Connects a local device to a network resource.</span></span>                                                                                                                                                                                 |
| [<span data-ttu-id="0c225-121">**WNetAddConnection3**</span><span class="sxs-lookup"><span data-stu-id="0c225-121">**WNetAddConnection3**</span></span>](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a)                             | <span data-ttu-id="0c225-122">將本機裝置連接到網路資源。</span><span class="sxs-lookup"><span data-stu-id="0c225-122">Connects a local device to a network resource.</span></span> <span data-ttu-id="0c225-123">這個函式包含一個以上的參數，而非 **WNetAddConnection2** 函式，這是一個視窗的控制碼，可供網路提供者作為對話方塊的主視窗。</span><span class="sxs-lookup"><span data-stu-id="0c225-123">This function includes one more parameter than the **WNetAddConnection2** function, a handle to a window that the network provider can use as an owner window for dialog boxes.</span></span> |
| [<span data-ttu-id="0c225-124">**WNetCancelConnection**</span><span class="sxs-lookup"><span data-stu-id="0c225-124">**WNetCancelConnection**</span></span>](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnectiona)                         | <span data-ttu-id="0c225-125">取消網路連接。</span><span class="sxs-lookup"><span data-stu-id="0c225-125">Cancels a network connection.</span></span> <span data-ttu-id="0c225-126">提供的 (是為了與16位版本的 Windows 相容。 ) </span><span class="sxs-lookup"><span data-stu-id="0c225-126">(Provided for compatibility with 16-bit versions of Windows.)</span></span>                                                                                                                                    |
| [<span data-ttu-id="0c225-127">**WNetCancelConnection2**</span><span class="sxs-lookup"><span data-stu-id="0c225-127">**WNetCancelConnection2**</span></span>](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a)                       | <span data-ttu-id="0c225-128">取消網路連線，讓您能夠使用持續連線的相關資訊來更新使用者設定檔。</span><span class="sxs-lookup"><span data-stu-id="0c225-128">Cancels a network connection, providing the ability to update the user profile with information about persistent connections.</span></span>                                                                                                  |
| [<span data-ttu-id="0c225-129">**WNetConnectionDialog**</span><span class="sxs-lookup"><span data-stu-id="0c225-129">**WNetConnectionDialog**</span></span>](/windows/win32/api/winnetwk/nf-winnetwk-wnetconnectiondialog)                         | <span data-ttu-id="0c225-130">啟動一般流覽對話方塊，以連接到網路資源。</span><span class="sxs-lookup"><span data-stu-id="0c225-130">Starts a general browsing dialog box for connecting to network resources.</span></span>                                                                                                                                                      |
| [<span data-ttu-id="0c225-131">**WNetConnectionDialog1**</span><span class="sxs-lookup"><span data-stu-id="0c225-131">**WNetConnectionDialog1**</span></span>](/windows/win32/api/winnetwk/nf-winnetwk-wnetconnectiondialog1a)                       | <span data-ttu-id="0c225-132">使用 [**CONNECTDLGSTRUCT**](/windows/win32/api/winnetwk/ns-winnetwk-connectdlgstructa) 結構啟動一般流覽對話方塊，以連接到網路資源。</span><span class="sxs-lookup"><span data-stu-id="0c225-132">Starts a general browsing dialog box for connecting to network resources, using a [**CONNECTDLGSTRUCT**](/windows/win32/api/winnetwk/ns-winnetwk-connectdlgstructa) structure.</span></span>                                                                                  |
| [<span data-ttu-id="0c225-133">**WNetDisconnectDialog**</span><span class="sxs-lookup"><span data-stu-id="0c225-133">**WNetDisconnectDialog**</span></span>](/windows/win32/api/winnetwk/nf-winnetwk-wnetdisconnectdialog)                         | <span data-ttu-id="0c225-134">啟動從網路資源中斷連線的一般流覽對話方塊。</span><span class="sxs-lookup"><span data-stu-id="0c225-134">Starts a general browsing dialog box for disconnecting from network resources.</span></span>                                                                                                                                                 |
| [<span data-ttu-id="0c225-135">**WNetDisconnectDialog1**</span><span class="sxs-lookup"><span data-stu-id="0c225-135">**WNetDisconnectDialog1**</span></span>](/windows/win32/api/winnetwk/nf-winnetwk-wnetdisconnectdialog1a)                       | <span data-ttu-id="0c225-136">開始使用 [**DISCDLGSTRUCT**](/windows/win32/api/winnetwk/ns-winnetwk-discdlgstructa) 結構，從網路資源中斷連接的一般流覽對話方塊。</span><span class="sxs-lookup"><span data-stu-id="0c225-136">Starts a general browsing dialog box for disconnecting from network resources, using a [**DISCDLGSTRUCT**](/windows/win32/api/winnetwk/ns-winnetwk-discdlgstructa) structure.</span></span>                                                                                   |
| [<span data-ttu-id="0c225-137">**WNetGetConnection**</span><span class="sxs-lookup"><span data-stu-id="0c225-137">**WNetGetConnection**</span></span>](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetconnectiona)                               | <span data-ttu-id="0c225-138">抓取與本機裝置相關聯之網路資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="0c225-138">Retrieves the name of the network resource associated with a local device.</span></span>                                                                                                                                                     |
| [<span data-ttu-id="0c225-139">**WNetGetUniversalName**</span><span class="sxs-lookup"><span data-stu-id="0c225-139">**WNetGetUniversalName**</span></span>](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetuniversalnamea)                         | <span data-ttu-id="0c225-140">針對網路資源提供以磁片磁碟機為基礎的路徑時，會傳回更通用的名稱格式。</span><span class="sxs-lookup"><span data-stu-id="0c225-140">When given a drive-based path for a network resource, returns a more universal form of the name.</span></span>                                                                                                                               |
| [<span data-ttu-id="0c225-141">**WNetRestoreConnectionW**</span><span class="sxs-lookup"><span data-stu-id="0c225-141">**WNetRestoreConnectionW**</span></span>](/windows/win32/api/winnetwk/nf-winnetwk-wnetrestoreconnectionw)                     | <span data-ttu-id="0c225-142">將連接還原至網路資源，並在必要時提示使用者輸入名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="0c225-142">Restores the connection to a network resource, prompting the user, if necessary, for a name and password.</span></span>                                                                                                                      |
| [<span data-ttu-id="0c225-143">**WNetUseConnection**</span><span class="sxs-lookup"><span data-stu-id="0c225-143">**WNetUseConnection**</span></span>](/windows/win32/api/winnetwk/nf-winnetwk-wnetuseconnectiona)                               | <span data-ttu-id="0c225-144">將本機裝置連接到網路資源;自動選取未使用的本機裝置，以重新導向至網路資源。</span><span class="sxs-lookup"><span data-stu-id="0c225-144">Connects a local device to a network resource; automatically selects an unused local device to redirect to the network resource.</span></span>                                                                                               |



 

> [!Note]  
> <span data-ttu-id="0c225-145">[**WNetAddConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnectiona)和 [**WNetCancelConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnectiona)函式支援與 Windows 的工作組相容。</span><span class="sxs-lookup"><span data-stu-id="0c225-145">The [**WNetAddConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnectiona) and [**WNetCancelConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnectiona) functions are supported for compatibility with Windows for Workgroups.</span></span> <span data-ttu-id="0c225-146">不過，新的應用程式應該使用 [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a) 或 [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a)，以及 [**WNetCancelConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a)。</span><span class="sxs-lookup"><span data-stu-id="0c225-146">However, new applications should use [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a) or [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a), and [**WNetCancelConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a).</span></span>

 

## <a name="enumeration-functions"></a><span data-ttu-id="0c225-147">列舉函數</span><span class="sxs-lookup"><span data-stu-id="0c225-147">Enumeration Functions</span></span>

<span data-ttu-id="0c225-148">呼叫下列 WNet 函式來列舉網路資源。</span><span class="sxs-lookup"><span data-stu-id="0c225-148">Call the following WNet functions to enumerate network resources.</span></span>



| <span data-ttu-id="0c225-149">函式</span><span class="sxs-lookup"><span data-stu-id="0c225-149">Function</span></span>                                     | <span data-ttu-id="0c225-150">描述</span><span class="sxs-lookup"><span data-stu-id="0c225-150">Description</span></span>                                                                             |
|----------------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="0c225-151">**WNetCloseEnum**</span><span class="sxs-lookup"><span data-stu-id="0c225-151">**WNetCloseEnum**</span></span>](/windows/win32/api/winnetwk/nf-winnetwk-wnetcloseenum)       | <span data-ttu-id="0c225-152">結束網路資源列舉。</span><span class="sxs-lookup"><span data-stu-id="0c225-152">Ends a network resource enumeration.</span></span>                                                    |
| [<span data-ttu-id="0c225-153">**WNetEnumResource**</span><span class="sxs-lookup"><span data-stu-id="0c225-153">**WNetEnumResource**</span></span>](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea) | <span data-ttu-id="0c225-154">繼續列舉 **WNetOpenEnum** 函式所啟動的網路資源。</span><span class="sxs-lookup"><span data-stu-id="0c225-154">Continues an enumeration of network resources started by the **WNetOpenEnum** function.</span></span> |
| [<span data-ttu-id="0c225-155">**WNetOpenEnum**</span><span class="sxs-lookup"><span data-stu-id="0c225-155">**WNetOpenEnum**</span></span>](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma)         | <span data-ttu-id="0c225-156">啟動網路資源的列舉。</span><span class="sxs-lookup"><span data-stu-id="0c225-156">Starts an enumeration of network resources.</span></span>                                             |



 

## <a name="information-functions"></a><span data-ttu-id="0c225-157">資訊函數</span><span class="sxs-lookup"><span data-stu-id="0c225-157">Information Functions</span></span>

<span data-ttu-id="0c225-158">呼叫下列 WNet 資訊和公用程式函式，以取得網路提供者和其他資訊。</span><span class="sxs-lookup"><span data-stu-id="0c225-158">Call the following WNet informational and utility functions to retrieve network provider and other information.</span></span>



| <span data-ttu-id="0c225-159">函式</span><span class="sxs-lookup"><span data-stu-id="0c225-159">Function</span></span>                                                         | <span data-ttu-id="0c225-160">描述</span><span class="sxs-lookup"><span data-stu-id="0c225-160">Description</span></span>                                                                                         |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0c225-161">**WNetGetLastError**</span><span class="sxs-lookup"><span data-stu-id="0c225-161">**WNetGetLastError**</span></span>](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetlasterrora)                     | <span data-ttu-id="0c225-162">傳回由網路提供者所報告的 WNet 函式所設定的最新錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="0c225-162">Returns the most recent error code set by a WNet function, the one reported by a network provider.</span></span>  |
| [<span data-ttu-id="0c225-163">**WNetGetNetworkInformation**</span><span class="sxs-lookup"><span data-stu-id="0c225-163">**WNetGetNetworkInformation**</span></span>](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetnetworkinformationa)   | <span data-ttu-id="0c225-164">傳回與特定網路提供者相關的擴充資訊。</span><span class="sxs-lookup"><span data-stu-id="0c225-164">Returns extended information about a specific network provider.</span></span>                                     |
| [<span data-ttu-id="0c225-165">**WNetGetProviderName**</span><span class="sxs-lookup"><span data-stu-id="0c225-165">**WNetGetProviderName**</span></span>](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetprovidernamea)               | <span data-ttu-id="0c225-166">傳回特定網路類型的提供者名稱。</span><span class="sxs-lookup"><span data-stu-id="0c225-166">Returns the provider name for a specific type of network.</span></span>                                           |
| [<span data-ttu-id="0c225-167">**WNetGetResourceInformation**</span><span class="sxs-lookup"><span data-stu-id="0c225-167">**WNetGetResourceInformation**</span></span>](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetresourceinformationa) | <span data-ttu-id="0c225-168">傳回擁有資源的網路提供者，並取得資源類型的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="0c225-168">Returns the network provider that owns a resource, and obtains information about the resource type.</span></span> |
| [<span data-ttu-id="0c225-169">**WNetGetResourceParent**</span><span class="sxs-lookup"><span data-stu-id="0c225-169">**WNetGetResourceParent**</span></span>](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetresourceparenta)           | <span data-ttu-id="0c225-170">傳回網路資源的父系。</span><span class="sxs-lookup"><span data-stu-id="0c225-170">Returns the parent of a network resource.</span></span>                                                           |



 

## <a name="user-functions"></a><span data-ttu-id="0c225-171">使用者函式</span><span class="sxs-lookup"><span data-stu-id="0c225-171">User Functions</span></span>

<span data-ttu-id="0c225-172">呼叫下列 WNet 函式，以取得與本機裝置相關聯的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="0c225-172">Call the following WNet function to retrieve the name of the user associated with a local device.</span></span>



| <span data-ttu-id="0c225-173">函式</span><span class="sxs-lookup"><span data-stu-id="0c225-173">Function</span></span>                           | <span data-ttu-id="0c225-174">描述</span><span class="sxs-lookup"><span data-stu-id="0c225-174">Description</span></span>                                                                              |
|------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0c225-175">**WNetGetUser**</span><span class="sxs-lookup"><span data-stu-id="0c225-175">**WNetGetUser**</span></span>](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetusera) | <span data-ttu-id="0c225-176">傳回目前的預設使用者名稱，或建立連接的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="0c225-176">Returns the current default user name, or the user name that established the connection.</span></span> |



 

<span data-ttu-id="0c225-177">許多 WNet 函數會使用 [**NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) 結構來儲存網路資源的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="0c225-177">Many of the WNet functions use a [**NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) structure to store information about a network resource.</span></span>

 

 
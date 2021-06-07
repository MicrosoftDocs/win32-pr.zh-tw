---
description: 所有服務提供者都必須執行基本的電話語音功能。
ms.assetid: 4250f3a0-a66a-4a6e-8566-d71be7463179
title: TSPI 基本電話語音功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5308def0c94df9fa59f2022bf25c4dbb1843e2f8
ms.sourcegitcommit: 8ebcf6cd36f67f8bcf78e76ae8923d65b8995c8a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/05/2021
ms.locfileid: "111524152"
---
# <a name="tspi-basic-telephony-functions"></a><span data-ttu-id="88f14-103">TSPI 基本電話語音功能</span><span class="sxs-lookup"><span data-stu-id="88f14-103">TSPI Basic Telephony Functions</span></span>

<span data-ttu-id="88f14-104">所有服務提供者都必須執行基本的電話語音功能。</span><span class="sxs-lookup"><span data-stu-id="88f14-104">All service providers must implement Basic Telephony functions.</span></span> <span data-ttu-id="88f14-105">以下是依類別分類的功能清單。</span><span class="sxs-lookup"><span data-stu-id="88f14-105">The following is a list of such functions by category.</span></span> <span data-ttu-id="88f14-106">如果函式指出已在應用程式的回復訊息中完成，則會將函數識別為 *非同步* 。</span><span class="sxs-lookup"><span data-stu-id="88f14-106">A function is identified as *asynchronous* if it indicates completion in a REPLY message to the application.</span></span> <span data-ttu-id="88f14-107">如果函式一律會立即傳回其結果，則函式會被視為 *同步*。</span><span class="sxs-lookup"><span data-stu-id="88f14-107">If the function always returns its result immediately, the function is considered *synchronous*.</span></span>

-   [<span data-ttu-id="88f14-108">位址</span><span class="sxs-lookup"><span data-stu-id="88f14-108">Addresses</span></span>](#addresses)
-   [<span data-ttu-id="88f14-109">接聽撥入電話</span><span class="sxs-lookup"><span data-stu-id="88f14-109">Answering Incoming Calls</span></span>](#answering-incoming-calls)
-   [<span data-ttu-id="88f14-110">呼叫 Drop 函數</span><span class="sxs-lookup"><span data-stu-id="88f14-110">Call Drop Functions</span></span>](#call-drop-functions)
-   [<span data-ttu-id="88f14-111">撥號狀態和事件</span><span class="sxs-lookup"><span data-stu-id="88f14-111">Call States and Events</span></span>](#call-states-and-events)
-   [<span data-ttu-id="88f14-112">線路狀態和功能</span><span class="sxs-lookup"><span data-stu-id="88f14-112">Line Status and Capabilities</span></span>](#line-status-and-capabilities)
-   [<span data-ttu-id="88f14-113">行版本協商</span><span class="sxs-lookup"><span data-stu-id="88f14-113">Line Version Negotiation</span></span>](#line-version-negotiation)
-   [<span data-ttu-id="88f14-114">進行呼叫</span><span class="sxs-lookup"><span data-stu-id="88f14-114">Making Calls</span></span>](#making-calls)
-   [<span data-ttu-id="88f14-115">開啟和關閉行裝置</span><span class="sxs-lookup"><span data-stu-id="88f14-115">Opening and Closing Line Devices</span></span>](#opening-and-closing-line-devices)
-   [<span data-ttu-id="88f14-116">電話版本協商</span><span class="sxs-lookup"><span data-stu-id="88f14-116">Phone Version Negotiation</span></span>](#phone-version-negotiation)
-   [<span data-ttu-id="88f14-117">TSP 初始化和關機</span><span class="sxs-lookup"><span data-stu-id="88f14-117">TSP Initialization and Shutdown</span></span>](#tsp-initialization-and-shutdown)

## <a name="tsp-initialization-and-shutdown"></a><span data-ttu-id="88f14-118">TSP 初始化和關機</span><span class="sxs-lookup"><span data-stu-id="88f14-118">TSP Initialization and Shutdown</span></span>



|  <span data-ttu-id="88f14-119">函式</span><span class="sxs-lookup"><span data-stu-id="88f14-119">Function</span></span>                                                         |   <span data-ttu-id="88f14-120">描述</span><span class="sxs-lookup"><span data-stu-id="88f14-120">Description</span></span>                                                        |
|-----------------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="88f14-121">**TUISPI \_ providerInstall**</span><span class="sxs-lookup"><span data-stu-id="88f14-121">**TUISPI\_providerInstall**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_providerinstall) | <span data-ttu-id="88f14-122">安裝 TSP。</span><span class="sxs-lookup"><span data-stu-id="88f14-122">Installs a TSP.</span></span> <span data-ttu-id="88f14-123">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="88f14-123">Synchronous.</span></span>                              |
| [<span data-ttu-id="88f14-124">**TSPI \_ providerInstall**</span><span class="sxs-lookup"><span data-stu-id="88f14-124">**TSPI\_providerInstall**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providerinstall)     | <span data-ttu-id="88f14-125">安裝 TSP。</span><span class="sxs-lookup"><span data-stu-id="88f14-125">Installs the TSP.</span></span> <span data-ttu-id="88f14-126">版本2.0 已淘汰。</span><span class="sxs-lookup"><span data-stu-id="88f14-126">Obsolete with Version 2.0.</span></span> <span data-ttu-id="88f14-127">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="88f14-127">Synchronous.</span></span> |
| [<span data-ttu-id="88f14-128">**TSPI \_ providerInit**</span><span class="sxs-lookup"><span data-stu-id="88f14-128">**TSPI\_providerInit**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providerinit)           | <span data-ttu-id="88f14-129">初始化 TSP。</span><span class="sxs-lookup"><span data-stu-id="88f14-129">Initializes the TSP.</span></span> <span data-ttu-id="88f14-130">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="88f14-130">Synchronous.</span></span>                         |
| [<span data-ttu-id="88f14-131">**TSPI \_ providerShutdown**</span><span class="sxs-lookup"><span data-stu-id="88f14-131">**TSPI\_providerShutdown**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providershutdown)   | <span data-ttu-id="88f14-132">關閉服務提供者。</span><span class="sxs-lookup"><span data-stu-id="88f14-132">Shuts down the service provider.</span></span>                          |
| [<span data-ttu-id="88f14-133">**TUISPI \_ providerRemove**</span><span class="sxs-lookup"><span data-stu-id="88f14-133">**TUISPI\_providerRemove**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_providerremove)   | <span data-ttu-id="88f14-134">移除 TSP。</span><span class="sxs-lookup"><span data-stu-id="88f14-134">Removes a TSP.</span></span> <span data-ttu-id="88f14-135">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="88f14-135">Synchronous.</span></span>                               |
| [<span data-ttu-id="88f14-136">**TSPI \_ providerRemove**</span><span class="sxs-lookup"><span data-stu-id="88f14-136">**TSPI\_providerRemove**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providerremove)       | <span data-ttu-id="88f14-137">移除 TSP。</span><span class="sxs-lookup"><span data-stu-id="88f14-137">Removes a TSP.</span></span> <span data-ttu-id="88f14-138">版本2.0 已淘汰。</span><span class="sxs-lookup"><span data-stu-id="88f14-138">Obsolete with Version 2.0.</span></span> <span data-ttu-id="88f14-139">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="88f14-139">Synchronous.</span></span>    |



 

## <a name="phone-version-negotiation"></a><span data-ttu-id="88f14-140">電話版本協商</span><span class="sxs-lookup"><span data-stu-id="88f14-140">Phone Version Negotiation</span></span>



|  <span data-ttu-id="88f14-141">函式</span><span class="sxs-lookup"><span data-stu-id="88f14-141">Function</span></span>                                                         |   <span data-ttu-id="88f14-142">描述</span><span class="sxs-lookup"><span data-stu-id="88f14-142">Description</span></span>                                                        |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="88f14-143">**TSPI \_ phoneNegotiateTSPIVersion**</span><span class="sxs-lookup"><span data-stu-id="88f14-143">**TSPI\_phoneNegotiateTSPIVersion**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_phonenegotiatetspiversion) | <span data-ttu-id="88f14-144">傳回服務提供者在此裝置下可運作的最高 SPI 版本。</span><span class="sxs-lookup"><span data-stu-id="88f14-144">Returns the highest SPI version the service provider can operate under for this device.</span></span> |



 

## <a name="line-version-negotiation"></a><span data-ttu-id="88f14-145">行版本協商</span><span class="sxs-lookup"><span data-stu-id="88f14-145">Line Version Negotiation</span></span>



|  <span data-ttu-id="88f14-146">函式</span><span class="sxs-lookup"><span data-stu-id="88f14-146">Function</span></span>                                                         |   <span data-ttu-id="88f14-147">描述</span><span class="sxs-lookup"><span data-stu-id="88f14-147">Description</span></span>                                                        |
|-------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="88f14-148">**TSPI \_ lineNegotiateTSPIVersion**</span><span class="sxs-lookup"><span data-stu-id="88f14-148">**TSPI\_lineNegotiateTSPIVersion**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiatetspiversion) | <span data-ttu-id="88f14-149">允許應用程式與指定的線路裝置協調使用 TSPI 版本。</span><span class="sxs-lookup"><span data-stu-id="88f14-149">Allows an application to negotiate a TSPI version to use with a given line device.</span></span> <span data-ttu-id="88f14-150">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="88f14-150">Synchronous.</span></span> |



 

## <a name="line-status-and-capabilities"></a><span data-ttu-id="88f14-151">線路狀態和功能</span><span class="sxs-lookup"><span data-stu-id="88f14-151">Line Status and Capabilities</span></span>



|  <span data-ttu-id="88f14-152">函式</span><span class="sxs-lookup"><span data-stu-id="88f14-152">Function</span></span>                                                         |   <span data-ttu-id="88f14-153">描述</span><span class="sxs-lookup"><span data-stu-id="88f14-153">Description</span></span>                                                        |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="88f14-154">**TSPI \_ lineGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="88f14-154">**TSPI\_lineGetDevCaps**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevcaps)                 | <span data-ttu-id="88f14-155">傳回指定線路裝置的功能。</span><span class="sxs-lookup"><span data-stu-id="88f14-155">Returns the capabilities of a given line device.</span></span> <span data-ttu-id="88f14-156">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="88f14-156">Synchronous.</span></span>                                                                                                  |
| [<span data-ttu-id="88f14-157">**TSPI \_ lineGetDevConfig**</span><span class="sxs-lookup"><span data-stu-id="88f14-157">**TSPI\_lineGetDevConfig**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevconfig)             | <span data-ttu-id="88f14-158">傳回媒體資料流程裝置的設定。</span><span class="sxs-lookup"><span data-stu-id="88f14-158">Returns configuration of a media stream device.</span></span> <span data-ttu-id="88f14-159">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="88f14-159">Synchronous.</span></span>                                                                                                   |
| [<span data-ttu-id="88f14-160">**TSPI \_ lineGetLineDevStatus**</span><span class="sxs-lookup"><span data-stu-id="88f14-160">**TSPI\_lineGetLineDevStatus**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetlinedevstatus)     | <span data-ttu-id="88f14-161">傳回指定之開啟行裝置的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="88f14-161">Returns current status of the specified open line device.</span></span> <span data-ttu-id="88f14-162">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="88f14-162">Synchronous.</span></span>                                                                                         |
| [<span data-ttu-id="88f14-163">**TSPI \_ lineSetDevConfig**</span><span class="sxs-lookup"><span data-stu-id="88f14-163">**TSPI\_lineSetDevConfig**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetdevconfig)             | <span data-ttu-id="88f14-164">設定指定媒體串流裝置的設定。</span><span class="sxs-lookup"><span data-stu-id="88f14-164">Sets the configuration of the specified media stream device.</span></span> <span data-ttu-id="88f14-165">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="88f14-165">Synchronous.</span></span>                                                                                      |
| [<span data-ttu-id="88f14-166">**TSPI \_ lineSetStatusMessages**</span><span class="sxs-lookup"><span data-stu-id="88f14-166">**TSPI\_lineSetStatusMessages**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetstatusmessages)   | <span data-ttu-id="88f14-167">指定應用程式需要通知的狀態變更。</span><span class="sxs-lookup"><span data-stu-id="88f14-167">Specifies the status changes for which the application needs to be notified.</span></span> <span data-ttu-id="88f14-168">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="88f14-168">Synchronous.</span></span>                                                                      |
| [<span data-ttu-id="88f14-169">**TSPI \_ lineGetID**</span><span class="sxs-lookup"><span data-stu-id="88f14-169">**TSPI\_lineGetID**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetid)                           | <span data-ttu-id="88f14-170">抓取與指定的開啟行、位址或呼叫相關聯的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="88f14-170">Retrieves a device ID associated with the specified open line, address, or call.</span></span> <span data-ttu-id="88f14-171">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="88f14-171">Synchronous.</span></span>                                                                  |
| [<span data-ttu-id="88f14-172">**TSPI \_ lineGetIcon**</span><span class="sxs-lookup"><span data-stu-id="88f14-172">**TSPI\_lineGetIcon**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegeticon)                       | <span data-ttu-id="88f14-173">允許應用程式抓取顯示給使用者的圖示。</span><span class="sxs-lookup"><span data-stu-id="88f14-173">Allows an application to retrieve an icon for display to the user.</span></span> <span data-ttu-id="88f14-174">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="88f14-174">Synchronous.</span></span>                                                                                |
| [<span data-ttu-id="88f14-175">**TUISPI \_ lineConfigDialog**</span><span class="sxs-lookup"><span data-stu-id="88f14-175">**TUISPI\_lineConfigDialog**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialog)         | <span data-ttu-id="88f14-176">使指定行裝置的提供者顯示對話方塊，讓使用者能夠設定與線路裝置相關的參數。</span><span class="sxs-lookup"><span data-stu-id="88f14-176">Causes the provider of the specified line device to display a dialog box that allows the user to configure parameters related to the line device.</span></span> <span data-ttu-id="88f14-177">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="88f14-177">Synchronous.</span></span> |
| [<span data-ttu-id="88f14-178">**TUISPI \_ lineConfigDialogEdit**</span><span class="sxs-lookup"><span data-stu-id="88f14-178">**TUISPI\_lineConfigDialogEdit**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialogedit) | <span data-ttu-id="88f14-179">顯示對話方塊，讓使用者變更線路裝置的設定資訊。</span><span class="sxs-lookup"><span data-stu-id="88f14-179">Displays a dialog box allowing the user to change configuration information for a line device.</span></span> <span data-ttu-id="88f14-180">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="88f14-180">Synchronous.</span></span>                                                    |



 

## <a name="addresses"></a><span data-ttu-id="88f14-181">位址</span><span class="sxs-lookup"><span data-stu-id="88f14-181">Addresses</span></span>



|  <span data-ttu-id="88f14-182">函式</span><span class="sxs-lookup"><span data-stu-id="88f14-182">Function</span></span>                                                         |   <span data-ttu-id="88f14-183">描述</span><span class="sxs-lookup"><span data-stu-id="88f14-183">Description</span></span>                                                        |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="88f14-184">**TSPI \_ lineGetAddressCaps**</span><span class="sxs-lookup"><span data-stu-id="88f14-184">**TSPI\_lineGetAddressCaps**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddresscaps)     | <span data-ttu-id="88f14-185">傳回位址的電話語音功能。</span><span class="sxs-lookup"><span data-stu-id="88f14-185">Returns the telephony capabilities of an address.</span></span> <span data-ttu-id="88f14-186">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="88f14-186">Synchronous.</span></span>                           |
| [<span data-ttu-id="88f14-187">**TSPI \_ lineGetAddressStatus**</span><span class="sxs-lookup"><span data-stu-id="88f14-187">**TSPI\_lineGetAddressStatus**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddressstatus) | <span data-ttu-id="88f14-188">傳回指定之位址的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="88f14-188">Returns current status of a specified address.</span></span> <span data-ttu-id="88f14-189">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="88f14-189">Synchronous.</span></span>                              |
| [<span data-ttu-id="88f14-190">**TSPI \_ lineGetNumAddressIDs**</span><span class="sxs-lookup"><span data-stu-id="88f14-190">**TSPI\_lineGetNumAddressIDs**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetnumaddressids) | <span data-ttu-id="88f14-191">抓取指定行所支援的位址識別碼數目。</span><span class="sxs-lookup"><span data-stu-id="88f14-191">Retrieves the number of address identifiers supported on the indicated line.</span></span>             |
| [<span data-ttu-id="88f14-192">**TSPI \_ lineGetAddressID**</span><span class="sxs-lookup"><span data-stu-id="88f14-192">**TSPI\_lineGetAddressID**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddressid)         | <span data-ttu-id="88f14-193">使用替代格式抓取指定位址的位址識別碼。</span><span class="sxs-lookup"><span data-stu-id="88f14-193">Retrieves the address ID of an address specified using an alternate format.</span></span> <span data-ttu-id="88f14-194">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="88f14-194">Synchronous.</span></span> |



 

## <a name="opening-and-closing-line-devices"></a><span data-ttu-id="88f14-195">開啟和關閉行裝置</span><span class="sxs-lookup"><span data-stu-id="88f14-195">Opening and Closing Line Devices</span></span>



|  <span data-ttu-id="88f14-196">函式</span><span class="sxs-lookup"><span data-stu-id="88f14-196">Function</span></span>                                                         |   <span data-ttu-id="88f14-197">描述</span><span class="sxs-lookup"><span data-stu-id="88f14-197">Description</span></span>                                                        |
|-------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="88f14-198">**TSPI \_ lineOpen**</span><span class="sxs-lookup"><span data-stu-id="88f14-198">**TSPI\_lineOpen**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineopen)   | <span data-ttu-id="88f14-199">開啟指定的線路裝置，以提供後續的監視及/或控制行。</span><span class="sxs-lookup"><span data-stu-id="88f14-199">Opens a specified line device for providing subsequent monitoring and/or control of the line.</span></span> <span data-ttu-id="88f14-200">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="88f14-200">Synchronous.</span></span> |
| [<span data-ttu-id="88f14-201">**TSPI \_ lineClose**</span><span class="sxs-lookup"><span data-stu-id="88f14-201">**TSPI\_lineClose**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineclose) | <span data-ttu-id="88f14-202">關閉指定的已開啟行裝置。</span><span class="sxs-lookup"><span data-stu-id="88f14-202">Closes a specified opened line device.</span></span> <span data-ttu-id="88f14-203">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="88f14-203">Synchronous.</span></span>                                                        |



 

## <a name="call-states-and-events"></a><span data-ttu-id="88f14-204">撥號狀態和事件</span><span class="sxs-lookup"><span data-stu-id="88f14-204">Call States and Events</span></span>



|  <span data-ttu-id="88f14-205">函式</span><span class="sxs-lookup"><span data-stu-id="88f14-205">Function</span></span>                                                         |   <span data-ttu-id="88f14-206">描述</span><span class="sxs-lookup"><span data-stu-id="88f14-206">Description</span></span>                                                        |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="88f14-207">**TSPI \_ lineGetCallInfo**</span><span class="sxs-lookup"><span data-stu-id="88f14-207">**TSPI\_lineGetCallInfo**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallinfo)       | <span data-ttu-id="88f14-208">傳回有關呼叫的固定資訊。</span><span class="sxs-lookup"><span data-stu-id="88f14-208">Returns fixed information about a call.</span></span> <span data-ttu-id="88f14-209">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="88f14-209">Synchronous.</span></span>                                |
| [<span data-ttu-id="88f14-210">**TSPI \_ lineGetCallStatus**</span><span class="sxs-lookup"><span data-stu-id="88f14-210">**TSPI\_lineGetCallStatus**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallstatus)   | <span data-ttu-id="88f14-211">傳回指定之呼叫的完整撥號狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="88f14-211">Returns complete call status information for the specified call.</span></span> <span data-ttu-id="88f14-212">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="88f14-212">Synchronous.</span></span>       |
| [<span data-ttu-id="88f14-213">**TSPI \_ lineSetAppSpecific**</span><span class="sxs-lookup"><span data-stu-id="88f14-213">**TSPI\_lineSetAppSpecific**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetappspecific) | <span data-ttu-id="88f14-214">設定呼叫資訊結構的應用程式特定欄位。</span><span class="sxs-lookup"><span data-stu-id="88f14-214">Sets the application-specific field of a call's information structure.</span></span> <span data-ttu-id="88f14-215">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="88f14-215">Synchronous.</span></span> |



 

## <a name="making-calls"></a><span data-ttu-id="88f14-216">進行呼叫</span><span class="sxs-lookup"><span data-stu-id="88f14-216">Making Calls</span></span>



|  <span data-ttu-id="88f14-217">函式</span><span class="sxs-lookup"><span data-stu-id="88f14-217">Function</span></span>                                                         |   <span data-ttu-id="88f14-218">描述</span><span class="sxs-lookup"><span data-stu-id="88f14-218">Description</span></span>                                                        |
|-------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="88f14-219">**TSPI \_ lineMakeCall**</span><span class="sxs-lookup"><span data-stu-id="88f14-219">**TSPI\_lineMakeCall**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall) | <span data-ttu-id="88f14-220">進行輸出呼叫，並傳回它的呼叫控制碼。</span><span class="sxs-lookup"><span data-stu-id="88f14-220">Makes an outbound call and returns a call handle for it.</span></span> <span data-ttu-id="88f14-221">非同步：</span><span class="sxs-lookup"><span data-stu-id="88f14-221">Asynchronous.</span></span> |
| [<span data-ttu-id="88f14-222">**TSPI \_ lineDial**</span><span class="sxs-lookup"><span data-stu-id="88f14-222">**TSPI\_lineDial**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linedial)         | <span data-ttu-id="88f14-223">撥打一或多個) 的位址 (部分。</span><span class="sxs-lookup"><span data-stu-id="88f14-223">Dials (parts of one or more) dialable addresses.</span></span> <span data-ttu-id="88f14-224">非同步：</span><span class="sxs-lookup"><span data-stu-id="88f14-224">Asynchronous.</span></span>         |



 

## <a name="answering-incoming-calls"></a><span data-ttu-id="88f14-225">接聽撥入電話</span><span class="sxs-lookup"><span data-stu-id="88f14-225">Answering Incoming Calls</span></span>



|  <span data-ttu-id="88f14-226">函式</span><span class="sxs-lookup"><span data-stu-id="88f14-226">Function</span></span>                                                         |   <span data-ttu-id="88f14-227">描述</span><span class="sxs-lookup"><span data-stu-id="88f14-227">Description</span></span>                                                        |
|---------------------------------------------|-----------------------------------------|
| [<span data-ttu-id="88f14-228">**TSPI \_ lineAnswer**</span><span class="sxs-lookup"><span data-stu-id="88f14-228">**TSPI\_lineAnswer**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineanswer) | <span data-ttu-id="88f14-229">回答來電。</span><span class="sxs-lookup"><span data-stu-id="88f14-229">Answers an incoming call.</span></span> <span data-ttu-id="88f14-230">非同步：</span><span class="sxs-lookup"><span data-stu-id="88f14-230">Asynchronous.</span></span> |



 

## <a name="call-drop-functions"></a><span data-ttu-id="88f14-231">呼叫 Drop 函數</span><span class="sxs-lookup"><span data-stu-id="88f14-231">Call Drop Functions</span></span>



|  <span data-ttu-id="88f14-232">函式</span><span class="sxs-lookup"><span data-stu-id="88f14-232">Function</span></span>                                                         |   <span data-ttu-id="88f14-233">描述</span><span class="sxs-lookup"><span data-stu-id="88f14-233">Description</span></span>                                                        |
|-----------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="88f14-234">**TSPI \_ lineDrop**</span><span class="sxs-lookup"><span data-stu-id="88f14-234">**TSPI\_lineDrop**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linedrop) | <span data-ttu-id="88f14-235">中斷通話的連線，或放棄進行中的呼叫嘗試。</span><span class="sxs-lookup"><span data-stu-id="88f14-235">Disconnects a call, or abandons a call attempt in progress.</span></span> <span data-ttu-id="88f14-236">非同步：</span><span class="sxs-lookup"><span data-stu-id="88f14-236">Asynchronous.</span></span> |



 

 

 

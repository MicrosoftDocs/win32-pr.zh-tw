---
description: 所有服務提供者都必須執行基本的電話語音功能。
ms.assetid: 4250f3a0-a66a-4a6e-8566-d71be7463179
title: TSPI 基本電話語音功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6276be51482620af32650ad1625eea97bddb8e5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852483"
---
# <a name="tspi-basic-telephony-functions"></a><span data-ttu-id="d71b3-103">TSPI 基本電話語音功能</span><span class="sxs-lookup"><span data-stu-id="d71b3-103">TSPI Basic Telephony Functions</span></span>

<span data-ttu-id="d71b3-104">所有服務提供者都必須執行基本的電話語音功能。</span><span class="sxs-lookup"><span data-stu-id="d71b3-104">All service providers must implement Basic Telephony functions.</span></span> <span data-ttu-id="d71b3-105">以下是依類別分類的功能清單。</span><span class="sxs-lookup"><span data-stu-id="d71b3-105">The following is a list of such functions by category.</span></span> <span data-ttu-id="d71b3-106">如果函式指出已在應用程式的回復訊息中完成，則會將函數識別為 *非同步* 。</span><span class="sxs-lookup"><span data-stu-id="d71b3-106">A function is identified as *asynchronous* if it indicates completion in a REPLY message to the application.</span></span> <span data-ttu-id="d71b3-107">如果函式一律會立即傳回其結果，則函式會被視為 *同步*。</span><span class="sxs-lookup"><span data-stu-id="d71b3-107">If the function always returns its result immediately, the function is considered *synchronous*.</span></span>

-   [<span data-ttu-id="d71b3-108">位址</span><span class="sxs-lookup"><span data-stu-id="d71b3-108">Addresses</span></span>](#addresses)
-   [<span data-ttu-id="d71b3-109">接聽撥入電話</span><span class="sxs-lookup"><span data-stu-id="d71b3-109">Answering Incoming Calls</span></span>](#answering-incoming-calls)
-   [<span data-ttu-id="d71b3-110">呼叫 Drop 函數</span><span class="sxs-lookup"><span data-stu-id="d71b3-110">Call Drop Functions</span></span>](#call-drop-functions)
-   [<span data-ttu-id="d71b3-111">撥號狀態和事件</span><span class="sxs-lookup"><span data-stu-id="d71b3-111">Call States and Events</span></span>](#call-states-and-events)
-   [<span data-ttu-id="d71b3-112">線路狀態和功能</span><span class="sxs-lookup"><span data-stu-id="d71b3-112">Line Status and Capabilities</span></span>](#line-status-and-capabilities)
-   [<span data-ttu-id="d71b3-113">行版本協商</span><span class="sxs-lookup"><span data-stu-id="d71b3-113">Line Version Negotiation</span></span>](#line-version-negotiation)
-   [<span data-ttu-id="d71b3-114">進行呼叫</span><span class="sxs-lookup"><span data-stu-id="d71b3-114">Making Calls</span></span>](#making-calls)
-   [<span data-ttu-id="d71b3-115">開啟和關閉行裝置</span><span class="sxs-lookup"><span data-stu-id="d71b3-115">Opening and Closing Line Devices</span></span>](#opening-and-closing-line-devices)
-   [<span data-ttu-id="d71b3-116">電話版本協商</span><span class="sxs-lookup"><span data-stu-id="d71b3-116">Phone Version Negotiation</span></span>](#phone-version-negotiation)
-   [<span data-ttu-id="d71b3-117">TSP 初始化和關機</span><span class="sxs-lookup"><span data-stu-id="d71b3-117">TSP Initialization and Shutdown</span></span>](#tsp-initialization-and-shutdown)

## <a name="tsp-initialization-and-shutdown"></a><span data-ttu-id="d71b3-118">TSP 初始化和關機</span><span class="sxs-lookup"><span data-stu-id="d71b3-118">TSP Initialization and Shutdown</span></span>



|                                                           |                                                           |
|-----------------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="d71b3-119">**TUISPI \_ providerInstall**</span><span class="sxs-lookup"><span data-stu-id="d71b3-119">**TUISPI\_providerInstall**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_providerinstall) | <span data-ttu-id="d71b3-120">安裝 TSP。</span><span class="sxs-lookup"><span data-stu-id="d71b3-120">Installs a TSP.</span></span> <span data-ttu-id="d71b3-121">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="d71b3-121">Synchronous.</span></span>                              |
| [<span data-ttu-id="d71b3-122">**TSPI \_ providerInstall**</span><span class="sxs-lookup"><span data-stu-id="d71b3-122">**TSPI\_providerInstall**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providerinstall)     | <span data-ttu-id="d71b3-123">安裝 TSP。</span><span class="sxs-lookup"><span data-stu-id="d71b3-123">Installs the TSP.</span></span> <span data-ttu-id="d71b3-124">版本2.0 已淘汰。</span><span class="sxs-lookup"><span data-stu-id="d71b3-124">Obsolete with Version 2.0.</span></span> <span data-ttu-id="d71b3-125">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="d71b3-125">Synchronous.</span></span> |
| [<span data-ttu-id="d71b3-126">**TSPI \_ providerInit**</span><span class="sxs-lookup"><span data-stu-id="d71b3-126">**TSPI\_providerInit**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providerinit)           | <span data-ttu-id="d71b3-127">初始化 TSP。</span><span class="sxs-lookup"><span data-stu-id="d71b3-127">Initializes the TSP.</span></span> <span data-ttu-id="d71b3-128">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="d71b3-128">Synchronous.</span></span>                         |
| [<span data-ttu-id="d71b3-129">**TSPI \_ providerShutdown**</span><span class="sxs-lookup"><span data-stu-id="d71b3-129">**TSPI\_providerShutdown**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providershutdown)   | <span data-ttu-id="d71b3-130">關閉服務提供者。</span><span class="sxs-lookup"><span data-stu-id="d71b3-130">Shuts down the service provider.</span></span>                          |
| [<span data-ttu-id="d71b3-131">**TUISPI \_ providerRemove**</span><span class="sxs-lookup"><span data-stu-id="d71b3-131">**TUISPI\_providerRemove**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_providerremove)   | <span data-ttu-id="d71b3-132">移除 TSP。</span><span class="sxs-lookup"><span data-stu-id="d71b3-132">Removes a TSP.</span></span> <span data-ttu-id="d71b3-133">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="d71b3-133">Synchronous.</span></span>                               |
| [<span data-ttu-id="d71b3-134">**TSPI \_ providerRemove**</span><span class="sxs-lookup"><span data-stu-id="d71b3-134">**TSPI\_providerRemove**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providerremove)       | <span data-ttu-id="d71b3-135">移除 TSP。</span><span class="sxs-lookup"><span data-stu-id="d71b3-135">Removes a TSP.</span></span> <span data-ttu-id="d71b3-136">版本2.0 已淘汰。</span><span class="sxs-lookup"><span data-stu-id="d71b3-136">Obsolete with Version 2.0.</span></span> <span data-ttu-id="d71b3-137">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="d71b3-137">Synchronous.</span></span>    |



 

## <a name="phone-version-negotiation"></a><span data-ttu-id="d71b3-138">電話版本協商</span><span class="sxs-lookup"><span data-stu-id="d71b3-138">Phone Version Negotiation</span></span>



|                                                                           |                                                                                         |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="d71b3-139">**TSPI \_ phoneNegotiateTSPIVersion**</span><span class="sxs-lookup"><span data-stu-id="d71b3-139">**TSPI\_phoneNegotiateTSPIVersion**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_phonenegotiatetspiversion) | <span data-ttu-id="d71b3-140">傳回服務提供者在此裝置下可運作的最高 SPI 版本。</span><span class="sxs-lookup"><span data-stu-id="d71b3-140">Returns the highest SPI version the service provider can operate under for this device.</span></span> |



 

## <a name="line-version-negotiation"></a><span data-ttu-id="d71b3-141">行版本協商</span><span class="sxs-lookup"><span data-stu-id="d71b3-141">Line Version Negotiation</span></span>



|                                                                         |                                                                                                 |
|-------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d71b3-142">**TSPI \_ lineNegotiateTSPIVersion**</span><span class="sxs-lookup"><span data-stu-id="d71b3-142">**TSPI\_lineNegotiateTSPIVersion**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiatetspiversion) | <span data-ttu-id="d71b3-143">允許應用程式與指定的線路裝置協調使用 TSPI 版本。</span><span class="sxs-lookup"><span data-stu-id="d71b3-143">Allows an application to negotiate a TSPI version to use with a given line device.</span></span> <span data-ttu-id="d71b3-144">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="d71b3-144">Synchronous.</span></span> |



 

## <a name="line-status-and-capabilities"></a><span data-ttu-id="d71b3-145">線路狀態和功能</span><span class="sxs-lookup"><span data-stu-id="d71b3-145">Line Status and Capabilities</span></span>



|                                                                     |                                                                                                                                                                |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d71b3-146">**TSPI \_ lineGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="d71b3-146">**TSPI\_lineGetDevCaps**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevcaps)                 | <span data-ttu-id="d71b3-147">傳回指定線路裝置的功能。</span><span class="sxs-lookup"><span data-stu-id="d71b3-147">Returns the capabilities of a given line device.</span></span> <span data-ttu-id="d71b3-148">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="d71b3-148">Synchronous.</span></span>                                                                                                  |
| [<span data-ttu-id="d71b3-149">**TSPI \_ lineGetDevConfig**</span><span class="sxs-lookup"><span data-stu-id="d71b3-149">**TSPI\_lineGetDevConfig**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevconfig)             | <span data-ttu-id="d71b3-150">傳回媒體資料流程裝置的設定。</span><span class="sxs-lookup"><span data-stu-id="d71b3-150">Returns configuration of a media stream device.</span></span> <span data-ttu-id="d71b3-151">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="d71b3-151">Synchronous.</span></span>                                                                                                   |
| [<span data-ttu-id="d71b3-152">**TSPI \_ lineGetLineDevStatus**</span><span class="sxs-lookup"><span data-stu-id="d71b3-152">**TSPI\_lineGetLineDevStatus**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetlinedevstatus)     | <span data-ttu-id="d71b3-153">傳回指定之開啟行裝置的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="d71b3-153">Returns current status of the specified open line device.</span></span> <span data-ttu-id="d71b3-154">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="d71b3-154">Synchronous.</span></span>                                                                                         |
| [<span data-ttu-id="d71b3-155">**TSPI \_ lineSetDevConfig**</span><span class="sxs-lookup"><span data-stu-id="d71b3-155">**TSPI\_lineSetDevConfig**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetdevconfig)             | <span data-ttu-id="d71b3-156">設定指定媒體串流裝置的設定。</span><span class="sxs-lookup"><span data-stu-id="d71b3-156">Sets the configuration of the specified media stream device.</span></span> <span data-ttu-id="d71b3-157">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="d71b3-157">Synchronous.</span></span>                                                                                      |
| [<span data-ttu-id="d71b3-158">**TSPI \_ lineSetStatusMessages**</span><span class="sxs-lookup"><span data-stu-id="d71b3-158">**TSPI\_lineSetStatusMessages**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetstatusmessages)   | <span data-ttu-id="d71b3-159">指定應用程式需要通知的狀態變更。</span><span class="sxs-lookup"><span data-stu-id="d71b3-159">Specifies the status changes for which the application needs to be notified.</span></span> <span data-ttu-id="d71b3-160">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="d71b3-160">Synchronous.</span></span>                                                                      |
| [<span data-ttu-id="d71b3-161">**TSPI \_ lineGetID**</span><span class="sxs-lookup"><span data-stu-id="d71b3-161">**TSPI\_lineGetID**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetid)                           | <span data-ttu-id="d71b3-162">抓取與指定的開啟行、位址或呼叫相關聯的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="d71b3-162">Retrieves a device ID associated with the specified open line, address, or call.</span></span> <span data-ttu-id="d71b3-163">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="d71b3-163">Synchronous.</span></span>                                                                  |
| [<span data-ttu-id="d71b3-164">**TSPI \_ lineGetIcon**</span><span class="sxs-lookup"><span data-stu-id="d71b3-164">**TSPI\_lineGetIcon**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegeticon)                       | <span data-ttu-id="d71b3-165">允許應用程式抓取顯示給使用者的圖示。</span><span class="sxs-lookup"><span data-stu-id="d71b3-165">Allows an application to retrieve an icon for display to the user.</span></span> <span data-ttu-id="d71b3-166">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="d71b3-166">Synchronous.</span></span>                                                                                |
| [<span data-ttu-id="d71b3-167">**TUISPI \_ lineConfigDialog**</span><span class="sxs-lookup"><span data-stu-id="d71b3-167">**TUISPI\_lineConfigDialog**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialog)         | <span data-ttu-id="d71b3-168">使指定行裝置的提供者顯示對話方塊，讓使用者能夠設定與線路裝置相關的參數。</span><span class="sxs-lookup"><span data-stu-id="d71b3-168">Causes the provider of the specified line device to display a dialog box that allows the user to configure parameters related to the line device.</span></span> <span data-ttu-id="d71b3-169">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="d71b3-169">Synchronous.</span></span> |
| [<span data-ttu-id="d71b3-170">**TUISPI \_ lineConfigDialogEdit**</span><span class="sxs-lookup"><span data-stu-id="d71b3-170">**TUISPI\_lineConfigDialogEdit**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialogedit) | <span data-ttu-id="d71b3-171">顯示對話方塊，讓使用者變更線路裝置的設定資訊。</span><span class="sxs-lookup"><span data-stu-id="d71b3-171">Displays a dialog box allowing the user to change configuration information for a line device.</span></span> <span data-ttu-id="d71b3-172">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="d71b3-172">Synchronous.</span></span>                                                    |



 

## <a name="addresses"></a><span data-ttu-id="d71b3-173">位址</span><span class="sxs-lookup"><span data-stu-id="d71b3-173">Addresses</span></span>



|                                                                 |                                                                                          |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d71b3-174">**TSPI \_ lineGetAddressCaps**</span><span class="sxs-lookup"><span data-stu-id="d71b3-174">**TSPI\_lineGetAddressCaps**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddresscaps)     | <span data-ttu-id="d71b3-175">傳回位址的電話語音功能。</span><span class="sxs-lookup"><span data-stu-id="d71b3-175">Returns the telephony capabilities of an address.</span></span> <span data-ttu-id="d71b3-176">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="d71b3-176">Synchronous.</span></span>                           |
| [<span data-ttu-id="d71b3-177">**TSPI \_ lineGetAddressStatus**</span><span class="sxs-lookup"><span data-stu-id="d71b3-177">**TSPI\_lineGetAddressStatus**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddressstatus) | <span data-ttu-id="d71b3-178">傳回指定之位址的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="d71b3-178">Returns current status of a specified address.</span></span> <span data-ttu-id="d71b3-179">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="d71b3-179">Synchronous.</span></span>                              |
| [<span data-ttu-id="d71b3-180">**TSPI \_ lineGetNumAddressIDs**</span><span class="sxs-lookup"><span data-stu-id="d71b3-180">**TSPI\_lineGetNumAddressIDs**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetnumaddressids) | <span data-ttu-id="d71b3-181">抓取指定行所支援的位址識別碼數目。</span><span class="sxs-lookup"><span data-stu-id="d71b3-181">Retrieves the number of address identifiers supported on the indicated line.</span></span>             |
| [<span data-ttu-id="d71b3-182">**TSPI \_ lineGetAddressID**</span><span class="sxs-lookup"><span data-stu-id="d71b3-182">**TSPI\_lineGetAddressID**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddressid)         | <span data-ttu-id="d71b3-183">使用替代格式抓取指定位址的位址識別碼。</span><span class="sxs-lookup"><span data-stu-id="d71b3-183">Retrieves the address ID of an address specified using an alternate format.</span></span> <span data-ttu-id="d71b3-184">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="d71b3-184">Synchronous.</span></span> |



 

## <a name="opening-and-closing-line-devices"></a><span data-ttu-id="d71b3-185">開啟和關閉行裝置</span><span class="sxs-lookup"><span data-stu-id="d71b3-185">Opening and Closing Line Devices</span></span>



|                                           |                                                                                                            |
|-------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d71b3-186">**TSPI \_ lineOpen**</span><span class="sxs-lookup"><span data-stu-id="d71b3-186">**TSPI\_lineOpen**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineopen)   | <span data-ttu-id="d71b3-187">開啟指定的線路裝置，以提供後續的監視及/或控制行。</span><span class="sxs-lookup"><span data-stu-id="d71b3-187">Opens a specified line device for providing subsequent monitoring and/or control of the line.</span></span> <span data-ttu-id="d71b3-188">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="d71b3-188">Synchronous.</span></span> |
| [<span data-ttu-id="d71b3-189">**TSPI \_ lineClose**</span><span class="sxs-lookup"><span data-stu-id="d71b3-189">**TSPI\_lineClose**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineclose) | <span data-ttu-id="d71b3-190">關閉指定的已開啟行裝置。</span><span class="sxs-lookup"><span data-stu-id="d71b3-190">Closes a specified opened line device.</span></span> <span data-ttu-id="d71b3-191">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="d71b3-191">Synchronous.</span></span>                                                        |



 

## <a name="call-states-and-events"></a><span data-ttu-id="d71b3-192">撥號狀態和事件</span><span class="sxs-lookup"><span data-stu-id="d71b3-192">Call States and Events</span></span>



|                                                             |                                                                                     |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="d71b3-193">**TSPI \_ lineGetCallInfo**</span><span class="sxs-lookup"><span data-stu-id="d71b3-193">**TSPI\_lineGetCallInfo**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallinfo)       | <span data-ttu-id="d71b3-194">傳回有關呼叫的固定資訊。</span><span class="sxs-lookup"><span data-stu-id="d71b3-194">Returns fixed information about a call.</span></span> <span data-ttu-id="d71b3-195">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="d71b3-195">Synchronous.</span></span>                                |
| [<span data-ttu-id="d71b3-196">**TSPI \_ lineGetCallStatus**</span><span class="sxs-lookup"><span data-stu-id="d71b3-196">**TSPI\_lineGetCallStatus**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallstatus)   | <span data-ttu-id="d71b3-197">傳回指定之呼叫的完整撥號狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="d71b3-197">Returns complete call status information for the specified call.</span></span> <span data-ttu-id="d71b3-198">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="d71b3-198">Synchronous.</span></span>       |
| [<span data-ttu-id="d71b3-199">**TSPI \_ lineSetAppSpecific**</span><span class="sxs-lookup"><span data-stu-id="d71b3-199">**TSPI\_lineSetAppSpecific**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetappspecific) | <span data-ttu-id="d71b3-200">設定呼叫資訊結構的應用程式特定欄位。</span><span class="sxs-lookup"><span data-stu-id="d71b3-200">Sets the application-specific field of a call's information structure.</span></span> <span data-ttu-id="d71b3-201">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="d71b3-201">Synchronous.</span></span> |



 

## <a name="making-calls"></a><span data-ttu-id="d71b3-202">進行呼叫</span><span class="sxs-lookup"><span data-stu-id="d71b3-202">Making Calls</span></span>



|                                                 |                                                                        |
|-------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="d71b3-203">**TSPI \_ lineMakeCall**</span><span class="sxs-lookup"><span data-stu-id="d71b3-203">**TSPI\_lineMakeCall**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall) | <span data-ttu-id="d71b3-204">進行輸出呼叫，並傳回它的呼叫控制碼。</span><span class="sxs-lookup"><span data-stu-id="d71b3-204">Makes an outbound call and returns a call handle for it.</span></span> <span data-ttu-id="d71b3-205">非同步：</span><span class="sxs-lookup"><span data-stu-id="d71b3-205">Asynchronous.</span></span> |
| [<span data-ttu-id="d71b3-206">**TSPI \_ lineDial**</span><span class="sxs-lookup"><span data-stu-id="d71b3-206">**TSPI\_lineDial**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linedial)         | <span data-ttu-id="d71b3-207">撥打一或多個) 的位址 (部分。</span><span class="sxs-lookup"><span data-stu-id="d71b3-207">Dials (parts of one or more) dialable addresses.</span></span> <span data-ttu-id="d71b3-208">非同步：</span><span class="sxs-lookup"><span data-stu-id="d71b3-208">Asynchronous.</span></span>         |



 

## <a name="answering-incoming-calls"></a><span data-ttu-id="d71b3-209">接聽撥入電話</span><span class="sxs-lookup"><span data-stu-id="d71b3-209">Answering Incoming Calls</span></span>



|                                             |                                         |
|---------------------------------------------|-----------------------------------------|
| [<span data-ttu-id="d71b3-210">**TSPI \_ lineAnswer**</span><span class="sxs-lookup"><span data-stu-id="d71b3-210">**TSPI\_lineAnswer**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineanswer) | <span data-ttu-id="d71b3-211">回答來電。</span><span class="sxs-lookup"><span data-stu-id="d71b3-211">Answers an incoming call.</span></span> <span data-ttu-id="d71b3-212">非同步：</span><span class="sxs-lookup"><span data-stu-id="d71b3-212">Asynchronous.</span></span> |



 

## <a name="call-drop-functions"></a><span data-ttu-id="d71b3-213">呼叫 Drop 函數</span><span class="sxs-lookup"><span data-stu-id="d71b3-213">Call Drop Functions</span></span>



|                                         |                                                                           |
|-----------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="d71b3-214">**TSPI \_ lineDrop**</span><span class="sxs-lookup"><span data-stu-id="d71b3-214">**TSPI\_lineDrop**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linedrop) | <span data-ttu-id="d71b3-215">中斷通話的連線，或放棄進行中的呼叫嘗試。</span><span class="sxs-lookup"><span data-stu-id="d71b3-215">Disconnects a call, or abandons a call attempt in progress.</span></span> <span data-ttu-id="d71b3-216">非同步：</span><span class="sxs-lookup"><span data-stu-id="d71b3-216">Asynchronous.</span></span> |



 

 

 

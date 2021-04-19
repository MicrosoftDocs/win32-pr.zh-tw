---
description: 在下表中，基本的電話語音功能是依類別列出。
ms.assetid: 09d10789-bc36-47c7-b77d-8698ae75541a
title: 基本電話語音服務參考
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abe1282a406ea6746f1bb3af11d65164d8af0ce0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974196"
---
# <a name="basic-telephony-services-reference"></a><span data-ttu-id="cbdad-103">基本電話語音服務參考</span><span class="sxs-lookup"><span data-stu-id="cbdad-103">Basic Telephony Services Reference</span></span>

<span data-ttu-id="cbdad-104">在下表中，基本的電話語音功能是依類別列出。</span><span class="sxs-lookup"><span data-stu-id="cbdad-104">The Basic Telephony functions are listed by category in the following tables.</span></span> <span data-ttu-id="cbdad-105">如果函式指出已在應用程式的回復訊息中完成，則會將函數識別為 [*非同步*](a-tapgloss.md) 。</span><span class="sxs-lookup"><span data-stu-id="cbdad-105">A function is identified as [*asynchronous*](a-tapgloss.md) if it indicates completion in a REPLY message to the application.</span></span> <span data-ttu-id="cbdad-106">如果函式一律會立即將其結果傳回給應用程式，則會將函數視為 [*同步*](s-tapgloss.md)。</span><span class="sxs-lookup"><span data-stu-id="cbdad-106">If the function always returns its result to the application immediately, the function is considered [*synchronous*](s-tapgloss.md).</span></span>

<span data-ttu-id="cbdad-107">以下是基本電話語音服務功能的功能群組：</span><span class="sxs-lookup"><span data-stu-id="cbdad-107">Following is a functional grouping of the basic telephony service functions:</span></span>

-   [<span data-ttu-id="cbdad-108">位址格式</span><span class="sxs-lookup"><span data-stu-id="cbdad-108">Address Formats</span></span>](#address-formats)
-   [<span data-ttu-id="cbdad-109">位址</span><span class="sxs-lookup"><span data-stu-id="cbdad-109">Addresses</span></span>](#addresses)
-   [<span data-ttu-id="cbdad-110">接聽撥入電話</span><span class="sxs-lookup"><span data-stu-id="cbdad-110">Answering Incoming Calls</span></span>](#answering-incoming-calls)
-   [<span data-ttu-id="cbdad-111">呼叫 Drop 函數</span><span class="sxs-lookup"><span data-stu-id="cbdad-111">Call Drop Functions</span></span>](#call-drop-functions)
-   [<span data-ttu-id="cbdad-112">呼叫控制碼操作</span><span class="sxs-lookup"><span data-stu-id="cbdad-112">Call Handle Manipulation</span></span>](#call-handle-manipulation)
-   [<span data-ttu-id="cbdad-113">呼叫許可權控制</span><span class="sxs-lookup"><span data-stu-id="cbdad-113">Call Privilege Control</span></span>](#call-privilege-control)
-   [<span data-ttu-id="cbdad-114">撥號狀態和事件</span><span class="sxs-lookup"><span data-stu-id="cbdad-114">Call States and Events</span></span>](#call-states-and-events)
-   [<span data-ttu-id="cbdad-115">線路狀態和功能</span><span class="sxs-lookup"><span data-stu-id="cbdad-115">Line Status and Capabilities</span></span>](#line-status-and-capabilities)
-   [<span data-ttu-id="cbdad-116">行版本協商</span><span class="sxs-lookup"><span data-stu-id="cbdad-116">Line Version Negotiation</span></span>](#line-version-negotiation)
-   [<span data-ttu-id="cbdad-117">位置和國家/地區資訊</span><span class="sxs-lookup"><span data-stu-id="cbdad-117">Location and Country/Region Information</span></span>](#location-and-countryregion-information)
-   [<span data-ttu-id="cbdad-118">進行呼叫</span><span class="sxs-lookup"><span data-stu-id="cbdad-118">Making Calls</span></span>](#making-calls)
-   [<span data-ttu-id="cbdad-119">開啟和關閉行裝置</span><span class="sxs-lookup"><span data-stu-id="cbdad-119">Opening and Closing Line Devices</span></span>](#opening-and-closing-line-devices)
-   [<span data-ttu-id="cbdad-120">要求收件者服務</span><span class="sxs-lookup"><span data-stu-id="cbdad-120">Request Recipient Services</span></span>](#request-recipient-services)
-   [<span data-ttu-id="cbdad-121">TAPI 初始化和關機</span><span class="sxs-lookup"><span data-stu-id="cbdad-121">TAPI Initialization and Shutdown</span></span>](#tapi-initialization-and-shutdown)
-   [<span data-ttu-id="cbdad-122">免付費保護支援</span><span class="sxs-lookup"><span data-stu-id="cbdad-122">Toll Saver Support</span></span>](#toll-saver-support)

## <a name="tapi-initialization-and-shutdown"></a><span data-ttu-id="cbdad-123">TAPI 初始化和關機</span><span class="sxs-lookup"><span data-stu-id="cbdad-123">TAPI Initialization and Shutdown</span></span>



| <span data-ttu-id="cbdad-124">函式</span><span class="sxs-lookup"><span data-stu-id="cbdad-124">Function</span></span>                                     | <span data-ttu-id="cbdad-125">描述</span><span class="sxs-lookup"><span data-stu-id="cbdad-125">Description</span></span>                                                                             |
|----------------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="cbdad-126">**lineInitializeEx**</span><span class="sxs-lookup"><span data-stu-id="cbdad-126">**lineInitializeEx**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa) | <span data-ttu-id="cbdad-127">初始化 TAPI 行抽象概念，以供叫用應用程式使用。</span><span class="sxs-lookup"><span data-stu-id="cbdad-127">Initializes the TAPI line abstraction for use by the invoking application.</span></span> <span data-ttu-id="cbdad-128">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="cbdad-128">Synchronous.</span></span> |
| [<span data-ttu-id="cbdad-129">**lineShutdown**</span><span class="sxs-lookup"><span data-stu-id="cbdad-129">**lineShutdown**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)         | <span data-ttu-id="cbdad-130">關閉應用程式使用 TAPI 的線條抽象化。</span><span class="sxs-lookup"><span data-stu-id="cbdad-130">Shuts down the application's use of TAPI's line abstraction.</span></span> <span data-ttu-id="cbdad-131">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="cbdad-131">Synchronous.</span></span>               |



 

## <a name="line-version-negotiation"></a><span data-ttu-id="cbdad-132">行版本協商</span><span class="sxs-lookup"><span data-stu-id="cbdad-132">Line Version Negotiation</span></span>



| <span data-ttu-id="cbdad-133">函式</span><span class="sxs-lookup"><span data-stu-id="cbdad-133">Function</span></span>                                                   | <span data-ttu-id="cbdad-134">描述</span><span class="sxs-lookup"><span data-stu-id="cbdad-134">Description</span></span>                                                            |
|------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="cbdad-135">**lineNegotiateAPIVersion**</span><span class="sxs-lookup"><span data-stu-id="cbdad-135">**lineNegotiateAPIVersion**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion) | <span data-ttu-id="cbdad-136">允許應用程式協調 TAPI 版本以供使用。</span><span class="sxs-lookup"><span data-stu-id="cbdad-136">Allows an application to negotiate a TAPI version to use.</span></span> <span data-ttu-id="cbdad-137">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="cbdad-137">Synchronous.</span></span> |



 

## <a name="line-status-and-capabilities"></a><span data-ttu-id="cbdad-138">線路狀態和功能</span><span class="sxs-lookup"><span data-stu-id="cbdad-138">Line Status and Capabilities</span></span>



| <span data-ttu-id="cbdad-139">函式</span><span class="sxs-lookup"><span data-stu-id="cbdad-139">Function</span></span>                                               | <span data-ttu-id="cbdad-140">描述</span><span class="sxs-lookup"><span data-stu-id="cbdad-140">Description</span></span>                                                                                                                                                    |
|--------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cbdad-141">**lineGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="cbdad-141">**lineGetDevCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps)               | <span data-ttu-id="cbdad-142">傳回指定線路裝置的功能。</span><span class="sxs-lookup"><span data-stu-id="cbdad-142">Returns the capabilities of a given line device.</span></span> <span data-ttu-id="cbdad-143">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="cbdad-143">Synchronous.</span></span>                                                                                                  |
| [<span data-ttu-id="cbdad-144">**lineGetDevConfig**</span><span class="sxs-lookup"><span data-stu-id="cbdad-144">**lineGetDevConfig**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig)           | <span data-ttu-id="cbdad-145">傳回媒體資料流程裝置的設定。</span><span class="sxs-lookup"><span data-stu-id="cbdad-145">Returns configuration of a media stream device.</span></span> <span data-ttu-id="cbdad-146">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="cbdad-146">Synchronous.</span></span>                                                                                                   |
| [<span data-ttu-id="cbdad-147">**lineGetLineDevStatus**</span><span class="sxs-lookup"><span data-stu-id="cbdad-147">**lineGetLineDevStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus)   | <span data-ttu-id="cbdad-148">傳回指定之開啟行裝置的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="cbdad-148">Returns current status of the specified open line device.</span></span> <span data-ttu-id="cbdad-149">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="cbdad-149">Synchronous.</span></span>                                                                                         |
| [<span data-ttu-id="cbdad-150">**lineSetDevConfig**</span><span class="sxs-lookup"><span data-stu-id="cbdad-150">**lineSetDevConfig**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig)           | <span data-ttu-id="cbdad-151">設定指定媒體串流裝置的設定。</span><span class="sxs-lookup"><span data-stu-id="cbdad-151">Sets the configuration of the specified media stream device.</span></span> <span data-ttu-id="cbdad-152">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="cbdad-152">Synchronous.</span></span>                                                                                      |
| [<span data-ttu-id="cbdad-153">**lineSetStatusMessages**</span><span class="sxs-lookup"><span data-stu-id="cbdad-153">**lineSetStatusMessages**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages) | <span data-ttu-id="cbdad-154">指定應用程式需要通知的狀態變更。</span><span class="sxs-lookup"><span data-stu-id="cbdad-154">Specifies the status changes for which the application needs to be notified.</span></span> <span data-ttu-id="cbdad-155">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="cbdad-155">Synchronous.</span></span>                                                                      |
| [<span data-ttu-id="cbdad-156">**lineGetStatusMessages**</span><span class="sxs-lookup"><span data-stu-id="cbdad-156">**lineGetStatusMessages**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetstatusmessages) | <span data-ttu-id="cbdad-157">傳回應用程式目前的行和位址狀態訊息設定。</span><span class="sxs-lookup"><span data-stu-id="cbdad-157">Returns the application's current line and address status message settings.</span></span> <span data-ttu-id="cbdad-158">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="cbdad-158">Synchronous.</span></span>                                                                       |
| [<span data-ttu-id="cbdad-159">**lineGetID**</span><span class="sxs-lookup"><span data-stu-id="cbdad-159">**lineGetID**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetid)                         | <span data-ttu-id="cbdad-160">抓取與指定的開啟行、位址或呼叫相關聯的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="cbdad-160">Retrieves a device ID associated with the specified open line, address, or call.</span></span> <span data-ttu-id="cbdad-161">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="cbdad-161">Synchronous.</span></span>                                                                  |
| [<span data-ttu-id="cbdad-162">**lineGetIcon**</span><span class="sxs-lookup"><span data-stu-id="cbdad-162">**lineGetIcon**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegeticon)                     | <span data-ttu-id="cbdad-163">允許應用程式抓取顯示給使用者的圖示。</span><span class="sxs-lookup"><span data-stu-id="cbdad-163">Allows an application to retrieve an icon for display to the user.</span></span> <span data-ttu-id="cbdad-164">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="cbdad-164">Synchronous.</span></span>                                                                                |
| [<span data-ttu-id="cbdad-165">**lineConfigDialog**</span><span class="sxs-lookup"><span data-stu-id="cbdad-165">**lineConfigDialog**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog)           | <span data-ttu-id="cbdad-166">使指定行裝置的提供者顯示對話方塊，讓使用者能夠設定與線路裝置相關的參數。</span><span class="sxs-lookup"><span data-stu-id="cbdad-166">Causes the provider of the specified line device to display a dialog box that allows the user to configure parameters related to the line device.</span></span> <span data-ttu-id="cbdad-167">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="cbdad-167">Synchronous.</span></span> |
| [<span data-ttu-id="cbdad-168">**lineConfigDialogEdit**</span><span class="sxs-lookup"><span data-stu-id="cbdad-168">**lineConfigDialogEdit**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialogedit)   | <span data-ttu-id="cbdad-169">顯示對話方塊，讓使用者變更線路裝置的設定資訊。</span><span class="sxs-lookup"><span data-stu-id="cbdad-169">Displays a dialog box allowing the user to change configuration information for a line device.</span></span> <span data-ttu-id="cbdad-170">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="cbdad-170">Synchronous.</span></span>                                                    |



 

## <a name="addresses"></a><span data-ttu-id="cbdad-171">位址</span><span class="sxs-lookup"><span data-stu-id="cbdad-171">Addresses</span></span>



| <span data-ttu-id="cbdad-172">函式</span><span class="sxs-lookup"><span data-stu-id="cbdad-172">Function</span></span>                                             | <span data-ttu-id="cbdad-173">描述</span><span class="sxs-lookup"><span data-stu-id="cbdad-173">Description</span></span>                                                                              |
|------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cbdad-174">**lineGetAddressCaps**</span><span class="sxs-lookup"><span data-stu-id="cbdad-174">**lineGetAddressCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)     | <span data-ttu-id="cbdad-175">傳回位址的電話語音功能。</span><span class="sxs-lookup"><span data-stu-id="cbdad-175">Returns the telephony capabilities of an address.</span></span> <span data-ttu-id="cbdad-176">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="cbdad-176">Synchronous.</span></span>                           |
| [<span data-ttu-id="cbdad-177">**lineGetAddressStatus**</span><span class="sxs-lookup"><span data-stu-id="cbdad-177">**lineGetAddressStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus) | <span data-ttu-id="cbdad-178">傳回指定之位址的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="cbdad-178">Returns current status of a specified address.</span></span> <span data-ttu-id="cbdad-179">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="cbdad-179">Synchronous.</span></span>                              |
| [<span data-ttu-id="cbdad-180">**lineGetAddressID**</span><span class="sxs-lookup"><span data-stu-id="cbdad-180">**lineGetAddressID**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetaddressid)         | <span data-ttu-id="cbdad-181">使用替代格式抓取指定位址的位址識別碼。</span><span class="sxs-lookup"><span data-stu-id="cbdad-181">Retrieves the address ID of an address specified using an alternate format.</span></span> <span data-ttu-id="cbdad-182">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="cbdad-182">Synchronous.</span></span> |



 

## <a name="opening-and-closing-line-devices"></a><span data-ttu-id="cbdad-183">開啟和關閉行裝置</span><span class="sxs-lookup"><span data-stu-id="cbdad-183">Opening and Closing Line Devices</span></span>



| <span data-ttu-id="cbdad-184">函式</span><span class="sxs-lookup"><span data-stu-id="cbdad-184">Function</span></span>                       | <span data-ttu-id="cbdad-185">描述</span><span class="sxs-lookup"><span data-stu-id="cbdad-185">Description</span></span>                                                                                                |
|--------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cbdad-186">**lineOpen**</span><span class="sxs-lookup"><span data-stu-id="cbdad-186">**lineOpen**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineopen)   | <span data-ttu-id="cbdad-187">開啟指定的線路裝置，以提供後續的監視及/或控制行。</span><span class="sxs-lookup"><span data-stu-id="cbdad-187">Opens a specified line device for providing subsequent monitoring and/or control of the line.</span></span> <span data-ttu-id="cbdad-188">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="cbdad-188">Synchronous.</span></span> |
| [<span data-ttu-id="cbdad-189">**lineClose**</span><span class="sxs-lookup"><span data-stu-id="cbdad-189">**lineClose**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineclose) | <span data-ttu-id="cbdad-190">關閉指定的已開啟行裝置。</span><span class="sxs-lookup"><span data-stu-id="cbdad-190">Closes a specified opened line device.</span></span> <span data-ttu-id="cbdad-191">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="cbdad-191">Synchronous.</span></span>                                                        |



 

## <a name="address-formats"></a><span data-ttu-id="cbdad-192">位址格式</span><span class="sxs-lookup"><span data-stu-id="cbdad-192">Address Formats</span></span>



| <span data-ttu-id="cbdad-193">函式</span><span class="sxs-lookup"><span data-stu-id="cbdad-193">Function</span></span>                                                 | <span data-ttu-id="cbdad-194">描述</span><span class="sxs-lookup"><span data-stu-id="cbdad-194">Description</span></span>                                                                                       |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cbdad-195">**lineTranslateAddress**</span><span class="sxs-lookup"><span data-stu-id="cbdad-195">**lineTranslateAddress**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress)     | <span data-ttu-id="cbdad-196">轉譯標準格式的位址和可撥出格式的位址。</span><span class="sxs-lookup"><span data-stu-id="cbdad-196">Translates between an address in canonical format and an address in dialable format.</span></span> <span data-ttu-id="cbdad-197">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="cbdad-197">Synchronous.</span></span> |
| [<span data-ttu-id="cbdad-198">**lineSetCurrentLocation**</span><span class="sxs-lookup"><span data-stu-id="cbdad-198">**lineSetCurrentLocation**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetcurrentlocation) | <span data-ttu-id="cbdad-199">設定用來做為位址轉譯內容的位置。</span><span class="sxs-lookup"><span data-stu-id="cbdad-199">Sets the location used as the context for address translation.</span></span> <span data-ttu-id="cbdad-200">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="cbdad-200">Synchronous.</span></span>                       |
| [<span data-ttu-id="cbdad-201">**lineSetTollList**</span><span class="sxs-lookup"><span data-stu-id="cbdad-201">**lineSetTollList**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesettolllist)               | <span data-ttu-id="cbdad-202">操縱收費清單。</span><span class="sxs-lookup"><span data-stu-id="cbdad-202">Manipulates the toll list.</span></span> <span data-ttu-id="cbdad-203">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="cbdad-203">Synchronous.</span></span>                                                           |
| [<span data-ttu-id="cbdad-204">**lineGetTranslateCaps**</span><span class="sxs-lookup"><span data-stu-id="cbdad-204">**lineGetTranslateCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps)     | <span data-ttu-id="cbdad-205">傳回位址轉譯功能。</span><span class="sxs-lookup"><span data-stu-id="cbdad-205">Returns address translation capabilities.</span></span> <span data-ttu-id="cbdad-206">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="cbdad-206">Synchronous.</span></span>                                            |



 

## <a name="call-states-and-events"></a><span data-ttu-id="cbdad-207">撥號狀態和事件</span><span class="sxs-lookup"><span data-stu-id="cbdad-207">Call States and Events</span></span>



| <span data-ttu-id="cbdad-208">函式</span><span class="sxs-lookup"><span data-stu-id="cbdad-208">Function</span></span>                                         | <span data-ttu-id="cbdad-209">描述</span><span class="sxs-lookup"><span data-stu-id="cbdad-209">Description</span></span>                                                                         |
|--------------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="cbdad-210">**lineGetCallInfo**</span><span class="sxs-lookup"><span data-stu-id="cbdad-210">**lineGetCallInfo**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo)       | <span data-ttu-id="cbdad-211">傳回有關呼叫的固定資訊。</span><span class="sxs-lookup"><span data-stu-id="cbdad-211">Returns fixed information about a call.</span></span> <span data-ttu-id="cbdad-212">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="cbdad-212">Synchronous.</span></span>                                |
| [<span data-ttu-id="cbdad-213">**lineGetCallStatus**</span><span class="sxs-lookup"><span data-stu-id="cbdad-213">**lineGetCallStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus)   | <span data-ttu-id="cbdad-214">傳回指定之呼叫的完整撥號狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="cbdad-214">Returns complete call status information for the specified call.</span></span> <span data-ttu-id="cbdad-215">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="cbdad-215">Synchronous.</span></span>       |
| [<span data-ttu-id="cbdad-216">**lineSetAppSpecific**</span><span class="sxs-lookup"><span data-stu-id="cbdad-216">**lineSetAppSpecific**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetappspecific) | <span data-ttu-id="cbdad-217">設定呼叫資訊結構的應用程式特定欄位。</span><span class="sxs-lookup"><span data-stu-id="cbdad-217">Sets the application-specific field of a call's information structure.</span></span> <span data-ttu-id="cbdad-218">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="cbdad-218">Synchronous.</span></span> |



 

## <a name="making-calls"></a><span data-ttu-id="cbdad-219">進行呼叫</span><span class="sxs-lookup"><span data-stu-id="cbdad-219">Making Calls</span></span>



| <span data-ttu-id="cbdad-220">函式</span><span class="sxs-lookup"><span data-stu-id="cbdad-220">Function</span></span>                             | <span data-ttu-id="cbdad-221">描述</span><span class="sxs-lookup"><span data-stu-id="cbdad-221">Description</span></span>                                                            |
|--------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="cbdad-222">**lineMakeCall**</span><span class="sxs-lookup"><span data-stu-id="cbdad-222">**lineMakeCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linemakecall) | <span data-ttu-id="cbdad-223">進行輸出呼叫，並傳回它的呼叫控制碼。</span><span class="sxs-lookup"><span data-stu-id="cbdad-223">Makes an outbound call and returns a call handle for it.</span></span> <span data-ttu-id="cbdad-224">非同步：</span><span class="sxs-lookup"><span data-stu-id="cbdad-224">Asynchronous.</span></span> |
| [<span data-ttu-id="cbdad-225">**lineDial**</span><span class="sxs-lookup"><span data-stu-id="cbdad-225">**lineDial**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedial)         | <span data-ttu-id="cbdad-226">撥打一或多個) 的位址 (部分。</span><span class="sxs-lookup"><span data-stu-id="cbdad-226">Dials (parts of one or more) dialable addresses.</span></span> <span data-ttu-id="cbdad-227">非同步：</span><span class="sxs-lookup"><span data-stu-id="cbdad-227">Asynchronous.</span></span>         |



 

## <a name="answering-incoming-calls"></a><span data-ttu-id="cbdad-228">接聽撥入電話</span><span class="sxs-lookup"><span data-stu-id="cbdad-228">Answering Incoming Calls</span></span>



| <span data-ttu-id="cbdad-229">函式</span><span class="sxs-lookup"><span data-stu-id="cbdad-229">Function</span></span>                         | <span data-ttu-id="cbdad-230">描述</span><span class="sxs-lookup"><span data-stu-id="cbdad-230">Description</span></span>                             |
|----------------------------------|-----------------------------------------|
| [<span data-ttu-id="cbdad-231">**lineAnswer**</span><span class="sxs-lookup"><span data-stu-id="cbdad-231">**lineAnswer**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineanswer) | <span data-ttu-id="cbdad-232">回答來電。</span><span class="sxs-lookup"><span data-stu-id="cbdad-232">Answers an incoming call.</span></span> <span data-ttu-id="cbdad-233">非同步：</span><span class="sxs-lookup"><span data-stu-id="cbdad-233">Asynchronous.</span></span> |



 

## <a name="toll-saver-support"></a><span data-ttu-id="cbdad-234">免付費保護支援</span><span class="sxs-lookup"><span data-stu-id="cbdad-234">Toll Saver Support</span></span>



| <span data-ttu-id="cbdad-235">函式</span><span class="sxs-lookup"><span data-stu-id="cbdad-235">Function</span></span>                                   | <span data-ttu-id="cbdad-236">描述</span><span class="sxs-lookup"><span data-stu-id="cbdad-236">Description</span></span>                                                                                                 |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cbdad-237">**lineSetNumRings**</span><span class="sxs-lookup"><span data-stu-id="cbdad-237">**lineSetNumRings**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetnumrings) | <span data-ttu-id="cbdad-238">指出來電之前要接聽的環形數。</span><span class="sxs-lookup"><span data-stu-id="cbdad-238">Indicates the number of rings after which incoming calls are to be answered.</span></span> <span data-ttu-id="cbdad-239">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="cbdad-239">Synchronous.</span></span>                   |
| [<span data-ttu-id="cbdad-240">**lineGetNumRings**</span><span class="sxs-lookup"><span data-stu-id="cbdad-240">**lineGetNumRings**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetnumrings) | <span data-ttu-id="cbdad-241">傳回 [**lineSetNumRings**](/windows/desktop/api/Tapi/nf-tapi-linesetnumrings)要求的最小環形數。</span><span class="sxs-lookup"><span data-stu-id="cbdad-241">Returns the minimum number of rings requested with [**lineSetNumRings**](/windows/desktop/api/Tapi/nf-tapi-linesetnumrings).</span></span> <span data-ttu-id="cbdad-242">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="cbdad-242">Synchronous.</span></span> |



 

## <a name="call-privilege-control"></a><span data-ttu-id="cbdad-243">呼叫許可權控制</span><span class="sxs-lookup"><span data-stu-id="cbdad-243">Call Privilege Control</span></span>



| <span data-ttu-id="cbdad-244">函式</span><span class="sxs-lookup"><span data-stu-id="cbdad-244">Function</span></span>                                             | <span data-ttu-id="cbdad-245">描述</span><span class="sxs-lookup"><span data-stu-id="cbdad-245">Description</span></span>                                                               |
|------------------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="cbdad-246">**lineSetCallPrivilege**</span><span class="sxs-lookup"><span data-stu-id="cbdad-246">**lineSetCallPrivilege**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetcallprivilege) | <span data-ttu-id="cbdad-247">將應用程式的許可權設定為指定的許可權。</span><span class="sxs-lookup"><span data-stu-id="cbdad-247">Sets the application's privilege to the privilege specified.</span></span> <span data-ttu-id="cbdad-248">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="cbdad-248">Synchronous.</span></span> |



 

## <a name="call-drop-functions"></a><span data-ttu-id="cbdad-249">呼叫 Drop 函數</span><span class="sxs-lookup"><span data-stu-id="cbdad-249">Call Drop Functions</span></span>



| <span data-ttu-id="cbdad-250">函式</span><span class="sxs-lookup"><span data-stu-id="cbdad-250">Function</span></span>                                         | <span data-ttu-id="cbdad-251">描述</span><span class="sxs-lookup"><span data-stu-id="cbdad-251">Description</span></span>                                                               |
|--------------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="cbdad-252">**lineDrop**</span><span class="sxs-lookup"><span data-stu-id="cbdad-252">**lineDrop**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedrop)                     | <span data-ttu-id="cbdad-253">中斷通話的連線，或放棄進行中的呼叫嘗試。</span><span class="sxs-lookup"><span data-stu-id="cbdad-253">Disconnects a call, or abandons a call attempt in progress.</span></span> <span data-ttu-id="cbdad-254">非同步：</span><span class="sxs-lookup"><span data-stu-id="cbdad-254">Asynchronous.</span></span> |
| [<span data-ttu-id="cbdad-255">**lineDeallocateCall**</span><span class="sxs-lookup"><span data-stu-id="cbdad-255">**lineDeallocateCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) | <span data-ttu-id="cbdad-256">解除配置指定的呼叫控制碼。</span><span class="sxs-lookup"><span data-stu-id="cbdad-256">Deallocates the specified call handle.</span></span> <span data-ttu-id="cbdad-257">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="cbdad-257">Synchronous.</span></span>                       |



 

## <a name="call-handle-manipulation"></a><span data-ttu-id="cbdad-258">呼叫控制碼操作</span><span class="sxs-lookup"><span data-stu-id="cbdad-258">Call Handle Manipulation</span></span>



| <span data-ttu-id="cbdad-259">函式</span><span class="sxs-lookup"><span data-stu-id="cbdad-259">Function</span></span>                                                   | <span data-ttu-id="cbdad-260">描述</span><span class="sxs-lookup"><span data-stu-id="cbdad-260">Description</span></span>                                                                                                                    |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cbdad-261">**lineHandoff**</span><span class="sxs-lookup"><span data-stu-id="cbdad-261">**lineHandoff**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linehandoff)                         | <span data-ttu-id="cbdad-262">交給來電擁有權及/或將應用程式的許可權變更為呼叫。</span><span class="sxs-lookup"><span data-stu-id="cbdad-262">Hands off call ownership and/or changes an application's privileges to a call.</span></span> <span data-ttu-id="cbdad-263">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="cbdad-263">Synchronous.</span></span>                                    |
| [<span data-ttu-id="cbdad-264">**lineGetNewCalls**</span><span class="sxs-lookup"><span data-stu-id="cbdad-264">**lineGetNewCalls**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetnewcalls)                 | <span data-ttu-id="cbdad-265">將呼叫控制碼傳回給應用程式還沒有控制碼的指定行或位址上的呼叫。</span><span class="sxs-lookup"><span data-stu-id="cbdad-265">Returns call handles to calls on a specified line or address for which the application does not yet have handles.</span></span> <span data-ttu-id="cbdad-266">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="cbdad-266">Synchronous.</span></span> |
| [<span data-ttu-id="cbdad-267">**lineGetConfRelatedCalls**</span><span class="sxs-lookup"><span data-stu-id="cbdad-267">**lineGetConfRelatedCalls**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls) | <span data-ttu-id="cbdad-268">傳回呼叫控制碼的清單，這些呼叫控制碼屬於與指定為參數的呼叫相同的會議呼叫。</span><span class="sxs-lookup"><span data-stu-id="cbdad-268">Returns a list of call handles that are part of the same conference call as the call specified as a parameter.</span></span> <span data-ttu-id="cbdad-269">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="cbdad-269">Synchronous.</span></span>    |



 

## <a name="location-and-countryregion-information"></a><span data-ttu-id="cbdad-270">位置和國家/地區資訊</span><span class="sxs-lookup"><span data-stu-id="cbdad-270">Location and Country/Region Information</span></span>



| <span data-ttu-id="cbdad-271">函式</span><span class="sxs-lookup"><span data-stu-id="cbdad-271">Function</span></span>                                           | <span data-ttu-id="cbdad-272">描述</span><span class="sxs-lookup"><span data-stu-id="cbdad-272">Description</span></span>                                                                                           |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cbdad-273">**lineTranslateDialog**</span><span class="sxs-lookup"><span data-stu-id="cbdad-273">**lineTranslateDialog**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linetranslatedialog) | <span data-ttu-id="cbdad-274">顯示對話方塊，讓使用者變更位置和電話卡資訊。</span><span class="sxs-lookup"><span data-stu-id="cbdad-274">Displays a dialog box allowing the user to change location and calling card information.</span></span> <span data-ttu-id="cbdad-275">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="cbdad-275">Synchronous.</span></span> |
| [<span data-ttu-id="cbdad-276">**lineGetCountry**</span><span class="sxs-lookup"><span data-stu-id="cbdad-276">**lineGetCountry**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetcountry)           | <span data-ttu-id="cbdad-277">抓取撥號規則，以及特定國家/地區的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="cbdad-277">Retrieves dialing rules and other information about a given country/region.</span></span> <span data-ttu-id="cbdad-278">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="cbdad-278">Synchronous.</span></span>              |



 

## <a name="request-recipient-services"></a><span data-ttu-id="cbdad-279">要求收件者服務</span><span class="sxs-lookup"><span data-stu-id="cbdad-279">Request Recipient Services</span></span>

<span data-ttu-id="cbdad-280">下列兩個函式僅用來支援輔助電話語音。</span><span class="sxs-lookup"><span data-stu-id="cbdad-280">The following two functions are used only in support of Assisted Telephony.</span></span>



| <span data-ttu-id="cbdad-281">函式</span><span class="sxs-lookup"><span data-stu-id="cbdad-281">Function</span></span>                                                             | <span data-ttu-id="cbdad-282">描述</span><span class="sxs-lookup"><span data-stu-id="cbdad-282">Description</span></span>                                                                                                  |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cbdad-283">**lineRegisterRequestRecipient**</span><span class="sxs-lookup"><span data-stu-id="cbdad-283">**lineRegisterRequestRecipient**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineregisterrequestrecipient) | <span data-ttu-id="cbdad-284">針對指定的要求模式，將應用程式註冊或取消註冊為要求收件者。</span><span class="sxs-lookup"><span data-stu-id="cbdad-284">Registers or deregisters the application as a request recipient for the specified request mode.</span></span> <span data-ttu-id="cbdad-285">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="cbdad-285">Synchronous.</span></span> |
| [<span data-ttu-id="cbdad-286">**lineGetRequest**</span><span class="sxs-lookup"><span data-stu-id="cbdad-286">**lineGetRequest**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetrequest)                             | <span data-ttu-id="cbdad-287">從電話語音動態連結程式庫取得下一個要求。</span><span class="sxs-lookup"><span data-stu-id="cbdad-287">Gets the next request from the Telephony dynamic link library.</span></span> <span data-ttu-id="cbdad-288">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="cbdad-288">Synchronous.</span></span>                                  |



 

 

 




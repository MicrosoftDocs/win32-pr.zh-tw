---
description: 下列主題依類別列出補充電話語音功能。
ms.assetid: 0d1a81d2-aa9e-4a85-85d3-aa4eabb26eb5
title: 補充電話語音功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 527c39441a924a4f9787d22bf8db596882e7f257
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981568"
---
# <a name="supplementary-phone-service-functions"></a><span data-ttu-id="46650-103">補充電話語音功能</span><span class="sxs-lookup"><span data-stu-id="46650-103">Supplementary Phone Service Functions</span></span>

<span data-ttu-id="46650-104">下列主題依類別列出補充電話語音功能。</span><span class="sxs-lookup"><span data-stu-id="46650-104">The supplementary phone service functions are listed by category in the following topics.</span></span> <span data-ttu-id="46650-105">如果函式會將回復訊息中的完成指出至應用程式，則會將函式識別為 [*非同步*](a-tapgloss.md) 。</span><span class="sxs-lookup"><span data-stu-id="46650-105">A function is identified as [*asynchronous*](a-tapgloss.md) if it will indicate completion in a REPLY message to the application.</span></span> <span data-ttu-id="46650-106">如果函式一律會立即將其結果傳回給應用程式，則會將函數視為 [*同步*](s-tapgloss.md)。</span><span class="sxs-lookup"><span data-stu-id="46650-106">If the function always returns its result to the application immediately, the function is considered [*synchronous*](s-tapgloss.md).</span></span>

<span data-ttu-id="46650-107">以下是補充電話語音功能的功能群組：</span><span class="sxs-lookup"><span data-stu-id="46650-107">Following is a functional grouping of the supplementary phone service functions:</span></span>

-   [<span data-ttu-id="46650-108">按鈕</span><span class="sxs-lookup"><span data-stu-id="46650-108">Buttons</span></span>](#buttons)
-   [<span data-ttu-id="46650-109">資料區域</span><span class="sxs-lookup"><span data-stu-id="46650-109">Data areas</span></span>](#data-areas)
-   [<span data-ttu-id="46650-110">顯示器</span><span class="sxs-lookup"><span data-stu-id="46650-110">Display</span></span>](#display)
-   [<span data-ttu-id="46650-111">Hookswitch 裝置</span><span class="sxs-lookup"><span data-stu-id="46650-111">Hookswitch devices</span></span>](#hookswitch-devices)
-   [<span data-ttu-id="46650-112">燈</span><span class="sxs-lookup"><span data-stu-id="46650-112">Lamps</span></span>](#lamps)
-   [<span data-ttu-id="46650-113">開啟和關閉手機裝置</span><span class="sxs-lookup"><span data-stu-id="46650-113">Opening and closing phone devices</span></span>](#opening-and-closing-phone-devices)
-   [<span data-ttu-id="46650-114">電話初始化和關機</span><span class="sxs-lookup"><span data-stu-id="46650-114">Phone initialization and shutdown</span></span>](#phone-initialization-and-shutdown)
-   [<span data-ttu-id="46650-115">電話狀態和功能</span><span class="sxs-lookup"><span data-stu-id="46650-115">Phone status and capabilities</span></span>](#phone-status-and-capabilities)
-   [<span data-ttu-id="46650-116">電話版本協商</span><span class="sxs-lookup"><span data-stu-id="46650-116">Phone version negotiation</span></span>](#phone-version-negotiation)
-   [<span data-ttu-id="46650-117">環形</span><span class="sxs-lookup"><span data-stu-id="46650-117">Ring</span></span>](#ring)
-   [<span data-ttu-id="46650-118">狀態</span><span class="sxs-lookup"><span data-stu-id="46650-118">Status</span></span>](#status)

## <a name="phone-initialization-and-shutdown"></a><span data-ttu-id="46650-119">電話初始化和關機</span><span class="sxs-lookup"><span data-stu-id="46650-119">Phone Initialization and Shutdown</span></span>



| <span data-ttu-id="46650-120">函式</span><span class="sxs-lookup"><span data-stu-id="46650-120">Function</span></span>                                       | <span data-ttu-id="46650-121">描述</span><span class="sxs-lookup"><span data-stu-id="46650-121">Description</span></span>                                                                          |
|------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="46650-122">**phoneInitializeEx**</span><span class="sxs-lookup"><span data-stu-id="46650-122">**phoneInitializeEx**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) | <span data-ttu-id="46650-123">初始化 TAPI 電話抽象概念，以供叫用應用程式使用。</span><span class="sxs-lookup"><span data-stu-id="46650-123">Initializes TAPI phone abstraction for use by the invoking application.</span></span> <span data-ttu-id="46650-124">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="46650-124">Synchronous.</span></span> |
| [<span data-ttu-id="46650-125">**phoneShutdown**</span><span class="sxs-lookup"><span data-stu-id="46650-125">**phoneShutdown**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown)         | <span data-ttu-id="46650-126">關閉應用程式使用 TAPI 的電話抽象概念。</span><span class="sxs-lookup"><span data-stu-id="46650-126">Shuts down an application's use of TAPI's phone abstraction.</span></span> <span data-ttu-id="46650-127">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="46650-127">Synchronous.</span></span>            |



 

## <a name="phone-version-negotiation"></a><span data-ttu-id="46650-128">電話版本協商</span><span class="sxs-lookup"><span data-stu-id="46650-128">Phone Version Negotiation</span></span>



| <span data-ttu-id="46650-129">函式</span><span class="sxs-lookup"><span data-stu-id="46650-129">Function</span></span>                                                     | <span data-ttu-id="46650-130">描述</span><span class="sxs-lookup"><span data-stu-id="46650-130">Description</span></span>                                                            |
|--------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="46650-131">**phoneNegotiateAPIVersion**</span><span class="sxs-lookup"><span data-stu-id="46650-131">**phoneNegotiateAPIVersion**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateapiversion) | <span data-ttu-id="46650-132">允許應用程式協調 TAPI 版本以供使用。</span><span class="sxs-lookup"><span data-stu-id="46650-132">Allows an application to negotiate a TAPI version to use.</span></span> <span data-ttu-id="46650-133">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="46650-133">Synchronous.</span></span> |



 

## <a name="opening-and-closing-phone-devices"></a><span data-ttu-id="46650-134">開啟和關閉手機裝置</span><span class="sxs-lookup"><span data-stu-id="46650-134">Opening and Closing Phone Devices</span></span>



| <span data-ttu-id="46650-135">函式</span><span class="sxs-lookup"><span data-stu-id="46650-135">Function</span></span>                         | <span data-ttu-id="46650-136">描述</span><span class="sxs-lookup"><span data-stu-id="46650-136">Description</span></span>                                                                                               |
|----------------------------------|-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="46650-137">**phoneOpen**</span><span class="sxs-lookup"><span data-stu-id="46650-137">**phoneOpen**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneopen)   | <span data-ttu-id="46650-138">開啟指定的電話裝置，並為應用程式提供擁有者或監視器許可權。</span><span class="sxs-lookup"><span data-stu-id="46650-138">Opens the specified phone device, giving the application either owner or monitor privileges.</span></span> <span data-ttu-id="46650-139">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="46650-139">Synchronous.</span></span> |
| [<span data-ttu-id="46650-140">**phoneClose**</span><span class="sxs-lookup"><span data-stu-id="46650-140">**phoneClose**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneclose) | <span data-ttu-id="46650-141">關閉指定的 open phone 裝置。</span><span class="sxs-lookup"><span data-stu-id="46650-141">Closes a specified open phone device.</span></span> <span data-ttu-id="46650-142">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="46650-142">Synchronous.</span></span>                                                        |



 

## <a name="phone-status-and-capabilities"></a><span data-ttu-id="46650-143">電話狀態和功能</span><span class="sxs-lookup"><span data-stu-id="46650-143">Phone Status and Capabilities</span></span>



| <span data-ttu-id="46650-144">函式</span><span class="sxs-lookup"><span data-stu-id="46650-144">Function</span></span>                                       | <span data-ttu-id="46650-145">描述</span><span class="sxs-lookup"><span data-stu-id="46650-145">Description</span></span>                                                                                                                                                      |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="46650-146">**phoneGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="46650-146">**phoneGetDevCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps)     | <span data-ttu-id="46650-147">傳回指定電話裝置的功能。</span><span class="sxs-lookup"><span data-stu-id="46650-147">Returns the capabilities of a given phone device.</span></span> <span data-ttu-id="46650-148">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="46650-148">Synchronous.</span></span>                                                                                                   |
| [<span data-ttu-id="46650-149">**phoneGetID**</span><span class="sxs-lookup"><span data-stu-id="46650-149">**phoneGetID**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetid)               | <span data-ttu-id="46650-150">傳回與指定的電話裝置相關聯之指定裝置類別的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="46650-150">Returns a device ID for the given device class associated with the specified phone device.</span></span> <span data-ttu-id="46650-151">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="46650-151">Synchronous.</span></span>                                                          |
| [<span data-ttu-id="46650-152">**phoneGetIcon**</span><span class="sxs-lookup"><span data-stu-id="46650-152">**phoneGetIcon**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegeticon)           | <span data-ttu-id="46650-153">允許應用程式抓取顯示給使用者的圖示。</span><span class="sxs-lookup"><span data-stu-id="46650-153">Allows an application to retrieve an icon for display to the user.</span></span> <span data-ttu-id="46650-154">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="46650-154">Synchronous.</span></span>                                                                                  |
| [<span data-ttu-id="46650-155">**phoneConfigDialog**</span><span class="sxs-lookup"><span data-stu-id="46650-155">**phoneConfigDialog**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneconfigdialog) | <span data-ttu-id="46650-156">讓指定電話裝置的提供者顯示對話方塊，讓使用者能夠設定電話裝置的相關參數。</span><span class="sxs-lookup"><span data-stu-id="46650-156">Causes the provider of the specified phone device to display a dialog box that allows the user to configure parameters related to the phone device.</span></span> <span data-ttu-id="46650-157">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="46650-157">Synchronous.</span></span> |



 

## <a name="hookswitch-devices"></a><span data-ttu-id="46650-158">Hookswitch 裝置</span><span class="sxs-lookup"><span data-stu-id="46650-158">Hookswitch Devices</span></span>



| <span data-ttu-id="46650-159">函式</span><span class="sxs-lookup"><span data-stu-id="46650-159">Function</span></span>                                         | <span data-ttu-id="46650-160">描述</span><span class="sxs-lookup"><span data-stu-id="46650-160">Description</span></span>                                                                                       |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="46650-161">**phoneSetHookSwitch**</span><span class="sxs-lookup"><span data-stu-id="46650-161">**phoneSetHookSwitch**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonesethookswitch) | <span data-ttu-id="46650-162">將開啟的電話 hookswitch 裝置的勾點狀態設定為指定的模式。</span><span class="sxs-lookup"><span data-stu-id="46650-162">Sets the hook state of an open phone's hookswitch devices to a specified mode.</span></span> <span data-ttu-id="46650-163">非同步：</span><span class="sxs-lookup"><span data-stu-id="46650-163">Asynchronous.</span></span>      |
| [<span data-ttu-id="46650-164">**phoneGetHookSwitch**</span><span class="sxs-lookup"><span data-stu-id="46650-164">**phoneGetHookSwitch**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegethookswitch) | <span data-ttu-id="46650-165">查詢 open phone 裝置之 hookswitch 裝置的 hookswitch 模式。</span><span class="sxs-lookup"><span data-stu-id="46650-165">Queries the hookswitch mode of a hookswitch device of an open phone device.</span></span> <span data-ttu-id="46650-166">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="46650-166">Synchronous.</span></span>          |
| [<span data-ttu-id="46650-167">**phoneSetVolume**</span><span class="sxs-lookup"><span data-stu-id="46650-167">**phoneSetVolume**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonesetvolume)         | <span data-ttu-id="46650-168">設定 hookswitch 裝置的說話者在開啟的電話裝置上的音量。</span><span class="sxs-lookup"><span data-stu-id="46650-168">Sets the volume of a hookswitch device's speaker of an open phone device.</span></span> <span data-ttu-id="46650-169">非同步：</span><span class="sxs-lookup"><span data-stu-id="46650-169">Asynchronous.</span></span>           |
| [<span data-ttu-id="46650-170">**phoneGetVolume**</span><span class="sxs-lookup"><span data-stu-id="46650-170">**phoneGetVolume**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetvolume)         | <span data-ttu-id="46650-171">傳回 open phone 裝置之 hookswitch 裝置喇叭的磁片區設定。</span><span class="sxs-lookup"><span data-stu-id="46650-171">Returns the volume setting of a hookswitch device's speaker of an open phone device.</span></span> <span data-ttu-id="46650-172">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="46650-172">Synchronous.</span></span> |
| [<span data-ttu-id="46650-173">**phoneSetGain**</span><span class="sxs-lookup"><span data-stu-id="46650-173">**phoneSetGain**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonesetgain)             | <span data-ttu-id="46650-174">設定 hookswitch 裝置在開啟的電話裝置上的 mic 增益。</span><span class="sxs-lookup"><span data-stu-id="46650-174">Sets the gain of a hookswitch device's mic of an open phone device.</span></span> <span data-ttu-id="46650-175">非同步：</span><span class="sxs-lookup"><span data-stu-id="46650-175">Asynchronous.</span></span>                 |
| [<span data-ttu-id="46650-176">**phoneGetGain**</span><span class="sxs-lookup"><span data-stu-id="46650-176">**phoneGetGain**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetgain)             | <span data-ttu-id="46650-177">傳回 hookswitch 裝置 mic 的 open phone 增益設定。</span><span class="sxs-lookup"><span data-stu-id="46650-177">Returns the gain setting of a hookswitch device's mic of an open phone.</span></span> <span data-ttu-id="46650-178">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="46650-178">Synchronous.</span></span>              |



 

## <a name="display"></a><span data-ttu-id="46650-179">顯示</span><span class="sxs-lookup"><span data-stu-id="46650-179">Display</span></span>



| <span data-ttu-id="46650-180">函式</span><span class="sxs-lookup"><span data-stu-id="46650-180">Function</span></span>                                   | <span data-ttu-id="46650-181">描述</span><span class="sxs-lookup"><span data-stu-id="46650-181">Description</span></span>                                                              |
|--------------------------------------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="46650-182">**phoneSetDisplay**</span><span class="sxs-lookup"><span data-stu-id="46650-182">**phoneSetDisplay**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonesetdisplay) | <span data-ttu-id="46650-183">將資訊寫入至開啟的電話裝置的顯示。</span><span class="sxs-lookup"><span data-stu-id="46650-183">Writes information to the display of an open phone device.</span></span> <span data-ttu-id="46650-184">非同步：</span><span class="sxs-lookup"><span data-stu-id="46650-184">Asynchronous.</span></span> |
| [<span data-ttu-id="46650-185">**phoneGetDisplay**</span><span class="sxs-lookup"><span data-stu-id="46650-185">**phoneGetDisplay**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetdisplay) | <span data-ttu-id="46650-186">傳回手機顯示的目前內容。</span><span class="sxs-lookup"><span data-stu-id="46650-186">Returns the current contents of a phone's display.</span></span> <span data-ttu-id="46650-187">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="46650-187">Synchronous.</span></span>          |



 

## <a name="ring"></a><span data-ttu-id="46650-188">環形</span><span class="sxs-lookup"><span data-stu-id="46650-188">Ring</span></span>



| <span data-ttu-id="46650-189">函式</span><span class="sxs-lookup"><span data-stu-id="46650-189">Function</span></span>                             | <span data-ttu-id="46650-190">描述</span><span class="sxs-lookup"><span data-stu-id="46650-190">Description</span></span>                                                              |
|--------------------------------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="46650-191">**phoneSetRing**</span><span class="sxs-lookup"><span data-stu-id="46650-191">**phoneSetRing**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonesetring) | <span data-ttu-id="46650-192">根據指定的響鈴模式響鈴開啟的電話裝置。</span><span class="sxs-lookup"><span data-stu-id="46650-192">Rings an open phone device according to a given ring mode.</span></span> <span data-ttu-id="46650-193">非同步：</span><span class="sxs-lookup"><span data-stu-id="46650-193">Asynchronous.</span></span> |
| [<span data-ttu-id="46650-194">**phoneGetRing**</span><span class="sxs-lookup"><span data-stu-id="46650-194">**phoneGetRing**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetring) | <span data-ttu-id="46650-195">傳回已開啟之手機裝置的目前響鈴模式。</span><span class="sxs-lookup"><span data-stu-id="46650-195">Returns the current ring mode of an opened phone device.</span></span> <span data-ttu-id="46650-196">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="46650-196">Synchronous.</span></span>    |



 

## <a name="buttons"></a><span data-ttu-id="46650-197">按鈕</span><span class="sxs-lookup"><span data-stu-id="46650-197">Buttons</span></span>



| <span data-ttu-id="46650-198">函式</span><span class="sxs-lookup"><span data-stu-id="46650-198">Function</span></span>                                         | <span data-ttu-id="46650-199">描述</span><span class="sxs-lookup"><span data-stu-id="46650-199">Description</span></span>                                                                    |
|--------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="46650-200">**phoneSetButtonInfo**</span><span class="sxs-lookup"><span data-stu-id="46650-200">**phoneSetButtonInfo**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonesetbuttoninfo) | <span data-ttu-id="46650-201">設定與手機裝置上的按鈕相關聯的資訊。</span><span class="sxs-lookup"><span data-stu-id="46650-201">Sets the information associated with a button on a phone device.</span></span> <span data-ttu-id="46650-202">非同步：</span><span class="sxs-lookup"><span data-stu-id="46650-202">Asynchronous.</span></span> |
| [<span data-ttu-id="46650-203">**phoneGetButtonInfo**</span><span class="sxs-lookup"><span data-stu-id="46650-203">**phoneGetButtonInfo**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo) | <span data-ttu-id="46650-204">傳回與手機裝置上的按鈕相關聯的資訊。</span><span class="sxs-lookup"><span data-stu-id="46650-204">Returns information associated with a button on a phone device.</span></span> <span data-ttu-id="46650-205">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="46650-205">Synchronous.</span></span>   |



 

## <a name="lamps"></a><span data-ttu-id="46650-206">燈</span><span class="sxs-lookup"><span data-stu-id="46650-206">Lamps</span></span>



| <span data-ttu-id="46650-207">函式</span><span class="sxs-lookup"><span data-stu-id="46650-207">Function</span></span>                             | <span data-ttu-id="46650-208">描述</span><span class="sxs-lookup"><span data-stu-id="46650-208">Description</span></span>                                                                                 |
|--------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="46650-209">**phoneSetLamp**</span><span class="sxs-lookup"><span data-stu-id="46650-209">**phoneSetLamp**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonesetlamp) | <span data-ttu-id="46650-210">以指定的燈光源模式燈亮著指定的開啟電話裝置上的燈燈。</span><span class="sxs-lookup"><span data-stu-id="46650-210">Lights a lamp on a specified open phone device in a given lamp lighting mode.</span></span> <span data-ttu-id="46650-211">非同步：</span><span class="sxs-lookup"><span data-stu-id="46650-211">Asynchronous.</span></span> |
| [<span data-ttu-id="46650-212">**phoneGetLamp**</span><span class="sxs-lookup"><span data-stu-id="46650-212">**phoneGetLamp**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetlamp) | <span data-ttu-id="46650-213">傳回指定燈的目前燈泡模式。</span><span class="sxs-lookup"><span data-stu-id="46650-213">Returns the current lamp mode of the specified lamp.</span></span> <span data-ttu-id="46650-214">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="46650-214">Synchronous.</span></span>                           |



 

## <a name="data-areas"></a><span data-ttu-id="46650-215">資料區域</span><span class="sxs-lookup"><span data-stu-id="46650-215">Data Areas</span></span>



| <span data-ttu-id="46650-216">函式</span><span class="sxs-lookup"><span data-stu-id="46650-216">Function</span></span>                             | <span data-ttu-id="46650-217">描述</span><span class="sxs-lookup"><span data-stu-id="46650-217">Description</span></span>                                                                             |
|--------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="46650-218">**phoneSetData**</span><span class="sxs-lookup"><span data-stu-id="46650-218">**phoneSetData**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonesetdata) | <span data-ttu-id="46650-219">將資料緩衝區下載至電話裝置中的指定資料區域。</span><span class="sxs-lookup"><span data-stu-id="46650-219">Downloads a buffer of data to a given data area in the phone device.</span></span> <span data-ttu-id="46650-220">非同步：</span><span class="sxs-lookup"><span data-stu-id="46650-220">Asynchronous.</span></span>      |
| [<span data-ttu-id="46650-221">**phoneGetData**</span><span class="sxs-lookup"><span data-stu-id="46650-221">**phoneGetData**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetdata) | <span data-ttu-id="46650-222">將電話裝置中特定資料區域的內容上傳到緩衝區。</span><span class="sxs-lookup"><span data-stu-id="46650-222">Uploads the contents of a given data area in the phone device to a buffer.</span></span> <span data-ttu-id="46650-223">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="46650-223">Synchronous.</span></span> |



 

## <a name="status"></a><span data-ttu-id="46650-224">狀態</span><span class="sxs-lookup"><span data-stu-id="46650-224">Status</span></span>



| <span data-ttu-id="46650-225">函式</span><span class="sxs-lookup"><span data-stu-id="46650-225">Function</span></span>                                                 | <span data-ttu-id="46650-226">描述</span><span class="sxs-lookup"><span data-stu-id="46650-226">Description</span></span>                                                                               |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="46650-227">**phoneSetStatusMessages**</span><span class="sxs-lookup"><span data-stu-id="46650-227">**phoneSetStatusMessages**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages) | <span data-ttu-id="46650-228">指定應用程式想要收到通知的狀態變更。</span><span class="sxs-lookup"><span data-stu-id="46650-228">Specifies the status changes for which the application wants to be notified.</span></span> <span data-ttu-id="46650-229">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="46650-229">Synchronous.</span></span> |
| [<span data-ttu-id="46650-230">**phoneGetStatusMessages**</span><span class="sxs-lookup"><span data-stu-id="46650-230">**phoneGetStatusMessages**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages) | <span data-ttu-id="46650-231">傳回應用程式想要收到通知的狀態變更。</span><span class="sxs-lookup"><span data-stu-id="46650-231">Returns the status changes for which the application wants to be notified.</span></span> <span data-ttu-id="46650-232">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="46650-232">Synchronous.</span></span>   |
| [<span data-ttu-id="46650-233">**phoneGetStatus**</span><span class="sxs-lookup"><span data-stu-id="46650-233">**phoneGetStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetstatus)                 | <span data-ttu-id="46650-234">傳回開啟的電話裝置的完整狀態。</span><span class="sxs-lookup"><span data-stu-id="46650-234">Returns the complete status of an open phone device.</span></span> <span data-ttu-id="46650-235">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="46650-235">Synchronous.</span></span>                         |



 

 

 




---
title: 使用 Windows 標頭
description: 使用 Windows 標頭檔來建立使用 Windows API 的應用程式。
ms.assetid: a4def563-8ddc-4630-ae8a-86c07cf98374
keywords:
- Windows API，標頭檔
- C2065
- WINVER
- _WIN32_WINDOWS
- _WIN32_WINNT
- _WIN32_IE
- WIN32_LEAN_AND_MEAN
ms.topic: article
ms.date: 01/22/2020
ms.openlocfilehash: 4d27b14a6e545db9a9a38c205012b149942adf7f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382466"
---
# <a name="using-the-windows-headers"></a><span data-ttu-id="ceef9-110">使用 Windows 標頭</span><span class="sxs-lookup"><span data-stu-id="ceef9-110">Using the Windows Headers</span></span>

<span data-ttu-id="ceef9-111">Windows API 的標頭檔可讓您建立32和64位應用程式。</span><span class="sxs-lookup"><span data-stu-id="ceef9-111">The header files for the Windows API enable you to create 32- and 64-bit applications.</span></span> <span data-ttu-id="ceef9-112">它們包含 Unicode 和 ANSI API 版本的宣告。</span><span class="sxs-lookup"><span data-stu-id="ceef9-112">They include declarations for both Unicode and ANSI versions of the API.</span></span> <span data-ttu-id="ceef9-113">如需詳細資訊，請參閱 [WINDOWS API 中的 Unicode](/windows/desktop/Intl/unicode-in-the-windows-api)。</span><span class="sxs-lookup"><span data-stu-id="ceef9-113">For more information, see [Unicode in the Windows API](/windows/desktop/Intl/unicode-in-the-windows-api).</span></span> <span data-ttu-id="ceef9-114">它們使用的 [資料類型](windows-data-types.md) 可讓您從單一原始程式碼基底建立32和64位版本的應用程式。</span><span class="sxs-lookup"><span data-stu-id="ceef9-114">They use [data types](windows-data-types.md) that enable you to build both 32- and 64-bit versions of your application from a single source code base.</span></span> <span data-ttu-id="ceef9-115">如需詳細資訊，請參閱 [準備開始64位 Windows](/windows/desktop/WinProg64/getting-ready-for-64-bit-windows)。</span><span class="sxs-lookup"><span data-stu-id="ceef9-115">For more information, see [Getting Ready for 64-bit Windows](/windows/desktop/WinProg64/getting-ready-for-64-bit-windows).</span></span> <span data-ttu-id="ceef9-116">其他功能包括 [標頭注釋](header-annotations.md) 和 [嚴格的類型檢查](strict-type-checking.md)。</span><span class="sxs-lookup"><span data-stu-id="ceef9-116">Additional features include [Header Annotations](header-annotations.md) and [STRICT Type Checking](strict-type-checking.md).</span></span>

-   [<span data-ttu-id="ceef9-117">Visual C++ 和 Windows 標頭檔</span><span class="sxs-lookup"><span data-stu-id="ceef9-117">Visual C++ and the Windows Header Files</span></span>](#visual-c-and-the-windows-header-files)
-   [<span data-ttu-id="ceef9-118">條件式宣告的宏</span><span class="sxs-lookup"><span data-stu-id="ceef9-118">Macros for Conditional Declarations</span></span>](#macros-for-conditional-declarations)
-   [<span data-ttu-id="ceef9-119">設定 WINVER 或 \_ WIN32 \_ WINNT</span><span class="sxs-lookup"><span data-stu-id="ceef9-119">Setting WINVER or \_WIN32\_WINNT</span></span>](#setting-winver-or-_win32_winnt)
-   [<span data-ttu-id="ceef9-120">控制結構封裝</span><span class="sxs-lookup"><span data-stu-id="ceef9-120">Controlling Structure Packing</span></span>](#controlling-structure-packing)
-   [<span data-ttu-id="ceef9-121">更快速的組建，包含較小的標頭檔</span><span class="sxs-lookup"><span data-stu-id="ceef9-121">Faster Builds with Smaller Header Files</span></span>](#faster-builds-with-smaller-header-files)
-   [<span data-ttu-id="ceef9-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="ceef9-122">Related topics</span></span>](#related-topics)

## <a name="visual-c-and-the-windows-header-files"></a><span data-ttu-id="ceef9-123">Visual C++ 和 Windows 標頭檔</span><span class="sxs-lookup"><span data-stu-id="ceef9-123">Visual C++ and the Windows Header Files</span></span>

<span data-ttu-id="ceef9-124">Microsoft Visual C++ 包含 Visual C++ 發行時的最新 Windows 標頭檔案的複本。</span><span class="sxs-lookup"><span data-stu-id="ceef9-124">Microsoft Visual C++ includes copies of the Windows header files that were current at the time Visual C++ was released.</span></span> <span data-ttu-id="ceef9-125">因此，如果您從 SDK 安裝更新的標頭檔，您的電腦上可能會有多個版本的 Windows 標頭檔。</span><span class="sxs-lookup"><span data-stu-id="ceef9-125">Therefore, if you install updated header files from an SDK, you may end up with multiple versions of the Windows header files on your computer.</span></span> <span data-ttu-id="ceef9-126">如果您不確定您使用的是最新版的 SDK 標頭檔，當您在編譯使用 Visual C++ 發行之後引進之功能的程式碼時，將會收到下列錯誤碼：錯誤 C2065：未宣告的識別碼。</span><span class="sxs-lookup"><span data-stu-id="ceef9-126">If you do not ensure that you are using the latest version of the SDK header files, you will receive the following error code when compiling code that uses features that were introduced after Visual C++ was released: error C2065: undeclared identifier.</span></span>

## <a name="macros-for-conditional-declarations"></a><span data-ttu-id="ceef9-127">條件式宣告的宏</span><span class="sxs-lookup"><span data-stu-id="ceef9-127">Macros for Conditional Declarations</span></span>

<span data-ttu-id="ceef9-128">某些相依于特定 Windows 版本的函式是使用條件式程式碼宣告的。</span><span class="sxs-lookup"><span data-stu-id="ceef9-128">Certain functions that depend on a particular version of Windows are declared using conditional code.</span></span> <span data-ttu-id="ceef9-129">這可讓您使用編譯器來偵測您的應用程式是否使用其目標版本 (s) Windows 上不支援的功能。</span><span class="sxs-lookup"><span data-stu-id="ceef9-129">This enables you to use the compiler to detect whether your application uses functions that are not supported on its target version(s) of Windows.</span></span> <span data-ttu-id="ceef9-130">若要編譯使用這些函數的應用程式，您必須定義適當的宏。</span><span class="sxs-lookup"><span data-stu-id="ceef9-130">To compile an application that uses these functions, you must define the appropriate macros.</span></span> <span data-ttu-id="ceef9-131">否則，您會收到 C2065 錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="ceef9-131">Otherwise, you will receive the C2065 error message.</span></span>

<span data-ttu-id="ceef9-132">Windows 標頭檔會使用宏來指出哪些版本的 Windows 支援許多程式設計項目。</span><span class="sxs-lookup"><span data-stu-id="ceef9-132">The Windows header files use macros to indicate which versions of Windows support many programming elements.</span></span> <span data-ttu-id="ceef9-133">因此，您必須定義這些宏，以使用每個主要作業系統版本引進的新功能。</span><span class="sxs-lookup"><span data-stu-id="ceef9-133">Therefore, you must define these macros to use new functionality introduced in each major operating system release.</span></span> <span data-ttu-id="ceef9-134"> (個別的標頭檔可能會使用不同的宏;因此，如果發生編譯問題，請檢查包含條件式定義定義的標頭檔。 ) 如需詳細資訊，請參閱 Sdkddkver.h。</span><span class="sxs-lookup"><span data-stu-id="ceef9-134">(Individual header files may use different macros; therefore, if compilation problems occur, check the header file that contains the definition for conditional definitions.) For more information, see SdkDdkVer.h.</span></span>

<span data-ttu-id="ceef9-135">下表描述 Windows 標頭檔中使用的慣用宏。</span><span class="sxs-lookup"><span data-stu-id="ceef9-135">The following table describes the preferred macros used in the Windows header files.</span></span> <span data-ttu-id="ceef9-136">如果您定義 NTDDI \_ 版本，您也必須定義 \_ WIN32 \_ WINNT。</span><span class="sxs-lookup"><span data-stu-id="ceef9-136">If you define NTDDI\_VERSION, you must also define \_WIN32\_WINNT.</span></span>



| <span data-ttu-id="ceef9-137">需要的最低系統</span><span class="sxs-lookup"><span data-stu-id="ceef9-137">Minimum system required</span></span>                       | <span data-ttu-id="ceef9-138">NTDDI 版本的值 \_</span><span class="sxs-lookup"><span data-stu-id="ceef9-138">Value for NTDDI\_VERSION</span></span>            |
|-----------------------------------------------|-------------------------------------|
| <span data-ttu-id="ceef9-139">Windows 10 1903 "19H1"</span><span class="sxs-lookup"><span data-stu-id="ceef9-139">Windows 10 1903 "19H1"</span></span>                        | <span data-ttu-id="ceef9-140">**NTDDI \_WIN10 \_ 19H1** (0x0A000007) </span><span class="sxs-lookup"><span data-stu-id="ceef9-140">**NTDDI\_WIN10\_19H1** (0x0A000007)</span></span> |
| <span data-ttu-id="ceef9-141">Windows 10 1809 "Redstone 5"</span><span class="sxs-lookup"><span data-stu-id="ceef9-141">Windows 10 1809 "Redstone 5"</span></span>                  | <span data-ttu-id="ceef9-142">**NTDDI \_WIN10 \_ RS5** (0x0A000006) </span><span class="sxs-lookup"><span data-stu-id="ceef9-142">**NTDDI\_WIN10\_RS5** (0x0A000006)</span></span>  |
| <span data-ttu-id="ceef9-143">Windows 10 1803 "Redstone 4"</span><span class="sxs-lookup"><span data-stu-id="ceef9-143">Windows 10 1803 "Redstone 4"</span></span>                  | <span data-ttu-id="ceef9-144">**NTDDI \_WIN10 \_ RS4** (0x0A000005) </span><span class="sxs-lookup"><span data-stu-id="ceef9-144">**NTDDI\_WIN10\_RS4** (0x0A000005)</span></span>  |
| <span data-ttu-id="ceef9-145">Windows 10 1709 "Redstone 3"</span><span class="sxs-lookup"><span data-stu-id="ceef9-145">Windows 10 1709 "Redstone 3"</span></span>                  | <span data-ttu-id="ceef9-146">**NTDDI \_WIN10 \_ RS3** (0x0A000004) </span><span class="sxs-lookup"><span data-stu-id="ceef9-146">**NTDDI\_WIN10\_RS3** (0x0A000004)</span></span>  |
| <span data-ttu-id="ceef9-147">Windows 10 1703 "Redstone 2"</span><span class="sxs-lookup"><span data-stu-id="ceef9-147">Windows 10 1703 "Redstone 2"</span></span>                  | <span data-ttu-id="ceef9-148">**NTDDI \_WIN10 \_ RS2** (0x0A000003) </span><span class="sxs-lookup"><span data-stu-id="ceef9-148">**NTDDI\_WIN10\_RS2** (0x0A000003)</span></span>  |
| <span data-ttu-id="ceef9-149">Windows 10 1607 "Redstone 1"</span><span class="sxs-lookup"><span data-stu-id="ceef9-149">Windows 10 1607 "Redstone 1"</span></span>                  | <span data-ttu-id="ceef9-150">**NTDDI \_WIN10 \_ RS1** (0x0A000002) </span><span class="sxs-lookup"><span data-stu-id="ceef9-150">**NTDDI\_WIN10\_RS1** (0x0A000002)</span></span>  |
| <span data-ttu-id="ceef9-151">Windows 10 1511 「閾值2」</span><span class="sxs-lookup"><span data-stu-id="ceef9-151">Windows 10 1511 "Threshold 2"</span></span>                 | <span data-ttu-id="ceef9-152">**NTDDI \_WIN10 \_ TH2** (0x0A000001) </span><span class="sxs-lookup"><span data-stu-id="ceef9-152">**NTDDI\_WIN10\_TH2** (0x0A000001)</span></span>  |
| <span data-ttu-id="ceef9-153">Windows 10 1507 「閾值」</span><span class="sxs-lookup"><span data-stu-id="ceef9-153">Windows 10 1507 "Threshold"</span></span>                   | <span data-ttu-id="ceef9-154">**NTDDI \_WIN10** (0x0A000000) </span><span class="sxs-lookup"><span data-stu-id="ceef9-154">**NTDDI\_WIN10** (0x0A000000)</span></span>       |
| <span data-ttu-id="ceef9-155">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="ceef9-155">Windows 8.1</span></span>                                   | <span data-ttu-id="ceef9-156">**NTDDI \_WINBLUE** (0x06030000) </span><span class="sxs-lookup"><span data-stu-id="ceef9-156">**NTDDI\_WINBLUE** (0x06030000)</span></span>     |
| <span data-ttu-id="ceef9-157">Windows 8</span><span class="sxs-lookup"><span data-stu-id="ceef9-157">Windows 8</span></span>                                     | <span data-ttu-id="ceef9-158">**NTDDI \_WIN8** (0x06020000) </span><span class="sxs-lookup"><span data-stu-id="ceef9-158">**NTDDI\_WIN8** (0x06020000)</span></span>        |
| <span data-ttu-id="ceef9-159">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ceef9-159">Windows 7</span></span>                                     | <span data-ttu-id="ceef9-160">**NTDDI \_WIN7** (0x06010000) </span><span class="sxs-lookup"><span data-stu-id="ceef9-160">**NTDDI\_WIN7** (0x06010000)</span></span>        |
| <span data-ttu-id="ceef9-161">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ceef9-161">Windows Server 2008</span></span>                           | <span data-ttu-id="ceef9-162">**NTDDI \_WS08** (0x06000100) </span><span class="sxs-lookup"><span data-stu-id="ceef9-162">**NTDDI\_WS08** (0x06000100)</span></span>        |
| <span data-ttu-id="ceef9-163">Windows Vista 包含 Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="ceef9-163">Windows Vista with Service Pack 1 (SP1)</span></span>       | <span data-ttu-id="ceef9-164">**NTDDI \_VISTASP1** (0x06000100) </span><span class="sxs-lookup"><span data-stu-id="ceef9-164">**NTDDI\_VISTASP1** (0x06000100)</span></span>    |
| <span data-ttu-id="ceef9-165">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ceef9-165">Windows Vista</span></span>                                 | <span data-ttu-id="ceef9-166">**NTDDI \_VISTA** (0x06000000) </span><span class="sxs-lookup"><span data-stu-id="ceef9-166">**NTDDI\_VISTA** (0x06000000)</span></span>       |
| <span data-ttu-id="ceef9-167">Windows Server 2003 Service Pack 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="ceef9-167">Windows Server 2003 with Service Pack 2 (SP2)</span></span> | <span data-ttu-id="ceef9-168">**NTDDI \_WS03SP2** (0x05020200) </span><span class="sxs-lookup"><span data-stu-id="ceef9-168">**NTDDI\_WS03SP2** (0x05020200)</span></span>     |
| <span data-ttu-id="ceef9-169">Windows Server 2003 含 Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="ceef9-169">Windows Server 2003 with Service Pack 1 (SP1)</span></span> | <span data-ttu-id="ceef9-170">**NTDDI \_WS03SP1** (0x05020100) </span><span class="sxs-lookup"><span data-stu-id="ceef9-170">**NTDDI\_WS03SP1** (0x05020100)</span></span>     |
| <span data-ttu-id="ceef9-171">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ceef9-171">Windows Server 2003</span></span>                           | <span data-ttu-id="ceef9-172">**NTDDI \_WS03** (0x05020000) </span><span class="sxs-lookup"><span data-stu-id="ceef9-172">**NTDDI\_WS03** (0x05020000)</span></span>        |
| <span data-ttu-id="ceef9-173">Windows XP (含 Service Pack 3，SP3)</span><span class="sxs-lookup"><span data-stu-id="ceef9-173">Windows XP with Service Pack 3 (SP3)</span></span>          | <span data-ttu-id="ceef9-174">**NTDDI \_WINXPSP3** (0x05010300) </span><span class="sxs-lookup"><span data-stu-id="ceef9-174">**NTDDI\_WINXPSP3** (0x05010300)</span></span>    |
| <span data-ttu-id="ceef9-175">Windows XP with Service Pack 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="ceef9-175">Windows XP with Service Pack 2 (SP2)</span></span>          | <span data-ttu-id="ceef9-176">**NTDDI \_WINXPSP2** (0x05010200) </span><span class="sxs-lookup"><span data-stu-id="ceef9-176">**NTDDI\_WINXPSP2** (0x05010200)</span></span>    |
| <span data-ttu-id="ceef9-177">Windows XP Service Pack 1 (SP1) </span><span class="sxs-lookup"><span data-stu-id="ceef9-177">Windows XP with Service Pack 1 (SP1)</span></span>          | <span data-ttu-id="ceef9-178">**NTDDI \_WINXPSP1** (0x05010100) </span><span class="sxs-lookup"><span data-stu-id="ceef9-178">**NTDDI\_WINXPSP1** (0x05010100)</span></span>    |
| <span data-ttu-id="ceef9-179">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ceef9-179">Windows XP</span></span>                                    | <span data-ttu-id="ceef9-180">**NTDDI \_>TEST-WINXP** (0x05010000) </span><span class="sxs-lookup"><span data-stu-id="ceef9-180">**NTDDI\_WINXP** (0x05010000)</span></span>       |



 

<span data-ttu-id="ceef9-181">下表說明 Windows 標頭檔中使用的其他宏。</span><span class="sxs-lookup"><span data-stu-id="ceef9-181">The following tables describe other macros used in the Windows header files.</span></span>



| <span data-ttu-id="ceef9-182">需要的最低系統</span><span class="sxs-lookup"><span data-stu-id="ceef9-182">Minimum system required</span></span>                           | <span data-ttu-id="ceef9-183">\_WIN32 \_ WINNT 和 WINVER 的最小值</span><span class="sxs-lookup"><span data-stu-id="ceef9-183">Minimum value for \_WIN32\_WINNT and WINVER</span></span> |
|---------------------------------------------------|---------------------------------------------|
| <span data-ttu-id="ceef9-184">Windows 10</span><span class="sxs-lookup"><span data-stu-id="ceef9-184">Windows 10</span></span>                                        | <span data-ttu-id="ceef9-185">**\_ WIN32 \_ WINNT \_ WIN10** (0x0A00) </span><span class="sxs-lookup"><span data-stu-id="ceef9-185">**\_WIN32\_WINNT\_WIN10** (0x0A00)</span></span>          |
| <span data-ttu-id="ceef9-186">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="ceef9-186">Windows 8.1</span></span>                                       | <span data-ttu-id="ceef9-187">**\_ WIN32 \_ WINNT \_ WINBLUE** (0x0603) </span><span class="sxs-lookup"><span data-stu-id="ceef9-187">**\_WIN32\_WINNT\_WINBLUE** (0x0603)</span></span>        |
| <span data-ttu-id="ceef9-188">Windows 8</span><span class="sxs-lookup"><span data-stu-id="ceef9-188">Windows 8</span></span>                                         | <span data-ttu-id="ceef9-189">**\_ WIN32 \_ WINNT \_ WIN8** (0x0602) </span><span class="sxs-lookup"><span data-stu-id="ceef9-189">**\_WIN32\_WINNT\_WIN8** (0x0602)</span></span>           |
| <span data-ttu-id="ceef9-190">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ceef9-190">Windows 7</span></span>                                         | <span data-ttu-id="ceef9-191">**\_ WIN32 \_ WINNT \_ WIN7** (0x0601) </span><span class="sxs-lookup"><span data-stu-id="ceef9-191">**\_WIN32\_WINNT\_WIN7** (0x0601)</span></span>           |
| <span data-ttu-id="ceef9-192">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ceef9-192">Windows Server 2008</span></span>                               | <span data-ttu-id="ceef9-193">**\_ WIN32 \_ WINNT \_ WS08** (0x0600) </span><span class="sxs-lookup"><span data-stu-id="ceef9-193">**\_WIN32\_WINNT\_WS08** (0x0600)</span></span>           |
| <span data-ttu-id="ceef9-194">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ceef9-194">Windows Vista</span></span>                                     | <span data-ttu-id="ceef9-195">**\_ WIN32 \_ WINNT \_ VISTA** (0x0600) </span><span class="sxs-lookup"><span data-stu-id="ceef9-195">**\_WIN32\_WINNT\_VISTA** (0x0600)</span></span>          |
| <span data-ttu-id="ceef9-196">Windows Server 2003 （含 SP1）、Windows XP （含 SP2）</span><span class="sxs-lookup"><span data-stu-id="ceef9-196">Windows Server 2003 with SP1, Windows XP with SP2</span></span> | <span data-ttu-id="ceef9-197">**\_ WIN32 \_ WINNT \_ WS03** (0x0502) </span><span class="sxs-lookup"><span data-stu-id="ceef9-197">**\_WIN32\_WINNT\_WS03** (0x0502)</span></span>           |
| <span data-ttu-id="ceef9-198">Windows Server 2003、Windows XP</span><span class="sxs-lookup"><span data-stu-id="ceef9-198">Windows Server 2003, Windows XP</span></span>                   | <span data-ttu-id="ceef9-199">**\_ WIN32 \_ WINNT \_ >test-winxp** (0x0501) </span><span class="sxs-lookup"><span data-stu-id="ceef9-199">**\_WIN32\_WINNT\_WINXP** (0x0501)</span></span>          |



 



| <span data-ttu-id="ceef9-200">需要的最低版本</span><span class="sxs-lookup"><span data-stu-id="ceef9-200">Minimum version required</span></span>          | <span data-ttu-id="ceef9-201">\_WIN32 IE 的最小值 \_</span><span class="sxs-lookup"><span data-stu-id="ceef9-201">Minimum value of \_WIN32\_IE</span></span>      |
|-----------------------------------|-----------------------------------|
| <span data-ttu-id="ceef9-202">Internet Explorer 11。0</span><span class="sxs-lookup"><span data-stu-id="ceef9-202">Internet Explorer 11.0</span></span>            | <span data-ttu-id="ceef9-203">**\_ WIN32 \_ IE \_ IE110** (0x0A00) </span><span class="sxs-lookup"><span data-stu-id="ceef9-203">**\_WIN32\_IE\_IE110** (0x0A00)</span></span>   |
| <span data-ttu-id="ceef9-204">Internet Explorer 10。0</span><span class="sxs-lookup"><span data-stu-id="ceef9-204">Internet Explorer 10.0</span></span>            | <span data-ttu-id="ceef9-205">**\_ WIN32 \_ IE \_ IE100** (0x0A00) </span><span class="sxs-lookup"><span data-stu-id="ceef9-205">**\_WIN32\_IE\_IE100** (0x0A00)</span></span>   |
| <span data-ttu-id="ceef9-206">Internet Explorer 9.0</span><span class="sxs-lookup"><span data-stu-id="ceef9-206">Internet Explorer 9.0</span></span>             | <span data-ttu-id="ceef9-207">**\_ WIN32 \_ IE \_ IE90** (0x0900) </span><span class="sxs-lookup"><span data-stu-id="ceef9-207">**\_WIN32\_IE\_IE90** (0x0900)</span></span>    |
| <span data-ttu-id="ceef9-208">Internet Explorer 8.0</span><span class="sxs-lookup"><span data-stu-id="ceef9-208">Internet Explorer 8.0</span></span>             | <span data-ttu-id="ceef9-209">**\_ WIN32 \_ IE \_ IE80** (0x0800) </span><span class="sxs-lookup"><span data-stu-id="ceef9-209">**\_WIN32\_IE\_IE80** (0x0800)</span></span>    |
| <span data-ttu-id="ceef9-210">Internet Explorer 7.0</span><span class="sxs-lookup"><span data-stu-id="ceef9-210">Internet Explorer 7.0</span></span>             | <span data-ttu-id="ceef9-211">**\_ WIN32 \_ IE \_ IE70** (0x0700) </span><span class="sxs-lookup"><span data-stu-id="ceef9-211">**\_WIN32\_IE\_IE70** (0x0700)</span></span>    |
| <span data-ttu-id="ceef9-212">Internet Explorer 6.0 SP2</span><span class="sxs-lookup"><span data-stu-id="ceef9-212">Internet Explorer 6.0 SP2</span></span>         | <span data-ttu-id="ceef9-213">**\_ WIN32 \_ IE \_ IE60SP2** (0x0603) </span><span class="sxs-lookup"><span data-stu-id="ceef9-213">**\_WIN32\_IE\_IE60SP2** (0x0603)</span></span> |
| <span data-ttu-id="ceef9-214">Internet Explorer 6.0 SP1</span><span class="sxs-lookup"><span data-stu-id="ceef9-214">Internet Explorer 6.0 SP1</span></span>         | <span data-ttu-id="ceef9-215">**\_ WIN32 \_ IE \_ IE60SP1** (0x0601) </span><span class="sxs-lookup"><span data-stu-id="ceef9-215">**\_WIN32\_IE\_IE60SP1** (0x0601)</span></span> |
| <span data-ttu-id="ceef9-216">Internet Explorer 6.0</span><span class="sxs-lookup"><span data-stu-id="ceef9-216">Internet Explorer 6.0</span></span>             | <span data-ttu-id="ceef9-217">**\_ WIN32 \_ IE \_ IE60** (0x0600) </span><span class="sxs-lookup"><span data-stu-id="ceef9-217">**\_WIN32\_IE\_IE60** (0x0600)</span></span>    |
| <span data-ttu-id="ceef9-218">Internet Explorer 5.5</span><span class="sxs-lookup"><span data-stu-id="ceef9-218">Internet Explorer 5.5</span></span>             | <span data-ttu-id="ceef9-219">**\_ WIN32 \_ IE \_ IE55** (0x0550) </span><span class="sxs-lookup"><span data-stu-id="ceef9-219">**\_WIN32\_IE\_IE55** (0x0550)</span></span>    |
| <span data-ttu-id="ceef9-220">Internet Explorer 5.01</span><span class="sxs-lookup"><span data-stu-id="ceef9-220">Internet Explorer 5.01</span></span>            | <span data-ttu-id="ceef9-221">**\_ WIN32 \_ IE \_ IE501** (0x0501) </span><span class="sxs-lookup"><span data-stu-id="ceef9-221">**\_WIN32\_IE\_IE501** (0x0501)</span></span>   |
| <span data-ttu-id="ceef9-222">Internet Explorer 5.0、5.0 a、5.0 b</span><span class="sxs-lookup"><span data-stu-id="ceef9-222">Internet Explorer 5.0, 5.0a, 5.0b</span></span> | <span data-ttu-id="ceef9-223">**\_ WIN32 \_ IE \_ IE50** (0x0500) </span><span class="sxs-lookup"><span data-stu-id="ceef9-223">**\_WIN32\_IE\_IE50** (0x0500)</span></span>    |



 

## <a name="setting-winver-or-_win32_winnt"></a><span data-ttu-id="ceef9-224">設定 WINVER 或 \_ WIN32 \_ WINNT</span><span class="sxs-lookup"><span data-stu-id="ceef9-224">Setting WINVER or \_WIN32\_WINNT</span></span>

<span data-ttu-id="ceef9-225">您可以使用每個原始程式檔中的 define 語句來定義這些符號 \# ，或是指定 Visual C++ 所支援的/d 編譯器選項來定義這些符號。</span><span class="sxs-lookup"><span data-stu-id="ceef9-225">You can define these symbols by using the \#define statement in each source file, or by specifying the /D compiler option supported by Visual C++.</span></span>

<span data-ttu-id="ceef9-226">例如，若要在原始程式檔中設定 WINVER，請使用下列語句：</span><span class="sxs-lookup"><span data-stu-id="ceef9-226">For example, to set WINVER in your source file, use the following statement:</span></span>

`#define WINVER 0x0502`

<span data-ttu-id="ceef9-227">若要 \_ \_ 在原始程式檔中設定 WIN32 WINNT，請使用下列語句：</span><span class="sxs-lookup"><span data-stu-id="ceef9-227">To set \_WIN32\_WINNT in your source file, use the following statement:</span></span>

`#define _WIN32_WINNT 0x0502`

<span data-ttu-id="ceef9-228">若要 \_ \_ 使用/d 編譯器選項設定 WIN32 WINNT，請使用下列命令：</span><span class="sxs-lookup"><span data-stu-id="ceef9-228">To set \_WIN32\_WINNT using the /D compiler option, use the following command:</span></span>

<span data-ttu-id="ceef9-229">**cl-c/d \_WIN32 \_ WINNT = 0x0502** _source_**.cpp**</span><span class="sxs-lookup"><span data-stu-id="ceef9-229">**cl -c /D\_WIN32\_WINNT=0x0502** _source_**.cpp**</span></span>

<span data-ttu-id="ceef9-230">如需使用/D 編譯器選項的詳細資訊，請參閱 [/d (預處理器定義) ](/cpp/build/reference/d-preprocessor-definitions)。</span><span class="sxs-lookup"><span data-stu-id="ceef9-230">For information on using the /D compiler option, see [/D (preprocessor definitions)](/cpp/build/reference/d-preprocessor-definitions).</span></span>

<span data-ttu-id="ceef9-231">請注意，最新版本的 Windows 中所引進的某些功能可能會新增至舊版 Windows 的 service pack 中。</span><span class="sxs-lookup"><span data-stu-id="ceef9-231">Note that some features introduced in the latest version of Windows may be added to a service pack for a previous version of Windows.</span></span> <span data-ttu-id="ceef9-232">因此，若要以 service pack 為目標，您可能需要 \_ \_ 使用下一個主要作業系統版本的值來定義 WIN32 WINNT。</span><span class="sxs-lookup"><span data-stu-id="ceef9-232">Therefore, to target a service pack, you may need to define \_WIN32\_WINNT with the value for the next major operating system release.</span></span> <span data-ttu-id="ceef9-233">例如， [**GetDllDirectory**](/windows/desktop/api/winbase/nf-winbase-getdlldirectorya) 函式是在 Windows Server 2003 中引進，如果 \_ WIN32 \_ WINNT 0x0502 或更大，則會有條件地定義。</span><span class="sxs-lookup"><span data-stu-id="ceef9-233">For example, the [**GetDllDirectory**](/windows/desktop/api/winbase/nf-winbase-getdlldirectorya) function was introduced in Windows Server 2003 and is conditionally defined if \_WIN32\_WINNT is 0x0502 or greater.</span></span> <span data-ttu-id="ceef9-234">此函式也已新增至 Windows XP SP1。</span><span class="sxs-lookup"><span data-stu-id="ceef9-234">This function was also added to Windows XP with SP1.</span></span> <span data-ttu-id="ceef9-235">因此，如果您將 \_ WIN32 WINNT 定義 \_ 為以 windows xp 為目標的0x0501，您將會錯過 WINDOWS xp SP1 中定義的功能。</span><span class="sxs-lookup"><span data-stu-id="ceef9-235">Therefore, if you were to define \_WIN32\_WINNT as 0x0501 to target Windows XP, you would miss features that are defined in Windows XP with SP1.</span></span>

## <a name="controlling-structure-packing"></a><span data-ttu-id="ceef9-236">控制結構封裝</span><span class="sxs-lookup"><span data-stu-id="ceef9-236">Controlling Structure Packing</span></span>

<span data-ttu-id="ceef9-237">專案應該編譯為使用預設結構封裝（目前為8個位元組，因為最大整數類型是8個位元組）。</span><span class="sxs-lookup"><span data-stu-id="ceef9-237">Projects should be compiled to use the default structure packing, which is currently 8 bytes because the largest integral type is 8 bytes.</span></span> <span data-ttu-id="ceef9-238">這麼做可確保在應用程式中，所有結構類型都會編譯成與 Windows API 預期相同的對齊方式。</span><span class="sxs-lookup"><span data-stu-id="ceef9-238">Doing so ensures that all structure types within the header files are compiled into the application with the same alignment the Windows API expects.</span></span> <span data-ttu-id="ceef9-239">它也可確保具有8位元組值的結構正確對齊，且不會在強制執行資料對齊的處理器上造成對齊錯誤。</span><span class="sxs-lookup"><span data-stu-id="ceef9-239">It also ensures that structures with 8-byte values are properly aligned and will not cause alignment faults on processors that enforce data alignment.</span></span>

<span data-ttu-id="ceef9-240">如需詳細資訊，請參閱 [/Zp (結構成員對齊) ](/cpp/build/reference/zp-struct-member-alignment) 或 [套件](/cpp/preprocessor/pack)。</span><span class="sxs-lookup"><span data-stu-id="ceef9-240">For more information, see [/Zp (struct member alignment)](/cpp/build/reference/zp-struct-member-alignment) or [pack](/cpp/preprocessor/pack).</span></span>

## <a name="faster-builds-with-smaller-header-files"></a><span data-ttu-id="ceef9-241">更快速的組建，包含較小的標頭檔</span><span class="sxs-lookup"><span data-stu-id="ceef9-241">Faster Builds with Smaller Header Files</span></span>

<span data-ttu-id="ceef9-242">您可以排除一些較不常用的 API 宣告，以縮減 Windows 標頭檔的大小，如下所示：</span><span class="sxs-lookup"><span data-stu-id="ceef9-242">You can reduce the size of the Windows header files by excluding some of the less common API declarations as follows:</span></span>

-   <span data-ttu-id="ceef9-243">定義 WIN32 的 \_ 精簡 \_ 和 MEAN， \_ 以排除 Api，例如加密、DDE、RPC、Shell 和 Windows 通訊端。</span><span class="sxs-lookup"><span data-stu-id="ceef9-243">Define WIN32\_LEAN\_AND\_MEAN to exclude APIs such as Cryptography, DDE, RPC, Shell, and Windows Sockets.</span></span>

    `#define WIN32_LEAN_AND_MEAN`

-   <span data-ttu-id="ceef9-244">定義一個或多個不包含 api 的 *api* 符號。</span><span class="sxs-lookup"><span data-stu-id="ceef9-244">Define one or more of the NO *api* symbols to exclude the API.</span></span> <span data-ttu-id="ceef9-245">例如，NOCOMM 會排除序列通訊 API。</span><span class="sxs-lookup"><span data-stu-id="ceef9-245">For example, NOCOMM excludes the serial communication API.</span></span> <span data-ttu-id="ceef9-246">如需不支援 *api* 符號的清單，請參閱 Windows .h。</span><span class="sxs-lookup"><span data-stu-id="ceef9-246">For a list of support NO *api* symbols, see Windows.h.</span></span>

    `#define NOCOMM`

## <a name="related-topics"></a><span data-ttu-id="ceef9-247">相關主題</span><span class="sxs-lookup"><span data-stu-id="ceef9-247">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ceef9-248">Windows SDK 下載網站</span><span class="sxs-lookup"><span data-stu-id="ceef9-248">Windows SDK download site</span></span>](https://msdn.microsoft.com/windowsserver/bb980924.aspx)
</dt> </dl>

 

 
---
description: 本節說明如何判斷您的應用程式在哪一個版本的 Shell Dll 上執行，以及如何以特定版本的應用程式為目標。
title: 命令介面和 Shlwapi DLL 版本
ms.topic: article
ms.date: 09/24/2020
ms.assetid: ecfb6484-a1d6-4ace-8457-3940b111a4d2
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 49fb1767b7074da6480a47c52eb1384fb935317b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192674"
---
# <a name="shell-and-shlwapi-dll-versions"></a><span data-ttu-id="0d25d-103">命令介面和 Shlwapi DLL 版本</span><span class="sxs-lookup"><span data-stu-id="0d25d-103">Shell and Shlwapi DLL Versions</span></span>

<span data-ttu-id="0d25d-104">本節說明如何判斷您的應用程式在哪一個版本的 Shell Dll 上執行，以及如何以特定版本的應用程式為目標。</span><span class="sxs-lookup"><span data-stu-id="0d25d-104">This section describes how to determine which version of the Shell DLLs your application is running on and how to target your application for a specific version.</span></span>

-   [<span data-ttu-id="0d25d-105">DLL 版本號碼</span><span class="sxs-lookup"><span data-stu-id="0d25d-105">DLL Version Numbers</span></span>](#dll-version-numbers)
-   [<span data-ttu-id="0d25d-106">使用 DllGetVersion 來判斷版本號碼</span><span class="sxs-lookup"><span data-stu-id="0d25d-106">Using DllGetVersion to Determine the Version Number</span></span>](#using-dllgetversion-to-determine-the-version-number)
    -   [<span data-ttu-id="0d25d-107">使用 DllGetVersion</span><span class="sxs-lookup"><span data-stu-id="0d25d-107">Using DllGetVersion</span></span>](#using-dllgetversion)
-   [<span data-ttu-id="0d25d-108">專案版本</span><span class="sxs-lookup"><span data-stu-id="0d25d-108">Project Versions</span></span>](#project-versions)

## <a name="dll-version-numbers"></a><span data-ttu-id="0d25d-109">DLL 版本號碼</span><span class="sxs-lookup"><span data-stu-id="0d25d-109">DLL Version Numbers</span></span>

<span data-ttu-id="0d25d-110">Shell 檔中所討論的所有程式設計項目，都包含在兩個 Dll 中： Shell32.dll 和 Shlwapi.dll。</span><span class="sxs-lookup"><span data-stu-id="0d25d-110">All but a handful of the programming elements discussed in the Shell documentation are contained in two DLLs: Shell32.dll and Shlwapi.dll.</span></span> <span data-ttu-id="0d25d-111">由於持續的增強功能，這些 Dll 的不同版本會執行不同的功能。</span><span class="sxs-lookup"><span data-stu-id="0d25d-111">Because of ongoing enhancements, different versions of these DLLs implement different features.</span></span> <span data-ttu-id="0d25d-112">在整個 Shell 參考檔中，每個程式設計項目都會指定支援的最低 DLL 版本號碼。</span><span class="sxs-lookup"><span data-stu-id="0d25d-112">Throughout the Shell reference documentation, each programming element specifies a minimum supported DLL version number.</span></span> <span data-ttu-id="0d25d-113">此版本號碼表示程式設計專案會在該版本和後續 DLL 版本中執行，除非另有指定。</span><span class="sxs-lookup"><span data-stu-id="0d25d-113">This version number indicates that the programming element is implemented in that version and subsequent versions of the DLL unless otherwise specified.</span></span> <span data-ttu-id="0d25d-114">如果未指定版本號碼，則會在所有現有版本的 DLL 中執行程式設計專案。</span><span class="sxs-lookup"><span data-stu-id="0d25d-114">If no version number is specified, the programming element is implemented in all existing versions of the DLL.</span></span>

<span data-ttu-id="0d25d-115">在 Windows XP 之前，新的 Shell32.dll 和 Shlwapi.dll 版本有時會隨著新版本的 Windows Internet Explorer 而提供。</span><span class="sxs-lookup"><span data-stu-id="0d25d-115">Before Windows XP, new Shell32.dll and Shlwapi.dll versions were sometimes provided with new versions of Windows Internet Explorer.</span></span> <span data-ttu-id="0d25d-116">從 Windows XP 版以來，這些 Dll 不再提供為新版 Windows 本身以外的可轉散發檔案。</span><span class="sxs-lookup"><span data-stu-id="0d25d-116">As of Windows XP, those DLLs were no longer provided as redistributable files outside of new versions of Windows itself.</span></span> <span data-ttu-id="0d25d-117">下表概述不同的 DLL 版本，以及它們如何散發回可追溯至 Microsoft Internet Explorer 3.0、Windows 95 和 Microsoft Windows NT 4.0。</span><span class="sxs-lookup"><span data-stu-id="0d25d-117">The following table outlines the different DLL versions and how they were distributed dating back to Microsoft Internet Explorer 3.0, Windows 95, and Microsoft Windows NT 4.0.</span></span>

<span data-ttu-id="0d25d-118">您可以在 Windows 95 和 Microsoft Windows NT 4.0 的原始版本中找到 Shell32.dll 4.0 版。</span><span class="sxs-lookup"><span data-stu-id="0d25d-118">Shell32.dll version 4.0 is found in the original versions of Windows 95 and Microsoft Windows NT 4.0.</span></span> <span data-ttu-id="0d25d-119">Shell 未隨 Internet Explorer 3.0 版本更新，因此 Shell32.dll 沒有4.70 版。</span><span class="sxs-lookup"><span data-stu-id="0d25d-119">The Shell was not updated with the Internet Explorer 3.0 release, so Shell32.dll does not have a version 4.70.</span></span> <span data-ttu-id="0d25d-120">Shell32.dll 版本4.71 和4.72 隨附于對應的 Internet Explorer 版本，但不一定會安裝 (請參閱附注 1) 。</span><span class="sxs-lookup"><span data-stu-id="0d25d-120">Shell32.dll versions 4.71 and 4.72 were shipped with the corresponding Internet Explorer releases, but they were not necessarily installed (see note 1).</span></span> <span data-ttu-id="0d25d-121">若為 Microsoft Internet Explorer 4.01 和 Windows 98 的發行版本，Shell32.dll 和 Shlwapi.dll 分離的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="0d25d-121">For releases subsequent to Microsoft Internet Explorer 4.01 and Windows 98, the version numbers for Shell32.dll and Shlwapi.dll diverge.</span></span> <span data-ttu-id="0d25d-122">一般而言，您應該假設 Dll 具有不同的版本號碼，並個別測試每一個。</span><span class="sxs-lookup"><span data-stu-id="0d25d-122">In general, you should assume that the DLLs have different version numbers and test each one separately.</span></span>

#### <a name="shell32dll"></a><span data-ttu-id="0d25d-123">Shell32.dll</span><span class="sxs-lookup"><span data-stu-id="0d25d-123">Shell32.dll</span></span>

| <span data-ttu-id="0d25d-124">版本</span><span class="sxs-lookup"><span data-stu-id="0d25d-124">Version</span></span> | <span data-ttu-id="0d25d-125">散發平臺</span><span class="sxs-lookup"><span data-stu-id="0d25d-125">Distribution Platform</span></span>                                                       |
|---------|-----------------------------------------------------------------------------|
| <span data-ttu-id="0d25d-126">4.0</span><span class="sxs-lookup"><span data-stu-id="0d25d-126">4.0</span></span>     | <span data-ttu-id="0d25d-127">Windows 95 和 Microsoft Windows NT 4。0</span><span class="sxs-lookup"><span data-stu-id="0d25d-127">Windows 95 and Microsoft Windows NT 4.0</span></span>                                     |
| <span data-ttu-id="0d25d-128">4.71</span><span class="sxs-lookup"><span data-stu-id="0d25d-128">4.71</span></span>    | <span data-ttu-id="0d25d-129">Microsoft Internet Explorer 4.0。</span><span class="sxs-lookup"><span data-stu-id="0d25d-129">Microsoft Internet Explorer 4.0.</span></span> <span data-ttu-id="0d25d-130">請參閱注意 1。</span><span class="sxs-lookup"><span data-stu-id="0d25d-130">See note 1.</span></span>                                |
| <span data-ttu-id="0d25d-131">4.72</span><span class="sxs-lookup"><span data-stu-id="0d25d-131">4.72</span></span>    | <span data-ttu-id="0d25d-132">Internet Explorer 4.01 和 Windows 98。</span><span class="sxs-lookup"><span data-stu-id="0d25d-132">Internet Explorer 4.01 and Windows 98.</span></span> <span data-ttu-id="0d25d-133">請參閱注意 1。</span><span class="sxs-lookup"><span data-stu-id="0d25d-133">See note 1.</span></span>                          |
| <span data-ttu-id="0d25d-134">5.0</span><span class="sxs-lookup"><span data-stu-id="0d25d-134">5.0</span></span>     | <span data-ttu-id="0d25d-135">Windows 2000 和 Windows Millennium Edition (Windows Me) 。</span><span class="sxs-lookup"><span data-stu-id="0d25d-135">Windows 2000 and Windows Millennium Edition (Windows Me).</span></span> <span data-ttu-id="0d25d-136">請參閱附注2。</span><span class="sxs-lookup"><span data-stu-id="0d25d-136">See note 2.</span></span>       |
| <span data-ttu-id="0d25d-137">6.0</span><span class="sxs-lookup"><span data-stu-id="0d25d-137">6.0</span></span>     | <span data-ttu-id="0d25d-138">Windows XP</span><span class="sxs-lookup"><span data-stu-id="0d25d-138">Windows XP</span></span>                                                                  |
| <span data-ttu-id="0d25d-139">6.0.1</span><span class="sxs-lookup"><span data-stu-id="0d25d-139">6.0.1</span></span>   | <span data-ttu-id="0d25d-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0d25d-140">Windows Vista</span></span>                                                               |
| <span data-ttu-id="0d25d-141">6.1</span><span class="sxs-lookup"><span data-stu-id="0d25d-141">6.1</span></span>     | <span data-ttu-id="0d25d-142">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0d25d-142">Windows 7</span></span>                                                                   |

#### <a name="shlwapidll"></a><span data-ttu-id="0d25d-143">Shlwapi.dll</span><span class="sxs-lookup"><span data-stu-id="0d25d-143">Shlwapi.dll</span></span>

| <span data-ttu-id="0d25d-144">版本</span><span class="sxs-lookup"><span data-stu-id="0d25d-144">Version</span></span> | <span data-ttu-id="0d25d-145">散發平臺</span><span class="sxs-lookup"><span data-stu-id="0d25d-145">Distribution Platform</span></span>                                                       |
|---------|-----------------------------------------------------------------------------|
| <span data-ttu-id="0d25d-146">4.0</span><span class="sxs-lookup"><span data-stu-id="0d25d-146">4.0</span></span>     | <span data-ttu-id="0d25d-147">Windows 95 和 Microsoft Windows NT 4。0</span><span class="sxs-lookup"><span data-stu-id="0d25d-147">Windows 95 and Microsoft Windows NT 4.0</span></span>                                     |
| <span data-ttu-id="0d25d-148">4.71</span><span class="sxs-lookup"><span data-stu-id="0d25d-148">4.71</span></span>    | <span data-ttu-id="0d25d-149">Internet Explorer 4.0。</span><span class="sxs-lookup"><span data-stu-id="0d25d-149">Internet Explorer 4.0.</span></span> <span data-ttu-id="0d25d-150">請參閱注意 1。</span><span class="sxs-lookup"><span data-stu-id="0d25d-150">See note 1.</span></span>                                          |
| <span data-ttu-id="0d25d-151">4.72</span><span class="sxs-lookup"><span data-stu-id="0d25d-151">4.72</span></span>    | <span data-ttu-id="0d25d-152">Internet Explorer 4.01 和 Windows 98。</span><span class="sxs-lookup"><span data-stu-id="0d25d-152">Internet Explorer 4.01 and Windows 98.</span></span> <span data-ttu-id="0d25d-153">請參閱注意 1。</span><span class="sxs-lookup"><span data-stu-id="0d25d-153">See note 1.</span></span>                          |
| <span data-ttu-id="0d25d-154">4.7</span><span class="sxs-lookup"><span data-stu-id="0d25d-154">4.7</span></span>     | <span data-ttu-id="0d25d-155">Internet Explorer 3。x</span><span class="sxs-lookup"><span data-stu-id="0d25d-155">Internet Explorer 3.x</span></span>                                                       |
| <span data-ttu-id="0d25d-156">5.0</span><span class="sxs-lookup"><span data-stu-id="0d25d-156">5.0</span></span>     | <span data-ttu-id="0d25d-157">Microsoft Internet Explorer 5 與 Windows 98 SE。</span><span class="sxs-lookup"><span data-stu-id="0d25d-157">Microsoft Internet Explorer 5 and Windows 98 SE.</span></span> <span data-ttu-id="0d25d-158">請參閱附注2。</span><span class="sxs-lookup"><span data-stu-id="0d25d-158">See note 2.</span></span>                |
| <span data-ttu-id="0d25d-159">5.5</span><span class="sxs-lookup"><span data-stu-id="0d25d-159">5.5</span></span>     | <span data-ttu-id="0d25d-160">Microsoft Internet Explorer 5.5 和 Windows Millennium Edition (Windows Me) </span><span class="sxs-lookup"><span data-stu-id="0d25d-160">Microsoft Internet Explorer 5.5 and Windows Millennium Edition (Windows Me)</span></span> |
| <span data-ttu-id="0d25d-161">6.0</span><span class="sxs-lookup"><span data-stu-id="0d25d-161">6.0</span></span>     | <span data-ttu-id="0d25d-162">Windows XP 和 Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0d25d-162">Windows XP and Windows Vista</span></span>                                                |



<span data-ttu-id="0d25d-163">**附注1：** 所有具有 Internet Explorer 4.0 或4.01 的系統都會分別) Shlwapi.dll (4.71 或4.72 的相關版本。</span><span class="sxs-lookup"><span data-stu-id="0d25d-163">**Note 1:** All systems with Internet Explorer 4.0 or 4.01 had the associated version of Shlwapi.dll (4.71 or 4.72, respectively).</span></span> <span data-ttu-id="0d25d-164">不過，對於 Windows 98 之前的系統，Internet Explorer 4.0 和4.01 可以安裝，或不使用所謂的 *整合式 Shell*。</span><span class="sxs-lookup"><span data-stu-id="0d25d-164">However, for systems prior to Windows 98, Internet Explorer 4.0 and 4.01 can be installed with or without what was known as the *integrated Shell*.</span></span> <span data-ttu-id="0d25d-165">如果 Internet Explorer 是與整合式 Shell 一起安裝，則也會安裝 Shell32.dll (4.71 或 4.72) 相關聯的版本。</span><span class="sxs-lookup"><span data-stu-id="0d25d-165">If Internet Explorer was installed with the integrated Shell, the associated version of Shell32.dll (4.71 or 4.72) was also installed.</span></span> <span data-ttu-id="0d25d-166">如果 Internet Explorer 是在沒有整合式 Shell 的情況下安裝，Shell32.dll 會保持為4.0 版。</span><span class="sxs-lookup"><span data-stu-id="0d25d-166">If Internet Explorer was installed without the integrated Shell, Shell32.dll remained as version 4.0.</span></span> <span data-ttu-id="0d25d-167">換句話說，系統上的 Shlwapi.dll 版本4.71 或4.72 不保證 Shell32.dll 具有相同的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="0d25d-167">In other words, the presence of version 4.71 or 4.72 of Shlwapi.dll on a system does not guarantee that Shell32.dll has the same version number.</span></span> <span data-ttu-id="0d25d-168">所有 Windows 98 系統都有4.72 版的 Shell32.dll。</span><span class="sxs-lookup"><span data-stu-id="0d25d-168">All Windows 98 systems have version 4.72 of Shell32.dll.</span></span>

<span data-ttu-id="0d25d-169">**附注2：** Shlwapi.dll 的5.0 版是以 Internet Explorer 5 散發，並在安裝 Internet Explorer 5 的所有系統上找到，但 Windows 2000 除外。</span><span class="sxs-lookup"><span data-stu-id="0d25d-169">**Note 2:** Version 5.0 of Shlwapi.dll was distributed with Internet Explorer 5 and was found on all systems on which Internet Explorer 5 was installed, with the exception of Windows 2000.</span></span> <span data-ttu-id="0d25d-170">5.0 版的 Shell32.dll 是以 Windows 2000 和 Windows Millennium Edition 原生散發， (Windows Me) ，以及 Shlwapi.dll 版本5.0。</span><span class="sxs-lookup"><span data-stu-id="0d25d-170">Version 5.0 of Shell32.dll was distributed natively with Windows 2000 and Windows Millennium Edition (Windows Me), together with version 5.0 of Shlwapi.dll.</span></span>

## <a name="using-dllgetversion-to-determine-the-version-number"></a><span data-ttu-id="0d25d-171">使用 DllGetVersion 來判斷版本號碼</span><span class="sxs-lookup"><span data-stu-id="0d25d-171">Using DllGetVersion to Determine the Version Number</span></span>

<span data-ttu-id="0d25d-172">從版本4.71 開始，Shell Dll 和其他版本會開始匯出 [**DllGetVersion**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc)。</span><span class="sxs-lookup"><span data-stu-id="0d25d-172">Starting with version 4.71, the Shell DLLs, among others, began exporting [**DllGetVersion**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc).</span></span> <span data-ttu-id="0d25d-173">應用程式可以呼叫這個函式來判斷系統上有哪些 DLL 版本。</span><span class="sxs-lookup"><span data-stu-id="0d25d-173">This function can be called by an application to determine which DLL version is present on the system.</span></span>

> [!Note]  
> <span data-ttu-id="0d25d-174">Dll 不一定會匯出 [**DllGetVersion**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc)。</span><span class="sxs-lookup"><span data-stu-id="0d25d-174">DLLs do not necessarily export [**DllGetVersion**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc).</span></span> <span data-ttu-id="0d25d-175">請一律先測試它，再嘗試使用它。</span><span class="sxs-lookup"><span data-stu-id="0d25d-175">Always test for it before attempting to use it.</span></span>

<span data-ttu-id="0d25d-176">針對 windows 2000 之前的 Windows 版本， [**DllGetVersion**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc) 會傳回 [**DLLVERSIONINFO**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo) 結構，其中包含主要和次要版本號碼、組建編號和平臺識別碼。</span><span class="sxs-lookup"><span data-stu-id="0d25d-176">For Windows versions earlier than Windows 2000, [**DllGetVersion**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc) returns a [**DLLVERSIONINFO**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo) structure that contains the major and minor version numbers, the build number, and a platform ID.</span></span> <span data-ttu-id="0d25d-177">如果是 Windows 2000 和更新版本的系統， **DllGetVersion** 可能會傳回 [**DLLVERSIONINFO2**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo2) 結構。</span><span class="sxs-lookup"><span data-stu-id="0d25d-177">For Windows 2000 and later systems, **DllGetVersion** might instead return a [**DLLVERSIONINFO2**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo2) structure.</span></span> <span data-ttu-id="0d25d-178">除了透過 **DLLVERSIONINFO** 提供的資訊之外， **DLLVERSIONINFO2** 也會提供可識別最新安裝 service pack 的修正程式編號，以提供更健全的方式來比較版本號碼。</span><span class="sxs-lookup"><span data-stu-id="0d25d-178">In addition to the information provided through **DLLVERSIONINFO**, **DLLVERSIONINFO2** also provides the hotfix number that identifies the latest installed service pack, which provides a more robust way to compare version numbers.</span></span> <span data-ttu-id="0d25d-179">由於 **DLLVERSIONINFO2** 的第一個成員是 **DLLVERSIONINFO** 結構，因此之後的結構會回溯相容。</span><span class="sxs-lookup"><span data-stu-id="0d25d-179">Because the first member of **DLLVERSIONINFO2** is a **DLLVERSIONINFO** structure, the later structure is backward-compatible.</span></span>

### <a name="using-dllgetversion"></a><span data-ttu-id="0d25d-180">使用 DllGetVersion</span><span class="sxs-lookup"><span data-stu-id="0d25d-180">Using DllGetVersion</span></span>

<span data-ttu-id="0d25d-181">下列範例函數 `GetVersion` 會載入指定的 DLL，並嘗試呼叫其 [**DllGetVersion**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc) 函式。</span><span class="sxs-lookup"><span data-stu-id="0d25d-181">The following sample function `GetVersion` loads a specified DLL and attempts to call its [**DllGetVersion**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc) function.</span></span> <span data-ttu-id="0d25d-182">如果成功，它會使用宏將 [**DLLVERSIONINFO**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo) 結構中的主要和次要版本號碼，封裝至傳回給呼叫應用程式的 **DWORD** 。</span><span class="sxs-lookup"><span data-stu-id="0d25d-182">If successful, it uses a macro to pack the major and minor version numbers from the [**DLLVERSIONINFO**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo) structure into a **DWORD** that is returned to the calling application.</span></span> <span data-ttu-id="0d25d-183">如果 DLL 未匯出 **DllGetVersion**，函數會傳回零。</span><span class="sxs-lookup"><span data-stu-id="0d25d-183">If the DLL does not export **DllGetVersion**, the function returns zero.</span></span> <span data-ttu-id="0d25d-184">在 Windows 2000 和更新版本的系統中，您可以修改函式來處理 **DllGetVersion** 傳回 [**DLLVERSIONINFO2**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo2) 結構的可能性。</span><span class="sxs-lookup"><span data-stu-id="0d25d-184">With Windows 2000 and later systems, you can modify the function to handle the possibility that **DllGetVersion** returns a [**DLLVERSIONINFO2**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo2) structure.</span></span> <span data-ttu-id="0d25d-185">如果是的話，請使用該 **DLLVERSIONINFO2** 結構的 **ullVersion** 成員中的資訊來比較版本、組建編號和 service pack 版本。</span><span class="sxs-lookup"><span data-stu-id="0d25d-185">If so, use the information in that **DLLVERSIONINFO2** structure's **ullVersion** member to compare versions, build numbers, and service pack releases.</span></span> <span data-ttu-id="0d25d-186">[**MAKEDLLVERULL**](/windows/desktop/api/Shlwapi/nf-shlwapi-makedllverull)宏可簡化將這些值與 **ullVersion** 中的值進行比較的工作。</span><span class="sxs-lookup"><span data-stu-id="0d25d-186">The [**MAKEDLLVERULL**](/windows/desktop/api/Shlwapi/nf-shlwapi-makedllverull) macro simplifies the task of comparing these values to those in **ullVersion**.</span></span>

> [!Note]  
> <span data-ttu-id="0d25d-187">不當使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 可能會造成安全性風險。</span><span class="sxs-lookup"><span data-stu-id="0d25d-187">Using [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can pose security risks.</span></span> <span data-ttu-id="0d25d-188">請參閱 **LoadLibrary** 檔，以取得如何使用不同版本的 Windows 正確載入 dll 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="0d25d-188">Refer to the **LoadLibrary** documentation for information on how to correctly load DLLs with different versions of Windows.</span></span>


```C++
#include "stdafx.h"
#include "windows.h"
#include "windef.h"
#include "winbase.h"
#include "shlwapi.h"

#define PACKVERSION(major,minor) MAKELONG(minor,major)

DWORD GetVersion(LPCTSTR lpszDllName)
{
    HINSTANCE hinstDll;
    DWORD dwVersion = 0;

    /* For security purposes, LoadLibrary should be provided with a fully qualified 
       path to the DLL. The lpszDllName variable should be tested to ensure that it 
       is a fully qualified path before it is used. */
    hinstDll = LoadLibrary(lpszDllName);
    
    if(hinstDll)
    {
        DLLGETVERSIONPROC pDllGetVersion;
        pDllGetVersion = (DLLGETVERSIONPROC)GetProcAddress(hinstDll, "DllGetVersion");

        /* Because some DLLs might not implement this function, you must test for 
           it explicitly. Depending on the particular DLL, the lack of a DllGetVersion 
           function can be a useful indicator of the version. */

        if(pDllGetVersion)
        {
            DLLVERSIONINFO dvi;
            HRESULT hr;

            ZeroMemory(&dvi, sizeof(dvi));
            dvi.info1.cbSize = sizeof(dvi);

            hr = (*pDllGetVersion)(&dvi);

            if(SUCCEEDED(hr))
            {
               dwVersion = PACKVERSION(dvi.info1.dwMajorVersion, dvi.info1.dwMinorVersion);
            }
        }
        FreeLibrary(hinstDll);
    }
    return dwVersion;
}
```


<span data-ttu-id="0d25d-189">下列程式碼範例說明如何使用 `GetVersion` 來測試 Shell32.dll 是否為6.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="0d25d-189">The following code example illustrates how you can use `GetVersion` to test whether Shell32.dll is version 6.0 or later.</span></span>


```C++
LPCTSTR lpszDllName = L"C:\\Windows\\System32\\Shell32.dll";
DWORD dwVer = GetVersion(lpszDllName);
DWORD dwTarget = PACKVERSION(6,0);

if(dwVer >= dwTarget)
{
    // This version of Shell32.dll is version 6.0 or later.
}
else
{
    // Proceed knowing that version 6.0 or later additions are not available.
    // Use an alternate approach for older the DLL version.
}
```


## <a name="project-versions"></a><span data-ttu-id="0d25d-190">專案版本</span><span class="sxs-lookup"><span data-stu-id="0d25d-190">Project Versions</span></span>

<span data-ttu-id="0d25d-191">為了確保您的應用程式與 .dll 檔案的不同目標版本相容，版本宏會出現在標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="0d25d-191">To ensure that your application is compatible with different targeted versions of a .dll file, version macros are present in the header files.</span></span> <span data-ttu-id="0d25d-192">這些宏可用來定義、排除或重新定義不同版本 DLL 的特定定義。</span><span class="sxs-lookup"><span data-stu-id="0d25d-192">These macros are used to define, exclude, or redefine certain definitions for different versions of the DLL.</span></span> <span data-ttu-id="0d25d-193">如需這些宏的深入說明，請參閱 [使用 Windows 標頭](../winprog/using-the-windows-headers.md) 。</span><span class="sxs-lookup"><span data-stu-id="0d25d-193">See [Using the Windows Headers](../winprog/using-the-windows-headers.md) for an in-depth description of these macros.</span></span>

<span data-ttu-id="0d25d-194">例如，宏名稱 **\_ WIN32 \_ IE** 通常會在較舊的標頭中找到。</span><span class="sxs-lookup"><span data-stu-id="0d25d-194">For example, the macro name **\_WIN32\_IE** is commonly found in older headers.</span></span> <span data-ttu-id="0d25d-195">您必須負責將巨集定義為十六進位數位。</span><span class="sxs-lookup"><span data-stu-id="0d25d-195">You are responsible for defining the macro as a hexadecimal number.</span></span> <span data-ttu-id="0d25d-196">此版本號碼會定義使用 DLL 的應用程式目標版本。</span><span class="sxs-lookup"><span data-stu-id="0d25d-196">This version number defines the target version of the application that is using the DLL.</span></span> <span data-ttu-id="0d25d-197">下表顯示可用的版本號碼，以及每一個應用程式的效果。</span><span class="sxs-lookup"><span data-stu-id="0d25d-197">The following table shows the available version numbers and the effect each has on your application.</span></span>


| <span data-ttu-id="0d25d-198">版本</span><span class="sxs-lookup"><span data-stu-id="0d25d-198">Version</span></span> | <span data-ttu-id="0d25d-199">描述</span><span class="sxs-lookup"><span data-stu-id="0d25d-199">Description</span></span>                                                                                                                                                                                       |
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d25d-200">0x0200</span><span class="sxs-lookup"><span data-stu-id="0d25d-200">0x0200</span></span>  | <span data-ttu-id="0d25d-201">應用程式與 Shell32.dll 4.00 版和更新版本相容。</span><span class="sxs-lookup"><span data-stu-id="0d25d-201">The application is compatible with Shell32.dll version 4.00 and later.</span></span> <span data-ttu-id="0d25d-202">應用程式無法執行4.00 版之後加入的功能。</span><span class="sxs-lookup"><span data-stu-id="0d25d-202">The application cannot implement features that were added after version 4.00.</span></span>                                              |
| <span data-ttu-id="0d25d-203">0x0300</span><span class="sxs-lookup"><span data-stu-id="0d25d-203">0x0300</span></span>  | <span data-ttu-id="0d25d-204">應用程式與 Shell32.dll 4.70 版和更新版本相容。</span><span class="sxs-lookup"><span data-stu-id="0d25d-204">The application is compatible with Shell32.dll version 4.70 and later.</span></span> <span data-ttu-id="0d25d-205">應用程式無法執行4.70 版之後加入的功能。</span><span class="sxs-lookup"><span data-stu-id="0d25d-205">The application cannot implement features that were added after version 4.70.</span></span>                                              |
| <span data-ttu-id="0d25d-206">0x0400</span><span class="sxs-lookup"><span data-stu-id="0d25d-206">0x0400</span></span>  | <span data-ttu-id="0d25d-207">應用程式與 Shell32.dll 4.71 版和更新版本相容。</span><span class="sxs-lookup"><span data-stu-id="0d25d-207">The application is compatible with Shell32.dll version 4.71 and later.</span></span> <span data-ttu-id="0d25d-208">應用程式無法執行4.71 版之後加入的功能。</span><span class="sxs-lookup"><span data-stu-id="0d25d-208">The application cannot implement features that were added after version 4.71.</span></span>                                              |
| <span data-ttu-id="0d25d-209">0x0401</span><span class="sxs-lookup"><span data-stu-id="0d25d-209">0x0401</span></span>  | <span data-ttu-id="0d25d-210">應用程式與 Shell32.dll 4.72 版和更新版本相容。</span><span class="sxs-lookup"><span data-stu-id="0d25d-210">The application is compatible with Shell32.dll version 4.72 and later.</span></span> <span data-ttu-id="0d25d-211">應用程式無法執行4.72 版之後加入的功能。</span><span class="sxs-lookup"><span data-stu-id="0d25d-211">The application cannot implement features that were added after version 4.72.</span></span>                                              |
| <span data-ttu-id="0d25d-212">0x0500</span><span class="sxs-lookup"><span data-stu-id="0d25d-212">0x0500</span></span>  | <span data-ttu-id="0d25d-213">應用程式與 Shell32.dll 和 Shlwapi.dll 5.0 版和更新版本相容。</span><span class="sxs-lookup"><span data-stu-id="0d25d-213">The application is compatible with Shell32.dll and Shlwapi.dll version 5.0 and later.</span></span> <span data-ttu-id="0d25d-214">應用程式無法執行在5.0 版的 Shell32.dll 和 Shlwapi.dll 之後加入的功能。</span><span class="sxs-lookup"><span data-stu-id="0d25d-214">The application cannot implement features that were added after version 5.0 of Shell32.dll and Shlwapi.dll.</span></span> |
| <span data-ttu-id="0d25d-215">0x0501</span><span class="sxs-lookup"><span data-stu-id="0d25d-215">0x0501</span></span>  | <span data-ttu-id="0d25d-216">應用程式與 Shell32.dll 和 Shlwapi.dll 5.0 版和更新版本相容。</span><span class="sxs-lookup"><span data-stu-id="0d25d-216">The application is compatible with Shell32.dll and Shlwapi.dll version 5.0 and later.</span></span> <span data-ttu-id="0d25d-217">應用程式無法執行在5.0 版的 Shell32.dll 和 Shlwapi.dll 之後加入的功能。</span><span class="sxs-lookup"><span data-stu-id="0d25d-217">The application cannot implement features that were added after version 5.0 of Shell32.dll and Shlwapi.dll.</span></span> |
| <span data-ttu-id="0d25d-218">0x0600</span><span class="sxs-lookup"><span data-stu-id="0d25d-218">0x0600</span></span>  | <span data-ttu-id="0d25d-219">應用程式與 Shell32.dll 和 Shlwapi.dll 6.0 版和更新版本相容。</span><span class="sxs-lookup"><span data-stu-id="0d25d-219">The application is compatible with Shell32.dll and Shlwapi.dll version 6.0 and later.</span></span> <span data-ttu-id="0d25d-220">應用程式無法執行在6.0 版的 Shell32.dll 和 Shlwapi.dll 之後加入的功能。</span><span class="sxs-lookup"><span data-stu-id="0d25d-220">The application cannot implement features that were added after version 6.0 of Shell32.dll and Shlwapi.dll.</span></span> |


<span data-ttu-id="0d25d-221">如果您未在專案中定義 **\_ WIN32 \_ IE** 宏，則會自動將其定義為0x0500。</span><span class="sxs-lookup"><span data-stu-id="0d25d-221">If you do not define the **\_WIN32\_IE** macro in your project, it is automatically defined as 0x0500.</span></span> <span data-ttu-id="0d25d-222">若要定義不同的值，您可以將下列程式檔加入至 make 檔案中的編譯器指示詞。以所需的0x0400 版本號碼取代。</span><span class="sxs-lookup"><span data-stu-id="0d25d-222">To define a different value, you can add the following to the compiler directives in your make file; substitute the desired version number for 0x0400.</span></span>

```
/D _WIN32_IE=0x0400
```

<span data-ttu-id="0d25d-223">另一種方法是在包含 Shell 標頭檔之前，在原始程式碼中加入類似下列的程式程式碼。</span><span class="sxs-lookup"><span data-stu-id="0d25d-223">Another method is to add a line similar to the following in your source code before you include the Shell header files.</span></span> <span data-ttu-id="0d25d-224">以所需的0x0400 版本號碼取代。</span><span class="sxs-lookup"><span data-stu-id="0d25d-224">Substitute the desired version number for 0x0400.</span></span>

```
#define _WIN32_IE 0x0400
#include <commctrl.h>
```

---
description: 下列清單是您在使用檔案關聯時應該使用的建議最佳作法。
title: 檔案關聯的最佳作法
ms.topic: article
ms.date: 05/31/2018
ms.assetid: d4d0edf9-3475-4164-b0fa-15006e05e242
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: f49c1df6d145c32b8fcbdf70462b30f14f51b3d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511194"
---
# <a name="best-practices-for-file-associations"></a><span data-ttu-id="fc34a-103">檔案關聯的最佳作法</span><span class="sxs-lookup"><span data-stu-id="fc34a-103">Best Practices for File Associations</span></span>

<span data-ttu-id="fc34a-104">下列清單是您在使用檔案關聯時應該使用的建議最佳作法。</span><span class="sxs-lookup"><span data-stu-id="fc34a-104">The following list are recommended best practices you should use when working with file associations.</span></span>

-   [<span data-ttu-id="fc34a-105">不要從登錄複製檔案關聯</span><span class="sxs-lookup"><span data-stu-id="fc34a-105">Do Not Copy File Associations from the Registry</span></span>](#do-not-copy-file-associations-from-the-registry)
-   [<span data-ttu-id="fc34a-106">盡可能避免 Hard-Coding 的路徑</span><span class="sxs-lookup"><span data-stu-id="fc34a-106">Avoid Hard-Coding Paths into the Registry Where Possible</span></span>](#avoid-hard-coding-paths-into-the-registry-where-possible)
-   [<span data-ttu-id="fc34a-107">一律以引號括住展開字串</span><span class="sxs-lookup"><span data-stu-id="fc34a-107">Always Wrap Expanding Strings in Quotation Marks</span></span>](#always-wrap-expanding-strings-in-quotation-marks)
-   [<span data-ttu-id="fc34a-108">請勿將自動播放/自動播放與檔案關聯混淆</span><span class="sxs-lookup"><span data-stu-id="fc34a-108">Do Not Confuse Autoplay/Autorun with File Associations</span></span>](#do-not-confuse-autoplayautorun-with-file-associations)
-   [<span data-ttu-id="fc34a-109">請勿混淆 Internet Explorer MIME 資料庫與檔案關聯</span><span class="sxs-lookup"><span data-stu-id="fc34a-109">Do Not Confuse the Internet Explorer MIME Database with File Associations</span></span>](#do-not-confuse-the-internet-explorer-mime-database-with-file-associations)
-   [<span data-ttu-id="fc34a-110">使用正確格式和建立版本的 Progid</span><span class="sxs-lookup"><span data-stu-id="fc34a-110">Use Properly Formed and Versioned ProgIDs</span></span>](#use-properly-formed-and-versioned-progids)
-   [<span data-ttu-id="fc34a-111">請勿使用簡短的副檔名</span><span class="sxs-lookup"><span data-stu-id="fc34a-111">Do Not Use Short File Name Extensions</span></span>](#do-not-use-short-file-name-extensions)
-   [<span data-ttu-id="fc34a-112">在 IANA MIME 資料庫中註冊新的檔案類型</span><span class="sxs-lookup"><span data-stu-id="fc34a-112">Register New File Types in the IANA MIME Database</span></span>](#register-new-file-types-in-the-iana-mime-database)
-   [<span data-ttu-id="fc34a-113">使用 Windows Web 服務註冊檔案關聯</span><span class="sxs-lookup"><span data-stu-id="fc34a-113">Sign Up with the Windows Web Service for File Associations</span></span>](#sign-up-with-the-windows-web-service-for-file-associations)
-   [<span data-ttu-id="fc34a-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="fc34a-114">Related topics</span></span>](#related-topics)

## <a name="do-not-copy-file-associations-from-the-registry"></a><span data-ttu-id="fc34a-115">不要從登錄複製檔案關聯</span><span class="sxs-lookup"><span data-stu-id="fc34a-115">Do Not Copy File Associations from the Registry</span></span>

<span data-ttu-id="fc34a-116">建議您不要從登錄複製現有的檔案關聯。</span><span class="sxs-lookup"><span data-stu-id="fc34a-116">We recommended that you do not copy existing file associations from the registry.</span></span> <span data-ttu-id="fc34a-117">這通常會導致傳播格式不正確的檔案關聯。</span><span class="sxs-lookup"><span data-stu-id="fc34a-117">This often leads to the propagation of poorly formed file associations.</span></span> <span data-ttu-id="fc34a-118">相反地，您應該遵循檔案 [關聯範例案例](fa-sample-scenarios.md)中所述的步驟。</span><span class="sxs-lookup"><span data-stu-id="fc34a-118">Instead, you should follow the steps outlined in [File Association Sample Scenario](fa-sample-scenarios.md).</span></span>

## <a name="avoid-hard-coding-paths-into-the-registry-where-possible"></a><span data-ttu-id="fc34a-119">盡可能避免 Hard-Coding 的路徑</span><span class="sxs-lookup"><span data-stu-id="fc34a-119">Avoid Hard-Coding Paths into the Registry Where Possible</span></span>

<span data-ttu-id="fc34a-120">如同程式碼的程式碼路徑可能會造成問題，登錄的硬式編碼路徑也會導致問題。</span><span class="sxs-lookup"><span data-stu-id="fc34a-120">Just as hard-coding paths into programs can cause problems, hard-coding paths into the registry can also lead to problems.</span></span> <span data-ttu-id="fc34a-121">相反地，您應該使用登錄展開字串 (REG \_ EXPAND \_ SZ) 在適用的情況下提供獨立路徑。</span><span class="sxs-lookup"><span data-stu-id="fc34a-121">Instead, you should use registry expansion strings (REG\_EXPAND\_SZ) to provide path independence where applicable.</span></span> <span data-ttu-id="fc34a-122">例如，不要使用這個方法：</span><span class="sxs-lookup"><span data-stu-id="fc34a-122">For example, instead of using this method:</span></span>

```
HKEY_CLASSES_ROOT
   MyVendor.MyProgram.1
      DefaultIcon
         (Default) = C:\WINNT\hta.exe,1
```

<span data-ttu-id="fc34a-123">您應使用此方法：</span><span class="sxs-lookup"><span data-stu-id="fc34a-123">You should use this method:</span></span>

```
HKEY_CLASSES_ROOT
   MyVendor.MyProgram.1
      DefaultIcon
         (Default) = "%SYSTEMROOT%\hta.exe,1"
```

## <a name="always-wrap-expanding-strings-in-quotation-marks"></a><span data-ttu-id="fc34a-124">一律以引號括住展開字串</span><span class="sxs-lookup"><span data-stu-id="fc34a-124">Always Wrap Expanding Strings in Quotation Marks</span></span>

<span data-ttu-id="fc34a-125">展開字串時可以包含空格。</span><span class="sxs-lookup"><span data-stu-id="fc34a-125">Expanding strings can contain spaces when they expand.</span></span> <span data-ttu-id="fc34a-126">由於空格通常會被視為引數分隔符號，因此在某些情況下會造成問題。</span><span class="sxs-lookup"><span data-stu-id="fc34a-126">Because spaces are often interpreted as argument delimiters, they cause problems under certain circumstances.</span></span> <span data-ttu-id="fc34a-127">例如，用來叫用 Myprogram.exe 的命令可以儲存在登錄中，如下所示：</span><span class="sxs-lookup"><span data-stu-id="fc34a-127">For example, a command to invoke MyProgram can be stored in the registry as:</span></span>

`%SYSTEMROOT%\MyProgram %1 %2`

<span data-ttu-id="fc34a-128">Myprogram.exe 預期 %1 是檔案名的完整路徑，而 %2 是表示某些動作的參數。</span><span class="sxs-lookup"><span data-stu-id="fc34a-128">MyProgram expects that %1 is the full path to a file name, and %2 is a switch to indicate some action.</span></span> <span data-ttu-id="fc34a-129">如果使用引數 **c： \\ Program Files 執行此命令 \\ 我的檔 \\document.txt** 和 **/print**，並假設有 C： WINNT 的 SYSTEMROOT \\ ，它會展開為：</span><span class="sxs-lookup"><span data-stu-id="fc34a-129">If this command is executed with arguments **C:\\Program Files\\My Documents\\document.txt** and **/print**, and assuming a SYSTEMROOT of C:\\WINNT, it expands to:</span></span>

`C:\WINNT\MyProgram C:\Program Files\My Documents\document.txt /print`

<span data-ttu-id="fc34a-130">在此情況下，Myprogram.exe 會將第一個引數解釋為 C： \\ Program，而第二個引數是檔案 \\ My，這不是預期的行為。</span><span class="sxs-lookup"><span data-stu-id="fc34a-130">In this case, MyProgram interprets that the first argument is C:\\Program, and the second argument is Files\\My, which is not the intended behavior.</span></span> <span data-ttu-id="fc34a-131">如果展開的字串是以引號括住，就會正確地解讀引數，如下所示：</span><span class="sxs-lookup"><span data-stu-id="fc34a-131">The arguments are interpreted correctly, however, regardless of whether they contain spaces, if the expanding strings are wrapped in quotation marks as follows:</span></span>

`"%SYSTEMROOT%\MyProgram" "%1" "%2"`

## <a name="do-not-confuse-autoplayautorun-with-file-associations"></a><span data-ttu-id="fc34a-132">請勿將自動播放/自動播放與檔案關聯混淆</span><span class="sxs-lookup"><span data-stu-id="fc34a-132">Do Not Confuse Autoplay/Autorun with File Associations</span></span>

<span data-ttu-id="fc34a-133">檔案關聯在某些方面與自動播放/自動播放類似。</span><span class="sxs-lookup"><span data-stu-id="fc34a-133">File Associations are similar to Autoplay/Autorun in some ways.</span></span> <span data-ttu-id="fc34a-134">不過，自動播放/自動播放會提供與檔案關聯所提供不同的不同設備。</span><span class="sxs-lookup"><span data-stu-id="fc34a-134">However, Autoplay/Autorun offers separate and distinct facilities from those provided by file associations.</span></span> <span data-ttu-id="fc34a-135">如需詳細資訊，請參閱 [建立啟用自動安裝的 Cd-rom 應用程式](autoplay.md)。</span><span class="sxs-lookup"><span data-stu-id="fc34a-135">For more information see [Creating an AutoRun-enabled CD-ROM Application](autoplay.md).</span></span>

## <a name="do-not-confuse-the-internet-explorer-mime-database-with-file-associations"></a><span data-ttu-id="fc34a-136">請勿混淆 Internet Explorer MIME 資料庫與檔案關聯</span><span class="sxs-lookup"><span data-stu-id="fc34a-136">Do Not Confuse the Internet Explorer MIME Database with File Associations</span></span>

<span data-ttu-id="fc34a-137">檔案關聯類似于 Windows Internet Explorer MIME 資料庫，在該檔案類型中可以 (，而且) 包含 MIME 類型定義。</span><span class="sxs-lookup"><span data-stu-id="fc34a-137">File Associations are similar to the Windows Internet Explorer MIME database, in that file types can (and should) include a MIME type definition.</span></span> <span data-ttu-id="fc34a-138">不過，Internet Explorer MIME 資料庫是分開的，與檔案關聯不同。</span><span class="sxs-lookup"><span data-stu-id="fc34a-138">However, the Internet Explorer MIME database is separate and distinct from file associations.</span></span>

## <a name="use-properly-formed-and-versioned-progids"></a><span data-ttu-id="fc34a-139">使用正確格式和建立版本的 Progid</span><span class="sxs-lookup"><span data-stu-id="fc34a-139">Use Properly Formed and Versioned ProgIDs</span></span>

<span data-ttu-id="fc34a-140">一律使用已建立版本的 [progid](fa-progids.md)，即使只有一個版本的 ProgID。</span><span class="sxs-lookup"><span data-stu-id="fc34a-140">Always use [versioned ProgIDs](fa-progids.md), even if there is only one version of the ProgID.</span></span> <span data-ttu-id="fc34a-141">已建立版本的 Progid 有助於避免 ProgID 衝突和覆寫。</span><span class="sxs-lookup"><span data-stu-id="fc34a-141">Versioned ProgIDs help to avoid ProgID conflicts and overwrites.</span></span> <span data-ttu-id="fc34a-142">它們也可讓不同版本的應用程式並存。</span><span class="sxs-lookup"><span data-stu-id="fc34a-142">They also enable different versions of an application to co-exist.</span></span>

## <a name="do-not-use-short-file-name-extensions"></a><span data-ttu-id="fc34a-143">請勿使用簡短的副檔名</span><span class="sxs-lookup"><span data-stu-id="fc34a-143">Do Not Use Short File Name Extensions</span></span>

<span data-ttu-id="fc34a-144">完整的副檔名提供下列優點：</span><span class="sxs-lookup"><span data-stu-id="fc34a-144">Long file name extensions offer the following advantages:</span></span>

-   <span data-ttu-id="fc34a-145">簡短延伸的有限長度使其容易發生 *延伸衝突。*</span><span class="sxs-lookup"><span data-stu-id="fc34a-145">The limited length of short extensions make them prone to *extension collisions.*</span></span> <span data-ttu-id="fc34a-146">使用相同的延伸模組來分類多個檔案類型時，會發生延伸衝突。</span><span class="sxs-lookup"><span data-stu-id="fc34a-146">An extension collision occurs when the same extension is used to classify multiple file types.</span></span> <span data-ttu-id="fc34a-147">使用 long 擴充功能可大幅降低衝突的機率。</span><span class="sxs-lookup"><span data-stu-id="fc34a-147">Using long extensions significantly decreases the chances of a collision.</span></span>
-   <span data-ttu-id="fc34a-148">簡短檔案名通常有點難懂。</span><span class="sxs-lookup"><span data-stu-id="fc34a-148">Short file names tend to be somewhat cryptic.</span></span> <span data-ttu-id="fc34a-149">長延伸模組較有意義，因為其他資訊可以內嵌在延伸模組中。</span><span class="sxs-lookup"><span data-stu-id="fc34a-149">Long extensions tend to be more meaningful because additional information can be embedded in the extension.</span></span>

<span data-ttu-id="fc34a-150">如需詳細資訊，請參閱 [檔案名延伸](fa-file-extensions.md)。</span><span class="sxs-lookup"><span data-stu-id="fc34a-150">For more information, see [file name extensions](fa-file-extensions.md).</span></span>

## <a name="register-new-file-types-in-the-iana-mime-database"></a><span data-ttu-id="fc34a-151">在 IANA MIME 資料庫中註冊新的檔案類型</span><span class="sxs-lookup"><span data-stu-id="fc34a-151">Register New File Types in the IANA MIME Database</span></span>

<span data-ttu-id="fc34a-152"> (IANA 的網際網路指派號碼授權單位) 保留已註冊 MIME 類型的公用資料庫。</span><span class="sxs-lookup"><span data-stu-id="fc34a-152">The Internet Assigned Numbers Authority (IANA) keeps a public database of registered MIME types.</span></span> <span data-ttu-id="fc34a-153">在定義新的公用檔案類型時，建議您也為檔案類型定義 MIME 類型，並向 IANA 註冊此類型。</span><span class="sxs-lookup"><span data-stu-id="fc34a-153">When defining a new public file type, we recommended that you also define a MIME type for the file type and register this type with the IANA.</span></span> <span data-ttu-id="fc34a-154">註冊不會產生任何費用。</span><span class="sxs-lookup"><span data-stu-id="fc34a-154">There is no cost for registration.</span></span>

## <a name="sign-up-with-the-windows-web-service-for-file-associations"></a><span data-ttu-id="fc34a-155">使用 Windows Web 服務註冊檔案關聯</span><span class="sxs-lookup"><span data-stu-id="fc34a-155">Sign Up with the Windows Web Service for File Associations</span></span>

<span data-ttu-id="fc34a-156">應用程式開發人員可以註冊 Windows Web 服務，讓使用者用來尋找可在特定檔案類型上操作的應用程式。</span><span class="sxs-lookup"><span data-stu-id="fc34a-156">Application developers can sign up with the Windows Web Service that users use to find applications that can operate on specific file types.</span></span> <span data-ttu-id="fc34a-157">使用 web 服務進行註冊的程式，在 [Windows 檔案關聯系統的內建程式](https://support.microsoft.com/kb/929149)中有詳細的說明。</span><span class="sxs-lookup"><span data-stu-id="fc34a-157">The process for signing up with the web service is detailed in [Windows File Association System on-boarding process](https://support.microsoft.com/kb/929149).</span></span>

## <a name="related-topics"></a><span data-ttu-id="fc34a-158">相關主題</span><span class="sxs-lookup"><span data-stu-id="fc34a-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc34a-159">檔案關聯範例案例</span><span class="sxs-lookup"><span data-stu-id="fc34a-159">File Association Sample Scenario</span></span>](fa-sample-scenarios.md)
</dt> <dt>

[<span data-ttu-id="fc34a-160">在 Windows Vista 和更新版本中管理預設應用程式的指導方針</span><span class="sxs-lookup"><span data-stu-id="fc34a-160">Guidelines for Managing Default Applications in Windows Vista and Later</span></span>](vista-managing-defaults.md)
</dt> <dt>

[<span data-ttu-id="fc34a-161">預設程式</span><span class="sxs-lookup"><span data-stu-id="fc34a-161">Default Programs</span></span>](default-programs.md)
</dt> <dt>

[<span data-ttu-id="fc34a-162"> (SPAD) 設定程式存取和電腦預設值 </span><span class="sxs-lookup"><span data-stu-id="fc34a-162">Set Program Access and Computer Defaults (SPAD)</span></span>](cpl-setprogramaccess.md)
</dt> </dl>

 

 




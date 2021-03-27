---
description: 使用預設程式來設定預設的使用者體驗。
ms.assetid: 78cd05a4-df33-42b5-91b9-826ebce04a1d
title: 預設程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f8cd741794189e47888f4daa1d4585b2d8942cf
ms.sourcegitcommit: 1a97e0e0f92d4dcc2fb68738b910ba3910508df3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/19/2021
ms.locfileid: "103853176"
---
# <a name="default-programs"></a><span data-ttu-id="5c483-103">預設程式</span><span class="sxs-lookup"><span data-stu-id="5c483-103">Default Programs</span></span>

<span data-ttu-id="5c483-104">使用 **預設程式** 來設定預設的使用者體驗。</span><span class="sxs-lookup"><span data-stu-id="5c483-104">Use **Default Programs** to set the default user experience.</span></span> <span data-ttu-id="5c483-105">使用者可以從主控台或直接從 [**開始**] 功能表存取 **預設程式**。</span><span class="sxs-lookup"><span data-stu-id="5c483-105">Users can access **Default Programs** from Control Panel or directly from the **Start** menu.</span></span> <span data-ttu-id="5c483-106">[設定程式存取和電腦預設值 (SPAD)](cpl-setprogramaccess.md) 工具（Windows XP 中的使用者主要預設體驗）現在是 **預設程式** 的一部分。</span><span class="sxs-lookup"><span data-stu-id="5c483-106">[Set Program Access and Computer Defaults (SPAD)](cpl-setprogramaccess.md) tool, the primary defaults experience for users in Windows XP, is now one part of **Default Programs**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5c483-107">本主題不適用於 Windows 10。</span><span class="sxs-lookup"><span data-stu-id="5c483-107">This topic does not apply for Windows 10.</span></span> <span data-ttu-id="5c483-108">預設檔案關聯在 Windows 10 中的運作方式有所變更。</span><span class="sxs-lookup"><span data-stu-id="5c483-108">The way that default file associations work changed in Windows 10.</span></span> <span data-ttu-id="5c483-109">如需詳細資訊，請參閱 [這篇文章](https://blogs.windows.com/windowsexperience/2015/05/20/announcing-windows-10-insider-preview-build-10122-for-pcs/)中有關 **Windows 10 如何處理預設應用程式的變更** 一節。</span><span class="sxs-lookup"><span data-stu-id="5c483-109">For more information, see the section on **Changes to how Windows 10 handles default apps** in [this post](https://blogs.windows.com/windowsexperience/2015/05/20/announcing-windows-10-insider-preview-build-10122-for-pcs/).</span></span>

 

<span data-ttu-id="5c483-110">當使用者使用 **預設程式** 設定程式預設值時，預設設定只會套用至該使用者，而不會套用到其他可能使用相同電腦的使用者。</span><span class="sxs-lookup"><span data-stu-id="5c483-110">When a user sets program defaults using **Default Programs**, the default setting applies only to that user and not to other users who might use the same computer.</span></span> <span data-ttu-id="5c483-111">**預設程式** 提供一組 (在 Windows 8) 中淘汰的 api，可讓獨立軟體廠商 (isv) 在預設系統中包含其程式或應用程式。</span><span class="sxs-lookup"><span data-stu-id="5c483-111">**Default Programs** provides a set of APIs (deprecated in Windows 8) that enable independent software vendors (ISVs) to include their programs or applications in the defaults system.</span></span> <span data-ttu-id="5c483-112">API 集也可協助 Isv 將其狀態更妥善地管理為預設值。</span><span class="sxs-lookup"><span data-stu-id="5c483-112">The API set also helps ISVs better manage their status as defaults.</span></span>

<span data-ttu-id="5c483-113">本主題的組織方式如下：</span><span class="sxs-lookup"><span data-stu-id="5c483-113">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="5c483-114">預設程式及其相關的 API 集合簡介</span><span class="sxs-lookup"><span data-stu-id="5c483-114">Introduction to Default Programs and Its Related API Set</span></span>](#introduction-to-default-programs-and-its-related-api-set)
-   [<span data-ttu-id="5c483-115">註冊應用程式以搭配預設程式使用</span><span class="sxs-lookup"><span data-stu-id="5c483-115">Registering an Application for Use with Default Programs</span></span>](#registering-an-application-for-use-with-default-programs)
    -   [<span data-ttu-id="5c483-116">Progid</span><span class="sxs-lookup"><span data-stu-id="5c483-116">ProgIDs</span></span>](#progids)
    -   [<span data-ttu-id="5c483-117">註冊子機碼和值描述</span><span class="sxs-lookup"><span data-stu-id="5c483-117">Registration Subkey and Value Descriptions</span></span>](#registration-subkey-and-value-descriptions)
    -   [<span data-ttu-id="5c483-118">RegisteredApplications</span><span class="sxs-lookup"><span data-stu-id="5c483-118">RegisteredApplications</span></span>](#registeredapplications)
    -   [<span data-ttu-id="5c483-119">完整註冊範例</span><span class="sxs-lookup"><span data-stu-id="5c483-119">Full Registration Example</span></span>](#full-registration-example)
-   [<span data-ttu-id="5c483-120">成為預設瀏覽器</span><span class="sxs-lookup"><span data-stu-id="5c483-120">Becoming the Default Browser</span></span>](#becoming-the-default-browser)
-   [<span data-ttu-id="5c483-121">預設程式 UI</span><span class="sxs-lookup"><span data-stu-id="5c483-121">Default Programs UI</span></span>](#default-programs-ui)
-   [<span data-ttu-id="5c483-122">使用預設程式的最佳作法</span><span class="sxs-lookup"><span data-stu-id="5c483-122">Best Practices for Using Default Programs</span></span>](#best-practices-for-using-default-programs)
    -   [<span data-ttu-id="5c483-123">在安裝期間</span><span class="sxs-lookup"><span data-stu-id="5c483-123">During Installation</span></span>](#during-installation)
    -   [<span data-ttu-id="5c483-124">安裝後</span><span class="sxs-lookup"><span data-stu-id="5c483-124">After Installation</span></span>](#after-installation)
-   [<span data-ttu-id="5c483-125">其他資源</span><span class="sxs-lookup"><span data-stu-id="5c483-125">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="5c483-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="5c483-126">Related topics</span></span>](#related-topics)

## <a name="introduction-to-default-programs-and-its-related-api-set"></a><span data-ttu-id="5c483-127">預設程式及其相關的 API 集合簡介</span><span class="sxs-lookup"><span data-stu-id="5c483-127">Introduction to Default Programs and Its Related API Set</span></span>

<span data-ttu-id="5c483-128">**預設程式** 主要是針對使用標準檔案類型的應用程式所設計，例如 mp3 或 .jpg 檔案或標準通訊協定，例如 HTTP 或 mailto。</span><span class="sxs-lookup"><span data-stu-id="5c483-128">**Default Programs** is primarily designed for applications that use standard file types such as .mp3 or .jpg files or standard protocols, such as HTTP or mailto.</span></span> <span data-ttu-id="5c483-129">使用專屬通訊協定和檔案關聯的應用程式通常不會使用 **預設的程式** 功能。</span><span class="sxs-lookup"><span data-stu-id="5c483-129">Applications that use their own proprietary protocols and file associations do not typically use the **Default Programs** functionality.</span></span>

<span data-ttu-id="5c483-130">針對 **預設程式** 功能註冊應用程式之後，您可以使用 API 集來使用下列選項和功能：</span><span class="sxs-lookup"><span data-stu-id="5c483-130">After you register an application for **Default Programs** functionality, the following options and functionality are available by using the API set:</span></span>

-   <span data-ttu-id="5c483-131">還原應用程式的所有已註冊的預設值。</span><span class="sxs-lookup"><span data-stu-id="5c483-131">Restore all registered defaults for an application.</span></span> <span data-ttu-id="5c483-132">Windows 8 已淘汰。</span><span class="sxs-lookup"><span data-stu-id="5c483-132">Deprecated for Windows 8.</span></span>
-   <span data-ttu-id="5c483-133">為應用程式還原單一已註冊的預設值。</span><span class="sxs-lookup"><span data-stu-id="5c483-133">Restore a single registered default for an application.</span></span> <span data-ttu-id="5c483-134">Windows 8 已淘汰。</span><span class="sxs-lookup"><span data-stu-id="5c483-134">Deprecated for Windows 8.</span></span>
-   <span data-ttu-id="5c483-135">在單一呼叫中查詢特定預設值的擁有者，而不是搜尋登錄。</span><span class="sxs-lookup"><span data-stu-id="5c483-135">Query for the owner of a specific default in a single call instead of searching the registry.</span></span> <span data-ttu-id="5c483-136">您可以查詢檔案關聯、通訊協定或 [ **開始** ] 功能表標準動詞命令的預設值。</span><span class="sxs-lookup"><span data-stu-id="5c483-136">You can query for the default of a file association, protocol, or **Start** menu canonical verb.</span></span>
-   <span data-ttu-id="5c483-137">針對特定應用程式啟動 UI，讓使用者可以在其中設定個別的預設值。</span><span class="sxs-lookup"><span data-stu-id="5c483-137">Launch a UI for a specific application where a user can set individual defaults.</span></span>
-   <span data-ttu-id="5c483-138">移除所有的每個使用者關聯。</span><span class="sxs-lookup"><span data-stu-id="5c483-138">Remove all per-user associations.</span></span>

<span data-ttu-id="5c483-139">**預設程式** 也提供 UI，可讓您註冊應用程式，以便為使用者提供其他資訊。</span><span class="sxs-lookup"><span data-stu-id="5c483-139">**Default Programs** also provides a UI that enables you to register an application in order to provide additional information to the user.</span></span> <span data-ttu-id="5c483-140">例如，數位簽署的應用程式可以包含製造商首頁的 URL。</span><span class="sxs-lookup"><span data-stu-id="5c483-140">For example, a digitally signed application can include a URL to the manufacturer's home page.</span></span>

<span data-ttu-id="5c483-141">使用相關聯的 API 集可協助應用程式在 Windows Vista 中引進 (UAC) 功能的使用者帳戶控制下正確運作。</span><span class="sxs-lookup"><span data-stu-id="5c483-141">Use of the associated API set can help an application function correctly under the user account control (UAC) feature introduced in Windows Vista.</span></span> <span data-ttu-id="5c483-142">在 UAC 下，系統管理員會以標準使用者的身分顯示系統，讓系統管理員通常無法寫入 **HKEY \_ 本機 \_ 電腦** 子樹。</span><span class="sxs-lookup"><span data-stu-id="5c483-142">Under UAC, an administrator appears to the system as a standard user, so that administrator cannot typically write to the **HKEY\_LOCAL\_MACHINE** subtree.</span></span> <span data-ttu-id="5c483-143">這項限制是一種安全性功能，可防止進程成為系統管理員，而不需要系統管理員的知識。</span><span class="sxs-lookup"><span data-stu-id="5c483-143">This restriction is a security feature that prevents a process from acting as an administrator without the administrator's knowledge.</span></span>

<span data-ttu-id="5c483-144">使用者安裝程式通常是以提高許可權的進程執行。</span><span class="sxs-lookup"><span data-stu-id="5c483-144">Installation of a program by a user is typically performed as an elevated process.</span></span> <span data-ttu-id="5c483-145">不過，應用程式在安裝後於電腦層級修改預設關聯線為的嘗試會失敗。</span><span class="sxs-lookup"><span data-stu-id="5c483-145">However, attempts by an application to modify default association behaviors at a machine level post-installation will be unsuccessful.</span></span> <span data-ttu-id="5c483-146">相反地，預設值必須在每個使用者層級上註冊，如此可防止多個使用者覆寫彼此的預設值。</span><span class="sxs-lookup"><span data-stu-id="5c483-146">Instead, defaults must be registered on a per-user level, which prevents multiple users from overwriting each other's defaults.</span></span>

<span data-ttu-id="5c483-147">檔案和通訊協定關聯的階層式登錄結構，優先于電腦層級預設值的每個使用者預設值。</span><span class="sxs-lookup"><span data-stu-id="5c483-147">The hierarchical registry structure for file and protocol associations gives precedence to per-user defaults over machine-level defaults.</span></span> <span data-ttu-id="5c483-148">有些應用程式在其程式碼中包含的點，會在宣告 **HKEY \_ 本機 \_ 電腦** 中註冊的預設值時，暫時提升其許可權。</span><span class="sxs-lookup"><span data-stu-id="5c483-148">Some applications include points in their code that temporarily elevate their rights when they claim defaults registered in **HKEY\_LOCAL\_MACHINE**.</span></span> <span data-ttu-id="5c483-149">如果另一個應用程式已經註冊為每個使用者的預設值，則這些應用程式可能會遇到非預期的結果。</span><span class="sxs-lookup"><span data-stu-id="5c483-149">These applications might experience unexpected results if another application is already registered as the per-user default.</span></span> <span data-ttu-id="5c483-150">使用 **預設程式** 可避免這種混淆，並保證每個使用者層級的預期結果。</span><span class="sxs-lookup"><span data-stu-id="5c483-150">Use of **Default Programs** prevents this ambiguity and guarantees expected results on a per-user level.</span></span>

## <a name="registering-an-application-for-use-with-default-programs"></a><span data-ttu-id="5c483-151">註冊應用程式以搭配預設程式使用</span><span class="sxs-lookup"><span data-stu-id="5c483-151">Registering an Application for Use with Default Programs</span></span>

<span data-ttu-id="5c483-152">本節說明使用 **預設程式** 註冊應用程式所需的登錄子機碼和值。</span><span class="sxs-lookup"><span data-stu-id="5c483-152">This section shows you the registry subkeys and values needed to register an application with **Default Programs**.</span></span> <span data-ttu-id="5c483-153">其中包含完整的範例。</span><span class="sxs-lookup"><span data-stu-id="5c483-153">It includes a full example.</span></span>

<span data-ttu-id="5c483-154">本節包含下列主題：</span><span class="sxs-lookup"><span data-stu-id="5c483-154">This section contains the following topics:</span></span>

-   [<span data-ttu-id="5c483-155">Progid</span><span class="sxs-lookup"><span data-stu-id="5c483-155">ProgIDs</span></span>](#progids)
-   [<span data-ttu-id="5c483-156">註冊子機碼和值描述</span><span class="sxs-lookup"><span data-stu-id="5c483-156">Registration Subkey and Value Descriptions</span></span>](#registration-subkey-and-value-descriptions)
-   [<span data-ttu-id="5c483-157">RegisteredApplications</span><span class="sxs-lookup"><span data-stu-id="5c483-157">RegisteredApplications</span></span>](#registeredapplications)
-   [<span data-ttu-id="5c483-158">完整註冊範例</span><span class="sxs-lookup"><span data-stu-id="5c483-158">Full Registration Example</span></span>](#full-registration-example)

<span data-ttu-id="5c483-159">**預設程式** 會要求每個應用程式明確註冊檔案關聯、MIME 關聯，以及應將應用程式列為可能預設值的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="5c483-159">**Default Programs** requires each application to register explicitly the file associations, MIME associations, and protocols for which the application should be listed as a possible default.</span></span> <span data-ttu-id="5c483-160">您可以使用下列登錄專案來註冊關聯，稍後在本主題的註冊子機碼 [和值描述](#registration-subkey-and-value-descriptions)下會詳細說明：</span><span class="sxs-lookup"><span data-stu-id="5c483-160">You register the associations by using the following registry elements, which are explained in detail later in this topic under [Registration Subkey and Value Descriptions](#registration-subkey-and-value-descriptions):</span></span>

```
HKEY_LOCAL_MACHINE
   %ApplicationCapabilityPath%
      ApplicationDescription
      ApplicationName
      Hidden
      FileAssociations
         .file-extension1
         .file-extension2
         ...
         .file-extensionX
      MIMEAssociations
         MIME
      Startmenu
         StartmenuInternet
         Mail
      UrlAssociations
         url-scheme
   SOFTWARE
      RegisteredApplications
         Unique Application Name = %ApplicationCapabilityPath%
```

<span data-ttu-id="5c483-161">下列範例會顯示虛構 Contoso 瀏覽器的登錄專案，稱為 WebBrowser：</span><span class="sxs-lookup"><span data-stu-id="5c483-161">The following example shows the registry entries for a fictional Contoso browser that is called WebBrowser:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Contoso
         WebBrowser
            Capabilities
               ApplicationDescription = This award-winning Contoso browser is better than ever. Search the Internet and find exactly what you want in just seconds. Use integrated tabs and new phishing detectors to enhance your Internet experience.
               FileAssociations
                  .htm = ContosoHTML
                  .html = ContosoHTML
                  .shtml = ContosoHTML
                  .xht = ContosoHTML
                  .xhtml = ContosoHTML
               Startmenu
                  StartmenuInternet = Contoso.exe
               UrlAssociations
                  http = Contoso.Url.Http
                  https = Contoso.Url.Https
                  ftp = Contoso.Url.ftp
   SOFTWARE
      RegisteredApplications
         Contoso.WebBrowser.1.06 = SOFTWARE\Contoso\WebBrowser\Capabilities
```

### <a name="progids"></a><span data-ttu-id="5c483-162">Progid</span><span class="sxs-lookup"><span data-stu-id="5c483-162">ProgIDs</span></span>

<span data-ttu-id="5c483-163">應用程式必須提供特定的 [ProgID](fa-progids.md)。</span><span class="sxs-lookup"><span data-stu-id="5c483-163">An application must provide a specific [ProgID](fa-progids.md).</span></span> <span data-ttu-id="5c483-164">請務必包含通常寫入延伸模組之一般預設子機碼中的所有資訊。</span><span class="sxs-lookup"><span data-stu-id="5c483-164">Be sure to include all the information that is typically written into the generic default subkey for the extension.</span></span> <span data-ttu-id="5c483-165">例如，虛構的 Litware media player 會提供應用程式特定的 **HKEY \_ 本機 \_ 電腦** \\ **軟體** \\ **類別** \\ **LitwarePlayer11.AssocFile.MP3** 子機碼。</span><span class="sxs-lookup"><span data-stu-id="5c483-165">For example, the fictional Litware media player provides the application-specific **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Classes**\\**LitwarePlayer11.AssocFile.MP3** subkey.</span></span> <span data-ttu-id="5c483-166">該子機碼包含一般預設子 **機碼 HKEY \_ 本機 \_ 電腦** 軟體類別中的所有資訊 \\  \\  \\ **。 mp3** 加上您想要應用程式註冊的任何其他資訊。</span><span class="sxs-lookup"><span data-stu-id="5c483-166">That subkey includes all the information in the generic default subkey **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Classes**\\ **.mp3** plus any additional information that you want the application to register.</span></span> <span data-ttu-id="5c483-167">如此可確保當使用者將 mp3 關聯還原到 Litware 播放程式時，Litware 播放程式的資訊不會完整，也不會被另一個應用程式覆寫。</span><span class="sxs-lookup"><span data-stu-id="5c483-167">This ensures that if the user restores the .mp3 association to the Litware player, the Litware player's information is intact and has not been overwritten by another application.</span></span> <span data-ttu-id="5c483-168">如果預設子機碼是該資訊的唯一來源，則可能會發生 (覆寫。 ) </span><span class="sxs-lookup"><span data-stu-id="5c483-168">(Overwriting might occur if the default subkey is the only source of that information.)</span></span>

<span data-ttu-id="5c483-169">當您將 ProgID 對應至副檔名或通訊協定時，應用程式可以對應到一或多個。</span><span class="sxs-lookup"><span data-stu-id="5c483-169">When you map a ProgID to a file name extension or protocol, an application can map one-to-one or one-to-many.</span></span> <span data-ttu-id="5c483-170">在 Contoso 範例中，ContosoHTML 會指向提供 .htm、.html、. >.shtml、xht 和 xhtml 副檔名 shellexecute 資訊的單一 ProgID。</span><span class="sxs-lookup"><span data-stu-id="5c483-170">In the Contoso example, ContosoHTML points to a single ProgID that provides shellexecute information for the .htm, .html, .shtml, .xht, and .xhtml extensions.</span></span> <span data-ttu-id="5c483-171">因為每個通訊協定都有不同的 ProgID，所以當您使用通訊協定時，您可以讓每個通訊協定都有自己的執行字串。</span><span class="sxs-lookup"><span data-stu-id="5c483-171">Because a different ProgID exists for each protocol, when you use protocols you enable each protocol to have its own execution string.</span></span>

<span data-ttu-id="5c483-172">當您的 MIME 類型可以內嵌在瀏覽器中時，MIME 型別的 ProgID 必須包含 **clsid** 子機碼，以使用對應應用程式 (clsid) 的類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="5c483-172">When your MIME type can be viewed inline in a browser, the ProgID for the MIME type must contain the **CLSID** subkey that uses the class identifier (CLSID) of the corresponding application.</span></span> <span data-ttu-id="5c483-173">此 clsid 用於查閱 mime 資料庫中儲存于 **HKEY \_ 本機 \_ 電腦** \\ **軟體** \\ **類別** \\ **mime** \\ **資料庫** \\ **內容類型** 的 CLSID。</span><span class="sxs-lookup"><span data-stu-id="5c483-173">This CLSID is used in a lookup against the CLSID in the MIME database that is stored in **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Classes**\\**MIME**\\**Database**\\**Content Type**.</span></span> <span data-ttu-id="5c483-174">如果您的 MIME 類型不是要在瀏覽器中以內嵌方式來流覽，則可以省略此步驟。</span><span class="sxs-lookup"><span data-stu-id="5c483-174">If your MIME type is not intended to be viewed inline in a browser, this step can be omitted.</span></span>

### <a name="registration-subkey-and-value-descriptions"></a><span data-ttu-id="5c483-175">註冊子機碼和值描述</span><span class="sxs-lookup"><span data-stu-id="5c483-175">Registration Subkey and Value Descriptions</span></span>

<span data-ttu-id="5c483-176">本節說明使用 **預設程式** 來註冊應用程式時所使用的個別登錄子機碼和值，如先前所述。</span><span class="sxs-lookup"><span data-stu-id="5c483-176">This section describes the individual registry subkeys and values used in registering an application with **Default Programs**, as illustrated previously.</span></span>

### <a name="capabilities"></a><span data-ttu-id="5c483-177">功能</span><span class="sxs-lookup"><span data-stu-id="5c483-177">Capabilities</span></span>

<span data-ttu-id="5c483-178">[ **功能** ] 子機碼包含特定應用程式的所有 **預設程式** 資訊。</span><span class="sxs-lookup"><span data-stu-id="5c483-178">The **Capabilities** subkey contains all the **Default Programs** information for a specific application.</span></span> <span data-ttu-id="5c483-179">預留位置% ApplicationCapabilityPath% 指的是從 **HKEY \_ 目前 \_ 使用者** 或 **HKEY \_ 本機 \_ 電腦** 到應用程式 **功能** 子機碼的登錄路徑。</span><span class="sxs-lookup"><span data-stu-id="5c483-179">The placeholder %ApplicationCapabilityPath% refers to the registry path from either **HKEY\_CURRENT\_USER** or **HKEY\_LOCAL\_MACHINE** to the application's **Capabilities** subkey.</span></span> <span data-ttu-id="5c483-180">此子機碼包含下表所示的重要值。</span><span class="sxs-lookup"><span data-stu-id="5c483-180">This subkey contains the significant values shown in the following table.</span></span>



| <span data-ttu-id="5c483-181">值</span><span class="sxs-lookup"><span data-stu-id="5c483-181">Value</span></span>                  | <span data-ttu-id="5c483-182">類型</span><span class="sxs-lookup"><span data-stu-id="5c483-182">Type</span></span>                       | <span data-ttu-id="5c483-183">意義</span><span class="sxs-lookup"><span data-stu-id="5c483-183">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------------------|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c483-184">ApplicationDescription</span><span class="sxs-lookup"><span data-stu-id="5c483-184">ApplicationDescription</span></span> | <span data-ttu-id="5c483-185">REG \_ sz 或 reg \_ EXPAND \_ SZ</span><span class="sxs-lookup"><span data-stu-id="5c483-185">REG\_SZ or REG\_EXPAND\_SZ</span></span> | <span data-ttu-id="5c483-186">**必要**。</span><span class="sxs-lookup"><span data-stu-id="5c483-186">**Required**.</span></span> <span data-ttu-id="5c483-187">若要讓使用者能夠做出明智的預設指派選項，應用程式必須提供描述應用程式功能的字串。</span><span class="sxs-lookup"><span data-stu-id="5c483-187">To enable a user to make an informed default assignment choice, an application must provide a string that describes the application's capabilities.</span></span> <span data-ttu-id="5c483-188">雖然先前的 Contoso 範例會將描述直接指派給 ApplicationDescription 值，但應用程式通常會提供描述做為內嵌于 .dll 檔案中的資源，以利進行當地語系化。</span><span class="sxs-lookup"><span data-stu-id="5c483-188">Although the previous Contoso example assigns the description directly to the ApplicationDescription value, applications typically provide the description as a resource that is embedded in a .dll file to facilitate localization.</span></span> <span data-ttu-id="5c483-189">如果未提供 ApplicationDescription，則應用程式不會出現在可能的預設程式的 UI 清單中。</span><span class="sxs-lookup"><span data-stu-id="5c483-189">If ApplicationDescription is not provided, the application does not appear in UI lists of potential default programs.</span></span>                                                            |
| <span data-ttu-id="5c483-190">ApplicationName</span><span class="sxs-lookup"><span data-stu-id="5c483-190">ApplicationName</span></span>        | <span data-ttu-id="5c483-191">REG \_ sz 或 reg \_ EXPAND \_ SZ</span><span class="sxs-lookup"><span data-stu-id="5c483-191">REG\_SZ or REG\_EXPAND\_SZ</span></span> | <span data-ttu-id="5c483-192">**選擇性。**</span><span class="sxs-lookup"><span data-stu-id="5c483-192">**Optional.**</span></span> <span data-ttu-id="5c483-193">程式在 [預設程式] UI 中出現的名稱。</span><span class="sxs-lookup"><span data-stu-id="5c483-193">The name by which the program appears in the Default Programs UI.</span></span> <span data-ttu-id="5c483-194">如果應用程式未提供此資料，則會在 UI 中使用與應用程式的第一個已註冊 ProgID 相關聯之可執行程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="5c483-194">If this data is not provided by the application, the name of the executable program that is associated with the first registered ProgID for the application is used in the UI.</span></span> <span data-ttu-id="5c483-195">ApplicationName 必須一律符合在 [RegisteredApplications](#registeredapplications)中註冊的名稱。</span><span class="sxs-lookup"><span data-stu-id="5c483-195">ApplicationName must always match the name that is registered under [RegisteredApplications](#registeredapplications).</span></span> <span data-ttu-id="5c483-196">如果您想要不同的應用程式類型（例如瀏覽器和電子郵件客戶程式）指向相同的可執行檔，但其顯示為不同的名稱，您可以使用 ApplicationName。</span><span class="sxs-lookup"><span data-stu-id="5c483-196">You can use ApplicationName if you want different application types, such as a browser and an email client, to point to the same executable file while they appear as different names.</span></span><br/> |
| <span data-ttu-id="5c483-197">Hidden</span><span class="sxs-lookup"><span data-stu-id="5c483-197">Hidden</span></span>                 | <span data-ttu-id="5c483-198">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="5c483-198">REG\_DWORD</span></span>                 | <span data-ttu-id="5c483-199">**選擇性。**</span><span class="sxs-lookup"><span data-stu-id="5c483-199">**Optional.**</span></span> <span data-ttu-id="5c483-200">將此值設定為1，以在 [ **設定您的預設程式** ] 對話方塊中的程式清單中隱藏應用程式。</span><span class="sxs-lookup"><span data-stu-id="5c483-200">Set this value to 1 to suppress the application from the list of programs in the **Set your default programs** dialog.</span></span> <span data-ttu-id="5c483-201">如果這個值為0或不存在，則應用程式會在清單中正常顯示。</span><span class="sxs-lookup"><span data-stu-id="5c483-201">If this value is 0 or not present, then the application appears in the list normally.</span></span>                                                                                                                                                                                                                                                                                                                                                              |



 

### <a name="fileassociations"></a><span data-ttu-id="5c483-202">FileAssociations</span><span class="sxs-lookup"><span data-stu-id="5c483-202">FileAssociations</span></span>

<span data-ttu-id="5c483-203">**FileAssociations** 子機碼包含應用程式所宣告的特定檔案關聯。</span><span class="sxs-lookup"><span data-stu-id="5c483-203">The **FileAssociations** subkey contains specific file associations that are claimed by the application.</span></span> <span data-ttu-id="5c483-204">這些宣告會儲存為值，每個延伸模組都有一個值。</span><span class="sxs-lookup"><span data-stu-id="5c483-204">These claims are stored as values, with one value for each extension.</span></span> <span data-ttu-id="5c483-205">關聯會指向應用程式特定的 ProgID，而不是泛型 ProgID。</span><span class="sxs-lookup"><span data-stu-id="5c483-205">Associations point to an application-specific ProgID instead of a generic ProgID.</span></span> <span data-ttu-id="5c483-206">不過，並非所有關聯都必須指向相同的 ProgID。</span><span class="sxs-lookup"><span data-stu-id="5c483-206">However, all associations are not required to point to the same ProgID.</span></span>

### <a name="mimeassociations"></a><span data-ttu-id="5c483-207">MIMEAssociations</span><span class="sxs-lookup"><span data-stu-id="5c483-207">MIMEAssociations</span></span>

<span data-ttu-id="5c483-208">**MIMEAssociations** 子機碼包含應用程式所宣告的特定 MIME 類型。</span><span class="sxs-lookup"><span data-stu-id="5c483-208">The **MIMEAssociations** subkey contains specific MIME types that are claimed by the application.</span></span> <span data-ttu-id="5c483-209">這些宣告會儲存為值，每個 MIME 類型都有一個值。</span><span class="sxs-lookup"><span data-stu-id="5c483-209">These claims are stored as values, with one value for each MIME type.</span></span> <span data-ttu-id="5c483-210">每個 MIME 類型的值名稱都必須完全符合 MIME 資料庫中所儲存的 MIME 名稱。</span><span class="sxs-lookup"><span data-stu-id="5c483-210">The value name for each MIME type must exactly match the MIME name that is stored in the MIME database.</span></span> <span data-ttu-id="5c483-211">您也必須將應用程式特定的 ProgID 指派給此值，其中包含應用程式的對應 CLSID。</span><span class="sxs-lookup"><span data-stu-id="5c483-211">The value must also be assigned an application-specific ProgID that contains the corresponding CLSID of the application.</span></span>

### <a name="startmenu"></a><span data-ttu-id="5c483-212">Startmenu</span><span class="sxs-lookup"><span data-stu-id="5c483-212">Startmenu</span></span>

<span data-ttu-id="5c483-213">**Startmenu** 子機碼與 [**開始**] 功能表中使用者可指派的 **網際網路** 和 **電子郵件** 專案相關聯。</span><span class="sxs-lookup"><span data-stu-id="5c483-213">The **Startmenu** subkey is associated with the user-assignable **Internet** and **E-mail** entries in the **Start** menu.</span></span> <span data-ttu-id="5c483-214">應用程式必須個別註冊為這些專案的競爭者。</span><span class="sxs-lookup"><span data-stu-id="5c483-214">An application must register separately as a contender for those entries.</span></span> <span data-ttu-id="5c483-215">如需詳細資訊，請參閱 [使用用戶端類型註冊程式](reg-middleware-apps.md)。</span><span class="sxs-lookup"><span data-stu-id="5c483-215">For more information, see [Registering Programs with Client Types](reg-middleware-apps.md).</span></span>

> [!Note]  
> <span data-ttu-id="5c483-216">從 Windows 7 開始，[**開始**] 功能表中已不再有 **網際網路** 和 **電子郵件** 專案。</span><span class="sxs-lookup"><span data-stu-id="5c483-216">As of Windows 7, there are no longer **Internet** and **E-mail** entries in the **Start** menu.</span></span> <span data-ttu-id="5c483-217">與 **電子郵件** 專案相關的登錄資料仍會用於預設的 MAPI 用戶端，但 Windows 完全不會使用與 **網際網路** 專案相關聯的登錄資料。</span><span class="sxs-lookup"><span data-stu-id="5c483-217">The registry data associated with the **E-mail** entry is still used for the default MAPI client, but the registry data associated with the **Internet** entry is not used by Windows at all.</span></span>

 

<span data-ttu-id="5c483-218">藉由將應用程式的 [ **開始** ] 功能表註冊與其 **預設程式** 註冊產生關聯，應用程式在 [ **設定關聯** ] UI 中會顯示為可能的預設值。</span><span class="sxs-lookup"><span data-stu-id="5c483-218">By associating the **Start** menu registration of an application with its **Default Programs** registration, the application appears as a potential default in the **Set associations** UI.</span></span> <span data-ttu-id="5c483-219">如果使用者選擇使用應用程式做為預設值，然後選擇還原所有的應用程式預設值，則會將應用程式還原至該使用者的 [ **開始** ] 功能表位置。</span><span class="sxs-lookup"><span data-stu-id="5c483-219">If the user has chosen the application as the default and then chooses to restore all application defaults later, the application is restored to its **Start** menu position for that user.</span></span> <span data-ttu-id="5c483-220">如需詳細資訊和圖例，請參閱本主題稍後的 [預設程式 UI](#default-programs-ui) 一節。</span><span class="sxs-lookup"><span data-stu-id="5c483-220">For more information and an illustration, see the [Default Programs UI](#default-programs-ui) section later in this topic.</span></span>

<span data-ttu-id="5c483-221">**Startmenu** 子機碼有兩個專案： [StartMenuInternet] 和 [Mail]，其對應于 [**開始**] 功能表中的標準 **網際網路** 和 **電子郵件** 位置。</span><span class="sxs-lookup"><span data-stu-id="5c483-221">The **Startmenu** subkey has two entries: StartMenuInternet and Mail, which correspond to the canonical **Internet** and **E-mail** positions in the **Start** menu.</span></span> <span data-ttu-id="5c483-222">應用程式會在 [ **HKEY \_ 本機 \_ 電腦** \\ **軟體** \\ **客戶** 端 \\ **StartMenuInternet** 或 **HKEY \_ 本機 \_** 電腦軟體用戶端郵件 (] 下，指派等於應用程式登錄子機碼名稱的 StartMenuInternet 或 Mail 值， \\  \\  \\ 如) 的 [[註冊程式](reg-middleware-apps.md)] 中所述。</span><span class="sxs-lookup"><span data-stu-id="5c483-222">An application assigns either StartMenuInternet or Mail a value equal to the name of the application's registered subkey under **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**StartMenuInternet** or **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**Mail** (as described in [Registering Programs with Client Types](reg-middleware-apps.md)).</span></span>

<span data-ttu-id="5c483-223">在 [**開始**] 功能表中的 **電子郵件** 標準位置案例中，它代表預設的 mapi 用戶端，因此假設能夠處理 MAPI 呼叫。</span><span class="sxs-lookup"><span data-stu-id="5c483-223">In the case of the **E-mail** canonical position in the **Start** menu, it represents the default MAPI client and is therefore assumed capable of handing MAPI calls.</span></span> <span data-ttu-id="5c483-224">在 Windows 7 下，在 [**開始**] 功能表中已不再有 **電子郵件** 標準位置，這個子機碼會繼續用於預設的 MAPI 用戶端。</span><span class="sxs-lookup"><span data-stu-id="5c483-224">Under Windows 7, while there is no longer an **E-mail** canonical position in the **Start** menu, this subkey continues to be used for the default MAPI client.</span></span> <span data-ttu-id="5c483-225">宣告郵件預設值的應用程式應該在下列子機碼下註冊為 MAPI 處理常式：</span><span class="sxs-lookup"><span data-stu-id="5c483-225">An application claiming the mail default should register as a MAPI handler under the following subkey:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            CanonicalName
```

<span data-ttu-id="5c483-226">如果郵件用戶端無法支援 MAPI，但仍想要爭用 [ **開始** ] 功能表 **電子郵件** 標準位置，它可以在下列子機碼底下註冊命令列：</span><span class="sxs-lookup"><span data-stu-id="5c483-226">If a mail client cannot support MAPI but still wants to contend for the **Start** menu **E-mail** canonical position, it can register a command line under the following subkey:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            CanonicalName
               shell
                  open
                     command
```

<span data-ttu-id="5c483-227">此外，在 [ **HKEY \_ 本機 \_ 電腦** \\ **軟體** \\ **用戶端** \\ **郵件** \\ *CanonicalName* ] 下，新增具有應用程式名稱的預設值。</span><span class="sxs-lookup"><span data-stu-id="5c483-227">Also, under **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**Mail**\\*CanonicalName* add a default value with the application name.</span></span>

<span data-ttu-id="5c483-228">這些專案可讓您從 [ **開始** ] 功能表的 **電子郵件** 位置啟動應用程式。</span><span class="sxs-lookup"><span data-stu-id="5c483-228">These entries allow the application to be launched from the **Start** menu's **E-mail** position.</span></span> <span data-ttu-id="5c483-229">請注意，系統仍會對應用程式進行 MAPI 呼叫，並且會在先前的 MAPI 處理常式中執行，如果未設定 MAPI 處理常式，則會失敗。</span><span class="sxs-lookup"><span data-stu-id="5c483-229">Note that MAPI calls are still made to the application, and either fall through to the prior MAPI handler, or fail if no MAPI handler has been set.</span></span> <span data-ttu-id="5c483-230">如需詳細資訊，請參閱 [使用用戶端類型註冊程式](reg-middleware-apps.md)。</span><span class="sxs-lookup"><span data-stu-id="5c483-230">For more information, see [Registering Programs with Client Types](reg-middleware-apps.md).</span></span>

### <a name="urlassociations"></a><span data-ttu-id="5c483-231">UrlAssociations</span><span class="sxs-lookup"><span data-stu-id="5c483-231">UrlAssociations</span></span>

<span data-ttu-id="5c483-232">**UrlAssociations** 子機碼包含應用程式所宣告的特定 URL 通訊協定。</span><span class="sxs-lookup"><span data-stu-id="5c483-232">The **UrlAssociations** subkey contains the specific URL protocols that are claimed by the application.</span></span> <span data-ttu-id="5c483-233">這些宣告會儲存為值，每個通訊協定都有一個值。</span><span class="sxs-lookup"><span data-stu-id="5c483-233">These claims are stored as values, with one value for each protocol.</span></span> <span data-ttu-id="5c483-234">每個通訊協定都必須指向應用程式特定的 ProgID，而不是一般 ProgID。</span><span class="sxs-lookup"><span data-stu-id="5c483-234">Each protocol must point to an application-specific ProgID instead of to a generic ProgID.</span></span> <span data-ttu-id="5c483-235">如 Contoso 範例中所述，您可以針對每個通訊協定使用不同的 ProgID，讓每個通訊協定都有自己的執行字串。</span><span class="sxs-lookup"><span data-stu-id="5c483-235">As mentioned in the Contoso example, you can use a different ProgID for each protocol in order for each to have its own execution string.</span></span>

### <a name="registeredapplications"></a><span data-ttu-id="5c483-236">RegisteredApplications</span><span class="sxs-lookup"><span data-stu-id="5c483-236">RegisteredApplications</span></span>

<span data-ttu-id="5c483-237">**RegisteredApplications** 的完整子機碼為：</span><span class="sxs-lookup"><span data-stu-id="5c483-237">The full subkey for **RegisteredApplications** is:</span></span>

<span data-ttu-id="5c483-238">**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **RegisteredApplications**</span><span class="sxs-lookup"><span data-stu-id="5c483-238">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**RegisteredApplications**</span></span>

<span data-ttu-id="5c483-239">此子機碼為作業系統提供應用程式的 **預設程式** 資訊的登錄位置。</span><span class="sxs-lookup"><span data-stu-id="5c483-239">This subkey provides the operating system with the registry location of the **Default Programs** information for the application.</span></span> <span data-ttu-id="5c483-240">位置會儲存為值，其名稱必須與應用程式的名稱相符。</span><span class="sxs-lookup"><span data-stu-id="5c483-240">The location is stored as a value whose name must match the name of the application.</span></span>

### <a name="full-registration-example"></a><span data-ttu-id="5c483-241">完整註冊範例</span><span class="sxs-lookup"><span data-stu-id="5c483-241">Full Registration Example</span></span>

<span data-ttu-id="5c483-242">此範例顯示用來註冊虛構 Litware 媒體播放機的子機碼和值。</span><span class="sxs-lookup"><span data-stu-id="5c483-242">This example shows the subkeys and values that are used in registering the fictional Litware media player.</span></span> <span data-ttu-id="5c483-243">此範例包含 ProgID 專案，以顯示其如何彼此搭配。</span><span class="sxs-lookup"><span data-stu-id="5c483-243">The example includes the ProgID entries in order to show how it all fits together.</span></span>

<span data-ttu-id="5c483-244">下列子機碼顯示針對. mp3 MIME 類型的應用程式特定 ProgID：</span><span class="sxs-lookup"><span data-stu-id="5c483-244">The following subkey shows the application-specific ProgID for the .mp3 MIME type:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         LitwarePlayer11.MIME.MP3
            CLSID
               (Default) = {CD3AFA76-B84F-48F0-9393-7EDC34128127}
```

<span data-ttu-id="5c483-245">接下來是應用程式特定的 ProgID，會將 Litware 程式與. mp3 副檔名產生關聯。</span><span class="sxs-lookup"><span data-stu-id="5c483-245">Next is the application-specific ProgID that associates the Litware program with the .mp3 file name extension.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         LitwarePlayer11.AssocFile.MP3
            (Default) = MP3 Format Sound
            DefaultIcon
               (Default) = %ProgramFiles%\Litware\litware.dll, 0
            shell
               open
                  command
                     (Default) = %ProgramFiles%\Litware\litware.exe
```

<span data-ttu-id="5c483-246">下一個專案顯示的是 mpeg-2 MIME 類型和副檔名的結合 ProgID。</span><span class="sxs-lookup"><span data-stu-id="5c483-246">The next entries show the combined ProgID for both the .mpeg MIME type and file name extension.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         LitwarePlayer11.AssocFile.MPG
            (Default) = Movie Clip
            CLSID
               (Default) = {D92B76F4-CFA0-4b93-866B-7730FEB4CD7B}
            DefaultIcon
               (Default) = %ProgramFiles%\Litware\litware.dll, 0
            shell
               open
                  command
                     (Default) = %ProgramFiles%\Litware\litware.exe
```

<span data-ttu-id="5c483-247">下個專案會在 **預設程式** 中註冊 Litware 程式，並使用先前註冊的 progid</span><span class="sxs-lookup"><span data-stu-id="5c483-247">The next entries register the Litware program in **Default Programs** and use the previously registered ProgIDs</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Litware
         LitwarePlayer
            Capabilities
               ApplicationDescription = The new Litware Media Player breaks new ground in exciting fictional programs.
               FileAssociations
                  .mp3 = LitwarePlayer11.AssocFile.MP3
                  .mpeg = LitwarePlayer11.AssocFile.MPG
               MimeAssociations
                  audio/mp3 = LitwarePlayer11.MIME.MP3
                  audio/mpeg = LitwarePlayer11.AssocFile.MPG
```

<span data-ttu-id="5c483-248">最後，此範例會註冊 Litware **預設程式** 註冊的位置。</span><span class="sxs-lookup"><span data-stu-id="5c483-248">Lastly, this example registers the location of the Litware **Default Programs** registration.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      RegisteredApplications
         Litware Player = Software\Litware\LitwarePlayer\Capabilities
```

## <a name="becoming-the-default-browser"></a><span data-ttu-id="5c483-249">成為預設瀏覽器</span><span class="sxs-lookup"><span data-stu-id="5c483-249">Becoming the Default Browser</span></span>

<span data-ttu-id="5c483-250">瀏覽器註冊必須遵循本主題中所述的最佳做法。</span><span class="sxs-lookup"><span data-stu-id="5c483-250">Browser registration must follow the best practices outlined in this topic.</span></span> <span data-ttu-id="5c483-251">當您安裝瀏覽器時，Windows 可以向使用者呈現系統通知，讓使用者可以選取瀏覽器做為系統預設值。</span><span class="sxs-lookup"><span data-stu-id="5c483-251">When the browser is installed, Windows can present the user with a system notification through which the user can select the browser as the system default.</span></span> <span data-ttu-id="5c483-252">當符合下列條件時，就會顯示此通知：</span><span class="sxs-lookup"><span data-stu-id="5c483-252">This notification is shown when these conditions are met:</span></span>

-   <span data-ttu-id="5c483-253">瀏覽器的安裝程式會使用 **SHCNE \_ ASSOCCHANGED** 旗標來呼叫 [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) ，告訴 Windows 已註冊新的通訊協定處理常式。</span><span class="sxs-lookup"><span data-stu-id="5c483-253">The browser's installer calls [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) with the **SHCNE\_ASSOCCHANGED** flag to tell Windows that new protocol handlers have been registered.</span></span>
-   <span data-ttu-id="5c483-254">Windows 偵測到一或多個新的應用程式已註冊來處理 HTTP://和 HTTPs://通訊協定，且使用者尚未收到通知。</span><span class="sxs-lookup"><span data-stu-id="5c483-254">Windows detects that one or more new applications have registered to handle both http:// and https:// protocols, and the user has not yet been notified.</span></span> <span data-ttu-id="5c483-255">換句話說，使用者未看到下列其中一項：廣告應用程式的系統通知、包含應用程式的 OpenWith 飛出視窗，或應用程式的 [設定使用者預設值] (主控台) SUD] 頁面。</span><span class="sxs-lookup"><span data-stu-id="5c483-255">In other words, none of the following have been shown to the user: a system notification advertising the application, an OpenWith flyout that contains the application, or the Set User Defaults (SUD) Control Panel page for the application.</span></span>

<span data-ttu-id="5c483-256">下列範例會顯示瀏覽器的安裝程式在寫入登錄機碼之後應該執行的建議註冊程式碼。</span><span class="sxs-lookup"><span data-stu-id="5c483-256">The following example shows the recommended registration code that the browser's installer should run after it writes its registry keys.</span></span>

<span data-ttu-id="5c483-257">[**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) 會先通知系統有新的關聯選項可供使用。</span><span class="sxs-lookup"><span data-stu-id="5c483-257">[**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) first notifies the system that new association choices are available.</span></span> <span data-ttu-id="5c483-258">需要 **SHChangeNotify** 呼叫，才能確保系統預設值的正常運作。</span><span class="sxs-lookup"><span data-stu-id="5c483-258">The **SHChangeNotify** call is required to ensure the proper functioning of system defaults.</span></span>

<span data-ttu-id="5c483-259">然後， [**睡眠**](/windows/win32/api/synchapi/nf-synchapi-sleep) 語句可讓系統處理常式的時間處理通知。</span><span class="sxs-lookup"><span data-stu-id="5c483-259">A [**Sleep**](/windows/win32/api/synchapi/nf-synchapi-sleep) statement then allows time for system processes to handle the notification.</span></span>


```C++
void NotifySystemOfNewRegistration()
{
    SHChangeNotify(SHCNE_ASSOCCHANGED, SHCNF_DWORD | SHCNF_FLUSH, nullptr, nullptr);
    Sleep(1000);
}
```



<span data-ttu-id="5c483-260">如果使用者在未進行新的預設瀏覽器選取的情況下，關閉或忽略產生的通知或飛出視窗，預設瀏覽器會維持不變。</span><span class="sxs-lookup"><span data-stu-id="5c483-260">If the user dismisses or ignores the resulting notification or flyout without making a new default browser selection, the default browser remains unchanged.</span></span> <span data-ttu-id="5c483-261">請注意，使用者也可以隨時透過其他機制變更預設瀏覽器，包括主控台中的設定使用者預設值。</span><span class="sxs-lookup"><span data-stu-id="5c483-261">Note that the user can also change the default browser at any time through other mechanisms, including Set User Defaults in the Control Panel.</span></span>

## <a name="default-programs-ui"></a><span data-ttu-id="5c483-262">預設程式 UI</span><span class="sxs-lookup"><span data-stu-id="5c483-262">Default Programs UI</span></span>

<span data-ttu-id="5c483-263">本節中的圖例顯示使用者所見之 **預設程式** 的 UI。</span><span class="sxs-lookup"><span data-stu-id="5c483-263">The illustrations in this section show the UI for **Default Programs** as seen by the user.</span></span>

<span data-ttu-id="5c483-264">下圖顯示主控台中的主要 **預設程式** 視窗。</span><span class="sxs-lookup"><span data-stu-id="5c483-264">The following illustration shows the main **Default Programs** window in Control Panel.</span></span>

![[預設程式] 專案頁面的螢幕擷取畫面](images/defaultprogramsmain.png)

<span data-ttu-id="5c483-266">當使用者選擇 [ **設定您的預設程式** ] 選項時，會出現下列視窗。</span><span class="sxs-lookup"><span data-stu-id="5c483-266">When a user chooses the **Set your default programs** option, the following window appears.</span></span> <span data-ttu-id="5c483-267">使用者可以使用此頁面，為所有檔案類型和通訊協定指派預設程式，此程式是可能的預設程式。</span><span class="sxs-lookup"><span data-stu-id="5c483-267">Users can use this page to assign a default program for all file types and protocols for which the program is a possible default.</span></span> <span data-ttu-id="5c483-268">如下圖所示，所有 [已註冊](#registering-an-application-for-use-with-default-programs) 的程式和程式圖示都會出現在左側的 [ **程式** ] 方塊中。</span><span class="sxs-lookup"><span data-stu-id="5c483-268">As shown in the following illustration, all [registered](#registering-an-application-for-use-with-default-programs) programs and the program icon appear in the **Programs** box on the left.</span></span>

![[設定您的預設程式] 頁面的螢幕擷取畫面](images/setyourdefaultprograms.png)

<span data-ttu-id="5c483-270">當使用者從清單中選取程式時，會顯示程式圖示和提供者。</span><span class="sxs-lookup"><span data-stu-id="5c483-270">When the user selects a program from the list, the program icon and provider are displayed.</span></span> <span data-ttu-id="5c483-271">如果 URL 內嵌在程式的數位簽署憑證中，程式也可以顯示 URL。</span><span class="sxs-lookup"><span data-stu-id="5c483-271">If the URL is embedded in the program's digitally signed certificate, the program can also display a URL.</span></span> <span data-ttu-id="5c483-272">未經過數位簽署的程式無法顯示 URL。</span><span class="sxs-lookup"><span data-stu-id="5c483-272">Programs that are not digitally signed cannot display a URL.</span></span>

<span data-ttu-id="5c483-273">程式在註冊期間提供的描述性文字也會顯示。</span><span class="sxs-lookup"><span data-stu-id="5c483-273">Descriptive text, which is supplied by the program during registration, is also displayed.</span></span> <span data-ttu-id="5c483-274">這是必要文字。</span><span class="sxs-lookup"><span data-stu-id="5c483-274">This text is required.</span></span> <span data-ttu-id="5c483-275">在 [描述] 方塊下方，指出目前已將程式指派給已註冊要處理之完整數位的預設數目。</span><span class="sxs-lookup"><span data-stu-id="5c483-275">Beneath the description box is an indication of how many defaults the program is currently assigned out of the full number it is registered to handle.</span></span>

<span data-ttu-id="5c483-276">若要將程式指派或還原為其註冊的所有檔案和通訊協定的預設值，使用者按一下 [ **將此程式設定為預設值** ]。</span><span class="sxs-lookup"><span data-stu-id="5c483-276">To assign or restore a program as the default for all files and protocols for which it is registered, the user clicks the **Set this program as default** option.</span></span>

<span data-ttu-id="5c483-277">若要將個別的檔案類型和通訊協定指派給程式，使用者可以按一下 [ **選擇此程式的預設值** ] 選項，它會顯示程式視窗的 **設定關聯** ，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="5c483-277">To assign individual file types and protocols to a program, the user clicks the **Choose defaults for this program** option, which displays a **Set associations for a program** window like the one in the following illustration.</span></span>

> [!Note]  
> <span data-ttu-id="5c483-278">建議您使用 [**IApplicationAssociationRegistrationUI：： LaunchAdvancedAssociationUI**](/windows/desktop/api/Shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui)呼叫 **程式的設定關聯**。</span><span class="sxs-lookup"><span data-stu-id="5c483-278">We recommend you call the **Set associations for a program** by using [**IApplicationAssociationRegistrationUI::LaunchAdvancedAssociationUI**](/windows/desktop/api/Shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui).</span></span>

 

![[設定關聯的程式] 頁面的螢幕擷取畫面](images/setassociationsforaprogram.png)

## <a name="best-practices-for-using-default-programs"></a><span data-ttu-id="5c483-280">使用預設程式的最佳作法</span><span class="sxs-lookup"><span data-stu-id="5c483-280">Best Practices for Using Default Programs</span></span>

<span data-ttu-id="5c483-281">本節提供在您註冊應用程式時使用 **預設程式** 的最佳做法指導方針。</span><span class="sxs-lookup"><span data-stu-id="5c483-281">This section provides best practice guidelines for using **Default Programs** when you register applications.</span></span> <span data-ttu-id="5c483-282">它也提供建立應用程式的設計建議，以提供使用者最佳的 **預設程式** 功能。</span><span class="sxs-lookup"><span data-stu-id="5c483-282">It also offers design suggestions for creating an application that provides users with optimal **Default Programs** functionality.</span></span>

### <a name="during-installation"></a><span data-ttu-id="5c483-283">在安裝期間</span><span class="sxs-lookup"><span data-stu-id="5c483-283">During Installation</span></span>

<span data-ttu-id="5c483-284">除了通常會在 Windows XP 下執行的安裝程式之外，Windows Vista 或更新版本的應用程式必須向「 **預設程式** 」功能註冊，才能利用其功能。</span><span class="sxs-lookup"><span data-stu-id="5c483-284">In addition to the installation procedures normally practiced under Windows XP, a Windows Vista or later based application must register with the **Default Programs** feature to take advantage of its functionality.</span></span>

<span data-ttu-id="5c483-285">在安裝期間，執行下列步驟順序。</span><span class="sxs-lookup"><span data-stu-id="5c483-285">Perform the following sequence of steps during installation.</span></span> <span data-ttu-id="5c483-286">步驟1-3 符合 Windows XP 中使用的步驟;步驟4是 Windows Vista 的新功能。</span><span class="sxs-lookup"><span data-stu-id="5c483-286">Steps 1-3 match the steps that were used in Windows XP; step 4 was new in Windows Vista.</span></span>

1.  <span data-ttu-id="5c483-287">安裝必要的二進位檔案。</span><span class="sxs-lookup"><span data-stu-id="5c483-287">Install the necessary binary files.</span></span>
2.  <span data-ttu-id="5c483-288">將 Progid 寫入 HKEY \_ 本機 \_ 電腦。</span><span class="sxs-lookup"><span data-stu-id="5c483-288">Write ProgIDs to HKEY\_LOCAL\_MACHINE.</span></span> <span data-ttu-id="5c483-289">請注意，應用程式必須建立其關聯的應用程式特定 Progid。</span><span class="sxs-lookup"><span data-stu-id="5c483-289">Note that applications must create application-specific ProgIDs for their associations.</span></span>
3.  <span data-ttu-id="5c483-290">如先前 [註冊應用程式以搭配預設程式使用](#registering-an-application-for-use-with-default-programs)所述，使用 **預設程式** 來註冊應用程式。</span><span class="sxs-lookup"><span data-stu-id="5c483-290">Register the application with **Default Programs** as previously explained in [Registering an Application for Use with Default Programs](#registering-an-application-for-use-with-default-programs).</span></span>

### <a name="after-installation"></a><span data-ttu-id="5c483-291">安裝後</span><span class="sxs-lookup"><span data-stu-id="5c483-291">After Installation</span></span>

<span data-ttu-id="5c483-292">本節討論應用程式提示應先對每個使用者呈現其預設選項。</span><span class="sxs-lookup"><span data-stu-id="5c483-292">This section discusses how the application prompt should first present its default options to each user.</span></span> <span data-ttu-id="5c483-293">它也會討論應用程式如何監視其狀態，以做為其可能的關聯和通訊協定的預設值。</span><span class="sxs-lookup"><span data-stu-id="5c483-293">It also discusses how an application can monitor its status as the default for its possible associations and protocols.</span></span>

### <a name="first-run-experiences"></a><span data-ttu-id="5c483-294">首次執行體驗</span><span class="sxs-lookup"><span data-stu-id="5c483-294">First Run Experiences</span></span>

<span data-ttu-id="5c483-295">當使用者第一次執行應用程式時，建議應用程式向使用者顯示通常包含這兩個選項的 UI：</span><span class="sxs-lookup"><span data-stu-id="5c483-295">When the application is run by a user for the first time, it is recommended that the application display UI to the user that typically includes these two choices:</span></span>

-   <span data-ttu-id="5c483-296">接受預設的應用程式設定。</span><span class="sxs-lookup"><span data-stu-id="5c483-296">Accept the default application settings.</span></span> <span data-ttu-id="5c483-297">預設會選取這個選項。</span><span class="sxs-lookup"><span data-stu-id="5c483-297">This option is selected by default.</span></span>
-   <span data-ttu-id="5c483-298">自訂預設的應用程式設定。</span><span class="sxs-lookup"><span data-stu-id="5c483-298">Customize the default application settings.</span></span>

<span data-ttu-id="5c483-299">在 Windows 8 之前，如果使用者接受預設設定，則您的應用程式會呼叫 [**IApplicationAssociationRegistration：： SetAppAsDefaultAll**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-setappasdefaultall)，將安裝期間宣告的所有電腦層級關聯轉換成該使用者的每個使用者設定。</span><span class="sxs-lookup"><span data-stu-id="5c483-299">Prior to Windows 8, if the user accepts the default settings, your application calls [**IApplicationAssociationRegistration::SetAppAsDefaultAll**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-setappasdefaultall), which converts all machine-level associations that are declared during installation to per-user settings for that user.</span></span>

<span data-ttu-id="5c483-300">如果使用者決定自訂設定，您的應用程式就會呼叫 [**IApplicationAssociationRegistrationUI：： LaunchAdvancedAssociationUI**](/windows/desktop/api/Shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui) 來顯示檔案關聯 UI。</span><span class="sxs-lookup"><span data-stu-id="5c483-300">If the user decides to customize the settings, your application calls [**IApplicationAssociationRegistrationUI::LaunchAdvancedAssociationUI**](/windows/desktop/api/Shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui) to display the file association UI.</span></span> <span data-ttu-id="5c483-301">下圖顯示虛構 Litware 媒體播放機的這個視窗。</span><span class="sxs-lookup"><span data-stu-id="5c483-301">The following illustration shows this window for the fictional Litware media player.</span></span>

![litware 的 [設定程式的關聯] 頁面的螢幕擷取畫面](images/setassociationsforaprogramforlitware.png)

<span data-ttu-id="5c483-303">[檔案關聯] 視窗會顯示應用程式註冊的預設值，也會顯示其他延伸模組和通訊協定的目前預設值。</span><span class="sxs-lookup"><span data-stu-id="5c483-303">The file association window shows the defaults that the application registered and also shows the current default for other extensions and protocols.</span></span> <span data-ttu-id="5c483-304">當使用者完成自訂預設值之後，他們會按一下 [ **儲存** ] 按鈕來認可變更。</span><span class="sxs-lookup"><span data-stu-id="5c483-304">After the user finishes customizing their defaults, they click the **Save** button to commit the changes.</span></span> <span data-ttu-id="5c483-305">如果使用者按一下 [ **取消**]，視窗會關閉而不儲存變更。</span><span class="sxs-lookup"><span data-stu-id="5c483-305">If the user clicks **Cancel**, the window closes without saving changes.</span></span>

<span data-ttu-id="5c483-306">您應該將此 UI 用於您的應用程式，而不是建立自己的應用程式。</span><span class="sxs-lookup"><span data-stu-id="5c483-306">You should use this UI for your applications instead of creating your own.</span></span> <span data-ttu-id="5c483-307">如此一來，您就可以儲存先前開發檔案關聯 UI 所需的資源。</span><span class="sxs-lookup"><span data-stu-id="5c483-307">By doing so, you save the resources that were previously required to develop file association UI.</span></span> <span data-ttu-id="5c483-308">您也保證可以正確地儲存關聯。</span><span class="sxs-lookup"><span data-stu-id="5c483-308">You also guarantee that associations are saved correctly.</span></span>

### <a name="set-an-application-to-check-whether-it-is-the-default"></a><span data-ttu-id="5c483-309">設定應用程式以檢查它是否為預設值</span><span class="sxs-lookup"><span data-stu-id="5c483-309">Set an Application to Check Whether It Is the Default</span></span>

> [!Note]  
> <span data-ttu-id="5c483-310">Windows 8 不再支援此功能。</span><span class="sxs-lookup"><span data-stu-id="5c483-310">This is no longer supported as of Windows 8.</span></span>

 

<span data-ttu-id="5c483-311">應用程式通常會在執行時檢查它們是否設定為預設值。</span><span class="sxs-lookup"><span data-stu-id="5c483-311">Applications typically check whether they are set as the default when they are run.</span></span> <span data-ttu-id="5c483-312">藉由呼叫 [**IApplicationAssociationRegistration：： QueryAppIsDefault**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefault) 或 [**IApplicationAssociationRegistration：： QueryAppIsDefaultAll**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefaultall)，設定您的應用程式來進行這項檢查。</span><span class="sxs-lookup"><span data-stu-id="5c483-312">Set your applications to make this check by calling [**IApplicationAssociationRegistration::QueryAppIsDefault**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefault) or [**IApplicationAssociationRegistration::QueryAppIsDefaultAll**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefaultall).</span></span>

<span data-ttu-id="5c483-313">如果應用程式判斷不是預設值，它可能會顯示 UI，詢問使用者是否要接受目前的情況，或將應用程式設為預設值。</span><span class="sxs-lookup"><span data-stu-id="5c483-313">If the application determines that it is not the default, it can present UI that asks the user whether to accept the current situation or to make the application the default.</span></span> <span data-ttu-id="5c483-314">一律在此 UI 中包含選取的核取方塊，並顯示不會再詢問的選項。</span><span class="sxs-lookup"><span data-stu-id="5c483-314">Always include a check box in this UI that is selected by default and that presents the option not to be asked again.</span></span>

> [!Note]  
> <span data-ttu-id="5c483-315">預設值應該是使用者導向的選項。</span><span class="sxs-lookup"><span data-stu-id="5c483-315">The choice of default should be user driven.</span></span> <span data-ttu-id="5c483-316">應用程式永遠不會在不詢問使用者的情況下回收預設值。</span><span class="sxs-lookup"><span data-stu-id="5c483-316">An application should never reclaim a default without asking the user.</span></span>

 

<span data-ttu-id="5c483-317">下圖顯示對話方塊範例。</span><span class="sxs-lookup"><span data-stu-id="5c483-317">The following illustration shows an example dialog box.</span></span>

![[範例] 對話方塊的螢幕擷取畫面](images/notthedefaultui.png)

## <a name="additional-resources"></a><span data-ttu-id="5c483-319">其他資源</span><span class="sxs-lookup"><span data-stu-id="5c483-319">Additional Resources</span></span>

-   [<span data-ttu-id="5c483-320">**IApplicationAssociationRegistration**</span><span class="sxs-lookup"><span data-stu-id="5c483-320">**IApplicationAssociationRegistration**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration)
-   [<span data-ttu-id="5c483-321">**IApplicationAssociationRegistrationUI**</span><span class="sxs-lookup"><span data-stu-id="5c483-321">**IApplicationAssociationRegistrationUI**</span></span>](/windows/desktop/api/Shobjidl/nn-shobjidl-iapplicationassociationregistrationui)

## <a name="related-topics"></a><span data-ttu-id="5c483-322">相關主題</span><span class="sxs-lookup"><span data-stu-id="5c483-322">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c483-323">檔案關聯的最佳作法</span><span class="sxs-lookup"><span data-stu-id="5c483-323">Best Practices for File Associations</span></span>](fa-best-practices.md)
</dt> <dt>

[<span data-ttu-id="5c483-324">檔案關聯範例案例</span><span class="sxs-lookup"><span data-stu-id="5c483-324">File Association Sample Scenario</span></span>](fa-sample-scenarios.md)
</dt> <dt>

[<span data-ttu-id="5c483-325">在 Windows Vista 和更新版本中管理預設應用程式的指導方針</span><span class="sxs-lookup"><span data-stu-id="5c483-325">Guidelines for Managing Default Applications in Windows Vista and Later</span></span>](vista-managing-defaults.md)
</dt> <dt>

[<span data-ttu-id="5c483-326"> (SPAD) 設定程式存取和電腦預設值 </span><span class="sxs-lookup"><span data-stu-id="5c483-326">Set Program Access and Computer Defaults (SPAD)</span></span>](cpl-setprogramaccess.md)
</dt> </dl>

 

 

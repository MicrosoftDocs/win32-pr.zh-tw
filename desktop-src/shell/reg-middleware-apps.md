---
description: 本主題說明如何在 Windows 登錄中註冊程式，作為下列其中一種用戶端類型：瀏覽器、電子郵件、媒體播放、立即訊息或適用于 JAVA 的虛擬機器。
title: 使用用戶端類型註冊程式
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 33fcb63c-3db2-44df-acfe-8c88e2e634e4
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 71dd4e3192dc75821fd0a3e8c0d4742e1a8d571a
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "103853511"
---
# <a name="registering-programs-with-client-types"></a><span data-ttu-id="b8363-103">使用用戶端類型註冊程式</span><span class="sxs-lookup"><span data-stu-id="b8363-103">Registering Programs with Client Types</span></span>

<span data-ttu-id="b8363-104">本主題說明如何在 Windows 登錄中註冊程式，作為下列其中一種用戶端類型：瀏覽器、電子郵件、媒體播放、立即訊息或適用于 JAVA 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="b8363-104">This topic explains how to register a program in the Windows registry as one of the following client types: browser, email, media playback, instant messaging, or virtual machine for Java.</span></span>

> [!Note]  
> <span data-ttu-id="b8363-105">這項資訊適用于下列作業系統：</span><span class="sxs-lookup"><span data-stu-id="b8363-105">This information applies to the following operating systems:</span></span>
> 
> -   <span data-ttu-id="b8363-106">Windows 2000 Service Pack 3 (SP3) </span><span class="sxs-lookup"><span data-stu-id="b8363-106">Windows 2000 Service Pack 3 (SP3)</span></span>
> -   <span data-ttu-id="b8363-107">Windows 2000 Service Pack 4 (SP4) </span><span class="sxs-lookup"><span data-stu-id="b8363-107">Windows 2000 Service Pack 4 (SP4)</span></span>
> -   <span data-ttu-id="b8363-108">Windows XP Service Pack 1 (SP1) </span><span class="sxs-lookup"><span data-stu-id="b8363-108">Windows XP Service Pack 1 (SP1)</span></span>
> -   <span data-ttu-id="b8363-109">Windows XP Service Pack 2 (SP2) </span><span class="sxs-lookup"><span data-stu-id="b8363-109">Windows XP Service Pack 2 (SP2)</span></span>
> -   <span data-ttu-id="b8363-110">Windows XP Service Pack 3 (SP3) </span><span class="sxs-lookup"><span data-stu-id="b8363-110">Windows XP Service Pack 3 (SP3)</span></span>
> -   <span data-ttu-id="b8363-111">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b8363-111">Windows Server 2003</span></span>
> -   <span data-ttu-id="b8363-112">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b8363-112">Windows Vista</span></span>
> -   <span data-ttu-id="b8363-113">Windows Vista Service Pack 1 (SP1) </span><span class="sxs-lookup"><span data-stu-id="b8363-113">Windows Vista Service Pack 1 (SP1)</span></span>
> -   <span data-ttu-id="b8363-114">Windows 8</span><span class="sxs-lookup"><span data-stu-id="b8363-114">Windows 8</span></span>

 

<span data-ttu-id="b8363-115">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="b8363-115">This topic includes the following sections.</span></span>

-   [<span data-ttu-id="b8363-116">所有用戶端類型的一般註冊元素</span><span class="sxs-lookup"><span data-stu-id="b8363-116">Common Registration Elements for All Client Types</span></span>](#common-registration-elements-for-all-client-types)
    -   [<span data-ttu-id="b8363-117">選取正式名稱</span><span class="sxs-lookup"><span data-stu-id="b8363-117">Selecting a Canonical Name</span></span>](#selecting-a-canonical-name)
    -   [<span data-ttu-id="b8363-118">註冊程式的顯示名稱</span><span class="sxs-lookup"><span data-stu-id="b8363-118">Registering a Program's Display Name</span></span>](#registering-a-programs-display-name)
    -   [<span data-ttu-id="b8363-119">註冊程式的圖示</span><span class="sxs-lookup"><span data-stu-id="b8363-119">Registering a Program's Icon</span></span>](#registering-a-programs-icon)
    -   [<span data-ttu-id="b8363-120">註冊開啟的動詞</span><span class="sxs-lookup"><span data-stu-id="b8363-120">Registering an Open Verb</span></span>](#registering-an-open-verb)
    -   [<span data-ttu-id="b8363-121">註冊安裝資訊</span><span class="sxs-lookup"><span data-stu-id="b8363-121">Registering Installation Information</span></span>](#registering-installation-information)
-   [<span data-ttu-id="b8363-122">特定用戶端類型的註冊元素</span><span class="sxs-lookup"><span data-stu-id="b8363-122">Registration Elements for Specific Client Types</span></span>](#registration-elements-for-specific-client-types)
    -   [<span data-ttu-id="b8363-123">開始功能表註冊</span><span class="sxs-lookup"><span data-stu-id="b8363-123">Start Menu Registration</span></span>](#start-menu-registration)
    -   [<span data-ttu-id="b8363-124">郵件用戶端註冊</span><span class="sxs-lookup"><span data-stu-id="b8363-124">Mail Client Registration</span></span>](#mail-client-registration)
-   [<span data-ttu-id="b8363-125">完成範例註冊</span><span class="sxs-lookup"><span data-stu-id="b8363-125">Complete Sample Registrations</span></span>](#complete-sample-registrations)
    -   [<span data-ttu-id="b8363-126">範例瀏覽器</span><span class="sxs-lookup"><span data-stu-id="b8363-126">A Sample Browser</span></span>](#a-sample-browser)
    -   [<span data-ttu-id="b8363-127">範例郵件瀏覽器</span><span class="sxs-lookup"><span data-stu-id="b8363-127">A Sample Mail Browser</span></span>](#a-sample-mail-browser)
    -   [<span data-ttu-id="b8363-128">範例媒體播放機</span><span class="sxs-lookup"><span data-stu-id="b8363-128">A Sample Media Player</span></span>](#a-sample-media-player)
    -   [<span data-ttu-id="b8363-129">範例即時 Messenger 程式</span><span class="sxs-lookup"><span data-stu-id="b8363-129">A Sample Instant Messenger Program</span></span>](#a-sample-instant-messenger-program)
    -   [<span data-ttu-id="b8363-130">適用于 JAVA 的虛擬機器範例</span><span class="sxs-lookup"><span data-stu-id="b8363-130">A Sample Virtual Machine for Java</span></span>](#a-sample-virtual-machine-for-java)
-   [<span data-ttu-id="b8363-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="b8363-131">Related topics</span></span>](#related-topics)

<span data-ttu-id="b8363-132">本主題會擴充現有的檔，將程式註冊為特定的用戶端類型。</span><span class="sxs-lookup"><span data-stu-id="b8363-132">This topic extends existing documentation about registering a program as a particular client type.</span></span> <span data-ttu-id="b8363-133">如需該檔的連結，請參閱相關主題一節。</span><span class="sxs-lookup"><span data-stu-id="b8363-133">For links to that documentation, see the Related Topics section.</span></span>

## <a name="common-registration-elements-for-all-client-types"></a><span data-ttu-id="b8363-134">所有用戶端類型的一般註冊元素</span><span class="sxs-lookup"><span data-stu-id="b8363-134">Common Registration Elements for All Client Types</span></span>

<span data-ttu-id="b8363-135">將程式註冊為用戶端類型時，無論用戶端類型為何，大部分的登錄專案都相同。</span><span class="sxs-lookup"><span data-stu-id="b8363-135">When registering a program as a client type, most of the registry entries are the same regardless of the client type.</span></span> <span data-ttu-id="b8363-136">不過，某些登錄專案是用戶端類型專屬的，而且這些專案會在 [ [特定用戶端類型的註冊元素](#registration-elements-for-specific-client-types) ] 區段中注明。</span><span class="sxs-lookup"><span data-stu-id="b8363-136">Some registry entries, however, are specific to the client type and these are noted in the [Registration Elements for Specific Client Types](#registration-elements-for-specific-client-types) section.</span></span>

<span data-ttu-id="b8363-137">本節將討論下列主題：</span><span class="sxs-lookup"><span data-stu-id="b8363-137">This section discusses the following topics:</span></span>

-   [<span data-ttu-id="b8363-138">選取正式名稱</span><span class="sxs-lookup"><span data-stu-id="b8363-138">Selecting a Canonical Name</span></span>](#selecting-a-canonical-name)
-   [<span data-ttu-id="b8363-139">註冊程式的顯示名稱</span><span class="sxs-lookup"><span data-stu-id="b8363-139">Registering a Program's Display Name</span></span>](#registering-a-programs-display-name)
-   [<span data-ttu-id="b8363-140">註冊程式的圖示</span><span class="sxs-lookup"><span data-stu-id="b8363-140">Registering a Program's Icon</span></span>](#registering-a-programs-icon)
-   [<span data-ttu-id="b8363-141">註冊開啟的動詞</span><span class="sxs-lookup"><span data-stu-id="b8363-141">Registering an Open Verb</span></span>](#registering-an-open-verb)
-   [<span data-ttu-id="b8363-142">註冊安裝資訊</span><span class="sxs-lookup"><span data-stu-id="b8363-142">Registering Installation Information</span></span>](#registering-installation-information)

> [!Note]  
> <span data-ttu-id="b8363-143">在本主題中，以斜體指定的子機碼名稱是使用者定義子機碼名稱或一組可能值的預留位置。</span><span class="sxs-lookup"><span data-stu-id="b8363-143">Subkey names given in italics throughout this topic are placeholders for user-defined subkey names or a set of possible values.</span></span> <span data-ttu-id="b8363-144">[完整範例註冊](#complete-sample-registrations)一節中提供了完整的範例名稱範例。</span><span class="sxs-lookup"><span data-stu-id="b8363-144">Full examples with example names in place are provided in the [Complete Sample Registrations](#complete-sample-registrations) section.</span></span>

 

<span data-ttu-id="b8363-145">所有用戶端類型註冊資訊都會儲存在下列子機碼底下：</span><span class="sxs-lookup"><span data-stu-id="b8363-145">All client type registration information is stored under the following subkey:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
```

<span data-ttu-id="b8363-146">*ClientTypeName* 是下列其中一個子機碼名稱：</span><span class="sxs-lookup"><span data-stu-id="b8363-146">*ClientTypeName* is one of the following subkey names:</span></span>

-   <span data-ttu-id="b8363-147">瀏覽器的 StartMenuInternet () </span><span class="sxs-lookup"><span data-stu-id="b8363-147">StartMenuInternet (for browsers)</span></span>
-   <span data-ttu-id="b8363-148">電子郵件) 的郵件 (</span><span class="sxs-lookup"><span data-stu-id="b8363-148">Mail (for email)</span></span>
-   <span data-ttu-id="b8363-149">媒體播放) 媒體 (</span><span class="sxs-lookup"><span data-stu-id="b8363-149">Media (for media playback)</span></span>
-   <span data-ttu-id="b8363-150">立即訊息) 的 IM (</span><span class="sxs-lookup"><span data-stu-id="b8363-150">IM (for instant messaging)</span></span>
-   <span data-ttu-id="b8363-151">適用于 JAVA) 的虛擬機器 JAVAVM (</span><span class="sxs-lookup"><span data-stu-id="b8363-151">JavaVM (for virtual machine for Java)</span></span>

<span data-ttu-id="b8363-152">在本主題中，您將會看到名為 "Litware Inc." 的虛構電腦程式的參考，其中包含名為 Litview.exe 的可執行檔。</span><span class="sxs-lookup"><span data-stu-id="b8363-152">Throughout this topic, you will note references to a fictional computer program named "Lit View" by Litware Inc., with an executable file named Litview.exe.</span></span> <span data-ttu-id="b8363-153">這項假設性的程式是為了方便說明，可交換為立即 messenger、瀏覽器或其他類型的用戶端程式。</span><span class="sxs-lookup"><span data-stu-id="b8363-153">This hypothetical program is used interchangeably as an instant messenger, a browser, or another type of client program as needed for illustrative purposes.</span></span>

### <a name="selecting-a-canonical-name"></a><span data-ttu-id="b8363-154">選取正式名稱</span><span class="sxs-lookup"><span data-stu-id="b8363-154">Selecting a Canonical Name</span></span>

<span data-ttu-id="b8363-155">廠商必須選擇程式的 *標準名稱* 。</span><span class="sxs-lookup"><span data-stu-id="b8363-155">The vendor must choose a *canonical name* for the program.</span></span> <span data-ttu-id="b8363-156">標準名稱永遠不會向使用者顯示，因此不需要當地語系化。</span><span class="sxs-lookup"><span data-stu-id="b8363-156">The canonical name is never shown to the user, so it does not need to be localized.</span></span> <span data-ttu-id="b8363-157">其唯一目的是提供可用來識別程式的唯一字串。</span><span class="sxs-lookup"><span data-stu-id="b8363-157">Its only purpose is to provide a unique string that can be used to identify the program.</span></span> <span data-ttu-id="b8363-158">它通常會與程式的英文名稱相同，但這只是一種慣例。</span><span class="sxs-lookup"><span data-stu-id="b8363-158">It is typically the same as the English name of the program, but this is merely a convention.</span></span>

<span data-ttu-id="b8363-159">針對瀏覽器以外的用戶端類型，標準名稱可以是任何字串。</span><span class="sxs-lookup"><span data-stu-id="b8363-159">For client types other than browsers, the canonical name can be any string.</span></span> <span data-ttu-id="b8363-160">選擇一個不太可能由另一個廠商使用的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="b8363-160">Choose a unique name, one that is not likely to be used by another vendor.</span></span>

<span data-ttu-id="b8363-161">針對瀏覽器用戶端，正式名稱必須是相關聯可執行檔的名稱（包括副檔名）;例如，"Litview.exe"。</span><span class="sxs-lookup"><span data-stu-id="b8363-161">For browser clients, the canonical name must be the name—including the extension—of the associated executable; for instance, "Litview.exe".</span></span>

<span data-ttu-id="b8363-162">以下是標準名稱的一些範例。</span><span class="sxs-lookup"><span data-stu-id="b8363-162">Here are some examples of canonical names.</span></span>

-   <span data-ttu-id="b8363-163">Iexplore.exe (瀏覽器) </span><span class="sxs-lookup"><span data-stu-id="b8363-163">Iexplore.exe (browser)</span></span>
-   <span data-ttu-id="b8363-164">Windows Mail (電子郵件) </span><span class="sxs-lookup"><span data-stu-id="b8363-164">Windows Mail (email)</span></span>
-   <span data-ttu-id="b8363-165">Windows Media Player (媒體) </span><span class="sxs-lookup"><span data-stu-id="b8363-165">Windows Media Player (media)</span></span>
-   <span data-ttu-id="b8363-166">Windows Messenger (立即訊息) </span><span class="sxs-lookup"><span data-stu-id="b8363-166">Windows Messenger (instant messaging)</span></span>

<span data-ttu-id="b8363-167">建立子機碼以註冊正式名稱，如下所示。</span><span class="sxs-lookup"><span data-stu-id="b8363-167">Register the canonical name by creating a subkey as shown here.</span></span> <span data-ttu-id="b8363-168">子機碼的名稱是標準名稱。</span><span class="sxs-lookup"><span data-stu-id="b8363-168">The name of the subkey is the canonical name.</span></span> <span data-ttu-id="b8363-169">與該程式註冊相關的所有資訊都會存在於此子機碼底下。</span><span class="sxs-lookup"><span data-stu-id="b8363-169">All information relating to that program's registration will exist under this subkey.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
```

### <a name="registering-a-programs-display-name"></a><span data-ttu-id="b8363-170">註冊程式的顯示名稱</span><span class="sxs-lookup"><span data-stu-id="b8363-170">Registering a Program's Display Name</span></span>

<span data-ttu-id="b8363-171">註冊的下一步是指定程式的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="b8363-171">The next step in registration is to specify the program's display name.</span></span> <span data-ttu-id="b8363-172">它會以標準名稱索引鍵的形式提供值，如下所示。</span><span class="sxs-lookup"><span data-stu-id="b8363-172">It is given as a value under the canonical name key as shown here.</span></span> <span data-ttu-id="b8363-173">請再次注意， *CanonicalName* 和 *ClientTypeName* 不是索引鍵的實際名稱，而是只有真正名稱的預留位置，例如 *亮視圖*。</span><span class="sxs-lookup"><span data-stu-id="b8363-173">Note again that *CanonicalName* and *ClientTypeName* are not the actual names of the keys, but only placeholders for the true names, such as *Lit View*.</span></span>

> [!Note]  
> <span data-ttu-id="b8363-174">從 Windows 8，用來註冊 [設定程式存取和電腦預設值的名稱 (SPAD) ](cpl-setprogramaccess.md) 和 [預設程式](default-programs.md) 應該相符，才能讓 SPAD 變更觸發預設程式註冊。</span><span class="sxs-lookup"><span data-stu-id="b8363-174">As of Windows 8, the name used to register for [Set Program Access and Computer Defaults (SPAD)](cpl-setprogramaccess.md) and for [Default Programs](default-programs.md) should match in order for SPAD changes to trigger Default Programs registrations.</span></span>

 

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               LocalizedString = @FilePath,-StringID
```

<span data-ttu-id="b8363-175">**>localizedstring** 值是 REG \_ SZ 字串，其中包含 "at" 符號 ( @ ) 、.dll 或 .exe 檔案的完整路徑、逗號、減號和十進位整數。</span><span class="sxs-lookup"><span data-stu-id="b8363-175">The **LocalizedString** value is a REG\_SZ string and consists of an "at" sign (@), the full path to a .dll or .exe file, a comma, a minus sign, and a decimal integer.</span></span> <span data-ttu-id="b8363-176">十進位整數是字串資源的識別碼（包含在 .dll 或 .exe 檔案中），其值會以此用戶端的名稱顯示給使用者。</span><span class="sxs-lookup"><span data-stu-id="b8363-176">The decimal integer is the ID of a string resource—contained within the .dll or .exe file—whose value is to be displayed to the user as the name of this client.</span></span> <span data-ttu-id="b8363-177">請注意，即使檔案路徑包含空格，也不需要加上引號。</span><span class="sxs-lookup"><span data-stu-id="b8363-177">Note that the file path does not require quotation marks, even if it contains spaces.</span></span>

<span data-ttu-id="b8363-178">以這種方式註冊顯示名稱字串，可讓相同的註冊用於多種語言。</span><span class="sxs-lookup"><span data-stu-id="b8363-178">Registering the display name string in this manner allows the same registration to be used for multiple languages.</span></span> <span data-ttu-id="b8363-179">每個語言安裝都會提供不同的資源檔，並以相同的資源識別碼儲存顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="b8363-179">Each language installation provides a different resource file with the display name stored at the same resource ID.</span></span>

<span data-ttu-id="b8363-180">下列範例顯示虛構的「立即查看」立即訊息程式的註冊。</span><span class="sxs-lookup"><span data-stu-id="b8363-180">The following example shows the registration for a fictional Lit View instant messaging program.</span></span> <span data-ttu-id="b8363-181">因為這是立即訊息程式，所以在此案例中， *CanonicalName* 子機碼 (在 **IM** 子機 *碼下)* 。</span><span class="sxs-lookup"><span data-stu-id="b8363-181">Because it is an instant messaging program, the *CanonicalName* subkey (in this case *Lit View*) is stored under the **IM** subkey.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         IM
            Lit View
               (Default) = Lit View
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
```

<span data-ttu-id="b8363-182">請注意，使用 (預設) 專案做為用戶端顯示名稱的次要宣告。</span><span class="sxs-lookup"><span data-stu-id="b8363-182">Note the use of the (Default) entry as a secondary declaration of the client's display name.</span></span> <span data-ttu-id="b8363-183">如果 **>localizedstring** 不存在，則會改用 (預設) 值。</span><span class="sxs-lookup"><span data-stu-id="b8363-183">If the **LocalizedString** is not present, the (Default) value is used instead.</span></span> <span data-ttu-id="b8363-184">這適用于所有用戶端類型 (的網際網路瀏覽器、電子郵件瀏覽器、即時 messengers 和媒體播放機) 。</span><span class="sxs-lookup"><span data-stu-id="b8363-184">This works with all client types (Internet browsers, email browsers, instant messengers, and media players).</span></span> <span data-ttu-id="b8363-185">為了與 [Internet Explorer 用戶端](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa753633(v=vs.85))登錄配置相容，電子郵件程式應將 *CanonicalName* 子機碼 (預設) 值設定為目前安裝之語言的用戶端顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="b8363-185">For backward compatibility with the [Internet Explorer Client Registry Layout](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa753633(v=vs.85)), email programs should set the (Default) value of the *CanonicalName* subkey to the client's display name in the currently installed language.</span></span>

### <a name="registering-a-programs-icon"></a><span data-ttu-id="b8363-186">註冊程式的圖示</span><span class="sxs-lookup"><span data-stu-id="b8363-186">Registering a Program's Icon</span></span>

> [!Note]  
> <span data-ttu-id="b8363-187">本節不適用 Windows 2000。</span><span class="sxs-lookup"><span data-stu-id="b8363-187">This section does not apply to Windows 2000.</span></span>

 

<span data-ttu-id="b8363-188">依預設，Windows XP 和 Windows Vista [ **開始** ] 功能表的上方區段包含 [ **網際網路** ] 和 [ **電子郵件** ] 圖示。</span><span class="sxs-lookup"><span data-stu-id="b8363-188">By default, the upper section of the Windows XP and Windows Vista **Start** menu contains **Internet** and **E-mail** icons.</span></span> <span data-ttu-id="b8363-189">這些圖示不會出現在 Windows 7 和更新版本中。</span><span class="sxs-lookup"><span data-stu-id="b8363-189">These icons are not present in Windows 7 and later.</span></span> <span data-ttu-id="b8363-190">針對瀏覽器和電子郵件客戶程式，將程式指派為其用戶端類型的預設值時，會針對這些 [ **開始** ] 功能表項目顯示該程式的註冊圖示。</span><span class="sxs-lookup"><span data-stu-id="b8363-190">For browser and email clients, when a program is assigned as the default for their client type, that program's registered icon is displayed for those **Start** menu entries.</span></span>

<span data-ttu-id="b8363-191">瀏覽器和電子郵件客戶程式都必須註冊程式的圖示。</span><span class="sxs-lookup"><span data-stu-id="b8363-191">Registering a program's icon is mandatory for browser and email clients.</span></span> <span data-ttu-id="b8363-192">註冊媒體播放、即時消息或適用于 JAVA 用戶端類型的虛擬機器的圖示是選擇性的，而這些用戶端類型的註冊圖示目前不是由 Windows 使用，且不會顯示在 Windows XP 或 Windows Vista [ **開始** ] 功能表的上方區段中。</span><span class="sxs-lookup"><span data-stu-id="b8363-192">Registering an icon for the media playback, instant messaging, or virtual machine for Java client types is optional, and registered icons for those client types are not currently used by Windows and are not displayed in the upper section of the Windows XP or Windows Vista **Start** menus.</span></span>

<span data-ttu-id="b8363-193">若要註冊用戶端程式的圖示，請新增具有預設值的 **DefaultIcon** 子機碼，如下所示。</span><span class="sxs-lookup"><span data-stu-id="b8363-193">To register an icon for a client program, add a **DefaultIcon** subkey with a default value as shown here.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               DefaultIcon
                  (Default) = FilePath,IconIndex
```

<span data-ttu-id="b8363-194">**FilePath** 值是包含圖示之檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="b8363-194">The **FilePath** value is the full path to the file that contains the icon.</span></span> <span data-ttu-id="b8363-195">即使此路徑包含空格，也不需要引號。</span><span class="sxs-lookup"><span data-stu-id="b8363-195">This path does not require quotation marks, even if it contains spaces.</span></span>

<span data-ttu-id="b8363-196">**>iconindex** 值的解釋如下：</span><span class="sxs-lookup"><span data-stu-id="b8363-196">The **IconIndex** value is interpreted as follows:</span></span>

-   <span data-ttu-id="b8363-197">如果 **>iconindex** 是正數，則會使用數位作為儲存在檔案中之以 *零為基* 底之圖示陣列的索引。</span><span class="sxs-lookup"><span data-stu-id="b8363-197">If **IconIndex** is a positive number, the number is used as the index of the *zero-based* array of icons stored in the file.</span></span> <span data-ttu-id="b8363-198">例如，如果 **>iconindex** 是1，則會從檔案載入第二個圖示。</span><span class="sxs-lookup"><span data-stu-id="b8363-198">For example, if **IconIndex** is 1, the second icon is loaded from the file.</span></span>
-   <span data-ttu-id="b8363-199">如果 **>iconindex** 為負數，則會使用 **>iconindex** 的絕對值作為資源識別碼 (而不是圖示的索引) 。</span><span class="sxs-lookup"><span data-stu-id="b8363-199">If **IconIndex** is a negative number, the absolute value of **IconIndex** is used as the resource identifier (rather than the index) for the icon.</span></span> <span data-ttu-id="b8363-200">例如，如果 **>iconindex** 為-3，則會從檔案載入其資源識別碼為3的圖示。</span><span class="sxs-lookup"><span data-stu-id="b8363-200">For example, if **IconIndex** is -3, the icon whose resource identifier is 3 is loaded from the file.</span></span>

<span data-ttu-id="b8363-201">下列範例示範如何註冊假設性的視圖瀏覽器。</span><span class="sxs-lookup"><span data-stu-id="b8363-201">The following example shows the registration of a hypothetical Lit View browser.</span></span> <span data-ttu-id="b8363-202">Litview.exe 檔案中儲存的第二個圖示會用來做為預設值。</span><span class="sxs-lookup"><span data-stu-id="b8363-202">The second icon stored in the Litview.exe file is used as the default.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         StartMenuInternet
            LITVIEW.EXE
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\Litview.exe,1
```

### <a name="registering-an-open-verb"></a><span data-ttu-id="b8363-203">註冊開啟的動詞</span><span class="sxs-lookup"><span data-stu-id="b8363-203">Registering an Open Verb</span></span>

> [!Note]  
> <span data-ttu-id="b8363-204">本節不適用 Windows 2000。</span><span class="sxs-lookup"><span data-stu-id="b8363-204">This section does not apply to Windows 2000.</span></span> <span data-ttu-id="b8363-205">下列步驟僅適用于瀏覽器和電子郵件客戶程式。</span><span class="sxs-lookup"><span data-stu-id="b8363-205">The following step is necessary only for browser and email clients.</span></span>

 

<span data-ttu-id="b8363-206">假設使用者已選取您的程式做為預設網際網路或電子郵件程式。</span><span class="sxs-lookup"><span data-stu-id="b8363-206">Assume that a user has selected your program as the default Internet or email program.</span></span> <span data-ttu-id="b8363-207">該使用者按一下 Windows XP 或 Windows Vista [**開始**] 功能表中的 [**網際網路**] 或 [**電子郵件**] 圖示，以開啟程式。</span><span class="sxs-lookup"><span data-stu-id="b8363-207">That user clicks the **Internet** or **E-mail** icon in the Windows XP or Windows Vista **Start** menu to open the program.</span></span> <span data-ttu-id="b8363-208">此時會執行已註冊的命令列，如下所示。</span><span class="sxs-lookup"><span data-stu-id="b8363-208">At that point, the command line registered as shown here is executed.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               shell
                  open
                     command
                        (Default) = command line
```

<span data-ttu-id="b8363-209">命令列必須指定檔案的完整絕對路徑，後面接著選擇性的命令列選項。</span><span class="sxs-lookup"><span data-stu-id="b8363-209">The command line must specify a fully qualified absolute path to the file, followed by optional command-line options.</span></span> <span data-ttu-id="b8363-210">如果專案類型是 REG \_ EXPAND \_ SZ，則環境變數可以在路徑中使用。</span><span class="sxs-lookup"><span data-stu-id="b8363-210">If the entry type is REG\_EXPAND\_SZ, environment variables can be used in the path.</span></span> <span data-ttu-id="b8363-211">適當地使用引號，以確保命令列中的空格不會誤解。</span><span class="sxs-lookup"><span data-stu-id="b8363-211">Use quotation marks appropriately to ensure that spaces in the command line are not misinterpreted.</span></span> <span data-ttu-id="b8363-212">命令列應該以適當的預設值執行程式。</span><span class="sxs-lookup"><span data-stu-id="b8363-212">The command line should execute the program with appropriate defaults.</span></span> <span data-ttu-id="b8363-213">瀏覽器通常預設為使用者的首頁。</span><span class="sxs-lookup"><span data-stu-id="b8363-213">Browsers generally default to the user's home page.</span></span> <span data-ttu-id="b8363-214">電子郵件程式通常會開啟使用者的 **收件** 匣。</span><span class="sxs-lookup"><span data-stu-id="b8363-214">Email programs generally open the user's **Inbox**.</span></span>

<span data-ttu-id="b8363-215">下列範例會示範如何註冊 `open` 假想亮 View 瀏覽器的動詞。</span><span class="sxs-lookup"><span data-stu-id="b8363-215">The following example shows the registration of an `open` verb for a hypothetical Lit View browser.</span></span> <span data-ttu-id="b8363-216">它不會指定任何命令列選項。</span><span class="sxs-lookup"><span data-stu-id="b8363-216">It specifies no command-line options.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         StartMenuInternet
            LITVIEW.EXE
               shell
                  open
                     command
                        (Default) = "C:\Program Files\LitwareInc\Litview.exe"
```

<span data-ttu-id="b8363-217">請注意，在此值中，引號是放在路徑周圍，因為它包含內嵌的空格。</span><span class="sxs-lookup"><span data-stu-id="b8363-217">Note that in this value, quotation marks are placed around the path because it contains embedded spaces.</span></span> <span data-ttu-id="b8363-218">省略這些引號可能會導致命令列被誤解。</span><span class="sxs-lookup"><span data-stu-id="b8363-218">Omitting these quotation marks could cause the command line to be misinterpreted.</span></span>

### <a name="registering-installation-information"></a><span data-ttu-id="b8363-219">註冊安裝資訊</span><span class="sxs-lookup"><span data-stu-id="b8363-219">Registering Installation Information</span></span>

> [!Note]  
> <span data-ttu-id="b8363-220">本節不適用 Windows Server 2003。</span><span class="sxs-lookup"><span data-stu-id="b8363-220">This section does not apply to Windows Server 2003.</span></span>

 

-   [<span data-ttu-id="b8363-221">重新安裝命令</span><span class="sxs-lookup"><span data-stu-id="b8363-221">The Reinstall Command</span></span>](#the-reinstall-command)
-   [<span data-ttu-id="b8363-222">隱藏圖示命令</span><span class="sxs-lookup"><span data-stu-id="b8363-222">The Hide Icons Command</span></span>](#the-hide-icons-command)
-   [<span data-ttu-id="b8363-223">顯示圖示命令</span><span class="sxs-lookup"><span data-stu-id="b8363-223">The Show Icons Command</span></span>](#the-show-icons-command)
-   [<span data-ttu-id="b8363-224">組程式設定</span><span class="sxs-lookup"><span data-stu-id="b8363-224">Group Program Configuration</span></span>](#group-program-configuration)
-   [<span data-ttu-id="b8363-225">瀏覽器註冊範例</span><span class="sxs-lookup"><span data-stu-id="b8363-225">Browser Registration Example</span></span>](#browser-registration-example)

<span data-ttu-id="b8363-226">使用者選取個別電腦預設程式的功能，如下表所示進行命名和存取。</span><span class="sxs-lookup"><span data-stu-id="b8363-226">The feature by which the user selects per-machine default programs is named and accessed as shown in the following table.</span></span> <span data-ttu-id="b8363-227"> (Windows Vista 引進了一項新功能，就是 **設定您的預設程式，讓** 使用者可以設定依使用者的預設值。 ) </span><span class="sxs-lookup"><span data-stu-id="b8363-227">(Windows Vista introduced a new feature, **Set your default programs**, by which a user can set per-user defaults.)</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b8363-228">作業系統</span><span class="sxs-lookup"><span data-stu-id="b8363-228">Operating System</span></span></th>
<th><span data-ttu-id="b8363-229">標題</span><span class="sxs-lookup"><span data-stu-id="b8363-229">Title</span></span></th>
<th><span data-ttu-id="b8363-230">存取位置</span><span class="sxs-lookup"><span data-stu-id="b8363-230">Access Location</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b8363-231">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b8363-231">Windows 7</span></span></td>
<td><span data-ttu-id="b8363-232">設定程式存取和電腦預設值</span><span class="sxs-lookup"><span data-stu-id="b8363-232">Set Program Access and Computer Defaults</span></span></td>
<td><ul>
<li><span data-ttu-id="b8363-233"><strong>開始</strong> 功能表 <strong>預設程式</strong> 選項</span><span class="sxs-lookup"><span data-stu-id="b8363-233"><strong>Start</strong> menu <strong>Default Programs</strong> option</span></span></li>
<li><span data-ttu-id="b8363-234"><strong>預設程式</strong> 主控台專案</span><span class="sxs-lookup"><span data-stu-id="b8363-234"><strong>Default Programs</strong> Control Panel item</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b8363-235">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b8363-235">Windows Vista</span></span></td>
<td><span data-ttu-id="b8363-236">設定程式存取和電腦預設值</span><span class="sxs-lookup"><span data-stu-id="b8363-236">Set Program Access and Computer Defaults</span></span></td>
<td><ul>
<li><span data-ttu-id="b8363-237"><strong>開始</strong> 功能表 <strong>預設程式</strong> 選項</span><span class="sxs-lookup"><span data-stu-id="b8363-237"><strong>Start</strong> menu <strong>Default Programs</strong> option</span></span></li>
<li><span data-ttu-id="b8363-238"><strong>預設程式</strong> 主控台專案</span><span class="sxs-lookup"><span data-stu-id="b8363-238"><strong>Default Programs</strong> Control Panel item</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b8363-239">Windows XP SP2</span><span class="sxs-lookup"><span data-stu-id="b8363-239">Windows XP SP2</span></span></td>
<td><span data-ttu-id="b8363-240">設定程式存取和預設值</span><span class="sxs-lookup"><span data-stu-id="b8363-240">Set Program Access and Defaults</span></span></td>
<td><ul>
<li><span data-ttu-id="b8363-241"><strong>開始</strong> 功能表</span><span class="sxs-lookup"><span data-stu-id="b8363-241"><strong>Start</strong> menu</span></span></li>
<li><span data-ttu-id="b8363-242"><strong>新增或移除程式</strong> 主控台專案</span><span class="sxs-lookup"><span data-stu-id="b8363-242"><strong>Add or Remove Programs</strong> Control Panel item</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b8363-243">Windows XP SP1</span><span class="sxs-lookup"><span data-stu-id="b8363-243">Windows XP SP1</span></span></td>
<td><span data-ttu-id="b8363-244">設定程式</span><span class="sxs-lookup"><span data-stu-id="b8363-244">Configure Programs</span></span></td>
<td><ul>
<li><span data-ttu-id="b8363-245"><strong>新增或移除程式</strong> 主控台專案</span><span class="sxs-lookup"><span data-stu-id="b8363-245"><strong>Add or Remove Programs</strong> Control Panel item</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="b8363-246">為了簡單起見，本主題使用功能的 Windows 7 標題。</span><span class="sxs-lookup"><span data-stu-id="b8363-246">For simplicity, this topic uses the Windows 7 title of the feature.</span></span> <span data-ttu-id="b8363-247">所有版本的功能也就一般稱為 SPAD。</span><span class="sxs-lookup"><span data-stu-id="b8363-247">All versions of the feature are popularly referred to as SPAD.</span></span>

> [!Note]  
> <span data-ttu-id="b8363-248">如果您執行的是 Windows 2000 或 Windows XP，則必須至少安裝 Windows 2000 SP3 或 Windows XP SP1，才能看到 [ **設定程式存取和預設值** ] 頁面。</span><span class="sxs-lookup"><span data-stu-id="b8363-248">If you are running Windows 2000 or Windows XP, you must have at least Windows 2000 SP3 or Windows XP SP1 installed to see the **Set Program Access and Defaults** page.</span></span> <span data-ttu-id="b8363-249">在 Windows Vista 和更新版本中，存取 [ **設定程式存取和電腦預設值** ] 頁面需要系統管理員許可權。</span><span class="sxs-lookup"><span data-stu-id="b8363-249">In Windows Vista and later, access to the **Set Program Access and Computer Defaults** page requires Administrator privileges.</span></span> <span data-ttu-id="b8363-250">基於這個理由，我們鼓勵開發人員註冊您的 [預設程式](default-programs.md) 主控台專案，讓任何使用者都能管理應用程式預設值。</span><span class="sxs-lookup"><span data-stu-id="b8363-250">For this reason, developers are encouraged to register for the [Set your default programs](default-programs.md) Control Panel item so that any user can manage application defaults.</span></span>

 

<span data-ttu-id="b8363-251">下列登錄樹狀目錄顯示必須在程式的 **InstallInfo** 機碼中註冊的各種資訊，程式才會出現在 [ **設定程式存取和電腦預設值** ] 頁面上，以作為其用戶端類型的選項。</span><span class="sxs-lookup"><span data-stu-id="b8363-251">The following registry tree shows the variety of information that must be registered in the program's **InstallInfo** key in order for the program to appear on the **Set Program Access and Computer Defaults** page as an option for its client type.</span></span> <span data-ttu-id="b8363-252">下列各節將詳細討論這些值。</span><span class="sxs-lookup"><span data-stu-id="b8363-252">Each of these values is discussed in detail in the following sections.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               InstallInfo
                  HideIconsCommand = command line
                  ReinstallCommand = command line
                  ShowIconsCommand = command line
                  IconsVisible = 1
```

<span data-ttu-id="b8363-253">命令列必須指定檔案的完整絕對路徑，後面接著選擇性的命令列選項。</span><span class="sxs-lookup"><span data-stu-id="b8363-253">The command line must specify a fully qualified absolute path to the file, followed by optional command-line options.</span></span> <span data-ttu-id="b8363-254">適當地使用引號，以確保命令列中的空格不會誤解。</span><span class="sxs-lookup"><span data-stu-id="b8363-254">Use quotation marks appropriately to ensure that spaces in the command line are not misinterpreted.</span></span>

### <a name="the-reinstall-command"></a><span data-ttu-id="b8363-255">重新安裝命令</span><span class="sxs-lookup"><span data-stu-id="b8363-255">The Reinstall Command</span></span>

<span data-ttu-id="b8363-256">當使用者使用 [ **設定程式存取和電腦預設值** ] 頁面來選取您的程式做為其用戶端類型的預設值時，會執行 ReinstallCommand 值中宣告的重新安裝命令列。</span><span class="sxs-lookup"><span data-stu-id="b8363-256">The reinstall command line declared in the ReinstallCommand value is executed when the user uses the **Set Program Access and Computer Defaults** page to select your program as the default for its client type.</span></span> <span data-ttu-id="b8363-257">在 Windows Vista 和更新版本中，存取此頁面需要系統管理員許可權層級。</span><span class="sxs-lookup"><span data-stu-id="b8363-257">In Windows Vista and later, access to this page requires an Administrator privilege level.</span></span> <span data-ttu-id="b8363-258">在 Windows 8 中，如果您已針對 [ **設定程式存取] 和 [電腦預設值** ] 和 [ **預設程式**] 使用相同的名稱來註冊應用程式，則會對目前的使用者套用該應用程式的 **預設程式** 中指定的預設值，以及執行重新安裝命令。</span><span class="sxs-lookup"><span data-stu-id="b8363-258">In Windows 8, if you have registered your application using the same name for both **Set Program Access and Computer Defaults** and **Default Programs**, the defaults specified in **Default Programs** for that application will be applied for the current user as well as running the reinstall command.</span></span>

<span data-ttu-id="b8363-259">重新安裝命令列所啟動的程式必須將應用程式與應用程式可處理[的一組完整檔案和](fa-intro.md)[通訊協定](/previous-versions//aa767743(v=vs.85))類型產生關聯。</span><span class="sxs-lookup"><span data-stu-id="b8363-259">The program launched by the reinstall command line must associate the application with the complete set of [file](fa-intro.md) and [protocol](/previous-versions//aa767743(v=vs.85)) types the application can handle.</span></span> <span data-ttu-id="b8363-260">所有應用程式都必須在重新安裝命令中建立處理常式功能。</span><span class="sxs-lookup"><span data-stu-id="b8363-260">All applications must establish handler capability in the reinstall command.</span></span> <span data-ttu-id="b8363-261">應用程式可以使用重新安裝命令來註冊功能，並選擇性地建立預設狀態。</span><span class="sxs-lookup"><span data-stu-id="b8363-261">Applications can use the reinstall command to register capability as well as optionally establish default status.</span></span> <span data-ttu-id="b8363-262">當應用程式選擇在重新安裝命令中同時執行功能和預設處理常式狀態時，它也應該恢復任何所需的可見連結或快捷方式。</span><span class="sxs-lookup"><span data-stu-id="b8363-262">When an application chooses to implement both capability and default handler status in the reinstall command, it should also reinstate any visible links or shortcuts desired.</span></span> <span data-ttu-id="b8363-263">大部分應用程式選擇的可見進入點會列在 [隱藏圖示命令](#the-hide-icons-command)中。</span><span class="sxs-lookup"><span data-stu-id="b8363-263">The visible entry points most applications choose are listed in [The Hide Icons Command](#the-hide-icons-command).</span></span>

> [!Note]  
> <span data-ttu-id="b8363-264">強烈建議應用程式在重新安裝命令中執行處理功能。</span><span class="sxs-lookup"><span data-stu-id="b8363-264">It is highly recommended that applications implement handling capability in the reinstall command.</span></span>

 

<span data-ttu-id="b8363-265">重新安裝程式完成後，重新安裝命令列所啟動的程式應該會結束。</span><span class="sxs-lookup"><span data-stu-id="b8363-265">Once the reinstall process is complete, the program launched by the reinstall command line should exit.</span></span> <span data-ttu-id="b8363-266">它不應該啟動對應的程式;它應該只會註冊預設值。</span><span class="sxs-lookup"><span data-stu-id="b8363-266">It should not launch the corresponding program; it should merely register defaults.</span></span> <span data-ttu-id="b8363-267">例如，瀏覽器的重新安裝命令不應開啟使用者的首頁。</span><span class="sxs-lookup"><span data-stu-id="b8363-267">For example, the reinstall command for a browser should not open the user's home page.</span></span>

> [!Note]  
> <span data-ttu-id="b8363-268">針對 Windows XP 和 Windows Vista 中的瀏覽器和電子郵件客戶程式，在重新安裝命令中選擇建立處理功能和預設狀態的應用程式，應該在 [開始] 功能表的頂端註冊對應的圖示。</span><span class="sxs-lookup"><span data-stu-id="b8363-268">For browser and email clients in Windows XP and Windows Vista, applications that choose to establish both handling capability and default status in the reinstall command should register for the corresponding icon at the top of the Start menu.</span></span> <span data-ttu-id="b8363-269">如需其他資訊，請參閱 [開始功能表註冊](#start-menu-registration) 。</span><span class="sxs-lookup"><span data-stu-id="b8363-269">See [Start Menu Registration](#start-menu-registration) for additional information.</span></span>

 

### <a name="the-hide-icons-command"></a><span data-ttu-id="b8363-270">隱藏圖示命令</span><span class="sxs-lookup"><span data-stu-id="b8363-270">The Hide Icons Command</span></span>

<span data-ttu-id="b8363-271">當使用者在 [**設定程式存取和電腦預設值**] 頁面中清除 [**啟用對這個程式的存取**] 方塊時，會執行在 HideIconsCommand 值中宣告的命令列。</span><span class="sxs-lookup"><span data-stu-id="b8363-271">The command line declared in the HideIconsCommand value is executed when the user clears the **Enable access to this program** box in the **Set Program Access and Computer Defaults** page.</span></span> <span data-ttu-id="b8363-272">此命令列必須隱藏在使用者介面中顯示的所有程式存取點。</span><span class="sxs-lookup"><span data-stu-id="b8363-272">This command line must hide all of your program's access points that are visible in the user interface.</span></span> <span data-ttu-id="b8363-273">特定的指導方針是移除下列位置的快捷方式和圖示：</span><span class="sxs-lookup"><span data-stu-id="b8363-273">The specific guidelines are to remove shortcuts and icons from the following locations:</span></span>

-   <span data-ttu-id="b8363-274">桌面圖示</span><span class="sxs-lookup"><span data-stu-id="b8363-274">Desktop icons</span></span>
-   <span data-ttu-id="b8363-275">[開始] 功能表連結，包括 **Startup** 群組</span><span class="sxs-lookup"><span data-stu-id="b8363-275">Start menu links, including the **Startup** group</span></span>
-   <span data-ttu-id="b8363-276">快速啟動 bar 連結</span><span class="sxs-lookup"><span data-stu-id="b8363-276">Quick Launch bar links</span></span>
-   <span data-ttu-id="b8363-277">[通知] 區域</span><span class="sxs-lookup"><span data-stu-id="b8363-277">Notification area</span></span>
-   <span data-ttu-id="b8363-278">快顯功能表</span><span class="sxs-lookup"><span data-stu-id="b8363-278">Shortcut menus</span></span>
-   <span data-ttu-id="b8363-279">資料夾工作區</span><span class="sxs-lookup"><span data-stu-id="b8363-279">Folder task band</span></span>

<span data-ttu-id="b8363-280">此命令列也必須防止自動叫用程式，例如 **執行** 登錄機碼中指定的程式。</span><span class="sxs-lookup"><span data-stu-id="b8363-280">This command line must also prevent automatic invocations of the program, such as those specified in the **Run** registry key.</span></span> <span data-ttu-id="b8363-281">建議廠商在應用程式的隱藏存取回呼中實施這些指導方針。</span><span class="sxs-lookup"><span data-stu-id="b8363-281">Vendors are encouraged to implement these guidelines in the application's Hide Access callback.</span></span>

<span data-ttu-id="b8363-282">隱藏圖示時，您不需要放棄註冊 (應用程式功能) 檔案類型。</span><span class="sxs-lookup"><span data-stu-id="b8363-282">You do not need to relinquish registration (application capability) of file types when icons are hidden.</span></span> <span data-ttu-id="b8363-283">您也不需要為檔案和通訊協定類型放棄應用程式的預設狀態。</span><span class="sxs-lookup"><span data-stu-id="b8363-283">You also do not need to relinquish the application's default status for file and protocol types.</span></span> <span data-ttu-id="b8363-284">當 UI 中遇到這些類型時，這樣做可能會導致不良的使用者體驗。</span><span class="sxs-lookup"><span data-stu-id="b8363-284">Doing so can lead to a bad user experience when these types are encountered in the UI.</span></span>

<span data-ttu-id="b8363-285">成功隱藏圖示之後，您必須將 IconsVisible 登錄值更新為0，如下所示：</span><span class="sxs-lookup"><span data-stu-id="b8363-285">After successfully hiding icons, you must update the IconsVisible registry value to 0 as shown:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               InstallInfo
                  IconsVisible = 0
```

<span data-ttu-id="b8363-286">IconsVisible 專案的類型為 **REG \_ DWORD**。</span><span class="sxs-lookup"><span data-stu-id="b8363-286">The IconsVisible entry is of type **REG\_DWORD**.</span></span>

### <a name="an-alternate-hide-icons-method-in-spad"></a><span data-ttu-id="b8363-287">SPAD 中的替代隱藏圖示方法</span><span class="sxs-lookup"><span data-stu-id="b8363-287">An Alternate Hide Icons Method in SPAD</span></span>

<span data-ttu-id="b8363-288">針對某些繼承應用程式，隱藏存取的完整執行可能不實用。</span><span class="sxs-lookup"><span data-stu-id="b8363-288">For some legacy applications, a full implementation of Hide Access may not be practical.</span></span> <span data-ttu-id="b8363-289">另一種可達到相同效果的方法是卸載應用程式。</span><span class="sxs-lookup"><span data-stu-id="b8363-289">An alternative method that achieves the same effect is to uninstall the application.</span></span> <span data-ttu-id="b8363-290">下一節顯示範例行為和範例程式碼來執行此替代方案。</span><span class="sxs-lookup"><span data-stu-id="b8363-290">The section below shows example behavior and sample code to implement this alternative.</span></span> <span data-ttu-id="b8363-291">一般而言，獨立軟體廠商 (Isv) 應避免此替代方案，因為它將會：</span><span class="sxs-lookup"><span data-stu-id="b8363-291">In general, independent software vendors (ISVs) should avoid this alternative since it will:</span></span>

-   <span data-ttu-id="b8363-292">從系統完全卸載應用程式。</span><span class="sxs-lookup"><span data-stu-id="b8363-292">Uninstall the application completely from the system.</span></span>
-   <span data-ttu-id="b8363-293">移除先前選取的預設值。</span><span class="sxs-lookup"><span data-stu-id="b8363-293">Remove previously selected defaults.</span></span>
-   <span data-ttu-id="b8363-294">不要讓 UI 選項重新安裝應用程式。</span><span class="sxs-lookup"><span data-stu-id="b8363-294">Leave no UI option to reinstall the application.</span></span>
-   <span data-ttu-id="b8363-295">讓 [啟用存取] 功能不再可用，因為卸載會從 SPAD 完全移除應用程式。</span><span class="sxs-lookup"><span data-stu-id="b8363-295">Make the enable access feature no longer available, since an uninstallation removes the application completely from SPAD.</span></span>

<span data-ttu-id="b8363-296">建議的使用者體驗如下所示：</span><span class="sxs-lookup"><span data-stu-id="b8363-296">The recommended user experience is as follows:</span></span>

-   <span data-ttu-id="b8363-297">當使用者在 SPAD 中取消核取 [ **啟用此程式存取** ] 方塊時，會顯示下列 UI。</span><span class="sxs-lookup"><span data-stu-id="b8363-297">When the user unchecks the **Enable access to this program** box in SPAD, the following UI is presented.</span></span>

    ![關於隱藏程式存取權的對話方塊](images/hideaccessvista.png)

-   <span data-ttu-id="b8363-299">當使用者選取 **[確定]** 時，主控台專案的 [ **程式和功能** ] 隨即啟動，讓使用者可以卸載應用程式。</span><span class="sxs-lookup"><span data-stu-id="b8363-299">When the user selects **OK**, the **Programs and Features** Control Panel item launches to allow the user to uninstall the application.</span></span>
-   <span data-ttu-id="b8363-300">Windows XP 使用者應該會看到這個對話方塊。</span><span class="sxs-lookup"><span data-stu-id="b8363-300">Windows XP users should be presented with this dialog box.</span></span>

    ![對等的 windows xp 對話方塊](images/hideaccessxp.png)

-   <span data-ttu-id="b8363-302">當 Windows XP 使用者選取 **[確定]** 時，會啟動 [ **新增或移除程式** ] 主控台專案，讓使用者可以卸載應用程式。</span><span class="sxs-lookup"><span data-stu-id="b8363-302">When the Windows XP user selects **OK**, the **Add or Remove Programs** Control Panel item launches to allow the user to uninstall the application.</span></span>

<span data-ttu-id="b8363-303">下列程式碼會為隱藏存取功能提供可重複使用的執行方式，如上面所述。</span><span class="sxs-lookup"><span data-stu-id="b8363-303">The following code provides a reusable implementation for the Hide Access feature as outlined above.</span></span> <span data-ttu-id="b8363-304">它可用於 Windows XP、Windows Vista 和 Windows 7。</span><span class="sxs-lookup"><span data-stu-id="b8363-304">It can be used on Windows XP, Windows Vista, and Windows 7.</span></span>


```
#include <windows.h>
#include <shlwapi.h>
#include <strsafe.h>

PCWSTR c_pszMessage1 = L"To hide access to this program, you need to uninstall it by ";
PCWSTR c_pszMessage2 = L"using\n%s in Control Panel.\n\nWould you like to start %s?";
PCWSTR c_pszApplicationName  = L"Sample App";

int _tmain(int argc, WCHAR* argv[])
{
    OSVERSIONINFO version;
    version.dwOSVersionInfoSize = sizeof(version);

    if (GetVersionEx(&version))
    {
        PCWSTR pszCPLName = NULL;

        if (version.dwMajorVersion >= 6)
        {
            // Windows Vista and later
            pszCPLName = L"Programs and Features";
        }
        else if (version.dwMajorVersion == 5 &&
                 version.dwMinorVersion == 1)
        {
            // Windows XP
            pszCPLName = L"Add/Remove Programs";
        }

        if (pszCPLName != NULL)
        {
            WCHAR szMessage[256], szScratch[256];
            if (SUCCEEDED(StringCchPrintf(szScratch, 
                                          ARRAYSIZE(szScratch), 
                                          c_pszMessage2, 
                                          pszCPLName, 
                                          pszCPLName)))
            {
                if (SUCCEEDED(StringCchCopy(szMessage, 
                                            ARRAYSIZE(szMessage), 
                                            c_pszMessage1)))
                {
                    if (SUCCEEDED(StringCchCat(szMessage, 
                                               ARRAYSIZE(szMessage), 
                                               szScratch)))
                    {
                        if (IDOK == MessageBox(NULL, 
                                               szMessage, 
                                               c_pszApplicationName, 
                                               MB_OKCANCEL))
                        {
                            ShellExecute(NULL, 
                                         NULL, 
                                         L"appwiz.cpl", 
                                         NULL, 
                                         NULL, 
                                         SW_SHOWNORMAL);
                        }
                    }
                }
            }
        }
    }
    return 0;
}
```



### <a name="the-show-icons-command"></a><span data-ttu-id="b8363-305">顯示圖示命令</span><span class="sxs-lookup"><span data-stu-id="b8363-305">The Show Icons Command</span></span>

<span data-ttu-id="b8363-306">當使用者在 [**設定程式存取和電腦預設值**] 頁面中檢查 [**啟用存取此程式**] 方塊時，會執行在 ShowIconsCommand 專案中宣告的命令列。</span><span class="sxs-lookup"><span data-stu-id="b8363-306">The command line declared in the ShowIconsCommand entry is executed when the user checks the **Enable access to this program** box in the **Set Program Access and Computer Defaults** page.</span></span> <span data-ttu-id="b8363-307">此命令列可還原程式的存取點，包括 [ **開始** ] 功能表、桌面上和 [ **啟動** ] 群組中的存取點，以及一般自動叫用，例如在 [ **執行** ] 登錄機碼中指定的存取點。</span><span class="sxs-lookup"><span data-stu-id="b8363-307">This command line may restore your program's access points, including those in the **Start** menu, on the desktop, and in the **Startup** group, as well as normal automatic invocations, such as those specified in the **Run** registry key.</span></span> <span data-ttu-id="b8363-308">對大部分應用程式感興趣的可見存取點會列在 [隱藏圖示命令](#the-hide-icons-command)中。</span><span class="sxs-lookup"><span data-stu-id="b8363-308">The visible access points of interest to most applications are listed in [The Hide Icons Command](#the-hide-icons-command).</span></span> <span data-ttu-id="b8363-309">應用程式不應變更每個使用者預設值;這項變更應該由使用者透過 **預設程式** 來完成。</span><span class="sxs-lookup"><span data-stu-id="b8363-309">The application should not change per-user defaults; that change should be done by the user through **Default Programs**.</span></span>

<span data-ttu-id="b8363-310">成功顯示圖示之後，您必須將 IconsVisible 登錄值更新為1，如下所示：</span><span class="sxs-lookup"><span data-stu-id="b8363-310">After successfully showing your icons, you must update the IconsVisible registry value to 1 as shown:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               InstallInfo
                  IconsVisible = 1
```

<span data-ttu-id="b8363-311">請注意，如果您已使用 HideIconsCommand 專案提示卸載應用程式，ShowIconsCommand 專案就不會使用。</span><span class="sxs-lookup"><span data-stu-id="b8363-311">Note that if you have used the HideIconsCommand entry to prompt an uninstall of the application, the ShowIconsCommand entry is of no use.</span></span> <span data-ttu-id="b8363-312">它應該從登錄中移除，並在卸載過程中移除其餘的應用程式資訊。</span><span class="sxs-lookup"><span data-stu-id="b8363-312">It should be removed from the registry with the rest of the application's information during the uninstall process.</span></span>

### <a name="group-program-configuration"></a><span data-ttu-id="b8363-313">組程式設定</span><span class="sxs-lookup"><span data-stu-id="b8363-313">Group Program Configuration</span></span>

> [!Note]  
> <span data-ttu-id="b8363-314">本節不適用 Windows 2000。</span><span class="sxs-lookup"><span data-stu-id="b8363-314">This section does not apply to Windows 2000.</span></span>

 

<span data-ttu-id="b8363-315">在系統準備過程中，OEM 可以建立針對 JAVA 用戶端程式隱藏 Microsoft 瀏覽器、電子郵件、媒體播放、立即訊息或虛擬機器存取點的設定，並指定自己的預設程式。</span><span class="sxs-lookup"><span data-stu-id="b8363-315">As part of system preparation, an OEM can establish a configuration that hides access points for the Microsoft browser, email, media playback, instant messaging, or virtual machine for Java client programs and specifies their own default programs.</span></span> <span data-ttu-id="b8363-316">Oem 可以設定下列登錄值，讓使用者隨時都能將電腦重設為此預設設定。</span><span class="sxs-lookup"><span data-stu-id="b8363-316">OEMs can enable users to reset their computers at any time to this default configuration by setting the following registry values.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               InstallInfo
                  OEMShowIcons = 1
                  OEMDefault = 1
```

<span data-ttu-id="b8363-317">如果設定這些金鑰，使用者就可以在 [**設定程式存取和電腦預設值**] 頁面上，選取 [**電腦製造商**] 選項來還原 OEM 設定。</span><span class="sxs-lookup"><span data-stu-id="b8363-317">If these keys are set, users can restore the OEM configuration by selecting the **Computer Manufacturer** option on the **Set Program Access and Computer Defaults** page.</span></span> <span data-ttu-id="b8363-318">如果未設定這些金鑰，則不會顯示 [ **電腦製造商** ] 選項。</span><span class="sxs-lookup"><span data-stu-id="b8363-318">If these keys are not set, the **Computer Manufacturer** option is not shown.</span></span>

<span data-ttu-id="b8363-319">**OEMShowIcons** 專案（如果有的話）會設定指定用戶端的圖示顯示狀態（如果使用者選取 **電腦製造商** 的話）。</span><span class="sxs-lookup"><span data-stu-id="b8363-319">The **OEMShowIcons** entry, if present, sets the icon show state for the specified client that is applied if the user selects **Computer Manufacturer**.</span></span> <span data-ttu-id="b8363-320">值為1會顯示圖示，值為0則不會顯示圖示。</span><span class="sxs-lookup"><span data-stu-id="b8363-320">A value of 1 causes icons to be shown, and a value of 0 causes icons to not be shown.</span></span> <span data-ttu-id="b8363-321">如果 **OEMShowIcons** 不存在，則選取 [ **電腦製造商** ] 並不會影響圖示顯示設定。</span><span class="sxs-lookup"><span data-stu-id="b8363-321">If **OEMShowIcons** is absent, selecting **Computer Manufacturer** has no effect on the icon show setting.</span></span> <span data-ttu-id="b8363-322">**OEMShowIcons** 的類型為 **REG \_ DWORD**。</span><span class="sxs-lookup"><span data-stu-id="b8363-322">**OEMShowIcons** is of type **REG\_DWORD**.</span></span>

<span data-ttu-id="b8363-323">如果出現並設定為1， **OEMDefault** 專案就會建立指定之型別的預設用戶端的 OEM 喜好設定。</span><span class="sxs-lookup"><span data-stu-id="b8363-323">The **OEMDefault** entry, if present and set to 1, establishes the OEM preference for the default client of the indicated type.</span></span> <span data-ttu-id="b8363-324">只有一個特定類型的用戶端可以標記為 OEM 預設值。</span><span class="sxs-lookup"><span data-stu-id="b8363-324">Only one client of a particular type can be marked as the OEM default.</span></span> <span data-ttu-id="b8363-325">如果有多個用戶端的註冊包含 **OEMDefault** 專案，則會忽略所有專案，而且目前的用戶端會繼續作為預設用戶端使用。</span><span class="sxs-lookup"><span data-stu-id="b8363-325">If more then one client's registration contains the **OEMDefault** entry, then all are ignored and the current client continues to be used as default client.</span></span> <span data-ttu-id="b8363-326">如果 **OEMDefault** 專案不存在或存在，而且設定為0，則在使用者選取 **電腦製造商** 時，不會將該特定用戶端當做預設用戶端使用。</span><span class="sxs-lookup"><span data-stu-id="b8363-326">If the **OEMDefault** entry is not present or is present and set to 0, then that particular client is not used as the default client if the user selects **Computer Manufacturer**.</span></span> <span data-ttu-id="b8363-327">**OEMDefault** 的類型為 **REG \_ DWORD**。</span><span class="sxs-lookup"><span data-stu-id="b8363-327">**OEMDefault** is of type **REG\_DWORD**.</span></span>

<span data-ttu-id="b8363-328">除了將電腦重設為 OEM 所建立之預設設定的選項之外，使用者還有其他三個設定選項：</span><span class="sxs-lookup"><span data-stu-id="b8363-328">In addition to the option to reset their computers to the default configuration established by the OEM, users have three other configuration options:</span></span>

-   <span data-ttu-id="b8363-329">將其電腦設定為 Microsoft Windows 設定。</span><span class="sxs-lookup"><span data-stu-id="b8363-329">Set their computer to a Microsoft Windows configuration.</span></span> <span data-ttu-id="b8363-330">在此情況下，[ **設定程式存取和電腦預設值** ] 頁面可讓您存取在相關產品類別中註冊之電腦上的所有 microsoft 和非 microsoft 軟體。</span><span class="sxs-lookup"><span data-stu-id="b8363-330">In this case, the **Set Program Access and Computer Defaults** page enables access to all Microsoft and non-Microsoft software on the computer registered in the relevant product categories.</span></span> <span data-ttu-id="b8363-331">系統會選取 Microsoft Windows 程式做為每個類別的預設選項。</span><span class="sxs-lookup"><span data-stu-id="b8363-331">Microsoft Windows programs are selected as the default option for each category.</span></span>
-   <span data-ttu-id="b8363-332">將其電腦設定為非 Microsoft 設定。</span><span class="sxs-lookup"><span data-stu-id="b8363-332">Set their computer to a non-Microsoft configuration.</span></span> <span data-ttu-id="b8363-333">此設定會隱藏存取點 (例如 [ **開始** ] 功能表) 至 windows Internet Explorer、Windows Media Player、windows Messenger 和 Microsoft Outlook Express。</span><span class="sxs-lookup"><span data-stu-id="b8363-333">This configuration hides access points (such as the **Start** menu) to Windows Internet Explorer, Windows Media Player, Windows Messenger, and Microsoft Outlook Express.</span></span> <span data-ttu-id="b8363-334">它可讓您存取電腦上的非 Microsoft 軟體。</span><span class="sxs-lookup"><span data-stu-id="b8363-334">It enables access to the non-Microsoft software on the computer in these categories.</span></span> <span data-ttu-id="b8363-335">此外，如果類別中有非 Microsoft 程式，則會設定為該類別的預設值。</span><span class="sxs-lookup"><span data-stu-id="b8363-335">Furthermore, if a non-Microsoft program is available in a category, it is set as the default for that category.</span></span> <span data-ttu-id="b8363-336">如果類別中有一個以上的非 Microsoft 程式，系統會要求使用者選擇應使用哪一個非 Microsoft 程式做為預設。</span><span class="sxs-lookup"><span data-stu-id="b8363-336">If more than one non-Microsoft program is available in a category, the user is asked to choose which non-Microsoft program should be used as the default.</span></span>
-   <span data-ttu-id="b8363-337">建立自訂設定。</span><span class="sxs-lookup"><span data-stu-id="b8363-337">Establish a custom configuration.</span></span> <span data-ttu-id="b8363-338">使用者可以自行選擇是否要啟用或移除存取權，並在適當的情況下混用 Microsoft 與非 Microsoft 程式。</span><span class="sxs-lookup"><span data-stu-id="b8363-338">Users make their own selections for enabling or removing access, mixing Microsoft and non-Microsoft programs as they see fit.</span></span> <span data-ttu-id="b8363-339">使用者會依類別目錄來建立預設選項。</span><span class="sxs-lookup"><span data-stu-id="b8363-339">Users establish default options on a category-by-category basis.</span></span>

<span data-ttu-id="b8363-340">使用者隨時都可以隨時變更這些選項。</span><span class="sxs-lookup"><span data-stu-id="b8363-340">Users are free to change any of these options at any time.</span></span>

### <a name="browser-registration-example"></a><span data-ttu-id="b8363-341">瀏覽器註冊範例</span><span class="sxs-lookup"><span data-stu-id="b8363-341">Browser Registration Example</span></span>

<span data-ttu-id="b8363-342">下列範例顯示虛構亮 View 瀏覽器的完整 **InstallInfo** 註冊。</span><span class="sxs-lookup"><span data-stu-id="b8363-342">The following example shows the full **InstallInfo** registration for a fictional Lit View browser.</span></span> <span data-ttu-id="b8363-343">在此情況下，命令列參數可讓 Litview.exe 檔案執行每個值所需的任何動作。</span><span class="sxs-lookup"><span data-stu-id="b8363-343">In this case the command line switches allow the Litview.exe file to perform whatever actions are necessary for each value.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         StartMenuInternet
            LITVIEW.EXE
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\Litview.exe" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\Litview.exe" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\Litview.exe" /showicons
                  IconsVisible = 1
```

<span data-ttu-id="b8363-344">請注意，引號是放在路徑周圍，因為它們包含內嵌的空格。</span><span class="sxs-lookup"><span data-stu-id="b8363-344">Note that quotation marks are placed around the paths because they contain embedded spaces.</span></span>

## <a name="registration-elements-for-specific-client-types"></a><span data-ttu-id="b8363-345">特定用戶端類型的註冊元素</span><span class="sxs-lookup"><span data-stu-id="b8363-345">Registration Elements for Specific Client Types</span></span>

<span data-ttu-id="b8363-346">您也可以在本主題結尾的相關主題一節所列的資源中找到下列資訊。</span><span class="sxs-lookup"><span data-stu-id="b8363-346">The following information also can be found in the resources listed in the Related Topics section at the end of this topic.</span></span>

-   [<span data-ttu-id="b8363-347">開始功能表註冊</span><span class="sxs-lookup"><span data-stu-id="b8363-347">Start Menu Registration</span></span>](#start-menu-registration)
-   [<span data-ttu-id="b8363-348">郵件用戶端註冊</span><span class="sxs-lookup"><span data-stu-id="b8363-348">Mail Client Registration</span></span>](#mail-client-registration)

### <a name="start-menu-registration"></a><span data-ttu-id="b8363-349">開始功能表註冊</span><span class="sxs-lookup"><span data-stu-id="b8363-349">Start Menu Registration</span></span>

<span data-ttu-id="b8363-350">在 Windows XP 中，應用程式通常會在整部電腦的 (**HKEY \_ 本機 \_ 電腦** 上註冊預設值) 而不是使用者 (**HKEY 目前的 \_ \_ 使用者**) 領域。</span><span class="sxs-lookup"><span data-stu-id="b8363-350">Under Windows XP, applications typically registered defaults on a machine-wide (**HKEY\_LOCAL\_MACHINE**) rather than a user (**HKEY\_CURRENT\_USER**) scope.</span></span> <span data-ttu-id="b8363-351">隨著 Windows Vista 的使用者帳戶控制 (UAC) ，在 [**開始**] 功能表中宣告 **網際網路** 和 **電子郵件** 位置的應用程式，必須在正確的執行內容中執行重新安裝命令。</span><span class="sxs-lookup"><span data-stu-id="b8363-351">With the Windows Vista introduction of the User Account Control (UAC), applications that claim the **Internet** and **E-mail** slots in the **Start** menu must implement the reinstall command within the correct execution context.</span></span>

> [!Note]  
> <span data-ttu-id="b8363-352">從 Windows 7 起，已移除 [開始] 功能表的 **電子郵件** 連結。</span><span class="sxs-lookup"><span data-stu-id="b8363-352">The Start menu **E-mail** link has been removed as of Windows 7.</span></span> <span data-ttu-id="b8363-353">不過，本節所討論的註冊仍應執行，因為它會指派預設的 MAPI 用戶端。</span><span class="sxs-lookup"><span data-stu-id="b8363-353">However, the registration discussed in this section should still be performed because it assigns the default MAPI client.</span></span>

 

<span data-ttu-id="b8363-354">Windows XP、Windows Vista 或 Windows 7 上的受限使用者無法存取 SPAD。</span><span class="sxs-lookup"><span data-stu-id="b8363-354">A limited user on Windows XP, Windows Vista, or Windows 7 cannot access SPAD.</span></span> <span data-ttu-id="b8363-355">基於這個理由，我們鼓勵開發人員註冊您的 **預設程式** 主控台專案，讓任何使用者都可以管理每個使用者的應用程式預設值。</span><span class="sxs-lookup"><span data-stu-id="b8363-355">For this reason, developers are encouraged to register for the **Set your default programs** Control Panel item so that any user can manage per-user application defaults.</span></span>

<span data-ttu-id="b8363-356">在 SPAD 中所做的選擇只會影響個別電腦的設定。</span><span class="sxs-lookup"><span data-stu-id="b8363-356">Selections made in SPAD should only affect per-machine settings.</span></span>

<span data-ttu-id="b8363-357">設定登錄值，如下所示。</span><span class="sxs-lookup"><span data-stu-id="b8363-357">Set the registry value as follows.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            (Default) = CanonicalName
```

> [!Note]
> 
> <span data-ttu-id="b8363-358">**下列資訊僅適用于 Windows XP。**</span><span class="sxs-lookup"><span data-stu-id="b8363-358">**The following information applies to Windows XP only.**</span></span>
> 
> <span data-ttu-id="b8363-359">如果在 HKEY 本機電腦下註冊電腦層級的預設值 \_ \_ （如上所示），則應用程式應該刪除下列子機碼底下指派給預設專案的值：</span><span class="sxs-lookup"><span data-stu-id="b8363-359">If the registration of the computer-level default under HKEY\_LOCAL\_MACHINE as shown above is successful, the application should delete the value assigned to the Default entry under the following subkey:</span></span>
> 
> ```
> HKEY_CURRENT_USER
>    SOFTWARE
>       Clients
>          ClientTypeName
> ```
> 
> <span data-ttu-id="b8363-360">如果在 HKEY 本機電腦下註冊電腦層級的預設值（如上 \_ \_ 所示）失敗，通常是因為使用者沒有子機碼的寫入權限，應用程式應該設定下列值：</span><span class="sxs-lookup"><span data-stu-id="b8363-360">If the registration of the computer-level default under HKEY\_LOCAL\_MACHINE as shown above fails, usually because the user does not have write permission to the subkey, the application should set the following value:</span></span>
> 
> ```
> HKEY_CURRENT_USER
>    SOFTWARE
>       Clients
>          ClientTypeName
>             (Default) = CanonicalName
> ```
> 
> <span data-ttu-id="b8363-361">這只會為目前的使用者註冊標準名稱，而不會為所有使用者註冊。</span><span class="sxs-lookup"><span data-stu-id="b8363-361">This registers the canonical name only for the current user, not for all users.</span></span>

 

<span data-ttu-id="b8363-362">更新登錄機碼之後，程式應該使用 **wParam** = 0 廣播 [**WM \_ SETTINGCHANGE**](../winmsg/wm-settingchange.md)訊息，並將 **lParam** 指向以 null 終止的字串 "Software \\ Clients \\ **ClientTypeName**"，以通知作業系統預設用戶端已變更。</span><span class="sxs-lookup"><span data-stu-id="b8363-362">After updating the registry keys, the program should broadcast the [**WM\_SETTINGCHANGE**](../winmsg/wm-settingchange.md) message with **wParam** = 0 and **lParam** pointing to the null-terminated string "Software\\Clients\\**ClientTypeName**" to notify the operating system that the default client has changed.</span></span>

### <a name="mail-client-registration"></a><span data-ttu-id="b8363-363">郵件用戶端註冊</span><span class="sxs-lookup"><span data-stu-id="b8363-363">Mail Client Registration</span></span>

<span data-ttu-id="b8363-364">若為郵件用戶端，程式必須在 **HKEY \_ 類別的 \_ 根** mailto 金鑰下註冊設定，才能 \\ 服務使用此通訊協定的 url `mailto` 。</span><span class="sxs-lookup"><span data-stu-id="b8363-364">For a mail client, the program needs to have registered settings under the **HKEY\_CLASSES\_ROOT**\\**mailto** key in order to service URLs that use the `mailto` protocol.</span></span> <span data-ttu-id="b8363-365">設定可在下列機碼底下鏡像這些設定的值和索引鍵。</span><span class="sxs-lookup"><span data-stu-id="b8363-365">Set values and keys that mirror those settings under the following key.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         Mail
            CanonicalName
               Protocols
                  mailto
```

<span data-ttu-id="b8363-366">此登錄階層會取代 `mailto` 在 **HKEY \_ 類別 \_ 根目錄** \\ **mailto** 找到的現有登錄階層。</span><span class="sxs-lookup"><span data-stu-id="b8363-366">This registry hierarchy replaces the existing `mailto` registry hierarchy found at **HKEY\_CLASSES\_ROOT**\\**mailto**.</span></span> <span data-ttu-id="b8363-367">階層保持不變，只有位置已變更。</span><span class="sxs-lookup"><span data-stu-id="b8363-367">The hierarchy remains the same, only the location has changed.</span></span> <span data-ttu-id="b8363-368">此階層的格式記載于 MSDN 上的 [非同步插即用通訊協定總覽和教學](/previous-versions//aa767913(v=vs.85))課程。</span><span class="sxs-lookup"><span data-stu-id="b8363-368">The format of this hierarchy is documented on MSDN under [Asynchronous Pluggable Protocol Overviews and Tutorials](/previous-versions//aa767913(v=vs.85)).</span></span> <span data-ttu-id="b8363-369">一般來說， `mailto` 通訊協定會註冊到程式，而不是非同步通訊協定，在這種情況下，會套用將 [應用程式註冊至 URI 配置](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85)) 的檔。</span><span class="sxs-lookup"><span data-stu-id="b8363-369">Typically, the `mailto` protocol is registered to a program rather than an asynchronous protocol, in which case the documentation on [Registering an Application to a URI Scheme](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85)) applies.</span></span>

<span data-ttu-id="b8363-370">下列範例會顯示註冊 `mailto` `mailto` 至程式之處理常式的註冊區段。</span><span class="sxs-lookup"><span data-stu-id="b8363-370">The following example shows the `mailto` section of the registration for a `mailto` handler registered to a program.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         Mail
            CanonicalName
               Protocols
                  mailto
                     (Default) = URL:MailTo Protocol
                     EditFlags = 02 00 00 00
                     URL Protocol
                     DefaultIcon
                        (Default) = %FilePath%,IconIndex
                     shell
                        open
                           command
                              (Default) = command line
```

<span data-ttu-id="b8363-371">EditFlags 登錄值記錄在標題為「定義檔案類型屬性」一節的 [檔案類型](fa-file-types.md) 中。</span><span class="sxs-lookup"><span data-stu-id="b8363-371">The EditFlags registry value is documented in [File Types](fa-file-types.md) in the section titled "Defining File Type Attributes."</span></span>

## <a name="complete-sample-registrations"></a><span data-ttu-id="b8363-372">完成範例註冊</span><span class="sxs-lookup"><span data-stu-id="b8363-372">Complete Sample Registrations</span></span>

<span data-ttu-id="b8363-373">下列範例是為了顯示各種用戶端類型的完整註冊需求而提供。</span><span class="sxs-lookup"><span data-stu-id="b8363-373">The following examples are provided to show the complete registration requirements for the various client types.</span></span>

-   [<span data-ttu-id="b8363-374">範例瀏覽器</span><span class="sxs-lookup"><span data-stu-id="b8363-374">A Sample Browser</span></span>](#a-sample-browser)
-   [<span data-ttu-id="b8363-375">範例郵件瀏覽器</span><span class="sxs-lookup"><span data-stu-id="b8363-375">A Sample Mail Browser</span></span>](#a-sample-mail-browser)
-   [<span data-ttu-id="b8363-376">範例媒體播放機</span><span class="sxs-lookup"><span data-stu-id="b8363-376">A Sample Media Player</span></span>](#a-sample-media-player)
-   [<span data-ttu-id="b8363-377">範例即時 Messenger 程式</span><span class="sxs-lookup"><span data-stu-id="b8363-377">A Sample Instant Messenger Program</span></span>](#a-sample-instant-messenger-program)
-   [<span data-ttu-id="b8363-378">適用于 JAVA 的虛擬機器範例</span><span class="sxs-lookup"><span data-stu-id="b8363-378">A Sample Virtual Machine for Java</span></span>](#a-sample-virtual-machine-for-java)

### <a name="a-sample-browser"></a><span data-ttu-id="b8363-379">範例瀏覽器</span><span class="sxs-lookup"><span data-stu-id="b8363-379">A Sample Browser</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         StartMenuInternet
            LITVIEW.EXE
               (Default) = Lit View
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /showicons
                  IconsVisible = 1
                  shell
                     open
                        command
                           (Default) = "C:\Program Files\LitwareInc\LITVIEW.EXE" /homepage
```

### <a name="a-sample-mail-browser"></a><span data-ttu-id="b8363-380">範例郵件瀏覽器</span><span class="sxs-lookup"><span data-stu-id="b8363-380">A Sample Mail Browser</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         Mail
            Lit View
               (Default) = Lit View
               DLLPath = @C:\Program Files\LItwareInc\LitwareMAPI.dll
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /showicons
                  IconsVisible = 1
               shell
                  open
                     command
                        (Default) = "C:\Program Files\LitwareInc\LITVIEW.EXE" /inbox
               protocols
                  mailto
                     (Default) = URL:MailTo Protocol
                     EditFlags = 02 00 00 00
                     URL Protocol
                     DefaultIcon
                        (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
                     shell
                        open
                           command
                              (Default) = "C:\Program Files\LitwareInc\LITVIEW.EXE" /mailto:%1
```

### <a name="a-sample-media-player"></a><span data-ttu-id="b8363-381">範例媒體播放機</span><span class="sxs-lookup"><span data-stu-id="b8363-381">A Sample Media Player</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         Media
            Lit View
               (Default) = Lit View
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /showicons
                  IconsVisible = 1
```

### <a name="a-sample-instant-messenger-program"></a><span data-ttu-id="b8363-382">範例即時 Messenger 程式</span><span class="sxs-lookup"><span data-stu-id="b8363-382">A Sample Instant Messenger Program</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         IM
            Lit View
               (Default) = Lit View
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /showicons
                  IconsVisible = 1
```

### <a name="a-sample-virtual-machine-for-java"></a><span data-ttu-id="b8363-383">適用于 JAVA 的虛擬機器範例</span><span class="sxs-lookup"><span data-stu-id="b8363-383">A Sample Virtual Machine for Java</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         JavaVM
            Lit View
               (Default) = Lit View
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /showicons
                  IconsVisible = 1
```

<span data-ttu-id="b8363-384">*此處所描述的範例公司、組織、產品、功能變數名稱、電子郵件地址、標誌、人員、地點及事件均屬虛構。任何真實的公司、組織、產品、功能變數名稱、電子郵件地址、標誌、人員、地點或事件，都不會有任何關聯。*</span><span class="sxs-lookup"><span data-stu-id="b8363-384">*The example companies, organizations, products, domain names, email addresses, logos, people, places, and events depicted herein are fictitious. No association with any real company, organization, product, domain name, email address, logo, person, place, or event is intended or should be inferred.*</span></span>

## <a name="related-topics"></a><span data-ttu-id="b8363-385">相關主題</span><span class="sxs-lookup"><span data-stu-id="b8363-385">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8363-386">預設程式</span><span class="sxs-lookup"><span data-stu-id="b8363-386">Default Programs</span></span>](default-programs.md)
</dt> <dt>

<span data-ttu-id="b8363-387">[如何使用 Windows [開始] 功能表註冊網際網路瀏覽器或電子郵件客戶程式](start-menu-reg.md)</span><span class="sxs-lookup"><span data-stu-id="b8363-387">[How to Register an Internet Browser or Email Client With the Windows Start Menu](start-menu-reg.md)</span></span>
</dt> <dt>

<span data-ttu-id="b8363-388">[Internet Explorer 用戶端登錄配置 (請參閱「用戶端登錄機碼定義」一節) ](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa753633(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b8363-388">[Internet Explorer Client Registry Layout (see the "Client Registry Key Definitions" section)](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa753633(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="b8363-389">[非同步插即用通訊協定的總覽和教學課程](/previous-versions//aa767913(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b8363-389">[Asynchronous Pluggable Protocol Overviews and Tutorials](/previous-versions//aa767913(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="b8363-390">[將應用程式註冊至 URI 配置](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b8363-390">[Registering an Application to a URI Scheme](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85))</span></span>
</dt> </dl>

 

 

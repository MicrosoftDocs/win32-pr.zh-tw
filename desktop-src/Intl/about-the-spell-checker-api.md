---
description: 針對全球使用者，文字輸入是新式運算體驗的一部分，適用于博客、批註、tweet、立即訊息，或任何其他類型的文字類型。 在 Windows 8 中，已內建編輯控制項的拼寫檢查。
ms.assetid: ED569D4F-568B-4381-91C3-8EAEDA4DD47C
title: 關於拼寫檢查 API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f0d356823e665781052e2a2d5ea98b358155038
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850259"
---
# <a name="about-the-spell-checking-api"></a><span data-ttu-id="c50ef-104">關於拼寫檢查 API</span><span class="sxs-lookup"><span data-stu-id="c50ef-104">About the Spell Checking API</span></span>

<span data-ttu-id="c50ef-105">針對全球使用者，文字輸入是新式運算體驗的一部分，適用于博客、批註、tweet、立即訊息，或任何其他類型的文字類型。</span><span class="sxs-lookup"><span data-stu-id="c50ef-105">For users worldwide, textual input is part of a modern computing experience, for blogging, commenting, tweeting, instant messaging, or any other kind of text typing.</span></span> <span data-ttu-id="c50ef-106">在 Windows 8 中，已內建編輯控制項的拼寫檢查。</span><span class="sxs-lookup"><span data-stu-id="c50ef-106">In Windows 8, spell checking is built-in to edit controls.</span></span>

<span data-ttu-id="c50ef-107">開發人員可以在其應用程式中使用拼寫檢查 API，以使用可用的拼寫檢查服務。</span><span class="sxs-lookup"><span data-stu-id="c50ef-107">Developers can use the spell checking API in their apps to consume available spell checking services.</span></span> <span data-ttu-id="c50ef-108">開發人員也可以建立可成為提供者的拼寫檢查，並整合到 Windows 拼寫檢查架構中。</span><span class="sxs-lookup"><span data-stu-id="c50ef-108">Developers can also create spell checkers that become providers and are integrated into the Windows spell checking framework.</span></span>

<span data-ttu-id="c50ef-109">拼寫檢查 API 的設計目的是要讓 Windows 元件物件模型的專業 C/c + + 開發人員使用 (COM) 應用程式。</span><span class="sxs-lookup"><span data-stu-id="c50ef-109">The Spell Checking API is designed for use by professional C/C++ developers of Windows Component Object Model (COM) apps.</span></span> <span data-ttu-id="c50ef-110">在 Windows 或 ASP.NET 服務中不支援使用拼寫檢查 API。</span><span class="sxs-lookup"><span data-stu-id="c50ef-110">The Spell Checking API is not supported for use in a Windows or ASP.NET service.</span></span>

## <a name="versioning"></a><span data-ttu-id="c50ef-111">版本控制</span><span class="sxs-lookup"><span data-stu-id="c50ef-111">Versioning</span></span>

<span data-ttu-id="c50ef-112">從 Windows 8 或 Windows Server 2012 開始，可以使用拼寫檢查 API。</span><span class="sxs-lookup"><span data-stu-id="c50ef-112">The Spell Checking API is available beginning with the Windows 8 or Windows Server 2012.</span></span> <span data-ttu-id="c50ef-113">API 的未來新增將會藉由建立新介面來處理，而這些介面可使用現有的 [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 來決定。</span><span class="sxs-lookup"><span data-stu-id="c50ef-113">Future additions to the API will be handled by creating new interfaces that can be determined using [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the existing ones.</span></span>

## <a name="interfaces"></a><span data-ttu-id="c50ef-114">介面</span><span class="sxs-lookup"><span data-stu-id="c50ef-114">Interfaces</span></span>

<span data-ttu-id="c50ef-115">所有介面都必須在不再使用時釋放。</span><span class="sxs-lookup"><span data-stu-id="c50ef-115">All interfaces must be released when they are no longer used.</span></span> <span data-ttu-id="c50ef-116">所有傳回的 (out 參數) **LPWSTR** 字串 (和 [**IEnumString**](/windows/win32/api/objidlbase/nn-objidlbase-ienumstring)) 的 **LPOLESTR** 專案都必須在不再使用 CoTaskMemFree 時，與 [](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree)一起釋放。</span><span class="sxs-lookup"><span data-stu-id="c50ef-116">All returned (out parameter) **LPWSTR** strings (and **LPOLESTR** items from [**IEnumString**](/windows/win32/api/objidlbase/nn-objidlbase-ienumstring)) must be released with [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) when no longer used.</span></span>

## <a name="error-handling"></a><span data-ttu-id="c50ef-117">錯誤處理</span><span class="sxs-lookup"><span data-stu-id="c50ef-117">Error handling</span></span>

<span data-ttu-id="c50ef-118">錯誤會以 **HRESULT** s 傳回。</span><span class="sxs-lookup"><span data-stu-id="c50ef-118">Errors are returned as **HRESULT** s.</span></span> <span data-ttu-id="c50ef-119">此 API 不支援 [**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo)和 [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo) 。</span><span class="sxs-lookup"><span data-stu-id="c50ef-119">[**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo) and [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo) are not supported in this API.</span></span> <span data-ttu-id="c50ef-120">除了不正確的引數之外，錯誤並不是特別可採取動作。</span><span class="sxs-lookup"><span data-stu-id="c50ef-120">Errors are not particularly actionable except for incorrect arguments.</span></span>

<span data-ttu-id="c50ef-121">任何 API 呼叫可能會傳回標準 RPC 錯誤碼，因為它們是跨進程。</span><span class="sxs-lookup"><span data-stu-id="c50ef-121">Standard RPC error codes may be returned by any of the API calls because they are out-of-proc.</span></span> <span data-ttu-id="c50ef-122">標準 RPC 超時適用。</span><span class="sxs-lookup"><span data-stu-id="c50ef-122">Standard RPC timeouts apply.</span></span>

## <a name="security"></a><span data-ttu-id="c50ef-123">安全性</span><span class="sxs-lookup"><span data-stu-id="c50ef-123">Security</span></span>

<span data-ttu-id="c50ef-124">拼寫檢查 API 可能會)  (的拼寫檢查提供者載入外部程式碼。</span><span class="sxs-lookup"><span data-stu-id="c50ef-124">The Spell Checking API may load external code (spell check providers).</span></span> <span data-ttu-id="c50ef-125">它會在進程外執行此程式碼，並在受限制的安全性內容下執行。</span><span class="sxs-lookup"><span data-stu-id="c50ef-125">It will run this code out-of-proc and under a restricted security context.</span></span>

## <a name="dictionary-files"></a><span data-ttu-id="c50ef-126">字典檔</span><span class="sxs-lookup"><span data-stu-id="c50ef-126">Dictionary files</span></span>

<span data-ttu-id="c50ef-127">語言的使用者專屬詞典（包含新增、排除和自動換行清單的內容）位於% AppData% \\ Microsoft \\ 拼寫下 \\ *<language tag>* 。</span><span class="sxs-lookup"><span data-stu-id="c50ef-127">The user-specific dictionaries for a language, which hold the content for the Added, Excluded, and AutoCorrect word lists, are located under %AppData%\\Microsoft\\Spelling\\*<language tag>*.</span></span> <span data-ttu-id="c50ef-128">檔案名是預設值。 scripting.dic (新增) ，專有 (排除) 和預設值。 acl (自動校正) 。</span><span class="sxs-lookup"><span data-stu-id="c50ef-128">The filenames are default.dic (Added), default.exc (Excluded) and default.acl (AutoCorrect).</span></span> <span data-ttu-id="c50ef-129">這些檔案是 UTF-16 LE 純文字，必須以適當的位元組順序標記 (BOM) 來開頭。</span><span class="sxs-lookup"><span data-stu-id="c50ef-129">The files are UTF-16 LE plaintext that must start with the appropriate Byte Order Mark (BOM).</span></span> <span data-ttu-id="c50ef-130">每一行都包含新增和排除的字組清單中的單字 () ，或自動校正字組（以分隔號分隔的單字） ( " \| " )  (在 [自動校正字組] 清單) 中。</span><span class="sxs-lookup"><span data-stu-id="c50ef-130">Each line contains a word (in the Added and Excluded word lists), or an autocorrect pair with the words separated by a vertical bar ("\|") (in the AutoCorrect word list).</span></span> <span data-ttu-id="c50ef-131">目錄中的 scripting.dic、. 專有和 acl 檔案將會由拼寫檢查服務偵測，並新增至使用者字組清單。</span><span class="sxs-lookup"><span data-stu-id="c50ef-131">Other .dic, .exc, and .acl files present in the directory will be detected by the spell checking service and added to the user word lists.</span></span> <span data-ttu-id="c50ef-132">這些檔案會被視為唯讀，且不會由拼寫檢查 API 修改。</span><span class="sxs-lookup"><span data-stu-id="c50ef-132">These files are considered to be read-only and are not modified by the spell checking API.</span></span>

## <a name="installing-a-spell-checking-provider"></a><span data-ttu-id="c50ef-133">安裝拼寫檢查提供者</span><span class="sxs-lookup"><span data-stu-id="c50ef-133">Installing a spell checking provider</span></span>

<span data-ttu-id="c50ef-134">安裝拼寫檢查提供者時，必須將它所使用的所有檔案都放在允許從 SID ([安全識別碼](../secauthz/security-identifiers.md)) 「所有應用程式封裝」中讀取權限的位置。</span><span class="sxs-lookup"><span data-stu-id="c50ef-134">The installation of a spell checking provider must place all the files it uses in a location that allows read access from the SID ([security identifier](../secauthz/security-identifiers.md)) "ALL APPLICATION PACKAGES".</span></span> <span data-ttu-id="c50ef-135">將它安裝在 [Program Files] 下的資料夾也可以正常運作。</span><span class="sxs-lookup"><span data-stu-id="c50ef-135">Installing it in a folder under "Program Files" works well.</span></span> <span data-ttu-id="c50ef-136">此外，提供者必須在登錄中設定一些索引鍵，才能讓它出現在拼寫檢查 API 中。</span><span class="sxs-lookup"><span data-stu-id="c50ef-136">Also, the provider must set some keys in the registry for it to appear to the spell checking API.</span></span> <span data-ttu-id="c50ef-137">它可以位於 HKEY \_ CURRENT \_ user HIVE 或 HKEY \_ 本機電腦 hive 中， \_ 取決於它是否應該僅針對目前的使用者或所有使用者進行安裝。</span><span class="sxs-lookup"><span data-stu-id="c50ef-137">It can be in either the HKEY\_CURRENT\_USER hive or the HKEY\_LOCAL\_MACHINE hive depending on whether it should install only for the current user or all users.</span></span>


```
Key: <Registry hive>\SOFTWARE\Classes\CLSID\<Server CLSID>
     Default (REG_SZ) = <Name of the provider>

Key: <Registry hive>\SOFTWARE\Classes\CLSID\<Server CLSID>\InprocServer32
     ThreadingModel (REG_SZ) = "Both"

Key: <Registry hive>\SOFTWARE\Classes\CLSID\<Server CLSID>\Version
     Version (REG_SZ) = <Version>

Key: <Registry hive>\SOFTWARE\Microsoft\Spelling\Spellers\<Provider id string>
     CLSID (REG_SZ) = <CLSID of the COM Server that implements the provider>
```



<span data-ttu-id="c50ef-138">[拼寫檢查提供者範例](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SpellCheckerProvider)提供安裝提供者所需的註冊範例。</span><span class="sxs-lookup"><span data-stu-id="c50ef-138">The [spell checking provider sample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SpellCheckerProvider) provides an example of the registration needed to install a provider.</span></span>

<span data-ttu-id="c50ef-139">如果您要為拼寫檢查提供者建立新的拼寫檢查選項，請參閱 [**IOptionDescription：： Id**](/windows/desktop/api/Spellcheck/nf-spellcheck-ioptiondescription-get_id) 以取得命名指引。</span><span class="sxs-lookup"><span data-stu-id="c50ef-139">If you are creating new spell checking options for a spell checking provider, see [**IOptionDescription::Id**](/windows/desktop/api/Spellcheck/nf-spellcheck-ioptiondescription-get_id) for guidance on naming.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c50ef-140">相關主題</span><span class="sxs-lookup"><span data-stu-id="c50ef-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c50ef-141">拼寫檢查 API 參考</span><span class="sxs-lookup"><span data-stu-id="c50ef-141">Spell Checking API Reference</span></span>](spell-checker-api-reference.md)
</dt> <dt>

[<span data-ttu-id="c50ef-142">拼寫檢查用戶端範例</span><span class="sxs-lookup"><span data-stu-id="c50ef-142">Spell checking client sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SpellCheckerClient)
</dt> <dt>

[<span data-ttu-id="c50ef-143">拼寫檢查提供者範例</span><span class="sxs-lookup"><span data-stu-id="c50ef-143">Spell checking provider sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SpellCheckerProvider)
</dt> <dt>

[<span data-ttu-id="c50ef-144">**IOptionDescription：： Id**</span><span class="sxs-lookup"><span data-stu-id="c50ef-144">**IOptionDescription::Id**</span></span>](/windows/desktop/api/Spellcheck/nf-spellcheck-ioptiondescription-get_id)
</dt> <dt>

[<span data-ttu-id="c50ef-145">**IEnumString**</span><span class="sxs-lookup"><span data-stu-id="c50ef-145">**IEnumString**</span></span>](/windows/win32/api/objidlbase/nn-objidlbase-ienumstring)
</dt> <dt>

<span data-ttu-id="c50ef-146">[**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span><span class="sxs-lookup"><span data-stu-id="c50ef-146">[**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span></span>
</dt> </dl>

 

 

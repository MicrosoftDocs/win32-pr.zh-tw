---
description: Shell 會使用程式設計識別碼 (ProgID) 登錄子機碼，以將檔案類型與應用程式產生關聯，以及控制關聯的行為。
ms.assetid: f2b666d6-bf22-47b5-87e1-8de5ff51c152
title: 程式設計識別碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67720fed1ad4b8401d11f6532cdc79836911e7cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991078"
---
# <a name="programmatic-identifiers"></a><span data-ttu-id="ffe42-103">程式設計識別碼</span><span class="sxs-lookup"><span data-stu-id="ffe42-103">Programmatic Identifiers</span></span>

<span data-ttu-id="ffe42-104">Shell 會使用程式設計識別碼 (ProgID) 登錄子機碼，以將檔案類型與應用程式產生關聯，以及控制關聯的行為。</span><span class="sxs-lookup"><span data-stu-id="ffe42-104">The Shell uses a programmatic identifier (ProgID) registry subkey to associate a file type with an application, and to control the behavior of the association.</span></span> <span data-ttu-id="ffe42-105">用於檔案關聯的 ProgID 專案位於登錄的 **HKEY \_ 類別 \_ 根目錄** 下。</span><span class="sxs-lookup"><span data-stu-id="ffe42-105">The ProgID entries used for file associations are located under **HKEY\_CLASSES\_ROOT** in the registry.</span></span>

<span data-ttu-id="ffe42-106">本主題的組織方式如下：</span><span class="sxs-lookup"><span data-stu-id="ffe42-106">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="ffe42-107">檔案關聯所使用的程式設計識別碼元素</span><span class="sxs-lookup"><span data-stu-id="ffe42-107">Programmatic Identifier Elements Used by File Associations</span></span>](#programmatic-identifier-elements-used-by-file-associations)
-   [<span data-ttu-id="ffe42-108">使用已建立版本的程式設計識別碼</span><span class="sxs-lookup"><span data-stu-id="ffe42-108">Using Versioned Programmatic Identifiers</span></span>](#using-versioned-programmatic-identifiers)
-   [<span data-ttu-id="ffe42-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="ffe42-109">Related topics</span></span>](#related-topics)

<span data-ttu-id="ffe42-110">如需詳細資訊，請參閱 [如何註冊新應用程式的檔案類型](how-to-register-a-file-type-for-a-new-application.md)</span><span class="sxs-lookup"><span data-stu-id="ffe42-110">For additional information, read [How To Register a File Type for a New Application](how-to-register-a-file-type-for-a-new-application.md)</span></span>

## <a name="programmatic-identifier-elements-used-by-file-associations"></a><span data-ttu-id="ffe42-111">檔案關聯所使用的程式設計識別碼元素</span><span class="sxs-lookup"><span data-stu-id="ffe42-111">Programmatic Identifier Elements Used by File Associations</span></span>

<span data-ttu-id="ffe42-112">ProgID 金鑰名稱的正確格式為「 \[ *廠商」或「應用程式*」 \] 。 \[*元件* \] 。 \[*版本* \] ，以句號分隔，而且沒有空格，如 Word.Doc>ument 6。</span><span class="sxs-lookup"><span data-stu-id="ffe42-112">The proper format of a ProgID key name is \[*Vendor or Application*\].\[*Component*\].\[*Version*\], separated by periods and with no spaces, as in Word.Document.6.</span></span> <span data-ttu-id="ffe42-113">*版本* 部分是選擇性的，但強烈建議使用。</span><span class="sxs-lookup"><span data-stu-id="ffe42-113">The *Version* portion is optional but strongly recommended.</span></span> <span data-ttu-id="ffe42-114">如需詳細資訊，請參閱使用已建立版本的程式 [設計識別碼](#using-versioned-programmatic-identifiers)。</span><span class="sxs-lookup"><span data-stu-id="ffe42-114">For more information, see [Using Versioned Programmatic Identifiers](#using-versioned-programmatic-identifiers).</span></span>

<span data-ttu-id="ffe42-115">ProgID 子機碼應包含下列元素。</span><span class="sxs-lookup"><span data-stu-id="ffe42-115">A ProgID subkey should include the following elements.</span></span> <span data-ttu-id="ffe42-116">請注意，此機碼中的某些字串資料需要特定的格式。</span><span class="sxs-lookup"><span data-stu-id="ffe42-116">Note that some string data in this key requires specific formatting.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ffe42-117">元素</span><span class="sxs-lookup"><span data-stu-id="ffe42-117">Element</span></span></th>
<th><span data-ttu-id="ffe42-118">描述</span><span class="sxs-lookup"><span data-stu-id="ffe42-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ffe42-119"><strong> (預設) </strong></span><span class="sxs-lookup"><span data-stu-id="ffe42-119"><strong>(Default)</strong></span></span></td>
<td><span data-ttu-id="ffe42-120">將 ProgID 子機碼的預設專案設定為該 ProgID 的易記名稱，適合顯示給使用者。</span><span class="sxs-lookup"><span data-stu-id="ffe42-120">Set the default entry of the ProgID subkey to a friendly name for that ProgID, suitable to display to the user.</span></span> <span data-ttu-id="ffe42-121">在執行 Windows 2000 或更新版本的系統上，FriendlyTypeName 專案會取代使用此專案來保存易記名稱。</span><span class="sxs-lookup"><span data-stu-id="ffe42-121">The use of this entry to hold the friendly name is deprecated by the FriendlyTypeName entry on systems running Windows 2000 or later.</span></span> <span data-ttu-id="ffe42-122">不過，您應該將此值設定為回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="ffe42-122">However, you should set this value for backward compatibility.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ffe42-123"><strong>AllowSilentDefaultTakeOver</strong> (Windows 8) 引進</span><span class="sxs-lookup"><span data-stu-id="ffe42-123"><strong>AllowSilentDefaultTakeOver</strong> (introduced in Windows 8)</span></span></td>
<td><span data-ttu-id="ffe42-124">設定此選用專案，以指出當您決定公用檔案類型的預設處理常式時，Windows 應忽略此 ProgID。</span><span class="sxs-lookup"><span data-stu-id="ffe42-124">Set this optional entry to signal that Windows should ignore this ProgID when determining a default handler for a public file type.</span></span> <span data-ttu-id="ffe42-125">不論是否已設定此值，ProgID 都會繼續出現在 OpenWith 快捷方式功能表和對話方塊中。</span><span class="sxs-lookup"><span data-stu-id="ffe42-125">Regardless of whether this value is set, the ProgID continues to appear in the OpenWith shortcut menu and dialog.</span></span> <span data-ttu-id="ffe42-126">這是 REG_NONE 的值。</span><span class="sxs-lookup"><span data-stu-id="ffe42-126">This is a REG_NONE value.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ffe42-127"> (在 Windows 7) 引進的<strong>AppUserModelID</strong></span><span class="sxs-lookup"><span data-stu-id="ffe42-127"><strong>AppUserModelID</strong> (introduced in Windows 7)</span></span></td>
<td><span data-ttu-id="ffe42-128">將此選擇性專案設定為應用程式的明確應用程式使用者模型識別碼 (AppUserModelID) 如果應用程式使用明確的 AppUserModelID，並使用系統自動產生的 <strong>最新</strong> 或 <strong>經常</strong> 跳躍的快捷方式清單，或提供自訂捷徑清單。</span><span class="sxs-lookup"><span data-stu-id="ffe42-128">Set this optional entry to the application's explicit Application User Model ID (AppUserModelID) if the application uses an explicit AppUserModelID and uses either the system's automatically generated <strong>Recent</strong> or <strong>Frequent</strong> Jump Lists or provides a custom Jump List.</span></span> <span data-ttu-id="ffe42-129">如果應用程式使用明確的 AppUserModelID 但未設定此值，則專案不會出現在該應用程式的快捷方式清單中。</span><span class="sxs-lookup"><span data-stu-id="ffe42-129">If an application uses an explicit AppUserModelID and does not set this value, items will not appear in that application's Jump Lists.</span></span> <span data-ttu-id="ffe42-130">這是 REG_SZ 字串。</span><span class="sxs-lookup"><span data-stu-id="ffe42-130">This is a REG_SZ string.</span></span> <span data-ttu-id="ffe42-131">如需詳細資訊，請參閱 <a href="appids.md">應用程式使用者模型識別碼 (AppUserModelIDs) </a>。</span><span class="sxs-lookup"><span data-stu-id="ffe42-131">For more information, see <a href="appids.md">Application User Model IDs (AppUserModelIDs)</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ffe42-132"><strong>EditFlags</strong></span><span class="sxs-lookup"><span data-stu-id="ffe42-132"><strong>EditFlags</strong></span></span></td>
<td><span data-ttu-id="ffe42-133">使用 <a href="/windows/desktop/api/Shlwapi/ne-shlwapi-filetypeattributeflags"><strong>FILETYPEATTRIBUTEFLAGS</strong></a> 列舉中的旗標設定此選擇性專案。</span><span class="sxs-lookup"><span data-stu-id="ffe42-133">Set this optional entry using flags from the <a href="/windows/desktop/api/Shlwapi/ne-shlwapi-filetypeattributeflags"><strong>FILETYPEATTRIBUTEFLAGS</strong></a> enumeration.</span></span> <span data-ttu-id="ffe42-134">EditFlags 專案會控制 Shell 處理連結至此 ProgID 之檔案類型的某些層面。</span><span class="sxs-lookup"><span data-stu-id="ffe42-134">The EditFlags entry controls some aspects of the Shell's handling of the file types linked to this ProgID.</span></span> <span data-ttu-id="ffe42-135">您也可以使用 EditFlags 專案，限制使用者可以使用檔案的屬性工作表來修改這些檔案類型的特定部分。</span><span class="sxs-lookup"><span data-stu-id="ffe42-135">You can also use the EditFlags entry to limit how much the user can modify certain aspects of these file types using a file's property sheet.</span></span> <span data-ttu-id="ffe42-136">用於 EditFlags 的 <strong>FILETYPEATTRIBUTEFLAGS</strong> 值是二進位值，可讓您將多個屬性結合成位 or 運算中的單一值。</span><span class="sxs-lookup"><span data-stu-id="ffe42-136">The <strong>FILETYPEATTRIBUTEFLAGS</strong> values used for EditFlags are binary values designed so that you can combine multiple attributes into a single value in a bitwise OR operation.</span></span> <span data-ttu-id="ffe42-137">這是 REG_DWORD 或 REG_BINARY 值。</span><span class="sxs-lookup"><span data-stu-id="ffe42-137">This is a REG_DWORD or REG_BINARY value.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ffe42-138"><strong>FriendlyTypeName</strong></span><span class="sxs-lookup"><span data-stu-id="ffe42-138"><strong>FriendlyTypeName</strong></span></span></td>
<td><span data-ttu-id="ffe42-139">將此專案設定為 ProgID 的易記名稱，適合顯示給使用者。</span><span class="sxs-lookup"><span data-stu-id="ffe42-139">Set this entry to a friendly name for the ProgID, suitable to display to the user.</span></span> <span data-ttu-id="ffe42-140">為求一致，此字串應該包含與此 ProgID 索引鍵的預設專案相同的資料。</span><span class="sxs-lookup"><span data-stu-id="ffe42-140">For consistency, this string should contain the same data as the Default entry for this ProgID key.</span></span> <span data-ttu-id="ffe42-141">這個專案可以是 REG_SZ 或 REG_EXPAND_SZ 字串，但必須格式化為間接字串 (完整的檔案名和資源值，並在前面加上 @ 符號) ，例如 <em>@% SystemRoot% \shell32.dll，-154</em>。</span><span class="sxs-lookup"><span data-stu-id="ffe42-141">This entry can be either a REG_SZ or REG_EXPAND_SZ string, but it must be formatted as an indirect string (a fully qualified file name and resource value preceded by the @ symbol), for instance <em>@%SystemRoot%\shell32.dll,-154</em>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ffe42-142"><strong>InfoTip</strong></span><span class="sxs-lookup"><span data-stu-id="ffe42-142"><strong>InfoTip</strong></span></span></td>
<td><span data-ttu-id="ffe42-143">將此專案設定為命令介面顯示此 ProgID 的簡短說明訊息。</span><span class="sxs-lookup"><span data-stu-id="ffe42-143">Set this entry to a brief help message that the Shell displays for this ProgID.</span></span> <span data-ttu-id="ffe42-144">[提示] 專案會顯示在滑鼠停留對話方塊中。</span><span class="sxs-lookup"><span data-stu-id="ffe42-144">The InfoTip entry displays in a mouse-over dialog box.</span></span> <span data-ttu-id="ffe42-145">這個值可以是 REG_SZ 或 REG_EXPAND_SZ 字串，但就像 FriendlyTypeName 一樣，它必須格式化為間接字串。</span><span class="sxs-lookup"><span data-stu-id="ffe42-145">This value can be either a REG_SZ or REG_EXPAND_SZ string but, like FriendlyTypeName, it must be formatted as an indirect string.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ffe42-146"><strong>CurVer</strong></span><span class="sxs-lookup"><span data-stu-id="ffe42-146"><strong>CurVer</strong></span></span></td>
<td><span data-ttu-id="ffe42-147">將此子機碼 (預設) 專案設定為此 ProgID 的最新版本。</span><span class="sxs-lookup"><span data-stu-id="ffe42-147">Set the (Default) entry of this subkey to the most current version of this ProgID.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="ffe42-148">除非您有並存的應用程式版本，也就是在相同的系統上安裝多個版本，所以您應該避免使用 <strong>CurVer</strong>。</span><span class="sxs-lookup"><span data-stu-id="ffe42-148">Unless you have side-by-side application versions, that is, multiple versions installed on the same system, you should avoid using <strong>CurVer</strong>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ffe42-149"><strong>DefaultIcon</strong>。</span><span class="sxs-lookup"><span data-stu-id="ffe42-149"><strong>DefaultIcon</strong>.</span></span></td>
<td><span data-ttu-id="ffe42-150">將此子機碼的 (預設) 專案設定為您想要針對與此 ProgID 相關聯的檔案類型顯示的預設圖示。</span><span class="sxs-lookup"><span data-stu-id="ffe42-150">Set the (Default) entry of this subkey to the default icon that you want to display for file types associated with this ProgID.</span></span> <span data-ttu-id="ffe42-151">此值可以是 REG_SZ 或 REG_EXPAND_SZ 字串，但必須以完整檔案名的形式提供，其具有其附隨的資源值，例如 <em>% SystemRoot% \shell32.dll，-154</em>。</span><span class="sxs-lookup"><span data-stu-id="ffe42-151">This value can be either a REG_SZ or REG_EXPAND_SZ string, but it must be provided as a fully qualified file name with its attendant resource value, for instance <em>%SystemRoot%\shell32.dll,-154</em>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="ffe42-152">下列登錄機碼範例說明檔案關聯 ProgID 索引鍵節點：</span><span class="sxs-lookup"><span data-stu-id="ffe42-152">The following registry key example illustrates a file association ProgID key node:</span></span>

```
HKEY_CLASSES_ROOT
   Vendor.App.1
      (Default) = My Friendly Name
      AllowSilentDefaultTakeOver
      AppUserModelID = Vendor.Application
      EditFlags = 0x00000001
      FriendlyTypeName = @%SystemRoot%\shell32.dll,-154
      InfoTip = @%SystemRoot%\shell32.dll,-54
      CurVer
         (Default) = Vendor.App.1
      DefaultIcon
         (Default) = %SystemRoot%\shell32.dll,-1
```

## <a name="using-versioned-programmatic-identifiers"></a><span data-ttu-id="ffe42-153">使用已建立版本的程式設計識別碼</span><span class="sxs-lookup"><span data-stu-id="ffe42-153">Using Versioned Programmatic Identifiers</span></span>

<span data-ttu-id="ffe42-154">版本設定的 ProgID 是在其名稱中表示版本的 ProgID。</span><span class="sxs-lookup"><span data-stu-id="ffe42-154">A versioned ProgID is one whose version is indicated in its name.</span></span> <span data-ttu-id="ffe42-155">您通常會將句點和版本號碼加入至名稱來完成這項作業。</span><span class="sxs-lookup"><span data-stu-id="ffe42-155">You typically do this by adding a period and the version number to the name.</span></span> <span data-ttu-id="ffe42-156">例如：</span><span class="sxs-lookup"><span data-stu-id="ffe42-156">For example:</span></span>

-   <span data-ttu-id="ffe42-157">Word.Doc>ument 6</span><span class="sxs-lookup"><span data-stu-id="ffe42-157">Word.Document.6</span></span>
-   <span data-ttu-id="ffe42-158">Word.Doc>ument 8</span><span class="sxs-lookup"><span data-stu-id="ffe42-158">Word.Document.8</span></span>

<span data-ttu-id="ffe42-159">這些是版本設定的 Progid，分別為6和8版。</span><span class="sxs-lookup"><span data-stu-id="ffe42-159">These are versioned ProgIDs, with versions 6 and 8 respectively.</span></span> <span data-ttu-id="ffe42-160">如果您有並存的應用程式，也就是同時安裝了支援多個應用程式版本的應用程式，則請使用 CurVer 與獨立版本的 Progid。</span><span class="sxs-lookup"><span data-stu-id="ffe42-160">If you have a side-by-side application, that is, one that supports multiple versions of your application installed at the same time, then use CurVer and Version Independent ProgIDs.</span></span> <span data-ttu-id="ffe42-161">否則，應該避免 CurVer 和版本獨立 Progid，因為它們會導致效率不好。</span><span class="sxs-lookup"><span data-stu-id="ffe42-161">Otherwise, CurVer and Version Independent ProgIDs should be avoided because they will lead to inefficiency.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ffe42-162">相關主題</span><span class="sxs-lookup"><span data-stu-id="ffe42-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ffe42-163">如何註冊新應用程式的檔案類型</span><span class="sxs-lookup"><span data-stu-id="ffe42-163">How To Register a File Type for a New Application</span></span>](how-to-register-a-file-type-for-a-new-application.md)
</dt> <dt>

[<span data-ttu-id="ffe42-164">應用程式註冊</span><span class="sxs-lookup"><span data-stu-id="ffe42-164">Application Registration</span></span>](app-registration.md)
</dt> <dt>

[<span data-ttu-id="ffe42-165">檔案類型</span><span class="sxs-lookup"><span data-stu-id="ffe42-165">File Types</span></span>](fa-file-types.md)
</dt> <dt>

[<span data-ttu-id="ffe42-166">檔案關聯的運作方式</span><span class="sxs-lookup"><span data-stu-id="ffe42-166">How File Associations Work</span></span>](fa-how-work.md)
</dt> <dt>

[<span data-ttu-id="ffe42-167">依檔案類型或種類的內容視圖</span><span class="sxs-lookup"><span data-stu-id="ffe42-167">Content View By File Type or Kind</span></span>](prophand-content-view.md)
</dt> <dt>

[<span data-ttu-id="ffe42-168">檔案類型驗證器</span><span class="sxs-lookup"><span data-stu-id="ffe42-168">File Type Verifier</span></span>](file-type-verifier.md)
</dt> <dt>

[<span data-ttu-id="ffe42-169">檔案類型處理常式</span><span class="sxs-lookup"><span data-stu-id="ffe42-169">File Type Handlers</span></span>](fa-file-extensions.md)
</dt> <dt>

[<span data-ttu-id="ffe42-170">認知類型</span><span class="sxs-lookup"><span data-stu-id="ffe42-170">Perceived Types</span></span>](fa-perceivedtypes.md)
</dt> <dt>

[<span data-ttu-id="ffe42-171">關聯陣列</span><span class="sxs-lookup"><span data-stu-id="ffe42-171">Association Arrays</span></span>](fa-associationarray.md)
</dt> </dl>

 

 





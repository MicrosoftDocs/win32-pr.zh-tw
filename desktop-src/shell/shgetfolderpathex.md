---
UID: ''
title: SHGetFolderPathEx 函式
description: 抓取 KNOWNFOLDERID 所識別之已知資料夾的路徑。
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: SHGetFolderPath
ms.topic: reference
req.header: Shlobj.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: Shell32.lib
req.dll: API-MS-Win-Storage-Exports-Internal-L1-1-0.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location:
- API-MS-Win-Storage-Exports-Internal-L1-1-0.dll
api_name:
- SHGetFolderPathEx
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: 0dfc3342f3eca5622c25d2df7319cd2323f516ff
ms.sourcegitcommit: 1f6a1bfc1c4bb2641bc3ba44beb1f2727c94681b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2020
ms.locfileid: "104971660"
---
# <a name="shgetfolderpathex-function"></a><span data-ttu-id="ad2fc-103">SHGetFolderPathEx 函式</span><span class="sxs-lookup"><span data-stu-id="ad2fc-103">SHGetFolderPathEx function</span></span>

## <a name="description"></a><span data-ttu-id="ad2fc-104">Description</span><span class="sxs-lookup"><span data-stu-id="ad2fc-104">Description</span></span>

<span data-ttu-id="ad2fc-105">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="ad2fc-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span>
<span data-ttu-id="ad2fc-106">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="ad2fc-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="ad2fc-107">抓取資料夾的 [KNOWNFOLDERID](/windows/desktop/shell/knownfolderid)所識別之已知資料夾的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="ad2fc-107">Retrieves the full path of a known folder identified by the folder's [KNOWNFOLDERID](/windows/desktop/shell/knownfolderid).</span></span>
<span data-ttu-id="ad2fc-108">這可讓您設定字串緩衝區的初始大小，藉此擴充 [SHGetKnownFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) 。</span><span class="sxs-lookup"><span data-stu-id="ad2fc-108">This extends [SHGetKnownFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) by allowing you to set the initial size of the string buffer.</span></span>

```cpp
HRESULT WINAPI SHGetFolderPathEx(
  _In_     REFKNOWNFOLDERID rfid,
  _In_     DWORD            dwFlags,
  _In_opt_ HANDLE           hToken,
  _Out_    LPWSTR           pszPath,
  _In_     UINT             cchPath
);
```

## <a name="parameters"></a><span data-ttu-id="ad2fc-109">參數</span><span class="sxs-lookup"><span data-stu-id="ad2fc-109">Parameters</span></span>

### <a name="rfid-in"></a><span data-ttu-id="ad2fc-110">rfid [in]</span><span class="sxs-lookup"><span data-stu-id="ad2fc-110">rfid [in]</span></span>

<span data-ttu-id="ad2fc-111">識別資料夾之 **KNOWNFOLDERID** 的參考。</span><span class="sxs-lookup"><span data-stu-id="ad2fc-111">A reference to the **KNOWNFOLDERID** that identifies the folder.</span></span>

### <a name="dwflags-in"></a><span data-ttu-id="ad2fc-112">dwFlags [in]</span><span class="sxs-lookup"><span data-stu-id="ad2fc-112">dwFlags [in]</span></span>

<span data-ttu-id="ad2fc-113">指定特殊抓取選項的旗標。</span><span class="sxs-lookup"><span data-stu-id="ad2fc-113">Flags that specify special retrieval options.</span></span>
<span data-ttu-id="ad2fc-114">這個值可以是 0;否則，會有一或多個 [KNOWN_FOLDER_FLAG](/windows/desktop/api/shlobj_core/ne-shlobj_core-known_folder_flag) 值。</span><span class="sxs-lookup"><span data-stu-id="ad2fc-114">This value can be 0; otherwise, one or more of the [KNOWN_FOLDER_FLAG](/windows/desktop/api/shlobj_core/ne-shlobj_core-known_folder_flag) values.</span></span>

### <a name="htoken-in-optional"></a><span data-ttu-id="ad2fc-115">hToken [in，optional]</span><span class="sxs-lookup"><span data-stu-id="ad2fc-115">hToken [in, optional]</span></span>

<span data-ttu-id="ad2fc-116">代表特定使用者的 [存取權杖](/windows/desktop/SecAuthZ/access-tokens) 。</span><span class="sxs-lookup"><span data-stu-id="ad2fc-116">An [access token](/windows/desktop/SecAuthZ/access-tokens) that represents a particular user.</span></span>
<span data-ttu-id="ad2fc-117">如果這個參數是 **Null**，這是最常見的使用方式，則函式會要求目前使用者的已知資料夾。</span><span class="sxs-lookup"><span data-stu-id="ad2fc-117">If this parameter is **NULL**, which is the most common usage, the function requests the known folder for the current user.</span></span>

<span data-ttu-id="ad2fc-118">藉由傳遞該使用者的 *hToken* 來要求特定使用者的資料夾。</span><span class="sxs-lookup"><span data-stu-id="ad2fc-118">Request a specific user's folder by passing the *hToken* of that user.</span></span>
<span data-ttu-id="ad2fc-119">這通常是在具有足夠許可權的服務內容中完成，以取得指定使用者的權杖。</span><span class="sxs-lookup"><span data-stu-id="ad2fc-119">This is typically done in the context of a service that has sufficient privileges to retrieve the token of a given user.</span></span>
<span data-ttu-id="ad2fc-120">該權杖必須以 [TOKEN_QUERY](/windows/desktop/SecAuthZ/access-rights-for-access-token-objects) 和 [TOKEN_IMPERSONATE](/windows/desktop/SecAuthZ/access-rights-for-access-token-objects) 許可權開啟。</span><span class="sxs-lookup"><span data-stu-id="ad2fc-120">That token must be opened with [TOKEN_QUERY](/windows/desktop/SecAuthZ/access-rights-for-access-token-objects) and [TOKEN_IMPERSONATE](/windows/desktop/SecAuthZ/access-rights-for-access-token-objects) rights.</span></span>
<span data-ttu-id="ad2fc-121">在某些情況下，您也必須包含 [TOKEN_DUPLICATE](/windows/desktop/SecAuthZ/access-rights-for-access-token-objects)。</span><span class="sxs-lookup"><span data-stu-id="ad2fc-121">In some cases, you also need to include [TOKEN_DUPLICATE](/windows/desktop/SecAuthZ/access-rights-for-access-token-objects).</span></span>
<span data-ttu-id="ad2fc-122">除了傳遞使用者的 *hToken* 之外，還必須裝載該特定使用者的登錄 hive。</span><span class="sxs-lookup"><span data-stu-id="ad2fc-122">In addition to passing the user's *hToken*, the registry hive of that specific user must be mounted.</span></span>
<span data-ttu-id="ad2fc-123">如需存取控制問題的進一步討論，請參閱 [存取控制](/windows/desktop/SecAuthZ/access-control) 。</span><span class="sxs-lookup"><span data-stu-id="ad2fc-123">See [Access Control](/windows/desktop/SecAuthZ/access-control) for further discussion of access control issues.</span></span>

<span data-ttu-id="ad2fc-124">指派 *hToken* 參數-1 的值表示預設使用者。</span><span class="sxs-lookup"><span data-stu-id="ad2fc-124">Assigning the *hToken* parameter a value of -1 indicates the Default User.</span></span>
<span data-ttu-id="ad2fc-125">這可讓 [SHGetKnownFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) 的用戶端找到資料夾位置 (例如，預設使用者的 **桌面** 資料夾) 。</span><span class="sxs-lookup"><span data-stu-id="ad2fc-125">This allows clients of [SHGetKnownFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) to find folder locations (such as the **Desktop** folder) for the Default User.</span></span>
<span data-ttu-id="ad2fc-126">建立任何新的使用者帳戶時，預設的使用者使用者設定檔會重複，並包含 **檔** 和 **桌面** 等特殊資料夾。</span><span class="sxs-lookup"><span data-stu-id="ad2fc-126">The Default User user profile is duplicated when any new user account is created, and includes special folders such as **Documents** and **Desktop**.</span></span>
<span data-ttu-id="ad2fc-127">任何新增至預設使用者資料夾的專案也會出現在任何新的使用者帳戶中。</span><span class="sxs-lookup"><span data-stu-id="ad2fc-127">Any items added to the Default User folder also appear in any new user account.</span></span>
<span data-ttu-id="ad2fc-128">請注意，存取預設使用者資料夾需要系統管理員許可權。</span><span class="sxs-lookup"><span data-stu-id="ad2fc-128">Note that access to the Default User folders requires administrator privileges.</span></span>

### <a name="pszpath-out"></a><span data-ttu-id="ad2fc-129">pszPath [out]</span><span class="sxs-lookup"><span data-stu-id="ad2fc-129">pszPath [out]</span></span>

<span data-ttu-id="ad2fc-130">以 null 結束的 Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="ad2fc-130">A null-terminated, Unicode string.</span></span>
<span data-ttu-id="ad2fc-131">這個緩衝區的大小必須是 cchPath。</span><span class="sxs-lookup"><span data-stu-id="ad2fc-131">This buffer must be of size cchPath.</span></span>
<span data-ttu-id="ad2fc-132">當 **SHGetFolderPathEx** 成功傳回時，此參數會包含已知資料夾的路徑。</span><span class="sxs-lookup"><span data-stu-id="ad2fc-132">When **SHGetFolderPathEx** returns successfully, this parameter contains the path for the known folder.</span></span>

### <a name="cchpath-in"></a><span data-ttu-id="ad2fc-133">cchPath [in]</span><span class="sxs-lookup"><span data-stu-id="ad2fc-133">cchPath [in]</span></span>

<span data-ttu-id="ad2fc-134">*PpszPath* 緩衝區的大小（以字元為單位）。</span><span class="sxs-lookup"><span data-stu-id="ad2fc-134">The size of the *ppszPath* buffer, in characters.</span></span>

## <a name="returns"></a><span data-ttu-id="ad2fc-135">傳回</span><span class="sxs-lookup"><span data-stu-id="ad2fc-135">Returns</span></span>

<span data-ttu-id="ad2fc-136">如果成功，則傳回 **S_OK** ，否則傳回錯誤值。</span><span class="sxs-lookup"><span data-stu-id="ad2fc-136">Returns **S_OK** if successful, or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad2fc-137">備註</span><span class="sxs-lookup"><span data-stu-id="ad2fc-137">Remarks</span></span>

<span data-ttu-id="ad2fc-138">因為 [SHGetFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) 是 [SHGetKnownFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath)的包裝函式，所以此函式 (**SHGetFolderPathEx**) 也可作為 **SHGetFolderPath** 的擴充功能。</span><span class="sxs-lookup"><span data-stu-id="ad2fc-138">Since [SHGetFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) is a wrapper for [SHGetKnownFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath), this function (**SHGetFolderPathEx**) also serves as an extension to **SHGetFolderPath**.</span></span>

## <a name="see-also"></a><span data-ttu-id="ad2fc-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ad2fc-139">See also</span></span>

[<span data-ttu-id="ad2fc-140">KNOWNFOLDERID</span><span class="sxs-lookup"><span data-stu-id="ad2fc-140">KNOWNFOLDERID</span></span>](/windows/desktop/shell/knownfolderid)

[<span data-ttu-id="ad2fc-141">KNOWN_FOLDER_FLAG</span><span class="sxs-lookup"><span data-stu-id="ad2fc-141">KNOWN_FOLDER_FLAG</span></span>](/windows/desktop/api/shlobj_core/ne-shlobj_core-known_folder_flag)

[<span data-ttu-id="ad2fc-142">SHGetFolderPath</span><span class="sxs-lookup"><span data-stu-id="ad2fc-142">SHGetFolderPath</span></span>](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha)

[<span data-ttu-id="ad2fc-143">SHGetKnownFolderIDList</span><span class="sxs-lookup"><span data-stu-id="ad2fc-143">SHGetKnownFolderIDList</span></span>](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderidlist)

[<span data-ttu-id="ad2fc-144">SHGetKnownFolderPath</span><span class="sxs-lookup"><span data-stu-id="ad2fc-144">SHGetKnownFolderPath</span></span>](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath)

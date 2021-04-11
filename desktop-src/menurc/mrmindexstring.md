---
title: 'MrmIndexString 函式 (MrmResourceIndexer) '
description: 為屬於 UWP 應用程式的單一字串資源編制索引。
ms.assetid: 098F47E7-4BEC-452F-A33C-111F3F524E67
keywords:
- MrmIndexString 函式功能表與其他資源
topic_type:
- apiref
api_name:
- MrmIndexString
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec0c81155ae2484dd38f29e332a5f0093b07cd9a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104093939"
---
# <a name="mrmindexstring-function"></a><span data-ttu-id="db5b6-104">MrmIndexString 函式</span><span class="sxs-lookup"><span data-stu-id="db5b6-104">MrmIndexString function</span></span>

<span data-ttu-id="db5b6-105">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="db5b6-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="db5b6-106">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="db5b6-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="db5b6-107">為屬於 UWP 應用程式的單一字串資源編制索引。</span><span class="sxs-lookup"><span data-stu-id="db5b6-107">Indexes a single string resource belonging to a UWP app.</span></span> <span data-ttu-id="db5b6-108">接受明確 (，但) 資源限定詞的選擇性清單。</span><span class="sxs-lookup"><span data-stu-id="db5b6-108">Takes an explicit (but optional) list of resource qualifiers.</span></span> <span data-ttu-id="db5b6-109">如需詳細資訊，以及如何使用這些 Api 的案例式逐步解說，請參閱 [封裝資源索引 (PRI) api 和自訂群組建系統](/windows/uwp/app-resources/pri-apis-custom-build-systems)。</span><span class="sxs-lookup"><span data-stu-id="db5b6-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="db5b6-110">語法</span><span class="sxs-lookup"><span data-stu-id="db5b6-110">Syntax</span></span>


```C++
HRESULT HRESULT MrmIndexString(
  _In_     MrmResourceIndexerHandle indexer,
  _In_     PCWSTR                   resourceUri,
  _In_     PCWSTR                   resourceString,
  _In_opt_ PCWSTR                   qualifiers
);
```



## <a name="parameters"></a><span data-ttu-id="db5b6-111">參數</span><span class="sxs-lookup"><span data-stu-id="db5b6-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db5b6-112">*索引子* \[在\]</span><span class="sxs-lookup"><span data-stu-id="db5b6-112">*indexer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db5b6-113">類型： **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span><span class="sxs-lookup"><span data-stu-id="db5b6-113">Type: **[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span></span>

<span data-ttu-id="db5b6-114">識別將為字串資源編制索引之資源索引子的控制碼。</span><span class="sxs-lookup"><span data-stu-id="db5b6-114">A handle identifying the resource indexer that will index the string resources.</span></span>

</dd> <dt>

<span data-ttu-id="db5b6-115">*resourceUri* \[在\]</span><span class="sxs-lookup"><span data-stu-id="db5b6-115">*resourceUri* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db5b6-116">類型： **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="db5b6-116">Type: **PCWSTR**</span></span>

<span data-ttu-id="db5b6-117">要指派給資源的資源 URI。</span><span class="sxs-lookup"><span data-stu-id="db5b6-117">The resource URI to assign to the resource.</span></span> <span data-ttu-id="db5b6-118">當您稍後從此資源索引子產生 PRI 檔案時，會使用此路徑做為此資源的資源對應子樹名稱。</span><span class="sxs-lookup"><span data-stu-id="db5b6-118">The path will be used as the resource map subtree name for this resource when you later generate a PRI file from this resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="db5b6-119">*resourceString* \[在\]</span><span class="sxs-lookup"><span data-stu-id="db5b6-119">*resourceString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db5b6-120">類型： **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="db5b6-120">Type: **PCWSTR**</span></span>

<span data-ttu-id="db5b6-121">字串資源的值。</span><span class="sxs-lookup"><span data-stu-id="db5b6-121">The value of the string resource.</span></span>

</dd> <dt>

<span data-ttu-id="db5b6-122">*限定詞* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="db5b6-122">*qualifiers* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="db5b6-123">類型： **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="db5b6-123">Type: **PCWSTR**</span></span>

<span data-ttu-id="db5b6-124">選擇性的資源限定詞清單，例如 L "language-en-us \_ scale-100 \_ 對比-標準"。</span><span class="sxs-lookup"><span data-stu-id="db5b6-124">An optional list of resource qualifiers, for example L"language-en-US\_scale-100\_contrast-standard".</span></span> <span data-ttu-id="db5b6-125">空字串或 **nullptr** 表示中立的資源。</span><span class="sxs-lookup"><span data-stu-id="db5b6-125">An empty string or **nullptr** indicates a neutral resource.</span></span> <span data-ttu-id="db5b6-126">系統 *不* 會從 *resourceUri* 推斷資源限定詞。</span><span class="sxs-lookup"><span data-stu-id="db5b6-126">Resource qualifiers are *not* inferred from *resourceUri*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db5b6-127">傳回值</span><span class="sxs-lookup"><span data-stu-id="db5b6-127">Return value</span></span>

<span data-ttu-id="db5b6-128">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="db5b6-128">Type: **HRESULT**</span></span>

<span data-ttu-id="db5b6-129">如果函式 \_ 成功，則為 [正常]，否則為其他值。</span><span class="sxs-lookup"><span data-stu-id="db5b6-129">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="db5b6-130">使用 winerror.h 中定義的成功 () 或失敗 ()  (宏) ，判斷成功或失敗。</span><span class="sxs-lookup"><span data-stu-id="db5b6-130">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="db5b6-131">備註</span><span class="sxs-lookup"><span data-stu-id="db5b6-131">Remarks</span></span>

<span data-ttu-id="db5b6-132">如果您想要指定任何資源限定詞，請在 *限定詞* 參數中傳遞它們。</span><span class="sxs-lookup"><span data-stu-id="db5b6-132">If you want to specify any resource qualifiers, then pass them in the *qualifiers* parameter.</span></span> <span data-ttu-id="db5b6-133">系統 *不* 會從 *resourceUri* 推斷資源限定詞。</span><span class="sxs-lookup"><span data-stu-id="db5b6-133">Resource qualifiers are *not* inferred from *resourceUri*.</span></span>

<span data-ttu-id="db5b6-134">使用 *resourceUri* 的檔案名區段做為資源名稱。</span><span class="sxs-lookup"><span data-stu-id="db5b6-134">The file name segment of *resourceUri* is used as the resource name.</span></span>

## <a name="requirements"></a><span data-ttu-id="db5b6-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="db5b6-135">Requirements</span></span>



| <span data-ttu-id="db5b6-136">需求</span><span class="sxs-lookup"><span data-stu-id="db5b6-136">Requirement</span></span> | <span data-ttu-id="db5b6-137">值</span><span class="sxs-lookup"><span data-stu-id="db5b6-137">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db5b6-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="db5b6-138">Minimum supported client</span></span><br/> | <span data-ttu-id="db5b6-139">Windows 10， \[ 僅限1803版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="db5b6-139">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="db5b6-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="db5b6-140">Minimum supported server</span></span><br/> | <span data-ttu-id="db5b6-141">\[僅限 Windows Server desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="db5b6-141">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="db5b6-142">標頭</span><span class="sxs-lookup"><span data-stu-id="db5b6-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="db5b6-143"><dt>MrmResourceIndexer。h</dt></span><span class="sxs-lookup"><span data-stu-id="db5b6-143"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="db5b6-144">程式庫</span><span class="sxs-lookup"><span data-stu-id="db5b6-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="db5b6-145"><dt>Mrmsupport .lib</dt></span><span class="sxs-lookup"><span data-stu-id="db5b6-145"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="db5b6-146">DLL</span><span class="sxs-lookup"><span data-stu-id="db5b6-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="db5b6-147"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db5b6-147"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="db5b6-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="db5b6-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db5b6-149">套件資源索引 (PRI) API 和自訂建置系統</span><span class="sxs-lookup"><span data-stu-id="db5b6-149">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 


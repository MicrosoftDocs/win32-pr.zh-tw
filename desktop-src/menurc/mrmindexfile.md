---
title: 'MrmIndexFile 函式 (MrmResourceIndexer) '
description: 編制屬於 UWP 應用程式的資源檔索引。 接受明確 (，但) 資源限定詞的選擇性清單。 如需詳細資訊，以及如何使用這些 Api 的案例式逐步解說，請參閱封裝資源索引 (PRI) Api 和自訂群組建系統。
ms.assetid: C9F245B4-D2D3-4863-BB64-72619FC73D3C
keywords:
- MrmIndexFile 函式功能表與其他資源
topic_type:
- apiref
api_name:
- MrmIndexFile
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9db3e0521f954a2d5d5e0286fb6f21b8e5f55eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466593"
---
# <a name="mrmindexfile-function"></a><span data-ttu-id="235a2-106">MrmIndexFile 函式</span><span class="sxs-lookup"><span data-stu-id="235a2-106">MrmIndexFile function</span></span>

<span data-ttu-id="235a2-107">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="235a2-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="235a2-108">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="235a2-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="235a2-109">編制屬於 UWP 應用程式的資源檔索引。</span><span class="sxs-lookup"><span data-stu-id="235a2-109">Indexes a resource file belonging to a UWP app.</span></span> <span data-ttu-id="235a2-110">接受明確 (，但) 資源限定詞的選擇性清單。</span><span class="sxs-lookup"><span data-stu-id="235a2-110">Takes an explicit (but optional) list of resource qualifiers.</span></span> <span data-ttu-id="235a2-111">如需詳細資訊，以及如何使用這些 Api 的案例式逐步解說，請參閱 [封裝資源索引 (PRI) api 和自訂群組建系統](/windows/uwp/app-resources/pri-apis-custom-build-systems)。</span><span class="sxs-lookup"><span data-stu-id="235a2-111">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="235a2-112">語法</span><span class="sxs-lookup"><span data-stu-id="235a2-112">Syntax</span></span>


```C++
HRESULT HRESULT MrmIndexFile(
  _In_     MrmResourceIndexerHandle indexer,
  _In_     PCWSTR                   resourceUri,
  _In_     PCWSTR                   filePath,
  _In_opt_ PCWSTR                   qualifiers
);
```



## <a name="parameters"></a><span data-ttu-id="235a2-113">參數</span><span class="sxs-lookup"><span data-stu-id="235a2-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="235a2-114">*索引子* \[在\]</span><span class="sxs-lookup"><span data-stu-id="235a2-114">*indexer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="235a2-115">類型： **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span><span class="sxs-lookup"><span data-stu-id="235a2-115">Type: **[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span></span>

<span data-ttu-id="235a2-116">識別將為資源檔編制索引之資源索引子的控制碼。</span><span class="sxs-lookup"><span data-stu-id="235a2-116">A handle identifying the resource indexer that will index the resource file.</span></span>

</dd> <dt>

<span data-ttu-id="235a2-117">*resourceUri* \[在\]</span><span class="sxs-lookup"><span data-stu-id="235a2-117">*resourceUri* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="235a2-118">類型： **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="235a2-118">Type: **PCWSTR**</span></span>

<span data-ttu-id="235a2-119">要指派給資源的資源 URI。</span><span class="sxs-lookup"><span data-stu-id="235a2-119">The resource URI to assign to the resource.</span></span> <span data-ttu-id="235a2-120">當您稍後從此資源索引子產生 PRI 檔案時，會使用此路徑做為此資源的資源對應子樹名稱。</span><span class="sxs-lookup"><span data-stu-id="235a2-120">The path will be used as the resource map subtree name for this resource when you later generate a PRI file from this resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="235a2-121">*filePath* \[在\]</span><span class="sxs-lookup"><span data-stu-id="235a2-121">*filePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="235a2-122">類型： **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="235a2-122">Type: **PCWSTR**</span></span>

<span data-ttu-id="235a2-123">檔案的相對路徑，該檔案包含您想要編制索引的資源。</span><span class="sxs-lookup"><span data-stu-id="235a2-123">A relative path to a file containing a resource that you want to index.</span></span> <span data-ttu-id="235a2-124">此路徑相對於您要產生 PRI 檔案之 UWP 應用程式的專案根目錄。</span><span class="sxs-lookup"><span data-stu-id="235a2-124">This path is relative to the project root of the UWP app for which you are generating PRI files.</span></span> <span data-ttu-id="235a2-125">該專案根目錄是您傳遞至 [**MrmCreateResourceIndexer**](mrmcreateresourceindexer.md)的 *projectRoot* 值。</span><span class="sxs-lookup"><span data-stu-id="235a2-125">That project root is the value of *projectRoot* that you passed to [**MrmCreateResourceIndexer**](mrmcreateresourceindexer.md).</span></span>

</dd> <dt>

<span data-ttu-id="235a2-126">*限定詞* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="235a2-126">*qualifiers* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="235a2-127">類型： **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="235a2-127">Type: **PCWSTR**</span></span>

<span data-ttu-id="235a2-128">選擇性的資源限定詞清單，例如 L "language-en-us \_ scale-100 \_ 對比-標準"。</span><span class="sxs-lookup"><span data-stu-id="235a2-128">An optional list of resource qualifiers, for example L"language-en-US\_scale-100\_contrast-standard".</span></span> <span data-ttu-id="235a2-129">空字串或 **nullptr** 表示中立的資源。</span><span class="sxs-lookup"><span data-stu-id="235a2-129">An empty string or **nullptr** indicates a neutral resource.</span></span> <span data-ttu-id="235a2-130">資源限定詞 *不* 會從 *resourceUri* 或 *containerPath* 推斷。</span><span class="sxs-lookup"><span data-stu-id="235a2-130">Resource qualifiers are *not* inferred from *resourceUri* nor from *containerPath*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="235a2-131">傳回值</span><span class="sxs-lookup"><span data-stu-id="235a2-131">Return value</span></span>

<span data-ttu-id="235a2-132">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="235a2-132">Type: **HRESULT**</span></span>

<span data-ttu-id="235a2-133">如果函式 \_ 成功，則為 [正常]，否則為其他值。</span><span class="sxs-lookup"><span data-stu-id="235a2-133">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="235a2-134">使用 winerror.h 中定義的成功 () 或失敗 ()  (宏) ，判斷成功或失敗。</span><span class="sxs-lookup"><span data-stu-id="235a2-134">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="235a2-135">備註</span><span class="sxs-lookup"><span data-stu-id="235a2-135">Remarks</span></span>

<span data-ttu-id="235a2-136">如果您想要指定任何資源限定詞，請在 *限定詞* 參數中傳遞它們。</span><span class="sxs-lookup"><span data-stu-id="235a2-136">If you want to specify any resource qualifiers, then pass them in the *qualifiers* parameter.</span></span> <span data-ttu-id="235a2-137">資源限定詞不是從 *resourceUri* 或 *filePath* 推斷 *而* 來。</span><span class="sxs-lookup"><span data-stu-id="235a2-137">Resource qualifiers are *not* inferred from *resourceUri* nor from *filePath*.</span></span>

<span data-ttu-id="235a2-138">*ResourceUri* (不是 *filePath*) 的檔案名區段會用來做為資源名稱。</span><span class="sxs-lookup"><span data-stu-id="235a2-138">The file name segment of *resourceUri* (not *filePath*) is used as the resource name.</span></span>

## <a name="requirements"></a><span data-ttu-id="235a2-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="235a2-139">Requirements</span></span>



| <span data-ttu-id="235a2-140">需求</span><span class="sxs-lookup"><span data-stu-id="235a2-140">Requirement</span></span> | <span data-ttu-id="235a2-141">值</span><span class="sxs-lookup"><span data-stu-id="235a2-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="235a2-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="235a2-142">Minimum supported client</span></span><br/> | <span data-ttu-id="235a2-143">Windows 10， \[ 僅限1803版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="235a2-143">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="235a2-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="235a2-144">Minimum supported server</span></span><br/> | <span data-ttu-id="235a2-145">\[僅限 Windows Server desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="235a2-145">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="235a2-146">標頭</span><span class="sxs-lookup"><span data-stu-id="235a2-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="235a2-147"><dt>MrmResourceIndexer。h</dt></span><span class="sxs-lookup"><span data-stu-id="235a2-147"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="235a2-148">程式庫</span><span class="sxs-lookup"><span data-stu-id="235a2-148">Library</span></span><br/>                  | <dl> <span data-ttu-id="235a2-149"><dt>Mrmsupport .lib</dt></span><span class="sxs-lookup"><span data-stu-id="235a2-149"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="235a2-150">DLL</span><span class="sxs-lookup"><span data-stu-id="235a2-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="235a2-151"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="235a2-151"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="235a2-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="235a2-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="235a2-153">套件資源索引 (PRI) API 和自訂建置系統</span><span class="sxs-lookup"><span data-stu-id="235a2-153">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 


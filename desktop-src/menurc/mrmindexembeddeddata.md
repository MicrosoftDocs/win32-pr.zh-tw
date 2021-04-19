---
title: 'MrmIndexEmbeddedData 函式 (MrmResourceIndexer) '
description: 編制屬於 UWP 應用程式的單一 embeddeddata 資源的索引。
ms.assetid: 4DA37CF9-43B6-44EE-8A10-DBD4510D7885
keywords:
- MrmIndexEmbeddedData 函式功能表與其他資源
topic_type:
- apiref
api_name:
- MrmIndexEmbeddedData
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 308d08e0e125e7919ad3eb32e6cba2184356fce5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966907"
---
# <a name="mrmindexembeddeddata-function"></a><span data-ttu-id="7f23b-104">MrmIndexEmbeddedData 函式</span><span class="sxs-lookup"><span data-stu-id="7f23b-104">MrmIndexEmbeddedData function</span></span>

<span data-ttu-id="7f23b-105">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="7f23b-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="7f23b-106">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="7f23b-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="7f23b-107">編制屬於 UWP 應用程式的單一 **embeddeddata** 資源的索引。</span><span class="sxs-lookup"><span data-stu-id="7f23b-107">Indexes a single **embeddeddata** resource belonging to a UWP app.</span></span> <span data-ttu-id="7f23b-108">接受明確 (，但) 資源限定詞的選擇性清單。</span><span class="sxs-lookup"><span data-stu-id="7f23b-108">Takes an explicit (but optional) list of resource qualifiers.</span></span> <span data-ttu-id="7f23b-109">如需詳細資訊，以及如何使用這些 Api 的案例式逐步解說，請參閱 [封裝資源索引 (PRI) api 和自訂群組建系統](/windows/uwp/app-resources/pri-apis-custom-build-systems)。</span><span class="sxs-lookup"><span data-stu-id="7f23b-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="7f23b-110">語法</span><span class="sxs-lookup"><span data-stu-id="7f23b-110">Syntax</span></span>


```C++
HRESULT HRESULT MrmIndexEmbeddedData(
  _In_           MrmResourceIndexerHandle indexer,
  _In_           PCWSTR                   resourceUri,
  _In_     const BYTE                     *embeddedData,
  _In_           ULONG                    embeddedDataSize,
  _In_opt_       PCWSTR                   qualifiers
);
```



## <a name="parameters"></a><span data-ttu-id="7f23b-111">參數</span><span class="sxs-lookup"><span data-stu-id="7f23b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f23b-112">*索引子* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7f23b-112">*indexer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f23b-113">類型： **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span><span class="sxs-lookup"><span data-stu-id="7f23b-113">Type: **[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span></span>

<span data-ttu-id="7f23b-114">識別將為資源檔編制索引之資源索引子的控制碼。</span><span class="sxs-lookup"><span data-stu-id="7f23b-114">A handle identifying the resource indexer that will index the resource file.</span></span>

</dd> <dt>

<span data-ttu-id="7f23b-115">*resourceUri* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7f23b-115">*resourceUri* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f23b-116">類型： **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="7f23b-116">Type: **PCWSTR**</span></span>

<span data-ttu-id="7f23b-117">要指派給資源的資源 URI。</span><span class="sxs-lookup"><span data-stu-id="7f23b-117">The resource URI to assign to the resource.</span></span> <span data-ttu-id="7f23b-118">當您稍後從此資源索引子產生 PRI 檔案時，會使用此路徑做為此資源的資源對應子樹名稱。</span><span class="sxs-lookup"><span data-stu-id="7f23b-118">The path will be used as the resource map subtree name for this resource when you later generate a PRI file from this resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="7f23b-119">*embeddedData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7f23b-119">*embeddedData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f23b-120">類型： \**CONST BYTE \** _</span><span class="sxs-lookup"><span data-stu-id="7f23b-120">Type: \**const BYTE\** _</span></span>

<span data-ttu-id="7f23b-121">您想要編制索引之資源的資料指標。</span><span class="sxs-lookup"><span data-stu-id="7f23b-121">A pointer to the data of the resource that you want to index.</span></span>

</dd> <dt>

<span data-ttu-id="7f23b-122">_embeddedDataSize \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7f23b-122">_embeddedDataSize\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f23b-123">類型： **ULONG**</span><span class="sxs-lookup"><span data-stu-id="7f23b-123">Type: **ULONG**</span></span>

<span data-ttu-id="7f23b-124">*EmbeddedData* 所指向之資料的大小。</span><span class="sxs-lookup"><span data-stu-id="7f23b-124">The size of the data pointed to by *embeddedData*.</span></span>

</dd> <dt>

<span data-ttu-id="7f23b-125">*限定詞* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="7f23b-125">*qualifiers* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7f23b-126">類型： **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="7f23b-126">Type: **PCWSTR**</span></span>

<span data-ttu-id="7f23b-127">選擇性的資源限定詞清單，例如 L "language-en-us \_ scale-100 \_ 對比-標準"。</span><span class="sxs-lookup"><span data-stu-id="7f23b-127">An optional list of resource qualifiers, for example L"language-en-US\_scale-100\_contrast-standard".</span></span> <span data-ttu-id="7f23b-128">空字串或 **nullptr** 表示中立的資源。</span><span class="sxs-lookup"><span data-stu-id="7f23b-128">An empty string or **nullptr** indicates a neutral resource.</span></span> <span data-ttu-id="7f23b-129">系統 *不* 會從 *resourceUri* 推斷資源限定詞。</span><span class="sxs-lookup"><span data-stu-id="7f23b-129">Resource qualifiers are *not* inferred from *resourceUri*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f23b-130">傳回值</span><span class="sxs-lookup"><span data-stu-id="7f23b-130">Return value</span></span>

<span data-ttu-id="7f23b-131">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="7f23b-131">Type: **HRESULT**</span></span>

<span data-ttu-id="7f23b-132">如果函式 \_ 成功，則為 [正常]，否則為其他值。</span><span class="sxs-lookup"><span data-stu-id="7f23b-132">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="7f23b-133">使用 winerror.h 中定義的成功 () 或失敗 ()  (宏) ，判斷成功或失敗。</span><span class="sxs-lookup"><span data-stu-id="7f23b-133">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f23b-134">備註</span><span class="sxs-lookup"><span data-stu-id="7f23b-134">Remarks</span></span>

<span data-ttu-id="7f23b-135">如果您想要指定任何資源限定詞，請在 *限定詞* 參數中傳遞它們。</span><span class="sxs-lookup"><span data-stu-id="7f23b-135">If you want to specify any resource qualifiers, then pass them in the *qualifiers* parameter.</span></span> <span data-ttu-id="7f23b-136">系統 *不* 會從 *resourceUri* 推斷資源限定詞。</span><span class="sxs-lookup"><span data-stu-id="7f23b-136">Resource qualifiers are *not* inferred from *resourceUri*.</span></span>

<span data-ttu-id="7f23b-137">使用 *resourceUri* 的檔案名區段做為資源名稱。</span><span class="sxs-lookup"><span data-stu-id="7f23b-137">The file name segment of *resourceUri* is used as the resource name.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f23b-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="7f23b-138">Requirements</span></span>



| <span data-ttu-id="7f23b-139">需求</span><span class="sxs-lookup"><span data-stu-id="7f23b-139">Requirement</span></span> | <span data-ttu-id="7f23b-140">值</span><span class="sxs-lookup"><span data-stu-id="7f23b-140">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f23b-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7f23b-141">Minimum supported client</span></span><br/> | <span data-ttu-id="7f23b-142">Windows 10， \[ 僅限1803版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7f23b-142">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="7f23b-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7f23b-143">Minimum supported server</span></span><br/> | <span data-ttu-id="7f23b-144">\[僅限 Windows Server desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7f23b-144">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7f23b-145">標頭</span><span class="sxs-lookup"><span data-stu-id="7f23b-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f23b-146"><dt>MrmResourceIndexer。h</dt></span><span class="sxs-lookup"><span data-stu-id="7f23b-146"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="7f23b-147">程式庫</span><span class="sxs-lookup"><span data-stu-id="7f23b-147">Library</span></span><br/>                  | <dl> <span data-ttu-id="7f23b-148"><dt>Mrmsupport .lib</dt></span><span class="sxs-lookup"><span data-stu-id="7f23b-148"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="7f23b-149">DLL</span><span class="sxs-lookup"><span data-stu-id="7f23b-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7f23b-150"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f23b-150"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="7f23b-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7f23b-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f23b-152">套件資源索引 (PRI) API 和自訂建置系統</span><span class="sxs-lookup"><span data-stu-id="7f23b-152">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

